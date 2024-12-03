## `hylang:python3.11`

```console
$ docker pull hylang@sha256:ad4432185578632c7797571f711499be4e565cab4cbd74c8f8a520919e35986d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
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

### `hylang:python3.11` - linux; amd64

```console
$ docker pull hylang@sha256:4b1cbd1a67d697dd13359a05ccd43eb398f6b3bda08a78c242bab1eef4f42b8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53957637 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2dabf0cf297d8ae12d90e776927b45aa431727c81c3e9226c92b08c86b6f4d4`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.11.10
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=07a4356e912900e61a15cb0949a06c4a05012e213ecd6b4e84d0f67aabbee372
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c58b365c3bcb57c930511e3fef962d15491ef2daba1e111fb5a6b41dbdecfc6b`  
		Last Modified: Tue, 03 Dec 2024 02:28:05 GMT  
		Size: 3.3 MB (3317301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bc3f72291794502343f023ab10455e459897b13a73f38b6b56cf266dccb7ec5`  
		Last Modified: Tue, 03 Dec 2024 02:28:05 GMT  
		Size: 16.2 MB (16202769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42dacf6a4601de71542906f1be2bca5a78b8f430479b260a7097b9870498af69`  
		Last Modified: Tue, 03 Dec 2024 02:28:05 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c0b2781fa151bf8bd5dca5fe2f163bdbec146ed01997011b3ec43e22a32cb8`  
		Last Modified: Tue, 03 Dec 2024 03:26:30 GMT  
		Size: 6.2 MB (6205736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:7d6f768da447959cdad1f20191d65709a22c95a54d035681965b85aaa76b947d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2475848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87ade08bad3ec36cca50e4990cbe09fc960879909885e8347bd16fe28e12fd36`

```dockerfile
```

-	Layers:
	-	`sha256:24aecfc300b13e262cb25e4773662b7bb54a30835389bcb1d8204cedffe8ca01`  
		Last Modified: Tue, 03 Dec 2024 03:26:29 GMT  
		Size: 2.5 MB (2466571 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:41b2fa4868f2fac027a5332c2f0f8b90449f241edc2bfac5412550db81f28983`  
		Last Modified: Tue, 03 Dec 2024 03:26:29 GMT  
		Size: 9.3 KB (9277 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11` - linux; arm variant v5

```console
$ docker pull hylang@sha256:559ec2ff659f0df62ee7ea54c9236f2d33c88151f39433544c45d60af6b2b318
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50461553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:738cbc9a91607413b63aa0fbb19c0660ebacc7cd6d3da4038bf3d5a9d1dcc65d`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1733097600'
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.11.10
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=07a4356e912900e61a15cb0949a06c4a05012e213ecd6b4e84d0f67aabbee372
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:25d432086d20067bebfff2b163f22d49e7da8528782652615fe170bf8c39194d`  
		Last Modified: Tue, 03 Dec 2024 01:27:20 GMT  
		Size: 25.8 MB (25754926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ce20c4e66ffa1764742e2df6279cf58e8b7ebdfaf2f9fb30499a842e87e2036`  
		Last Modified: Tue, 03 Dec 2024 07:27:17 GMT  
		Size: 2.9 MB (2890005 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec20e765ec9f60a57a670c292ea519a11d6eb1ee41be34bb79210a72e7830b1`  
		Last Modified: Tue, 03 Dec 2024 07:45:04 GMT  
		Size: 15.6 MB (15610200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:809080d275bf032318dd9b95d2d3b2601b2322b9006598027a249eac03c1aab9`  
		Last Modified: Tue, 03 Dec 2024 07:45:03 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d3ea37d74b6771c56cdaffce251639e14d5e54555bc3282bfc5f1d068caa808`  
		Last Modified: Tue, 03 Dec 2024 09:54:57 GMT  
		Size: 6.2 MB (6206173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:212a053097be736877b65ae7a3992054ae656fc88b917e85e2efdc4d62ba63a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2479499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86eaca8a88c6fe1c40ea33f23e701e4d533c5fa05e4d3e28062639a4f08ddf26`

```dockerfile
```

-	Layers:
	-	`sha256:37c05c860bb3ff5a79810c47f2173e5775981525367fb02d92b87619d89ad5e9`  
		Last Modified: Tue, 03 Dec 2024 09:54:57 GMT  
		Size: 2.5 MB (2470114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fb0d3f4748667c8b2db6291d25174ed59d481b1e3aab2ad32ebba050341b5ae`  
		Last Modified: Tue, 03 Dec 2024 09:54:56 GMT  
		Size: 9.4 KB (9385 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11` - linux; arm variant v7

```console
$ docker pull hylang@sha256:23844feb4eac80fd6d0c45d299fa8ce0f6ef55e25c2a3d55a7082400027cfddf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48058138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cafaff06266f29a882d972c0676192f40feac6d9a38c13e161ce1abe15809f8f`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1733097600'
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.11.10
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=07a4356e912900e61a15cb0949a06c4a05012e213ecd6b4e84d0f67aabbee372
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:80b4fb4796cece09f69103235c60ffd0226a78c400a2953144b84c17de4df93d`  
		Last Modified: Tue, 03 Dec 2024 01:28:14 GMT  
		Size: 23.9 MB (23933588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7af53e937c53489a63b2fd3e623a6ac9d5a8f3e6f6d3e6a8e49612e843fa812e`  
		Last Modified: Tue, 03 Dec 2024 11:45:12 GMT  
		Size: 2.7 MB (2721230 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23c2a200079606abeab266ecef6b77f6c679234feba79113b692df45fa35a09f`  
		Last Modified: Tue, 03 Dec 2024 12:28:24 GMT  
		Size: 15.2 MB (15196816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:200b690ef95255649cd9993ac9bcc2693b0fb67588121e7400ec4c87b9458eee`  
		Last Modified: Tue, 03 Dec 2024 12:28:23 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:857f5a19ac65ee05564ff4fa62b0decf9c89d576b102aa2c90fae7731a4da415`  
		Last Modified: Tue, 03 Dec 2024 19:42:24 GMT  
		Size: 6.2 MB (6206255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:3a932ca6bce91405f2633a0e101a769ce7d5bdf0ca5826496f9e18d616e8ec1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2478255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8678ac55800b22f1057dfe17c4d8e06a2ad45046e37a1275aa869cc17a5790`

```dockerfile
```

-	Layers:
	-	`sha256:e19f3a585dfc343200997fc78bcf79388220c9375faec40863947cf68450a5ae`  
		Last Modified: Tue, 03 Dec 2024 19:42:24 GMT  
		Size: 2.5 MB (2468871 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5074e1f2945221b5dcdf2bd010dc3018b55badba8bd48f51995cd98e419da140`  
		Last Modified: Tue, 03 Dec 2024 19:42:23 GMT  
		Size: 9.4 KB (9384 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:c37e08b0d46b533e69c10c0e11bf861766cbe986f745ee119bf5e8bad2a4ec35
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53528410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3185ae235f7fefdc1796e662d1124179d587276ccf17a4cda5ea80daf1dae60`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1733097600'
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.11.10
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=07a4356e912900e61a15cb0949a06c4a05012e213ecd6b4e84d0f67aabbee372
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bb3f2b52e6af242cee1bc6c19ce79e05544f8a1d13f5a6c1e828d98d2dbdc94e`  
		Last Modified: Tue, 03 Dec 2024 01:30:11 GMT  
		Size: 28.1 MB (28058810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e88090b39a19b3e4a9f95f2a3043886f41461282cccea8072ad8f29213b9c5fa`  
		Last Modified: Tue, 03 Dec 2024 09:05:11 GMT  
		Size: 3.1 MB (3137738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1de48ef0f3fc94a8a11350b14f218f8e0fe589580f458c369619605e4b8df955`  
		Last Modified: Tue, 03 Dec 2024 09:30:16 GMT  
		Size: 16.1 MB (16125649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffbc83a7526a8264586e2f3926c99f8147947b5a9d6ad2fd931e938b05bcca0`  
		Last Modified: Tue, 03 Dec 2024 09:30:15 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e89f54e91fa4b085782013060a1dbaba9c0e19fa3806369d54763c17cd6176f7`  
		Last Modified: Tue, 03 Dec 2024 16:04:15 GMT  
		Size: 6.2 MB (6205963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:8f2b8587692ac7b3934b6824749ffe68708c13f05125ab9dd6b4be6229d11158
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2476320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79cdef55f1088e49a42eac12b045fa78f48cc019f50bd89c6b60e11565e99528`

```dockerfile
```

-	Layers:
	-	`sha256:f220e5cce2e2021080e34fa8c61f99d55b8fc1fa26f6da658c36edab2d40c701`  
		Last Modified: Tue, 03 Dec 2024 16:04:14 GMT  
		Size: 2.5 MB (2466891 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:643a691b0152e0fa6f0901c097772a26b465a2752212d60753a372197ef44a74`  
		Last Modified: Tue, 03 Dec 2024 16:04:14 GMT  
		Size: 9.4 KB (9429 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11` - linux; 386

```console
$ docker pull hylang@sha256:afd8c7c97bf3f2464c55917dd1e84acb3e33c991c59e5393a08465dcc60884ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.2 MB (55161922 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4996482da6d6c4509b3410a0bfed37a388a2f7a1f06ec3494fa8729409bc3819`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.11.10
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=07a4356e912900e61a15cb0949a06c4a05012e213ecd6b4e84d0f67aabbee372
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe39b7dd2256dad6379a7cb02aa0e62f9c22b530b49fbeee0425b7ad73f4de7`  
		Last Modified: Tue, 03 Dec 2024 02:43:49 GMT  
		Size: 3.3 MB (3316836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b32ce6926929605f58d2811d9fc0e6080e68f344571d18dc67487e147bae192`  
		Last Modified: Tue, 03 Dec 2024 02:43:50 GMT  
		Size: 16.4 MB (16433626 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420dbbad2917bca205d005ed75c28b50209b8f71d9a8138120cbe6b2dbf811d6`  
		Last Modified: Tue, 03 Dec 2024 02:43:49 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffaa246457e890e0f0cd81c0e8be9929f9d003e8224285a5e7a850b779b58203`  
		Last Modified: Tue, 03 Dec 2024 03:23:02 GMT  
		Size: 6.2 MB (6205723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:9b679de10503f3a4e3e87a81a107b34cf84a93d94d12587d6840d5828ae35b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2472875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90506ce655b4b286341013cbee3b47cd3b0b7eae26a6079fe98e6d89f2774479`

```dockerfile
```

-	Layers:
	-	`sha256:8e21ed1bdc46d43a2f79b2b1452987263d0050e84d60a9b4e7ddfa14e1e980ba`  
		Last Modified: Tue, 03 Dec 2024 03:23:02 GMT  
		Size: 2.5 MB (2463650 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1115ed7a92587919c1a21b5a5a6fe1a55f44db48378c69525a8ac228c1d8ccd`  
		Last Modified: Tue, 03 Dec 2024 03:23:02 GMT  
		Size: 9.2 KB (9225 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11` - linux; ppc64le

```console
$ docker pull hylang@sha256:6ee22e9485f3b8c99d9fe642e9e4a4aaa800c9e8412d1a4ae8c2c34745399463
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.6 MB (58626752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0abda35892ff92e28ac86306372764e96235b972c44de4b3b7a72a0daac1be32`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1733097600'
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.11.10
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=07a4356e912900e61a15cb0949a06c4a05012e213ecd6b4e84d0f67aabbee372
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e62b6946337cc6b72ec307008f1acc46e12a4f98e6f0e29c92b5538bbafd7ce6`  
		Last Modified: Tue, 03 Dec 2024 01:28:28 GMT  
		Size: 32.1 MB (32063265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ba68a8efae139652387c0a6040f41e0ece6c5c1566515128c32008ed23c9611`  
		Last Modified: Tue, 03 Dec 2024 07:17:46 GMT  
		Size: 3.5 MB (3520170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75e9c2a02fa7fc703af31b195c58a2d1e5a43dc173f829f170204920361b74b1`  
		Last Modified: Tue, 03 Dec 2024 07:34:00 GMT  
		Size: 16.8 MB (16836830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7173e24abb2d0cf869dbf8e5158ca10597ba7dc744d4a9249aaf28a48316795d`  
		Last Modified: Tue, 03 Dec 2024 07:33:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9a039b4578d0a65803259ab7190eebc40fd50a692b37d0672d7caa88da131da`  
		Last Modified: Tue, 03 Dec 2024 15:59:37 GMT  
		Size: 6.2 MB (6206239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:45c48c14dc93c46cce5066ae0c85bb49da855a81747ad0c5ed2e0e4b9486c570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2480331 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8520ece1c33d7f5b2062945feba822cd1f9054a4968000b705f188ca9d3bd90e`

```dockerfile
```

-	Layers:
	-	`sha256:ba6c40192649e717fc3e1aa1a130e4c21e97571f04b67b7cc91a053aebee3299`  
		Last Modified: Tue, 03 Dec 2024 15:59:37 GMT  
		Size: 2.5 MB (2470986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:06cb2f02b4555379c57f9896205ea48328a1b17cfcedd0f63904546eb5b3f61c`  
		Last Modified: Tue, 03 Dec 2024 15:59:37 GMT  
		Size: 9.3 KB (9345 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11` - linux; s390x

```console
$ docker pull hylang@sha256:1c3eee7b7bbf83e2cab04624e11dcc344e9dde5747c1353ecc25f46099a116b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52101629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3258ad54c760dda8c97acde0551aab09f4db1bf32fddcb3545d846ef1e2df0c`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 08 Oct 2024 19:58:40 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1733097600'
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 08 Oct 2024 19:58:40 GMT
ENV LANG=C.UTF-8
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_VERSION=3.11.10
# Tue, 08 Oct 2024 19:58:40 GMT
ENV PYTHON_SHA256=07a4356e912900e61a15cb0949a06c4a05012e213ecd6b4e84d0f67aabbee372
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==65.5.1' 		wheel 	; 	pip3 --version # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["python3"]
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9378ae44108012049addde60d193467e2b15a247b2f953ad5c27e073c4573d42`  
		Last Modified: Tue, 03 Dec 2024 01:28:18 GMT  
		Size: 26.9 MB (26878971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20e060c6c4e7ea69f8ea280fa8a0b48f72e5a9cd7a445ea87d0a7a5d70254957`  
		Last Modified: Tue, 03 Dec 2024 06:29:22 GMT  
		Size: 3.0 MB (2980790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4bdfc1878eb1c9a00d8639101970e82f3a5d9b19b4534c4c302ff9700000dbc`  
		Last Modified: Tue, 03 Dec 2024 06:42:03 GMT  
		Size: 16.0 MB (16035843 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5762d7269e423f154ea3b0c64db05b52357242482839395600c8fd68edd97dba`  
		Last Modified: Tue, 03 Dec 2024 06:42:03 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f11b1bb45354724c026516e4727f5762d58817e1d381da1a1df0c06fbd0dc3d`  
		Last Modified: Tue, 03 Dec 2024 10:23:05 GMT  
		Size: 6.2 MB (6205774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:b7c86c928c4c6dabafa8a85a0ceda846bb98adae8b4186dbd81d129ae69562c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2475557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c2881b01f219600fb47d7afc775b2a98781a52136561a78c0c244a6330691af`

```dockerfile
```

-	Layers:
	-	`sha256:b2f944981239ab6c481daf8d2e562dfe511dbe94a1c93ed5a9d558062b515f1d`  
		Last Modified: Tue, 03 Dec 2024 10:23:05 GMT  
		Size: 2.5 MB (2466280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:167bff63627d9907b5551560b170c5d659671be73cac673a7f9e943c327b8fb7`  
		Last Modified: Tue, 03 Dec 2024 10:23:05 GMT  
		Size: 9.3 KB (9277 bytes)  
		MIME: application/vnd.in-toto+json
