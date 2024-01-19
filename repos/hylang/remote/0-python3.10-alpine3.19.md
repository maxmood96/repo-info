## `hylang:0-python3.10-alpine3.19`

```console
$ docker pull hylang@sha256:82122034cfc98281f0aee0519826d83aeda95d1625a174551aeff834840c070f
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

### `hylang:0-python3.10-alpine3.19` - linux; amd64

```console
$ docker pull hylang@sha256:b0bc92ed53221c669791a61ae4307f8368c471256df826231b5547a4a4729f31
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23463497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ddfe5732695f1a16c7637b90a07baac361fe38d533e27f0cf70d1b15a37d20`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 08 Dec 2023 01:20:49 GMT
ADD file:1f4eb46669b5b6275af19eb7471a6899a61c276aa7d925b8ae99310b14b75b92 in / 
# Fri, 08 Dec 2023 01:20:49 GMT
CMD ["/bin/sh"]
# Mon, 18 Dec 2023 19:30:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Dec 2023 19:30:20 GMT
ENV LANG=C.UTF-8
# Mon, 18 Dec 2023 19:30:20 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 18 Dec 2023 19:30:20 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Mon, 18 Dec 2023 19:30:20 GMT
ENV PYTHON_VERSION=3.10.13
# Mon, 18 Dec 2023 19:30:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 18 Dec 2023 19:30:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 18 Dec 2023 19:30:20 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 18 Dec 2023 19:30:20 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Mon, 18 Dec 2023 19:30:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Mon, 18 Dec 2023 19:30:20 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Mon, 18 Dec 2023 19:30:20 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 18 Dec 2023 19:30:20 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:661ff4d9561e3fd050929ee5097067c34bafc523ee60f5294a37fd08056a73ca`  
		Last Modified: Fri, 08 Dec 2023 01:21:10 GMT  
		Size: 3.4 MB (3408480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44cda88cd45dc00d3349d343b46e92f0d55daa059d276f3ecf860c174bbedf81`  
		Last Modified: Sat, 09 Dec 2023 01:44:02 GMT  
		Size: 621.7 KB (621692 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48c91875651ed05bd18926dbdaf7dcad60d34762cd2ab2ab80954031cdf851f7`  
		Last Modified: Sat, 09 Dec 2023 01:46:37 GMT  
		Size: 12.2 MB (12213745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a3bf9ff3965616e6c4ba6917c0cb75281baf44e209eea3b48253f7e94b76058`  
		Last Modified: Sat, 09 Dec 2023 01:46:35 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:890dbb47e8a99bac4818f59228bb2bf039e5c3b11c3bf855bab7eb4f7793a29e`  
		Last Modified: Fri, 19 Jan 2024 00:12:12 GMT  
		Size: 3.1 MB (3080736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464c589193f5f26b3385356e9361c5e062ea5faa1c7f1cd25797a0ea90a55460`  
		Last Modified: Fri, 19 Jan 2024 00:51:00 GMT  
		Size: 4.1 MB (4138602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:cd050e78a1e0c2e83310c1b6ad893cc7351633a61350c8c7dafe472b1377ae9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **872.7 KB (872702 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2db66ac72331c87fe17c57589014ed81f43503352fb4107a2363c6e5811d4556`

```dockerfile
```

-	Layers:
	-	`sha256:cfe1dff6f602a38392dc4422be5e6c7c7340c7c718f7ec552d207df505a13bdf`  
		Last Modified: Fri, 19 Jan 2024 00:51:00 GMT  
		Size: 862.2 KB (862249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d72e3b17809cb4bff3ce0ed758e9d2dd7e9146914b7e95c6e15aeda3a6456cf`  
		Last Modified: Fri, 19 Jan 2024 00:51:00 GMT  
		Size: 10.5 KB (10453 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.19` - linux; arm variant v6

```console
$ docker pull hylang@sha256:600ccbf2ef30b6ac5d43c2c72599a9948ac52a1e57f6823c6ab6537e1d518b56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.9 MB (22873044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04450c76d82430b12e4f684674fb3c2de7e8534b2c61675a4f83812f7f3780d7`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 08 Dec 2023 01:49:15 GMT
ADD file:d43ed267a41631ce0e5a4ef5aac821a75300a83f85ecb6259f5616852f89e989 in / 
# Fri, 08 Dec 2023 01:49:15 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 09:55:38 GMT
ENV LANG=C.UTF-8
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_VERSION=3.10.13
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0803c38384d9fd0f9afaec8fd13d267547b660dcd46bb92a3d63c5d76e78b04c`  
		Last Modified: Fri, 08 Dec 2023 01:49:33 GMT  
		Size: 3.2 MB (3165143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c42929f9f4a31e1902cdf6c4235d3aa6d6778d097653c2630af687f5e8e809d3`  
		Last Modified: Fri, 08 Dec 2023 23:46:53 GMT  
		Size: 622.9 KB (622903 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4ba8899ab076b5547690900a8c24e26834e5d9ecc5221382f130c30f621996d`  
		Last Modified: Fri, 08 Dec 2023 23:48:04 GMT  
		Size: 11.9 MB (11865298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b918890bde921cccc5776942cffe8f237ae527ae1898538d025b3b29acbf19f7`  
		Last Modified: Fri, 08 Dec 2023 23:48:01 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a59bbdee93d8e05d07b44017459ca41f8666fbf1281bee35bd63e06147c4269`  
		Last Modified: Fri, 08 Dec 2023 23:48:04 GMT  
		Size: 3.1 MB (3080731 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a0d372eec4c2149a0ecb633fc136589955ae32ce3f406209e3c44c7b451452b`  
		Last Modified: Mon, 08 Jan 2024 20:09:40 GMT  
		Size: 4.1 MB (4138728 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:cfaaa64bbb3e91a579f15d389b6bbc6b93877fe6eb94794e723de58cb6a7267e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **10.3 KB (10324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d342352ad373a05fdfe7b2f4221d9d7cb4b8814d63609e31f93663805d7b1ba`

```dockerfile
```

-	Layers:
	-	`sha256:ca4e683b29dee1e6f1c23283294e1df725d722050e22ffbef14a01d7d0c6250b`  
		Last Modified: Mon, 08 Jan 2024 20:09:40 GMT  
		Size: 10.3 KB (10324 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.19` - linux; arm variant v7

```console
$ docker pull hylang@sha256:8f55b5a57f93324312ba89ffcd2512b28263d6b584bb87a70e6185d401278233
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.2 MB (22207130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dbac0258a7c5c69088a0d6e1e35d27e05aaea221f931a58f6c1fcd3a505fa66`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 08 Dec 2023 01:57:20 GMT
ADD file:13b9291053208eec61cd7c97bac2fa154380ad8d10182567763eea3e10c5882f in / 
# Fri, 08 Dec 2023 01:57:20 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 09:55:38 GMT
ENV LANG=C.UTF-8
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_VERSION=3.10.13
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1086c24c41097f090ce847d192c11307e1715eeb563a2cf4f410b2a199ae1942`  
		Last Modified: Fri, 08 Dec 2023 01:57:36 GMT  
		Size: 2.9 MB (2918701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e0196bec49f2a69fdcb2616601ab1de1723d29440f95d478ab8ca13b3fa59c6`  
		Last Modified: Sat, 09 Dec 2023 02:18:07 GMT  
		Size: 621.9 KB (621916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc9b77178c1dd13d21a4fa406af1ba0242eb03f64f97197076ad4d3ea3e07827`  
		Last Modified: Sat, 09 Dec 2023 02:20:35 GMT  
		Size: 11.4 MB (11446639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0086b4ff591270ec14e1c19864e65ea8f7707ac396c91c468315d3d621a4316a`  
		Last Modified: Sat, 09 Dec 2023 02:20:33 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1b2bb1be3c39838b7c128776cc9a08f1d34fceb28bff262112778032c7ad1db`  
		Last Modified: Sat, 09 Dec 2023 02:20:34 GMT  
		Size: 3.1 MB (3080732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:baad67ab32ce1135b1f65aac0a2f0c40e6f797c01048815d8583bd3e1c7da74e`  
		Last Modified: Sat, 06 Jan 2024 04:55:06 GMT  
		Size: 4.1 MB (4138902 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:e44e875dad95ca2725f94f3abc32bddf0f4e05c8fb1a6a86afe7300667577858
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **874.5 KB (874520 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f04a7944b90d2ed46ba865c3fe95e9f354aa303dc3c7f3e545db323b6aed830c`

```dockerfile
```

-	Layers:
	-	`sha256:d95e864a765c4343f4a362025a8b7fa87f6b770ea3008997832532664111eab0`  
		Last Modified: Sat, 06 Jan 2024 04:55:05 GMT  
		Size: 864.8 KB (864781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae86f83807bb083bc6169e6abac0a725040c016b1bb3998eb62ba910bf2832aa`  
		Last Modified: Sat, 06 Jan 2024 04:55:05 GMT  
		Size: 9.7 KB (9739 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:fc3d1e88a03138247cc76672ec657c68495eacb62659e9e5402fcb3810ffe150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23479190 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7820535c3a8183fac6b6761027e6408d73c091ddc836cec7e0d4e182cf43f971`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 08 Dec 2023 01:39:30 GMT
ADD file:8182c73f869a899cf624a59c400acb8226776d15e4d3a0d240a94e65340540d0 in / 
# Fri, 08 Dec 2023 01:39:30 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 09:55:38 GMT
ENV LANG=C.UTF-8
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_VERSION=3.10.13
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c303524923177661067f7eb378c3dd5277088c2676ebd1cd78e68397bb80fdbf`  
		Last Modified: Fri, 08 Dec 2023 01:39:48 GMT  
		Size: 3.3 MB (3347794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e853c0f38ea7ee895b324be2572635fb61172c5bb439c16909ff93c5626bf9e3`  
		Last Modified: Sat, 09 Dec 2023 01:29:58 GMT  
		Size: 624.7 KB (624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e2bf8fadd7561c3865302dcbab4663eb36e0cf6304ff93f509f8805860c96be`  
		Last Modified: Sat, 09 Dec 2023 01:32:33 GMT  
		Size: 12.3 MB (12286950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1ada407d4d2c971c1aebc4674b6a4c646e3eec3d467ba5cdc020425cad06cc7`  
		Last Modified: Sat, 09 Dec 2023 01:32:21 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad274ec315323040018b08f6054c66a02ead755999e2e8e9ac6304f25b7ee5f2`  
		Last Modified: Sat, 09 Dec 2023 01:32:22 GMT  
		Size: 3.1 MB (3080742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cb6a1dcc627f3a5e6f430277b9012d9af02833d526416170f5ee1f3fa7f6906`  
		Last Modified: Sat, 06 Jan 2024 00:38:49 GMT  
		Size: 4.1 MB (4138743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:3c6bc54bc9b828efdeb9c659d7e547cab682a6250a5a697d00580970ed8d8433
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.9 KB (871915 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab98444df4b4c6d6d1dd5706457dacab381814f7c8247fc801c8b0ff8702b4f9`

```dockerfile
```

-	Layers:
	-	`sha256:04fd4c0c92c4ffbdf7755827b3dc7f1616308a46578b85383534d820f4aa3eda`  
		Last Modified: Sat, 06 Jan 2024 00:38:49 GMT  
		Size: 862.3 KB (862260 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ac6e264f38f329a1c565eead6196f5a1b491c2d6c9cafa62c417c1db5193d72`  
		Last Modified: Sat, 06 Jan 2024 00:38:48 GMT  
		Size: 9.7 KB (9655 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.19` - linux; 386

```console
$ docker pull hylang@sha256:f36cee0bdde4984057a004072781acc1fba7c94a864865d4f69e9eaffa3d0f21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.5 MB (23520775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3fd3b69c65458d3111412324f8ed6cb5709752e416a241f3898b7a81c4d32e07`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 08 Dec 2023 01:38:25 GMT
ADD file:bd52540f209ba362654d795d7893669c819d35011a16f9f319301727a33b3bd9 in / 
# Fri, 08 Dec 2023 01:38:25 GMT
CMD ["/bin/sh"]
# Mon, 18 Dec 2023 19:30:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Dec 2023 19:30:20 GMT
ENV LANG=C.UTF-8
# Mon, 18 Dec 2023 19:30:20 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 18 Dec 2023 19:30:20 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Mon, 18 Dec 2023 19:30:20 GMT
ENV PYTHON_VERSION=3.10.13
# Mon, 18 Dec 2023 19:30:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 18 Dec 2023 19:30:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 18 Dec 2023 19:30:20 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 18 Dec 2023 19:30:20 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Mon, 18 Dec 2023 19:30:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Mon, 18 Dec 2023 19:30:20 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Mon, 18 Dec 2023 19:30:20 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 18 Dec 2023 19:30:20 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9acd8b4c9d4385585f74dabb4bc6b3351888710ae37ec5dbd9ea950281b8f9bb`  
		Last Modified: Fri, 08 Dec 2023 01:38:43 GMT  
		Size: 3.2 MB (3244115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee2119bf6dee75c7b7760616d3acb471ec49b73b34ea14f7bc5482840548fad5`  
		Last Modified: Sat, 09 Dec 2023 04:27:59 GMT  
		Size: 622.4 KB (622375 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2e3affd2e5116428aea0dd5dde4f3ca2fb12636470dac20d890dd7c84b6f31`  
		Last Modified: Sat, 09 Dec 2023 04:30:34 GMT  
		Size: 12.4 MB (12434829 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5f06864606374732dfe0f8782c5c191c7d86444c6aa5deb979cb815961a720a`  
		Last Modified: Sat, 09 Dec 2023 04:30:31 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48442c66396bf0b811acfdfefd38dce2a650808ea5db93677d9fc3f1489a1055`  
		Last Modified: Fri, 19 Jan 2024 01:23:50 GMT  
		Size: 3.1 MB (3080721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8d012e25012ce5fd98b9972594709a155ffe5c6dd68d46b9078d6e1966ee73c`  
		Last Modified: Fri, 19 Jan 2024 01:50:50 GMT  
		Size: 4.1 MB (4138495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:44928043cd1b2221054cfad57688201e9c4eece3c3825c0576b5679f892d5577
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **872.6 KB (872610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3afbda5b3edd28d535fb9a08ac036c2c771542722d968c83eb918f689fb6aed`

```dockerfile
```

-	Layers:
	-	`sha256:976cdf437a78dc6a04a4393a64591b627ce1ee82c3b19a07507a37c1f00f155a`  
		Last Modified: Fri, 19 Jan 2024 01:50:50 GMT  
		Size: 862.2 KB (862204 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3eb1c875b854f1b1206f51e5c3cf5cf6f74c3db176db4e861450b475369b219f`  
		Last Modified: Fri, 19 Jan 2024 01:50:50 GMT  
		Size: 10.4 KB (10406 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.19` - linux; ppc64le

```console
$ docker pull hylang@sha256:2536eb4bc0f57d2d059282ab49e2dbaf93e324221f7f075ce95bf5eb06d2fd66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23924125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f40ead0d8c9cf8edb0e3495f41492e51626b57aef1bb33bee6a4dac09800449`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 08 Dec 2023 01:22:51 GMT
ADD file:052421189f8d269382daaaa8beb63c687e4d8ca908c421abdce53bcc627a40b4 in / 
# Fri, 08 Dec 2023 01:22:51 GMT
CMD ["/bin/sh"]
# Mon, 18 Dec 2023 19:30:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 18 Dec 2023 19:30:20 GMT
ENV LANG=C.UTF-8
# Mon, 18 Dec 2023 19:30:20 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 18 Dec 2023 19:30:20 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Mon, 18 Dec 2023 19:30:20 GMT
ENV PYTHON_VERSION=3.10.13
# Mon, 18 Dec 2023 19:30:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Mon, 18 Dec 2023 19:30:20 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 18 Dec 2023 19:30:20 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Mon, 18 Dec 2023 19:30:20 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Mon, 18 Dec 2023 19:30:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/049c52c665e8c5fd1751f942316e0a5c777d304f/public/get-pip.py
# Mon, 18 Dec 2023 19:30:20 GMT
ENV PYTHON_GET_PIP_SHA256=7cfd4bdc4d475ea971f1c0710a5953bcc704d171f83c797b9529d9974502fcc6
# Mon, 18 Dec 2023 19:30:20 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Mon, 18 Dec 2023 19:30:20 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:243ac51c334a47917a84be93e972ee6378987e9b3b917a5a8df29025e161c1f3`  
		Last Modified: Fri, 08 Dec 2023 01:23:14 GMT  
		Size: 3.4 MB (3358233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a081cf452e352600ba7e978072f652f412217d025eb9e6fdee9520f88252831c`  
		Last Modified: Sat, 09 Dec 2023 02:20:52 GMT  
		Size: 625.1 KB (625119 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f125d9957cc32280d2bd14eb3b7488afae667e851a3785d29f2c35a2d4035492`  
		Last Modified: Sat, 09 Dec 2023 02:23:33 GMT  
		Size: 12.7 MB (12720993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7677af67d83c32ed4beb1d0de612fdf0f8b07c3a5e43749872a6c5846623745c`  
		Last Modified: Sat, 09 Dec 2023 02:23:30 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65b3345f81fc7dde1f09719a9a27bbae81b1bcaa13a0627b1a061e19ab414802`  
		Last Modified: Fri, 19 Jan 2024 00:38:44 GMT  
		Size: 3.1 MB (3080712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:416338cfb3ded23390b748ffa4c627c624350e5e4149c8d5a53422935a8f3ae5`  
		Last Modified: Fri, 19 Jan 2024 02:29:31 GMT  
		Size: 4.1 MB (4138825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:5ce4279c54421f2e82e2f2293956c438d8da3577b8694cafca63f21c3d4e9e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **871.2 KB (871188 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c67d4de7779ad65da786fe2a0e8b9f020d5243c5adb14f528baa6131b1b32b5`

```dockerfile
```

-	Layers:
	-	`sha256:67bda344fa48e3f3287d64faa83eef37bc84fb95b357ee8ba66cc8ad9f3c9c94`  
		Last Modified: Fri, 19 Jan 2024 02:29:30 GMT  
		Size: 860.7 KB (860671 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dbb7de9bacbc512b7f655db44478e6714fed17474cfdba16843dbcc3eab41b97`  
		Last Modified: Fri, 19 Jan 2024 02:29:30 GMT  
		Size: 10.5 KB (10517 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.19` - linux; s390x

```console
$ docker pull hylang@sha256:eae3b0b71e017e115617ab8e21e5cfa90227fd201c5b200844a5aff1ade6c9dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23573500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17147b3fcbab10e84124038c843588b82be1b4c6afe4792a62bfba5579160955`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 08 Dec 2023 01:41:50 GMT
ADD file:47e0982fc3ae485c06d46f3c0022afd39ed7ec95fe755c2391e6b0cfcae65dfc in / 
# Fri, 08 Dec 2023 01:41:51 GMT
CMD ["/bin/sh"]
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Dec 2023 09:55:38 GMT
ENV LANG=C.UTF-8
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_VERSION=3.10.13
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Fri, 08 Dec 2023 09:55:38 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Fri, 08 Dec 2023 09:55:38 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 08 Dec 2023 09:55:38 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0fca3ee44ced87b7184bc23390283fdf10cfae0e844a25b785dd11c463815227`  
		Last Modified: Fri, 08 Dec 2023 01:42:30 GMT  
		Size: 3.2 MB (3242332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b44507c21692f6a1dfe3960dcd32b105ed10a012358912cf6e622dd984c44e76`  
		Last Modified: Sat, 09 Dec 2023 00:43:53 GMT  
		Size: 622.9 KB (622924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:865871f2eaf29165dfd7ba5e9387aafbfd336ddbc201ef2054f7fd368e961eda`  
		Last Modified: Sat, 09 Dec 2023 00:45:36 GMT  
		Size: 12.5 MB (12488564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8bc6936aba4baa48357b2eb9a7c1efa827d374483f2d2b4de86bb3ed13aab7b`  
		Last Modified: Sat, 09 Dec 2023 00:45:34 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ecbec11c6f4504879314c1e9787ea41de87df4a228048acc9427f6fe79a167e`  
		Last Modified: Sat, 09 Dec 2023 00:45:35 GMT  
		Size: 3.1 MB (3080695 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7db51bb897c52698bb5c098e0fdade420d1766734fd83e556c03b7e7adb23d`  
		Last Modified: Sat, 06 Jan 2024 00:29:28 GMT  
		Size: 4.1 MB (4138742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:08317b9ed8258e1ea6ef463a0f4b867a12f3ff1bf4ed955bfd4ca563ddcd41b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **870.2 KB (870242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cfc33559f0552f099337ff78cf10ee72d01ffeda2229d129b2be304f11f8f017`

```dockerfile
```

-	Layers:
	-	`sha256:4d904ae80ed3d418ea6000d12e1205d25ddb990e79ec7235f7b1d68fe3a48637`  
		Last Modified: Sat, 06 Jan 2024 00:29:27 GMT  
		Size: 860.6 KB (860605 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:140d78f895961ef1d722987e00514cf4d451ac6ef34ce3301ddc62590292a46a`  
		Last Modified: Sat, 06 Jan 2024 00:29:27 GMT  
		Size: 9.6 KB (9637 bytes)  
		MIME: application/vnd.in-toto+json
