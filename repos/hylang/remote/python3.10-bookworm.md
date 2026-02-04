## `hylang:python3.10-bookworm`

```console
$ docker pull hylang@sha256:9db2b7afa48d0a59e42305204760877537b70ebf4ebdaf99a8d7677375170f01
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

### `hylang:python3.10-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:c249fcd482b87269bad91af469768e57c34458b302e58d61b095b150a7016f87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52286410 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fd9f4a60a42bd93245c5f052747da4e9b9a3b04774ec34f73fbe772965687de`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1769990400'
# Wed, 04 Feb 2026 20:15:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:15:27 GMT
ENV LANG=C.UTF-8
# Wed, 04 Feb 2026 20:15:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Feb 2026 20:15:27 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Feb 2026 20:15:27 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 04 Feb 2026 20:15:27 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 04 Feb 2026 20:31:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:31:09 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:31:09 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:12:40 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:12:40 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:12:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:12:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4831516dd0cb86845f5f902cb9b9d25b5c853152c337eb57e4737a9b7e2a2eb9`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 28.2 MB (28228487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64c98d67a0cbb2ae6a93577aac0580ece0b9a669660e1975dbf6445f6a70b4b8`  
		Last Modified: Wed, 04 Feb 2026 20:25:00 GMT  
		Size: 3.5 MB (3517404 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7939dbdfffa160cb3ec7942f66a2d393bff8117a5429728267e745329fd378ff`  
		Last Modified: Wed, 04 Feb 2026 20:31:17 GMT  
		Size: 15.4 MB (15373407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0b342eabc3c2f544ee81a7f35ba68beff6d5f502899c6c052723181e506e84e`  
		Last Modified: Wed, 04 Feb 2026 20:31:17 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eaf86571dddc5213092228f7148587f6864c1fda9605682ac1acc6294ddba198`  
		Last Modified: Wed, 04 Feb 2026 21:12:47 GMT  
		Size: 5.2 MB (5166861 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:56097438f94d89f860977633d860977eeb6d741133cfa614bcb21f733edec562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2631128 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:898b2d4b6c9b7bbfb44548ab1f581c3e5f81f5651e4c27314bc851f0a3c55ca0`

```dockerfile
```

-	Layers:
	-	`sha256:812ac0ebd29d2064df5002d633ba0daf27f6761ad34e17242fd6a5b591b675ce`  
		Last Modified: Wed, 04 Feb 2026 21:12:47 GMT  
		Size: 2.6 MB (2623034 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2d730e875cd015a5b866c6f929481bd1741a338c1c2cf095e0192dc7bbc83ca0`  
		Last Modified: Wed, 04 Feb 2026 21:12:47 GMT  
		Size: 8.1 KB (8094 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:f60b04915a58b9da08df5e5d4772bc4a062ae4b0dc86803abe208a8a7dc0d32d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48845717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92cc7ad9a64bcedf9d8229990365d0279af44adc579c4629ddc14811c8322c5e`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 03:59:45 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 03:59:45 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 03:59:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 03:59:45 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Feb 2026 03:59:45 GMT
ENV PYTHON_VERSION=3.10.19
# Tue, 03 Feb 2026 03:59:45 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Tue, 03 Feb 2026 04:10:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Feb 2026 04:10:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Feb 2026 04:10:27 GMT
CMD ["python3"]
# Tue, 03 Feb 2026 05:17:55 GMT
ENV HY_VERSION=1.2.0
# Tue, 03 Feb 2026 05:17:55 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 03 Feb 2026 05:17:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 03 Feb 2026 05:17:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6036aff531a372e1e9da48952322760c8c052f6735e66afd3251a32e5baace8d`  
		Last Modified: Tue, 03 Feb 2026 01:13:33 GMT  
		Size: 25.8 MB (25757618 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2a7e1f4ad35525a6c1f95723555daaa18871c0a91fa09745a81c5ee5eff0f9c`  
		Last Modified: Tue, 03 Feb 2026 04:10:35 GMT  
		Size: 3.1 MB (3091867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a71058f85dc371a5800ad6dc57f0af4c2de60d1fa04d8d67671eb8e620f8a0a0`  
		Last Modified: Tue, 03 Feb 2026 04:10:35 GMT  
		Size: 14.8 MB (14828924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ab6857c93a3f36cc7c8fd14a57851d6a1a6a96d8e5853cf126bca40e2d03fd`  
		Last Modified: Tue, 03 Feb 2026 04:10:34 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:154285f324311b6be9eec70c5806f20c89214b625f117c4bed89be910e53b77f`  
		Last Modified: Tue, 03 Feb 2026 05:18:02 GMT  
		Size: 5.2 MB (5167057 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:d6ef2e94d7b23b1cabe7601abdb8423f3ae44841e977a545cfbb36971789577d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:151d10b6815d9acf7a98c032e0066d44024f31a7ff07cb588d67af430b360405`

```dockerfile
```

-	Layers:
	-	`sha256:18325bc8e8d151acab174953c843b9add076be2293a6c9d69e9ed1fea185bc5a`  
		Last Modified: Tue, 03 Feb 2026 05:18:02 GMT  
		Size: 2.6 MB (2626854 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d6999530163b4e829c232542aa6c91e3338be27f78c643eaf04b60db97d6bee`  
		Last Modified: Tue, 03 Feb 2026 05:18:02 GMT  
		Size: 8.2 KB (8174 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:2ffc73e7f060ca5baaca857ea95907a5066cd93c3eafeb04bada4206242d0739
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.4 MB (46440151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bdbc4a39c53237017b079770fc1b6a67640a90029210b2a771a7477842e1585`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 04:27:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:27:09 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:27:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:27:09 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Feb 2026 04:27:09 GMT
ENV PYTHON_VERSION=3.10.19
# Tue, 03 Feb 2026 04:27:09 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Tue, 03 Feb 2026 04:37:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Feb 2026 04:37:49 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Feb 2026 04:37:49 GMT
CMD ["python3"]
# Tue, 03 Feb 2026 05:26:18 GMT
ENV HY_VERSION=1.2.0
# Tue, 03 Feb 2026 05:26:18 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 03 Feb 2026 05:26:18 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 03 Feb 2026 05:26:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6763f462e69d93f50a8712f0d5b2a26a36efcb65e2fab2dd4e1620eb3df42efe`  
		Last Modified: Tue, 03 Feb 2026 01:13:37 GMT  
		Size: 23.9 MB (23934092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef122c80d7f1900604d3af701eb91ff458fca338455616231cc6a30e88f09e55`  
		Last Modified: Tue, 03 Feb 2026 04:37:56 GMT  
		Size: 2.9 MB (2926398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e8e825c30fa94f2a1a428f1d8a05b966ca0f929606b6c86c01e204e2946ff85`  
		Last Modified: Tue, 03 Feb 2026 04:37:57 GMT  
		Size: 14.4 MB (14412219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26124e490fa5da83dcfb5b9ccb20529d26ec8caa0fbe9bbcabbd40f4a94ca663`  
		Last Modified: Tue, 03 Feb 2026 04:37:57 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a983964685e70d9e90959e7bd0dc1d8d1d98cd6140a36bec58ba52fae69a6b4`  
		Last Modified: Tue, 03 Feb 2026 05:26:26 GMT  
		Size: 5.2 MB (5167191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:f18afabb50cf8834ce0e4bc6e767bd4fefff5fb075b6a79b9715639146d26699
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2633475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3b2a52264ee29481c213d234ccc90a3d11df158996dcc0ac2e750ce2f2f6ae7`

```dockerfile
```

-	Layers:
	-	`sha256:cd6fc2240f7c2c8de6e5ab3e2cba78a00f61c83a4af0ee2a876b440294a49a68`  
		Last Modified: Tue, 03 Feb 2026 05:26:26 GMT  
		Size: 2.6 MB (2625303 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3779f2e1fbfea6a2c9e2be699d98fb94a558ca1092038fd878bfb8264d9c20c`  
		Last Modified: Tue, 03 Feb 2026 05:26:26 GMT  
		Size: 8.2 KB (8172 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:3d304e74090e79ef1640a0fd68d4b0609aa54119a3d86f9c7fae83cdb4c6265d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51933864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a557b7480f5b07e0189a7e7b7b32eb9769e6945b82d1906dc43b9d14ff5f2eb`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1769990400'
# Wed, 04 Feb 2026 20:18:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:18:06 GMT
ENV LANG=C.UTF-8
# Wed, 04 Feb 2026 20:18:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Feb 2026 20:18:06 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Feb 2026 20:18:06 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 04 Feb 2026 20:18:06 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 04 Feb 2026 20:38:13 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:38:13 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:38:13 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:10:54 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:10:54 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:10:54 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:10:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d3d5d8ab26d25b9040a3c2160d7ddfe3911ae81035d5b1b0904f3ebda32476b6`  
		Last Modified: Tue, 03 Feb 2026 01:13:36 GMT  
		Size: 28.1 MB (28107823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15197736cc235ef924ae407b4ee535fe5b5ec7b5f066801d04537139f5a0f4de`  
		Last Modified: Wed, 04 Feb 2026 20:30:29 GMT  
		Size: 3.3 MB (3349694 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7d58788f602c02ba2378381988b6665368c4851b9933a4a4cae8000a04b69bf`  
		Last Modified: Wed, 04 Feb 2026 20:38:21 GMT  
		Size: 15.3 MB (15309142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f24759406808ec70bf1a4fd8b6849e676c637bca70253d1386f2da8224a8daf`  
		Last Modified: Wed, 04 Feb 2026 20:38:21 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:455d46b213ad9489f977039724c0ddcf6dbdad6ad998ca7f9436cbf8e0e68345`  
		Last Modified: Wed, 04 Feb 2026 21:11:02 GMT  
		Size: 5.2 MB (5166954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:fbaa734d1d9c60477525673d4433a139cbe9a5e6b418f99d762dadafa1e77e24
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2631505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea04d586f08d00a163bbc8c74010f10a320b5272409e53d1c9a1baae29bbb523`

```dockerfile
```

-	Layers:
	-	`sha256:9a0b3252b3bcdad5646a2c5ebc0754a9b7f4abd12dfafd7e4015dfd6c4a5f080`  
		Last Modified: Wed, 04 Feb 2026 21:11:02 GMT  
		Size: 2.6 MB (2623307 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48cd55d485e33e5d9b844942c5b814d463ea671e73d6582ef1e4a841a2c0560d`  
		Last Modified: Wed, 04 Feb 2026 21:11:02 GMT  
		Size: 8.2 KB (8198 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:18f0670abc8e4b0c5381075badcd29ee71e6849f1c8bd5892f1a2f5b2dc3991d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53513971 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab3f19e3c5a3291b3bf5bfcef5ee94e00effe0d661944ea6f43abecf71d3d737`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1769990400'
# Wed, 04 Feb 2026 20:28:59 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 04 Feb 2026 20:28:59 GMT
ENV LANG=C.UTF-8
# Wed, 04 Feb 2026 20:28:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 04 Feb 2026 20:28:59 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 04 Feb 2026 20:28:59 GMT
ENV PYTHON_VERSION=3.10.19
# Wed, 04 Feb 2026 20:28:59 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Wed, 04 Feb 2026 20:36:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 20:36:31 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 20:36:31 GMT
CMD ["python3"]
# Wed, 04 Feb 2026 21:07:04 GMT
ENV HY_VERSION=1.2.0
# Wed, 04 Feb 2026 21:07:04 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 04 Feb 2026 21:07:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Feb 2026 21:07:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5f93d228262ac8f12d9af5f87a89d9722b3f4d559df30edfa91327db9f457723`  
		Last Modified: Tue, 03 Feb 2026 01:13:52 GMT  
		Size: 29.2 MB (29210015 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052b07fbc1dfb6ca632fbf9c490563cca0ab8aae5d53a46801e9d8eae6aecd87`  
		Last Modified: Wed, 04 Feb 2026 20:36:39 GMT  
		Size: 3.5 MB (3518056 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f9dd27309fa2e8ce61035e626e01898c8e52d1108fc9b26462604c3a221e2b3`  
		Last Modified: Wed, 04 Feb 2026 20:36:40 GMT  
		Size: 15.6 MB (15618757 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7c5146d222e79f169a7193a548b22b32c7a732d29bef71499d00db486af05a2`  
		Last Modified: Wed, 04 Feb 2026 20:36:39 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75235d547375d9f1a62e8f0d814a9e3bf558a3559073f1a175eb6d1503ef21cd`  
		Last Modified: Wed, 04 Feb 2026 21:07:11 GMT  
		Size: 5.2 MB (5166893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:bd2eb760a5d36134d5856ecda179d6d529799efa85b2eb8e27c6b5f8785027f4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c4b12d9b35ea118dd4155b8563dfa69dd44039a6bd5deae92ae733c3f7d38f6`

```dockerfile
```

-	Layers:
	-	`sha256:6a0e2cfebdebda7f395782861471cfc5b18678023e65316da4a083790f443f79`  
		Last Modified: Wed, 04 Feb 2026 21:07:11 GMT  
		Size: 2.6 MB (2620185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5db8db13b1eb3a8a9d64dbda185ec90e793e5a36becff64ad46008b601f9e617`  
		Last Modified: Wed, 04 Feb 2026 21:07:11 GMT  
		Size: 8.1 KB (8062 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:9f95153bd1bb0736c25bf16ae41933b42d7b31e5a383736f20c5a937011ff5b7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.0 MB (56950791 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f376f117f11b5a0680aca0a031117576330f087881bc20fd55080c20c2c59d`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 08:11:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 08:11:11 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 08:11:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 08:11:11 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Feb 2026 08:11:11 GMT
ENV PYTHON_VERSION=3.10.19
# Tue, 03 Feb 2026 08:11:11 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Tue, 03 Feb 2026 09:08:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Feb 2026 09:08:36 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Feb 2026 09:08:36 GMT
CMD ["python3"]
# Tue, 03 Feb 2026 12:56:47 GMT
ENV HY_VERSION=1.2.0
# Tue, 03 Feb 2026 12:56:47 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 03 Feb 2026 12:56:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 03 Feb 2026 12:56:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44f9b3b774eb4de46f4d3df8f11098fdd3e4e53c351c2785cefdcd390c4e8754`  
		Last Modified: Tue, 03 Feb 2026 08:36:34 GMT  
		Size: 3.7 MB (3722239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4279e094a2b8a175e6c5054a8f6a3820d3962ce1adf443b3a18cd2690a98d8e1`  
		Last Modified: Tue, 03 Feb 2026 09:08:55 GMT  
		Size: 16.0 MB (15991986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7636b78273f3326fe6cbdfd984613c4ce9ba302a8b1fe6060c6c848a80dd3f9`  
		Last Modified: Tue, 03 Feb 2026 09:08:54 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb9dd4a7916d722a864061364df2e52afb598ba63ac35f6b2390be57ea39ae3d`  
		Last Modified: Tue, 03 Feb 2026 12:57:02 GMT  
		Size: 5.2 MB (5167603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:d29b755b6235a830a412bd39a6c20ffd3890112b6157f2717405277db3b9e5d7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31140d24484fe0ac952f8b7d916ba4feebc62b646ef22ed7c72ff47c1a426974`

```dockerfile
```

-	Layers:
	-	`sha256:8bd905c6f25fa04c1a7ed42df0047da908cbcf00464d364f4f92d1086d015315`  
		Last Modified: Tue, 03 Feb 2026 12:57:02 GMT  
		Size: 2.6 MB (2627540 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:47288fecc48cc37cc9cdfcb10050ea13692ec9a150d3686ae628755b4db66a89`  
		Last Modified: Tue, 03 Feb 2026 12:57:02 GMT  
		Size: 8.1 KB (8138 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.10-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:ef4b32e685749c6153641bb2afe73be76249112ff497b241c239eea48c81926a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50399245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99a39f59b3231645daaaa71df4cfcabeb0b4f4e83b7760e8ea4f4bb6b3471c9b`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 04:34:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 04:34:09 GMT
ENV LANG=C.UTF-8
# Tue, 03 Feb 2026 04:34:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 04:34:09 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 03 Feb 2026 04:34:09 GMT
ENV PYTHON_VERSION=3.10.19
# Tue, 03 Feb 2026 04:34:09 GMT
ENV PYTHON_SHA256=c8f4a596572201d81dd7df91f70e177e19a70f1d489968b54b5fbbf29a97c076
# Tue, 03 Feb 2026 04:54:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 03 Feb 2026 04:54:49 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 03 Feb 2026 04:54:49 GMT
CMD ["python3"]
# Tue, 03 Feb 2026 06:03:24 GMT
ENV HY_VERSION=1.2.0
# Tue, 03 Feb 2026 06:03:24 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 03 Feb 2026 06:03:24 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 03 Feb 2026 06:03:24 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ecc55ea5c88be14e2088142b1ea9ace24ffd6e3f4d54fd2ead5df425a13dd658`  
		Last Modified: Tue, 03 Feb 2026 01:12:48 GMT  
		Size: 26.9 MB (26884382 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb47276a1118c9833131beac6cf010837f6f2a056d5859d63fae2b16fcb6b64f`  
		Last Modified: Tue, 03 Feb 2026 04:46:23 GMT  
		Size: 3.2 MB (3182708 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:522b611008d11e3f6c2961cf269fa32f22681d8e279fc826d0239450a5a06db0`  
		Last Modified: Tue, 03 Feb 2026 04:55:02 GMT  
		Size: 15.2 MB (15164928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e36112630bfb8bb5989a0bd4e85d3bca252f86c0f9dca7e1c16c3d11e1b6c73`  
		Last Modified: Tue, 03 Feb 2026 04:55:02 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4efaec1b3ab93778d58ea16cddbf0739ab6790519e638d1bf17d00a0998b3d1a`  
		Last Modified: Tue, 03 Feb 2026 06:03:36 GMT  
		Size: 5.2 MB (5166976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:4e9c0d1966f2cf9ae89ba96964d25708fc59d2b38bf4f3268a0d761903f7d632
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cde3366e7afffdca30e0f707077de99fdb5895bff552ce1e93a0b954b1507fd`

```dockerfile
```

-	Layers:
	-	`sha256:1a2147d068567b034636de5b56bd34a4a9b219ea7846e8a676593f445c03ca4c`  
		Last Modified: Tue, 03 Feb 2026 06:03:36 GMT  
		Size: 2.6 MB (2619850 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7447c48df4e0fbb4e1ff84e76e184265bf28c7d3eb5e9e64e62d3a832d1436e8`  
		Last Modified: Tue, 03 Feb 2026 06:03:36 GMT  
		Size: 8.1 KB (8094 bytes)  
		MIME: application/vnd.in-toto+json
