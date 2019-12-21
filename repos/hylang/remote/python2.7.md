## `hylang:python2.7`

```console
$ docker pull hylang@sha256:23c0b5e076291d2b38b836d5ec8a714950d0171eb0ff6ba9fcd3d3e2d16dc342
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x
	-	windows version 10.0.17763.914; amd64
	-	windows version 10.0.17134.1130; amd64
	-	windows version 10.0.14393.3384; amd64

### `hylang:python2.7` - linux; amd64

```console
$ docker pull hylang@sha256:5d632b0c2bec92e291ab9233ca1ca63a9eaa1ac2dba5d20c329fd5ac6223dd14
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52457641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d6fbd16c3a9227f97c8cb30def7b3888274b80720c29bfb8f5b8b055c27e2f3`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 22 Nov 2019 14:55:09 GMT
ADD file:bc8179c87c8dbb3d962bed1801f99e7c860ff03797cde6ad19b107d43b973ada in / 
# Fri, 22 Nov 2019 14:55:10 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 05:38:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Nov 2019 05:38:51 GMT
ENV LANG=C.UTF-8
# Sat, 23 Nov 2019 07:35:28 GMT
ENV PYTHONIOENCODING=UTF-8
# Sat, 23 Nov 2019 07:35:36 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 07:35:37 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Sat, 23 Nov 2019 07:35:37 GMT
ENV PYTHON_VERSION=2.7.17
# Sat, 23 Nov 2019 07:38:22 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Sat, 23 Nov 2019 07:38:23 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 23 Nov 2019 07:38:23 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 23 Nov 2019 07:38:23 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 23 Nov 2019 07:38:38 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 23 Nov 2019 07:38:38 GMT
CMD ["python2"]
# Sat, 23 Nov 2019 23:31:09 GMT
ENV HY_VERSION=0.17.0
# Sat, 23 Nov 2019 23:31:14 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 23 Nov 2019 23:31:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:000eee12ec04cc914bf96e8f5dee7767510c2aca3816af6078bd9fbe3150920c`  
		Last Modified: Fri, 22 Nov 2019 15:02:49 GMT  
		Size: 27.1 MB (27092654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a1fc2539e7f0834bc769585a1233b308c2cf553c516ddf65b479ee4af96e75b`  
		Last Modified: Sat, 23 Nov 2019 07:49:39 GMT  
		Size: 2.7 MB (2749061 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21142e4357ee97d32f836b9b23e107b837dd61ad9cbe88e42fa9ed529fafb647`  
		Last Modified: Sat, 23 Nov 2019 07:49:44 GMT  
		Size: 18.0 MB (17996463 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c09cd5028ba1b854297602aecb31068b7b0daf25b7fd557e1bbcb9987c52071`  
		Last Modified: Sat, 23 Nov 2019 07:49:40 GMT  
		Size: 2.2 MB (2153650 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a72c72802c7d571d1da3487d1cd25460963bb669d79ac8264f5d7c35b4fdab`  
		Last Modified: Sat, 23 Nov 2019 23:33:16 GMT  
		Size: 2.5 MB (2465813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python2.7` - linux; arm variant v5

```console
$ docker pull hylang@sha256:32c3f05d809dbcc2feeaed6ee2eb3d558152b336c1d2ad3a69a913038e6276ff
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50330300 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2888e719fe7862a1d3faa163bee095fa3c2ae0142051aedceaa5f07e0a4db63b`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 22 Nov 2019 12:13:54 GMT
ADD file:94ed554e445cf749e10644dfa0d836103c120a6ea388bf6dc9f18f7c6b2f095a in / 
# Fri, 22 Nov 2019 12:13:56 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 22:28:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2019 22:28:54 GMT
ENV LANG=C.UTF-8
# Sat, 23 Nov 2019 00:57:58 GMT
ENV PYTHONIOENCODING=UTF-8
# Sat, 23 Nov 2019 00:58:12 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 00:58:13 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Sat, 23 Nov 2019 00:58:14 GMT
ENV PYTHON_VERSION=2.7.17
# Sat, 21 Dec 2019 00:08:07 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Sat, 21 Dec 2019 00:08:09 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 21 Dec 2019 00:08:09 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 21 Dec 2019 00:08:10 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 21 Dec 2019 00:08:37 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 21 Dec 2019 00:08:38 GMT
CMD ["python2"]
# Sat, 21 Dec 2019 02:11:56 GMT
ENV HY_VERSION=0.17.0
# Sat, 21 Dec 2019 02:12:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 21 Dec 2019 02:12:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:45ae7e8aa5bfd9e1b0db11d7fa5a56a8af11b69fc56707d763f89aa2c61b7e8f`  
		Last Modified: Fri, 22 Nov 2019 12:22:20 GMT  
		Size: 24.8 MB (24829480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbda3418e99393e2edf005ae9fe0e0b589e274bbff50a1cf836858e9dfb42c03`  
		Last Modified: Sat, 23 Nov 2019 01:19:22 GMT  
		Size: 2.4 MB (2448177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d234d2e84e6769a5fd0ab4f0784d68cd6b2a02def0ec61d132474086b2e8776`  
		Last Modified: Sat, 21 Dec 2019 00:39:22 GMT  
		Size: 18.4 MB (18429630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5ff63f9e9688725638f2ba27a9532f8e08ab64b044d59b4e0302b3db6ddba3`  
		Last Modified: Sat, 21 Dec 2019 00:39:10 GMT  
		Size: 2.2 MB (2154641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb3b3c947f6357885d04e5b595fdf0a5463457971ce285d060a24dc4aee9dc86`  
		Last Modified: Sat, 21 Dec 2019 02:14:43 GMT  
		Size: 2.5 MB (2468372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python2.7` - linux; arm variant v7

```console
$ docker pull hylang@sha256:bb4fe8f3dc9da1e4b23350eb4c5e02f0f0f894bd7ef1ebf6e8d017df7b14ef16
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47834651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a72fed9acca5bef883e4a60dab80aebd06cab190dfdd7e54293f5162204a5167`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 22 Nov 2019 13:22:45 GMT
ADD file:85cf6081b7d1948b250d1b3749a65e2561cddafb7cd748db6b7b7420a376a48f in / 
# Fri, 22 Nov 2019 13:22:46 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:59:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Nov 2019 00:59:42 GMT
ENV LANG=C.UTF-8
# Sat, 23 Nov 2019 04:02:55 GMT
ENV PYTHONIOENCODING=UTF-8
# Sat, 23 Nov 2019 04:04:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 04:04:12 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Sat, 23 Nov 2019 04:04:14 GMT
ENV PYTHON_VERSION=2.7.17
# Sat, 21 Dec 2019 02:21:34 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Sat, 21 Dec 2019 02:21:39 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 21 Dec 2019 02:21:42 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 21 Dec 2019 02:21:44 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 21 Dec 2019 02:22:24 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 21 Dec 2019 02:22:25 GMT
CMD ["python2"]
# Sat, 21 Dec 2019 04:09:37 GMT
ENV HY_VERSION=0.17.0
# Sat, 21 Dec 2019 04:09:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 21 Dec 2019 04:09:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cf3d03fb414460b7542c20e72fe29a83f08d22fd2c7a8cab1834eec2976e4b2`  
		Last Modified: Fri, 22 Nov 2019 13:33:25 GMT  
		Size: 22.7 MB (22699053 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fea9f5f4a66f0e9335c5e1b76fdbecbb77641d7c04b77df34ed69c82708e7b25`  
		Last Modified: Sat, 23 Nov 2019 04:26:22 GMT  
		Size: 2.3 MB (2346075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd76b426c83f379150ed60ebeba6cebf867e840330b27c408acb3dbfe452c42e`  
		Last Modified: Sat, 21 Dec 2019 03:10:14 GMT  
		Size: 18.2 MB (18166210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfa1ff58625a224606bf4435effd6fc8ae9f95f4a666fd51d0a00f1e27a56d22`  
		Last Modified: Sat, 21 Dec 2019 03:10:09 GMT  
		Size: 2.2 MB (2155000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1df1172ec6fede40ec9d186f454b20994475eeeba0df6f24105a7b6bcbe5d59`  
		Last Modified: Sat, 21 Dec 2019 04:14:43 GMT  
		Size: 2.5 MB (2468313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python2.7` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:48594cac0de0384bfae20eba0a6ca798f4618de80ec83847fe70811c58f25966
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52424437 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61fc72cb963b2e27c18e311c245eeb414e70091fdf5b012684df8a38f9310d48`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 22 Nov 2019 13:41:59 GMT
ADD file:69e0891ef62c74ec5e9bae38f8d2770ab2f0d7ea0d3cf1dc85875763be0b10b7 in / 
# Fri, 22 Nov 2019 13:42:02 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 08:17:42 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Nov 2019 08:17:45 GMT
ENV LANG=C.UTF-8
# Sat, 23 Nov 2019 11:34:10 GMT
ENV PYTHONIOENCODING=UTF-8
# Sat, 23 Nov 2019 11:34:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 11:34:23 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Sat, 23 Nov 2019 11:34:24 GMT
ENV PYTHON_VERSION=2.7.17
# Sat, 21 Dec 2019 01:01:46 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Sat, 21 Dec 2019 01:01:51 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 21 Dec 2019 01:01:52 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 21 Dec 2019 01:01:53 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 21 Dec 2019 01:02:18 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 21 Dec 2019 01:02:26 GMT
CMD ["python2"]
# Sat, 21 Dec 2019 05:25:50 GMT
ENV HY_VERSION=0.17.0
# Sat, 21 Dec 2019 05:26:08 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 21 Dec 2019 05:26:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a4f3dd4087f9309af4187e5dda90741441f057da59c2270598e16aa8019b0ca2`  
		Last Modified: Fri, 22 Nov 2019 13:49:50 GMT  
		Size: 25.9 MB (25850802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e06ddc179ed33667eb5f4d8685be38f54766e646c8e38fe40a360036a771ef43`  
		Last Modified: Sat, 23 Nov 2019 11:59:43 GMT  
		Size: 2.6 MB (2622191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b0cee0d06a8e284ee4e0129388d51475ef33d8663e7ad683b0e6f16e4d2332`  
		Last Modified: Sat, 21 Dec 2019 01:47:18 GMT  
		Size: 19.3 MB (19327885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f44262c04164ecbe16038f6a2d117f8655285b4f1bfcc079c43253ffb27c72fb`  
		Last Modified: Sat, 21 Dec 2019 01:47:12 GMT  
		Size: 2.2 MB (2155327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f502103cebd6c1efd662075fb449282ac9175863ec5a6a9f39e39de7d59e709`  
		Last Modified: Sat, 21 Dec 2019 05:31:40 GMT  
		Size: 2.5 MB (2468232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python2.7` - linux; 386

```console
$ docker pull hylang@sha256:643d1149efcbad80b53e960773dbab89c3d27f5808dba20c765367f45747a4a3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53744200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7de6f98a272d85fe94126800b54100492d3584d0e2a3bb9264d496c8b0f676d7`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 22 Nov 2019 16:50:19 GMT
ADD file:68f0911eb53ffc655e6a641b4acfb0670c2fd84c7dc34b0128735f0478532a6b in / 
# Fri, 22 Nov 2019 16:50:19 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 09:04:45 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Nov 2019 09:04:45 GMT
ENV LANG=C.UTF-8
# Sat, 23 Nov 2019 11:56:36 GMT
ENV PYTHONIOENCODING=UTF-8
# Sat, 23 Nov 2019 11:56:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 11:56:47 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Sat, 23 Nov 2019 11:56:48 GMT
ENV PYTHON_VERSION=2.7.17
# Sat, 21 Dec 2019 04:23:40 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Sat, 21 Dec 2019 04:23:40 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 21 Dec 2019 04:23:40 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 21 Dec 2019 04:23:41 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 21 Dec 2019 04:23:54 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 21 Dec 2019 04:23:54 GMT
CMD ["python2"]
# Sat, 21 Dec 2019 05:57:11 GMT
ENV HY_VERSION=0.17.0
# Sat, 21 Dec 2019 05:57:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 21 Dec 2019 05:57:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ce9b44038a207698571bb0cc0b950ee2a3608cb09b2b20712b353a54ae619111`  
		Last Modified: Fri, 22 Nov 2019 16:58:27 GMT  
		Size: 27.7 MB (27746760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f29a00829c83c1160bcf06026fb81d493430148411271e317735a19029daf89c`  
		Last Modified: Sat, 23 Nov 2019 12:13:08 GMT  
		Size: 2.8 MB (2762476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffa9ada5156979750457bfe57baa8e87437a41586d51169ba9b4a23a8707da8c`  
		Last Modified: Sat, 21 Dec 2019 04:55:07 GMT  
		Size: 18.6 MB (18612725 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:560ad982655ccf9b6f95e0e3f6c77b900be9d73ff3822e07fe8075e4eb84d1c2`  
		Last Modified: Sat, 21 Dec 2019 04:55:03 GMT  
		Size: 2.2 MB (2154383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e704a0ee9a84f0d5a0f2feca4badf9f9aff8cd238e785bd18b54eb033c2c0560`  
		Last Modified: Sat, 21 Dec 2019 06:00:01 GMT  
		Size: 2.5 MB (2467856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python2.7` - linux; ppc64le

```console
$ docker pull hylang@sha256:f1d93a2309abefd6c01000e9d3699cab43a0336d1fe549d229e00620d8e6fe2a
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.9 MB (56878305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ef0ab7a07860d77bb83d658a8429991ca055a425b8805a92ba98e6accdaa9ce`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 22 Nov 2019 14:55:33 GMT
ADD file:56ee7f5cc8715d22f4efb9ec5b1c24fac7fdf8f6dc9c07c45625c4f89bdccac3 in / 
# Fri, 22 Nov 2019 14:55:37 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 09:04:07 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Nov 2019 09:04:10 GMT
ENV LANG=C.UTF-8
# Sat, 23 Nov 2019 11:55:23 GMT
ENV PYTHONIOENCODING=UTF-8
# Sat, 23 Nov 2019 11:55:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 11:55:44 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Sat, 23 Nov 2019 11:55:49 GMT
ENV PYTHON_VERSION=2.7.17
# Sat, 23 Nov 2019 12:01:13 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Sat, 23 Nov 2019 12:01:18 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 23 Nov 2019 12:01:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 23 Nov 2019 12:01:22 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 23 Nov 2019 12:01:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 23 Nov 2019 12:01:50 GMT
CMD ["python2"]
# Sat, 23 Nov 2019 17:11:33 GMT
ENV HY_VERSION=0.17.0
# Sat, 23 Nov 2019 17:11:52 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 23 Nov 2019 17:11:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e190211f5678d77388755410611e5e6a755e195e7a1096473c675edc074a2389`  
		Last Modified: Fri, 22 Nov 2019 15:04:10 GMT  
		Size: 30.5 MB (30517327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e38c6e9b5232166f984300526c0651df12b59b39311ade6f29f881dbce4910d9`  
		Last Modified: Sat, 23 Nov 2019 12:20:13 GMT  
		Size: 2.9 MB (2871635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7246faa7e9ac7268b03a7a57688d1d9a35feb8d5bf99ee9fec485ee42de877e8`  
		Last Modified: Sat, 23 Nov 2019 12:20:17 GMT  
		Size: 18.9 MB (18868285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d6bd234efedc68e03de1f46caf388bfb572334e09b9744abb8a5df5ae6bdf43`  
		Last Modified: Sat, 23 Nov 2019 12:20:13 GMT  
		Size: 2.2 MB (2154517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af463cd2a14f2e49dd97464eb5cfcd3c2cf98efdbaedfb533d8ee0d288ae8c89`  
		Last Modified: Sat, 23 Nov 2019 17:17:26 GMT  
		Size: 2.5 MB (2466541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python2.7` - linux; s390x

```console
$ docker pull hylang@sha256:eca02106725542ca6aecad77f3555c74b999c518860d967b5daae4501a6a619c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51078046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61d5f6017ef83df1c60f5ace5db719fa268b20d84c1ab52bebad690986a8ce96`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 16 Oct 2019 23:42:48 GMT
ADD file:4bf0501a845ff525e4edaa88b6641f72b2f2df61d0ebf4ef03222cf79feee915 in / 
# Wed, 16 Oct 2019 23:42:48 GMT
CMD ["bash"]
# Thu, 17 Oct 2019 08:39:37 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Oct 2019 08:39:37 GMT
ENV LANG=C.UTF-8
# Thu, 17 Oct 2019 10:23:46 GMT
ENV PYTHONIOENCODING=UTF-8
# Thu, 17 Oct 2019 10:23:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		netbase 	&& rm -rf /var/lib/apt/lists/*
# Thu, 17 Oct 2019 10:23:58 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Thu, 24 Oct 2019 00:50:31 GMT
ENV PYTHON_VERSION=2.7.17
# Fri, 15 Nov 2019 03:48:33 GMT
RUN set -ex 		&& savedAptMark="$(apt-mark showmanual)" 	&& apt-get update && apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		libbz2-dev 		libc6-dev 		libdb-dev 		libgdbm-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		wget 		xz-utils 		zlib1g-dev 		$(command -v gpg > /dev/null || echo 'gnupg dirmngr') 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 	&& make install 	&& ldconfig 		&& apt-mark auto '.*' > /dev/null 	&& apt-mark manual $savedAptMark 	&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	&& apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false 	&& rm -rf /var/lib/apt/lists/* 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Fri, 15 Nov 2019 03:48:33 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Fri, 15 Nov 2019 03:48:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Fri, 15 Nov 2019 03:48:34 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Fri, 15 Nov 2019 03:48:49 GMT
RUN set -ex; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 15 Nov 2019 03:48:50 GMT
CMD ["python2"]
# Fri, 15 Nov 2019 04:20:52 GMT
ENV HY_VERSION=0.17.0
# Fri, 15 Nov 2019 04:20:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 15 Nov 2019 04:20:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ad1fb1a183ba14bd1dc12e9413867f1b9b9687c6ba30209f34777d4cee3bcba8`  
		Last Modified: Wed, 16 Oct 2019 23:48:34 GMT  
		Size: 25.7 MB (25718301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac417b901c23ad41a28964017401e79dc68e938807d2d2808b560b02a2e22d3d`  
		Last Modified: Thu, 17 Oct 2019 10:39:56 GMT  
		Size: 2.4 MB (2442023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03904ebf4332813688dcfced1ceb548454cd90016a99bea98a97113acde891aa`  
		Last Modified: Fri, 15 Nov 2019 04:02:11 GMT  
		Size: 18.3 MB (18298836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fa13ca45ee4d52d3c80dab65492f3369bc76354cef568055ea9164e25f8684`  
		Last Modified: Fri, 15 Nov 2019 04:02:06 GMT  
		Size: 2.2 MB (2153293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d2b50adc96bed52bccbeff13c73b3a9103e5a662405e66bab734d3702cee4ae`  
		Last Modified: Fri, 15 Nov 2019 04:24:31 GMT  
		Size: 2.5 MB (2465593 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python2.7` - windows version 10.0.17763.914; amd64

```console
$ docker pull hylang@sha256:ae4e28f6a397d3f676ca7044758db4283d80038244bce36fe4c4e4ef9e38c517
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2265083999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1020ba689dc38c212cf614118d82b4d683ea6a21848cc94fb46991c2a615da6d`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 15 Sep 2018 09:10:26 GMT
RUN Apply image 1809-RTM-amd64
# Fri, 29 Nov 2019 04:34:15 GMT
RUN Install update 1809-amd64
# Tue, 10 Dec 2019 21:34:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 01:10:01 GMT
ENV PYTHON_VERSION=2.7.17
# Wed, 11 Dec 2019 01:10:02 GMT
ENV PYTHON_RELEASE=2.7.17
# Wed, 11 Dec 2019 01:11:59 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}.amd64.msi' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.msi'; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'python.msi', 			'/quiet', 			'/qn', 			'TARGETDIR=C:\Python', 			'ALLUSERS=1', 			'ADDLOCAL=DefaultFeature,Extensions,TclTk,Tools,PrependPath' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.msi -Force; 		Write-Host 'Complete.'
# Wed, 11 Dec 2019 01:12:01 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Wed, 11 Dec 2019 01:12:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Wed, 11 Dec 2019 01:12:04 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Wed, 11 Dec 2019 01:13:09 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2019 01:13:36 GMT
RUN pip install --no-cache-dir virtualenv
# Wed, 11 Dec 2019 01:13:37 GMT
CMD ["python"]
# Wed, 11 Dec 2019 01:42:43 GMT
ENV HY_VERSION=0.17.0
# Wed, 11 Dec 2019 01:43:19 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 11 Dec 2019 01:43:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:65014b3c312172f10bd6701a063f9b5aaf9a916c2d2cb843d406a6f77ded3f8d`  
		Last Modified: Tue, 13 Nov 2018 18:50:17 GMT  
		Size: 1.5 GB (1534685324 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:faf31ee0aa3d3c60a38dd03c7554d632065cef50eab052ef1444590786249d07`  
		Size: 681.6 MB (681618026 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:e147f14e0d6a9cbd5261162dea8f3aac7a34db5d9f6a587a9aac6b88722a2da4`  
		Last Modified: Tue, 10 Dec 2019 22:07:34 GMT  
		Size: 1.2 KB (1211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e149e4386bb4e3ef4905fba057c6de2e777c90363739d26403684d35647fa62`  
		Last Modified: Wed, 11 Dec 2019 01:21:31 GMT  
		Size: 1.2 KB (1159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63fbc4f495276c58d77356bafa24bf14bb038dacef91110c764ddd2c68e60475`  
		Last Modified: Wed, 11 Dec 2019 01:21:30 GMT  
		Size: 1.2 KB (1186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b834aea9069dae57ddf9692b9128c582add906d47aaf68548b698b3c50621b2f`  
		Last Modified: Wed, 11 Dec 2019 01:21:52 GMT  
		Size: 38.9 MB (38937795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2691f02b84e7e134c4c5f542bae1d79121d716db61a3bc2968ae4e985b32e6ec`  
		Last Modified: Wed, 11 Dec 2019 01:21:29 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09013b363839e63e6de1f6b87708d08a2a93aa6fbb142168882be83de78b40e9`  
		Last Modified: Wed, 11 Dec 2019 01:21:26 GMT  
		Size: 1.2 KB (1191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:274b0016f46ca64020ffca139291e6cd1a838b081630353f436adf905d697ee1`  
		Last Modified: Wed, 11 Dec 2019 01:21:26 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0849fb1bad3788fc9bc13ecba31d08ccaa9442077137960b66329785e46443c`  
		Last Modified: Wed, 11 Dec 2019 01:21:50 GMT  
		Size: 5.0 MB (4974605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5c4b55641e7e1383fa4e862c0c84775701a6ec16b5798c5b40314eae00b0a41`  
		Last Modified: Wed, 11 Dec 2019 01:21:28 GMT  
		Size: 3.8 MB (3779861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d033a1b453e66df13cc14cd4b0641f7153534e35fec5e1ea7cce1929729c38f2`  
		Last Modified: Wed, 11 Dec 2019 01:21:26 GMT  
		Size: 1.2 KB (1182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bbc5b4e7ac2758ef746bcc2b53ef3cd75e7a39ef66a749d5c578753e9de9eaa`  
		Last Modified: Wed, 11 Dec 2019 13:21:40 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78d90290aa273d5d1641659ec5154b8ba85a938c061636147a6c2e1b82e2523c`  
		Last Modified: Wed, 11 Dec 2019 13:21:42 GMT  
		Size: 1.1 MB (1077714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cfb5eb5f59e50ee5ef032a2c828d0d8e3897425deed3de15163cec432eb48d3`  
		Last Modified: Wed, 11 Dec 2019 13:21:40 GMT  
		Size: 1.2 KB (1184 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python2.7` - windows version 10.0.17134.1130; amd64

```console
$ docker pull hylang@sha256:e4dda2241ea1c5e81e552661f7f2fe830252b1140b00a5dbe9ef0b20323dd8d5
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 GB (2404747837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42ba5793eaa9ede254b30a69b9274ac78fe1667e4c4497101f4c85cbc6f9a446`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 12 Apr 2018 09:20:54 GMT
RUN Apply image 1803-RTM-amd64
# Sat, 09 Nov 2019 08:10:48 GMT
RUN Install update 1803-amd64
# Wed, 13 Nov 2019 13:25:11 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Nov 2019 15:18:22 GMT
ENV PYTHON_VERSION=2.7.17
# Wed, 13 Nov 2019 15:18:23 GMT
ENV PYTHON_RELEASE=2.7.17
# Wed, 13 Nov 2019 15:20:34 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}.amd64.msi' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.msi'; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'python.msi', 			'/quiet', 			'/qn', 			'TARGETDIR=C:\Python', 			'ALLUSERS=1', 			'ADDLOCAL=DefaultFeature,Extensions,TclTk,Tools,PrependPath' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.msi -Force; 		Write-Host 'Complete.'
# Wed, 13 Nov 2019 15:20:35 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Wed, 13 Nov 2019 15:20:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Wed, 13 Nov 2019 15:20:38 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Wed, 13 Nov 2019 15:21:54 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 13 Nov 2019 15:22:30 GMT
RUN pip install --no-cache-dir virtualenv
# Wed, 13 Nov 2019 15:22:31 GMT
CMD ["python"]
# Fri, 15 Nov 2019 03:24:38 GMT
ENV HY_VERSION=0.17.0
# Fri, 15 Nov 2019 03:25:26 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Fri, 15 Nov 2019 03:25:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d9e8b01179bfc94a5bdb1810fbd76b999aa52016001ace2d3a4c4bc7065a9601`  
		Last Modified: Tue, 18 Sep 2018 22:43:55 GMT  
		Size: 1.7 GB (1659688273 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:3eb83143ff4b7dafaf8aee4e558c4743488812347fac8581e8b2f61b8e5d06e0`  
		Size: 696.1 MB (696065307 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:680d3df54e320ad0b3c81d3cef7c520d3507801f5428387ec9aa1b2a25cc79bc`  
		Last Modified: Thu, 14 Nov 2019 23:40:46 GMT  
		Size: 1.2 KB (1206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b952b62076c9d0c106f914ee1846ecfa2f98d552c5c492a328f9fd8c5f12bf0`  
		Last Modified: Fri, 15 Nov 2019 02:29:24 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b41b20f27c7f2a06d0eee48b4037aa9a941dc8367a5fa7ed80d0186f491ff784`  
		Last Modified: Fri, 15 Nov 2019 02:29:23 GMT  
		Size: 1.2 KB (1202 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b11f1ed79ac185f15fb2e8f7ac945590e8072aafd955bc31af704d954a7b0e8`  
		Last Modified: Fri, 15 Nov 2019 02:29:46 GMT  
		Size: 39.2 MB (39217532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ed7ed8c7f3e756d14885165b880d20d22cec128819a698fd88b27715de45806`  
		Last Modified: Fri, 15 Nov 2019 02:29:23 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e830ba90f2af3a55aeaebe1a5f547c043f7f63432c171b085ac54b56cc0ceaa6`  
		Last Modified: Fri, 15 Nov 2019 02:29:20 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:781d83143c7d8f857ad62f5c52e03b69b54395e9072d5986950c72222a8b7bbb`  
		Last Modified: Fri, 15 Nov 2019 02:29:20 GMT  
		Size: 1.2 KB (1183 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c335776d632530b8d57f4a8495c86324c45e5b8ebb6146d22bac8230726c1da2`  
		Last Modified: Fri, 15 Nov 2019 02:29:34 GMT  
		Size: 4.9 MB (4949775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34be8c626c291c74f26473bbe487e01e6dd143a4d1ae64995b5f42c7bd688a4`  
		Last Modified: Fri, 15 Nov 2019 02:29:21 GMT  
		Size: 3.7 MB (3747610 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8050722d860d7ffd360c246e5beb4fb07f672fb70512975897b90cfe5bf5f4d`  
		Last Modified: Fri, 15 Nov 2019 02:29:21 GMT  
		Size: 1.2 KB (1180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f7ee9812621a8bb4cbd37f1a1123cf36569bd6c6f8dc04b128444340ac4a4c3`  
		Last Modified: Fri, 15 Nov 2019 03:32:52 GMT  
		Size: 1.2 KB (1171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bf6242e1a4b4769ea993f22ef40c7e672520c38e734fa632f1647c110a3397a`  
		Last Modified: Fri, 15 Nov 2019 03:32:54 GMT  
		Size: 1.1 MB (1068683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b038c7996cc7bb68b9c082577822245d1ffe2e91475064ea040974b48f44a273`  
		Last Modified: Fri, 15 Nov 2019 03:32:52 GMT  
		Size: 1.2 KB (1176 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python2.7` - windows version 10.0.14393.3384; amd64

```console
$ docker pull hylang@sha256:9019e42fdddbfda628aa908bfae157e1d2fe772b23c09415e80880cf013c31fa
```

-	Docker Version: 18.03.1-ee-4
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.8 GB (5787174067 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3de094ab8e7458c24355e672706ddd1a889ae1189d8ea1a0feeb94959db850`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sat, 19 Nov 2016 17:05:00 GMT
RUN Apply image 1607-RTM-amd64
# Wed, 27 Nov 2019 14:43:00 GMT
RUN Install update ltsc2016-amd64
# Wed, 11 Dec 2019 00:35:49 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Dec 2019 01:03:56 GMT
ENV PYTHON_VERSION=2.7.17
# Wed, 11 Dec 2019 01:03:58 GMT
ENV PYTHON_RELEASE=2.7.17
# Wed, 11 Dec 2019 01:06:27 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}.amd64.msi' -f $env:PYTHON_RELEASE, $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.msi'; 		Write-Host 'Installing ...'; 	Start-Process msiexec -Wait 		-ArgumentList @( 			'/i', 			'python.msi', 			'/quiet', 			'/qn', 			'TARGETDIR=C:\Python', 			'ALLUSERS=1', 			'ADDLOCAL=DefaultFeature,Extensions,TclTk,Tools,PrependPath' 		); 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.msi -Force; 		Write-Host 'Complete.'
# Wed, 11 Dec 2019 01:06:29 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Wed, 11 Dec 2019 01:06:31 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Wed, 11 Dec 2019 01:06:32 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Wed, 11 Dec 2019 01:08:31 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing pip=={0} ...' -f $env:PYTHON_PIP_VERSION); 	python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip=={0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 11 Dec 2019 01:09:39 GMT
RUN pip install --no-cache-dir virtualenv
# Wed, 11 Dec 2019 01:09:41 GMT
CMD ["python"]
# Wed, 11 Dec 2019 01:43:38 GMT
ENV HY_VERSION=0.17.0
# Wed, 11 Dec 2019 01:44:58 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 11 Dec 2019 01:45:00 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3889bb8d808bbae6fa5a33e07093e65c31371bcf9e4c38c21be6b9af52ad1548`  
		Last Modified: Tue, 18 Sep 2018 20:20:50 GMT  
		Size: 4.1 GB (4069985900 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:55d044e60c8959ce88aee467913bb11827c1ec057a2fd108a293e274dbd74f1d`  
		Size: 1.7 GB (1652717978 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:530e4240d4261ce165890648d1df6230dc4f9ce5df2e6cf9f0d5876694c3d4f0`  
		Last Modified: Wed, 11 Dec 2019 01:14:39 GMT  
		Size: 1.2 KB (1208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b0fc5ac64f92b1725178e8a81bf7c984989e70bcd1dd8f35aa1018cfc462da7`  
		Last Modified: Wed, 11 Dec 2019 01:20:34 GMT  
		Size: 1.2 KB (1203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91f9350657917fdc4491f23a8efb1bf94834a13e5c4a218fd05bf003a79fb350`  
		Last Modified: Wed, 11 Dec 2019 01:20:31 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8519793d32284fec35cb6975fe742fdafc521ef0ce25db012db0560a8670a860`  
		Last Modified: Wed, 11 Dec 2019 01:20:56 GMT  
		Size: 39.7 MB (39665149 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b772691d1b71be25bb80a2bb2d1ab747979f975d716bfac502802e3b1e84fe7`  
		Last Modified: Wed, 11 Dec 2019 01:20:32 GMT  
		Size: 1.2 KB (1185 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5bf765289fdc9959f788ba53990776f7684bce5679b5eb9db4d537dc6459ad5`  
		Last Modified: Wed, 11 Dec 2019 01:20:28 GMT  
		Size: 1.2 KB (1188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15ffe4a93e5cde7661ee3a6471e2e4f2bb6e45eab43d6ed88932337979b491f1`  
		Last Modified: Wed, 11 Dec 2019 01:20:28 GMT  
		Size: 1.2 KB (1177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a5ef19b9966b41728d6fe2f6cab9f87b157d0c4e2e3979bb45e23cd92b24cdd`  
		Last Modified: Wed, 11 Dec 2019 01:20:43 GMT  
		Size: 10.0 MB (9978917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2fca74f16b84172ba7f24cb6adb91662adc5910d988c953971a2da575c58c1d`  
		Last Modified: Wed, 11 Dec 2019 01:20:31 GMT  
		Size: 8.8 MB (8759784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23af693f219d1cb74719f5e27f2c5e8feb7055c6c43dd1df99b886edd47e1295`  
		Last Modified: Wed, 11 Dec 2019 01:20:28 GMT  
		Size: 1.2 KB (1165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db518a8d50d28be1ee7e42788a5ebf59f4a4d74d38f9a8d6b8c76d242827db1a`  
		Last Modified: Wed, 11 Dec 2019 13:22:22 GMT  
		Size: 1.2 KB (1167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c750792986e691c7dd62f907197280d77b57571b412f8e95e97807f4f151a35b`  
		Last Modified: Wed, 11 Dec 2019 13:22:25 GMT  
		Size: 6.1 MB (6055648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:214638fcdf9fe4430c1fed20ca904909f0ee64986db65569d0d93929534553ed`  
		Last Modified: Wed, 11 Dec 2019 13:22:22 GMT  
		Size: 1.2 KB (1210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
