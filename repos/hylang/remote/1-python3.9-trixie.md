## `hylang:1-python3.9-trixie`

```console
$ docker pull hylang@sha256:babd69ce50f89016ec69f8e964bff85109d54083657ce16b7b29244f859895e3
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

### `hylang:1-python3.9-trixie` - linux; amd64

```console
$ docker pull hylang@sha256:3855b37d0751fc2b6e8b5a01b4e109d31220c2f7f91c0a8b42c07539aa08ec6c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48661349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:613f84cf140f13b732af57b4385aa999fe5f8ebc5fc1cdec5e34617fd6085419`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 09 Oct 2025 17:36:41 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 17:36:41 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_VERSION=3.9.24
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_SHA256=668391afabd5083faafa4543753d190f82f33ce6ba22d6e9ac728b43644b278a
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
CMD ["python3"]
# Tue, 28 Oct 2025 19:06:06 GMT
ENV HY_VERSION=1.1.0
# Tue, 28 Oct 2025 19:06:06 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 28 Oct 2025 19:06:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 28 Oct 2025 19:06:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57466e36deb99f355eab1131bc21d799709189ecdd7fb41cf4c17d5f53724e2`  
		Last Modified: Tue, 21 Oct 2025 02:16:18 GMT  
		Size: 1.3 MB (1292662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f010d693edcb2d965ff3c2a741fc92cded69746aa616f746e7813896fdd443b`  
		Last Modified: Tue, 21 Oct 2025 02:16:19 GMT  
		Size: 13.9 MB (13873867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21ed5e7e522581efdab14b4fde1d7d493901b4d25736b947520695c7911da66b`  
		Last Modified: Tue, 21 Oct 2025 02:16:18 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10b9f8c13b0e423e8a5845bc1f37654723120b8e46a33a63d6281ce2b31775b`  
		Last Modified: Tue, 28 Oct 2025 19:07:19 GMT  
		Size: 3.7 MB (3716646 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:77f1cb02d73302e28b9714164ac854c673c8f87596d32f3f0c8ba8818db4b3f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e490133caafdd95f7e8bfb831ae0018eb2c7287d69889883cd7273bf453bc046`

```dockerfile
```

-	Layers:
	-	`sha256:829b57fcd2f133ad122826a2a6cab4222e53473fa74688c9537dff8ce525224f`  
		Last Modified: Tue, 28 Oct 2025 20:26:49 GMT  
		Size: 2.2 MB (2199877 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b0286216deab82961715cd4b2e765aafae2214bf3b00ec45e9dfd4f76efc7e9`  
		Last Modified: Tue, 28 Oct 2025 20:26:50 GMT  
		Size: 9.3 KB (9296 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-trixie` - linux; arm variant v5

```console
$ docker pull hylang@sha256:aeabe21ec4f5c8f284910b2c1ce66b6e409b46ab7379cedd344f838f2977009d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46465386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7d6ff0ac99a8b6905c3e186217a69b1950ccc4607add5adde101972e38cae825`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 09 Oct 2025 17:36:41 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 17:36:41 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_VERSION=3.9.24
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_SHA256=668391afabd5083faafa4543753d190f82f33ce6ba22d6e9ac728b43644b278a
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
CMD ["python3"]
# Tue, 28 Oct 2025 19:07:57 GMT
ENV HY_VERSION=1.1.0
# Tue, 28 Oct 2025 19:07:57 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 28 Oct 2025 19:07:57 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 28 Oct 2025 19:07:57 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:389bac9f76fa529ccf801fd7c9cb260ecee27d208221c25004185ab22936c4d4`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 27.9 MB (27946283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8f3ceedc7433f2bf9e62cb28589541a4bfbd2c983d8b0cc25a1b59f3095af27`  
		Last Modified: Tue, 21 Oct 2025 03:17:54 GMT  
		Size: 1.3 MB (1275559 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3348dc90c9be93a05f63c6c30c874c3dbe351539f88e0e986d287a8b3531a8`  
		Last Modified: Tue, 21 Oct 2025 03:17:55 GMT  
		Size: 13.5 MB (13526527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4b69dd71adee27e13888d3407d5aad2f0c929c606f84ad8758512b84dfcc955`  
		Last Modified: Tue, 21 Oct 2025 03:17:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2054324c6de13ab3a7f7885968d756e1aa8322a68f79be3abb6af25ee20bdbc`  
		Last Modified: Tue, 28 Oct 2025 19:08:18 GMT  
		Size: 3.7 MB (3716768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:8cd916f33b86f87afeed8654217736ecd4754b2071d983c55782170189bc41c7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4318098d11e7239f6a407ba1b15aec696fe58fa713b5ff0b601fc19d093a6864`

```dockerfile
```

-	Layers:
	-	`sha256:e34de80b073e2a79284090c90bbbfe2683c3197a1848ae5843422f393a974ca5`  
		Last Modified: Tue, 28 Oct 2025 20:26:53 GMT  
		Size: 2.2 MB (2202878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:147e786c0a9425a45da66e4eb03fa75030e65d1a03d6e47c8447ee0c3383cf8d`  
		Last Modified: Tue, 28 Oct 2025 20:26:54 GMT  
		Size: 9.4 KB (9408 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-trixie` - linux; arm variant v7

```console
$ docker pull hylang@sha256:d8389e71cd3d3867dfd6f85ff3507458aa2512e9108f7eba83bce738839a8806
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.5 MB (44452524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c32191f079e7812fee81eb9dd0b99dc46467f8c70a9e14d2bd92e89d2e4270e`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 09 Oct 2025 17:36:41 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 17:36:41 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_VERSION=3.9.24
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_SHA256=668391afabd5083faafa4543753d190f82f33ce6ba22d6e9ac728b43644b278a
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
CMD ["python3"]
# Tue, 28 Oct 2025 19:08:15 GMT
ENV HY_VERSION=1.1.0
# Tue, 28 Oct 2025 19:08:15 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 28 Oct 2025 19:08:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 28 Oct 2025 19:08:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e700df98be6e78aab9ead4375242aa7e453705fe87e3341e08715efd74a134fd`  
		Last Modified: Tue, 21 Oct 2025 03:47:31 GMT  
		Size: 1.2 MB (1248124 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:928228e2f2fd2cd2711bc2d408fc5624551ddf1d938c1ed381765401cdf1ed5b`  
		Last Modified: Tue, 21 Oct 2025 03:52:53 GMT  
		Size: 13.3 MB (13274421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b02aea12edb684fa879896913fbcf01ab523585c71096bb4efd5d60861fd3d0`  
		Last Modified: Tue, 21 Oct 2025 03:52:52 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6235f9af6cd0e2141b45f67545728e21c508395a66857e8ede0cda6f21aec095`  
		Last Modified: Tue, 28 Oct 2025 19:08:28 GMT  
		Size: 3.7 MB (3716836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:15fa7005659fe3c7bc1be1626709a9b4f9d35fce907eb39cdf019f23ed8611d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14904ea69361c24fbd31e778cf9622d4a065e6d80c541b7225c48ff28071dd88`

```dockerfile
```

-	Layers:
	-	`sha256:f3da8e2f169ce81162625bf03a3522d3ec6fcd296e32f72b83b9deda9e3bb58a`  
		Last Modified: Tue, 28 Oct 2025 20:26:58 GMT  
		Size: 2.2 MB (2201331 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3b7d000c3aedba4f0bd7f2e0d86c756a010ad946b2ff8987460897a70193c8e7`  
		Last Modified: Tue, 28 Oct 2025 20:26:58 GMT  
		Size: 9.4 KB (9407 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-trixie` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:3e2dbc734b1bdf1727cc2d68eea1d55ed5692f26df2a7987144a2b3cd3e90292
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48951760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90cc65f72258d32929cf013f2395710e3d7015402dbf80c171258425bcf5f046`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 09 Oct 2025 17:36:41 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 17:36:41 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_VERSION=3.9.24
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_SHA256=668391afabd5083faafa4543753d190f82f33ce6ba22d6e9ac728b43644b278a
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
CMD ["python3"]
# Tue, 28 Oct 2025 19:07:46 GMT
ENV HY_VERSION=1.1.0
# Tue, 28 Oct 2025 19:07:46 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 28 Oct 2025 19:07:46 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 28 Oct 2025 19:07:46 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f0ad3620aa99591dc844594f5fe458a9d8ef84830017ce702a90e2b8546e10e`  
		Last Modified: Tue, 21 Oct 2025 02:22:55 GMT  
		Size: 1.3 MB (1273096 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb90d33c90e6245c66601264da8aae995538c5ef979af12cb0111cfb3b4ae37`  
		Last Modified: Tue, 21 Oct 2025 02:22:56 GMT  
		Size: 13.8 MB (13819613 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9f8bae26b9f2099a18e802900c9c0460a5a613858973cb2a7a975a88d30f97`  
		Last Modified: Tue, 21 Oct 2025 02:22:55 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cec629f64d9d5c7b2897990b5cc9e75d2633b5e3b78f31f70df87eec654e53d`  
		Last Modified: Tue, 28 Oct 2025 19:07:58 GMT  
		Size: 3.7 MB (3716674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:63e113b679e12b0c29436eb1b948c987f00c0bb5edc1fac530eeb2c887ddabbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e830166ef0a8a9e3c71bb0c1d586e8a5710d5bdc77af57142f0f13616c9596b`

```dockerfile
```

-	Layers:
	-	`sha256:8c4dd0edd243daee5da8f89301a322727f395c992712186db37b734daab01eb8`  
		Last Modified: Tue, 28 Oct 2025 20:27:02 GMT  
		Size: 2.2 MB (2200191 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3d0ae8a357ad537b92682ec7b318ebe9ff86ccc3548e2cae9f01666e9867d18`  
		Last Modified: Tue, 28 Oct 2025 20:27:03 GMT  
		Size: 9.4 KB (9448 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-trixie` - linux; 386

```console
$ docker pull hylang@sha256:5e2ebba6ada3d72a2eca4593eba50ac946a19e5d76f4e5058b5e4997f2937890
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50237072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce44667de08f00f862fa096d925e0f55eb261c556c2704891a95b64a2a19cb2c`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 09 Oct 2025 17:36:41 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 17:36:41 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_VERSION=3.9.24
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_SHA256=668391afabd5083faafa4543753d190f82f33ce6ba22d6e9ac728b43644b278a
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
CMD ["python3"]
# Tue, 28 Oct 2025 19:08:14 GMT
ENV HY_VERSION=1.1.0
# Tue, 28 Oct 2025 19:08:14 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 28 Oct 2025 19:08:14 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 28 Oct 2025 19:08:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a200ee423ccf07f171bf6258fbbc6605bc433e00c155b029f6be82d2ccacf21f`  
		Last Modified: Tue, 21 Oct 2025 02:15:32 GMT  
		Size: 1.3 MB (1296563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7d38fe8b41fc82e072417d9c21174474e3e2d19235c2ae646456c35d69363ac`  
		Last Modified: Tue, 21 Oct 2025 02:15:33 GMT  
		Size: 13.9 MB (13929034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90c4990b5cc4dfd4feacfebca90f9fa3c5d0632487de74ee3720316748b8139`  
		Last Modified: Tue, 21 Oct 2025 02:15:31 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cd83715c87da4e4f3101e2f60adad662ea8ce74356d9551f7045ba24bd93cf1`  
		Last Modified: Tue, 28 Oct 2025 19:08:25 GMT  
		Size: 3.7 MB (3716597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:c7ec7b488339f930c246a0c2cd410948064cf1716af1c1c2625b065051a7df51
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3758193ca284fd1166a18e8ca3d6c085ff7dce897fc7b55e2749e2f234d28b79`

```dockerfile
```

-	Layers:
	-	`sha256:89d316522aedb411c78cc05e5aaa6a219f5cb775d11c0d772bd922fb504072d7`  
		Last Modified: Tue, 28 Oct 2025 20:27:07 GMT  
		Size: 2.2 MB (2197038 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff032a28090c8f0f7ca902bac4784795808a1a3c9305597b495124d19b056681`  
		Last Modified: Tue, 28 Oct 2025 20:27:08 GMT  
		Size: 9.2 KB (9244 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-trixie` - linux; ppc64le

```console
$ docker pull hylang@sha256:987385746f6e995a6721b49046227f444dc7fc672447f1c2722cbebcebb1cea0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.8 MB (52838665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93139c05e585e71b8f70d6c267d4329b82a169f84db520a159b7f59bf66338f0`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 09 Oct 2025 17:36:41 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 17:36:41 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_VERSION=3.9.24
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_SHA256=668391afabd5083faafa4543753d190f82f33ce6ba22d6e9ac728b43644b278a
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
CMD ["python3"]
# Tue, 28 Oct 2025 19:37:55 GMT
ENV HY_VERSION=1.1.0
# Tue, 28 Oct 2025 19:37:55 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 28 Oct 2025 19:37:55 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 28 Oct 2025 19:37:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb558dffcc860262e2beb67e32665bd21619cba0fcdc6a241d92e98e82bc66c3`  
		Last Modified: Tue, 21 Oct 2025 12:43:45 GMT  
		Size: 1.3 MB (1320968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f6718de0c75c2c1d77a82013514c7e3be839c03d6cc63f94245d1a7cfe56c352`  
		Last Modified: Tue, 21 Oct 2025 14:12:22 GMT  
		Size: 14.2 MB (14201894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfeff2dbbcaf762d28c7258136b8063201a785f6ca3acf619973fc2bf9d84c8e`  
		Last Modified: Tue, 21 Oct 2025 14:12:21 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdec0cd0acab2b1074545059b544dfa85d4446731954ef222ece6d4fd255412d`  
		Last Modified: Tue, 28 Oct 2025 19:38:20 GMT  
		Size: 3.7 MB (3717037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:b6df4cdce0bcdd2b4b3025ec7e23f1320585e24e6d3209433f5d89313753c77f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212832 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62f4c8f26a1fbab54fecb7dec73f68e38e0a4e6059eed4251fafb5298726d29`

```dockerfile
```

-	Layers:
	-	`sha256:bcc78a1374a9b09e1c982d0ce3e45a956e0d8d3454f07d736744784f560fd31e`  
		Last Modified: Tue, 28 Oct 2025 20:27:12 GMT  
		Size: 2.2 MB (2203468 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bc5ec96bcd71a0e4dbff9ae6994cb9e0ab0bea820189c468cddbbfa72a03ad4e`  
		Last Modified: Tue, 28 Oct 2025 20:27:13 GMT  
		Size: 9.4 KB (9364 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-trixie` - linux; riscv64

```console
$ docker pull hylang@sha256:e68b8694f7cad0a3ef5964efdbf00c84ddc51bc69c9c1a11d7d19b47e5f5c1eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47032655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff6c36395d09cf3662b0dc5c23bf365856c3738d30c6c2b404a2ebec4474a9f8`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 08 Oct 2025 19:19:01 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 08 Oct 2025 19:19:01 GMT
ENV LANG=C.UTF-8
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_VERSION=3.9.24
# Wed, 08 Oct 2025 19:19:01 GMT
ENV PYTHON_SHA256=668391afabd5083faafa4543753d190f82f33ce6ba22d6e9ac728b43644b278a
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["python3"]
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HY_VERSION=1.1.0
# Wed, 08 Oct 2025 19:19:01 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 08 Oct 2025 19:19:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Oct 2025 19:19:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:557a3f1451d93ce350365e520b97eb9b8a07657581de0c11399fbe6f5092d90b`  
		Last Modified: Thu, 23 Oct 2025 11:04:25 GMT  
		Size: 1.3 MB (1260102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87f06ce9695e4be7bf0426bdb4090b77f655bf8ffe9100002673d9c6d67a4e9b`  
		Last Modified: Thu, 23 Oct 2025 15:04:44 GMT  
		Size: 13.8 MB (13779208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72357e4ca1fd363a888a2bf92b245fac5651c93775f0e056b2a8bd5551c4bad1`  
		Last Modified: Thu, 23 Oct 2025 15:04:43 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95cf0e10572fe2c6c09a4eaa68767dad1012d8bcccfb79853afdb0bfd721be21`  
		Last Modified: Sat, 25 Oct 2025 01:40:18 GMT  
		Size: 3.7 MB (3717445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:fcb0ae671b4590ad95d1757f1ca3931c1860eb8895fe5e213113041f3270ba0c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203138 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c3b381948f60fb645de73bc06d3ef27de54ed3e8fc472b314ed53d9de38084a`

```dockerfile
```

-	Layers:
	-	`sha256:6e00d2054fc8dd42b412ddea64749de3281846a2080e15ebf9f075f4368c1363`  
		Last Modified: Sat, 25 Oct 2025 02:20:27 GMT  
		Size: 2.2 MB (2193839 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce7bcfa72fdc89aad84b39b8a99dd02a782d3fd0406633769651274c7733eaac`  
		Last Modified: Sat, 25 Oct 2025 02:20:28 GMT  
		Size: 9.3 KB (9299 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9-trixie` - linux; s390x

```console
$ docker pull hylang@sha256:daec3f820e61ec033c5ae34e328e0df1e8420fc658e8785d2880590adb87d3c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48687335 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a07da0565d4ae1de23a28964387fecc0438f3a0882c57cea4503bfd9f7c57a86`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 09 Oct 2025 17:36:41 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 17:36:41 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_VERSION=3.9.24
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_SHA256=668391afabd5083faafa4543753d190f82f33ce6ba22d6e9ac728b43644b278a
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
CMD ["python3"]
# Tue, 28 Oct 2025 19:28:38 GMT
ENV HY_VERSION=1.1.0
# Tue, 28 Oct 2025 19:28:38 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 28 Oct 2025 19:28:38 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 28 Oct 2025 19:28:38 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e414015a43e56e4b06133185cabf480df8d52b2f49fb047b4d68df5892c90435`  
		Last Modified: Tue, 21 Oct 2025 19:46:14 GMT  
		Size: 1.3 MB (1305251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a6640726562c5962a66640965d126e1180057acb069ac98479ed5bc0d4581a`  
		Last Modified: Tue, 21 Oct 2025 20:54:51 GMT  
		Size: 13.8 MB (13827623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af570fae2827e692f2a4a92da7b2953bd9c50c94061bc20616bbe0c2282e25f4`  
		Last Modified: Tue, 21 Oct 2025 20:54:49 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d16bdb23a5620578a1c8a7f0f6cbe804adde204a2be0103de81fb3ef3c91b9b`  
		Last Modified: Tue, 28 Oct 2025 19:29:02 GMT  
		Size: 3.7 MB (3716958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:5a11eed5ef781ba7e625c5f40994f7aca5cc144fb528e05e3c553ae1e9020acd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6750ef0c7ef2373e0363202e9cf49d2093a65dddb36abef7795f51de5c6a9615`

```dockerfile
```

-	Layers:
	-	`sha256:e26b71a8b3c143e273f09fdbdb5b5f9fa631e12f5bbb7dedf99ba7f632adda13`  
		Last Modified: Tue, 28 Oct 2025 20:27:22 GMT  
		Size: 2.2 MB (2201316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1e82a45c67df69d7d400341b5915043b1583d0062da7396067c9c710aa58de4`  
		Last Modified: Tue, 28 Oct 2025 20:27:23 GMT  
		Size: 9.3 KB (9296 bytes)  
		MIME: application/vnd.in-toto+json
