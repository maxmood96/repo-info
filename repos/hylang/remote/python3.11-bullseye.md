## `hylang:python3.11-bullseye`

```console
$ docker pull hylang@sha256:1e98db29ad2b7bdf478d57c778135d6756eeab2fa02ccf4382ce8d8087d3d94a
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

### `hylang:python3.11-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:14d7fd96cd75bc1117de31bab44e05c8600206a46cfa2900361e5c51a4540a58
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.1 MB (54103802 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7240cfa9e0fe17cf96434063b663d11888b664a626d9d1a1902ef4ad9db5e8`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.11.9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da9bdc27ef4991ac3c74046b5d3c0f98285c56690ccd4368a32e2ee4d1cf6275`  
		Last Modified: Wed, 24 Apr 2024 13:14:56 GMT  
		Size: 1.1 MB (1078226 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97a259f9d0ca29e596fa806464c0b95f253ad1c4a109560502c79509b2319e9e`  
		Last Modified: Wed, 24 Apr 2024 13:15:56 GMT  
		Size: 12.0 MB (12031599 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29fbafc9c31dfacfa8173f4760e4b1f3a96bbaa4cdde6f0efdb6ed4fcd5c10ed`  
		Last Modified: Wed, 24 Apr 2024 13:15:55 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9d5cdbb1744e617e35c9f001b4fe09d2c6b9192207c99ffc19e08a571be52869`  
		Last Modified: Wed, 24 Apr 2024 13:15:56 GMT  
		Size: 3.4 MB (3424395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77fc6ee928b042358d8dde7687f77263d08c10890a9ccfcdfe102f8191eb7ea2`  
		Last Modified: Wed, 24 Apr 2024 13:56:50 GMT  
		Size: 6.1 MB (6135075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:2f4fe54251d63c1bb5d7ef461381abdccb79d38e340328ac7679a3bfac546242
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c06ba572d5e4776890bed71cc8a14cc8dc45841c2f571c38f46eee072b2078ef`

```dockerfile
```

-	Layers:
	-	`sha256:5780dd8e9cc03ae544a2d90dc688f8bb9363e3e12412f1a8c834fc806d6e8a0e`  
		Last Modified: Wed, 24 Apr 2024 13:56:50 GMT  
		Size: 2.7 MB (2683011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:00f4dd6804e1081c7686124fef107937b8d581bc90d42003de6ea11440b136b7`  
		Last Modified: Wed, 24 Apr 2024 13:56:49 GMT  
		Size: 9.2 KB (9150 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bullseye` - linux; arm variant v5

```console
$ docker pull hylang@sha256:e3ea1f5d41677a8e197a9aa2a448a9a7f63aaf2fe2f5f704508f4d9989cdd8f9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51300258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be035286a6a24a5cb9986758d745776c9718e5b9096732e3b0d105d4c4558389`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:4ccbd1f9bcc76d259ba2b235681f1b749e86690e8805ee49f9fb44abc9ff5dc2 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.11.9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
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
	-	`sha256:2438f3883cb848a901cb08a6c99ec3ef261d41ca6f0d5321f274d995c58fa24e`  
		Last Modified: Wed, 24 Apr 2024 03:57:14 GMT  
		Size: 28.9 MB (28936577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45a1ba506e6324f6b7f3739f88a626cf81ca8f3b949d6468cc78cbe37cf92438`  
		Last Modified: Wed, 24 Apr 2024 11:08:56 GMT  
		Size: 1.1 MB (1061195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b62a2e94daee37014d91b0d254d132ef4b21aade71eec2cccc4e563e8d4dbe`  
		Last Modified: Wed, 24 Apr 2024 11:09:45 GMT  
		Size: 11.7 MB (11743265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d09074b0d949124a1ee178e8b4de396e70108aa91cce7b93aa919259c5c5c142`  
		Last Modified: Wed, 24 Apr 2024 11:09:43 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c185ec383e0492cadeb71ad816286cac679d30ebc3e00edc33bfabb01c89e8b1`  
		Last Modified: Wed, 24 Apr 2024 11:09:44 GMT  
		Size: 3.4 MB (3423870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:029f7895340ae6ec25335b867e8cb9eaa36f851f51ce1528054c867a08b489c5`  
		Last Modified: Thu, 25 Apr 2024 01:15:51 GMT  
		Size: 6.1 MB (6135108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:01f5c1ddf2a3f924b880afbef5483d8255f7892b8141cb15a72b13498604581a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1897e322a219383e603349b09b66d447f96e0f202b1a13992dcdbcdf79b26ede`

```dockerfile
```

-	Layers:
	-	`sha256:cc6f45c68efaedd5853c29242183d78c497a921768b506035b51e63389c3da26`  
		Last Modified: Thu, 25 Apr 2024 01:15:51 GMT  
		Size: 2.7 MB (2683253 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37a9821f6ad5c98efff42527a3acd0abcd40a5b718265682e37893bf35c078b8`  
		Last Modified: Thu, 25 Apr 2024 01:15:50 GMT  
		Size: 9.2 KB (9220 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:2864fd0df5c86778f496492f1765d787dfe9a6237b31dbf2bf5c44ded1abb0bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48497092 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2d2621e26db00e986ea80f5eb5d311baf3fc245fcb9f496b60356665dcd9994b`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:f7685078edb9bb9e45a932713c0364f985baac4241d098518b48718ca3f587aa in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.11.9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
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
	-	`sha256:e373dd4d84cbc3bf4d587e26357a41105c418866d41051d5ad5d54c706941e10`  
		Last Modified: Wed, 10 Apr 2024 01:05:12 GMT  
		Size: 26.6 MB (26588474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1c14143f6e29cb70f615129565c8cd2db50a1cea76683eafb0ae0ecb1548a74`  
		Last Modified: Wed, 10 Apr 2024 06:17:00 GMT  
		Size: 1.0 MB (1042007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d81d68e2b508596eea2351bc0256dc176fba6d8daa421599240d661ae6d8c0a7`  
		Last Modified: Wed, 10 Apr 2024 06:18:16 GMT  
		Size: 11.3 MB (11308101 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22f1b4bc7ada4f63a5ce70613164006e50fd6e4c5d67f2639f3ac32ecce48a4a`  
		Last Modified: Wed, 10 Apr 2024 06:18:13 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49b859dabf49c5ea79b7d37328ff2a55c1ca1e227d801ad57282cf5440cbcdee`  
		Last Modified: Wed, 10 Apr 2024 06:18:15 GMT  
		Size: 3.4 MB (3423332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c71c19a05409671ca6cfa03ba6d54e425dfd424a4eda0c9501096c70895c55a1`  
		Last Modified: Fri, 12 Apr 2024 10:23:54 GMT  
		Size: 6.1 MB (6134933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:6abeb35e971f8177bc01476bb202eb1737026caf222eca17146235c8222ea2d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:895cbfbca5201c04dec9006bc26664e9b05aeab6ffcb967a019052557360e31d`

```dockerfile
```

-	Layers:
	-	`sha256:29a023ccbb09170e08e6ad9999eabecfcb08dc7c3f0f6363c158657ac517dcfc`  
		Last Modified: Fri, 12 Apr 2024 10:23:53 GMT  
		Size: 2.7 MB (2685105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d68925c3249ef3a1d1fb4d59d71fa2bc4427264b97bbd72c4166ef6bbfb27843`  
		Last Modified: Fri, 12 Apr 2024 10:23:53 GMT  
		Size: 9.2 KB (9216 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:d7f2b05c09bbe244c23e82e6b9d57edc0578f6a3ff1420e934b88dcd9a7cdad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52793235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee00da964c5692d03cf93d50ac8931dda62cbaf55dd686c83525951406ccdde6`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:b6a7ade0a9cb3d95d76b5cee3357ae94ff134a72609e260e046cda9537b31b9d in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.11.9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
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
	-	`sha256:778ddef5c8e3dfac8ba7265cbd22065f975b42a467e899f753d6d42d1b069da4`  
		Last Modified: Wed, 10 Apr 2024 00:44:46 GMT  
		Size: 30.1 MB (30076306 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1298edbf932e7e37b9f3dbe56a614b00cd314e1fe1a0cbc28c855d6eb0043075`  
		Last Modified: Wed, 10 Apr 2024 04:10:51 GMT  
		Size: 1.1 MB (1064443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffdb19db777cdd38cd9398a3fccff43116c1512e8223538f304959da38cba68b`  
		Last Modified: Wed, 10 Apr 2024 04:11:59 GMT  
		Size: 12.1 MB (12093684 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3f6657314016a730b97ac6c33e65721eeddc58498388974e15be7bc9b297e06`  
		Last Modified: Wed, 10 Apr 2024 04:11:57 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a9f5e44a2152b2165ae5edff4987dc159ef301da458573642d196878ad7f0ff`  
		Last Modified: Wed, 10 Apr 2024 04:11:58 GMT  
		Size: 3.4 MB (3423470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db1f10fc55856f87ccbbd72d04a09d41fc0341334584a75a61d3c29f6b8a9b2`  
		Last Modified: Thu, 11 Apr 2024 10:02:09 GMT  
		Size: 6.1 MB (6135089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:89630aeb7809ab5c230794e7187e94706718aa6a59933f30f69f92505aa9bbc1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692226 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346bf7d3721dc0f5b649208209cae01469cbe049ae2ca60be5497ea6057153be`

```dockerfile
```

-	Layers:
	-	`sha256:f7a2b23b6f5594c8e820816477a3121e373a1082839ca7ddac645b7dc13aad04`  
		Last Modified: Thu, 11 Apr 2024 10:02:09 GMT  
		Size: 2.7 MB (2683070 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b7aa4841a66e1d3ee7b3f8e3d8fc9e2b5c27276e980acbe9c2a601b4e405d95`  
		Last Modified: Thu, 11 Apr 2024 10:02:09 GMT  
		Size: 9.2 KB (9156 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:25a9b0cd43138aa7d8a4b2f2cfb32769129cc3c41977ff5b8405600acc72f254
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.2 MB (55198338 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f77904ed18cfc92d94822cf0d1eefc2557b50d326a889fc1ce4bdfc603377620`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:51089e94fd65259117206f5ee6b1fd709e8c1754176d4f625ae49abbee751047 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.11.9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
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
	-	`sha256:112c04b2ac24eb2c6dfef961130b9b3d298e6d4b8e125bbebaa1137d773f7d7d`  
		Last Modified: Wed, 24 Apr 2024 03:44:22 GMT  
		Size: 32.4 MB (32424773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5ac7a2bad38d481d6b7d7eab67e963ee845b84f86a8b6194e45c1af3f491dc`  
		Last Modified: Wed, 24 Apr 2024 13:18:04 GMT  
		Size: 1.1 MB (1090979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89dffb33a40ec1b2ee5246559f4fbd3b80b8c0486267e9c37a62a90a728ee1d7`  
		Last Modified: Wed, 24 Apr 2024 13:19:04 GMT  
		Size: 12.1 MB (12123369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a92d9e431ae32ed831e3994f39c31a964cebcaa4e4b16da00129118e98e0c74`  
		Last Modified: Wed, 24 Apr 2024 13:19:01 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928ef8a73bf033afd63c9f3d3b5ccf5c2d7872d3dadf680e335beda78be21d13`  
		Last Modified: Wed, 24 Apr 2024 13:19:03 GMT  
		Size: 3.4 MB (3423924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f753c92a1f54fbc83ab33359e75e276cfa9a809b1bf6342c315494a8ffd7cc5`  
		Last Modified: Wed, 24 Apr 2024 13:56:48 GMT  
		Size: 6.1 MB (6135050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:35e688116c8c9f91a898320e188c4695000438e8416851aeb3ff038c2266c754
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7f9597e95a85eb822b936c66f086115082eade646b36fdf7b2899cc3fd6af01`

```dockerfile
```

-	Layers:
	-	`sha256:6191141325df9c8682e4f4f57dac8c70e24779c60f5572e43a650c310f8d5357`  
		Last Modified: Wed, 24 Apr 2024 13:56:47 GMT  
		Size: 2.7 MB (2680117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:021348a62dc0885f95c6eb8852ff8a3b57bc72c31438ecbe06af034adbb39df1`  
		Last Modified: Wed, 24 Apr 2024 13:56:47 GMT  
		Size: 9.1 KB (9121 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bullseye` - linux; ppc64le

```console
$ docker pull hylang@sha256:e73411ea8c13bd3e944fbe804bd82d7cacad8a4b9bf5553960056624962ff38d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.3 MB (58340288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83842a2ac46272e00525cfc14d9304395d2378bbef44689d22141f41ae229495`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:33f8251ee78dc536740a4ab4a9c9a75ab2c3f5d7be0a41f41dea318cc8e93dbd in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.11.9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
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
	-	`sha256:2608681ad30ed92fce8f1b566ae32649b5bfa30cc4df8792977ed14a0bc7cbe6`  
		Last Modified: Wed, 10 Apr 2024 01:32:01 GMT  
		Size: 35.3 MB (35304089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9131144283edf66263b4e2b710e8a59aecc7ab54561a0a207fb414bb6e68fb9`  
		Last Modified: Wed, 10 Apr 2024 06:21:14 GMT  
		Size: 1.1 MB (1095282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2cf13de52dd2bb3b187a6a6f749e00c4417cb0fac35b3bd0f247ef567dcfa78d`  
		Last Modified: Wed, 10 Apr 2024 06:22:27 GMT  
		Size: 12.4 MB (12381009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4a36493ff14d6f27b5a10904f0282d9f3855a296f9dddb3d82cb32b0f155612`  
		Last Modified: Wed, 10 Apr 2024 06:22:24 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9927c9a961dfe9f5b7c0e3aa7321ed9f1327fade98305eb7198ad18522cb8bf`  
		Last Modified: Wed, 10 Apr 2024 06:22:25 GMT  
		Size: 3.4 MB (3424373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a7ac46cb63c4050a5ca9aba7367c3ba0eb6bd88908a89d8abbc5b8e725f1d77`  
		Last Modified: Thu, 11 Apr 2024 09:14:30 GMT  
		Size: 6.1 MB (6135291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:bff76452d86c5c9253aac2eb499b137b451fd9f2e8756483a93d7bc8ba8b010f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0beb9e42fbb889e554a6a2beaae8d8633a08f6a4187fd126776f36a187d6198b`

```dockerfile
```

-	Layers:
	-	`sha256:84220bb1f3989df979c5b4fa32ed43f5ae7f691bb92b56c6d77d4cad1a375bfd`  
		Last Modified: Thu, 11 Apr 2024 09:14:29 GMT  
		Size: 2.7 MB (2687232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8697f64cdeb68b330b520181a788acf93e5449bcf5e665bc239d6ee4d6eca84f`  
		Last Modified: Thu, 11 Apr 2024 09:14:29 GMT  
		Size: 9.2 KB (9184 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11-bullseye` - linux; s390x

```console
$ docker pull hylang@sha256:cc154a0151c7bcfe17de538f4724de161b4e3b02d2bcb26af3e179a61e131008
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52289474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89ab4c5c9bf33e289363e601651153d362587ed1a3e0b0eb8eff0ba02c08d8b7`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:173b309178d19f7fccea713c7c575233510e5f065fd2d92a5378f001a1d33846 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.11.9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=24.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
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
	-	`sha256:499f72f2d94381b6df4b58d8ad4918f9e03fc5d140cb0704842fd78e2e63e391`  
		Last Modified: Wed, 10 Apr 2024 01:49:00 GMT  
		Size: 29.7 MB (29666840 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef8ed15e1623b295ee0caf240f20a1ae5e90d7fc5c0c62062e38d7f66234b0e5`  
		Last Modified: Wed, 10 Apr 2024 06:08:20 GMT  
		Size: 1.1 MB (1076184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6877a35ce202b6b2fa1bfc11855d6f0f3c6eb1d3171d25ef97bccfaaaae968f1`  
		Last Modified: Wed, 10 Apr 2024 06:09:13 GMT  
		Size: 12.0 MB (11987846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dda660ae2bcc421de8333eb5e3159d6d0e03aac898e65f816e3bb6edf3cf152f`  
		Last Modified: Wed, 10 Apr 2024 06:09:12 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abd8c01f78c3655dc9245d8aec0dedb652035f334eb3d9a40931dc7d838375ea`  
		Last Modified: Wed, 10 Apr 2024 06:09:13 GMT  
		Size: 3.4 MB (3423398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0f14361906d06ee65307080cd891ba74a42e84ecf46e90203614fbb2408bcf7`  
		Last Modified: Sat, 13 Apr 2024 18:19:44 GMT  
		Size: 6.1 MB (6134963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:5a76b811d67341eabdd4cbf7f360d61d7035bf26526799ed93c6f0cb58d2154d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692197 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8358f09a4b3d9102442258e27a6fee3c26193c4d582ca81e548fc673563f958b`

```dockerfile
```

-	Layers:
	-	`sha256:01e069779e2c39b2af0c751d7fafa47d5ae45bd6e4a785e7e4d9b6a838f11d8d`  
		Last Modified: Sat, 13 Apr 2024 18:19:44 GMT  
		Size: 2.7 MB (2683051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e1bf001e54a331b4cc06e5206ed6fc0d9d62af07cda3a12c84b39ca7a008d91e`  
		Last Modified: Sat, 13 Apr 2024 18:19:44 GMT  
		Size: 9.1 KB (9146 bytes)  
		MIME: application/vnd.in-toto+json
