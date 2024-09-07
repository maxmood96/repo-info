## `hylang:python3.11-alpine3.19`

```console
$ docker pull hylang@sha256:b442a0a16d45c9f403a47b093f41485aa070a9b31269432abd21d587c8e2a7e5
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

### `hylang:python3.11-alpine3.19` - linux; amd64

```console
$ docker pull hylang@sha256:35e2fe07c6bed6aa7526b6929035e959fd4076d7cf67587293b2a169e588e746
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.0 MB (26042499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21945917af3f9f2e6338ad1ae0c0c5ab22eecd84b1bccd5f16cb063335dbc936`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:9e193d6fff4bce11c0ee715ad87def9ef40e9608d4be84cf73391edd45b2810e in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.11.9
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=24.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:94c7366c1c3058fbc60a5ea04b6d13199a592a67939a043c41c051c4bfcd117a`  
		Last Modified: Fri, 06 Sep 2024 22:20:51 GMT  
		Size: 3.4 MB (3419706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17e6f497155a16caa14f1a69b950044df89b6073afcd1e3d97c5af4ce9b6621e`  
		Last Modified: Fri, 06 Sep 2024 23:35:46 GMT  
		Size: 627.9 KB (627923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bef66da41e89ef80a2c6976376f410105a32e13c71bf29e8f47afcc120ab2702`  
		Last Modified: Fri, 06 Sep 2024 23:35:46 GMT  
		Size: 12.7 MB (12671513 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c865fa006888f480329fd6384abfb129097a519cb3df60dbb38e464a8394092`  
		Last Modified: Fri, 06 Sep 2024 23:35:45 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a564239f383a09d3317dc31c02fde4f09c7fe219359dda1357be9121319bd0a`  
		Last Modified: Fri, 06 Sep 2024 23:35:46 GMT  
		Size: 3.1 MB (3131017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f718ada5417b54156b2664f0a38899e42f2aed724fea7be341e4b8fa209b41e`  
		Last Modified: Sat, 07 Sep 2024 00:10:53 GMT  
		Size: 6.2 MB (6192112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:14d6b2005c5d126bb999855f43539fa0e3c41c156f4cc7ab2cbf3a53976bcbe8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1044698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0d69a09614629fdb4afee2fd1725467b42477c8a262bcd4ed6c886db7fa4b34`

```dockerfile
```

-	Layers:
	-	`sha256:b08b59f527506bb408cca5033dea0e802e355c963d2c35941c058bb1b117e816`  
		Last Modified: Sat, 07 Sep 2024 00:10:53 GMT  
		Size: 1.0 MB (1036189 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a5cda2ad4dc6d4156edb95807a792f38c357bf07f0fdea7964b92cc0ada3fa45`  
		Last Modified: Sat, 07 Sep 2024 00:10:53 GMT  
		Size: 8.5 KB (8509 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.19` - linux; arm variant v6

```console
$ docker pull hylang@sha256:19d64b7f4dc0589c9d53a1f7af26448ae05a2c80744a57e769d5ee45d55b6e18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.4 MB (25398225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04f66762d277341821756acc16760d82c10d3de3323d8b82647454b2c2132c64`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:87d4cb9e99b4a12939a030198a62d49f1c5b7856f27d62fea0e948cd2120d51d in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.11.9
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=24.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8922ced57063579c37aeb21c1c664433762d26f8051e187a63b559c21b36da53`  
		Last Modified: Fri, 06 Sep 2024 22:49:59 GMT  
		Size: 3.2 MB (3176391 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0a39bdf9d326d55be66a6472913d0bdbe3b64af11a3fa17f368b4581b594e62`  
		Last Modified: Sat, 07 Sep 2024 10:50:50 GMT  
		Size: 628.8 KB (628820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03245f9ec47671e82b6a791cda8c6d8ac02ace7fca577023cb54ebc8b26351cc`  
		Last Modified: Sat, 07 Sep 2024 11:27:10 GMT  
		Size: 12.3 MB (12269601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c2c5879612027be27065a5e0769644061cd02e17f939512dcf8c4441f8267ee`  
		Last Modified: Sat, 07 Sep 2024 11:27:09 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30db182e75afb5cc0d60945c1407297f65be089879307c2cc4a816099ee8a3c0`  
		Last Modified: Sat, 07 Sep 2024 11:27:10 GMT  
		Size: 3.1 MB (3131003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:447d274ed2ca3ba11264a98959f12dd959a7fb7b54866c3f628bb5a7fe6be442`  
		Last Modified: Sat, 07 Sep 2024 13:40:20 GMT  
		Size: 6.2 MB (6192180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:fd9299976d90463b2a748768c8f795a1512080a22721d44b92361a0b02414c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.4 KB (8378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0da88f68de2ef3d27178a9ea57051912c94a1b234835fbd13ead59f459629570`

```dockerfile
```

-	Layers:
	-	`sha256:6c5eac003c8c538c16f081dc79bf2f8dd706c5408c91a6473170069448929bba`  
		Last Modified: Sat, 07 Sep 2024 13:40:19 GMT  
		Size: 8.4 KB (8378 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.19` - linux; arm variant v7

```console
$ docker pull hylang@sha256:c60f25bc1b754e87f7525cfafaac79c7034558c92e7ec200475e8d4ee770f4ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.7 MB (24728739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c68968567054f1bdd4312565886a3939ead3efcd813f705a7bfb0229f0473b08`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:a0a04eec8c7b34f27431bfd6edc27b4c05f2174daf93e40c263717d2469dcebd in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.11.9
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=24.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:426a5537ab470cede64a1b269dbc9f485fa674bec59555cdaa5a1c96e6675b0d`  
		Last Modified: Fri, 06 Sep 2024 22:08:37 GMT  
		Size: 2.9 MB (2927664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2773a0915bfcbc78e079faa18251ac0d879f0f82697ee83220c411ab06dd1bb`  
		Last Modified: Sat, 07 Sep 2024 11:07:13 GMT  
		Size: 628.0 KB (627974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4a6d3805aa2b2a26fd8acc15105cde01e849bc69c183ed96db15e3614df7168`  
		Last Modified: Sat, 07 Sep 2024 11:43:36 GMT  
		Size: 11.8 MB (11849691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8e97463e54c03703908485cb724f0fdce670af71d43c6630175a4eef815b681`  
		Last Modified: Sat, 07 Sep 2024 11:43:35 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cc9067085eaf1458172c632539e8168689acb8014f2a78be34fd08b49355f3`  
		Last Modified: Sat, 07 Sep 2024 11:43:36 GMT  
		Size: 3.1 MB (3131004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79eac1f594f00e11260b8ce3e68718d89662390fde7b5ebfc3268bbe02b0bb1`  
		Last Modified: Sat, 07 Sep 2024 14:22:56 GMT  
		Size: 6.2 MB (6192176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:50a7b7499ad1987663fcf489741b18edb26d147586dbfcd502f7092b6ffff487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1047685 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea6ea212e67a0b841500b2d45230499e584dd58cdbafc05ca01070f0b1d35045`

```dockerfile
```

-	Layers:
	-	`sha256:5a41ae34baced0476ac8f2cbdb5d5df92425918e459aa9ed16dd73a98408a814`  
		Last Modified: Sat, 07 Sep 2024 14:22:56 GMT  
		Size: 1.0 MB (1039089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:642c8e347e5e6bd73320a892424ae47f8d9dde99456fffe1c7018d6a544c40ee`  
		Last Modified: Sat, 07 Sep 2024 14:22:56 GMT  
		Size: 8.6 KB (8596 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.19` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:b4eb81c5bb5bd26f8ae31979951d236600763963a3f5150d483801c7eca7ce68
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26061819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2d9f021aef0da7d948a596c8073380eb6065f8c7bb611277cd003bf96a47bf7`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:9865d69f45511580cc2a05d8a9573251b6eb5a84520efe2e8295532e3ccd6321 in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.11.9
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=24.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:188a7166e45935ced07634efdc8e63c13f5f7673b60b051b353475ee00e28fe0`  
		Last Modified: Fri, 06 Sep 2024 22:44:50 GMT  
		Size: 3.4 MB (3359103 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaf2f2790992c8c78211ff5181c3fb0eb2710f0d4ab4c29278770b838db532c2`  
		Last Modified: Sat, 07 Sep 2024 10:20:39 GMT  
		Size: 630.3 KB (630335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:920901b654117e3e9e6317a99751f294300298e0fc53f446c6130e8c88284292`  
		Last Modified: Sat, 07 Sep 2024 10:51:12 GMT  
		Size: 12.7 MB (12749048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56e5e2217c6d4d874159df00fce041bfd89ad6001efc7c41fb44c77493efd8a9`  
		Last Modified: Sat, 07 Sep 2024 10:51:11 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d597f61a71b14f4ed955ff92c75b3eaa9ee968afb468268ec988d6cca8b1b8d`  
		Last Modified: Sat, 07 Sep 2024 10:51:12 GMT  
		Size: 3.1 MB (3131011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a4f3c40a38040011603d86c8fb9b0f16ec059d5c2306d02f5de1364d2cc4b5b`  
		Last Modified: Sat, 07 Sep 2024 13:55:45 GMT  
		Size: 6.2 MB (6192093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:616f7a0537791211d76fe673462ab4a2c26cbf23cc01ddbe957656a78e91950d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1045150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d04f2da9c1e3edced0aa8306af7a109225407ebd882847abd297db7f06ffc5d`

```dockerfile
```

-	Layers:
	-	`sha256:920d1943efcc9a228fb01d752a417ff94ca38d72da6ddbd830458ea4b2dcee2b`  
		Last Modified: Sat, 07 Sep 2024 13:55:44 GMT  
		Size: 1.0 MB (1036245 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abeba84bdb60f7fa6549f452dd219b7c982cef0ff2de82ee6b207fd92b7afaa0`  
		Last Modified: Sat, 07 Sep 2024 13:55:44 GMT  
		Size: 8.9 KB (8905 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.19` - linux; 386

```console
$ docker pull hylang@sha256:8a102331b34af0c1fec5c93d1e5290e3bec6020212c1eade1e62518db73f9fa2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.1 MB (26065795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:563950d2bbcd9d33f7f2876cf8687c86b121395ddc6eee842d57c1cd3f4bfd55`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:19a9ac542bad192441d76d7dbe5496866d50d90786aa582a9a470a6f5c620f42 in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.11.9
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=24.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f8365d87ce9a9886c88284fcf1fc48ad082e1d5ba8d0d788aeb9e49923921970`  
		Last Modified: Fri, 06 Sep 2024 22:41:58 GMT  
		Size: 3.3 MB (3253605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964d0f859517122d61c53071bbfdc41ab87fb9f1a18fb98993a55d0f2e539c0c`  
		Last Modified: Fri, 06 Sep 2024 23:31:59 GMT  
		Size: 628.4 KB (628423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc8db9ca9e1e3e1cc8dfa9a3f484c19ebba64134c16a4d835b84a600d54f0d65`  
		Last Modified: Fri, 06 Sep 2024 23:31:59 GMT  
		Size: 12.9 MB (12860300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae076cd1b30ae65f0a74dda1fa42b62e1b413a858935eaff980bc5f69b45db82`  
		Last Modified: Fri, 06 Sep 2024 23:31:58 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0aaf57bc1d4a261f0e7bca30a81654aa00c1279b81354c31a1ee79405f6040a`  
		Last Modified: Fri, 06 Sep 2024 23:31:59 GMT  
		Size: 3.1 MB (3131032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ba478bb0c6bc0f172dd7620873c5bf4e008e25633fe4adff2ead0b1777ab20`  
		Last Modified: Sat, 07 Sep 2024 00:10:44 GMT  
		Size: 6.2 MB (6192206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:87bb1dafe7fd16967319f11e58ff415c199a2396fd5e78a476e597509e503745
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1044641 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80a542e8379b4d291e8655c654f3fbac4176391997466948cc7a8badf89ee533`

```dockerfile
```

-	Layers:
	-	`sha256:32d191590d0853b248aea6eb7fb75eeebf253456efd4dbe3e440b019efd91702`  
		Last Modified: Sat, 07 Sep 2024 00:10:43 GMT  
		Size: 1.0 MB (1036164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79bd0dc1cc03377e0fe84be72bfb879226bced72fb2186ac9eb4a74a564629db`  
		Last Modified: Sat, 07 Sep 2024 00:10:43 GMT  
		Size: 8.5 KB (8477 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.19` - linux; ppc64le

```console
$ docker pull hylang@sha256:85d1de336c6fde508a51ad08b5aab702434bb96009c6b4b13f7cb497c4361864
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26488746 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4dde9f384bee4a707703aec4c38eed39430dd0b5492a4ac8138fb10c32b7dfe1`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:2b460e2f1af1fd81bcf839fbca42c282e18754a310086d2d55772cfcaff3154e in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.11.9
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=24.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1274ef399099f48829c82f23090a3c36444839648f7cf9fbf44c7518257fcdd2`  
		Last Modified: Fri, 06 Sep 2024 22:26:51 GMT  
		Size: 3.4 MB (3364467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5749dced5c3ea885609ac4ce0f87b1f345b6e9df997e9a8b0aaceac5eaaa6e3f`  
		Last Modified: Sat, 07 Sep 2024 09:58:37 GMT  
		Size: 630.8 KB (630837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbaceb5da0809ba124f4b8ed98e868f3903ae7ccfcb126248551698e7faa45c9`  
		Last Modified: Sat, 07 Sep 2024 10:38:01 GMT  
		Size: 13.2 MB (13169927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e74fd317ba4f8a90542f04adede9a7d0c1bdaba545099aa903f4a2ee83d57b`  
		Last Modified: Sat, 07 Sep 2024 10:38:00 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f6df34bfb2fad8fdeee88e438a610ec70a5be6d7c5e7d139606daf2e08b68ed`  
		Last Modified: Sat, 07 Sep 2024 10:38:01 GMT  
		Size: 3.1 MB (3131023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0bf4dc69af615c256203cc798f106ee2994bcbd2be90d96c66ecee88e450b9cc`  
		Last Modified: Sat, 07 Sep 2024 13:57:17 GMT  
		Size: 6.2 MB (6192262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:889ee76cc3d32188876d5b37e425c5d173231eca40850dabd2e938fae3533a32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1042834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c272558883b669e9ebfcbb50bb8dcd895b6c78cac338afcff02c965785b4c2e3`

```dockerfile
```

-	Layers:
	-	`sha256:3983bd8f584d5f24c0dda184da1ceca642d78c2f5a938dd26e9b523e5a717063`  
		Last Modified: Sat, 07 Sep 2024 13:57:16 GMT  
		Size: 1.0 MB (1034269 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32bc5b47d7c16ef9492f1120417c611d8d8c3212e992fb8a5f12b0ef1774e461`  
		Last Modified: Sat, 07 Sep 2024 13:57:16 GMT  
		Size: 8.6 KB (8565 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.19` - linux; s390x

```console
$ docker pull hylang@sha256:c9ec267063f9a757e64d726b01b9882515b75e4f1754149732d39c2a9f564ff1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.2 MB (26187996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df6f1efa6a091d286b74e58abef272bf43f7360ffff9f0443dda6e4eea11d04`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 29 Aug 2024 19:15:55 GMT
ADD file:accee20143ffbe803d23675898d25fedbb25c04fcc9f4ddaa1ba5f066c5ae260 in / 
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["/bin/sh"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 29 Aug 2024 19:15:55 GMT
ENV LANG=C.UTF-8
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_VERSION=3.11.9
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--enable-optimizations') 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_PIP_VERSION=24.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/def4aec84b261b939137dd1c69eff0aabb4a7bf4/public/get-pip.py
# Thu, 29 Aug 2024 19:15:55 GMT
ENV PYTHON_GET_PIP_SHA256=bc37786ec99618416cc0a0ca32833da447f4d91ab51d2c138dd15b7af21e8e9a
# Thu, 29 Aug 2024 19:15:55 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 		wheel 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["python3"]
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HY_VERSION=0.29.0
# Thu, 29 Aug 2024 19:15:55 GMT
ENV HYRULE_VERSION=0.6.0
# Thu, 29 Aug 2024 19:15:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 29 Aug 2024 19:15:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:dbf93dbda29c680e293e8229956c663ae9d4e8435d70335c363568788915cac5`  
		Last Modified: Fri, 06 Sep 2024 22:49:04 GMT  
		Size: 3.3 MB (3253357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bf180b200a9685ef5f8a9f8ba267cdaf8e59fe28f3b974eee5118a914d262ab`  
		Last Modified: Sat, 07 Sep 2024 09:10:44 GMT  
		Size: 629.0 KB (628993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b29fd1ed0cd32bf9f776a3569c20991097766184bc5f9eb3762fdaf81ddb854`  
		Last Modified: Sat, 07 Sep 2024 09:43:04 GMT  
		Size: 13.0 MB (12982424 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:270d1ac2132b3dea6f392a42122fdcebf0649775c8a1b6a6af37572d7feceae6`  
		Last Modified: Sat, 07 Sep 2024 09:43:04 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:327c07bab781eda593b1807452fc2d560af96c3415f7d7a63f75a38748985e78`  
		Last Modified: Sat, 07 Sep 2024 09:43:04 GMT  
		Size: 3.1 MB (3131023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9d0b330a4a99d22d5bc809d73bb7fbd9dacd6c12e963cb730b2ebea4737753d`  
		Last Modified: Sat, 07 Sep 2024 11:51:07 GMT  
		Size: 6.2 MB (6191969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.19` - unknown; unknown

```console
$ docker pull hylang@sha256:f1a86416784b5219b78f1f464fee46dee434221b4f612e5e080162256d76895b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1042756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb017976b3c90fa8c052b61b43db1664862271c9511b285af44c7125fcfdaac2`

```dockerfile
```

-	Layers:
	-	`sha256:e39e473afb88c0f3588d6568acafd7ebbba5b1b939363584ad857dddb21082da`  
		Last Modified: Sat, 07 Sep 2024 11:51:07 GMT  
		Size: 1.0 MB (1034235 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:307632157543b16277930052d6eb8036479fdfff647bcd3283a1a494630b1673`  
		Last Modified: Sat, 07 Sep 2024 11:51:07 GMT  
		Size: 8.5 KB (8521 bytes)  
		MIME: application/vnd.in-toto+json
