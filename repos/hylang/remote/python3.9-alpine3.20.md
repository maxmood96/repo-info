## `hylang:python3.9-alpine3.20`

```console
$ docker pull hylang@sha256:bf95986ced6a2101fcbd8157cf2006c9d5cc179d542a5a98e67229c32b384234
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

### `hylang:python3.9-alpine3.20` - linux; amd64

```console
$ docker pull hylang@sha256:a4f8649062fbb33d2e9ce3a484aaed3046e9520bf5eabbc037df01ad5004d2ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.5 MB (22496258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be2960ea52af722b0b724612a9ab7f3a913ef2d8930a9f56f36334bb6cd6806f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 04:30:01 GMT
ADD alpine-minirootfs-3.20.4-x86_64.tar.gz / # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["python3"]
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:63b69af3dc5582ce6b63be03623e334ccd4e5cb4bde42702bbfc7a986a1bf432`  
		Last Modified: Tue, 07 Jan 2025 02:28:35 GMT  
		Size: 3.6 MB (3613999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:290f5aaa0357a0b01be7e7983ee4d889c6835a821f92945fc0cbba12d06d09ca`  
		Last Modified: Tue, 07 Jan 2025 03:18:35 GMT  
		Size: 443.9 KB (443921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7272bd4930182314a063c930d53749c6b134d8602f731c67c39dd720615695`  
		Last Modified: Tue, 07 Jan 2025 03:18:35 GMT  
		Size: 14.8 MB (14768495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:24cac0249f703ed4555d735513093f0d8c9cb0daa168033f6069a95b32d45c42`  
		Last Modified: Tue, 07 Jan 2025 03:18:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e3875075fd28bbad86a6ba5ae50d50a1c96a13b8ef573f56b2a3fde6d6569d`  
		Last Modified: Tue, 07 Jan 2025 04:23:36 GMT  
		Size: 3.7 MB (3669594 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:a611daff6acc2fe30eec427ac07ea33a6d3df9455877c1c3b665be5795c1788d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.3 KB (660347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e23dc6c15bb95115eac2977da541736a21c9fa310937b1fc3b5f18483cebaf47`

```dockerfile
```

-	Layers:
	-	`sha256:eb1a24e7c3ec1bb9d963e39df31be7651eba2a755629871d7fb76ba44c74772c`  
		Last Modified: Tue, 07 Jan 2025 04:23:36 GMT  
		Size: 652.3 KB (652321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5424555a526f2c66feccb7b16837f880cbf00bd5e80d514e0dd60de61c97212c`  
		Last Modified: Tue, 07 Jan 2025 04:23:36 GMT  
		Size: 8.0 KB (8026 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine3.20` - linux; arm variant v6

```console
$ docker pull hylang@sha256:4bfa5283001be765cd331dba523a85b1421e1fbe5a15d045213f2cc63b9115e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.9 MB (23936282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a787031915b3d9bcb6789a6d125c990f43611ad785ab26cc5f47b4b76792fe2e`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armhf.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["python3"]
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:655a2516811563036720a66963f9c64bc14eb53aac8eeceaebcda6bf661651bb`  
		Last Modified: Mon, 09 Sep 2024 07:03:58 GMT  
		Size: 3.4 MB (3366596 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9be0ab417dbcb0046d0ccc0e89ca0760a1be6e19d9dd44bd3985a517723442`  
		Last Modified: Tue, 12 Nov 2024 14:21:21 GMT  
		Size: 456.0 KB (456017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8f6e58ed60a4005f5ac173ea4bee02bcb5835af742e30617140022db5d70fe3`  
		Last Modified: Wed, 04 Dec 2024 21:23:21 GMT  
		Size: 16.4 MB (16443738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4f409d601d47210c6f5d54c0f1f01536d1409eabbd1324bc40ea10f1cc0cc1b`  
		Last Modified: Wed, 04 Dec 2024 21:23:20 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f33679767360b92cb019bdecea0b8964d8e83e8fdc6f1e35d0cebe0dc2461a2`  
		Last Modified: Wed, 04 Dec 2024 22:09:40 GMT  
		Size: 3.7 MB (3669682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:fe6867d7592e2d8269b65eb71f1c666b6285ec4f86a3c6dd6ca9f659fe3ad4bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7886 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abbf317fde5a9cc220385e1e38c7e2f67e6bdab37cd57af8a03efa4edc109d40`

```dockerfile
```

-	Layers:
	-	`sha256:842e39af9dc4c0ac29101e239950285c2b49a7a2c8da18c7f2912ec2623bdda2`  
		Last Modified: Wed, 11 Dec 2024 19:31:07 GMT  
		Size: 7.9 KB (7886 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine3.20` - linux; arm variant v7

```console
$ docker pull hylang@sha256:a57fc400dc2ce01b91867c5cea30ded280e59adc0f0d2aba64a3c180a7ff2f15
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.1 MB (23106424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1880986f1edbfaab177dc627fb8344531c6a55ffca4702944b370b9d0f87d3f`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-armv7.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["python3"]
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2723bbe95689a46bd4cbe83e27fb42475660f41b02c96d21411fa76d803e8553`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 3.1 MB (3095487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6a7b3f0e95844a9d728ec36cd0a6d3a25cde46780e99640722e89eb89868dde`  
		Last Modified: Wed, 04 Dec 2024 23:43:27 GMT  
		Size: 455.2 KB (455165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:757381fafdb2d01bc693fce8c22d0b291748d59ec2033b51699779437aaf4990`  
		Last Modified: Thu, 05 Dec 2024 02:50:24 GMT  
		Size: 15.9 MB (15885751 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23748feb9788002071213253a40577f9ca69c7c20575c13635f728108529fdb0`  
		Last Modified: Thu, 05 Dec 2024 02:50:23 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87cef5b133881ebea28d4321a0161a92e43d78e53b7e958cdb2063b3dbef6b8c`  
		Last Modified: Wed, 11 Dec 2024 19:37:28 GMT  
		Size: 3.7 MB (3669772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:4cecea574a01c9ec223269e636b20300007c3c8b739c2aeb5316d4b2c682eec2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **668.9 KB (668942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab93928375d9fe6653a7c0599a77d06edd01d7cc45bba5291f3cfd73d0847f10`

```dockerfile
```

-	Layers:
	-	`sha256:d96278f2f8a64e9c5d342acc3499ab9b1300992fdff2d501d3a0881865168197`  
		Last Modified: Wed, 11 Dec 2024 19:37:27 GMT  
		Size: 660.8 KB (660840 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4d7ebcf286e8a4f223060c5ffdb7ca12fbcf7c01bb63e02606e32cc62a9a8ff5`  
		Last Modified: Wed, 11 Dec 2024 19:37:27 GMT  
		Size: 8.1 KB (8102 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:5a7252207fbca3845cde9a8864c573601ef83c4e085a1db35fcc29ecc78d89c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.9 MB (25922403 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b52a24cfb53d36b6aef26d2be607d079c7aed1cc53165d1fe52b0d42596d404`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-aarch64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["python3"]
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9986a736f7d3d24bb01b0a560fa0f19c4b57e56c646e1f998941529d28710e6b`  
		Last Modified: Mon, 09 Sep 2024 07:03:59 GMT  
		Size: 4.1 MB (4087726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de61e223e3d6667838145ce293b86882fe701b04ea3217154c9de4814e37e838`  
		Last Modified: Wed, 04 Dec 2024 22:48:34 GMT  
		Size: 457.5 KB (457466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00327c80a25dee55d01a0229a75cfb8a477f6613eaf76b8a230775dd015ca718`  
		Last Modified: Thu, 05 Dec 2024 00:53:36 GMT  
		Size: 17.7 MB (17707217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe608407f277be140f4f2f1f539e8c187a2cbda38f95058dd13ead603fe413a6`  
		Last Modified: Thu, 05 Dec 2024 00:53:35 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca3bad6aeb7df6382ae6fb616793544760fdf0820c92ea85c7ffb9ca5bd5cbc7`  
		Last Modified: Wed, 11 Dec 2024 19:36:40 GMT  
		Size: 3.7 MB (3669746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:e69f76bea27c8d63e0299a37719f53383be861605a66547da4485cba4ea3e3d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.1 KB (666126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df7f25556fa186645e44e36b6c526c5035aae9ef07d06fffd74a96ce2d613eb`

```dockerfile
```

-	Layers:
	-	`sha256:1f0acb768513a1b711b4212fbada5707eecb1a0954ac223b74503a586e45b0bb`  
		Last Modified: Wed, 11 Dec 2024 19:36:39 GMT  
		Size: 658.0 KB (657996 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:765d250a14cb7342437a0338c4328d36c03dcc360161beac4e74ce8a244872a9`  
		Last Modified: Wed, 11 Dec 2024 19:36:39 GMT  
		Size: 8.1 KB (8130 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine3.20` - linux; 386

```console
$ docker pull hylang@sha256:d45a3d34eb64280cef5ba8a74c39e2f65c7260d73daedfa62560098b182c0d9f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **22.6 MB (22583469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f04e09c535639be6c6bc68ad2a515a815a3506a62812d58d2341a98b3aa98d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 04:30:01 GMT
ADD alpine-minirootfs-3.20.4-x86.tar.gz / # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["python3"]
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a48310298946cd9150f3929f2f8cebe3709f1c7ecd0e99ff2b0c9b6502172586`  
		Last Modified: Tue, 07 Jan 2025 02:28:41 GMT  
		Size: 3.5 MB (3463189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0888cd7ecb434e447f283929d3744a208dcd6df2894ef103220c30aa9820f4fe`  
		Last Modified: Tue, 07 Jan 2025 03:30:34 GMT  
		Size: 444.4 KB (444376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:57c52bd2a70dfa6aac44d34ec3875d2172490c72242c23d5986062a4cf52e433`  
		Last Modified: Tue, 07 Jan 2025 03:30:35 GMT  
		Size: 15.0 MB (15005973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08db78f31efee7204a96c8771f722b27b7178d4c210f15709bf19252d4035a01`  
		Last Modified: Tue, 07 Jan 2025 03:30:34 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4af3b03f2b9fd19f0b432ecab01b1f19a7da3036291a7d9710d8cdafb1a664e0`  
		Last Modified: Tue, 07 Jan 2025 04:19:02 GMT  
		Size: 3.7 MB (3669684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:f674485c0be26675d60bf2615955747a9a36eda8f6f689193f4184805bd83bdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **660.3 KB (660290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db8baf8f77265d02285843c5596c162f33fb383cd2450fafb911c3634418cf1b`

```dockerfile
```

-	Layers:
	-	`sha256:85ee8f4f52f2d1ea5ea3b6e52e3c9c082fa554a7eaf6bef66ea198615d3fe747`  
		Last Modified: Tue, 07 Jan 2025 04:19:01 GMT  
		Size: 652.3 KB (652296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f86b6b50df91d18435d072a198cb95ebbe19f70cadec3f24c7c123c885106ba0`  
		Last Modified: Tue, 07 Jan 2025 04:19:01 GMT  
		Size: 8.0 KB (7994 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine3.20` - linux; ppc64le

```console
$ docker pull hylang@sha256:201048f9a51510fe66fe401f36416dc31716a84a90bfcb8df73173b89dae1397
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **23.2 MB (23150021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:614afefc76c29b60eb022473c5c7e485d190a5364b57b11ab95d4c2b03315c21`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 04:30:01 GMT
ADD alpine-minirootfs-3.20.4-ppc64le.tar.gz / # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["python3"]
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c96bc34ea0111931eae2007b7db67b205ebd3c8a096d711e1be59e48f25006a3`  
		Last Modified: Tue, 07 Jan 2025 02:32:24 GMT  
		Size: 3.6 MB (3568727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5874797fd4d5c5516c705b7850433463089259824f2b1147ed89224c9b8ac04c`  
		Last Modified: Tue, 07 Jan 2025 08:30:48 GMT  
		Size: 446.5 KB (446523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7892e0bd57c25e40204843a5842c7b497c2ec0f9af95d324ee9247820add3d`  
		Last Modified: Tue, 07 Jan 2025 09:00:35 GMT  
		Size: 15.5 MB (15464813 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1292aac043ee18d0a247a5d24812b10ae3b7c49efe2fb81d99d0539ba27c5284`  
		Last Modified: Tue, 07 Jan 2025 09:00:34 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e016b3937c43913b96b5e754a3b901d7c7f574c738ca1ac2704ac6cc55e9df6`  
		Last Modified: Tue, 07 Jan 2025 11:44:56 GMT  
		Size: 3.7 MB (3669709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:3ed65784a54eb2886972647de04edc5f48d78758450b7453162368ef8d5476b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **658.5 KB (658473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56482feb9b410d6b6600e512455ca11378fad5fe9a5feae687eb6c6c5bb08ef2`

```dockerfile
```

-	Layers:
	-	`sha256:3de3f140127a6567cb899cf26b0d0d4c60150ee3e340dba3ba6d628a4f4458cc`  
		Last Modified: Tue, 07 Jan 2025 11:44:56 GMT  
		Size: 650.4 KB (650404 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a302300de1c66cf8f6981cc79408901d3eb3a25b6f994c0e0d55130d152109e`  
		Last Modified: Tue, 07 Jan 2025 11:44:56 GMT  
		Size: 8.1 KB (8069 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine3.20` - linux; riscv64

```console
$ docker pull hylang@sha256:8bb2da3c2ead4853d0292dceeb106b53caedf3606b2a908f10317c84a2884a98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.4 MB (24414255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5242e589a17ddb4dbd902720bd07a8ed1075d4f595ac06d95b44fb69c8f35138`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-riscv64.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["python3"]
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ea37667e50ca807fa8abc1caf0d21091cbbe1d66b2c217158fb3e91c2787afaf`  
		Last Modified: Tue, 12 Nov 2024 00:55:56 GMT  
		Size: 3.4 MB (3371482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd3dbf8fcb536fa7a4e0e93c6002da248193bb3ad21b4a1e7dcb3a51a87f7ba1`  
		Last Modified: Wed, 13 Nov 2024 03:46:10 GMT  
		Size: 456.0 KB (456031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d463dabbb89d1d1c6672d19f64f4a7ce0a7138c84debe05de9c5e3243338e0bd`  
		Last Modified: Wed, 04 Dec 2024 22:44:32 GMT  
		Size: 16.9 MB (16915701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8883c18363fc1e46766213636d7b8d222906f612a6f4732595cbab3d24b7dff`  
		Last Modified: Wed, 04 Dec 2024 22:44:29 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b686b4c701b03d308fbb9a359707814e23e4d88d00a0dc3832936fe5d9fce9b`  
		Last Modified: Wed, 04 Dec 2024 23:17:03 GMT  
		Size: 3.7 MB (3670790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:9d67f6db785aab7d9b0a2823eaf408987960dd538574c425c466cbcdea3d7f4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.1 KB (664086 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56fec29b0cdc392704cd2eaab609656993e1857383f69d3c5191e83ea3fe2908`

```dockerfile
```

-	Layers:
	-	`sha256:f0a4120f94a50087500f5a90d8784536e85f7c9053321e9e88001031c8ceeff1`  
		Last Modified: Wed, 11 Dec 2024 19:38:58 GMT  
		Size: 656.0 KB (656016 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69e35946c9f6d56ca46e2e4fc53d5afa33a06fcbc75f142cac889c935c28b7de`  
		Last Modified: Wed, 11 Dec 2024 19:38:58 GMT  
		Size: 8.1 KB (8070 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-alpine3.20` - linux; s390x

```console
$ docker pull hylang@sha256:fdef5fe1a5fdf36c276159783a562e320cddb1f49c5e3eba0bffff588aa499f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **24.9 MB (24909709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb7ce4b22a5ca2e1ff8ca5df67b7ea56877bf089291dc7c3a910eadce8f635d3`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 06 Sep 2024 12:05:36 GMT
ADD alpine-minirootfs-3.20.3-s390x.tar.gz / # buildkit
# Fri, 06 Sep 2024 12:05:36 GMT
CMD ["/bin/sh"]
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["python3"]
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 11 Dec 2024 00:16:44 GMT
ENV HYRULE_VERSION=0.7.0
# Wed, 11 Dec 2024 00:16:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 11 Dec 2024 00:16:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4261d20208fd5fe57c9f53c86783089a963169d6db6f16306e083ca43f937e0b`  
		Last Modified: Tue, 12 Nov 2024 00:55:29 GMT  
		Size: 3.5 MB (3461608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:886581440a7387e35ae0982554985be4e50cddce78417dd941ff973243ed63d3`  
		Last Modified: Wed, 04 Dec 2024 21:48:53 GMT  
		Size: 456.1 KB (456137 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd15fb6b4c7f75560d4a68a3514c02d9c88df4ca5e3326812f31fa525677d02e`  
		Last Modified: Wed, 04 Dec 2024 23:24:29 GMT  
		Size: 17.3 MB (17321947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84ddbd9ec6caeca33d9409b2c765cb37637729aae8ace88dd9dc320c9cc7360d`  
		Last Modified: Wed, 04 Dec 2024 23:24:28 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54b9f04b703e5d7bda1ce2c82ddceffaed2748d325d5e25c70478d39628edaf0`  
		Last Modified: Wed, 11 Dec 2024 19:39:49 GMT  
		Size: 3.7 MB (3669768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:a67ccc86a863a269508c42d85588a338de89aded8530983cc66ca29ca14bc34e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.0 KB (664012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2909ea32226ed3a06ad977fc7dec62d11ceca8bb08a46ed0daba0a7bd93dc3b1`

```dockerfile
```

-	Layers:
	-	`sha256:88186e436f82ba7adfb884eda85abe4886f841402cdc98cf0b7dcf36f1848850`  
		Last Modified: Wed, 11 Dec 2024 19:39:49 GMT  
		Size: 656.0 KB (655986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0fd240c14ad549e89c6706ada149fc787bf752a2a8e2d6a1e9d1de4ec225c2e`  
		Last Modified: Wed, 11 Dec 2024 19:39:49 GMT  
		Size: 8.0 KB (8026 bytes)  
		MIME: application/vnd.in-toto+json
