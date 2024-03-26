## `hylang:0-python3.10-alpine3.18`

```console
$ docker pull hylang@sha256:b844d39d743fbc3faa6f77a118b91bad0e7200d3b5c5d621a02f380c07ed9b50
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

### `hylang:0-python3.10-alpine3.18` - linux; amd64

```console
$ docker pull hylang@sha256:cfc524fc1d906d5539865fa7787b43656faa2d71eb7bf57720952e047fa70c83
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23293333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd9d38ca7b0d21e8271e692549897aa1cbc3398010c12e17f42f76f1524e8666`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["/bin/sh"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.10.14
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
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
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36988be9c68b1d574f1a24e9dc49c2d5c9ce9c4a2748652c735207995b3f4f10`  
		Last Modified: Sat, 16 Mar 2024 05:41:28 GMT  
		Size: 620.3 KB (620317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09aeb0d078f348337327f8651987dd40ff1652ac0536decc673960b123f7c29a`  
		Last Modified: Wed, 20 Mar 2024 21:08:05 GMT  
		Size: 12.0 MB (12048639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9909fbdf4139a54a985b7224ae7add6abea81166fb1d8a362f546b508e284439`  
		Last Modified: Wed, 20 Mar 2024 21:08:03 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1eae9ac3d47257ff8628e15db5cba16d5921a95a756353fa57c1041fc4af5f4f`  
		Last Modified: Wed, 20 Mar 2024 21:08:04 GMT  
		Size: 3.1 MB (3081102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:843c308b432a7173217a52820da7f2b4fd3541cb4663c4df2195f6f5f53d2676`  
		Last Modified: Wed, 20 Mar 2024 21:50:03 GMT  
		Size: 4.1 MB (4140490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:50fdad2682ff8451a1b19600648265a1ce76be1d827a8f36cda98c63d5bfa151
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1029108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85940deb91d43899dfcd060964a9a780310d65eb5aa9bc0717e89170890caf0c`

```dockerfile
```

-	Layers:
	-	`sha256:d1e28c9a096f134e471f237e86704765ba705df85ff590bcc4bbcfea772b2a4f`  
		Last Modified: Wed, 20 Mar 2024 21:50:03 GMT  
		Size: 1.0 MB (1019961 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a41fd367148fc94ff900313508db749381855c7672ddf9bb9728361cd35cef3c`  
		Last Modified: Wed, 20 Mar 2024 21:50:02 GMT  
		Size: 9.1 KB (9147 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.18` - linux; arm variant v6

```console
$ docker pull hylang@sha256:8e562297a3f6fd63c5bb95ccd20642ea40b8424383de2d29f9bc53d406cc39ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22687042 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a48046b641bb227f232f88e694e5beafa7e2b0bf81d049fcce03fbd76b662df8`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["/bin/sh"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.10.14
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
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
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f6a868fba7e3ecf67dca297570e42afd95b5471949a648b3adc957441262ad5`  
		Last Modified: Sat, 16 Mar 2024 08:42:28 GMT  
		Size: 620.8 KB (620844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b48a7ad7b198642ebdbf57294f9aa4559dc3b7cc451980fcf65022558e8a986`  
		Last Modified: Mon, 25 Mar 2024 19:51:14 GMT  
		Size: 11.7 MB (11696967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a9e3c138dd82bff8da0f2585e6162ae3be7b45042b02b00e207afb9acdb1b1b`  
		Last Modified: Mon, 25 Mar 2024 19:51:12 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cca63c3a22019611e9311bf11fcbc791f2acbea4ff97d5bd64075f5dcbe217d8`  
		Last Modified: Mon, 25 Mar 2024 19:51:13 GMT  
		Size: 3.1 MB (3081105 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e288ee3f0dab9e1f509bd48c43787b9712ef97ea6688ad3a72ebecc85e4a872`  
		Last Modified: Mon, 25 Mar 2024 21:13:53 GMT  
		Size: 4.1 MB (4140824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:1323935f7a132a5fd59b889531ac55111cc1e7e863ce1642b784f612232792df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 KB (9001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a41b91a2d2cc59b355d89b04160d2feb070e306d9b22fd160e678e0955697018`

```dockerfile
```

-	Layers:
	-	`sha256:0c7085f5ac505b172e78ffb601725bc75676e1e5abf682aba0bbeaa3931ca75b`  
		Last Modified: Mon, 25 Mar 2024 21:13:52 GMT  
		Size: 9.0 KB (9001 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.18` - linux; arm variant v7

```console
$ docker pull hylang@sha256:33965a95c094de61c913f836c6d26ecb4e4726c8e32cffcdc8dee3cf79a7a24e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (22019133 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:454be8f068aae49499210e00e8453c1a3bfc01c762b351683b913c90e8f87556`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["/bin/sh"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.10.14
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
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
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc8c0790fe39f905b02705c19231cbbda01a194d14667ed2753d0ec47a8b111`  
		Last Modified: Sat, 16 Mar 2024 08:33:47 GMT  
		Size: 619.9 KB (619866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:975139ce9fe97f2a6c2a5f957ef140c51a0f9b707540b074c33824b6f5235057`  
		Last Modified: Wed, 20 Mar 2024 21:48:41 GMT  
		Size: 11.3 MB (11275616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28049aad6001316b77e18d89540aa368bd79cf595ca4cc066b9fb073d70accfe`  
		Last Modified: Wed, 20 Mar 2024 21:48:39 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3819dd26b188e82ffb9e9c6f9e0b25e202a942149967951f0498c43d3a1f469e`  
		Last Modified: Wed, 20 Mar 2024 21:48:41 GMT  
		Size: 3.1 MB (3081136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d60ead442c7715f2b4e4d006cb8ead06d793b01a72bb361170d1b4c152288315`  
		Last Modified: Wed, 20 Mar 2024 22:52:45 GMT  
		Size: 4.1 MB (4140879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:bcfb3e7e781a989571712df9db15167c0c210d8f2b30aacfed8c11183f234b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1031796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eef9871cf4b6e7f6254fb43a6e268551868e048ee76699e7292125cc64d02948`

```dockerfile
```

-	Layers:
	-	`sha256:89113d8dd67a13445d4df505e37c1d3446bd0c003455baafb5aca375d045bfb3`  
		Last Modified: Wed, 20 Mar 2024 22:52:45 GMT  
		Size: 1.0 MB (1022579 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:73e56cd97b81b9b78b3c3b4ef39fc927fbb9cbe59fe4e4bc3208f591cd01df0e`  
		Last Modified: Wed, 20 Mar 2024 22:52:44 GMT  
		Size: 9.2 KB (9217 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:d8cbf767ad2452acb23de00c2299199932645ce76143471c1919776d831729a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23282877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f21bc6a16462da468d88c6ceb6311ed6dd2cf135eca88fe5fdf24d7c4259c11`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["/bin/sh"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.10.14
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
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
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f06ecd04ab391509e98624d65ab64885219624b8a2a65155ca50cff587ce2eb3`  
		Last Modified: Sat, 16 Mar 2024 10:08:38 GMT  
		Size: 622.6 KB (622607 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5f29200ba69616f395e0a834a187513e4cdb4b6ada8c369be403d44823d41af`  
		Last Modified: Wed, 20 Mar 2024 20:59:17 GMT  
		Size: 12.1 MB (12104815 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59252386c45fcb8b913d700aa897a4c60830068431ab3055be6b178254c5f843`  
		Last Modified: Wed, 20 Mar 2024 20:59:15 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbca2a257709c19da63fcb1ef5a2d349cec2def16b1b32574509cbd2239ce382`  
		Last Modified: Wed, 20 Mar 2024 20:59:16 GMT  
		Size: 3.1 MB (3081137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57513902adc5370c0caf64ddf8ae342b861eb0be7837209addd31f2eb6a05fae`  
		Last Modified: Wed, 20 Mar 2024 22:10:32 GMT  
		Size: 4.1 MB (4140716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:9cc14420917b46e4b6c7296771f1f7eb9257d5916aefe118bc4478a08ab038ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1029129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1de211fad25710ee068c2314820923807976e5d9f748e0e46b7a8b8f3d0a3439`

```dockerfile
```

-	Layers:
	-	`sha256:8e91a21451d5a4fb68b0c2cc4f6e254ce006ec506835180d8a077bbff5bb13bf`  
		Last Modified: Wed, 20 Mar 2024 22:10:32 GMT  
		Size: 1.0 MB (1019972 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52dcb47be0b5ccb7070ebed258f4b0ed422c09e37698c0a066b11f9bde23621b`  
		Last Modified: Wed, 20 Mar 2024 22:10:31 GMT  
		Size: 9.2 KB (9157 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.18` - linux; 386

```console
$ docker pull hylang@sha256:55d006cb23ae61b4bb1ac5de47577f0951d05fafb1c8a726f49b159ca97ec13c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23251472 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bced5bc548def3b73c4b1a90fad44651003d79764aa8c5f1c94fcea3e8f709c9`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["/bin/sh"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.10.14
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
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
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e85c98d4c13c9bb557ec60a2a31fdd405940fc815bb2ae8b1d2c9cf0634b773c`  
		Last Modified: Sat, 16 Mar 2024 08:23:13 GMT  
		Size: 620.2 KB (620242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67deadf635286eda9121c14b2ed8ef3c6b56b1f191c8fc3347b11655b9d198d9`  
		Last Modified: Wed, 20 Mar 2024 22:08:08 GMT  
		Size: 12.2 MB (12170189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f1243cd511ad8159f0d8f4a38ac31f6fddf57bd1749b7af7efd191577159d2`  
		Last Modified: Wed, 20 Mar 2024 22:08:05 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ef2bd75f8e6c36ed77336a585274a23d8f5ed1008d79f21ff7c4fc0c25b6deb`  
		Last Modified: Wed, 20 Mar 2024 22:08:07 GMT  
		Size: 3.1 MB (3081106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36fd73ae50432e719df0d4ad8fbf10fa0170a00313f7501fe2483b9a147b7e83`  
		Last Modified: Wed, 20 Mar 2024 22:49:42 GMT  
		Size: 4.1 MB (4140627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:9eda9350e2b91b15ce38c981c2dccaf72924ad73d1f9593bac7ff583d02c8146
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1029054 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe4da8cc99c67331bb357d0f04dac048c9f2822167ad5ef0436c2c8015d3df1`

```dockerfile
```

-	Layers:
	-	`sha256:6ad0bad922d2ccc01411d8f381bd45362867c405dc591caf803fd9364dabb4b9`  
		Last Modified: Wed, 20 Mar 2024 22:49:41 GMT  
		Size: 1.0 MB (1019936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d9b5c869cf61c71074bd98fc2c14668825d16c9cc083090fcaad789b5641b91`  
		Last Modified: Wed, 20 Mar 2024 22:49:41 GMT  
		Size: 9.1 KB (9118 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.18` - linux; ppc64le

```console
$ docker pull hylang@sha256:422a55dfb0d6c34365936a42739e94e63b9af906b8c3a2aa0b1a50d4f8288e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23634474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9c8bf1eb5b261e01833f15d1c78b431cf783cc109ffd2d6661a1bd7c49ad9e0`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["/bin/sh"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.10.14
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
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
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4098228a344ecd4e40e0c60b5fffc0f24fb7f0f03fc2b9bd7200a733893bde`  
		Last Modified: Sat, 16 Mar 2024 05:02:31 GMT  
		Size: 623.0 KB (622980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5770ad599cc10e8ce341f79f5d2bda2b01a0902889d5038560850d95c574e691`  
		Last Modified: Wed, 20 Mar 2024 21:27:23 GMT  
		Size: 12.4 MB (12440879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:133895abee7ebfa1aea5aecfe71c3b2b47c69575792d33f5c8be73b67b551759`  
		Last Modified: Wed, 20 Mar 2024 21:27:21 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e22878b79d3c2b52915ca27b6ac47525d1faba094943c405b7b9e482ffb45ef2`  
		Last Modified: Wed, 20 Mar 2024 21:27:23 GMT  
		Size: 3.1 MB (3081154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b159e3a5279a106dff18dec50fa16a5aab326568bc79215da43a250ba48ddb3d`  
		Last Modified: Wed, 20 Mar 2024 22:05:28 GMT  
		Size: 4.1 MB (4140732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:7fd4545685a7dea3b3f092cec505478817ce20d22a77afade4cbf5a5b7a9c046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1027226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4e2a2d756f55d93bb5601d7f1bab74e2a2760371e50ed6dca67d732407e6d72`

```dockerfile
```

-	Layers:
	-	`sha256:bbc49ea87f7f457e5180341e5fc266d9cc1b6ed1eaaef3856fb8db2053e39bb9`  
		Last Modified: Wed, 20 Mar 2024 22:05:27 GMT  
		Size: 1.0 MB (1018041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:42f2b38e36535e6087ad9a7cfeb1ba787f84feda814484204f86aa93a69c3a77`  
		Last Modified: Wed, 20 Mar 2024 22:05:27 GMT  
		Size: 9.2 KB (9185 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-alpine3.18` - linux; s390x

```console
$ docker pull hylang@sha256:f5616f15ed0843fa9c8ef3c89cb04c7c976395905738618dd1e4ba0622420e8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23157632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65138e994b215b4238eea79b1ca8158564318d44c179ddd31bc6f8347d6c595a`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["/bin/sh"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.10.14
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
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
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97c4f98bf0f1eb75c60f7795e298cfeecdcb24a5d349d6b0d7d5e30f8da4e51b`  
		Last Modified: Sat, 27 Jan 2024 04:06:09 GMT  
		Size: 623.3 KB (623318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df848e9647ab904e6976b200f1399317d49b138c2ff4ec646bee07d02f646ecc`  
		Last Modified: Wed, 20 Mar 2024 21:46:53 GMT  
		Size: 12.1 MB (12094726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4dd5665b7779f95317451a59446cd6c025ae3aa0c36f0b04c69fac8d49cc36a`  
		Last Modified: Wed, 20 Mar 2024 21:46:52 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9939d2c22dd097ae63713e782a861f4bae9eef3b3fdc3001a4b95485f5a55f12`  
		Last Modified: Wed, 20 Mar 2024 21:46:52 GMT  
		Size: 3.1 MB (3081131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14383758a5926e0ffee108c3a061b76b272037b240503ca7c3cacc6c004615ef`  
		Last Modified: Thu, 21 Mar 2024 01:52:16 GMT  
		Size: 4.1 MB (4140683 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:8a184fceaf129898eccbaa225d338025e509e2fdf9f5569d86b13427d54453f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1027154 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984e4bb19cd73dfb59e270e85b74648f68797ef0aabcab21575bc8d212456a5d`

```dockerfile
```

-	Layers:
	-	`sha256:03f239eefdf3d7cd52bd44db930d45ec10d8fd8f78daae71e33cabf86b52c565`  
		Last Modified: Thu, 21 Mar 2024 01:52:16 GMT  
		Size: 1.0 MB (1018007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9848ff46e6b1159d1eeb3aba1e0884441ee961dc65bbde2f1af18e35cbdff12`  
		Last Modified: Thu, 21 Mar 2024 01:52:15 GMT  
		Size: 9.1 KB (9147 bytes)  
		MIME: application/vnd.in-toto+json
