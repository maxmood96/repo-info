## `hylang:1-python3.9-bullseye`

```console
$ docker pull hylang@sha256:e070dc50bf3f7f3ae29e1057a5509553297a2957e94652d41989d3b20bb91a2a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:1-python3.9-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:f44dde5a09adbf3106560901a6979457e3c5944c9cadc7dcc8d5c25f1af6cbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48926519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:385b4bcb1930236b7e3f30df85983894ecebed880b1e76a484ffc49a01a127e0`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 04:30:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["python3"]
# Thu, 27 Feb 2025 17:10:02 GMT
ENV HY_VERSION=1.0.0
# Thu, 27 Feb 2025 17:10:02 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 27 Feb 2025 17:10:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 27 Feb 2025 17:10:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ac14194e2e9c843fd02accf690dd5adfedad3f1c4297a15f62d2cf0733f5ff5e`  
		Last Modified: Mon, 17 Mar 2025 23:20:48 GMT  
		Size: 871.2 KB (871219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39238d834826a40612754fa86ed517d26c20d8a69505a2ace3db0596182f12d4`  
		Last Modified: Mon, 17 Mar 2025 23:20:48 GMT  
		Size: 14.1 MB (14131362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67e586f3058717fabcc99bc063a106ae92a64457ddff450a4045183441f5fb18`  
		Last Modified: Mon, 17 Mar 2025 23:20:48 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c10184b203a59b76c80923cfe0c713b8fbde00fd4ef6a88bdcd8b75fe1bc655c`  
		Last Modified: Tue, 18 Mar 2025 00:18:33 GMT  
		Size: 3.7 MB (3669853 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:f862b0d9361924e921943ff75080e59b9a92b508f126434704f59323d91c8251
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2723179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c566bd0f38fe9ca436c1e3492e05fc9fea63745769260e7f7f8ae69a6ad68b8a`

```dockerfile
```

-	Layers:
	-	`sha256:b5ae25a791173c62a0ee337448afe688eba16308f690aaa4400f4011c41daca2`  
		Last Modified: Tue, 18 Mar 2025 00:18:33 GMT  
		Size: 2.7 MB (2715164 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91b2ae99e8757370d1c15e4f953c5d2e04ed3287c252a562db8fce296662b507`  
		Last Modified: Tue, 18 Mar 2025 00:18:33 GMT  
		Size: 8.0 KB (8015 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:65d5ab51ceb9a74a2eff56320f27be52879966a0ad699b2c0493b4d54d5f8515
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43372726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac5ec87039fe9aa658b1441f51342efd03c2271ae5587ca9baaa3352ab90938e`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 04:30:01 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1740355200'
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["python3"]
# Thu, 27 Feb 2025 17:10:02 GMT
ENV HY_VERSION=1.0.0
# Thu, 27 Feb 2025 17:10:02 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 27 Feb 2025 17:10:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 27 Feb 2025 17:10:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b0ca501b624d9dae81049df15e1024733ee21141b25f8ca123d98e0d13df5d12`  
		Last Modified: Tue, 25 Feb 2025 01:31:18 GMT  
		Size: 25.5 MB (25535432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75bf10effdbdb43dfe3fb64366fb0a66189ea37984901bc7e709dbf612f77838`  
		Last Modified: Tue, 25 Feb 2025 11:31:54 GMT  
		Size: 836.9 KB (836943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90479611d4b2cdd498fabd866deb07291bf0bd9fab42f52764a3cb83c8b5061e`  
		Last Modified: Tue, 25 Feb 2025 13:40:51 GMT  
		Size: 13.3 MB (13330025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4dbafe0b65de536599f8975ea67df7a25982da27e670036e49df1a6756fa3d1d`  
		Last Modified: Tue, 25 Feb 2025 13:40:50 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49afd5fa9879dab01aed5d173cf3d0b98bfad26b97382b031ddc4b8e2bc46a53`  
		Last Modified: Tue, 25 Feb 2025 17:55:53 GMT  
		Size: 3.7 MB (3670076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:8c9170e535955deb2ae3229fff258d251726431020792e82cdceac56bc2fa8ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2725499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3aa8ec53d9f6d936b7be7fbd997f395b05d647b7f460e1063c38dd48983013ee`

```dockerfile
```

-	Layers:
	-	`sha256:70d2ad6a374fc41d1540cd869d1ef002fb8c32b9a89a110bc2064a9c42103bb2`  
		Last Modified: Thu, 27 Feb 2025 18:21:21 GMT  
		Size: 2.7 MB (2717409 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f00b8c4ce233e8bd8fbf6ae65d9ffbb79cfdd2687865b2bc548b438ae0b1742`  
		Last Modified: Thu, 27 Feb 2025 18:21:20 GMT  
		Size: 8.1 KB (8090 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:02164a20c392b979acd0ce73d6cb1426b854fa1f7d2108cfe17afff92546a985
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47417707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79b15d171b097692a6bf8ffed286b5aed4cd2707292ed72e439b0d8bd0d08ff4`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 04:30:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["python3"]
# Thu, 27 Feb 2025 17:10:02 GMT
ENV HY_VERSION=1.0.0
# Thu, 27 Feb 2025 17:10:02 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 27 Feb 2025 17:10:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 27 Feb 2025 17:10:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ae10c5f584ce1b218d2a6a1b0821e6ff0869f199833d1a1bb6b3108bb531994`  
		Last Modified: Mon, 17 Mar 2025 23:36:23 GMT  
		Size: 859.1 KB (859144 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f22f9130dac56b94b5d422817f4f191e9a3b7d38aaa94fafac8a0076c1a2639e`  
		Last Modified: Tue, 18 Mar 2025 00:46:19 GMT  
		Size: 14.1 MB (14142395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d795ef305a47d57301cb37eff2153b395124130fe7d050db5ea1f3475bc7bbec`  
		Last Modified: Tue, 18 Mar 2025 00:46:18 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70a98def61a981835a734a15bb6ad8dc6befa1b7eac666715b66880ca52c2886`  
		Last Modified: Tue, 18 Mar 2025 09:36:31 GMT  
		Size: 3.7 MB (3669996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:7c31f9d9d10a669b11aec2b6948f60a3413ee358da198591511717df68dcc30b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2723542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a116404d9b4f5e2cae6766c0a9164dbb5f204e7c5128312b28ab6ce477adbf23`

```dockerfile
```

-	Layers:
	-	`sha256:97248a67b303d92d5be6c6319f6e83c4e53eb7338813fa63117148d70c0bfeb2`  
		Last Modified: Tue, 18 Mar 2025 09:36:31 GMT  
		Size: 2.7 MB (2715423 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:74f266775d0d5074291c067ed5ec7d356d1c28118c45fed7b569e085eb7d5048`  
		Last Modified: Tue, 18 Mar 2025 09:36:30 GMT  
		Size: 8.1 KB (8119 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:a37ff2d292063f4e2d3f045d39cad570012b307590e481884b8bd0154c70cc16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49975865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89db3c95290e6bbbf9bd3420d0070e424d658948e4460e2bcceefa8808604bc5`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Dec 2024 04:30:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Dec 2024 04:30:01 GMT
ENV LANG=C.UTF-8
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_VERSION=3.9.21
# Wed, 04 Dec 2024 04:30:01 GMT
ENV PYTHON_SHA256=3126f59592c9b0d798584755f2bf7b081fa1ca35ce7a6fea980108d752a05bb1
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Dec 2024 04:30:01 GMT
CMD ["python3"]
# Thu, 27 Feb 2025 17:10:02 GMT
ENV HY_VERSION=1.0.0
# Thu, 27 Feb 2025 17:10:02 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 27 Feb 2025 17:10:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 27 Feb 2025 17:10:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e83ba34877ecae8e583197e97ef35a452a1d1b81c406023bf40d3c79d5ba9025`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 31.2 MB (31180337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d8b12e562c0b5e12f558c504948c84fd7bb43aeb5a76ef432753bfb534e608d`  
		Last Modified: Mon, 17 Mar 2025 23:36:54 GMT  
		Size: 884.1 KB (884054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23d882276a0a2718f14e0cc7c366cab00b74341f3ae48201bdaa69e1ff4b4e98`  
		Last Modified: Mon, 17 Mar 2025 23:36:54 GMT  
		Size: 14.2 MB (14241406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34395be73d0287b7eed3bf5b688632021f38bc7af46f184d7c3910134dd76adf`  
		Last Modified: Mon, 17 Mar 2025 23:36:54 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe9cb6227a89d3034704d4eee2366ef8b330a7f01daa5467a002749c5e4605e`  
		Last Modified: Tue, 18 Mar 2025 00:24:49 GMT  
		Size: 3.7 MB (3669818 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:7be7f858de99b553afcba975b99efb6c5e5fc85727b5ccd5f3729e45e8ad76c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19700f447c0ef226ca730afd1fb08c871bd61a7a046488f574dfbaf319d20fc2`

```dockerfile
```

-	Layers:
	-	`sha256:e17c8efeb59332a5c451a0fcc649f5563e18c970ecb8bc492b9e88bc367afdaa`  
		Last Modified: Tue, 18 Mar 2025 00:24:49 GMT  
		Size: 2.7 MB (2712276 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76a7e60216f928d9780b9322efc209cd40097f789d4d58e776fe93edb6b58573`  
		Last Modified: Tue, 18 Mar 2025 00:24:49 GMT  
		Size: 8.0 KB (7983 bytes)  
		MIME: application/vnd.in-toto+json
