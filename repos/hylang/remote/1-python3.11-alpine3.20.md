## `hylang:1-python3.11-alpine3.20`

```console
$ docker pull hylang@sha256:c7890b290f752a954622c5867c1ceeacbfd178366fe7938ec5e3e2f3d1514787
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

### `hylang:1-python3.11-alpine3.20` - linux; amd64

```console
$ docker pull hylang@sha256:380fe08ce19b7298beb0bb88d62e8123b8497cb91a54dd09c549eef3a8ddab6b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.4 MB (26413873 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d551f38a7d79b123f18442833bee2ca45a1bfcb791a8658526346d509dd5e7f`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
ADD alpine-minirootfs-3.20.6-x86_64.tar.gz / # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 22:49:59 GMT
ENV LANG=C.UTF-8
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0a9a5dfd008f05ebc27e4790db0709a29e527690c21bcbcd01481eaeb6bb49dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:36 GMT  
		Size: 3.6 MB (3626897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a157f2195d297499bff548d11818817ccd520c10f8fe1ed8d576ee633d7ab0b6`  
		Last Modified: Fri, 14 Feb 2025 19:19:15 GMT  
		Size: 458.3 KB (458338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1235e3de1fd933fb2a3bb435160d91c0b522f9d54bbaedb65502b01101065f29`  
		Last Modified: Fri, 14 Feb 2025 19:19:16 GMT  
		Size: 16.1 MB (16110901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a023630adeb631c4b563129373f76895275659ff3c24157cab08a3c47d26dd41`  
		Last Modified: Fri, 14 Feb 2025 19:19:15 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526c415f8fd5af878639f2951137786fd9ec4b88e11321698f09581d23ef4a43`  
		Last Modified: Wed, 19 Mar 2025 22:58:56 GMT  
		Size: 6.2 MB (6217488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:b5e6481b8ed43f0489dc32826a79e22343b68b54faa3da5f47d581c4d0361939
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.3 KB (666255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8b3b512b5d6f0ba10b1640da7ff60c6e101037625446ca15f9ebe456c6ba992`

```dockerfile
```

-	Layers:
	-	`sha256:6d9d8304292b3f38bce7e42c1339f1ef2b75f565ccf208cc3d410388250571cc`  
		Last Modified: Wed, 19 Mar 2025 22:58:56 GMT  
		Size: 658.2 KB (658217 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba250eed50ebbc5532d19de2663fbe37ec4b94ab68d582f97780ca754ff36a59`  
		Last Modified: Wed, 19 Mar 2025 22:58:55 GMT  
		Size: 8.0 KB (8038 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.20` - linux; arm variant v6

```console
$ docker pull hylang@sha256:4af30136ced85803957a98e5de7f5e2710ec75ce88c84ca536ff07a3bf3a0ef6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.8 MB (25751413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d421a2c0c23fe236096cf2b46cecf548448ddb7c71a399c2cfcbb08dbb3bcf2`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
ADD alpine-minirootfs-3.20.6-armhf.tar.gz / # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 22:49:59 GMT
ENV LANG=C.UTF-8
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c9aedc9d4e47fa9429e5c329420d8a93e16c433e361d0f9281565ed4da3c057e`  
		Last Modified: Fri, 14 Feb 2025 18:28:14 GMT  
		Size: 3.4 MB (3372531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6478cac8bebe0716496c5082cc4bf5745ac6f5ea7aee119fd3d7169f6492813`  
		Last Modified: Sat, 15 Feb 2025 08:33:08 GMT  
		Size: 459.1 KB (459087 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee92a26080f65d8b34959ce7271b9df4095145456a39a047fb9558d2fa012380`  
		Last Modified: Sat, 15 Feb 2025 08:46:29 GMT  
		Size: 15.7 MB (15701959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43c63a98b25696271ae47667ac2cbe6efdb0333aa7360f4e171ade811c9757a0`  
		Last Modified: Sat, 15 Feb 2025 08:46:28 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda168b575786b9a930545b9a6823961123aac8c958ec11a346719dd020924b3`  
		Last Modified: Wed, 19 Mar 2025 23:00:32 GMT  
		Size: 6.2 MB (6217586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:c76680e0026bed065870b7a6b9e484df090049015851710c837a570ac21a3d1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b88eed84f89784b7936289e2c586121bb6a3e9a7389dd0ecc8c30498d2f41a8`

```dockerfile
```

-	Layers:
	-	`sha256:53da85a984a14ba88f142d6d1a6f0155ece735ae750fd356946563a9112db869`  
		Last Modified: Wed, 19 Mar 2025 23:00:31 GMT  
		Size: 7.9 KB (7899 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.20` - linux; arm variant v7

```console
$ docker pull hylang@sha256:8cdc02965773be6d61b072bf0c1fb689216c983812a79b2837cd6b826cc8a52a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **25.1 MB (25053589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab40a7a0ac58bd473294b037e43390aa3781019169f89d6bdb32eac0feb130ee`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
ADD alpine-minirootfs-3.20.6-armv7.tar.gz / # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 22:49:59 GMT
ENV LANG=C.UTF-8
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:772078ddbdee5be52d429e08f953aaad6715a90d7e4d6496eb1cd4004efa8a95`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.1 MB (3095969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd39f1bc2ba1576819866de04b365eaef7c391558f86bc6f3c2e4143114066f6`  
		Last Modified: Sat, 15 Feb 2025 08:28:25 GMT  
		Size: 458.3 KB (458309 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15d96647f2ddcf606013d9c9e908e48cd0cec34c358f12b9b35a3695d73e09df`  
		Last Modified: Sat, 15 Feb 2025 08:41:56 GMT  
		Size: 15.3 MB (15281653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7881101b988a9e801753aea48152604eec514e4c32295a2386a355c10045747`  
		Last Modified: Sat, 15 Feb 2025 08:41:55 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:390a8ec189ce1ccae2b10ff80c0c96d2742949fb59e67c725d1151c72a518f80`  
		Last Modified: Wed, 19 Mar 2025 23:34:05 GMT  
		Size: 6.2 MB (6217411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:652f112a557b62975143db7249cd17cab79989ac2098647dcda2eea92e2b8e7e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **669.2 KB (669228 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f13ca1901ef878f648b202457a8bffed076f9200606302931338a63d3734913`

```dockerfile
```

-	Layers:
	-	`sha256:aa75f41fb40b67521a8b71db7b22e6c1b0f27cc0520c115887e1b3d09b0289ff`  
		Last Modified: Wed, 19 Mar 2025 23:34:04 GMT  
		Size: 661.1 KB (661114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2dac061d8715af29f3cf419aa99a1b4ae541e953dd041349a1a27a683778f67b`  
		Last Modified: Wed, 19 Mar 2025 23:34:04 GMT  
		Size: 8.1 KB (8114 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.20` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:e54c6b2074db56321f8d639040372610db905e8b0222911abf5a3c9f07359d25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.0 MB (27014020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac03b200ab4f546736dba0ee787884fa21f7cbb318e6b67c27b3bfbcade43662`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
ADD alpine-minirootfs-3.20.6-aarch64.tar.gz / # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 22:49:59 GMT
ENV LANG=C.UTF-8
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:94e9d8af22013aabf0edcaf42950c88b0a1350c3a9ce076d61b98a535a673dd9`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 4.1 MB (4091165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6335b4f9bcc69d7d61b9fb68f8ef0649d2a6c102a5e7ce9ff67be434951b03b2`  
		Last Modified: Sat, 15 Feb 2025 05:35:54 GMT  
		Size: 460.5 KB (460476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a2e1471a7e52433dd1e154ab4c9dc2b6917d9e9ae7ef935616595866c93b18b`  
		Last Modified: Sat, 15 Feb 2025 05:48:07 GMT  
		Size: 16.2 MB (16244783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c390965b290b256ccbd8876cf93b9897903ce9d9b52fd97a84c9699ae93b349`  
		Last Modified: Sat, 15 Feb 2025 05:48:06 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aee593a723744e6e3b173c255656cdc30d1266a4f3a137aa5f016d0bf2704e0e`  
		Last Modified: Wed, 19 Mar 2025 23:20:42 GMT  
		Size: 6.2 MB (6217347 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:8a91808515e68fbf3016b98d9295a4e0070c11773be850f7b02bf3e044e75786
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.4 KB (666415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c3e7cb86e740c19842f5dca542c11d8194965022285b987160943df1ec8af27`

```dockerfile
```

-	Layers:
	-	`sha256:415a59e4a30c6d75ead31e082dc925d911d549c1a35a6457700f6c73dc46d8ee`  
		Last Modified: Wed, 19 Mar 2025 23:20:42 GMT  
		Size: 658.3 KB (658273 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0bcedbeb4562eafba8c43e113f8c0a130c0656d6757b1d3d07a804c4cb04dc6e`  
		Last Modified: Wed, 19 Mar 2025 23:20:42 GMT  
		Size: 8.1 KB (8142 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.20` - linux; 386

```console
$ docker pull hylang@sha256:4269bd553c4f9220f3c4f736487dd90f28a40b92d9fd0cb2215ec8e256683e48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.5 MB (26491970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e60aee591b9b5a984c3001440d39b4c7ae587b7d5fd68b91953a535056858767`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
ADD alpine-minirootfs-3.20.6-x86.tar.gz / # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 22:49:59 GMT
ENV LANG=C.UTF-8
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b3d7db73e90671cb6b7925cc878d43a2781451bed256cf0626110f5386cdd4dc`  
		Last Modified: Fri, 14 Feb 2025 12:05:37 GMT  
		Size: 3.5 MB (3471668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3d09047dc5b1a20ce2988dd358f0e8196457f2cffd454ea4c000fcda6bddb4f`  
		Last Modified: Fri, 14 Feb 2025 19:19:08 GMT  
		Size: 458.7 KB (458735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4e6270814d1ac012aa54e851b03859ebdbdaaf416ca103f512ee500d6b174a`  
		Last Modified: Fri, 14 Feb 2025 19:19:08 GMT  
		Size: 16.3 MB (16343794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a214ec9d895cb91b1def331f12c5c07eff24c65de4923697cc661bfd292330`  
		Last Modified: Fri, 14 Feb 2025 19:19:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:502a072a65ece09832af1232fa7eff07832db9f77a28e7c9b14fbccd265646e1`  
		Last Modified: Wed, 19 Mar 2025 22:58:48 GMT  
		Size: 6.2 MB (6217523 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:2146702e8adb7c742a6859357f0578c86f30c02ae114057bcddaaba8d591b016
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **666.2 KB (666198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3516e7926610be4151780ba6c61513bec967cb571c4d42200bb2d8e5d349cf`

```dockerfile
```

-	Layers:
	-	`sha256:db02d2859b91530fbbb5a8c9caccf5b35c35083f666b7186b78d2142117736d4`  
		Last Modified: Wed, 19 Mar 2025 22:58:48 GMT  
		Size: 658.2 KB (658192 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a30b7e90471738916ef5a3f0898088cfc30dbdaa08c0029ba89fd13d3c8bdb52`  
		Last Modified: Wed, 19 Mar 2025 22:58:47 GMT  
		Size: 8.0 KB (8006 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.20` - linux; ppc64le

```console
$ docker pull hylang@sha256:cc3384dbe39eab7e52e16d70a064a2146f2167260c8f198bb2eb76f0d7088142
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **27.1 MB (27097538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f11646113501aa5863090bdaf837e179777947af4f15a8af51f9e47cd74314b`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
ADD alpine-minirootfs-3.20.6-ppc64le.tar.gz / # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 22:49:59 GMT
ENV LANG=C.UTF-8
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c9813c0f5a2f289ea6175876fd973d6d8adcd495da4a23e9273600c8f0a761c5`  
		Last Modified: Fri, 14 Feb 2025 12:05:35 GMT  
		Size: 3.6 MB (3575680 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3578207bd8f37bd53814243eaf0d3d05efb441ce07e31dd5395d9f25104bc32b`  
		Last Modified: Sat, 15 Feb 2025 00:03:42 GMT  
		Size: 460.9 KB (460851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fac4f3619ca1701087146b9086343d82465a9721d4efebc05b2eab1b4add4f5`  
		Last Modified: Sat, 15 Feb 2025 00:19:16 GMT  
		Size: 16.8 MB (16843252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a8ce9ec098d39ef6ebb42b67a04ccbc27a66a1fba5edbafbf1b4cf2f628c5c`  
		Last Modified: Sat, 15 Feb 2025 00:19:15 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:990e54242a01d3297a71250f5e6dd8ec58cbcaa073c433d212c4356c17b39181`  
		Last Modified: Wed, 19 Mar 2025 23:27:58 GMT  
		Size: 6.2 MB (6217507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:69252cf333110fe02fc701c4ad5d4f90baa25b8ff243f5900708ea5822540241
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.4 KB (664382 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e6e097e4fb9b6d972e2c9b6a1b9098957e5fc9aeff0b60bdc14ae0b5b225c7a`

```dockerfile
```

-	Layers:
	-	`sha256:11614cb713e17335500b730ae73b8402b0a1ac4223cf753d9b0307eb045a747f`  
		Last Modified: Wed, 19 Mar 2025 23:27:58 GMT  
		Size: 656.3 KB (656300 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5079326c8be2657d24b4061641b5c73bcd0eacb840efb10bd9c6cabf6456a022`  
		Last Modified: Wed, 19 Mar 2025 23:27:57 GMT  
		Size: 8.1 KB (8082 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11-alpine3.20` - linux; s390x

```console
$ docker pull hylang@sha256:c6982e9627876df6864d0b0c18b38b3f4ac13cb0e21efe85725a338dd5dea539
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **26.7 MB (26734473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64f0b7484872dc807324ac306e1cd4f8ca8b764870bc813cbf2b9358f7dda663`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 03 Dec 2024 22:49:59 GMT
ADD alpine-minirootfs-3.20.6-s390x.tar.gz / # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["/bin/sh"]
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Dec 2024 22:49:59 GMT
ENV LANG=C.UTF-8
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_VERSION=3.11.11
# Tue, 03 Dec 2024 22:49:59 GMT
ENV PYTHON_SHA256=2a9920c7a0cd236de33644ed980a13cbbc21058bfdc528febb6081575ed73be3
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		gnupg 		tar 		xz 				bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Dec 2024 22:49:59 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7c6bf3be7c8016421fb3033e19b6a313f264093e1ac9e77c9f931ade0d61b3f7`  
		Last Modified: Fri, 14 Feb 2025 12:05:38 GMT  
		Size: 3.5 MB (3464123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c09df7e74186943396ecff7b207156ec5cf5043ac3b666f0b5ebb68cda4e25d`  
		Last Modified: Sat, 15 Feb 2025 06:27:53 GMT  
		Size: 459.3 KB (459273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92e0ec8eb28f372ec2db60e8a0ac3ecbfb95ac31a8fa232c1c7b64ea590355bc`  
		Last Modified: Sat, 15 Feb 2025 06:41:01 GMT  
		Size: 16.6 MB (16593263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad1fb671e7ff987feb0e2b13e7961739bb496f208c5a5ade66c37149b35530c4`  
		Last Modified: Sat, 15 Feb 2025 06:41:00 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dec3edc335dcec2e1aeeaad80bb705fbe371f64468dc0b8cb0ec1132964b6eed`  
		Last Modified: Wed, 19 Mar 2025 23:51:10 GMT  
		Size: 6.2 MB (6217564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11-alpine3.20` - unknown; unknown

```console
$ docker pull hylang@sha256:04fe26d5c82c8f81266f08d46c2eab05595c430d22219a07968d47c0763660b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **664.3 KB (664304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f282969c8e77a2dc89eeea6d078a4cdd628788371cd518de24076f12eeef1507`

```dockerfile
```

-	Layers:
	-	`sha256:f2e4d60eba9702c4af56db3c45bbdde2edad6e035e23258b32658cb585053e83`  
		Last Modified: Wed, 19 Mar 2025 23:51:09 GMT  
		Size: 656.3 KB (656266 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40ed3f5a780ac915df8e4e6a48a5a2030cf16002532484a0ee33dbbdc13c75c6`  
		Last Modified: Wed, 19 Mar 2025 23:51:09 GMT  
		Size: 8.0 KB (8038 bytes)  
		MIME: application/vnd.in-toto+json
