## `hylang:python3.10-alpine3.18`

```console
$ docker pull hylang@sha256:3447385d574b0a0bf888ceec8af073278af1f9849b8ea44668f1bd2f2e6821d1
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

### `hylang:python3.10-alpine3.18` - linux; amd64

```console
$ docker pull hylang@sha256:c92e19f66f2035f882cf0e9de7d8b3e104be2a9ebc5b386f64f8c7bf18a3d723
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.3 MB (23287946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:684117f4489a053d7ba81b65cdc24b6542d263a6350df16af0efabee97576065`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 21 Oct 2023 15:49:12 GMT
ADD file:fc714080c3bcbbce7ac746a10d7b4355ffa36293a8d435d62cd5359ea8eb8364 in / 
# Sat, 21 Oct 2023 15:49:12 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Oct 2023 15:49:12 GMT
ENV LANG=C.UTF-8
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_VERSION=3.10.13
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
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
	-	`sha256:c926b61bad3b94ae7351bafd0c184c159ebf0643b085f7ef1d47ecdc7316833c`  
		Last Modified: Thu, 30 Nov 2023 23:23:28 GMT  
		Size: 3.4 MB (3402422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2bcb605b85d2003069c45f91cfda5f7425467172cbc6948511af1b32466482e4`  
		Last Modified: Fri, 01 Dec 2023 02:41:42 GMT  
		Size: 622.5 KB (622492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdbd72e2524a9c41e34a60ccce89481d42a05d471200f6bd15b2b6844e49647f`  
		Last Modified: Fri, 01 Dec 2023 02:42:28 GMT  
		Size: 12.0 MB (12043987 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a202763462d699c2095bd282abaaaeee41462dc76355592240b0f8fa1725561f`  
		Last Modified: Fri, 01 Dec 2023 02:42:27 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46cd35ad89c682fe6cdbb2b272223e56243ee28e8da421e9d09fe2c5103ff804`  
		Last Modified: Fri, 01 Dec 2023 02:42:27 GMT  
		Size: 3.1 MB (3080286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6dd47fe20c6c7712de0261a941c04096673a851575f74d06931dc6cb011a40b`  
		Last Modified: Fri, 05 Jan 2024 23:54:38 GMT  
		Size: 4.1 MB (4138527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:66b70de0b580950ff7a163c8d36ee7fb9a92f9dc931fe52569d1bbd9011ad6a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **870.2 KB (870207 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdc3cdf89411f0d80c48bec3ed5aacf0ac9ac7e6135cfd0c22fa384d1c85bee`

```dockerfile
```

-	Layers:
	-	`sha256:7d531662f48b4d7f3b59b4b37b41cf86d2acbddc7ae5e3584325cff09a6295fa`  
		Last Modified: Fri, 05 Jan 2024 23:54:38 GMT  
		Size: 861.1 KB (861060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8ddb4252be87131336a58f0f79fb7fb105933746197db241345e2e38533e360b`  
		Last Modified: Fri, 05 Jan 2024 23:54:38 GMT  
		Size: 9.1 KB (9147 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine3.18` - linux; arm variant v6

```console
$ docker pull hylang@sha256:c0f8f3dd66c4c54812d2abce3e2926b730eef57b52771e6b6cdc351e120ab7a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.7 MB (22728806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c87c857a6c28a19c4c9a4eeb8b972b9080935f7e38441705b01e0a47dcca232d`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 21 Oct 2023 15:49:12 GMT
ADD file:dbf65487d049081dc2d39b3d99d2c64b6c89754e7e2996a46169d3512e59f32a in / 
# Sat, 21 Oct 2023 15:49:12 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Oct 2023 15:49:12 GMT
ENV LANG=C.UTF-8
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_VERSION=3.10.13
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
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
	-	`sha256:85ae953f9e6740471d4e1440b27721679dc7a511e112eb73df467a4cde26e421`  
		Last Modified: Thu, 30 Nov 2023 22:49:40 GMT  
		Size: 3.1 MB (3146870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:020e6d725b1f9117d8a0fd87888f83e8a35c75b310a29e508a21850a48d9f10d`  
		Last Modified: Fri, 01 Dec 2023 11:12:14 GMT  
		Size: 622.9 KB (622885 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82413cc3e7a6f6d003edccdc77dcd19e93deac949846771dfaa96228a362e913`  
		Last Modified: Fri, 01 Dec 2023 11:12:51 GMT  
		Size: 11.7 MB (11739573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e3d61a881772fd356aea2f159d23bc65dac5fc59cbfef56a518063a2cf93e65`  
		Last Modified: Fri, 01 Dec 2023 11:12:50 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d149c08122ea03e73598eb73179dd31908cccbe57b05507e083c0c294c6563bd`  
		Last Modified: Fri, 01 Dec 2023 11:12:50 GMT  
		Size: 3.1 MB (3080347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:236b310b2fc37bb12e88f1dba35faeda3f0a0e6f8ed9ca248d84dcfcc5c9a6ca`  
		Last Modified: Mon, 08 Jan 2024 20:10:20 GMT  
		Size: 4.1 MB (4138901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:f304d3564bab36294bb1ef6ba20d8c9d5c890ef71609df3c1096c64e5ed4cd35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 KB (9001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:734033b14896919e6485e5081e405c59e8af24b3ba2274303372b576f3ceee91`

```dockerfile
```

-	Layers:
	-	`sha256:0ca5a4115b9c751c950242721bb762b62266a533544d12d83b11edf6440f5a10`  
		Last Modified: Mon, 08 Jan 2024 20:10:19 GMT  
		Size: 9.0 KB (9001 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine3.18` - linux; arm variant v7

```console
$ docker pull hylang@sha256:3450d799a6f8bb0a4119e8c3692277e1f45292aa9b45aee8cacc75057166755e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.0 MB (22015189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3c04aa1ca81a3d35eb9e05fcbb80210b97c2fb8be0ff6c42934fb20fe5a86f9`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 21 Oct 2023 15:49:12 GMT
ADD file:dcb85d43d1fb96861612c42288878b13debfa9d0b956adea1f2472d0c50f0144 in / 
# Sat, 21 Oct 2023 15:49:12 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Oct 2023 15:49:12 GMT
ENV LANG=C.UTF-8
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_VERSION=3.10.13
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
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
	-	`sha256:2387a44129d2147bd4e806bf369f3db92eb3ad3b6b8825c739db364b8baa4e26`  
		Last Modified: Thu, 30 Nov 2023 22:49:56 GMT  
		Size: 2.9 MB (2901006 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ff7e5a1e11ebe03d6acf7eb6082639d0e9d0e1385daeca0fd59c2a5245ba99f`  
		Last Modified: Fri, 01 Dec 2023 02:30:12 GMT  
		Size: 621.9 KB (621938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b65a04a0e1186705b1f03c9e00057450c80f283107ccb69d0f83457681032f4`  
		Last Modified: Fri, 01 Dec 2023 02:30:59 GMT  
		Size: 11.3 MB (11272820 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe4e9a7f3838ae22b54f6ec6dad1f7e30fb53b3900cdf3f7891b2d14d44f8646`  
		Last Modified: Fri, 01 Dec 2023 02:30:58 GMT  
		Size: 229.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a387ab0bf0ed4f447b9d3f98a4c2e8e8eff3f610700fcba4fc65a07d211ff9c`  
		Last Modified: Fri, 01 Dec 2023 02:30:58 GMT  
		Size: 3.1 MB (3080303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e91a7384460585bd994eab0d960f95fe035d1b5794ec794b8f5b5d5235ef6445`  
		Last Modified: Sat, 06 Jan 2024 04:55:40 GMT  
		Size: 4.1 MB (4138893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:f4cf0fc49eb640ac47d7615a86998649a1ad0a9d4af309b23a78172ef0abec3f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **872.0 KB (871970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8e6f0c2201ed3095e46892e4c42565c215ab354b26e7bf2bff39bd72ace56844`

```dockerfile
```

-	Layers:
	-	`sha256:7ae7a56f6c09633a6ff83df9808a31ef13276e901799383ae980b14d3e8a39b0`  
		Last Modified: Sat, 06 Jan 2024 04:55:40 GMT  
		Size: 863.6 KB (863572 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4748f734a518501bd7f45cfd202320537aea8f54ae6615d6f9ec07ee24467734`  
		Last Modified: Sat, 06 Jan 2024 04:55:40 GMT  
		Size: 8.4 KB (8398 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:19c22de61a8368368088836d13cfe30c7068d62fd7cb1a112c56ef76d228cde3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25785328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:24dbac5353f5ca01eadc3b558f2e001e942211b92645e3a937fc19d38db06162`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 28 Sep 2023 20:39:33 GMT
ADD file:ff3112828967e8004a3264d7ece3f81c88e6a1d44d360b9b5613caab15b41717 in / 
# Thu, 28 Sep 2023 20:39:34 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Oct 2023 15:49:12 GMT
ENV LANG=C.UTF-8
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_VERSION=3.10.13
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
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
	-	`sha256:579b34f0a95bb83b3acd6b3249ddc52c3d80f5c84b13c944e9e324feb86dd329`  
		Last Modified: Thu, 28 Sep 2023 20:40:08 GMT  
		Size: 3.3 MB (3331831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:352ed61460a111aaef7891660426e3a7b7b0f79c5767cc5d231b761daea57733`  
		Last Modified: Wed, 29 Nov 2023 05:41:29 GMT  
		Size: 624.7 KB (624729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cca60873726c8b03940eef12be19a4a61fbdb87afbf8eb19a0a3737273417d2`  
		Last Modified: Wed, 29 Nov 2023 05:43:10 GMT  
		Size: 14.6 MB (14609463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2d31606eca229fbffabd0efb03b49657ab47623bed1a2528651b35d868874b7`  
		Last Modified: Wed, 29 Nov 2023 05:43:09 GMT  
		Size: 228.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b73b4390ceeb9aa4014c5bfca82b8dd594a4a4ea78133f14b4d3cb80343d5d8`  
		Last Modified: Wed, 29 Nov 2023 05:43:10 GMT  
		Size: 3.1 MB (3080307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e866abdd222b98d1be952f396fc624c616013ee60c6e51e3e9ef1c8f62c942d`  
		Last Modified: Sat, 06 Jan 2024 00:39:20 GMT  
		Size: 4.1 MB (4138770 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:fa5f0bae521e1a52256e3b98c5da68454760712ede141697f9ea0b83a010816e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **870.3 KB (870277 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4045868f5fd513e22a42e20b1ba7d835720b9e6ad46c20fe5544ed5142aa169b`

```dockerfile
```

-	Layers:
	-	`sha256:ebe9417773cb816a0a591333aecf65ce217da3dca978c5bea9b6bbdfb53974dc`  
		Last Modified: Sat, 06 Jan 2024 00:39:20 GMT  
		Size: 861.9 KB (861938 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4fb6d1eb74dd644d8c053eeb6c15ece7852ed20c7e8543dc758747683a064f57`  
		Last Modified: Sat, 06 Jan 2024 00:39:19 GMT  
		Size: 8.3 KB (8339 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine3.18` - linux; 386

```console
$ docker pull hylang@sha256:99b15c3079ec5d48cc7ba7d1c65fff3229dfdcf593514508341a903e04eaab4a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23249970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a9829fc76fd2fa8fbe7d69a8e6e39b5eb582318bdb98eb4f88d62af820ad89d`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 21 Oct 2023 15:49:12 GMT
ADD file:92902088cd15ed8f5dca2f7fc6570fb4e4824fac8b09e091c88e96bbd0ca814b in / 
# Sat, 21 Oct 2023 15:49:12 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Oct 2023 15:49:12 GMT
ENV LANG=C.UTF-8
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_VERSION=3.10.13
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
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
	-	`sha256:4966a8bd129b0a6adf93dc295a8fbe8f665d3194a684a5ce199c1c3596dbf3d9`  
		Last Modified: Fri, 01 Dec 2023 02:04:18 GMT  
		Size: 3.2 MB (3238831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdf5d54f9b80cc86c8bf93637d018e9432b6daf1aa4841e0302b2e9c5e4697a4`  
		Last Modified: Fri, 01 Dec 2023 07:08:31 GMT  
		Size: 622.3 KB (622335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90f19469ef327fd56a015927d8d98d11117794a05d94692322eee98e2eddeddc`  
		Last Modified: Fri, 01 Dec 2023 07:09:19 GMT  
		Size: 12.2 MB (12169492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dd51e0541372bb86e3a8c2bb537e9c02edaa8232387af3d4ea7bbdaa055a234`  
		Last Modified: Fri, 01 Dec 2023 07:09:18 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a1adac080a536f2ec81cbb1b945ebb2cce55decf22f84ecd59edc3c70546d2f`  
		Last Modified: Fri, 01 Dec 2023 07:09:19 GMT  
		Size: 3.1 MB (3080298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:208c9540f3cc35c01bb36c3e2154f47d951708cb796ad1fb5b148c0e1eb7b0b0`  
		Last Modified: Fri, 05 Jan 2024 23:54:48 GMT  
		Size: 4.1 MB (4138787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:dcc395a46cd8c6e4f7f262c283452a627f3811adf8c040565af13e19be691fb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **870.2 KB (870153 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a5ffe7bdd0cef3ee5bb024436e94814a7810261399fd34c9e36061cacf55f51`

```dockerfile
```

-	Layers:
	-	`sha256:4018c57bf2971754b992203fe58036358ec2b927d1ffbbe9f3df11f9689e961a`  
		Last Modified: Fri, 05 Jan 2024 23:54:48 GMT  
		Size: 861.0 KB (861035 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8803e7b6bfead7f5d9fabdac3deb19936b748856091c2dec63f27e1b08959af`  
		Last Modified: Fri, 05 Jan 2024 23:54:47 GMT  
		Size: 9.1 KB (9118 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine3.18` - linux; ppc64le

```console
$ docker pull hylang@sha256:ca037a83bcfddc9f8e1af205db2617af387a1da1be0c0741925a1208fbc7bdd0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.6 MB (23628735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36abe36bc1bd4c72068d4a71242f6b418f43f97a37d7d91eaf6911b353e24c59`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 21 Oct 2023 15:49:12 GMT
ADD file:3450a1687b552498a987f87cb844b7f597c7181d7c3d31943d7b3036d5300d5e in / 
# Sat, 21 Oct 2023 15:49:12 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Oct 2023 15:49:12 GMT
ENV LANG=C.UTF-8
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_VERSION=3.10.13
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
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
	-	`sha256:4e13780adf2776477b14ef9c0f4f563f820a2fde166d472218037b979e84d31a`  
		Last Modified: Thu, 30 Nov 2023 23:20:01 GMT  
		Size: 3.3 MB (3348322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390ff5286851231527dab5805788a0c2b2d063e43d90426e6a9290489c9ee807`  
		Last Modified: Fri, 01 Dec 2023 03:44:43 GMT  
		Size: 625.1 KB (625117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:766f34e4c7c20ea0a113fc49bcce914ad4f79c5dd296d1008a0f6649cadb3fd3`  
		Last Modified: Fri, 01 Dec 2023 03:45:28 GMT  
		Size: 12.4 MB (12435995 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89e40c8a99b8c4c30eb0dc5d01bfb02c66209296e58809c0f49ef40f96442cb2`  
		Last Modified: Fri, 01 Dec 2023 03:45:28 GMT  
		Size: 233.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58c4543534db24fb838d0543f380d5d35452837b65fa515ee5049ba6d526e4f8`  
		Last Modified: Fri, 01 Dec 2023 03:45:28 GMT  
		Size: 3.1 MB (3080338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3dd5ea25bd777d706d876a0b303edb0af9446693e774808d14f15ea4a1799f1`  
		Last Modified: Sat, 06 Jan 2024 02:42:14 GMT  
		Size: 4.1 MB (4138730 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:bbe68d00ec49dbf5ce8958d2502f2c5aca4547cc0a490e289376963d0c4fccc3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.8 KB (867825 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d67601254e3995a2a35d210481abab8918574a5f34377c61c7972c9d9858ae4b`

```dockerfile
```

-	Layers:
	-	`sha256:2474d77aea57396a12b11a845af4bb3641aa5a507f08bf07c598b0ed19490671`  
		Last Modified: Sat, 06 Jan 2024 02:42:14 GMT  
		Size: 859.5 KB (859458 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f5122e08af74e71b555b8b0b4d39caad6649e4e77fe7ab77e21a11c110b38a1`  
		Last Modified: Sat, 06 Jan 2024 02:42:13 GMT  
		Size: 8.4 KB (8367 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-alpine3.18` - linux; s390x

```console
$ docker pull hylang@sha256:1ff79f30c8838cee09c2c0ac4f693a1575f396d4f5e4e8346348244a1a676de2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23153273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a4285c34b1ba6cc5c29862597c6e745ba1d38b38e3534b405e7429460484d84c`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 21 Oct 2023 15:49:12 GMT
ADD file:50d6643abf7df167a927decd69d193b980557ff73cca48dce86d57e2ff25ad45 in / 
# Sat, 21 Oct 2023 15:49:12 GMT
CMD ["/bin/sh"]
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 21 Oct 2023 15:49:12 GMT
ENV LANG=C.UTF-8
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_VERSION=3.10.13
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		python3 --version # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/4cfa4081d27285bda1220a62a5ebf5b4bd749cdb/public/get-pip.py
# Sat, 21 Oct 2023 15:49:12 GMT
ENV PYTHON_GET_PIP_SHA256=9cc01665956d22b3bf057ae8287b035827bfd895da235bcea200ab3b811790b6
# Sat, 21 Oct 2023 15:49:12 GMT
RUN set -eux; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Sat, 21 Oct 2023 15:49:12 GMT
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
	-	`sha256:2ea477e1c0c3db3337ee1d7c659f8c465021a65c036998ed3fa3b667d4b30153`  
		Last Modified: Thu, 30 Nov 2023 22:42:52 GMT  
		Size: 3.2 MB (3217454 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28a35e8347eed15bdf065db4baf4be15e7227287d9f94ad22890350f3290e439`  
		Last Modified: Fri, 01 Dec 2023 02:09:37 GMT  
		Size: 623.0 KB (622975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05428310ad96fc53fb4bc69b209192633f15d25d790a25a8ea2ea959039b237c`  
		Last Modified: Fri, 01 Dec 2023 02:10:12 GMT  
		Size: 12.1 MB (12093572 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81b6b63654af10f922634f493d6beb174464dd372eb56ef96fe1cd432c970cc3`  
		Last Modified: Fri, 01 Dec 2023 02:10:11 GMT  
		Size: 230.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:127c634f0ef9b10dde21b2db3597634a84a83194cf55239b233a36e7daa3aa26`  
		Last Modified: Fri, 01 Dec 2023 02:10:11 GMT  
		Size: 3.1 MB (3080305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6e361ceb28285f27b9a19e6245e647e704c481094be6e5cdf8f83b7b2e37bad`  
		Last Modified: Sat, 06 Jan 2024 00:30:07 GMT  
		Size: 4.1 MB (4138737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-alpine3.18` - unknown; unknown

```console
$ docker pull hylang@sha256:cc6c5d143ab4bb0f79ef30ce5b2d2d3fda5271e2841d7559b6c55db4ba889cb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **867.8 KB (867753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa8b252fadb6238c7a09e799f204e6a74e72308faa78cba19c53dda54d2136b`

```dockerfile
```

-	Layers:
	-	`sha256:f72a12a8b280101f475da7747c975e43ba64e88c81238ed792f0d296e9a0e9cd`  
		Last Modified: Sat, 06 Jan 2024 00:30:06 GMT  
		Size: 859.4 KB (859424 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc231d25c1caa7aca079d36983388c88e5560562c08cefd02b2a986512567443`  
		Last Modified: Sat, 06 Jan 2024 00:30:06 GMT  
		Size: 8.3 KB (8329 bytes)  
		MIME: application/vnd.in-toto+json
