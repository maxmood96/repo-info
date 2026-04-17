## `hylang:python3.11-alpine3.22`

```console
$ docker pull hylang@sha256:c7a32e45b87ff573719234de92bab64a976e0d3da07b07fcc5115250ab2bb7ea
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

### `hylang:python3.11-alpine3.22` - linux; amd64

```console
$ docker pull hylang@sha256:9a4d4d661f1893584e4fc9168817accad6529dfcb3eb5f9d94f3729f30f5955e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27159320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f33c804748df84ef26d281fe03555b61afad7c8c3b4a382ca5720517571a061`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:30:59 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:30:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:30:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 17 Apr 2026 00:30:59 GMT
ENV PYTHON_VERSION=3.11.15
# Fri, 17 Apr 2026 00:30:59 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Fri, 17 Apr 2026 00:35:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:35:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:35:59 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:16:14 GMT
ENV HY_VERSION=1.2.0
# Fri, 17 Apr 2026 01:16:14 GMT
ENV HYRULE_VERSION=1.0.1
# Fri, 17 Apr 2026 01:16:14 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 17 Apr 2026 01:16:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6df53a89c0f42f83bc7aabe3219368a7a07f91c01d26df826ad018dcdcbe12c2`  
		Last Modified: Fri, 17 Apr 2026 00:36:06 GMT  
		Size: 455.0 KB (454972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ca0c990548b90611452accb73caff22dd22ed3b8f9a5ff4e57794013cfe79ed`  
		Last Modified: Fri, 17 Apr 2026 00:36:06 GMT  
		Size: 16.0 MB (15953262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2468f2064dc96c59da89b52bee21c81fbb8fed8cede1e44484fce7b7bc642c6a`  
		Last Modified: Fri, 17 Apr 2026 00:36:05 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f95701454708c52394ec96a8a6b3da6d51ff0b767bf9271e345f073226b0f56`  
		Last Modified: Fri, 17 Apr 2026 01:16:20 GMT  
		Size: 6.9 MB (6942649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:9e8bb8d498eab75b5d6fa2537ce305c602f03ec73de484280195b61e6f582ce0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.0 KB (706043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3aa314f365788c974b24bca34f880b3825447791bb54888ec0123f25f4735a0`

```dockerfile
```

-	Layers:
	-	`sha256:6f30c0c2b5b88a4c5d274ec9bef7351efdeb00dc151565fafaec153c24d6a5ac`  
		Last Modified: Fri, 17 Apr 2026 01:16:20 GMT  
		Size: 697.9 KB (697940 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4c80d99e624027ea3b102950bb80839ac35b1d1c565d20a17ff17a11c70f3f4`  
		Last Modified: Fri, 17 Apr 2026 01:16:19 GMT  
		Size: 8.1 KB (8103 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.22` - linux; arm variant v6

```console
$ docker pull hylang@sha256:7fdd992902f4ca551ba31e94e504f464bd98e7e5443031e67b01bfae81b4f053
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26402696 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fef272a9a9a5b9408014322eb5cbedf9e2697e10dd40bb6ff5e3588d8f401c1a`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:27 GMT
ADD alpine-minirootfs-3.22.4-armhf.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:27 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:32:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:32:14 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:32:14 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:32:14 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 17 Apr 2026 00:32:14 GMT
ENV PYTHON_VERSION=3.11.15
# Fri, 17 Apr 2026 00:32:14 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Fri, 17 Apr 2026 00:38:43 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:38:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:38:43 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:15:33 GMT
ENV HY_VERSION=1.2.0
# Fri, 17 Apr 2026 01:15:33 GMT
ENV HYRULE_VERSION=1.0.1
# Fri, 17 Apr 2026 01:15:33 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 17 Apr 2026 01:15:33 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:08c654e9a4409dbbeb5faba9659360f33dbc6f7a6d79ebebe08f57d22a1b76fc`  
		Last Modified: Thu, 16 Apr 2026 23:53:31 GMT  
		Size: 3.5 MB (3507383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fff0462c99f42d64940d449078f07489e2cad7e67b06c74315442afdadf90073`  
		Last Modified: Fri, 17 Apr 2026 00:38:48 GMT  
		Size: 455.9 KB (455909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b2236b8fa033f13b71ea88a9bd43b091c0c32d1943d48f595475bcf62051712`  
		Last Modified: Fri, 17 Apr 2026 00:38:48 GMT  
		Size: 15.5 MB (15496548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8157b6f1d10ee717becf1fa16e238be380db625b7f76841e4b6bbed958bfbcf6`  
		Last Modified: Fri, 17 Apr 2026 00:38:48 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e86f157c9d42d9dcf043d0459001df9120e2408c8d0187191f17285c046ec7ac`  
		Last Modified: Fri, 17 Apr 2026 01:15:38 GMT  
		Size: 6.9 MB (6942610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:4311e20028561df1ac7e04a00d58c749f26dbe0e3d84b316a6d9595b363ff54c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **8.0 KB (7968 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f022fd038d35a47a27659c752f7d53e5d7f0d1ff80ba97d3d2cd984344bb0a9`

```dockerfile
```

-	Layers:
	-	`sha256:9654868e5b5128c7071d238692a98aa6810442aa487d9ee4243dc814bc2307e1`  
		Last Modified: Fri, 17 Apr 2026 01:15:38 GMT  
		Size: 8.0 KB (7968 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.22` - linux; arm variant v7

```console
$ docker pull hylang@sha256:86ef8b02bc1358db8b544572fbaef6453fa5897836d8a346e8e64951e930abe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.7 MB (25715077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53497797ffa9ede874dcb56f4b90ee26e6c1106954ce7e96a4dc4cd49663561b`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:54:02 GMT
ADD alpine-minirootfs-3.22.4-armv7.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:54:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:38:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:38:20 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:38:20 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:38:20 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 17 Apr 2026 00:38:20 GMT
ENV PYTHON_VERSION=3.11.15
# Fri, 17 Apr 2026 00:38:20 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Fri, 17 Apr 2026 00:44:52 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:44:52 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:44:52 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:18:47 GMT
ENV HY_VERSION=1.2.0
# Fri, 17 Apr 2026 01:18:47 GMT
ENV HYRULE_VERSION=1.0.1
# Fri, 17 Apr 2026 01:18:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 17 Apr 2026 01:18:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:99e8c7f1cf08d3156a369084c1a1fd745878aa29f4a0f55d73e953b93f0b7a93`  
		Last Modified: Thu, 16 Apr 2026 23:54:07 GMT  
		Size: 3.2 MB (3225830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2883c41d5cffede81ce509208a0bebb67686bd9f6d3a66450ef1b0d4680dab3`  
		Last Modified: Fri, 17 Apr 2026 00:44:59 GMT  
		Size: 455.0 KB (455005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5320d7fb18affe77fe5966adecd6c28f2cc065d39324e0ed5a04034280a98a64`  
		Last Modified: Fri, 17 Apr 2026 00:44:59 GMT  
		Size: 15.1 MB (15091376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f79b0bc62561b972349f5f2858cddf96bc20a7dd4592ae5647f51afbf2491bf5`  
		Last Modified: Fri, 17 Apr 2026 00:44:59 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:414d51a7b02641415e07e0f4f0151cf2011ae77ac24453495df698d528a48fb4`  
		Last Modified: Fri, 17 Apr 2026 01:18:53 GMT  
		Size: 6.9 MB (6942617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:57b6acd7afb32290346f73a0b183c4df0e66c533afbf5c171e88ed7d1658fa5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **709.1 KB (709149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80b56432e779ac2be0a2945549d1b615de9913ad1661807a69bab39a1b15460e`

```dockerfile
```

-	Layers:
	-	`sha256:52cef46eabcf110ab1fb159f9c4a391beb81b38882dc308fdaf2e50f7cdb71d7`  
		Last Modified: Fri, 17 Apr 2026 01:18:53 GMT  
		Size: 701.0 KB (700966 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ba6374fc3021b89b914b7eb072160de3c82dfeff853cc0b2f05f0bef3ecd536`  
		Last Modified: Fri, 17 Apr 2026 01:18:53 GMT  
		Size: 8.2 KB (8183 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:edea602e5167a86272a20fad75aa561220b1cf4467ec853b81c87c348bc84859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.6 MB (27572457 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dfefa786954f9ed7858d2aac9b4ee70816663593ecd8395734341db947b8aa98`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:34:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:34:01 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 00:34:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:34:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 17 Apr 2026 00:34:01 GMT
ENV PYTHON_VERSION=3.11.15
# Fri, 17 Apr 2026 00:34:01 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Fri, 17 Apr 2026 00:39:54 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:39:54 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:39:54 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:40:18 GMT
ENV HY_VERSION=1.2.0
# Fri, 17 Apr 2026 01:40:18 GMT
ENV HYRULE_VERSION=1.0.1
# Fri, 17 Apr 2026 01:40:18 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 17 Apr 2026 01:40:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68f21ca51a14dcd86052a498fa06f0530189b9ff326a749eb27917a1a8a57268`  
		Last Modified: Fri, 17 Apr 2026 00:40:01 GMT  
		Size: 457.3 KB (457326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc179f724180a4cd8ddcbbf0bb407305c21e3802cffaee3a6efdac3143f78967`  
		Last Modified: Fri, 17 Apr 2026 00:40:02 GMT  
		Size: 16.0 MB (16030273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d77254010d09a671c64ad0799c2db74e7c6aa0de7990e4b960a4b00470c80478`  
		Last Modified: Fri, 17 Apr 2026 00:40:01 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a82518b9d20212fb1928a3eb03b1bf3c448b13218c1259aa1f21da2d865c008`  
		Last Modified: Fri, 17 Apr 2026 01:40:24 GMT  
		Size: 6.9 MB (6942718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:fb55fd68d40ead19c10a5da6bc963e0e3349f33611df9157b1af86c23c7da61d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.2 KB (706203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1cd36c2297b8fb08d4611fbae4c8f8aa284dc413997afc6dd78a815fbfe10628`

```dockerfile
```

-	Layers:
	-	`sha256:59f01fde74377c05ef4cb66e73d3916fac3a2915d5d7660857fb9112ca970a28`  
		Last Modified: Fri, 17 Apr 2026 01:40:24 GMT  
		Size: 698.0 KB (697996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8e119dda799c98b1fa0969b6ebaa5c1c874ada1e93cefb84f687df4c44ec94e5`  
		Last Modified: Fri, 17 Apr 2026 01:40:24 GMT  
		Size: 8.2 KB (8207 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.22` - linux; 386

```console
$ docker pull hylang@sha256:7af8cd8be540f9c3b3d454c28a755bd1c607e0f3519e6c2843948302dc5d328b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.2 MB (27199764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc1eed895374fc46d63e7ec9d75b52a3ad9ead6272a2891a0082268072dd122f`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 17 Apr 2026 02:42:29 GMT
ADD alpine-minirootfs-3.22.4-x86.tar.gz / # buildkit
# Fri, 17 Apr 2026 02:42:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 05:55:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 05:55:59 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 05:55:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 05:55:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 17 Apr 2026 05:55:59 GMT
ENV PYTHON_VERSION=3.11.15
# Fri, 17 Apr 2026 05:55:59 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Fri, 17 Apr 2026 06:00:31 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 06:00:31 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 06:00:31 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 09:06:11 GMT
ENV HY_VERSION=1.2.0
# Fri, 17 Apr 2026 09:06:11 GMT
ENV HYRULE_VERSION=1.0.1
# Fri, 17 Apr 2026 09:06:11 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 17 Apr 2026 09:06:11 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:481dba1f7704181ddc1e2b499675e9651a93f972d4cd141a4933d44622cdc88a`  
		Last Modified: Fri, 17 Apr 2026 02:42:34 GMT  
		Size: 3.6 MB (3624721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7db66acce49090c649f7d3afa599b5f0b706312dca19f11949d6b94753e6b8a`  
		Last Modified: Fri, 17 Apr 2026 06:00:38 GMT  
		Size: 455.4 KB (455437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1545d317034c64b483d0912dcd6fd4bd2986eda2106a2ab9cbc68a18c32790c1`  
		Last Modified: Fri, 17 Apr 2026 06:00:39 GMT  
		Size: 16.2 MB (16176615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1a4041bc695d3522ccd88f6b0eb251511570e607c77e05d39734879cd7f3372`  
		Last Modified: Fri, 17 Apr 2026 06:00:39 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a169fe9414eed8d2d4bf4cea77b4da8eed5a876a6fe885e115a552e20f4b9285`  
		Last Modified: Fri, 17 Apr 2026 09:06:17 GMT  
		Size: 6.9 MB (6942742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:24a6b4ca71c811a4f86fe91d8cee47829dcc540859a1a5b508423b3ee26fbbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **706.0 KB (705986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5eba4242a570c7ca709513ec3e0897b4f7b439197ede8dbdd164c274e2012fc`

```dockerfile
```

-	Layers:
	-	`sha256:55a2b59d937663a2e8fd679d225bd1ceed2cb9597c750be06c9a1abfbfd71c99`  
		Last Modified: Fri, 17 Apr 2026 09:06:17 GMT  
		Size: 697.9 KB (697915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d32e5c69a2723e039fd4a84d968d398696436b9c8bbcb6cf4365d78404eae284`  
		Last Modified: Fri, 17 Apr 2026 09:06:17 GMT  
		Size: 8.1 KB (8071 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.22` - linux; ppc64le

```console
$ docker pull hylang@sha256:ff432ed305dbe14dba7a2b836a44580b62159ece7e1f9bf580e036cbfccb52b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.8 MB (27814711 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b37affe21e53ac9fd5b4313029956166f6caba2e4fb498b7798ec21e3be68220`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 17 Apr 2026 00:00:29 GMT
ADD alpine-minirootfs-3.22.4-ppc64le.tar.gz / # buildkit
# Fri, 17 Apr 2026 00:00:29 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 01:45:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 01:45:13 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 01:45:13 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 01:45:13 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 17 Apr 2026 01:45:13 GMT
ENV PYTHON_VERSION=3.11.15
# Fri, 17 Apr 2026 01:45:13 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Fri, 17 Apr 2026 01:57:37 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 01:57:37 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 01:57:37 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 02:29:41 GMT
ENV HY_VERSION=1.2.0
# Fri, 17 Apr 2026 02:29:41 GMT
ENV HYRULE_VERSION=1.0.1
# Fri, 17 Apr 2026 02:29:41 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 17 Apr 2026 02:29:41 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9d65ab042d46bde09babe9a9587237000067c332d24fd9ca516fea7bdfb77c80`  
		Last Modified: Fri, 17 Apr 2026 00:00:38 GMT  
		Size: 3.7 MB (3736656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6535d603abd5fcf706978ed3c1d5730eecc849310feff44ea8ce5422f4cacb32`  
		Last Modified: Fri, 17 Apr 2026 01:54:57 GMT  
		Size: 457.7 KB (457732 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34cbf8bc8fb087171baddaf342940c9718a4618c269701f98d0cb58163ba1678`  
		Last Modified: Fri, 17 Apr 2026 01:57:53 GMT  
		Size: 16.7 MB (16677208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d285d1359f06018d68e88943dda31549531ba645e4826d0741c1f69553f01ef0`  
		Last Modified: Fri, 17 Apr 2026 01:57:52 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f41416590f5a9af4665ec6eef4ffd63cbb71ba9ea551209f0af497ad5bf95f`  
		Last Modified: Fri, 17 Apr 2026 02:29:57 GMT  
		Size: 6.9 MB (6942865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:5f23b6d3810888af2344213da40fca92aa877502dc8fe5acd2d2758eda074acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.2 KB (704170 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:628f1db22864e866a1a082f707e77c788b608866ec16278cbc5066eda58f783a`

```dockerfile
```

-	Layers:
	-	`sha256:1cd1dfb7bffbbf70171879c2da0de26641740683502af04c3cc448aa7bcb4f7a`  
		Last Modified: Fri, 17 Apr 2026 02:29:57 GMT  
		Size: 696.0 KB (696023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c18ffe20785ce7ec634cad75cf657ae64b25109238d200592937d7f8c49b016c`  
		Last Modified: Fri, 17 Apr 2026 02:29:57 GMT  
		Size: 8.1 KB (8147 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.22` - linux; riscv64

```console
$ docker pull hylang@sha256:4d80ed745dade2ad207bc6968554f05c135854dd1feb5b9d86290926f9a7f6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.8 MB (26781110 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b0f615246f276facfaa7fa20d5352541afe36c4c79851d81dcd6bebe062436`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Jan 2026 03:49:43 GMT
ADD alpine-minirootfs-3.22.3-riscv64.tar.gz / # buildkit
# Wed, 28 Jan 2026 03:49:43 GMT
CMD ["/bin/sh"]
# Wed, 04 Mar 2026 20:33:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Mar 2026 20:33:24 GMT
ENV LANG=C.UTF-8
# Wed, 04 Mar 2026 20:33:24 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Mar 2026 20:33:24 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Mar 2026 20:33:24 GMT
ENV PYTHON_VERSION=3.11.15
# Wed, 04 Mar 2026 20:33:24 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Thu, 05 Mar 2026 00:59:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 05 Mar 2026 00:59:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 05 Mar 2026 00:59:29 GMT
CMD ["python3"]
# Thu, 05 Mar 2026 07:32:06 GMT
ENV HY_VERSION=1.2.0
# Thu, 05 Mar 2026 07:32:06 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 05 Mar 2026 07:32:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 05 Mar 2026 07:32:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:15ea87d2370d91334d14e1cb46366adb6a57bbae717f07f8c9f55735cf137f62`  
		Last Modified: Wed, 28 Jan 2026 03:50:15 GMT  
		Size: 3.5 MB (3517422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23730d4ce8db1175bdb1ef21fd480435fb8177910f7bebf9f5d900f25b726b71`  
		Last Modified: Wed, 04 Mar 2026 21:06:08 GMT  
		Size: 457.4 KB (457416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df10c7dada97d419ecd322d2ad4cb9fca34e77c8a99a4b4f50871c9c80dca67`  
		Last Modified: Thu, 05 Mar 2026 01:00:22 GMT  
		Size: 15.9 MB (15888584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79d9191417fb9fc826d0fa944812c1842a80071a8c9760249b78fdfcd716ac0f`  
		Last Modified: Thu, 05 Mar 2026 01:00:19 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7f1aa92640c436796aeefa8235902314852b464c6b0fc7aea381573f14ecb52`  
		Last Modified: Thu, 05 Mar 2026 07:32:50 GMT  
		Size: 6.9 MB (6917439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:ad1b387bee82c0caf37a7d63a1d09d63be9ddeee62594b7859c9c0f9964cd658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.9 KB (704853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c557da57920b46bc65580c5c2ed44535223b00c76c3e2263677ef4e75569ed41`

```dockerfile
```

-	Layers:
	-	`sha256:45a7141ae799de4e84afef9de829b6a158dd69a40b3331407fbfb85b164a7252`  
		Last Modified: Thu, 05 Mar 2026 07:32:49 GMT  
		Size: 696.7 KB (696706 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d69cfb2c02bd9b4b95e45dab08d101ac45d543c691422bb6ab9ce6c8f100c27`  
		Last Modified: Thu, 05 Mar 2026 07:32:49 GMT  
		Size: 8.1 KB (8147 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-alpine3.22` - linux; s390x

```console
$ docker pull hylang@sha256:cf228d4d1079e5a4e6109153c8eb8f8a1aabae1b2b55ea21848e20e4c641c608
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.5 MB (27485524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fd61cd562050f3e208fb1c3a16903fc7ece12b90dd1c1783a00f5b7416a9614`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:56 GMT
ADD alpine-minirootfs-3.22.4-s390x.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:56 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 02:16:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 02:16:31 GMT
ENV LANG=C.UTF-8
# Fri, 17 Apr 2026 02:16:31 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 02:16:31 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 17 Apr 2026 02:16:31 GMT
ENV PYTHON_VERSION=3.11.15
# Fri, 17 Apr 2026 02:16:31 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Fri, 17 Apr 2026 02:24:28 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 02:24:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 02:24:29 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 03:10:20 GMT
ENV HY_VERSION=1.2.0
# Fri, 17 Apr 2026 03:10:20 GMT
ENV HYRULE_VERSION=1.0.1
# Fri, 17 Apr 2026 03:10:20 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 17 Apr 2026 03:10:20 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:54b429821fc7436a26fe07d9038b86e2bef4ef3bf03e43e9ae5e91ab8e4b37a9`  
		Last Modified: Thu, 16 Apr 2026 23:54:12 GMT  
		Size: 3.7 MB (3653873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fdcb8ad0e779755845989eacbda8ae5c94610f08898bcfa49aa15041fcbba0`  
		Last Modified: Fri, 17 Apr 2026 02:23:58 GMT  
		Size: 456.0 KB (456002 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3703b9949bedc421adc9c462b164141cec6e4c187a1d3ecec01ee6e39c75097`  
		Last Modified: Fri, 17 Apr 2026 02:24:40 GMT  
		Size: 16.4 MB (16432753 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3859ec1efe80c1f6857deb8d0409991b3bdabd87b5aed049ef6c623a4c62b2c2`  
		Last Modified: Fri, 17 Apr 2026 02:24:40 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be7e3abf6970aca1c81709abc8e9b1d1373cab9f40d5d225f07bc92af0828051`  
		Last Modified: Fri, 17 Apr 2026 03:10:31 GMT  
		Size: 6.9 MB (6942648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-alpine3.22` - unknown; unknown

```console
$ docker pull hylang@sha256:d92213645e8ddf0c0d53265a99a1a8df78512d126ddc239e00e5ff706e6e14a3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **704.1 KB (704092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dab9c2d9ab33f278dc7037d68c22c573cbbf31453280053c7d8f46a6041c2ee`

```dockerfile
```

-	Layers:
	-	`sha256:2a1460373bbda15956be9856967b2c5ed26fb21cd5471edfdbddbdc60cf16e96`  
		Last Modified: Fri, 17 Apr 2026 03:10:31 GMT  
		Size: 696.0 KB (695989 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39fff532aed89c92273f92aa61ebf36524c92af648fb375dae8400a94483870f`  
		Last Modified: Fri, 17 Apr 2026 03:10:31 GMT  
		Size: 8.1 KB (8103 bytes)  
		MIME: application/vnd.in-toto+json
