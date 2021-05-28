## `hylang:python3.10-rc-alpine3.12`

```console
$ docker pull hylang@sha256:bc29172c5af0347f77dedabbdf4045064caf82b2b952d09048f5365699b7d858
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

### `hylang:python3.10-rc-alpine3.12` - linux; amd64

```console
$ docker pull hylang@sha256:794e479e0e6562769c712bd08150b08ee489d872b79deeafd109e42a1f8c2157
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.9 MB (20851405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71a2e8689b3a2a846cb690150a7bfe29290f597c0952ebf32d3d3a17d4325011`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 21:48:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Apr 2021 04:33:20 GMT
ENV LANG=C.UTF-8
# Thu, 15 Apr 2021 04:33:21 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Thu, 15 Apr 2021 04:33:22 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 May 2021 17:59:02 GMT
ENV PYTHON_VERSION=3.10.0b1
# Tue, 04 May 2021 18:07:54 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Tue, 04 May 2021 18:07:55 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 24 May 2021 19:33:01 GMT
ENV PYTHON_PIP_VERSION=21.1.2
# Mon, 24 May 2021 19:33:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/936e08ce004d0b2fae8952c50f7ccce1bc578ce5/public/get-pip.py
# Mon, 24 May 2021 19:33:02 GMT
ENV PYTHON_GET_PIP_SHA256=8890955d56a8262348470a76dc432825f61a84a54e2985a86cd520f656a6e220
# Mon, 24 May 2021 19:33:08 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 24 May 2021 19:33:08 GMT
CMD ["python3"]
# Mon, 24 May 2021 20:01:37 GMT
ENV HY_VERSION=1.0a1
# Mon, 24 May 2021 20:01:42 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Mon, 24 May 2021 20:01:42 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f10fb83f8d87c8aff3b967582dc9e6ebc4ae331f587a295e74942cd23ae6de90`  
		Last Modified: Thu, 15 Apr 2021 08:46:46 GMT  
		Size: 655.7 KB (655732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0120f345b3e6f5c144a189111d245c2147279236456709917ce517912e754db`  
		Last Modified: Tue, 04 May 2021 19:20:56 GMT  
		Size: 11.7 MB (11746800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56949793ec3a222a26f939f6acfe7a09a5168716215b3465f756ad51c5df2674`  
		Last Modified: Tue, 04 May 2021 19:20:53 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499a8589b474f1deb1a5402602db74799c96d2e7be9dc2af221e681cb23b0855`  
		Last Modified: Mon, 24 May 2021 19:39:41 GMT  
		Size: 2.3 MB (2348410 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:471b93315efa4083b92e1466bc2b9b2fb85b32d209494fef10d1be11415b4048`  
		Last Modified: Mon, 24 May 2021 20:06:52 GMT  
		Size: 3.3 MB (3299662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-rc-alpine3.12` - linux; arm variant v6

```console
$ docker pull hylang@sha256:17db57ee0235588343e73e2f0cadc7dd2dd5170f0783f00cce57d17f31eeeccc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.3 MB (20282889 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:17da76bdcb2aa676c035fb4fcfe22f1cd4b45fa255a75ca9aafac222770141ed`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Thu, 27 May 2021 07:23:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 May 2021 07:23:21 GMT
ENV LANG=C.UTF-8
# Thu, 27 May 2021 07:23:22 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Thu, 27 May 2021 07:23:23 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 27 May 2021 07:23:23 GMT
ENV PYTHON_VERSION=3.10.0b1
# Thu, 27 May 2021 07:33:30 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Thu, 27 May 2021 07:33:31 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 27 May 2021 07:33:31 GMT
ENV PYTHON_PIP_VERSION=21.1.2
# Thu, 27 May 2021 07:33:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/936e08ce004d0b2fae8952c50f7ccce1bc578ce5/public/get-pip.py
# Thu, 27 May 2021 07:33:32 GMT
ENV PYTHON_GET_PIP_SHA256=8890955d56a8262348470a76dc432825f61a84a54e2985a86cd520f656a6e220
# Thu, 27 May 2021 07:33:40 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 27 May 2021 07:33:40 GMT
CMD ["python3"]
# Thu, 27 May 2021 13:34:02 GMT
ENV HY_VERSION=1.0a1
# Thu, 27 May 2021 13:34:10 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 27 May 2021 13:34:10 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ba3969ddf8c8bdc760ebcd0638fe212ef95372905d03ac9b2d9909f7f937ceb`  
		Last Modified: Thu, 27 May 2021 11:40:22 GMT  
		Size: 659.6 KB (659620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45e03a61aae961a7f51a389e26ebba20851a8eeb3e44123361e4b3917f083ba4`  
		Last Modified: Thu, 27 May 2021 11:40:24 GMT  
		Size: 11.4 MB (11369662 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e05a44e12597b8a94e3127551fc70541fb3753851afc1d2e044e9a4a97ed9ee`  
		Last Modified: Thu, 27 May 2021 11:40:20 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:502b4ac2649acb3577d3584e12440f7d0a1a58ef5ead7687bb8743455851ac8a`  
		Last Modified: Thu, 27 May 2021 11:40:21 GMT  
		Size: 2.3 MB (2348416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a08e675225897d619f7baa8259278fc3707e8982628e3263dbbe0fe450ff2d`  
		Last Modified: Thu, 27 May 2021 13:39:59 GMT  
		Size: 3.3 MB (3299705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-rc-alpine3.12` - linux; arm variant v7

```console
$ docker pull hylang@sha256:eaedeee42f193f26cc3a774403de3995533317667028de5c8c0dd9ce166830fc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **19.1 MB (19087850 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e5a0531581c8078774a57d61b950111e948dc938b05aa22944ef62ad468019`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 14 Apr 2021 18:57:50 GMT
ADD file:d844cc7b5e00fb62be39d903a2fb4a08f700e75112c8eef1f31101e846ed010d in / 
# Wed, 14 Apr 2021 18:57:52 GMT
CMD ["/bin/sh"]
# Wed, 26 May 2021 11:59:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 May 2021 11:59:54 GMT
ENV LANG=C.UTF-8
# Wed, 26 May 2021 11:59:55 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 26 May 2021 11:59:56 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 26 May 2021 11:59:56 GMT
ENV PYTHON_VERSION=3.10.0b1
# Wed, 26 May 2021 12:06:44 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Wed, 26 May 2021 12:06:45 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Wed, 26 May 2021 12:06:45 GMT
ENV PYTHON_PIP_VERSION=21.1.2
# Wed, 26 May 2021 12:06:46 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/936e08ce004d0b2fae8952c50f7ccce1bc578ce5/public/get-pip.py
# Wed, 26 May 2021 12:06:46 GMT
ENV PYTHON_GET_PIP_SHA256=8890955d56a8262348470a76dc432825f61a84a54e2985a86cd520f656a6e220
# Wed, 26 May 2021 12:06:54 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 26 May 2021 12:06:54 GMT
CMD ["python3"]
# Wed, 26 May 2021 23:08:50 GMT
ENV HY_VERSION=1.0a1
# Wed, 26 May 2021 23:08:58 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 26 May 2021 23:08:58 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:420c7481a3a76d5d12df768d2745ddbe40357df0af780c756a5a7d1f2a43d288`  
		Last Modified: Wed, 14 Apr 2021 18:58:46 GMT  
		Size: 2.4 MB (2409178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a73ed3bcb331b81d4c30d697560c3000f2eb8ee6b39d71b121b7309d67a2f438`  
		Last Modified: Wed, 26 May 2021 14:55:36 GMT  
		Size: 652.0 KB (651981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2f8a0cf8f38d1e46defa4725698be02d2847c624cb39ce412162a13bd2cf831`  
		Last Modified: Wed, 26 May 2021 14:55:38 GMT  
		Size: 10.4 MB (10378341 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9a2e3adfd7943ddd73edf787ef7b9f2f53919297124698e319cfaf2865c0bd2`  
		Last Modified: Wed, 26 May 2021 14:55:35 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1e272b271e022d11a851b7094b9a8828679a658d81b0cedda2289cc8bdbcea2`  
		Last Modified: Wed, 26 May 2021 14:55:36 GMT  
		Size: 2.3 MB (2348403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af4fa8e8827a80e437c560adfac7cbbcca52fcfab35fce4b9fe90da73216c989`  
		Last Modified: Wed, 26 May 2021 23:18:10 GMT  
		Size: 3.3 MB (3299714 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-rc-alpine3.12` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:425c1f70e5c4badd005322ca4f9a0419d29484df4c73d08516a788a70b4d1236
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.8 MB (20845957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9df78ee772568f55281eec5262454a13e648f0f9b12f6384b36bcaf051cf4e9`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 26 May 2021 21:19:32 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 27 May 2021 09:44:43 GMT
ENV LANG=C.UTF-8
# Thu, 27 May 2021 09:44:44 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Thu, 27 May 2021 09:44:44 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 27 May 2021 09:44:45 GMT
ENV PYTHON_VERSION=3.10.0b1
# Thu, 27 May 2021 09:52:47 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Thu, 27 May 2021 09:52:48 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Thu, 27 May 2021 09:52:48 GMT
ENV PYTHON_PIP_VERSION=21.1.2
# Thu, 27 May 2021 09:52:48 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/936e08ce004d0b2fae8952c50f7ccce1bc578ce5/public/get-pip.py
# Thu, 27 May 2021 09:52:48 GMT
ENV PYTHON_GET_PIP_SHA256=8890955d56a8262348470a76dc432825f61a84a54e2985a86cd520f656a6e220
# Thu, 27 May 2021 09:52:55 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 27 May 2021 09:52:56 GMT
CMD ["python3"]
# Thu, 27 May 2021 19:24:31 GMT
ENV HY_VERSION=1.0a1
# Thu, 27 May 2021 19:24:36 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 27 May 2021 19:24:36 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f69a4f63bded7e204cb635c5c84bcd01163263c303f674e16403b75df63fb51`  
		Last Modified: Thu, 27 May 2021 12:10:58 GMT  
		Size: 658.3 KB (658294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41394a4a719f423a55c5c9570f1888eb6cec2e5f840c143ac570fb0ccb71632f`  
		Last Modified: Thu, 27 May 2021 12:10:59 GMT  
		Size: 11.8 MB (11828807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7234d303aa6e173900aa9c93115509b0edc993e82334530c1f9ed99655bb413a`  
		Last Modified: Thu, 27 May 2021 12:10:57 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2c9a097eaccb2b3ff611f96b42346dfbf8d1054bd45a973c4507f43504a7ff3`  
		Last Modified: Thu, 27 May 2021 12:10:58 GMT  
		Size: 2.3 MB (2348432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52280fb6c8c1c258fb7abc2c78d762bc797d5762f479af0dc0d38447db733734`  
		Last Modified: Thu, 27 May 2021 19:31:55 GMT  
		Size: 3.3 MB (3299496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-rc-alpine3.12` - linux; 386

```console
$ docker pull hylang@sha256:aab7bcfd39f735532a1ba9e8941c23b517ea8b9514246449bc68dd31d341795f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.1 MB (21094187 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06200e390b7821714cb33f2fa02f3ca6233415a8ee90b50751631d04d4395307`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:25:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 14 Apr 2021 19:25:48 GMT
ENV LANG=C.UTF-8
# Wed, 14 Apr 2021 19:25:49 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Wed, 14 Apr 2021 19:25:50 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 May 2021 18:26:55 GMT
ENV PYTHON_VERSION=3.10.0b1
# Tue, 04 May 2021 18:39:25 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Tue, 04 May 2021 18:39:25 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 24 May 2021 19:52:16 GMT
ENV PYTHON_PIP_VERSION=21.1.2
# Mon, 24 May 2021 19:52:16 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/936e08ce004d0b2fae8952c50f7ccce1bc578ce5/public/get-pip.py
# Mon, 24 May 2021 19:52:16 GMT
ENV PYTHON_GET_PIP_SHA256=8890955d56a8262348470a76dc432825f61a84a54e2985a86cd520f656a6e220
# Mon, 24 May 2021 19:52:24 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 24 May 2021 19:52:24 GMT
CMD ["python3"]
# Mon, 24 May 2021 20:34:32 GMT
ENV HY_VERSION=1.0a1
# Mon, 24 May 2021 20:34:37 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Mon, 24 May 2021 20:34:38 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af60c61b427f5518b074029ecdcbbd47445fa852df39326d1ecbeee2d7eb3d5`  
		Last Modified: Wed, 14 Apr 2021 23:34:53 GMT  
		Size: 661.9 KB (661850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e0f2901cc63e9c0b57d0e31335396939fcecd6cebfa02becd4379095a8b8cc`  
		Last Modified: Tue, 04 May 2021 20:04:51 GMT  
		Size: 12.0 MB (11988252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a64010064f1779540929c20fa938c54dbeb1c3223a72b09d580c6a9360387c8`  
		Last Modified: Tue, 04 May 2021 20:04:48 GMT  
		Size: 233.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c440b965754d5191b0182b4f1da6e8a7b06ce17f86f613f2ed2d1108d201fd60`  
		Last Modified: Mon, 24 May 2021 20:03:00 GMT  
		Size: 2.3 MB (2348432 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b6d5a6093b2cdf3d162790cc56a1ab013327da1380c11cfb4e266ce75a4a13`  
		Last Modified: Mon, 24 May 2021 20:41:49 GMT  
		Size: 3.3 MB (3299625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-rc-alpine3.12` - linux; ppc64le

```console
$ docker pull hylang@sha256:e7f2fd28f0a60d8e798adec2b0d7d4ea2a8d5149606dff674df91ca0d8a8593e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **21.7 MB (21662777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f99c61c407242a14810d574c8b37bddf9fd939b012b4fe2574676dc1d5d301b`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 14 Apr 2021 19:31:22 GMT
ADD file:f8b081207f6d35f8ebd06aa471e350644151d183801f678def586d8f37e81366 in / 
# Wed, 14 Apr 2021 19:31:29 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 05:21:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Apr 2021 05:21:35 GMT
ENV LANG=C.UTF-8
# Thu, 15 Apr 2021 05:21:43 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Thu, 15 Apr 2021 05:21:51 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 May 2021 19:08:47 GMT
ENV PYTHON_VERSION=3.10.0b1
# Tue, 04 May 2021 19:20:28 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Tue, 04 May 2021 19:20:46 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 24 May 2021 19:25:51 GMT
ENV PYTHON_PIP_VERSION=21.1.2
# Mon, 24 May 2021 19:25:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/936e08ce004d0b2fae8952c50f7ccce1bc578ce5/public/get-pip.py
# Mon, 24 May 2021 19:26:02 GMT
ENV PYTHON_GET_PIP_SHA256=8890955d56a8262348470a76dc432825f61a84a54e2985a86cd520f656a6e220
# Mon, 24 May 2021 19:26:52 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 24 May 2021 19:26:57 GMT
CMD ["python3"]
# Mon, 24 May 2021 22:22:27 GMT
ENV HY_VERSION=1.0a1
# Mon, 24 May 2021 22:23:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Mon, 24 May 2021 22:23:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:45707b9629c4ab8c6046680737229218fe844f38d08e5458b24605e1dbfd2709`  
		Last Modified: Wed, 14 Apr 2021 19:32:50 GMT  
		Size: 2.8 MB (2806750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b72e0cf4bbf8f6a43d488c1e80e36218d61c3dcc8c6ebd5ef3dd9c1fd0816f8e`  
		Last Modified: Thu, 15 Apr 2021 06:59:09 GMT  
		Size: 664.6 KB (664628 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585a9e96cd93e5f960e27606617b0de8b2855fd6c8b4af85aefd2c0092d551f3`  
		Last Modified: Tue, 04 May 2021 21:19:25 GMT  
		Size: 12.5 MB (12542228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604a5466e72a149fbba046cf97825fe92e44cbbd0387f0d0f0ca4423de9f6528`  
		Last Modified: Tue, 04 May 2021 21:19:22 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be046005f74c2f843614c886cba7ec3ef05a1cc47d4e19e65df9246d0c76b39a`  
		Last Modified: Mon, 24 May 2021 19:49:13 GMT  
		Size: 2.3 MB (2348584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e79fbaa5f1808deb2eb006387586521251a52b925e99eeee8132f7f5c4ba7c33`  
		Last Modified: Mon, 24 May 2021 22:28:13 GMT  
		Size: 3.3 MB (3300352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.10-rc-alpine3.12` - linux; s390x

```console
$ docker pull hylang@sha256:fed36269c43543ff0c5753b75c9346771ae9d85e6273a7592dc2639a90804ba2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **20.6 MB (20607396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36bafacc4ebef3414cfaecd4569fce00cddea200da2b01112593ea73c0a69470`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 14 Apr 2021 18:41:42 GMT
ADD file:c73a5ff435939cdc9d621ee9dc2aa5a54a5f5e0241caae8dc948c03c423d9fef in / 
# Wed, 14 Apr 2021 18:41:42 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 03:03:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 15 Apr 2021 03:03:36 GMT
ENV LANG=C.UTF-8
# Thu, 15 Apr 2021 03:03:39 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	;
# Thu, 15 Apr 2021 03:03:39 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 May 2021 18:27:17 GMT
ENV PYTHON_VERSION=3.10.0b1
# Tue, 04 May 2021 18:35:24 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 		LDFLAGS="-Wl,--strip-all" 	&& make install 	&& rm -rf /usr/src/python 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& python3 --version
# Tue, 04 May 2021 18:35:27 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Mon, 24 May 2021 19:48:51 GMT
ENV PYTHON_PIP_VERSION=21.1.2
# Mon, 24 May 2021 19:48:52 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/936e08ce004d0b2fae8952c50f7ccce1bc578ce5/public/get-pip.py
# Mon, 24 May 2021 19:48:52 GMT
ENV PYTHON_GET_PIP_SHA256=8890955d56a8262348470a76dc432825f61a84a54e2985a86cd520f656a6e220
# Mon, 24 May 2021 19:49:02 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Mon, 24 May 2021 19:49:03 GMT
CMD ["python3"]
# Mon, 24 May 2021 20:18:09 GMT
ENV HY_VERSION=1.0a1
# Mon, 24 May 2021 20:18:17 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Mon, 24 May 2021 20:18:19 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:27efec644c4207cbc4d1400f84f3402937aab5ce72489976148896e42a219820`  
		Last Modified: Wed, 14 Apr 2021 18:42:24 GMT  
		Size: 2.6 MB (2568428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3003d9f853d0f905ce6502084f7a6423cd871f2dbf70b8a1fdc6ada2253b5064`  
		Last Modified: Thu, 15 Apr 2021 06:50:17 GMT  
		Size: 660.5 KB (660522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90832dcd5c84fb2b2e2fac378528e551d44d9b1666fe1c550cde6afaa3362f22`  
		Last Modified: Tue, 04 May 2021 19:50:29 GMT  
		Size: 11.7 MB (11730152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc2a6f218ab1913dc69d17950c9814a56fb5c59fb61994ec10df43965d7c614`  
		Last Modified: Tue, 04 May 2021 19:50:26 GMT  
		Size: 234.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a8b1a9e861425c2ad9402a4fd2a707ae573f7d2a5b3f0b29e0d63ac88ee9d6c`  
		Last Modified: Mon, 24 May 2021 19:55:34 GMT  
		Size: 2.3 MB (2348411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8ac41f5e7ca71e9a81ef02051d439947595686f527ff5a683fa9d5008547e7c`  
		Last Modified: Mon, 24 May 2021 20:22:05 GMT  
		Size: 3.3 MB (3299649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
