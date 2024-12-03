## `python:3-slim-bookworm`

```console
$ docker pull python@sha256:f2d472e6f0633f885dbf5678bfa846c34ddad63e262fbb936b4a7d35ac6afac7
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

### `python:3-slim-bookworm` - linux; amd64

```console
$ docker pull python@sha256:b0c5cb8792bf58879f532c1e10f44e1af02d72735758374198f9717d67a7ae52
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44103781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d555597bdbad4bdccbc7875b3eee70ede09d6727e54afec5f1471c1c5665599`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 18 Oct 2024 23:23:40 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_VERSION=3.13.0
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_SHA256=086de5882e3cb310d4dca48457522e2e48018ecd43da9cdf827f6a0759efb07d
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:bc0965b23a04fe7f2d9fb20f597008fcf89891de1c705ffc1c80483a1f098e4f`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 28.2 MB (28231580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcccf87d013dafa7f4bd6b72c6c3c1f5a3a347e626690a07568d0a925cfb262e`  
		Last Modified: Tue, 03 Dec 2024 02:29:59 GMT  
		Size: 3.3 MB (3317321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acee09de1c5d11742e97e43b537a9c6dd6ec1346a50b75e9b68f39de44a4216f`  
		Last Modified: Tue, 03 Dec 2024 02:29:59 GMT  
		Size: 12.6 MB (12554630 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a576ef79af7ef1fe063c34530a90c344f6d622795c713ff9f2a771f3edc00cee`  
		Last Modified: Tue, 03 Dec 2024 02:29:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-slim-bookworm` - unknown; unknown

```console
$ docker pull python@sha256:25491f3e46c4a9e417cc553d897108d8adebb2e52cb6964917636b99010f7c18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2433198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:479c10e1d1f061646da536387d22435b3a9d311644622fa29dfa0328bc971954`

```dockerfile
```

-	Layers:
	-	`sha256:7eeb505355f69c4b2fd81bcd5c5f65d84d86abbe313354998e9a0e93bbcf99ec`  
		Last Modified: Tue, 03 Dec 2024 02:29:59 GMT  
		Size: 2.4 MB (2410655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:029a200bc83e5ada11beab44d1f4791a6149fa70b79560f56948f45dc69bdd4a`  
		Last Modified: Tue, 03 Dec 2024 02:29:59 GMT  
		Size: 22.5 KB (22543 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-slim-bookworm` - linux; arm variant v5

```console
$ docker pull python@sha256:1876ffee831600fc62602b748553c3fd1e756c43298a58fd5471e342329af0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.0 MB (42011836 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6ed2ef0445a78789debf6c5622a9a05d1dc708f7c303e3a8f2392a6399487d0`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 18 Oct 2024 23:23:40 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
CMD ["bash"]
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_VERSION=3.13.0
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_SHA256=086de5882e3cb310d4dca48457522e2e48018ecd43da9cdf827f6a0759efb07d
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:5ecbccf2cc6c4ffb179160d83e2f057a548b6aea719fc2b9b49c502da3d570e3`  
		Last Modified: Tue, 12 Nov 2024 00:55:10 GMT  
		Size: 26.9 MB (26890058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d63160e5f2b63ac023f3d80c3643198f26c2af7d25f48ab6f7e845ccb7b83a`  
		Last Modified: Tue, 12 Nov 2024 08:41:42 GMT  
		Size: 3.1 MB (3082327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d80407e40868c5937de19aee4f52c04ab2d5c58957d91738a6ae22814753d9c2`  
		Last Modified: Tue, 12 Nov 2024 09:07:46 GMT  
		Size: 12.0 MB (12039201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe78d739f5c9082d280b5a2e61b97511a4576533957123dfb091e33928b811ee`  
		Last Modified: Tue, 12 Nov 2024 09:07:45 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-slim-bookworm` - unknown; unknown

```console
$ docker pull python@sha256:1814434e32a0f93af13f80d428b006077728e157fb567cbffdb3a8e4308914ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2438115 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb1447bed1624e4eb8b84b48ae6032f5dc6ed001dfddf3c103100e64b440b7de`

```dockerfile
```

-	Layers:
	-	`sha256:8bcdaf2e7f05bcc0d6ca61bbc3b92c18f6d289ec081ecfc4a6ebee32fcbbff36`  
		Last Modified: Tue, 12 Nov 2024 09:07:46 GMT  
		Size: 2.4 MB (2415438 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:af17e163e92c928f4a1ed02b38a1dc2828df1797f80f050448eebe1dea621f5a`  
		Last Modified: Tue, 12 Nov 2024 09:07:45 GMT  
		Size: 22.7 KB (22677 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-slim-bookworm` - linux; arm variant v7

```console
$ docker pull python@sha256:5d64b8b2688c0843967e3845e7b144b9e80970286f88bb02306b8f3a6cb92392
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39297467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b9c67b089d900778251cf7b79aaf4174fef48ca62c4b98e631080489bdfdf89`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 18 Oct 2024 23:23:40 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
CMD ["bash"]
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_VERSION=3.13.0
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_SHA256=086de5882e3cb310d4dca48457522e2e48018ecd43da9cdf827f6a0759efb07d
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:ddd3c6488ea8b62db6811ba136fe14cba70219532910e67a91ed3388ec9f5757`  
		Last Modified: Tue, 12 Nov 2024 00:56:42 GMT  
		Size: 24.7 MB (24718909 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59c4bfae3208db1cc5e6056b1b437ead34955dc06d861e28ba3a55e24b0f301f`  
		Last Modified: Wed, 13 Nov 2024 01:46:58 GMT  
		Size: 2.9 MB (2914823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b06f4b6a431b83dc17644f0fd7cdb4a938941d112cd8b73d34da99ea24db8b9d`  
		Last Modified: Wed, 13 Nov 2024 02:42:17 GMT  
		Size: 11.7 MB (11663486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54010aca04da3581fe07f44ffe67f44ed1da83640f2121fdc7681aee5b50008c`  
		Last Modified: Wed, 13 Nov 2024 02:42:16 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-slim-bookworm` - unknown; unknown

```console
$ docker pull python@sha256:30a0c739a833c4344a7c7c55850f6b0a5ea9ff9224f90af1b0954188c5459fa7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2436855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005db629bf008b943fce081e87253b40f87f8b9f45f152089af0d2e191f40053`

```dockerfile
```

-	Layers:
	-	`sha256:bb1d45170be2c93661e7bd2ae24b5adcc44659f1b22aa1db3252d17f1bc172d6`  
		Last Modified: Wed, 13 Nov 2024 02:42:16 GMT  
		Size: 2.4 MB (2414179 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7ec244cd5ad03fe61a4730dcba32f6ddfe37a7dcf7f315fdebfadea2ad354f05`  
		Last Modified: Wed, 13 Nov 2024 02:42:16 GMT  
		Size: 22.7 KB (22676 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull python@sha256:a331635c51b8075c62c244b18f72934b6de2df6985f1d3adb90875dcc1ccf8d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44918698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e99ff6eabdf506067dd3ed0d387b5df06aba0b5ec3c49239dacc256a0d93ef7`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 18 Oct 2024 23:23:40 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
CMD ["bash"]
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_VERSION=3.13.0
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_SHA256=086de5882e3cb310d4dca48457522e2e48018ecd43da9cdf827f6a0759efb07d
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:6d29a096dd42e5e003949f934fa6b1a3ec8e076dd8cfc2a85a4e750a3639bf7a`  
		Last Modified: Tue, 12 Nov 2024 00:56:55 GMT  
		Size: 29.2 MB (29157356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e91ee31b4ebfcb39ea9ba6ce1a809ecf2cb20e34911e24306f962f7038edfcc`  
		Last Modified: Tue, 12 Nov 2024 20:26:43 GMT  
		Size: 3.3 MB (3332014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f7e82f83815d599042146404728cc6e0507b18ad1d6b67319b7e9cd30f25fff`  
		Last Modified: Tue, 12 Nov 2024 21:06:38 GMT  
		Size: 12.4 MB (12429079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ce972ab4a43b26d6ae3a965effd4c0401c5d41132676ad6f906957212879974`  
		Last Modified: Tue, 12 Nov 2024 21:06:37 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-slim-bookworm` - unknown; unknown

```console
$ docker pull python@sha256:c933fbc782387a04bc9b452bc09e250d81b2148b3bac93afa898508bb27758d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2434941 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeaabc6c8f21901f0af7fd4ffb555868b89fb35d3cdb12a62754ecaddbf40505`

```dockerfile
```

-	Layers:
	-	`sha256:b8ecb73a91a4a1e0601160f3ec1a57b5e377a07aeeea87f5687ddfe65ad83ccb`  
		Last Modified: Tue, 12 Nov 2024 21:06:37 GMT  
		Size: 2.4 MB (2412215 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d4cf625c4a02af7ab0cdd7182351875c0c1f343c5be8844e35dc1d53cbc1782`  
		Last Modified: Tue, 12 Nov 2024 21:06:37 GMT  
		Size: 22.7 KB (22726 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-slim-bookworm` - linux; 386

```console
$ docker pull python@sha256:cefd1373c80a74eb617bfb5a05f0c2d278e7a40600651ce6aeb668f03d9b344a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45307551 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2afe0ac3fbe7fab12dfa05c2fe9bcac960eca5496348e2ca570f6a367acb3bb5`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 18 Oct 2024 23:23:40 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_VERSION=3.13.0
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_SHA256=086de5882e3cb310d4dca48457522e2e48018ecd43da9cdf827f6a0759efb07d
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:ae6c80ee852fcccae85579165042a3767dcd1190112e87c9f22fa3e76a624c73`  
		Last Modified: Tue, 03 Dec 2024 01:27:10 GMT  
		Size: 29.2 MB (29205487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07acc7c26605f34644b7e09c90895c83eeb51a9452a2b6616b01f9e57f7ba0f1`  
		Last Modified: Tue, 03 Dec 2024 02:45:46 GMT  
		Size: 3.3 MB (3316837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c43fedfa38f74217844cea6d05dbc30e8a4c2e51be7ffa1c81947b373026f625`  
		Last Modified: Tue, 03 Dec 2024 02:45:47 GMT  
		Size: 12.8 MB (12784978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b383e2955db716df04aaec3b122d27e4464dfb6d688cf900d672a9a793014f2a`  
		Last Modified: Tue, 03 Dec 2024 02:45:46 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-slim-bookworm` - unknown; unknown

```console
$ docker pull python@sha256:9bf580cb81d3d00981b13bda55750e9cb904b2d72bb0ec904409bf684fce91bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2430245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59d9fe498a8947a4d65ed6a249eaebf03fd40db4ae24464c8592cf614cf8ca7f`

```dockerfile
```

-	Layers:
	-	`sha256:38c2eeeac86364837fd7fd33b761b6a6f39bdca5dfde44b5a994cdfa50df6fbf`  
		Last Modified: Tue, 03 Dec 2024 02:45:46 GMT  
		Size: 2.4 MB (2407757 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f98123be898e1772c2fd2e3d58eca82ed03d90c67e41b28ee3ce74c43700accd`  
		Last Modified: Tue, 03 Dec 2024 02:45:46 GMT  
		Size: 22.5 KB (22488 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-slim-bookworm` - linux; ppc64le

```console
$ docker pull python@sha256:ba86bfd8fac661824ed5a25428d4360bd5561c2376be3deb5c1ea1d3ee3a40b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49865672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a64e902db6c19eff3dc779f4fdaf91ffc1b3be9275880f603d11b6ac86cf3f`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 18 Oct 2024 23:23:40 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
CMD ["bash"]
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_VERSION=3.13.0
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_SHA256=086de5882e3cb310d4dca48457522e2e48018ecd43da9cdf827f6a0759efb07d
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:75e0ed8549227769329d9bb009b10ff68c47929fad577311f0d99115885347ef`  
		Last Modified: Tue, 12 Nov 2024 00:58:20 GMT  
		Size: 33.1 MB (33125353 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3763d3cbcc89420e3619a6d313adf9fd5dce8940eb31b61d8544d75a713990ca`  
		Last Modified: Tue, 12 Nov 2024 11:29:49 GMT  
		Size: 3.7 MB (3713651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f31553e39e713cf02a0c0d38e23162f6b9f89369c6fc5c72bcd849cfa3626ad`  
		Last Modified: Tue, 12 Nov 2024 12:04:41 GMT  
		Size: 13.0 MB (13026419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90e68ed501c534290430a491c3859e98a6b1e059420174feeab6a4081ce32c55`  
		Last Modified: Tue, 12 Nov 2024 12:04:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-slim-bookworm` - unknown; unknown

```console
$ docker pull python@sha256:d7b7cb43fadabd628094c6292ff6cc1f2a97cb9d5a78a44c1f2011a1847cd7ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2438880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a97e5fc9a61a4ba16bb4f4f96d1bba4452f766d6b127a2ce8c365653b6fc9218`

```dockerfile
```

-	Layers:
	-	`sha256:13bb91c7d2f37f5801aa6c36f10e6b44881d252cd6f04a37126781215c876e7a`  
		Last Modified: Tue, 12 Nov 2024 12:04:40 GMT  
		Size: 2.4 MB (2416264 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8cc63f45560b51398b509afe835a66ed9bd6737ab02c01a85e6bbdfdd852b627`  
		Last Modified: Tue, 12 Nov 2024 12:04:40 GMT  
		Size: 22.6 KB (22616 bytes)  
		MIME: application/vnd.in-toto+json

### `python:3-slim-bookworm` - linux; s390x

```console
$ docker pull python@sha256:aafa92f4ccc9805331646fc7fa0341dfe8183e3e0349eb30ac4dcd04beb1ee67
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43005309 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:984c0540bbd2c1b5dedb1d61f716c9fd828fcd44114a21cee5ff56d33ed14a8d`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 18 Oct 2024 23:23:40 GMT
ADD rootfs.tar.xz / # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
CMD ["bash"]
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_VERSION=3.13.0
# Fri, 18 Oct 2024 23:23:40 GMT
ENV PYTHON_SHA256=086de5882e3cb310d4dca48457522e2e48018ecd43da9cdf827f6a0759efb07d
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 18 Oct 2024 23:23:40 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:fa8cb447c1a4d7decc9cbf4223b78597699fc7980d77431c085cd6cf32c5b3ed`  
		Last Modified: Tue, 12 Nov 2024 00:59:17 GMT  
		Size: 27.5 MB (27491628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8325008f111f1461de1fd965973c41f920fffd12b8f572285d1ba7fe8caae46`  
		Last Modified: Tue, 12 Nov 2024 19:10:25 GMT  
		Size: 3.2 MB (3173170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d070cea61ae6ec1828044131f7cc5e14ec538d24377320a192dbc5b7a1591287`  
		Last Modified: Tue, 12 Nov 2024 19:38:58 GMT  
		Size: 12.3 MB (12340262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d9af391ebdaacd5e28720906af84292a432fe40bb0e06891403a7e400dab08`  
		Last Modified: Tue, 12 Nov 2024 19:38:58 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:3-slim-bookworm` - unknown; unknown

```console
$ docker pull python@sha256:f01bac89c7221e7d3d13d108e16679629dd400a86772ad47b76e96815f70e44b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2434164 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ca3a53f2fb05ab5b354f2920f8ebab79a460dad0abff95b85db595fc088b76f`

```dockerfile
```

-	Layers:
	-	`sha256:9ed56154c8fcca63a4099688f83445b08a80ce35acc038f54acb37a9c25cd6b4`  
		Last Modified: Tue, 12 Nov 2024 19:38:58 GMT  
		Size: 2.4 MB (2411620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:145718aa30a2099d263f8d38b7b580909ea833d1c6a6c91dbbb30999623e6255`  
		Last Modified: Tue, 12 Nov 2024 19:38:58 GMT  
		Size: 22.5 KB (22544 bytes)  
		MIME: application/vnd.in-toto+json
