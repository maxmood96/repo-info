## `hylang:1-python3.10-trixie`

```console
$ docker pull hylang@sha256:ba2838cb44053eb52e2377a984874166dc485fff45786a6e05e13f592cb96d03
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

### `hylang:1-python3.10-trixie` - linux; amd64

```console
$ docker pull hylang@sha256:78e5e5dc33929d55dfbff3e29f2dc78e2c9959c0c6efe1bebd1a3daed50f3955
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50059767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c8cd8eeda442e463e8d6b9cb4643225d0dbdc72e1fbac10d663a7939a2c83ab`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:05:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:05:33 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 02:05:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 24 Jun 2026 02:05:33 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 24 Jun 2026 02:05:33 GMT
ENV PYTHON_VERSION=3.10.20
# Wed, 24 Jun 2026 02:05:33 GMT
ENV PYTHON_SHA256=de6517421601e39a9a3bc3e1bc4c7b2f239297423ee05e282598c83ec0647505
# Wed, 24 Jun 2026 02:11:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 24 Jun 2026 02:11:28 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 24 Jun 2026 02:11:28 GMT
CMD ["python3"]
# Wed, 24 Jun 2026 02:46:34 GMT
ENV HY_VERSION=1.3.0
# Wed, 24 Jun 2026 02:46:34 GMT
ENV HYRULE_VERSION=1.1.0
# Wed, 24 Jun 2026 02:46:34 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 24 Jun 2026 02:46:34 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b2876568ccf8422a3a4400c36c805333feb503711c9d44873a61295fb73ccfd`  
		Last Modified: Wed, 24 Jun 2026 02:11:36 GMT  
		Size: 1.3 MB (1293293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e737dfad7625197cfb527045758452e364ec3da603df19d7781c8485d5d42f57`  
		Last Modified: Wed, 24 Jun 2026 02:11:37 GMT  
		Size: 13.8 MB (13823289 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45f9eb24ea676873533ee6f99f71066fd68d1719b427dca574341176c46c3fe9`  
		Last Modified: Wed, 24 Jun 2026 02:11:36 GMT  
		Size: 254.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b489730e238cfd0934b58c7fd7636abbcccbc8f1850d38ff8d2588dda5638b`  
		Last Modified: Wed, 24 Jun 2026 02:46:42 GMT  
		Size: 5.2 MB (5157512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:f1c41de8224e7ad0696e35c93151b09835fe68d3353bfa52d94ab603fdd84752
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209407 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1a7d6744457154fefca1191066554cce9e1ffa1dd7d6dee5f2f16d60c638dc2`

```dockerfile
```

-	Layers:
	-	`sha256:f7acfea8942eeed19fc6df2b7ecba85b14ab4315eaff0a484f5f6d41a9fa3244`  
		Last Modified: Wed, 24 Jun 2026 02:46:41 GMT  
		Size: 2.2 MB (2200089 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d232a68501ef976463aaaedd78ce9e773e063862690c167b13f3d6a26575603a`  
		Last Modified: Wed, 24 Jun 2026 02:46:41 GMT  
		Size: 9.3 KB (9318 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; arm variant v5

```console
$ docker pull hylang@sha256:939c2fbc42ec4a14f040a1d3c469e34d0690edeed1b46f153f454a05735bf9fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47878693 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f5aa1e19f1154fca196a1655d43c11bf715df441b7f335f778525690d3d99df`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:56:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:56:19 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:56:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 01:56:19 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 11 Jun 2026 01:56:19 GMT
ENV PYTHON_VERSION=3.10.20
# Thu, 11 Jun 2026 01:56:19 GMT
ENV PYTHON_SHA256=de6517421601e39a9a3bc3e1bc4c7b2f239297423ee05e282598c83ec0647505
# Thu, 11 Jun 2026 02:07:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 02:07:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 02:07:47 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 03:06:44 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 03:06:44 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 03:06:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 03:06:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ed883f3fd95b7edef302d7ca9520eefdae280af081509bd7e9e5b5ff8f4cda7c`  
		Last Modified: Wed, 10 Jun 2026 23:41:17 GMT  
		Size: 28.0 MB (27959200 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1682b4eeca2e8594503e3b4d6af46ee93f4e7f233ef04bc1154b86f7a0e1df4d`  
		Last Modified: Thu, 11 Jun 2026 02:07:55 GMT  
		Size: 1.3 MB (1276350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5df5cdc75dcdc34f941538362509fe02ec7e0542d1db02a43de486b83cff7c5d`  
		Last Modified: Thu, 11 Jun 2026 02:07:55 GMT  
		Size: 13.5 MB (13485201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf79b7d0953f8faecc2090a5d518290061e0e03900d3046358fee4551f1e2046`  
		Last Modified: Thu, 11 Jun 2026 02:07:55 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:831ff256f84d68f82aefd75147c123b0f690d54b4e89008ce6f89c5981e736c0`  
		Last Modified: Thu, 11 Jun 2026 03:06:52 GMT  
		Size: 5.2 MB (5157693 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:2c6ac67f11e2ac2790ea69f1f0b3c3118dbfcb7cd3253d8a5fdcc525d618a779
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b29cd081fe66d19f1892b277e55cdc352a6d1eb12506666a9e4ae58516c7d437`

```dockerfile
```

-	Layers:
	-	`sha256:f106f8523a23b123883cd1624e0ccd8ca034b70f06730b4a66361e6318dc476d`  
		Last Modified: Thu, 11 Jun 2026 03:06:51 GMT  
		Size: 2.2 MB (2203090 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8919e61e7a5da081411b1c334a2d86cf8d1da96bf4d53ac6c2c8348ac4c23af`  
		Last Modified: Thu, 11 Jun 2026 03:06:51 GMT  
		Size: 9.4 KB (9431 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; arm variant v7

```console
$ docker pull hylang@sha256:5a0795fa32688e10884ce8bb44c52b038533f002588d8a55f20ed68b59f4d5c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45836793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:276f81dffe4fcae03f8f8867bf4d91f6cded9c1d9f7cbc6d94895d9a2103d32a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:25:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 02:25:52 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 02:25:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:25:52 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 11 Jun 2026 02:25:52 GMT
ENV PYTHON_VERSION=3.10.20
# Thu, 11 Jun 2026 02:25:52 GMT
ENV PYTHON_SHA256=de6517421601e39a9a3bc3e1bc4c7b2f239297423ee05e282598c83ec0647505
# Thu, 11 Jun 2026 02:36:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 02:36:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 02:36:47 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 03:25:27 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 03:25:27 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 03:25:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 03:25:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4bd6ddea06d5009ee47ddb0f254a2569aff0230c005869ebd416b20295d945c0`  
		Last Modified: Wed, 10 Jun 2026 23:42:34 GMT  
		Size: 26.2 MB (26211004 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:480a67d08ac05b3f950a211e33ef394e3753475bd9fddcc21136236f9ebbcb4f`  
		Last Modified: Thu, 11 Jun 2026 02:36:55 GMT  
		Size: 1.2 MB (1249154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70847990a3ae2fef37abd669be7ee8b9759109a911ed057743ee8ee80de15d6f`  
		Last Modified: Thu, 11 Jun 2026 02:36:55 GMT  
		Size: 13.2 MB (13218562 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf06f435e9fe7ee30d05b4fb6390cdf498b65141254048edb9242fc551fbb63`  
		Last Modified: Thu, 11 Jun 2026 02:36:55 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bba0c14308387a7a3e1fbfe91838d31b582176365525c9ebae92c2d94be994f`  
		Last Modified: Thu, 11 Jun 2026 03:25:34 GMT  
		Size: 5.2 MB (5157823 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:8a533312c6c554b0e39b65d01314d0e647080e8280ed2ae6eb4e04f9ac83d090
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210974 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a57cca5d5cfac3d021034abecc9796902b6a2b9f2903a0db5a0af1bc4bfd09a2`

```dockerfile
```

-	Layers:
	-	`sha256:23c2af147406ba578debe2cee9461e52b955897ac0b391a976d93ed21f2b7b54`  
		Last Modified: Thu, 11 Jun 2026 03:25:34 GMT  
		Size: 2.2 MB (2201543 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3747a20f8dda38a30597f653e6c815d71356e7d5d7a87e039a0382c85a1ea78`  
		Last Modified: Thu, 11 Jun 2026 03:25:34 GMT  
		Size: 9.4 KB (9431 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:2ad411343fe178f699a7f6df6e69ac4744bc0bcc65e1ad9fe98a0d380351fdfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50359427 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03438cfabd2946d4991cb4331018ea28ba5081c60db0cbd98b8645a0fe863cb4`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:09:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:09:12 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:09:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 01:09:12 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 11 Jun 2026 01:09:12 GMT
ENV PYTHON_VERSION=3.10.20
# Thu, 11 Jun 2026 01:09:12 GMT
ENV PYTHON_SHA256=de6517421601e39a9a3bc3e1bc4c7b2f239297423ee05e282598c83ec0647505
# Thu, 11 Jun 2026 01:16:39 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 01:16:39 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 01:16:39 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 02:41:18 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 02:41:18 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 02:41:18 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 02:41:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a25cd16f2d8653f652f8292b34b21bfbabdc85d6b39861a24b85f0896df1a95e`  
		Last Modified: Wed, 10 Jun 2026 23:40:16 GMT  
		Size: 30.1 MB (30148530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5d23c1093aa8e8651a8b6da1ec1fff64daad8f1a39083cb538d194289b4895`  
		Last Modified: Thu, 11 Jun 2026 01:16:48 GMT  
		Size: 1.3 MB (1274132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e297ec80d442b388aab929f86a84c0ed01cd9823b432c7c27b384dc733ce98b7`  
		Last Modified: Thu, 11 Jun 2026 01:16:48 GMT  
		Size: 13.8 MB (13778963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ac3bc18c64d7033d45a89e441cfd1056265e45c50a0a50596b292988a4ef8e0`  
		Last Modified: Thu, 11 Jun 2026 01:16:48 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:485383c60595c574c652173a55a718da5c8ebe9e7b047b364a996c657c800ed8`  
		Last Modified: Thu, 11 Jun 2026 02:41:25 GMT  
		Size: 5.2 MB (5157553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:4f3f61aa41226c917c373b335bd2b7f21f8345264850cb1c0f0f4db3f06c3183
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb88e079987443e6cb447fcba03a89554f20bf33ee78841e72b7ad948163d04c`

```dockerfile
```

-	Layers:
	-	`sha256:c0bb1f7fbca694e3469d4fa6c8b892027cade57b9c70d1623e1ac90ec33f145c`  
		Last Modified: Thu, 11 Jun 2026 02:41:25 GMT  
		Size: 2.2 MB (2200395 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3c33503083f9cd0324f2bf87e04206445adc8f186670def699c442d5b1daa9e6`  
		Last Modified: Thu, 11 Jun 2026 02:41:25 GMT  
		Size: 9.5 KB (9471 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; 386

```console
$ docker pull hylang@sha256:c9f01e4b9a3351849eb2c041c41f811f0713a892c3406bb142beac3db839b31c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51610517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc4eb9322378ab58b88f010c3c4dac5d12471d48954f379af1ba1d65a08f121`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:09:03 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:09:03 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:09:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 01:09:03 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 11 Jun 2026 01:09:03 GMT
ENV PYTHON_VERSION=3.10.20
# Thu, 11 Jun 2026 01:09:03 GMT
ENV PYTHON_SHA256=de6517421601e39a9a3bc3e1bc4c7b2f239297423ee05e282598c83ec0647505
# Thu, 11 Jun 2026 01:29:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 01:29:25 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 01:29:25 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 02:39:46 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 02:39:46 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 02:39:46 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 02:39:46 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14101529825cd4826a88bba578523d91585282fd162b432c64a993c619d0e241`  
		Last Modified: Thu, 11 Jun 2026 01:29:31 GMT  
		Size: 1.3 MB (1297747 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6334c511a6624672255f4f9716e1011151e55c91bcb47383d62025f82a17a11`  
		Last Modified: Thu, 11 Jun 2026 01:29:32 GMT  
		Size: 13.9 MB (13853726 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7fc6db23e4bfc0c16c8215ba552bd9895956cbfb3ae06e3660d92832fd4e34`  
		Last Modified: Thu, 11 Jun 2026 01:29:31 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b91f4a9af80a5eee21608173a9c2042294e3dbe0475969e57755e4dd606dc2d`  
		Last Modified: Thu, 11 Jun 2026 02:39:53 GMT  
		Size: 5.2 MB (5157601 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:d9b33ffe9969b6fc3a1ab87be1cb51d48c7347c4e8d5d71e701a3f8104d57190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a798e17203d9ee2546f6903585c2251e63004cd944d6814415490b57cc2d9259`

```dockerfile
```

-	Layers:
	-	`sha256:a7e5a04977eb85c9df9c5f7b88b9affe0bd639beb49a964bb3a19a12ae60112c`  
		Last Modified: Thu, 11 Jun 2026 02:39:52 GMT  
		Size: 2.2 MB (2197250 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:37db322810b518fada439e364b19e4176456fb6b13b9be15a45e7d06a0131dc8`  
		Last Modified: Thu, 11 Jun 2026 02:39:52 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; ppc64le

```console
$ docker pull hylang@sha256:71362510acfee51a4ae73e234fcf16c58ef9cc18613d4eb10b16ab705232c1ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54238975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd3c95c1c8ad7ce61c3df19076dc70efffbf0e82db145cca2244c7a71c501936`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 07:45:04 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 07:45:04 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 07:45:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 07:45:04 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 11 Jun 2026 07:45:04 GMT
ENV PYTHON_VERSION=3.10.20
# Thu, 11 Jun 2026 07:45:04 GMT
ENV PYTHON_SHA256=de6517421601e39a9a3bc3e1bc4c7b2f239297423ee05e282598c83ec0647505
# Thu, 11 Jun 2026 08:51:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 08:51:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 08:51:29 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 12:35:57 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 12:35:57 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 12:35:57 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 12:35:57 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9d6b2e320e2b74843186d830e8202c50ebfaeccf823d239e3e3e349a8a508d80`  
		Last Modified: Thu, 11 Jun 2026 00:24:42 GMT  
		Size: 33.6 MB (33606340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c57fbe4f0b9ceabf43c157fcab90b068b7953cc59c03767db856195a2a61e8a9`  
		Last Modified: Thu, 11 Jun 2026 08:04:12 GMT  
		Size: 1.3 MB (1321251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee82bf02720ac77d0ac70bebd4f03f9f5b1bbcf94321a87db1706245a571308e`  
		Last Modified: Thu, 11 Jun 2026 08:51:45 GMT  
		Size: 14.2 MB (14153355 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e2e4442465262a81d28a351e6920fc3c5ea3ec36ecaba6a466cc37be513d2c`  
		Last Modified: Thu, 11 Jun 2026 08:51:44 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea6091976ec7d029131a3df430b8f0b1ab8572929300677e78736d2859ae611d`  
		Last Modified: Thu, 11 Jun 2026 12:36:10 GMT  
		Size: 5.2 MB (5157780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:4ce3af418bc23376a7e97f25f66d07a2cdb0cbe12f9bd0f0d10748545913c5be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2213068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581bc3c8108d5c4a4400c6291bd6963bf3eea323daa8091f916301078309c48f`

```dockerfile
```

-	Layers:
	-	`sha256:8552b462c100766b6f3f1db0cfe162df696b815b30fcd09a634b510f8ebad741`  
		Last Modified: Thu, 11 Jun 2026 12:36:10 GMT  
		Size: 2.2 MB (2203680 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec7addcece3dedf69b8f9ccc84a9548c7834881329b51e660b1ef6912b53c5ee`  
		Last Modified: Thu, 11 Jun 2026 12:36:09 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; riscv64

```console
$ docker pull hylang@sha256:423b246675b6afa45169c9d94e83893ca09f508eeba79492e550dd4540c1a462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48434036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bd30773fabc445c0d0402594ac22336c32b7eaa309254e7ba8687137e2d8e57`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1781049600'
# Sat, 13 Jun 2026 22:31:32 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 13 Jun 2026 22:31:32 GMT
ENV LANG=C.UTF-8
# Sat, 13 Jun 2026 22:31:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Sat, 13 Jun 2026 22:31:32 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Sat, 13 Jun 2026 22:31:32 GMT
ENV PYTHON_VERSION=3.10.20
# Sat, 13 Jun 2026 22:31:32 GMT
ENV PYTHON_SHA256=de6517421601e39a9a3bc3e1bc4c7b2f239297423ee05e282598c83ec0647505
# Sun, 14 Jun 2026 02:54:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Sun, 14 Jun 2026 02:54:22 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sun, 14 Jun 2026 02:54:22 GMT
CMD ["python3"]
# Mon, 15 Jun 2026 00:41:13 GMT
ENV HY_VERSION=1.3.0
# Mon, 15 Jun 2026 00:41:13 GMT
ENV HYRULE_VERSION=1.1.0
# Mon, 15 Jun 2026 00:41:13 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 15 Jun 2026 00:41:13 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0b510fe8545cab831b696965b5a825649c5c945581e912d31a08a0b30ff940c0`  
		Last Modified: Thu, 11 Jun 2026 03:01:06 GMT  
		Size: 28.3 MB (28282305 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd33606605beabefc562f6d07f775cdf9a828dd917655a01183b9fe511e508b3`  
		Last Modified: Sun, 14 Jun 2026 00:14:21 GMT  
		Size: 1.3 MB (1261210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63bdc1bce655309196364b04b0a023e18c61abb1b9111de565d87a1f32c70531`  
		Last Modified: Sun, 14 Jun 2026 02:55:33 GMT  
		Size: 13.7 MB (13731569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f004eaba5412c6be9ff0f396cbf57aabaf8feeccbd81d43c7b0c5cbf7a662f1`  
		Last Modified: Sun, 14 Jun 2026 02:55:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23734aff399bf0de9f06cb262a2e11ea14c0f4e3cb927a9cad13363c31f97c58`  
		Last Modified: Mon, 15 Jun 2026 00:42:17 GMT  
		Size: 5.2 MB (5158701 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:3fb7d76dc6d1e6ff37fd6e5fc539625a23c6579652f6506832034d600ffc2343
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203439 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06e38982b10b6bb1d64ab79b1da1210de779e87ce12e6e9ee6fbdb17ba46699e`

```dockerfile
```

-	Layers:
	-	`sha256:7b700f98f475bb71b7904db6e7bc5aae521a388e5b095721781baaa5cb76c771`  
		Last Modified: Mon, 15 Jun 2026 00:42:16 GMT  
		Size: 2.2 MB (2194051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:319c91a9bf619718dfd5801ddec31beaba258032629d676710335ed5dc01a820`  
		Last Modified: Mon, 15 Jun 2026 00:42:16 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.10-trixie` - linux; s390x

```console
$ docker pull hylang@sha256:91ac7ea0a276bca8f0a3b8488b26601b2cc49138a8072b92697b33219eb2fda1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50081273 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:092f0bf729973d73ba17491bd3048a0a1e21ffad05030ee392ba77f6b1faea74`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 02:35:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 02:35:51 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 02:35:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 11 Jun 2026 02:35:51 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 11 Jun 2026 02:35:51 GMT
ENV PYTHON_VERSION=3.10.20
# Thu, 11 Jun 2026 02:35:51 GMT
ENV PYTHON_SHA256=de6517421601e39a9a3bc3e1bc4c7b2f239297423ee05e282598c83ec0647505
# Thu, 11 Jun 2026 03:00:40 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 11 Jun 2026 03:00:40 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 11 Jun 2026 03:00:40 GMT
CMD ["python3"]
# Thu, 11 Jun 2026 04:04:18 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 04:04:18 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 04:04:18 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 04:04:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:760dcf74fdfe93300ce15b5b23adf9aa4af45b6ba9d69925863198f64881a537`  
		Last Modified: Wed, 10 Jun 2026 23:42:35 GMT  
		Size: 29.9 MB (29851354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:22e6ebe81c809d11446cb9d8ee1dc54cfcefcebce9a4bfd457553a7118acf502`  
		Last Modified: Thu, 11 Jun 2026 02:51:02 GMT  
		Size: 1.3 MB (1305780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdd215aaa5e5b9972fd4eb3e28c7def2390929d911f98f253245dcfbd13bfd4e`  
		Last Modified: Thu, 11 Jun 2026 03:00:54 GMT  
		Size: 13.8 MB (13766281 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:81e9b7288c675d2d974a780b985ca296c40465d407c95b79cd328419bfc88d4b`  
		Last Modified: Thu, 11 Jun 2026 03:00:53 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8e706f78740331c1faa039c7185cc6208c5fd582efb8dbb63af1fae6f37bda41`  
		Last Modified: Thu, 11 Jun 2026 04:04:29 GMT  
		Size: 5.2 MB (5157610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.10-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:0f627640ae3071951e8a15f74f6f3f25dd885b12c99c21b93def083616ff14db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210846 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3799b57c02843d81b6f28b1b973ed2b7ac661a9beac688c3636434c520221daa`

```dockerfile
```

-	Layers:
	-	`sha256:d97b51271e06fbe6652942aaaa918bccb7cbcbf9fa5ba4e73dc773f6d5234490`  
		Last Modified: Thu, 11 Jun 2026 04:04:29 GMT  
		Size: 2.2 MB (2201528 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e20b39f5febb9e2f05bc4809c4b5f021a83e46a7f33f0f55f1d7f9c0e2dc3ee`  
		Last Modified: Thu, 11 Jun 2026 04:04:29 GMT  
		Size: 9.3 KB (9318 bytes)  
		MIME: application/vnd.in-toto+json
