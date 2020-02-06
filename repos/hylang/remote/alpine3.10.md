## `hylang:alpine3.10`

```console
$ docker pull hylang@sha256:b570f4e854ee5c8d323272edd2d969a96a219050d620c96fb580c5af14018df7
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

### `hylang:alpine3.10` - linux; amd64

```console
$ docker pull hylang@sha256:8af74b04c78ecb2a8453dd82829f6111f2eb1d298439da115a1bd3772f978e42
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39634033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da288feb92de70d3514a8e013ceaa40f896d8dc774641ee0b8c6a5763ce8f117`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 18:05:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 23:09:17 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2020 23:09:19 GMT
RUN apk add --no-cache ca-certificates
# Thu, 23 Jan 2020 23:09:19 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 23 Jan 2020 23:21:25 GMT
ENV PYTHON_VERSION=3.8.1
# Thu, 23 Jan 2020 23:31:14 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Jan 2020 23:31:14 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 25 Jan 2020 02:50:05 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Thu, 06 Feb 2020 01:37:07 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Thu, 06 Feb 2020 01:37:07 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Thu, 06 Feb 2020 01:37:14 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 06 Feb 2020 01:37:14 GMT
CMD ["python3"]
# Thu, 06 Feb 2020 02:14:49 GMT
ENV HY_VERSION=0.18.0
# Thu, 06 Feb 2020 02:14:54 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 06 Feb 2020 02:14:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1baf8a687be7ffea0d5471a91e524515128c316739abda79ead8135ca464ea15`  
		Last Modified: Fri, 24 Jan 2020 05:53:56 GMT  
		Size: 301.7 KB (301729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:222352708f883250caf174db6052334f4b4fabc3f12cae8cb78d77739f865a84`  
		Last Modified: Fri, 24 Jan 2020 05:55:11 GMT  
		Size: 31.9 MB (31887295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4c0cab59d3dc13fef3502588687a72f572cc5d955f765fe0c3c7b7529fd728b`  
		Last Modified: Fri, 24 Jan 2020 05:54:53 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59d143c1dde110c20c431fc45e4757170aef46b8bec9a372428fa2cec618f145`  
		Last Modified: Thu, 06 Feb 2020 01:43:58 GMT  
		Size: 1.9 MB (1892271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8297b064aa3d06294109731e88cb1c88dbfdd3cebb5b79d49a7ecf82ee26500`  
		Last Modified: Thu, 06 Feb 2020 02:17:41 GMT  
		Size: 2.8 MB (2765541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:alpine3.10` - linux; arm variant v6

```console
$ docker pull hylang@sha256:cdb29be172809e52eac6f16c7728612cf2baaee979dbd4be0b7ae9fa7df55068
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.8 MB (36775297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a6618a3a0ec3e4203bf0d16df58d4447482049a2cf4480c7c283c19bf76d9d2`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:2aa80d52585a6b34b2cc5811d46965a084e50cfb8cd183f1a88b2b1bc6556e1f in / 
# Thu, 23 Jan 2020 16:53:28 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:45:48 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 17:45:49 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2020 17:45:52 GMT
RUN apk add --no-cache ca-certificates
# Thu, 23 Jan 2020 17:45:52 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 23 Jan 2020 17:55:31 GMT
ENV PYTHON_VERSION=3.8.1
# Thu, 23 Jan 2020 18:04:28 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Jan 2020 18:04:35 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 25 Jan 2020 01:52:53 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Thu, 06 Feb 2020 01:38:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Thu, 06 Feb 2020 01:38:55 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Thu, 06 Feb 2020 01:39:11 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 06 Feb 2020 01:39:12 GMT
CMD ["python3"]
# Thu, 06 Feb 2020 02:03:22 GMT
ENV HY_VERSION=0.18.0
# Thu, 06 Feb 2020 02:04:05 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 06 Feb 2020 02:04:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:896868b7b9168cabb308702db96dc9769d10c23e20fc66f5f4abedf4c75d7642`  
		Last Modified: Thu, 23 Jan 2020 16:54:07 GMT  
		Size: 2.6 MB (2571407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f08b91b513b40f71ff412d466bdf0eff491ed79d51070e557fa4eb8e2c490139`  
		Last Modified: Thu, 23 Jan 2020 18:49:44 GMT  
		Size: 302.1 KB (302113 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1cd3ae1d71709b5172f2b14fb56aa989ab4a4ab710e75fc266194e1c99723c6`  
		Last Modified: Thu, 23 Jan 2020 18:50:28 GMT  
		Size: 29.2 MB (29242426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4490ba3ab947d36423ac54bf063400e51bd9a644475de0997138203fd513df8b`  
		Last Modified: Thu, 23 Jan 2020 18:50:01 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c2e564f52c39a5ced768776cec4d8e33900bdfdc8a4b8d9fe78c6c4a9257bf`  
		Last Modified: Thu, 06 Feb 2020 01:44:23 GMT  
		Size: 1.9 MB (1892466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac3866b848dac0f0e1a18c9123ce4450088e18551ce9b0d24186a247f9eaac79`  
		Last Modified: Thu, 06 Feb 2020 02:08:00 GMT  
		Size: 2.8 MB (2766654 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:alpine3.10` - linux; arm variant v7

```console
$ docker pull hylang@sha256:be84cf34ada2634a391f502d4b10fb702b2a92f91a1adc4af698e7ebb5808bd2
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **36.1 MB (36069732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8714a3af382a58889743122a9646bfe2abf2089e69ab8320ad3349d2262a0c6`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:31 GMT
ADD file:d05c9f9143d11d12045d4faef882e5985e6b38fabe52237dd8d8c0627a9620ab in / 
# Thu, 23 Jan 2020 16:53:32 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:16:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 19:16:24 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2020 19:16:27 GMT
RUN apk add --no-cache ca-certificates
# Thu, 23 Jan 2020 19:16:29 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 23 Jan 2020 19:26:01 GMT
ENV PYTHON_VERSION=3.8.1
# Thu, 23 Jan 2020 19:33:48 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Jan 2020 19:33:51 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 25 Jan 2020 02:29:01 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Thu, 06 Feb 2020 02:16:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Thu, 06 Feb 2020 02:16:12 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Thu, 06 Feb 2020 02:16:26 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 06 Feb 2020 02:16:27 GMT
CMD ["python3"]
# Thu, 06 Feb 2020 02:39:51 GMT
ENV HY_VERSION=0.18.0
# Thu, 06 Feb 2020 02:40:00 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 06 Feb 2020 02:40:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4e972d957a606327b0b6c2e8aa4a6045c263b7496a536298aaebf690e9d85f1d`  
		Last Modified: Thu, 23 Jan 2020 16:53:59 GMT  
		Size: 2.4 MB (2378408 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec7d55ab1b842311f10b795319bc80abba3cf485d9888a91d16898a5e2ac9c3c`  
		Last Modified: Thu, 23 Jan 2020 20:16:54 GMT  
		Size: 300.9 KB (300937 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c32aca6216c30efe2eed24b8e39944e1bf61b4caa6381090e445453472ceb89c`  
		Last Modified: Thu, 23 Jan 2020 20:18:02 GMT  
		Size: 28.7 MB (28731621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:956bbe640691931e4e01e27b634c2023b2a7c3a9c8323c659d0a21203fdb6e66`  
		Last Modified: Thu, 23 Jan 2020 20:17:25 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4080dc8b778b7d8387b3741a758cee0435055457718917661722fb35e8b3dac3`  
		Last Modified: Thu, 06 Feb 2020 02:32:26 GMT  
		Size: 1.9 MB (1892485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d40da2be156f2345120963ef26166ca2e0ac76cb12bd9fce0d1d405ed82ac565`  
		Last Modified: Thu, 06 Feb 2020 02:46:02 GMT  
		Size: 2.8 MB (2766051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:alpine3.10` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:e170e71bfc73ee483af4ffc60e7a95370a440b3c164f9f96b11e5592f83a2bdc
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.7 MB (38665926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a5552a06e58862bc3565f83d12e29ba218b05a88370a5bd9e2b68205dda5fe19`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:39 GMT
ADD file:bdfbd4b0dfb53eecc80bac65894d1e2fcfafb27dcf24ab019176e2c9f60b9a39 in / 
# Thu, 23 Jan 2020 16:54:40 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 17:59:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 21:00:16 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2020 21:00:19 GMT
RUN apk add --no-cache ca-certificates
# Thu, 23 Jan 2020 21:00:19 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 23 Jan 2020 21:08:27 GMT
ENV PYTHON_VERSION=3.8.1
# Thu, 23 Jan 2020 21:16:01 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Jan 2020 21:16:05 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 25 Jan 2020 02:13:21 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Thu, 06 Feb 2020 01:52:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Thu, 06 Feb 2020 01:52:02 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Thu, 06 Feb 2020 01:52:15 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 06 Feb 2020 01:52:16 GMT
CMD ["python3"]
# Thu, 06 Feb 2020 02:40:11 GMT
ENV HY_VERSION=0.18.0
# Thu, 06 Feb 2020 02:40:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 06 Feb 2020 02:40:23 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f07e4bcf42b862c240f4c00f2f7ed362d7d93ca15151de547beda593f3b669e5`  
		Last Modified: Thu, 23 Jan 2020 16:55:24 GMT  
		Size: 2.7 MB (2717732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85ca76d770ee8a5b1349a6e561e1973830f13e671a50fb7a5c62cebdebbcea77`  
		Last Modified: Thu, 23 Jan 2020 22:00:18 GMT  
		Size: 302.4 KB (302378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e139dfa9cfadfaa2d5e6ab55df1dea4f1c3442260b3258dad4ddbb9b9697b54`  
		Last Modified: Thu, 23 Jan 2020 22:00:56 GMT  
		Size: 31.0 MB (30987038 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a5c70ff08dec151f24948e9a7fb5b7f88308203505055c9172923651f2f2875`  
		Last Modified: Thu, 23 Jan 2020 22:00:43 GMT  
		Size: 232.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f534bb455f844d6695ff34e47423d4cc8307fc672fcc0a0b51f7f88665f0e2c`  
		Last Modified: Thu, 06 Feb 2020 02:10:36 GMT  
		Size: 1.9 MB (1892466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1141b122e8bbc12e729924005791b5275dc42a16ae944e4998ee43774d62ebc0`  
		Last Modified: Thu, 06 Feb 2020 02:46:55 GMT  
		Size: 2.8 MB (2766080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:alpine3.10` - linux; 386

```console
$ docker pull hylang@sha256:d2166f55ded85419e6daa7f8fd62cca221277c56b7b786833ec5d2b36b602f53
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.0 MB (37964897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:09fd2024db4498aab1d1d1f1653530551ce2a24fe60dcdcb6a135ac14ab8554c`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Jan 2020 16:52:57 GMT
ADD file:8c429ecc11f3cadcecc39922ce15df6b51a649929959b331fed8d1f42d722474 in / 
# Thu, 23 Jan 2020 16:52:57 GMT
CMD ["/bin/sh"]
# Fri, 24 Jan 2020 02:47:15 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 24 Jan 2020 02:47:16 GMT
ENV LANG=C.UTF-8
# Fri, 24 Jan 2020 02:47:17 GMT
RUN apk add --no-cache ca-certificates
# Fri, 24 Jan 2020 02:47:17 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 24 Jan 2020 02:58:03 GMT
ENV PYTHON_VERSION=3.8.1
# Fri, 24 Jan 2020 03:05:14 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Fri, 24 Jan 2020 03:05:15 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 25 Jan 2020 01:57:44 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Thu, 06 Feb 2020 00:47:50 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Thu, 06 Feb 2020 00:47:51 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Thu, 06 Feb 2020 00:47:57 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 06 Feb 2020 00:47:57 GMT
CMD ["python3"]
# Thu, 06 Feb 2020 01:28:24 GMT
ENV HY_VERSION=0.18.0
# Thu, 06 Feb 2020 01:28:29 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 06 Feb 2020 01:28:29 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8ad089020f8a1fd366fb13feb183e2f4c7410e2232c54b40f6a54fd56029fdf3`  
		Last Modified: Thu, 23 Jan 2020 16:53:22 GMT  
		Size: 2.8 MB (2785861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3e2a250d0b78b8817a7772e2d0f681861ea95ef5d6f89e906a846355968f4e`  
		Last Modified: Fri, 24 Jan 2020 03:40:56 GMT  
		Size: 302.3 KB (302328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9817f7acccaa86d1d117817919531efa4b6c197a8caa7752ef0dc2df39e2b10`  
		Last Modified: Fri, 24 Jan 2020 03:41:47 GMT  
		Size: 30.2 MB (30218851 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:384bab2b398378c261250f66b9cd9eefa4af00460d0a42133daf662a1e423ded`  
		Last Modified: Fri, 24 Jan 2020 03:41:34 GMT  
		Size: 231.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ebe23c2430af29da0003a2ee4c8a223f01f674f6b914a92cd84076d44f32e55`  
		Last Modified: Thu, 06 Feb 2020 00:56:03 GMT  
		Size: 1.9 MB (1892208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a38977a47d6388ad1992406bc7e21c16e0ed333ff777206961dcd82640b2754`  
		Last Modified: Thu, 06 Feb 2020 01:31:19 GMT  
		Size: 2.8 MB (2765418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:alpine3.10` - linux; ppc64le

```console
$ docker pull hylang@sha256:db299236df0586fd546140f1a348e54e62db0dc483feee78b3b272ce97b8b311
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.5 MB (40532759 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8775f3b2bdbf43640c31e5b5ac1f26d2e19828833e8c2f7b7f70868c19ffd941`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Jan 2020 16:57:54 GMT
ADD file:5e383dfaf3281b9cc17caf519d1aeba934fa92632c10afb8cc189f6ba12d9f64 in / 
# Thu, 23 Jan 2020 16:57:58 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:41:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 19:41:01 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2020 19:41:08 GMT
RUN apk add --no-cache ca-certificates
# Thu, 23 Jan 2020 19:41:12 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 23 Jan 2020 19:50:46 GMT
ENV PYTHON_VERSION=3.8.1
# Thu, 23 Jan 2020 19:59:09 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Jan 2020 19:59:17 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 25 Jan 2020 02:34:41 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Thu, 06 Feb 2020 01:27:34 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Thu, 06 Feb 2020 01:27:36 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Thu, 06 Feb 2020 01:27:58 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 06 Feb 2020 01:28:01 GMT
CMD ["python3"]
# Thu, 06 Feb 2020 02:22:07 GMT
ENV HY_VERSION=0.18.0
# Thu, 06 Feb 2020 02:22:25 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 06 Feb 2020 02:22:28 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4ae00dedbff84a762d4b8b9176da2beee50017c43fe09a5ae92c2417d5634510`  
		Last Modified: Thu, 23 Jan 2020 16:58:43 GMT  
		Size: 2.8 MB (2808535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a40439424ae05468c06dc5cd9b4cc43c689b897b0a75c281fb7c5279017124aa`  
		Last Modified: Thu, 23 Jan 2020 20:40:47 GMT  
		Size: 304.5 KB (304458 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dce04c560dde79ed580395b8896d6fdeb345946a56b962021a4be89689dfd8`  
		Last Modified: Thu, 23 Jan 2020 20:41:23 GMT  
		Size: 32.8 MB (32760773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f7a82ec2559823c4ce553d558096236ee8c44b2fab78fe6841114ce5fd2b74f`  
		Last Modified: Thu, 23 Jan 2020 20:41:14 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472b589f608d770805c429bc74e6f5c3852c9aee7b3fb5bd56181cfbb1f6fbc8`  
		Last Modified: Thu, 06 Feb 2020 01:51:24 GMT  
		Size: 1.9 MB (1892484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbdd7f3c5aa9b15eb2acf3aa68dc50c470e55e0da61c676289076bb1cc3e1a6f`  
		Last Modified: Thu, 06 Feb 2020 02:29:47 GMT  
		Size: 2.8 MB (2766279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:alpine3.10` - linux; s390x

```console
$ docker pull hylang@sha256:25502159d0a324dfa7b39b4588505cfe26e8359ea14bdb0ee0f5435fd69aed91
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39281764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc20964e3dce41a1dbef1e76b7aa01102e8723cabf4b15e7d438644752ef46fc`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Jan 2020 16:52:43 GMT
ADD file:922e12714922ae035a33d6ceb8d2683ad3e454deca21ad02b699db908443342b in / 
# Thu, 23 Jan 2020 16:52:44 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 19:28:16 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Jan 2020 19:28:16 GMT
ENV LANG=C.UTF-8
# Thu, 23 Jan 2020 19:28:17 GMT
RUN apk add --no-cache ca-certificates
# Thu, 23 Jan 2020 19:28:17 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 23 Jan 2020 19:32:48 GMT
ENV PYTHON_VERSION=3.8.1
# Thu, 23 Jan 2020 19:36:49 GMT
RUN set -ex 	&& apk add --no-cache --virtual .fetch-deps 		gnupg 		tar 		xz 		&& wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz" 	&& wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc" 	&& export GNUPGHOME="$(mktemp -d)" 	&& gpg --batch --keyserver ha.pool.sks-keyservers.net --recv-keys "$GPG_KEY" 	&& gpg --batch --verify python.tar.xz.asc python.tar.xz 	&& { command -v gpgconf > /dev/null && gpgconf --kill all || :; } 	&& rm -rf "$GNUPGHOME" python.tar.xz.asc 	&& mkdir -p /usr/src/python 	&& tar -xJC /usr/src/python --strip-components=1 -f python.tar.xz 	&& rm python.tar.xz 		&& apk add --no-cache --virtual .build-deps  		bluez-dev 		bzip2-dev 		coreutils 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	&& apk del --no-network .fetch-deps 		&& cd /usr/src/python 	&& gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)" 	&& ./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	&& make -j "$(nproc)" 		EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000" 	&& make install 		&& find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-cache --virtual .python-rundeps 	&& apk del --no-network .build-deps 		&& find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + 	&& rm -rf /usr/src/python 		&& python3 --version
# Thu, 23 Jan 2020 19:36:50 GMT
RUN cd /usr/local/bin 	&& ln -s idle3 idle 	&& ln -s pydoc3 pydoc 	&& ln -s python3 python 	&& ln -s python3-config python-config
# Sat, 25 Jan 2020 01:51:22 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Thu, 06 Feb 2020 00:48:22 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Thu, 06 Feb 2020 00:48:22 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Thu, 06 Feb 2020 00:48:27 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 06 Feb 2020 00:48:27 GMT
CMD ["python3"]
# Thu, 06 Feb 2020 01:48:52 GMT
ENV HY_VERSION=0.18.0
# Thu, 06 Feb 2020 01:48:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 06 Feb 2020 01:48:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0449d076b2977b7e7ce4c35b0fe5199d86cabaf453e869da73b2efb66d6282dd`  
		Last Modified: Thu, 23 Jan 2020 16:53:07 GMT  
		Size: 2.6 MB (2573620 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:402c9e5c67190f78971413f5f9cc6772539561ab1bac99340e6440e104424c94`  
		Last Modified: Thu, 23 Jan 2020 19:57:33 GMT  
		Size: 302.4 KB (302381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead3ac7d3a0934409c8b01b7db36c7ed0808d1820eee015b9d47a3efcc312cdc`  
		Last Modified: Thu, 23 Jan 2020 19:58:08 GMT  
		Size: 31.7 MB (31747430 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f85f4825af674a500cabef261c50271851e3bba76fae38e217bacfb28c35f0d`  
		Last Modified: Thu, 23 Jan 2020 19:57:49 GMT  
		Size: 230.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf9d0eb35422e39a87c24c7d10daaabf26ede8372b90cc040c418e96a62b7c8d`  
		Last Modified: Thu, 06 Feb 2020 00:54:43 GMT  
		Size: 1.9 MB (1892265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20609e79053e35fb3825efb07f8dc64f0dd4c519454e8c078bbffc0006980bfb`  
		Last Modified: Thu, 06 Feb 2020 01:51:26 GMT  
		Size: 2.8 MB (2765838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
