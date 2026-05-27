## `hylang:1-python3.11-alpine3.23`

```console
$ docker pull hylang@sha256:d356d2ecb85a7f5f53a029b4c5bf66fa478287757d8feb6a7f46755ab02ee2be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `hylang:1-python3.11-alpine3.23` - linux; amd64

```console
$ docker pull hylang@sha256:e6bd32bc714cf68be289246730b23df231539d59b6fc23236eaa9220a4f75d9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27304034 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a26a179e1b516316783b0307371f08fa3dacc6980743324cb279979b7968bd46`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:40 GMT
ADD alpine-minirootfs-3.23.4-x86_64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:40 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:47:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:47:04 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:47:04 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 20:47:04 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 15 Apr 2026 20:47:04 GMT
ENV PYTHON_VERSION=3.11.15
# Wed, 15 Apr 2026 20:47:04 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Wed, 15 Apr 2026 20:51:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 20:51:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 20:51:29 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:12:03 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:12:03 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:12:03 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:12:03 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6a0ac1617861a677b045b7ff88545213ec31c0ff08763195a70a4a5adda577bb`  
		Last Modified: Wed, 15 Apr 2026 20:01:46 GMT  
		Size: 3.9 MB (3864189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c671a5c7ab3e0fe7526f4ff0a233b54727a1f407035f414a73138d2b0886733`  
		Last Modified: Wed, 15 Apr 2026 20:51:36 GMT  
		Size: 455.7 KB (455655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea923c2ed79ed2d7163aacc54686501cb3339215671be89b50b62814aeffb95c`  
		Last Modified: Wed, 15 Apr 2026 20:51:37 GMT  
		Size: 16.0 MB (16020930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd8e41ac72776720a5ce79d8a0c66e75ae8d3d836cb15cc6ae0682b0b7999a11`  
		Last Modified: Wed, 15 Apr 2026 20:51:36 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537efbbd1b1d85746c7c204b4182bdabb429d72412ee1f5cf22896795bf43e18`  
		Last Modified: Wed, 27 May 2026 00:12:09 GMT  
		Size: 7.0 MB (6963012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:52d122b208a476c875b553c88b4a08f5502b86353d2fa3a57df56e1c8fafb003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.4 KB (707378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e2084f3ae10b84537d0f389bbb384f84edebaea5ee0d4d3ec4f63c6e9b627bd`

```dockerfile
```

-	Layers:
	-	`sha256:233faaa7c7f2a707b331548966fc3c854de9b47588cc6064ba84e3b4d123aa4f`  
		Last Modified: Wed, 27 May 2026 00:12:09 GMT  
		Size: 698.0 KB (697971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f10f3ba7ac54c91ba028d8567c56a8ce4a44b332c86cd007f8a4e8ef62af7a1f`  
		Last Modified: Wed, 27 May 2026 00:12:09 GMT  
		Size: 9.4 KB (9407 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.23` - linux; arm variant v6

```console
$ docker pull hylang@sha256:c406d4bec57dad10c4abf49b8c439445ff4d16be9f8ff34fdc4dff7c886d907a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.6 MB (26565297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccf458427a2ed1186807bc3cd54d8a009ffd6a87a2fddea0f2a9ecf4a7afa8c1`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:02:13 GMT
ADD alpine-minirootfs-3.23.4-armhf.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:02:13 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:33:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:33:19 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:33:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 20:33:19 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 15 Apr 2026 20:33:19 GMT
ENV PYTHON_VERSION=3.11.15
# Wed, 15 Apr 2026 20:33:19 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Wed, 15 Apr 2026 20:40:11 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 20:40:11 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 20:40:11 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:11:18 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:11:18 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:11:18 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:11:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c9cf8ef099e6e20ca4c7a2ae5b731a4beff960c0ffb88dd64fd6cdfdfe04839d`  
		Last Modified: Wed, 15 Apr 2026 20:02:17 GMT  
		Size: 3.6 MB (3571863 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8fe9fe66473fbf3fd9087fa14bfb50ac3514cb2078c196a9c49694dd31fe9aa`  
		Last Modified: Wed, 15 Apr 2026 20:40:17 GMT  
		Size: 456.5 KB (456522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17c81bcd7c12e5fb55b59d1e5bbc3d6ed2e78142c63e4b7ecc0a18b43dbef56e`  
		Last Modified: Wed, 15 Apr 2026 20:40:17 GMT  
		Size: 15.6 MB (15573372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e85f9f6f833b1de12ee750063db57958f2011a2f2c56e866c05f7eaca02f3f3`  
		Last Modified: Wed, 15 Apr 2026 20:40:16 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e4718d4f0825715afcac27764c2ebc1da913043defa169174832b369cfe715f`  
		Last Modified: Wed, 27 May 2026 00:11:23 GMT  
		Size: 7.0 MB (6963290 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:b152a91703afe71a1b75a0ae70269f754b6749c474ee0abeb460cee20a101e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.3 KB (9304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64bff7cfb89e79d3c300cff8e5fb784e078e32c0a6abc3ed186c7c7045b88cbf`

```dockerfile
```

-	Layers:
	-	`sha256:d35d046a0b4b85439fd4aabc53b1d34b85aa01362401157c5c40bc65be2fcbae`  
		Last Modified: Wed, 27 May 2026 00:11:22 GMT  
		Size: 9.3 KB (9304 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.23` - linux; arm variant v7

```console
$ docker pull hylang@sha256:ed09b26638236ce4b059a6a1bb555b0a21c87ef21c9cd4cd117e78ee439bf44e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 MB (25864622 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2272422c76ab013bf7d86b2f0749f624294a2d7e496877897c0996229eead8f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:47 GMT
ADD alpine-minirootfs-3.23.4-armv7.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:47 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:42:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:42:41 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:42:41 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 20:42:41 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 15 Apr 2026 20:42:41 GMT
ENV PYTHON_VERSION=3.11.15
# Wed, 15 Apr 2026 20:42:41 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Wed, 15 Apr 2026 20:49:46 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 20:49:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 20:49:47 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:12:03 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:12:03 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:12:03 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:12:03 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c160e404c59d6d30c66a0d74bbd17337f178f5d898a9908e18c71ce3bbe28c99`  
		Last Modified: Wed, 15 Apr 2026 20:01:53 GMT  
		Size: 3.3 MB (3283123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d1c6fe2901c593f81aef3b53acbbc5a7f161be7d476659eab8059fa90feb68c`  
		Last Modified: Wed, 15 Apr 2026 20:49:53 GMT  
		Size: 455.6 KB (455628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd9c25af093a758634c632c251f65002772fe706cca817d0638913456a260459`  
		Last Modified: Wed, 15 Apr 2026 20:49:54 GMT  
		Size: 15.2 MB (15162461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca5b96a526363c2b9adf295ebd6761b80eae81796022b162cc4d5db1e6918b4`  
		Last Modified: Wed, 15 Apr 2026 20:49:53 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66727d6b601e33814434cf56fd9361921aa4fa20654a573e3680b24dd2df56c1`  
		Last Modified: Wed, 27 May 2026 00:12:09 GMT  
		Size: 7.0 MB (6963162 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:de7777e0a87eed5619eae0b571b549e40a0269754c5134cfa12a8b514d7bd0e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.9 KB (709897 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7265148fd560e5c380af71c3ca25cb8ba204e6b2f6a16d6f2a32d9a9d17bcbac`

```dockerfile
```

-	Layers:
	-	`sha256:a55849253f253b2d86439415b60361797bb25743ab4962f0722f07462745e799`  
		Last Modified: Wed, 27 May 2026 00:12:09 GMT  
		Size: 700.4 KB (700379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f02116fef92d71fce9af4b62ab193015e51d0a53c9fcac23a7a9f054748c8d6a`  
		Last Modified: Wed, 27 May 2026 00:12:09 GMT  
		Size: 9.5 KB (9518 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.23` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:2bcf10040b09808ccc221df59183c14f4c73bf42e602fef68fba8a33c29fe38a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 MB (27813698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f45418e04bde94912717415ce0c0f699fc3f16006126d2b809e711687e6b13e8`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:01:25 GMT
ADD alpine-minirootfs-3.23.4-aarch64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:01:25 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 20:51:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 20:51:02 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 20:51:02 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 20:51:02 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 15 Apr 2026 20:51:02 GMT
ENV PYTHON_VERSION=3.11.15
# Wed, 15 Apr 2026 20:51:02 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Wed, 15 Apr 2026 20:57:55 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 20:57:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 20:57:55 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:11:51 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:11:51 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:11:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:11:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d17f077ada118cc762df373ff803592abf2dfa3ddafaa7381e364dd27a88fca7`  
		Last Modified: Wed, 15 Apr 2026 20:01:32 GMT  
		Size: 4.2 MB (4199870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e77490d7efda81dfe52b629a83d8948b45ba6b3146de01c60d870803a5e4b04`  
		Last Modified: Wed, 15 Apr 2026 20:58:03 GMT  
		Size: 457.9 KB (457909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d27834a976a180a5a91fa422f1ad444d4e03e2441fe5b64d5bc64630703bf2c`  
		Last Modified: Wed, 15 Apr 2026 20:58:03 GMT  
		Size: 16.2 MB (16192466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e6fb1ada2c00ccee137e79b13fe7c1cbcb8599d6c1b1b4267724a5c3649c961`  
		Last Modified: Wed, 15 Apr 2026 20:58:03 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b1807dbbb9f8bf4650d620bc1881a038d8900d5ee28645d2cdd8f1a631e0d9e`  
		Last Modified: Wed, 27 May 2026 00:11:58 GMT  
		Size: 7.0 MB (6963206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:236f6d1c4c0c7f9ceffd95b7c66f8f3fc3df9fd8f721117476925fa072e4d4d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.0 KB (706984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f7bad26fd3d9155d0478b1c237b77353cc0c3958bc0daa385055bc243a92ef`

```dockerfile
```

-	Layers:
	-	`sha256:2a534b9ac8bb3e04f3a229f843b83ffb420bc68bf7bda8126c7dbeb47201aa26`  
		Last Modified: Wed, 27 May 2026 00:11:57 GMT  
		Size: 697.4 KB (697425 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c60c9733b4a096a0ffba62a99e042be6abec4a49c2fbde5ffd97359ada11f776`  
		Last Modified: Wed, 27 May 2026 00:11:57 GMT  
		Size: 9.6 KB (9559 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.23` - linux; 386

```console
$ docker pull hylang@sha256:adbbe7893a1c33d9e27b8d329e5ad08683842ec7838ad2797eebda7495579fea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.3 MB (27328933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62a9b0801b8491592dfe8679ce499b240a560efb475248d5488af22eb1c4f721`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 21:33:20 GMT
ADD alpine-minirootfs-3.23.4-x86.tar.gz / # buildkit
# Wed, 15 Apr 2026 21:33:20 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:27:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:27:59 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 22:27:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 22:27:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 15 Apr 2026 22:27:59 GMT
ENV PYTHON_VERSION=3.11.15
# Wed, 15 Apr 2026 22:27:59 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Wed, 15 Apr 2026 22:33:30 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 22:33:30 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 22:33:30 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:10:50 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:10:50 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:10:50 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:10:50 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1cf9b6fc5889fdc0b6b22dd2afeea78c7c7985e06a8208c77dc71888bcf17f12`  
		Last Modified: Wed, 15 Apr 2026 21:33:25 GMT  
		Size: 3.7 MB (3690446 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f13731e2a108826f15759cbc4f18c77163e5daba5890bad5e22584a4d9d71ee`  
		Last Modified: Wed, 15 Apr 2026 22:33:38 GMT  
		Size: 456.1 KB (456109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ea8bece7dfdbc1e5b5a7af46241431683daf0bf74bc3b954234f0ca1672a40a`  
		Last Modified: Wed, 15 Apr 2026 22:33:38 GMT  
		Size: 16.2 MB (16219338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3e61bf25751a4730d622f4c7582f590f9b51acff4a1a227176fc8410483f038`  
		Last Modified: Wed, 15 Apr 2026 22:33:37 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c16d2d9e5adfc71dae3ac0d408f11279b8fc7c015055e80ed33b89bf4b66d908`  
		Last Modified: Wed, 27 May 2026 00:10:57 GMT  
		Size: 7.0 MB (6962794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:ad9aeab40339dce37daa031b0af4f376d6f61809b725a9de250ff79a41033202
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **707.3 KB (707280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28f6d9568cab9b37712412977460c96af3a4fb43d78154b38f21aaff7b25111e`

```dockerfile
```

-	Layers:
	-	`sha256:d3a1d9f573c945e427522427d289b9be9284d6ad2f4b65669785d43e458736ab`  
		Last Modified: Wed, 27 May 2026 00:10:56 GMT  
		Size: 697.9 KB (697926 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2abe69330cc0f5c5880944f2e366fc108cf2140c0171f0827c52325aa7f818da`  
		Last Modified: Wed, 27 May 2026 00:10:56 GMT  
		Size: 9.4 KB (9354 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.23` - linux; ppc64le

```console
$ docker pull hylang@sha256:93eba392478cc53212cad03bb991d2f0639b0da9a9dd7174e4de1edda8c0d6b1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **28.1 MB (28074479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7626fd4e18f14bd8c71f907755c2785706dea33e82d246c2c1926b28706dc00`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:31 GMT
ADD alpine-minirootfs-3.23.4-ppc64le.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:31 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:29:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:29:19 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 22:29:19 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 22:29:19 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 15 Apr 2026 22:29:19 GMT
ENV PYTHON_VERSION=3.11.15
# Wed, 15 Apr 2026 22:29:19 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Wed, 15 Apr 2026 22:48:33 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 22:48:33 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 22:48:33 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:24:43 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:24:43 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:24:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:24:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f14c55dbf69723970b011b8f4e3d231f8c307d6db3c80dafa55949ab7d3ea6d2`  
		Last Modified: Wed, 15 Apr 2026 20:00:46 GMT  
		Size: 3.8 MB (3830929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5188be2ff5f3202965415e6a0385e7bbfdefc53657428e80c9077bf02386c09e`  
		Last Modified: Wed, 15 Apr 2026 22:39:55 GMT  
		Size: 458.3 KB (458328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e24c703ff309bc947055377142cee424bbc54ce45af07936f3cff904efc55257`  
		Last Modified: Wed, 15 Apr 2026 22:48:46 GMT  
		Size: 16.8 MB (16821688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d39226b439b013423cc2719e252ac853402d9d3d7bc3a6b3748747ff33858412`  
		Last Modified: Wed, 15 Apr 2026 22:48:45 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f8e86f2539be7c3d6e8779ecbebaf8b51f0a47d67cfe3e0e24dd96b4b707a6e`  
		Last Modified: Wed, 27 May 2026 00:25:00 GMT  
		Size: 7.0 MB (6963286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:e20d10e267fc03ce5bbad67711b658a76ad878955d3b6ed3c1da6ac30e79e737
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.9 KB (706853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d230becd9a7f69348a7bf664b075f0dfe6bd4598274c845a2acd9e9f190d162a`

```dockerfile
```

-	Layers:
	-	`sha256:d3f383b33f48075c44b321e817ee1eeefa2ae14c39669faabc8a6b8e4dbfcdfe`  
		Last Modified: Wed, 27 May 2026 00:25:00 GMT  
		Size: 697.4 KB (697378 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9fb8114064d779e8b3d0006df9b90cfe1b3f7726caab2cb027a2dda97c478825`  
		Last Modified: Wed, 27 May 2026 00:25:00 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.23` - linux; riscv64

```console
$ docker pull hylang@sha256:ec53283daae1a4b9a7f06f7bc99d2e70ba072b9505d146cf9d823f30872ee8de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.9 MB (26894446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d3a7bdb9db5a10d4ff325ca408577042950f4bac027966c19cac1f680e02fb3`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:30:47 GMT
ADD alpine-minirootfs-3.23.4-riscv64.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:30:47 GMT
CMD ["/bin/sh"]
# Thu, 16 Apr 2026 19:57:53 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2026 19:57:53 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2026 19:57:53 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Thu, 16 Apr 2026 19:57:53 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 16 Apr 2026 19:57:53 GMT
ENV PYTHON_VERSION=3.11.15
# Thu, 16 Apr 2026 19:57:53 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Thu, 16 Apr 2026 21:05:56 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 16 Apr 2026 21:05:57 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 16 Apr 2026 21:05:57 GMT
CMD ["python3"]
# Sat, 18 Apr 2026 06:44:00 GMT
ENV HY_VERSION=1.2.0
# Sat, 18 Apr 2026 06:44:00 GMT
ENV HYRULE_VERSION=1.0.1
# Sat, 18 Apr 2026 06:44:00 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 18 Apr 2026 06:44:00 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:352acc3ce0e18a8eecba8cebabbfac8f5d264e89513a883c1566d91d15491462`  
		Last Modified: Wed, 15 Apr 2026 20:31:19 GMT  
		Size: 3.6 MB (3587662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5938584958193c97edd29fd7dcb625012c86f6f8b1b1e786fedfa747f26cf307`  
		Last Modified: Thu, 16 Apr 2026 20:33:08 GMT  
		Size: 456.0 KB (455998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6932187b68f1bf0b128b8b04db5e85c5b73103a8c8de4496bb50ee0c09107bc`  
		Last Modified: Thu, 16 Apr 2026 21:06:49 GMT  
		Size: 15.9 MB (15906614 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0358a6a13147b675ce9c8f5df0fe9e39f54c74fd4aef6e69f49b52bd8db6ab2`  
		Last Modified: Thu, 16 Apr 2026 21:06:46 GMT  
		Size: 258.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7b96b64b7737ceaec7592c9eb99332b2492af8c23bfbbe77884637b8c8bf764`  
		Last Modified: Sat, 18 Apr 2026 06:44:44 GMT  
		Size: 6.9 MB (6943914 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:059dc1d9cd24cafabf6aa7ae0e34b13cf804a1c2dd738ea11ab590ffe738abb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.8 KB (706849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb6f98b08da5a60abd810e7e3a459c5cb9aa64f0593d00d0f78e09db69cee069`

```dockerfile
```

-	Layers:
	-	`sha256:4f9b5755102ca5e8f34defe02ef6f4b436c8aeb49d9c5506e0164418b5ee943d`  
		Last Modified: Sat, 18 Apr 2026 06:44:43 GMT  
		Size: 697.4 KB (697374 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be564d83969484198a564212f23c36c1ffd8db7c1c7d4b73a14dd7fda7e33dee`  
		Last Modified: Sat, 18 Apr 2026 06:44:43 GMT  
		Size: 9.5 KB (9475 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.23` - linux; s390x

```console
$ docker pull hylang@sha256:100266cc4757e4769a6ed93f332313eded5d9c52051e2f00dd2fed5120343ad5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27603787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:862141908631465245916a01018e55620acdf836068cd52c61df4f4559a7af64`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 15 Apr 2026 20:00:34 GMT
ADD alpine-minirootfs-3.23.4-s390x.tar.gz / # buildkit
# Wed, 15 Apr 2026 20:00:34 GMT
CMD ["/bin/sh"]
# Wed, 15 Apr 2026 22:55:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 15 Apr 2026 22:55:54 GMT
ENV LANG=C.UTF-8
# Wed, 15 Apr 2026 22:55:54 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 15 Apr 2026 22:55:54 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 15 Apr 2026 22:55:54 GMT
ENV PYTHON_VERSION=3.11.15
# Wed, 15 Apr 2026 22:55:54 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Wed, 15 Apr 2026 23:05:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 15 Apr 2026 23:05:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 15 Apr 2026 23:05:34 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:19:14 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:19:14 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:19:14 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:19:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:13188190f2c53fa4e825ed24ee94f77177787a7ddde7687d5fadb7431f136a37`  
		Last Modified: Wed, 15 Apr 2026 20:00:44 GMT  
		Size: 3.7 MB (3726532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d60dd658b4dca3ca9b4cf29ac953b460e7ff01f412fe94505c35500008f48e`  
		Last Modified: Wed, 15 Apr 2026 23:06:08 GMT  
		Size: 456.7 KB (456680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dbcb84469700cf86fd3b50015e0a02408d2f779299bfebe3f9afde960a6018f`  
		Last Modified: Wed, 15 Apr 2026 23:06:11 GMT  
		Size: 16.5 MB (16457256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e18bfa1ffff5eae6fdd3a7116165fd4b5523b870ce75093d8235b9d537a696ca`  
		Last Modified: Wed, 15 Apr 2026 23:06:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c5c863e25e9fbf47d6aca6b6b7825d0ad2026dd0f2adc85f00818b1be9c09cc`  
		Last Modified: Wed, 27 May 2026 00:19:28 GMT  
		Size: 7.0 MB (6963070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.23` - unknown; unknown

```console
$ docker pull hylang@sha256:1a64098485d5a731e8e5ab39ae1437423dad622a373ea2eb9b9bd7489e07c353
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.7 KB (706727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:265fdd7b42ebe86815c2e23f4a1e03494c6cfed607a3935fb165977869280e3d`

```dockerfile
```

-	Layers:
	-	`sha256:fd8c5ad34e3f82657c8a9d7fc8d5d74746e1b3db71a98f8a8ddc8d6f8028af17`  
		Last Modified: Wed, 27 May 2026 00:19:28 GMT  
		Size: 697.3 KB (697320 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03250409fb87ae0efd0b8881fa37a9c5b2e4f81e30857e46280a7399d6b1242f`  
		Last Modified: Wed, 27 May 2026 00:19:27 GMT  
		Size: 9.4 KB (9407 bytes)  
		MIME: application/vnd.in-toto+json
