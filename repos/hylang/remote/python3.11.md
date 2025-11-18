## `hylang:python3.11`

```console
$ docker pull hylang@sha256:9dd183bb5aac3b24aad323da2d74695797cde05126caba82f4c008a44827137d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
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
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `hylang:python3.11` - linux; amd64

```console
$ docker pull hylang@sha256:b250ecf03d691f12cb6c4a0e2b273712a241283af7ba73a13b2982681a9555cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51101707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e416e0a7b044de7acf39b43027c9bc9ad4d3f887a36fafedfc5a1c999fa3058a`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 04:23:03 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 04:23:03 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 04:23:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 04:23:03 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 Nov 2025 04:23:03 GMT
ENV PYTHON_VERSION=3.11.14
# Tue, 04 Nov 2025 04:23:03 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Tue, 04 Nov 2025 04:30:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 04:30:30 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 04:30:30 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 07:55:33 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 07:55:33 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 07:55:33 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 07:55:33 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d7ecded7702a5dbf6d0f79a71edc34b534d08f3051980e2c948fba72db3197fc`  
		Last Modified: Tue, 04 Nov 2025 00:13:18 GMT  
		Size: 29.8 MB (29778104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ee9c106547f05aa380c4cdec2837c546439943d73d965a3fc49f228dc8be993`  
		Last Modified: Tue, 04 Nov 2025 04:30:40 GMT  
		Size: 1.3 MB (1292954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f002d17b63fe84a7f8a66f20cfa63aec4f6cd2a44069f05b6296b0abfcf2a8e1`  
		Last Modified: Tue, 04 Nov 2025 04:30:41 GMT  
		Size: 14.4 MB (14361415 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65868b001a40155a1d3f5aa7f5a10ba02a7d55697301839dc047c9d549b670bc`  
		Last Modified: Tue, 04 Nov 2025 04:30:40 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:673b814103e9b725db7fdc1b34f297d6c46d0fb1d9501e9a55576e67e340c41e`  
		Last Modified: Tue, 04 Nov 2025 07:55:45 GMT  
		Size: 5.7 MB (5668986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:e0071f9386b68a406396f15285af2ff90d59b2cafaf34d17023c2d67fa3f496e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ca07738f7b917b753af209686305cc9b445c093dbc4a95a8f0f7d4d7cd10e33`

```dockerfile
```

-	Layers:
	-	`sha256:7cf231a82968e594ae0d8b3469d8813b4821a9b241e97393152166e50b7ca583`  
		Last Modified: Tue, 04 Nov 2025 09:18:35 GMT  
		Size: 2.2 MB (2199915 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c942eca1ca2ea57652318efbd58377ac7e9bd91a4b0638a0d10c8b7a3e54a5c4`  
		Last Modified: Tue, 04 Nov 2025 09:18:36 GMT  
		Size: 9.3 KB (9320 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11` - linux; arm variant v5

```console
$ docker pull hylang@sha256:39d154b317679d67329a2443194156b6f25962305cce22a0a1b4e246a0820f66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48886450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c8f98cc92a2d2b387c0826e79cc294e6e4471c732544a833299eaf7e91de4a1`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 04:00:40 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 04:00:40 GMT
ENV LANG=C.UTF-8
# Tue, 18 Nov 2025 04:00:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 04:00:40 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 18 Nov 2025 04:00:40 GMT
ENV PYTHON_VERSION=3.11.14
# Tue, 18 Nov 2025 04:00:40 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Tue, 18 Nov 2025 04:18:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 18 Nov 2025 04:18:32 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 18 Nov 2025 04:18:32 GMT
CMD ["python3"]
# Tue, 18 Nov 2025 05:32:50 GMT
ENV HY_VERSION=1.1.0
# Tue, 18 Nov 2025 05:32:50 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 18 Nov 2025 05:32:50 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 18 Nov 2025 05:32:50 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:162369d92f5e2c9de9e4dd78eaef29867d62d539b2379a8248fff07e1ed9a4f7`  
		Last Modified: Tue, 18 Nov 2025 04:18:46 GMT  
		Size: 1.3 MB (1275912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c3b8360c67f50c75f9c514b653d5791e285d2911c83a1743c9ba8e67638f4a2`  
		Last Modified: Tue, 18 Nov 2025 04:18:47 GMT  
		Size: 14.0 MB (13996671 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cdcca8f71274d464373dca3cd60599650109bccbcfd8545939f2be0545bbe1e4`  
		Last Modified: Tue, 18 Nov 2025 04:18:46 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3550fecf454bc04de6fa11ada894821975d727635ecc5e1df14e809cc26e0f02`  
		Last Modified: Tue, 18 Nov 2025 05:33:03 GMT  
		Size: 5.7 MB (5669471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:9f8362160f3b7cccae9d221109d4a59218a3c7b8f29638db330dcc8807c90cd4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ca0332df6f2f6bd4174ff9833602941ad76f060b425d43f9ca60df9760988c7`

```dockerfile
```

-	Layers:
	-	`sha256:0a5301c7b3d0f67d22dc01a12ad2177ee7572a90793d6925982f4d6b5aef63a9`  
		Last Modified: Tue, 18 Nov 2025 06:19:22 GMT  
		Size: 2.2 MB (2202910 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5d659e8a890089a911ef7d1347d7bed520c044be3190f2f82f69001251e6370b`  
		Last Modified: Tue, 18 Nov 2025 06:19:22 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11` - linux; arm variant v7

```console
$ docker pull hylang@sha256:7664990eb37b98caece099a07b6790b9dfe0723c24c18e33aa3f0755cc398c21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46859928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76ded1b372755fbf2b54642c04d49a0f04f20dec94dc2ec588bdd09274823268`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 02:33:28 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 02:33:28 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 02:33:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 02:33:28 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 Nov 2025 02:33:28 GMT
ENV PYTHON_VERSION=3.11.14
# Tue, 04 Nov 2025 02:33:28 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Tue, 04 Nov 2025 02:50:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 02:50:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 02:50:06 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 03:41:59 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 03:41:59 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 03:41:59 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 03:41:59 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8945aefb71bd942499dd072e2c7c869b6b74b7c4dd83bff59c209b7b95d52a9f`  
		Last Modified: Tue, 04 Nov 2025 00:13:33 GMT  
		Size: 26.2 MB (26213039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5099abf1892e1ab9a7f8d6c848eeba0eb19b9d30fdf89ba5f131e29f2146a2af`  
		Last Modified: Tue, 04 Nov 2025 02:50:26 GMT  
		Size: 1.2 MB (1248448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1ed5d7644d447662f4297ac53055827c981ad70a122124a8cc86589d0700853`  
		Last Modified: Tue, 04 Nov 2025 02:50:28 GMT  
		Size: 13.7 MB (13729238 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5b1bbb3722c900ad5411a539f0dc7671aca2abdb7a54caf2c6fdc2a8efee06`  
		Last Modified: Tue, 04 Nov 2025 02:50:26 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cc7925ef75b04d119ddc0f4e93383b856e3e60af22bff7361f1279b37121132`  
		Last Modified: Tue, 04 Nov 2025 03:42:12 GMT  
		Size: 5.7 MB (5668954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:31c3e63441b1056cb3a440fc75d4ccbb741732baa5bd4de675e643eb3af0f069
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:addf4b7c2f03f1e303d4674842bfdff1e4d4a51b38bcc67955c8e4b8600e94f7`

```dockerfile
```

-	Layers:
	-	`sha256:e02088ca4b86d44660a4bed9a18a5cf51f02b43da3693377dd3df2ad02d60a48`  
		Last Modified: Tue, 04 Nov 2025 12:18:35 GMT  
		Size: 2.2 MB (2201369 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7085575a77a3e8f89345fa60d68a24b6076cffefbecbfe87ae9259b55dde2f09`  
		Last Modified: Tue, 04 Nov 2025 12:18:35 GMT  
		Size: 9.4 KB (9431 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:18240b786fec6eb83329c188436319d2fde100be1bfc5b15683a556f66de764d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51397946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64ad5d18ead3750ccaba274b6fe353f8a37ec76ae1ee43244440197685eb57ed`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:38:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:38:54 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:38:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 01:38:54 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 Nov 2025 01:38:54 GMT
ENV PYTHON_VERSION=3.11.14
# Tue, 04 Nov 2025 01:38:54 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Tue, 04 Nov 2025 01:50:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 01:50:25 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 01:50:25 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 02:35:20 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 02:35:20 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 02:35:20 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 02:35:20 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:51365f04b68881c6fd3d04aa38cdb689fdee6efba2aa6afcf2da5385022cf475`  
		Last Modified: Tue, 04 Nov 2025 00:13:42 GMT  
		Size: 30.1 MB (30142298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e8ea7735c83f82e69e5b70f8a34ee72969666d6434d9c442a8680e9a5aa0167`  
		Last Modified: Tue, 04 Nov 2025 01:50:40 GMT  
		Size: 1.3 MB (1273632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6303e21d64b9e80197b44e27731d6d0898a31e447dfd8910ae8e62d835ffc9e`  
		Last Modified: Tue, 04 Nov 2025 01:50:42 GMT  
		Size: 14.3 MB (14312609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c318c623f71690dfe89caa29d2f7ab5cc4adbc3a11b5e42c8eede49516ed721d`  
		Last Modified: Tue, 04 Nov 2025 01:50:39 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2654d5226d25f0f310798111cec8385bfc853316c96239615ee1adb58846776`  
		Last Modified: Tue, 04 Nov 2025 02:35:34 GMT  
		Size: 5.7 MB (5669159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:df3e5011a614a6f9fe197fbbf9a1cc8cfebd370ee7e43e4c4a83031491375b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a79167c89959650bc25c26d3956fb12298d77c3c4ed31abfaef60b41ae101a67`

```dockerfile
```

-	Layers:
	-	`sha256:bd36c027eb0ced244a1fc640772f5eb6553596d1c755e41f39c2d9e9c6511030`  
		Last Modified: Tue, 04 Nov 2025 12:18:39 GMT  
		Size: 2.2 MB (2200229 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d5aadc4728e135482a4ebf160d8231cd5baf1c611d83536b6d7a541c6a7ac21d`  
		Last Modified: Tue, 04 Nov 2025 12:18:39 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11` - linux; 386

```console
$ docker pull hylang@sha256:c011c6da4d779bbaa672f57c0c0d68ac48c98955b3431fcd1c1260e0f9881c0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52663258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88ada71f466b16beff1c14b2c31b9cd820d30c18326b81c7a484d2b0c67aec86`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 01:43:58 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 01:43:58 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 01:43:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 01:43:58 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 Nov 2025 01:43:58 GMT
ENV PYTHON_VERSION=3.11.14
# Tue, 04 Nov 2025 01:43:58 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Tue, 04 Nov 2025 01:54:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 01:54:18 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 01:54:18 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 02:30:16 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 02:30:16 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 02:30:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 02:30:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7f24a3a0c200106d0d9ab7b6264e50c689910154fb57bf08185b9eaf995db758`  
		Last Modified: Tue, 04 Nov 2025 00:13:54 GMT  
		Size: 31.3 MB (31294783 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b04cfc0247f345327b20e687d2997e42e1f2afcc6f579d5812d2910aed3319a`  
		Last Modified: Tue, 04 Nov 2025 01:54:33 GMT  
		Size: 1.3 MB (1297135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152469a864108a4c6296741c22545ef0d1f59ab7fb96f573940f48e614d3a69c`  
		Last Modified: Tue, 04 Nov 2025 01:54:34 GMT  
		Size: 14.4 MB (14402062 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:82f4da8c10162cbac2492021e78ded5febbf1bbc67cdd49efb6b8a8f271d967b`  
		Last Modified: Tue, 04 Nov 2025 01:54:32 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:158c6250a530a9fe0ed40d35da2ae9d2c8eb2b8c25d379faafcfcd0055026aea`  
		Last Modified: Tue, 04 Nov 2025 02:30:29 GMT  
		Size: 5.7 MB (5669030 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:3d227e25d75b7f19819412b4c9442781223fbd18dcf2140f626bec0b37715540
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206344 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e275a60ce21fd0642fa126f59091132687407f78928e6865f550692eb8e749cb`

```dockerfile
```

-	Layers:
	-	`sha256:b9e11db9fb239bbd54438c151ad3bab1aa2436cfa3a32a8fee67e82fdf9f4f05`  
		Last Modified: Tue, 04 Nov 2025 09:23:17 GMT  
		Size: 2.2 MB (2197076 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d9a73b8e93775ec6ffbdfb9438df018bf1ab2da02a72e5eef1ae4a7746e94b0`  
		Last Modified: Tue, 04 Nov 2025 09:23:18 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11` - linux; ppc64le

```console
$ docker pull hylang@sha256:6084727e3a2c42a7bdf1e21b33cfc10ebe2cb5ea29d082dc991001be4e7323eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.3 MB (55287069 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f7dec461175558b63c5f90c94d4bb32e7dfdc06ab6d6ba3be461254a85e8b9`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 10:33:31 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 10:33:31 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 10:33:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 10:33:31 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 Nov 2025 10:33:31 GMT
ENV PYTHON_VERSION=3.11.14
# Tue, 04 Nov 2025 10:33:31 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Tue, 04 Nov 2025 11:31:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 11:31:08 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 11:31:08 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 20:06:05 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 20:06:05 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 20:06:05 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 20:06:05 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:eead2c4a2afd8217def9d0ca536e7e4108ac8a91745ca25e76eb059260c04aab`  
		Last Modified: Tue, 04 Nov 2025 00:20:53 GMT  
		Size: 33.6 MB (33598647 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38798fa0998cac5d52717f1c476b8942b4e6351f3b73edb03379b155af9b0c53`  
		Last Modified: Tue, 04 Nov 2025 10:51:46 GMT  
		Size: 1.3 MB (1321333 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d71a5729cf9f5ab1561cb37b2b0e05f36363276ed73965cf2ac543c70cda97a6`  
		Last Modified: Tue, 04 Nov 2025 11:31:42 GMT  
		Size: 14.7 MB (14697272 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:526cdb65c84a52f01c1dfab8c0a811b4c840696c32324d67cd52dc8991407a1b`  
		Last Modified: Tue, 04 Nov 2025 11:31:41 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:daa9b68c68eb809b56a42643309fca9063b9747c9a70ab0ea083b1efcddd2618`  
		Last Modified: Tue, 04 Nov 2025 20:06:28 GMT  
		Size: 5.7 MB (5669568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:c2159eedf0bedde747a2346503ac5d4a117dd6bd65fd968f4be0fa76743ae729
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b7c0bce876cbcee82eaa08a4226722913407738e4ebe53fefe826d0578ae4cff`

```dockerfile
```

-	Layers:
	-	`sha256:8c9449a8e7552d2f9106be94aa4ca58efc6cf7c4c6f8bc86cc9b97efd129b77a`  
		Last Modified: Tue, 04 Nov 2025 21:18:34 GMT  
		Size: 2.2 MB (2203506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bae3e1f113b7098892e058b0ba59f0e13f6271b1976b2b3e2ce8e644f6c238a6`  
		Last Modified: Tue, 04 Nov 2025 21:18:35 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11` - linux; riscv64

```console
$ docker pull hylang@sha256:b0ccb53d9b10fa7296bac5e241ced41137462071cbf8276b77c6f17ea73e319e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49413589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4fec2ff33bb40688d4a59ccbc1660a2970665c1503eb40102da357ad738a8d7`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1762202650'
# Thu, 06 Nov 2025 22:15:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Nov 2025 22:15:20 GMT
ENV LANG=C.UTF-8
# Thu, 06 Nov 2025 22:15:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 06 Nov 2025 22:15:20 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 06 Nov 2025 22:15:20 GMT
ENV PYTHON_VERSION=3.11.14
# Thu, 06 Nov 2025 22:15:20 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Sat, 08 Nov 2025 13:22:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Sat, 08 Nov 2025 13:22:09 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 08 Nov 2025 13:22:09 GMT
CMD ["python3"]
# Sun, 09 Nov 2025 20:32:34 GMT
ENV HY_VERSION=1.1.0
# Sun, 09 Nov 2025 20:32:34 GMT
ENV HYRULE_VERSION=1.0.0
# Sun, 09 Nov 2025 20:32:34 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sun, 09 Nov 2025 20:32:34 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1fea97c4573443f662afd8f2cefe2b4ac31f6f24527d29e771c1cc07a012c924`  
		Last Modified: Tue, 04 Nov 2025 00:29:17 GMT  
		Size: 28.3 MB (28275786 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4321fa2fab4685cf3a08032cd46bc0aeb0781651614ec91351b4aab4487fc6ef`  
		Last Modified: Thu, 06 Nov 2025 23:56:47 GMT  
		Size: 1.3 MB (1260095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4b12053d0b9219b0de7f23df747d05cc662b3c51f8eadc8b8bb8aed8a17a22c`  
		Last Modified: Sat, 08 Nov 2025 13:23:27 GMT  
		Size: 14.2 MB (14206996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fd1edfb88a975f25bfea4cd2863c4be773b029f46f219bde402d9ad50b700d`  
		Last Modified: Sat, 08 Nov 2025 13:23:26 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3813be05592d3472e0e6bbe7399bf985614ae6fe57bc50e9f93b1babce37c0d0`  
		Last Modified: Sun, 09 Nov 2025 20:33:42 GMT  
		Size: 5.7 MB (5670463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:d43be8b23fa282d9180eceb16f3ad1774043551f819027a02192912b140077bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bb167a68083cf015ab095d04cf00a6cba935ed1bcd507512c83d4cb8694e716`

```dockerfile
```

-	Layers:
	-	`sha256:cd56df2e23ff1eff26d6ffc8203dcdbd5499da30ee2db018c23958754b191aa0`  
		Last Modified: Sun, 09 Nov 2025 21:18:00 GMT  
		Size: 2.2 MB (2193877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1026bf4df43deee4389af92e730858912b9f126624f4f6e086b5119e92bfa2e`  
		Last Modified: Sun, 09 Nov 2025 21:18:00 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.11` - linux; s390x

```console
$ docker pull hylang@sha256:820a0e8881f191b1592636492e5955d991d630953735b512b354126e5cefb073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51175769 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6d7ee9d61ccf1fecaaa7a3d249590d86a56a0416ae188b5456f72ab765b25de`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 03 Nov 2025 20:44:10 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1762202650'
# Tue, 04 Nov 2025 12:05:55 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Nov 2025 12:05:55 GMT
ENV LANG=C.UTF-8
# Tue, 04 Nov 2025 12:05:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 04 Nov 2025 12:05:55 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 04 Nov 2025 12:05:55 GMT
ENV PYTHON_VERSION=3.11.14
# Tue, 04 Nov 2025 12:05:55 GMT
ENV PYTHON_SHA256=8d3ed8ec5c88c1c95f5e558612a725450d2452813ddad5e58fdb1a53b1209b78
# Tue, 04 Nov 2025 12:29:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 04 Nov 2025 12:29:33 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 04 Nov 2025 12:29:33 GMT
CMD ["python3"]
# Tue, 04 Nov 2025 16:57:06 GMT
ENV HY_VERSION=1.1.0
# Tue, 04 Nov 2025 16:57:06 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 04 Nov 2025 16:57:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 04 Nov 2025 16:57:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ad0bc025a1766baba34dfa4dbb5713703de6595994d855ebf4689c0b161314ee`  
		Last Modified: Tue, 04 Nov 2025 00:20:17 GMT  
		Size: 29.8 MB (29837392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3625ac5bda657e609a86d5ae749bde4b1ce2e45b9d6e043c5149653e38c49f76`  
		Last Modified: Tue, 04 Nov 2025 12:18:36 GMT  
		Size: 1.3 MB (1305470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0de17ced6b1123e603653912f8891d91f6f652717843d3d56b7a3390f056cf08`  
		Last Modified: Tue, 04 Nov 2025 12:30:05 GMT  
		Size: 14.4 MB (14363426 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f190f4465a778f3e0e675a663ad215f64b15c036c48b7726cedd60f0d5a18963`  
		Last Modified: Tue, 04 Nov 2025 12:30:04 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077334b33dce96864cce23af948d83de235f9d092f7a6c433d1f65f95ae2ee16`  
		Last Modified: Tue, 04 Nov 2025 16:57:23 GMT  
		Size: 5.7 MB (5669233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:f78efd0b8ebad76ddb0a43116c2a8f76c756f71cba687c64393077108c381d81
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a7c13feb192b3dab971bc8beead5b1dc3d2420585c415e3f9db6592cfe0d0df`

```dockerfile
```

-	Layers:
	-	`sha256:7d570de91b5392eec9da4713ec48813c8a120f2c4071bd8520e1ab496de37784`  
		Last Modified: Tue, 04 Nov 2025 18:18:27 GMT  
		Size: 2.2 MB (2201354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:27903417b98368d030c24c7244404e1015c2d3c7cd672cae691cf0d0532ef61f`  
		Last Modified: Tue, 04 Nov 2025 18:18:28 GMT  
		Size: 9.3 KB (9320 bytes)  
		MIME: application/vnd.in-toto+json
