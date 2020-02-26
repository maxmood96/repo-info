## `python:2-stretch`

```console
$ docker pull python@sha256:41cb3074907a76649e3058fa8d8fa5db1b7b7c8d36b1e3e73b8e84dbc5de7c43
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

### `python:2-stretch` - linux; amd64

```console
$ docker pull python@sha256:dac9c74d67d0cf758e3c7e888c6afd53986ef3c53c39f744582f6ff2cfa18b8e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **361.2 MB (361221601 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42da91c0e9e54e4649e2cade06eb413ce2e97667b6aa6c96b48c772ecfe5c882`
-	Default Command: `["python2"]`

```dockerfile
# Wed, 26 Feb 2020 00:41:14 GMT
ADD file:08c5ab7c53526da155d6be40a9795fc08afc9f47bd333c096e90185fe9fab2b1 in / 
# Wed, 26 Feb 2020 00:41:14 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:17:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:17:19 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 01:17:41 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:18:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 14:34:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 14:34:38 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 17:29:06 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 26 Feb 2020 17:29:13 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		tk-dev 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 17:29:13 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Wed, 26 Feb 2020 17:29:13 GMT
ENV PYTHON_VERSION=2.7.17
# Wed, 26 Feb 2020 17:36:32 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Wed, 26 Feb 2020 17:36:32 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Wed, 26 Feb 2020 17:36:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Wed, 26 Feb 2020 17:36:33 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Wed, 26 Feb 2020 17:36:38 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 26 Feb 2020 17:36:44 GMT
RUN pip install --no-cache-dir virtualenv
# Wed, 26 Feb 2020 17:36:44 GMT
CMD ["python2"]
```

-	Layers:
	-	`sha256:c0c53f743a403d45480d026864d9611d6eb898e897d60c13ae854ad453d462a4`  
		Last Modified: Wed, 26 Feb 2020 00:47:05 GMT  
		Size: 45.4 MB (45375932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66997431d390aecfd02e57222c9b5752d314a4508de82c9b43c66812c3434ed4`  
		Last Modified: Wed, 26 Feb 2020 01:23:37 GMT  
		Size: 10.8 MB (10797283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ea865e2909f355d736daef9076ecda63b3075c6267b858d9eaaf2e3966fc0d2`  
		Last Modified: Wed, 26 Feb 2020 01:23:36 GMT  
		Size: 4.3 MB (4340193 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:584bf23912b71bbd038602cb98cf5207cb2183a8b7b49fa4b16fa2018e09f508`  
		Last Modified: Wed, 26 Feb 2020 01:23:52 GMT  
		Size: 50.1 MB (50070212 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c4c73959f29d362478996015b71e5f4ba5360b835ec71c2435ff03f4d3f3112`  
		Last Modified: Wed, 26 Feb 2020 01:24:38 GMT  
		Size: 214.9 MB (214895058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fbadce1e9bc9bf3d6b6f0fdb909439580abd3b1d4797627540bcfb121187343`  
		Last Modified: Wed, 26 Feb 2020 17:51:18 GMT  
		Size: 5.7 MB (5747319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdd6c12ca42b124673d4a6797e229a091008d67208491f51461b5bc04e7fc355`  
		Last Modified: Wed, 26 Feb 2020 17:51:22 GMT  
		Size: 17.0 MB (17042903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6552f72366f11532fe7b78434d4e3afaa64994a29b309aab275574932454b149`  
		Last Modified: Wed, 26 Feb 2020 17:51:17 GMT  
		Size: 1.9 MB (1888291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa915aaa05ff50480bea15193aee47200ab165455c9875aed0306e8a0f40ee0e`  
		Last Modified: Wed, 26 Feb 2020 17:51:18 GMT  
		Size: 11.1 MB (11064410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:2-stretch` - linux; arm variant v5

```console
$ docker pull python@sha256:a27b7cd34022975da6b4108af035fdbd42e5d11d344050554f3b768c65cc50aa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **340.5 MB (340535503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6be29eee087fd78b3f2b302d5501347a2a44800a21f912800829114deabf31c8`
-	Default Command: `["python2"]`

```dockerfile
# Wed, 26 Feb 2020 00:53:01 GMT
ADD file:5ed8e2bc0bf117a359d81b052913e99f6139d0b36e5798d75392429effd5afd3 in / 
# Wed, 26 Feb 2020 00:53:06 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 03:54:05 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:54:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 03:55:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:58:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 07:33:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 07:33:12 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 09:28:29 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 26 Feb 2020 09:28:45 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		tk-dev 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 09:28:46 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Wed, 26 Feb 2020 09:28:46 GMT
ENV PYTHON_VERSION=2.7.17
# Wed, 26 Feb 2020 09:37:43 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Wed, 26 Feb 2020 09:37:44 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Wed, 26 Feb 2020 09:37:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Wed, 26 Feb 2020 09:37:46 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Wed, 26 Feb 2020 09:37:58 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 26 Feb 2020 09:38:10 GMT
RUN pip install --no-cache-dir virtualenv
# Wed, 26 Feb 2020 09:38:11 GMT
CMD ["python2"]
```

-	Layers:
	-	`sha256:3294d23573097fea5f2d79377bc86444ebf83e4bed50a8a6c62b7aa8637dd7fe`  
		Last Modified: Wed, 26 Feb 2020 01:03:12 GMT  
		Size: 44.1 MB (44066613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a952c5ec5882944f0e3977bb3d28960e53c97b7c4985863a7fd5b7c33b3a309b`  
		Last Modified: Wed, 26 Feb 2020 04:05:26 GMT  
		Size: 9.9 MB (9866766 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82b6614c3a732af22df2caaa8ead40737dc17a198f0ee9d057e6e53fee7f9f12`  
		Last Modified: Wed, 26 Feb 2020 04:05:23 GMT  
		Size: 4.2 MB (4159221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e937dfdc173e40ef43eb533cf95b65a5abf2a454023815cd5f3e958f46aa659`  
		Last Modified: Wed, 26 Feb 2020 04:05:50 GMT  
		Size: 48.3 MB (48282222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e683e4c4afc21fdc4903fc67d305c05658b8dc2baa598d3e201de1f811ed98c4`  
		Last Modified: Wed, 26 Feb 2020 04:07:00 GMT  
		Size: 203.1 MB (203065511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1bafb0350d353a713c1385c48185617a14fc0fad4c441a02a3816241ab0acf7`  
		Last Modified: Wed, 26 Feb 2020 09:55:14 GMT  
		Size: 5.5 MB (5531322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4dff6d34daa3d936664ca379f5c80d69f0f7ee28ed7337734e3b6601fcbafb62`  
		Last Modified: Wed, 26 Feb 2020 09:55:18 GMT  
		Size: 16.0 MB (16015985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de5a5096f1408fb09f3287055350397d580476ae67fe4eac9a20d1a2df61a9f4`  
		Last Modified: Wed, 26 Feb 2020 09:55:14 GMT  
		Size: 1.9 MB (1888490 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b2b8f638a71d676bb96f70d25c72e0f94a783fe3a7eb84c336da53f41f33cc`  
		Last Modified: Wed, 26 Feb 2020 09:55:14 GMT  
		Size: 7.7 MB (7659373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:2-stretch` - linux; arm variant v7

```console
$ docker pull python@sha256:f33f91e8896bf43e5f6eb9b4f01f8c895c5b869d16cfdeaaeb38d89505c7d032
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **327.8 MB (327839686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1429162073b58429936f957012ea6a876fdfc959dfcc95e0bf556a0b69d16883`
-	Default Command: `["python2"]`

```dockerfile
# Wed, 26 Feb 2020 00:59:40 GMT
ADD file:6497e2f777f4487d9221931005a8b4b81c021442a769b581e223cf30c81ff553 in / 
# Wed, 26 Feb 2020 00:59:53 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 02:27:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 02:27:16 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 02:28:08 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 02:30:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 09:57:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 09:57:23 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 12:03:50 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 26 Feb 2020 12:04:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		tk-dev 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 12:04:03 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Wed, 26 Feb 2020 12:04:03 GMT
ENV PYTHON_VERSION=2.7.17
# Wed, 26 Feb 2020 12:12:20 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Wed, 26 Feb 2020 12:12:21 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Wed, 26 Feb 2020 12:12:22 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Wed, 26 Feb 2020 12:12:24 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Wed, 26 Feb 2020 12:12:36 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 26 Feb 2020 12:12:49 GMT
RUN pip install --no-cache-dir virtualenv
# Wed, 26 Feb 2020 12:12:51 GMT
CMD ["python2"]
```

-	Layers:
	-	`sha256:2478a2ed882cb5fbb5e4e92c9f580da9ca52f5fc78b8bb439ecbf3ac18023caa`  
		Last Modified: Wed, 26 Feb 2020 01:11:29 GMT  
		Size: 42.1 MB (42100335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c541086e0dffa72464d4077dcc60504a1c08a73ecec554c159269786ba08fed`  
		Last Modified: Wed, 26 Feb 2020 02:37:24 GMT  
		Size: 9.5 MB (9498391 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edf0f97b070f73118badb36d21af3459f8317d4ac6d45aec680092cc962f1c47`  
		Last Modified: Wed, 26 Feb 2020 02:37:23 GMT  
		Size: 3.9 MB (3918781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d620eb05d9fd9184b8f200537b866a27af44aa6d7ef4dd6113bf1b51421d4795`  
		Last Modified: Wed, 26 Feb 2020 02:37:45 GMT  
		Size: 46.4 MB (46391794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7f6d10893167716e03df782cfd3f378f099999787bc15655d27fd06cc601e46`  
		Last Modified: Wed, 26 Feb 2020 02:38:40 GMT  
		Size: 195.5 MB (195548773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d715ba5db926cb5d3357ebd1c8da922a31cdf6952fb79abae4e76defe9d6de68`  
		Last Modified: Wed, 26 Feb 2020 12:30:49 GMT  
		Size: 5.2 MB (5196944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10c44243cb198dbc35eb268c4bf85b7e6d19f5580c7fd0fe9ab33ed890eaa401`  
		Last Modified: Wed, 26 Feb 2020 12:30:54 GMT  
		Size: 15.6 MB (15639406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:002344d09aef3e4909a420736dac0dbbc812d8f48f015cdfeed6817e8a880f22`  
		Last Modified: Wed, 26 Feb 2020 12:30:48 GMT  
		Size: 1.9 MB (1888497 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0470bf0a3cf5bf2d862696d36166d2be20fd67f0b4e85ffd0b8246946d3af568`  
		Last Modified: Wed, 26 Feb 2020 12:30:50 GMT  
		Size: 7.7 MB (7656765 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:2-stretch` - linux; arm64 variant v8

```console
$ docker pull python@sha256:526fd902c35632be8429b9cf15c0e88bc70dfda6670e4effbafe13b9678e14b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **342.2 MB (342224747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e3e4864b23540edad36c4a4d9dea57ae9274d28ce55e1d78e5d380b2031a8a3`
-	Default Command: `["python2"]`

```dockerfile
# Wed, 26 Feb 2020 00:50:03 GMT
ADD file:c82c7dc82c2eb3b50218c35e1b848f707b134d2df957f57125408f69aaeb9b96 in / 
# Wed, 26 Feb 2020 00:50:15 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 03:59:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 03:59:21 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 04:00:04 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 04:02:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 06:47:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 06:47:45 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 18:14:38 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 26 Feb 2020 18:14:52 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		tk-dev 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 18:14:53 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Wed, 26 Feb 2020 18:14:54 GMT
ENV PYTHON_VERSION=2.7.17
# Wed, 26 Feb 2020 18:22:57 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Wed, 26 Feb 2020 18:22:58 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Wed, 26 Feb 2020 18:22:59 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Wed, 26 Feb 2020 18:23:00 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Wed, 26 Feb 2020 18:23:10 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 26 Feb 2020 18:23:21 GMT
RUN pip install --no-cache-dir virtualenv
# Wed, 26 Feb 2020 18:23:22 GMT
CMD ["python2"]
```

-	Layers:
	-	`sha256:668c278237ef972312df4979c8fb1a927b38db5da09f094ae4fcc84a061dedf8`  
		Last Modified: Wed, 26 Feb 2020 00:58:30 GMT  
		Size: 43.2 MB (43158146 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b41cac09012800692bd13a1238260bfb293c18c7864536c494809f2983ad770`  
		Last Modified: Wed, 26 Feb 2020 04:08:32 GMT  
		Size: 9.7 MB (9748511 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:094b353938273b0bbc576a8a80a232614ca2d9bfe48769641eee7055f3db6a5e`  
		Last Modified: Wed, 26 Feb 2020 04:08:31 GMT  
		Size: 4.1 MB (4094435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95fba2538bf9e06bc84462d53d1effc13ecb38f026a6bc0df91cb9da3ffc0fb1`  
		Last Modified: Wed, 26 Feb 2020 04:08:53 GMT  
		Size: 48.0 MB (48024341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1c9497c36a170d2db3389cf07b65d1cb488f7af1bf0f048be8458986d60567`  
		Last Modified: Wed, 26 Feb 2020 04:09:50 GMT  
		Size: 202.3 MB (202280174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95ea131701612e2d503a7397051ed89b42adcc4773ff9866b760017d6b1971fe`  
		Last Modified: Wed, 26 Feb 2020 18:40:51 GMT  
		Size: 5.5 MB (5501322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fc188fd0d9695357f67d1950e4fd3a3428b9a4824a58b67d09557faffed30e1`  
		Last Modified: Wed, 26 Feb 2020 18:40:56 GMT  
		Size: 16.5 MB (16465160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1ea88f30c1c3f60b07c4c7d6e2660c3efd11c47ba7c8bd30e94d1d4f739106`  
		Last Modified: Wed, 26 Feb 2020 18:40:50 GMT  
		Size: 1.9 MB (1888521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8bbf687c8839e1df63b13de8ef3a0517221b6e4e2f563f1f08259e59ab1c69ea`  
		Last Modified: Wed, 26 Feb 2020 18:40:52 GMT  
		Size: 11.1 MB (11064137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:2-stretch` - linux; 386

```console
$ docker pull python@sha256:b1cede5d298c642c75d67f979e8d9c54ab2c2a5b33a01fd4c7f00149b7b9e5e0
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **364.6 MB (364605565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ab6aeafee31f03b5112e867ca752dcf90eb6be043bd0a5eaa4a03e507033df5`
-	Default Command: `["python2"]`

```dockerfile
# Wed, 26 Feb 2020 00:35:22 GMT
ADD file:f57292acaae4c3d7e8b3217b28f9efb27faef1c4e08ca95f4a25d1302355fb51 in / 
# Wed, 26 Feb 2020 00:35:23 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 01:23:23 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:23:30 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 01:24:00 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 01:25:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 11:25:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 11:25:04 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 15:31:18 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 26 Feb 2020 15:31:26 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		tk-dev 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 15:31:26 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Wed, 26 Feb 2020 15:31:26 GMT
ENV PYTHON_VERSION=2.7.17
# Wed, 26 Feb 2020 15:38:28 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Wed, 26 Feb 2020 15:38:28 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Wed, 26 Feb 2020 15:38:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Wed, 26 Feb 2020 15:38:28 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Wed, 26 Feb 2020 15:38:34 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 26 Feb 2020 15:38:40 GMT
RUN pip install --no-cache-dir virtualenv
# Wed, 26 Feb 2020 15:38:41 GMT
CMD ["python2"]
```

-	Layers:
	-	`sha256:ef83ea0a858b11598fe63ce7d80a401ebb47c746763b35564bd712f013cb961f`  
		Last Modified: Wed, 26 Feb 2020 00:41:45 GMT  
		Size: 46.1 MB (46095035 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa60bcba0a57a2662cae84d0bd1cc3e9baa383c9a1589cecbb68b4e65d231ce2`  
		Last Modified: Wed, 26 Feb 2020 01:31:18 GMT  
		Size: 10.8 MB (10818060 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a172f4142e9968e299cb42a03c7124d1456062e69197d3d50c972ca924d0d107`  
		Last Modified: Wed, 26 Feb 2020 01:31:15 GMT  
		Size: 4.6 MB (4561448 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a8d299990640c71bf2446b454c0391fe405a3390c363cf97eab4f8fe9cd57e6`  
		Last Modified: Wed, 26 Feb 2020 01:31:40 GMT  
		Size: 51.6 MB (51603478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e7d83f116087dbb03cd1e9e8196a8ccb100d15756be529f99a9e7779dff81e8`  
		Last Modified: Wed, 26 Feb 2020 01:32:40 GMT  
		Size: 220.0 MB (219969557 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d337048f4589fb336f45c9f9c52210c5f147d178c582a7a9468cbd234733771`  
		Last Modified: Wed, 26 Feb 2020 15:52:14 GMT  
		Size: 6.1 MB (6062074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f12fbdaaa65aafe46b14372af8cde9957ccabea360fb42c469b6f9649ca7639`  
		Last Modified: Wed, 26 Feb 2020 15:52:17 GMT  
		Size: 15.9 MB (15944837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:438ef3498a4daeebc3a70a19c611f9d76e3a60c526a811e5a8852acbef1124af`  
		Last Modified: Wed, 26 Feb 2020 15:52:13 GMT  
		Size: 1.9 MB (1888335 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9753390261ce9d0b16546af6f6452b6da734c4499a648f2c6a8d4ffee2ed672`  
		Last Modified: Wed, 26 Feb 2020 15:52:15 GMT  
		Size: 7.7 MB (7662741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:2-stretch` - linux; ppc64le

```console
$ docker pull python@sha256:affc6223c74eb58596f1598569db49525723a861e69f245e7d043d7794128fd8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **356.3 MB (356293187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4d6f453d015efc3bc7a9fbd8528c56252d462ef64fe9f37754715e9a56d606`
-	Default Command: `["python2"]`

```dockerfile
# Wed, 26 Feb 2020 01:36:21 GMT
ADD file:734d2a25bec5d510e72f822b21a5ef5786a928c6cb933209a04c6358fd600b67 in / 
# Wed, 26 Feb 2020 01:36:29 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 08:30:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 08:31:25 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 08:33:19 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 08:44:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 19:30:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 19:31:00 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 20:27:42 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 26 Feb 2020 20:28:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		tk-dev 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 20:28:24 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Wed, 26 Feb 2020 20:28:25 GMT
ENV PYTHON_VERSION=2.7.17
# Wed, 26 Feb 2020 20:35:23 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Wed, 26 Feb 2020 20:35:28 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Wed, 26 Feb 2020 20:35:34 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Wed, 26 Feb 2020 20:35:38 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Wed, 26 Feb 2020 20:35:56 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 26 Feb 2020 20:36:12 GMT
RUN pip install --no-cache-dir virtualenv
# Wed, 26 Feb 2020 20:36:17 GMT
CMD ["python2"]
```

-	Layers:
	-	`sha256:3a8babb46b416d2208716bc29bc3e805dd074b943418fc44ac89d66e363bc68a`  
		Last Modified: Wed, 26 Feb 2020 02:03:30 GMT  
		Size: 45.6 MB (45647081 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b58107739cb9bc4ee26b798057c5699d3917b41fdd5074d870c116173ef2b88d`  
		Last Modified: Wed, 26 Feb 2020 08:54:46 GMT  
		Size: 10.0 MB (10002548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2a9dde531080020a5aecc53631e693820a9b6870602303e1eec2d17f6591e1`  
		Last Modified: Wed, 26 Feb 2020 08:54:43 GMT  
		Size: 4.3 MB (4296749 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38d0a325b030abc66d25e8263d0ed1e03cd7c249159491c7681e444b6cf13fd8`  
		Last Modified: Wed, 26 Feb 2020 08:55:34 GMT  
		Size: 50.1 MB (50083192 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d28ed0e030df85f26e512a53e9ab53fea54fb890f9659448426dacc339ef6838`  
		Last Modified: Wed, 26 Feb 2020 08:57:33 GMT  
		Size: 210.5 MB (210509590 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7273e541031d2017d70ffbc13ce607edeee7055f99f7b19f7a26354524df2df9`  
		Last Modified: Wed, 26 Feb 2020 20:41:29 GMT  
		Size: 5.8 MB (5781849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1743218ec131c9689fcedfbf9d7f77a1e58cc8645a756b79f980232d594626`  
		Last Modified: Wed, 26 Feb 2020 20:41:32 GMT  
		Size: 17.0 MB (17018669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e909dc11aa4567b94f4fe2c232f62ce41ba67f2142dae9d16b8485558505e15`  
		Last Modified: Wed, 26 Feb 2020 20:41:28 GMT  
		Size: 1.9 MB (1888528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d18929f8f80cfe9d22358a0d38bcaf3d594f064f89d35b70c722539cfdc398c7`  
		Last Modified: Wed, 26 Feb 2020 20:41:30 GMT  
		Size: 11.1 MB (11064981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:2-stretch` - linux; s390x

```console
$ docker pull python@sha256:fbbd0c415e2be181874309314454e1d9254bb482c7b073d7eebb8eeaaba4e462
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **350.6 MB (350594913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:151c4fcc6517278e4e01cc1d3124708e0404f8ee69b0a006972785e895f3122d`
-	Default Command: `["python2"]`

```dockerfile
# Wed, 26 Feb 2020 00:44:30 GMT
ADD file:bb76ab55808bcd0567a32c3d7328d5c1719147f0f723a4aa574872eb8f12b4d4 in / 
# Wed, 26 Feb 2020 00:44:38 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 04:42:02 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 04:42:11 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 26 Feb 2020 04:42:56 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		bzr 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 04:44:53 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 09:54:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 09:54:48 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 10:27:52 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 26 Feb 2020 10:27:58 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		tk-dev 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 10:27:59 GMT
ENV GPG_KEY=C01E1CAD5EA2C4F0B8E3571504C367C218ADD4FF
# Wed, 26 Feb 2020 10:27:59 GMT
ENV PYTHON_VERSION=2.7.17
# Wed, 26 Feb 2020 10:32:21 GMT
RUN set -ex 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--enable-unicode=ucs4 	&& make -j "$(nproc)" 		PROFILE_TASK='-m test.regrtest --pgo 			test_array 			test_base64 			test_binascii 			test_binhex 			test_binop 			test_bytes 			test_c_locale_coercion 			test_class 			test_cmath 			test_codecs 			test_compile 			test_complex 			test_csv 			test_decimal 			test_dict 			test_float 			test_fstring 			test_hashlib 			test_io 			test_iter 			test_json 			test_long 			test_math 			test_memoryview 			test_pickle 			test_re 			test_set 			test_slice 			test_struct 			test_threading 			test_time 			test_traceback 			test_unicode 		' 	&& make install 	&& ldconfig 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python2 --version
# Wed, 26 Feb 2020 10:32:22 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Wed, 26 Feb 2020 10:32:22 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Wed, 26 Feb 2020 10:32:23 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Wed, 26 Feb 2020 10:32:28 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 26 Feb 2020 10:32:35 GMT
RUN pip install --no-cache-dir virtualenv
# Wed, 26 Feb 2020 10:32:37 GMT
CMD ["python2"]
```

-	Layers:
	-	`sha256:a2baf8ed1bce68a4f36469f3537f12b9e5bebc860ab4aac0954714901595c575`  
		Last Modified: Wed, 26 Feb 2020 00:49:08 GMT  
		Size: 45.2 MB (45232848 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a58b9c529db9ec73f2bb8ba3f678b389c4df7bdb3ff1083ebf516aee839533b2`  
		Last Modified: Wed, 26 Feb 2020 04:49:17 GMT  
		Size: 10.3 MB (10325927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d9d2deeb51ba62efa7f9206911520eae29fdd6a401851f5f400f881ef0fbc8`  
		Last Modified: Wed, 26 Feb 2020 04:49:16 GMT  
		Size: 4.4 MB (4372671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:945d494eee6f349916e86f798c51b0ee9e6c3e769f797eb840c23ce5857bed41`  
		Last Modified: Wed, 26 Feb 2020 04:49:30 GMT  
		Size: 50.5 MB (50500268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32172ae2ff63a2a428c16879a62e110ef908cf42a10b9fc15275a5bc9bb8707c`  
		Last Modified: Wed, 26 Feb 2020 04:50:00 GMT  
		Size: 206.9 MB (206915719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abaaf357f838ca23d5336d1e34bf81f121a5f0ff720b313ebb112560def4bc7c`  
		Last Modified: Wed, 26 Feb 2020 10:36:14 GMT  
		Size: 5.8 MB (5811961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2660ca31396e6ccfc9877ee60b61e4415eff0af2143487946803ba74e8124702`  
		Last Modified: Wed, 26 Feb 2020 10:36:16 GMT  
		Size: 17.9 MB (17889381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ab3c87312e600d2c9e8bf4bdd0e5b6d9851993fbba1248d62f315a633c444f`  
		Last Modified: Wed, 26 Feb 2020 10:36:19 GMT  
		Size: 1.9 MB (1888516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce174d9775b9c10fb1c463e20db844721caddfdb944b7eefc9e75f2c2dd9b20`  
		Last Modified: Wed, 26 Feb 2020 10:36:29 GMT  
		Size: 7.7 MB (7657622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
