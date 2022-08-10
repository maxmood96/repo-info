## `satosa:8-alpine`

```console
$ docker pull satosa@sha256:fa00b0ab420886685085b244405746ecce141ff81c408876a6d8c17f5e0960ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 6
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le

### `satosa:8-alpine` - linux; amd64

```console
$ docker pull satosa@sha256:889e8b702bc04ca43d059bdf24c8db677954c87e5318ba8a93d795e450d485dd
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42508179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fa3cc16430e95981e37a39687b5b6a8e23b8adf5eb81881cab4136b31de9b6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:00:15 GMT
ADD file:a2648378045615c3785c752423b1afc8dc1c2b213393344f4d0ca17e7255c1cb in / 
# Mon, 18 Jul 2022 21:00:15 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:14:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jul 2022 02:01:52 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 02:01:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 19 Jul 2022 02:01:54 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 10:48:21 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 11:00:13 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 11:00:14 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 11:00:14 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 11:00:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 11:00:21 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 11:47:34 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 11:47:34 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 11:48:17 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 11:48:18 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 11:48:19 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 11:48:19 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 11:48:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 11:48:19 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 11:48:19 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 11:48:19 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:530afca65e2ea04227630ae746e0c85b2bd1a179379cbf2b6501b49c4cab2ccc`  
		Last Modified: Mon, 18 Jul 2022 19:09:35 GMT  
		Size: 2.8 MB (2798806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc8c14b1a767335de44f2bc926cb52487979a0fe602ac5429643dbb238f297fb`  
		Last Modified: Tue, 19 Jul 2022 02:56:13 GMT  
		Size: 666.8 KB (666769 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:571274b8543b548747b5e9bef700a89692fe9403cc364be8d6e8a0792ccfe2b4`  
		Last Modified: Wed, 03 Aug 2022 11:19:35 GMT  
		Size: 12.5 MB (12508608 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f79a08255af5d614c7b4b81e358b5bb607bdcb14a6475c836d3d4f92f094846`  
		Last Modified: Wed, 03 Aug 2022 11:19:34 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca6b20e3f6abd46292c29437a6917dc82b769ebb239e2d971aedb6695e057715`  
		Last Modified: Wed, 03 Aug 2022 11:19:34 GMT  
		Size: 3.0 MB (3043671 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:071c974d4972d870a99bf0fba525cab86b298dd6e9405d3329a3495a164ae5c7`  
		Last Modified: Wed, 03 Aug 2022 11:49:00 GMT  
		Size: 9.4 MB (9398243 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c482d554455c83821852ea2cd26eaf97f49bb1c7983342cec7242b8ea5432234`  
		Last Modified: Wed, 03 Aug 2022 11:49:01 GMT  
		Size: 14.1 MB (14080297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b861965b84abb04a92b63eb19a620daf7360785f485bc2d526885601454b19ca`  
		Last Modified: Wed, 03 Aug 2022 11:48:58 GMT  
		Size: 9.4 KB (9439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16e011f2d9efad78d03ac0d4c7abe2f694dfc5f6c158ef9fa350a3f21d22a8e`  
		Last Modified: Wed, 03 Aug 2022 11:48:58 GMT  
		Size: 2.1 KB (2115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine` - linux; arm variant v6

```console
$ docker pull satosa@sha256:1ed78492e93849ebbee5cd80dd5e4a91eb2a41676fbc3d21584a17d402028ca7
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **160.2 MB (160179359 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e822b6bb9258ee22b55f2f03c3d389710a39d0a3fa1d10f1250cb00db2f3e268`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 19:49:37 GMT
ADD file:7a20333469e71664904a0cb8f61613250f2bd092b4a27bfa7bbae1dc7e21b7ed in / 
# Mon, 18 Jul 2022 19:49:37 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 00:30:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 00:30:05 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 00:30:07 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 00:30:07 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 02 Aug 2022 19:50:04 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 02 Aug 2022 20:30:07 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 02 Aug 2022 20:30:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 02 Aug 2022 20:30:08 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 02 Aug 2022 20:30:20 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 02 Aug 2022 20:30:20 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 03:20:45 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 03:20:45 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 03:27:52 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 03:27:54 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 03:27:54 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 03:27:54 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 03:27:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 03:27:55 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 03:27:55 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 03:27:55 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:b7885075fcd06a866d12dfd56eb704045eaadbd22dc03a224cd98715be566677`  
		Last Modified: Mon, 18 Jul 2022 19:08:42 GMT  
		Size: 2.6 MB (2606431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1ebe8e3a2f83d0ddc301c9b9d6405376eecb906b92082e05d5e257eff5f6293`  
		Last Modified: Wed, 27 Jul 2022 11:08:23 GMT  
		Size: 672.3 KB (672287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b647934af90a736595f675559fd3aebbcdbcfc67277de68401980916f3c217d7`  
		Last Modified: Wed, 03 Aug 2022 00:13:17 GMT  
		Size: 12.1 MB (12085055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcaef313095ff837d4848dec2c5e458a33e59ee4e1ab7a9d4e3d244d20b92fbf`  
		Last Modified: Wed, 03 Aug 2022 00:13:12 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba453d098c35b58faf7cc2ac6a90a0e9a8941dc90611ee397d12af0a546bbe87`  
		Last Modified: Wed, 03 Aug 2022 00:13:15 GMT  
		Size: 3.0 MB (3043708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e0a90158473abc47e6b9744b5cc61265a9552ba9217486241f5b7b4a5d12eec`  
		Last Modified: Wed, 03 Aug 2022 03:28:44 GMT  
		Size: 8.3 MB (8280231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a82dd9e01f89340501ac0415caccc1ad608cc08d55219cb26db2226dc64b83`  
		Last Modified: Wed, 03 Aug 2022 03:29:07 GMT  
		Size: 133.5 MB (133479861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4ee2ba314aef7361329abd7eaa7a8860079655317f4d5fc9d37f73f8b34de4`  
		Last Modified: Wed, 03 Aug 2022 03:28:39 GMT  
		Size: 9.4 KB (9438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24649d01bd9f34f035857fcb9324aef45128d255b0e7d7c9be9d0d9d58a928f3`  
		Last Modified: Wed, 03 Aug 2022 03:28:39 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine` - linux; arm variant v7

```console
$ docker pull satosa@sha256:9c12b392cb5946a433fe0c98001d362d79a953040068a9d0843c3a9a9c12fb8b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **163.4 MB (163401667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f55a50fb783bb28da31c92c6cff33c408ef6ea7e1c6da179086af8ce588f092d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:24:47 GMT
ADD file:68590e866bc6db27ad54d23de7dd275d0389cb86e4e6291a1243fcc234f2f7a1 in / 
# Mon, 18 Jul 2022 21:24:47 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 03:57:44 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 03:57:44 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 03:57:46 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 03:57:46 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 07:37:59 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 08:07:42 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 08:07:43 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 08:07:43 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 08:07:50 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 08:07:51 GMT
CMD ["python3"]
# Thu, 04 Aug 2022 13:27:03 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Thu, 04 Aug 2022 13:27:03 GMT
ENV SATOSA_VERSION=8.1.1
# Thu, 04 Aug 2022 13:30:23 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Thu, 04 Aug 2022 13:30:25 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Thu, 04 Aug 2022 13:30:25 GMT
WORKDIR /etc/satosa
# Thu, 04 Aug 2022 13:30:25 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Thu, 04 Aug 2022 13:30:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 04 Aug 2022 13:30:25 GMT
EXPOSE 8080
# Thu, 04 Aug 2022 13:30:25 GMT
USER satosa:satosa
# Thu, 04 Aug 2022 13:30:25 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:a6b45ace95f42a930d15c33679ab9c85d46019b7e73954cadc73bb9ba176509b`  
		Last Modified: Mon, 18 Jul 2022 19:08:56 GMT  
		Size: 2.4 MB (2412307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d826ef3e3e077607452c51ac5332613cc0a20903abe17b56af4b973f31f0e9b7`  
		Last Modified: Wed, 27 Jul 2022 10:54:47 GMT  
		Size: 664.1 KB (664079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:116f12212b7e97cde5b72713f0f3a3025a9ef6dffccdc353cd4d15407d343a72`  
		Last Modified: Wed, 03 Aug 2022 11:22:41 GMT  
		Size: 11.6 MB (11558755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef2affe775c9998dea9fd354aa8d4b6e97117d2092c84f1401265b9f9528bf7`  
		Last Modified: Wed, 03 Aug 2022 11:22:38 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032af4833525c8884057f85c0da98a7f2dedc337784e4ce3645fad79e6633b26`  
		Last Modified: Wed, 03 Aug 2022 11:22:39 GMT  
		Size: 3.0 MB (3043658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d65c3d7d841a308ff58960bdd0832a9c2fc9d01d091b4478549cf91ad4551edc`  
		Last Modified: Thu, 04 Aug 2022 13:31:47 GMT  
		Size: 8.0 MB (8026973 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:553863577a06e5d191ae29abc79bb81603188e34e406ebce36a4e4da49320df8`  
		Last Modified: Thu, 04 Aug 2022 13:31:59 GMT  
		Size: 137.7 MB (137684108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a6d66d75890a5436b91b581c5023634cbedf248e1dbb622b1241f80c5a4ed29`  
		Last Modified: Thu, 04 Aug 2022 13:31:45 GMT  
		Size: 9.4 KB (9439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94cab52b5f6577ce2ac31dd72be231ca9d43531003be80eacfe2f20bbfa5c5d5`  
		Last Modified: Thu, 04 Aug 2022 13:31:46 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:cccb94f4511ba8a1fd8ab69a69f483edef010e4fab16eeccfb637ae5395cdc67
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40930309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c83c2e990bd9017e2a1f46423fc6e313b33122d383dda9f8f9c00e8006d36921`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:57:05 GMT
ADD file:9ccb70abba88b6de789b29f17770246f765ffbb072fe598580bfc29ce3213f1c in / 
# Mon, 18 Jul 2022 21:57:05 GMT
CMD ["/bin/sh"]
# Mon, 18 Jul 2022 23:10:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 Jul 2022 01:53:04 GMT
ENV LANG=C.UTF-8
# Tue, 19 Jul 2022 01:53:05 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 19 Jul 2022 01:53:06 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 09:50:39 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 10:05:09 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 10:05:10 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 10:05:11 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 10:05:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 10:05:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 10:05:14 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 10:05:21 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 10:05:22 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 10:40:42 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 10:40:43 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 10:41:31 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 10:41:33 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 10:41:34 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 10:41:36 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 10:41:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 10:41:37 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 10:41:38 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 10:41:39 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:f97344484467e4c4ebb85aae724170073799295a3442c50ab532e249bd27b412`  
		Last Modified: Mon, 18 Jul 2022 19:08:29 GMT  
		Size: 2.7 MB (2694720 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05c36086fc9356a3d9879c8427af90dd86ad6fd35b3929bab2af384e98d0571c`  
		Last Modified: Tue, 19 Jul 2022 02:56:56 GMT  
		Size: 668.0 KB (668022 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255e9c7248a65c9bb1f14e3ffaf6aad2e14b965bfd9196b30e8c1efc8ddd1747`  
		Last Modified: Wed, 03 Aug 2022 10:34:00 GMT  
		Size: 12.6 MB (12579036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d32815e9cd0f789447579f484cec5ed6ff5b006c50c121a5e314519ffad01d5`  
		Last Modified: Wed, 03 Aug 2022 10:33:55 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a3c6e4018f23818adb74c050daeddb28d2efddbabe1135f85ed3ef29b17ec7b`  
		Last Modified: Wed, 03 Aug 2022 10:32:56 GMT  
		Size: 3.0 MB (3045000 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2feaf81b71b2f7b13ac6cefc0f434f31221423c1c94002a89138b4c60741ced`  
		Last Modified: Wed, 03 Aug 2022 10:42:41 GMT  
		Size: 8.2 MB (8224897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27c9e9ae46115c582ac3a68bb4b583d2ed73875acfb5ff520c5877d481be9cdc`  
		Last Modified: Wed, 03 Aug 2022 10:42:42 GMT  
		Size: 13.7 MB (13706894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26e959a5cfce7f6c07db205394594178b791ab1fd7b3425ded77627110666277`  
		Last Modified: Wed, 03 Aug 2022 10:42:40 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:143d97f09a0b08aff0f4993e07d50c6a62b1d1c84b442a35f1c8b7f9535005f4`  
		Last Modified: Wed, 03 Aug 2022 10:42:40 GMT  
		Size: 2.1 KB (2118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine` - linux; 386

```console
$ docker pull satosa@sha256:3b7052fea622f5d95da31220bc234a9258ae473482fb55269dea295fd83b4e05
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **173.0 MB (173023892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:712f8d15ddeef960a7327c512f8d03f337021df170d7531f5aa93eafbe51d2c5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:39 GMT
ADD file:b828bc14bc5ff03c8f7310fe0aed6ac5df19a393622d5d1d779a523234d07c0a in / 
# Tue, 09 Aug 2022 17:38:39 GMT
CMD ["/bin/sh"]
# Tue, 09 Aug 2022 21:22:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Aug 2022 21:22:15 GMT
ENV LANG=C.UTF-8
# Tue, 09 Aug 2022 21:22:17 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Tue, 09 Aug 2022 21:22:18 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 09 Aug 2022 22:02:59 GMT
ENV PYTHON_VERSION=3.10.6
# Tue, 09 Aug 2022 22:16:19 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Tue, 09 Aug 2022 22:16:19 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Tue, 09 Aug 2022 22:16:20 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Tue, 09 Aug 2022 22:16:21 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Tue, 09 Aug 2022 22:16:22 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Tue, 09 Aug 2022 22:16:23 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Tue, 09 Aug 2022 22:16:31 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 09 Aug 2022 22:16:31 GMT
CMD ["python3"]
# Wed, 10 Aug 2022 03:30:07 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 10 Aug 2022 03:30:08 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 10 Aug 2022 03:33:02 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 10 Aug 2022 03:33:03 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 10 Aug 2022 03:33:04 GMT
WORKDIR /etc/satosa
# Wed, 10 Aug 2022 03:33:06 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 10 Aug 2022 03:33:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 03:33:07 GMT
EXPOSE 8080
# Wed, 10 Aug 2022 03:33:08 GMT
USER satosa:satosa
# Wed, 10 Aug 2022 03:33:09 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6c0d3b419d848ea31ca748254611d5d5ce3b76e3d7bba520fd87400fbb75f3b9`  
		Last Modified: Tue, 09 Aug 2022 17:39:33 GMT  
		Size: 2.8 MB (2807121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb6e4c463b4b085b81ccd90e5d99d5d5b64a56c2f756e7ff5575080b0efc2e9f`  
		Last Modified: Tue, 09 Aug 2022 23:12:22 GMT  
		Size: 689.1 KB (689070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f30e501e19288fafd4b62af6aaf0b588b8da1b9f7bf0ed0bd8c7cf5550131f4b`  
		Last Modified: Tue, 09 Aug 2022 23:13:12 GMT  
		Size: 12.7 MB (12700838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e5383c9c382f8845fcf42a8ea747ddb3a99c87e277380a509277f27c6bf8d85`  
		Last Modified: Tue, 09 Aug 2022 23:13:10 GMT  
		Size: 229.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2450ac53e437f841f48f00e832466a3d7ce73190f3f5255c89dfb89edcd9193`  
		Last Modified: Tue, 09 Aug 2022 23:13:11 GMT  
		Size: 3.0 MB (3045003 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3183acab5e336c62f2d06a000d65364d4484e755eb4c01749dd6e443ee703e32`  
		Last Modified: Wed, 10 Aug 2022 03:34:01 GMT  
		Size: 8.5 MB (8512861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:350ea1863d968db10b0fe1fd8772d772c84631136d5fb13934b7c5a360cf66fc`  
		Last Modified: Wed, 10 Aug 2022 03:34:28 GMT  
		Size: 145.3 MB (145257262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92895882e21832e6f4d040fa6f60752d36b168dbc7f3893d1fc81a19da18cfc3`  
		Last Modified: Wed, 10 Aug 2022 03:33:59 GMT  
		Size: 9.4 KB (9392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85df40b1b491557b15d24c816c82279561fd23244d53603eeea4f9976ce8766`  
		Last Modified: Wed, 10 Aug 2022 03:33:59 GMT  
		Size: 2.1 KB (2116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `satosa:8-alpine` - linux; ppc64le

```console
$ docker pull satosa@sha256:f70b3121c8db732d980c4272ea937145d0745875aba33578b5667bbaf28fb1ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **164.3 MB (164310759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef00aeaa317867dd9dca82b0661794be10c5d0a082d11a8f76b597b76e88cb55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 18 Jul 2022 21:29:30 GMT
ADD file:69e4080f15f54e2d8f8aa25fdcba9c01dde149d43592edd5023106675e54a769 in / 
# Mon, 18 Jul 2022 21:29:31 GMT
CMD ["/bin/sh"]
# Wed, 27 Jul 2022 04:30:30 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 27 Jul 2022 04:30:31 GMT
ENV LANG=C.UTF-8
# Wed, 27 Jul 2022 04:30:33 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 27 Jul 2022 04:30:33 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 03 Aug 2022 19:40:20 GMT
ENV PYTHON_VERSION=3.10.6
# Wed, 03 Aug 2022 20:04:58 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version
# Wed, 03 Aug 2022 20:05:00 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done
# Wed, 03 Aug 2022 20:05:00 GMT
ENV PYTHON_PIP_VERSION=22.2.1
# Wed, 03 Aug 2022 20:05:00 GMT
ENV PYTHON_SETUPTOOLS_VERSION=63.2.0
# Wed, 03 Aug 2022 20:05:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/aeca83c7ba7f9cdfd681103c4dcbf0214f6d742e/public/get-pip.py
# Wed, 03 Aug 2022 20:05:01 GMT
ENV PYTHON_GET_PIP_SHA256=d0b5909f3ab32dae9d115aa68a4b763529823ad5589c56af15cf816fca2773d6
# Wed, 03 Aug 2022 20:05:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 03 Aug 2022 20:05:13 GMT
CMD ["python3"]
# Wed, 03 Aug 2022 21:15:12 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	;
# Wed, 03 Aug 2022 21:15:12 GMT
ENV SATOSA_VERSION=8.1.1
# Wed, 03 Aug 2022 21:21:36 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa
# Wed, 03 Aug 2022 21:21:41 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz
# Wed, 03 Aug 2022 21:21:41 GMT
WORKDIR /etc/satosa
# Wed, 03 Aug 2022 21:21:42 GMT
COPY file:052229d57447119afa18a76253b740426943fcd4cf1c553c23df3445a5ed9f32 in /usr/local/bin/ 
# Wed, 03 Aug 2022 21:21:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 03 Aug 2022 21:21:42 GMT
EXPOSE 8080
# Wed, 03 Aug 2022 21:21:43 GMT
USER satosa:satosa
# Wed, 03 Aug 2022 21:21:43 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:602896d442490cd3fbb6599f0f862d3673b7cd58eca3ac842b8e09bf8d012443`  
		Last Modified: Mon, 18 Jul 2022 19:09:09 GMT  
		Size: 2.8 MB (2789923 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6556a4bf6509d5fd24900f56a6175bd811b9dd8c6f4f51e2732b6888a2b8933`  
		Last Modified: Wed, 27 Jul 2022 13:49:16 GMT  
		Size: 677.0 KB (676971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c735731e55a5ddb324dd5eb175e1f3d88895a77ea93b8fb08428ee522445708b`  
		Last Modified: Wed, 03 Aug 2022 20:44:16 GMT  
		Size: 12.8 MB (12819587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e525d9b2b00fc7130f21f05f981c44d849b279417c15b38703c3f11d3c9bd667`  
		Last Modified: Wed, 03 Aug 2022 20:44:13 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb9bc880d40f528e2c6046dd7bad61fc78f27a3fbebe3f45d1348a72ace67d9b`  
		Last Modified: Wed, 03 Aug 2022 20:44:15 GMT  
		Size: 3.0 MB (3043656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b74e25b6a705707a07e0411366545458ad05f07844bde5b7bebddd988e69068`  
		Last Modified: Wed, 03 Aug 2022 21:23:08 GMT  
		Size: 8.5 MB (8476895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:141bd7d880682fd816129f41549c798cabb9e94494f7ee7714d6e83e63606b82`  
		Last Modified: Wed, 03 Aug 2022 21:23:23 GMT  
		Size: 136.5 MB (136491944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b412f1d24946cb1e7f3d66a4ae5595d3b71ae6040af529dc49507cb1dd4e06c`  
		Last Modified: Wed, 03 Aug 2022 21:23:06 GMT  
		Size: 9.4 KB (9434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8aa237953d155695df1943bb27b03cf1cc3f1716ea63b1cf5a8b12d97cd6cea`  
		Last Modified: Wed, 03 Aug 2022 21:23:06 GMT  
		Size: 2.1 KB (2116 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
