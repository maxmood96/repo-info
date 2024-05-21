## `hylang:python3.8-alpine3.18`

```console
$ docker pull hylang@sha256:e62745310af011d4558a585d48669213aaa16b2498611c5d975f0226bfa59e87
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

### `hylang:python3.8-alpine3.18` - linux; amd64

```console
$ docker pull hylang@sha256:9379508d9c4786b5d98ebeeaf3467cb9b2162ada0368bfc3d104082a8b895ff2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21823290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:216c559bc56d49b3de74768997a495a4148ec38c89b5cee43f99efb183531e5d`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Mar 2024 23:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_VERSION=3.8.19
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["python3"]
# Tue, 21 May 2024 16:47:57 GMT
ENV HY_VERSION=0.29.0
# Tue, 21 May 2024 16:47:57 GMT
ENV HYRULE_VERSION=0.6.0
# Tue, 21 May 2024 16:47:57 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 21 May 2024 16:47:57 GMT
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
	-	`sha256:1d5f94ede96b9bffdfba4e402d4351ba9af669dc2a0b003c7cd98846ef176f30`  
		Last Modified: Wed, 20 Mar 2024 21:10:22 GMT  
		Size: 11.2 MB (11192048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb7d0103352580c4ea76a86753c608f9f9be99a30fbb4faaefe2ec2fa4aeb22a`  
		Last Modified: Wed, 20 Mar 2024 21:10:20 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27cb2ffc36bf5f870bfe73da1c5543221e57968080e8ba901b6d2bd8c89cb3dd`  
		Last Modified: Wed, 20 Mar 2024 21:10:21 GMT  
		Size: 2.9 MB (2852094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cc3373b7e0b3be3474935b11a689e262a7941da1cb6061dd96af52c6f3b665f8`  
		Last Modified: Tue, 21 May 2024 17:53:30 GMT  
		Size: 3.8 MB (3756048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:afe808ad52dffc1dbb84d1bacac28cd3c5621385734cd55129a0c3e585c4fb6a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1031374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ab08496cfff381e4ff4f8d1b9e60254d2602bb7f188a691de0472b07184167`

```dockerfile
```

-	Layers:
	-	`sha256:c7a863aa4fee0c33f51f1c2038aacc28bbbdffc0984977c037fc4f051c2e9e0f`  
		Last Modified: Tue, 21 May 2024 17:53:29 GMT  
		Size: 1.0 MB (1022238 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9945f5352f033fb1f467ff17b1f0b8c53d1c141fff1b36d777561a1d4e6584af`  
		Last Modified: Tue, 21 May 2024 17:53:29 GMT  
		Size: 9.1 KB (9136 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.18` - linux; arm variant v6

```console
$ docker pull hylang@sha256:3f875b4eb4ecb06cd1e1f7411061f2ec50f1d7945eb0e8999957d8ed597bca8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.2 MB (21238576 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97235063f94441d5fe755fb99debd2faf3db54add9e62ffabee895dfb5e42bd`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Mar 2024 23:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_VERSION=3.8.19
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["python3"]
# Tue, 21 May 2024 16:47:57 GMT
ENV HY_VERSION=0.29.0
# Tue, 21 May 2024 16:47:57 GMT
ENV HYRULE_VERSION=0.6.0
# Tue, 21 May 2024 16:47:57 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 21 May 2024 16:47:57 GMT
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
	-	`sha256:fdb6434d4f4bde16adc46daf83520410c96335b5cca8c6958f25d47b3ec592f1`  
		Last Modified: Wed, 20 Mar 2024 20:36:42 GMT  
		Size: 10.9 MB (10862129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96947d8d8d7a4f01c7252d14cb812015921e5b2e19c17f87b208c1641a555426`  
		Last Modified: Wed, 20 Mar 2024 20:36:38 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4da6bd965cf7742d2da4468014bf6f500e1250172f2c25a371202959040a14`  
		Last Modified: Wed, 20 Mar 2024 20:36:41 GMT  
		Size: 2.9 MB (2852102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d082847b70b361c7f45dad1d0e2df875626835a3705447b37f4ebdc34c13ce3a`  
		Last Modified: Tue, 21 May 2024 20:04:13 GMT  
		Size: 3.8 MB (3756201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:87a26229e6f395e6686229f3e80ffd1b2b92b4994a724892000600b95a02df58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 KB (8987 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716aa856d38314e37a2d033c2768df2d75ada7cb7969b9e0b6e0e13640adbd3f`

```dockerfile
```

-	Layers:
	-	`sha256:ef923656ce4548d22d1797ce21847d0f49229be22ba5b925ca53ffc8548e384e`  
		Last Modified: Tue, 21 May 2024 20:04:12 GMT  
		Size: 9.0 KB (8987 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.18` - linux; arm variant v7

```console
$ docker pull hylang@sha256:d3c7a43ac95640be88be39b04540829d045fccf3a12f213e559931f6e068b150
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20601541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:011566fab1c00d5e683d33eafbe4f6904d90fbd417569f4b1b5eabff2b8a4504`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 27 Jan 2024 00:15:02 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Sat, 27 Jan 2024 00:15:02 GMT
CMD ["/bin/sh"]
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Mar 2024 23:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_VERSION=3.8.19
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["python3"]
# Tue, 21 May 2024 16:47:57 GMT
ENV HY_VERSION=0.29.0
# Tue, 21 May 2024 16:47:57 GMT
ENV HYRULE_VERSION=0.6.0
# Tue, 21 May 2024 16:47:57 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 21 May 2024 16:47:57 GMT
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
	-	`sha256:9914798ba4db9d4a5ca911c337c350232f421f3f0cf660afe3db94dedfc92dbd`  
		Last Modified: Wed, 20 Mar 2024 21:51:05 GMT  
		Size: 10.5 MB (10471811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd8806617e554be7a98537562ccb623ea6b58c2b74f85ab26bbd84bb4594058`  
		Last Modified: Wed, 20 Mar 2024 21:51:04 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75ae8740767a0300324cff73b9827d37b50a62306f5e5570c0df8197d1cb4f98`  
		Last Modified: Wed, 20 Mar 2024 21:51:04 GMT  
		Size: 2.9 MB (2852101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aacd4ec0640cf92e25d621ca9fa7db4b06e38014b8e1f2ae22aa52b359f74fe3`  
		Last Modified: Tue, 21 May 2024 21:16:44 GMT  
		Size: 3.8 MB (3756128 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:5bfdfebfab12ea25a48603e4b0f37c1380570641bdc7be10fc471893227d8ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1034062 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:843558f648a807afdc84bd5afb3e93d396b599ef2e6479482acd6c06649399a5`

```dockerfile
```

-	Layers:
	-	`sha256:895167470a3316d0e308f2ff784610cfbeab6197cd928d552430c8834059d5c7`  
		Last Modified: Tue, 21 May 2024 21:16:43 GMT  
		Size: 1.0 MB (1024856 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fcd1262217820ab6d54e9dc3149931c2bd48946821c323ce71d748bb957f5abf`  
		Last Modified: Tue, 21 May 2024 21:16:43 GMT  
		Size: 9.2 KB (9206 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:e38c57c81c09f1534455c553bbe33d834b5f0a6a4cbdc258c870daa3a22e088b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21799127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0638873382fda771da3e887857fc4476111dbe84ae27806d683eeda25afe2993`
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
ENV PYTHON_VERSION=3.8.19
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
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
	-	`sha256:52e81decbde729ad7c3c2c40e947e9378dc5b5e80d926417a83a5bed5a15b7b6`  
		Last Modified: Wed, 20 Mar 2024 21:01:37 GMT  
		Size: 11.3 MB (11264660 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51aa5da66cab626c7e506afcafd86baab887e2d027731ea09044c102c914bc6e`  
		Last Modified: Wed, 20 Mar 2024 21:01:36 GMT  
		Size: 241.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31e61d0a88541c8c07806c1c8c705ada70601f31aea0510f5a61dd7320be25fc`  
		Last Modified: Wed, 20 Mar 2024 21:01:36 GMT  
		Size: 2.9 MB (2852104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45cef00a54908b1dbf49716557830b555fbc6bb2022018fe34cc40521ef8eca`  
		Last Modified: Wed, 20 Mar 2024 22:14:42 GMT  
		Size: 3.7 MB (3726154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:cdf33be681cecf949019e5024dacc4da68ccc9447195b2bbe59e9cf395f990c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1030572 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea0ef1b56ecb722a3f9ecf33ab738507e59fb896529d7653d75bd5aca8a6a240`

```dockerfile
```

-	Layers:
	-	`sha256:c5449b602fd1f2ac149dbc7da3c09a254d2c68162788a553f2f135f46ad4f5b5`  
		Last Modified: Tue, 26 Mar 2024 01:13:21 GMT  
		Size: 1.0 MB (1022249 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7c119ff7c070ca7a07b7ba3955e4859bd98afa7c052ead753472ee57f79be398`  
		Last Modified: Tue, 26 Mar 2024 01:13:20 GMT  
		Size: 8.3 KB (8323 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.18` - linux; 386

```console
$ docker pull hylang@sha256:a25f3597c424d526ef56fd790190e517d65124b148c8b10109708a04dcc86e99
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.8 MB (21788588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29361284b035321003dfec1bc0131ca0a809e43b03b7a6a7e5b5294d7d332d1a`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Mar 2024 23:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_VERSION=3.8.19
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["python3"]
# Tue, 21 May 2024 16:47:57 GMT
ENV HY_VERSION=0.29.0
# Tue, 21 May 2024 16:47:57 GMT
ENV HYRULE_VERSION=0.6.0
# Tue, 21 May 2024 16:47:57 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 21 May 2024 16:47:57 GMT
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
	-	`sha256:402bbcb9e39da61ba9155cc8aba08badab2debea5744b85b765b2700ff6aab84`  
		Last Modified: Wed, 20 Mar 2024 22:10:39 GMT  
		Size: 11.3 MB (11320818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c964bf01f38c6d3bb18ef4eb265d4e032aeeabc7a9eac97fd4f0cc0fe771c3f9`  
		Last Modified: Wed, 20 Mar 2024 22:10:36 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb895d7dde59a388207bbbf3244f6f4eed707b379a4f5cb5ece5ac618d81298`  
		Last Modified: Wed, 20 Mar 2024 22:10:37 GMT  
		Size: 2.9 MB (2852099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:986cc666edff871b547ca80e51af0ef708b01220a930c31c4d1972a2ec7d6d7a`  
		Last Modified: Tue, 21 May 2024 17:53:39 GMT  
		Size: 3.8 MB (3756124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:7af881feb6cdfe2cd9231829213f1f90d4f4281a4e850afd764cb8496719359e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1031320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14000ea6411e66f9a720de5746f801bd38b15cd5dc3f3578d0436b5637c5a5a`

```dockerfile
```

-	Layers:
	-	`sha256:511e0002226b4953c35e83c9af8f84503df578cde128dcd7e0752cb6281abfc5`  
		Last Modified: Tue, 21 May 2024 17:53:39 GMT  
		Size: 1.0 MB (1022213 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:857a5043a591bbc68ddf1f08044411836c75564bf2753b62ce8fcb2f285ea464`  
		Last Modified: Tue, 21 May 2024 17:53:38 GMT  
		Size: 9.1 KB (9107 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.18` - linux; ppc64le

```console
$ docker pull hylang@sha256:1f16079ce12c6156ea85915e671c4864d0aab9b8ad3a9bbfa17cc122210541bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.1 MB (22132246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e9f98d934052838de8f0ab9f064d7c96282e54894dbc3b31674cd3c5e88413c`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 27 Jan 2024 00:27:42 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Sat, 27 Jan 2024 00:27:42 GMT
CMD ["/bin/sh"]
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Mar 2024 23:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_VERSION=3.8.19
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["python3"]
# Tue, 21 May 2024 16:47:57 GMT
ENV HY_VERSION=0.29.0
# Tue, 21 May 2024 16:47:57 GMT
ENV HYRULE_VERSION=0.6.0
# Tue, 21 May 2024 16:47:57 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 21 May 2024 16:47:57 GMT
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
	-	`sha256:fce637ab820cfde2bb5e13bd203b92fd1caecc396de4eaf93d02af11a441f64d`  
		Last Modified: Wed, 20 Mar 2024 21:30:00 GMT  
		Size: 11.6 MB (11552237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a84a4bbc1c79c487752ba558438ae92a7c903f84b01940e1b49297552afe6b55`  
		Last Modified: Wed, 20 Mar 2024 21:29:58 GMT  
		Size: 242.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc887d37229af74f12316a7eb48b1a504faebe07518b38b76127c815fd187ff`  
		Last Modified: Wed, 20 Mar 2024 21:30:00 GMT  
		Size: 2.9 MB (2852101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7465e412ffe8411b806fff9445f8d44344a198faeb1c1ef32964238fea6cdb7a`  
		Last Modified: Tue, 21 May 2024 18:42:31 GMT  
		Size: 3.8 MB (3756199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:5aa4ab405da38b4cdf3766553969526aea6c3bf8331540848bf413afaf3a8463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1029491 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f3762f3d2a09eb271961ee15515b62b11dada021cfb417eb5ceb34a32923fee`

```dockerfile
```

-	Layers:
	-	`sha256:fe823dbc163fd5f62406b5980b1512bd5fc39961784ab4a3c4cbbc987330cff8`  
		Last Modified: Tue, 21 May 2024 18:42:31 GMT  
		Size: 1.0 MB (1020318 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c222342b4ff045a4925a0321baf86460e139073583de840e09ecbc94eaf09d`  
		Last Modified: Tue, 21 May 2024 18:42:32 GMT  
		Size: 9.2 KB (9173 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.8-alpine3.18` - linux; s390x

```console
$ docker pull hylang@sha256:60613012a3363015835129eeb9cd123009c46ad0519d196b45f76ee05ecb06c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 MB (21730714 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06828f9b59db9b5ab9bafa608b16a7e88f525adfb6f6758dce0fe13a4f80f225`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 27 Jan 2024 00:39:19 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Sat, 27 Jan 2024 00:39:19 GMT
CMD ["/bin/sh"]
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Mar 2024 23:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_VERSION=3.8.19
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 			-o \( -type f -a -name 'wininst-*.exe' \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=57.5.0
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["python3"]
# Tue, 21 May 2024 16:47:57 GMT
ENV HY_VERSION=0.29.0
# Tue, 21 May 2024 16:47:57 GMT
ENV HYRULE_VERSION=0.6.0
# Tue, 21 May 2024 16:47:57 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 21 May 2024 16:47:57 GMT
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
	-	`sha256:460af4abcc1c58adcfbdfc710f73643e3c23d48338091a64e339924e053e4686`  
		Last Modified: Wed, 20 Mar 2024 21:48:40 GMT  
		Size: 11.3 MB (11281644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbaabd189f9cf5ad49458605182b9ae51776379966634502afc8da545509c85b`  
		Last Modified: Wed, 20 Mar 2024 21:48:39 GMT  
		Size: 240.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b8c1eb815271d552e90f97076d5bf77c73e43ddd9a31f1391a1cc8a14e9234f`  
		Last Modified: Wed, 20 Mar 2024 21:48:39 GMT  
		Size: 2.9 MB (2852098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f4a0e4d95f89d2cd6bb6c1f1a1879469510cb190617766b30b9e0caa1b6ac03`  
		Last Modified: Tue, 21 May 2024 20:20:34 GMT  
		Size: 3.8 MB (3755884 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.8-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:71212997ac2de11c78834bd7513afed2f268220be70790af41a4949924ff3df0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.0 MB (1029413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e1d7dad205a0d141f0647da06f826b53f7c124fecd65cfe5cedd093ef107b8cd`

```dockerfile
```

-	Layers:
	-	`sha256:5a972f02623676db2eded49cafe52aa471066b127ed64c485a597369b3036883`  
		Last Modified: Tue, 21 May 2024 20:20:34 GMT  
		Size: 1.0 MB (1020278 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7276155ee1ffa1705ec47f5a86007de0445cf462983b579904e30b5d0c4fad6b`  
		Last Modified: Tue, 21 May 2024 20:20:34 GMT  
		Size: 9.1 KB (9135 bytes)  
		MIME: application/vnd.in-toto+json
