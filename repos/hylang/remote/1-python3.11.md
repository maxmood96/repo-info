## `hylang:1-python3.11`

```console
$ docker pull hylang@sha256:431c4b51e013935d5706761413757938650a24e2ce65530ed7a1046ecddcc2f3
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

### `hylang:1-python3.11` - linux; amd64

```console
$ docker pull hylang@sha256:bf21a203c2cecf5788eac60a2f21d4c7fea977e429595550b733748710737a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52388736 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c583e6eb59f05ec8cf94ee9d8f1d4dda761fced9f175ff86b259bc964d304b8c`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:43:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:43:52 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:43:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:43:52 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 19 May 2026 23:43:52 GMT
ENV PYTHON_VERSION=3.11.15
# Tue, 19 May 2026 23:43:52 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Tue, 19 May 2026 23:52:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 19 May 2026 23:52:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 May 2026 23:52:06 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:12:00 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:12:00 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:12:00 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:12:00 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8649771fee179d7c2590c94f533aaa5fceb70e36e25dec83672fe836d99577c5`  
		Last Modified: Tue, 19 May 2026 23:52:15 GMT  
		Size: 1.3 MB (1293313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:797d495f2c68eb4664df918d39078ca04612d7ef47c57b5c784f7f6eedd42bf5`  
		Last Modified: Tue, 19 May 2026 23:52:15 GMT  
		Size: 14.4 MB (14366167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45006ceeeea9e2ca59a046b6f4ac9a212e4b27b3d8d6e7d348b03f0aaccdac99`  
		Last Modified: Tue, 19 May 2026 23:52:15 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a736a57c28969e112b6afa2898d04632c3b2ce2fca1919fb25e1812453cbdb29`  
		Last Modified: Wed, 27 May 2026 00:12:07 GMT  
		Size: 6.9 MB (6949080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:f1360b000ec03cdfa055254ccfcad0fbf4898eb01484e6df2783ebb1e9f67dec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d74f825211556d5a28a5cdfe9070fb8e2a58bba250a2d8b8f955b363be96a7f`

```dockerfile
```

-	Layers:
	-	`sha256:89e8c5fd4c3a13692cf00dd21ea6d3ea85fc51f9a7a3db91f2f0036786dd813c`  
		Last Modified: Wed, 27 May 2026 00:12:06 GMT  
		Size: 2.2 MB (2200049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:814789e682fffc30818adf83f689afdafad367ce2b488d2fb5f7262bd74b819e`  
		Last Modified: Wed, 27 May 2026 00:12:06 GMT  
		Size: 9.3 KB (9319 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11` - linux; arm variant v5

```console
$ docker pull hylang@sha256:c3070f5d9e2fd4c5c2edd65e5b4f32194e6049023e410f5a437f6a0307fdc0e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50176896 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d3132a6e4629e44c8365e7e9ed0415c58d66b8cdac907708804a8b935e700e1`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:21:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:21:24 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:21:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:21:24 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 20 May 2026 00:21:24 GMT
ENV PYTHON_VERSION=3.11.15
# Wed, 20 May 2026 00:21:24 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Wed, 20 May 2026 00:39:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 20 May 2026 00:39:22 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 00:39:22 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:10:45 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:10:45 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:10:45 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:10:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e606d3de4e92aecceae5647b2613468593ba0ba8a73f5d3188b17a62b929ebd`  
		Last Modified: Wed, 20 May 2026 00:39:30 GMT  
		Size: 1.3 MB (1276401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6563d25717f311e73dcb89cdacb82130f80b734028acd364f36118a1ca909615`  
		Last Modified: Wed, 20 May 2026 00:39:30 GMT  
		Size: 14.0 MB (13997317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d856016b82520a3313371f4ddf7c558b626a8b8967de8756a00063c4e0bf4a29`  
		Last Modified: Wed, 20 May 2026 00:39:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c604354a17d377e71ab2e3c5f639381cd4338636596a4792e7321077e29c37cc`  
		Last Modified: Wed, 27 May 2026 00:10:53 GMT  
		Size: 6.9 MB (6949060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:71ad40c80cde45564c7aa386559b126ca0ebd393e40370257f156ed2dce08b0f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0f494b6a334da1e2bed2c64d427b65adf5d052c68fc88164057bee6da343e62`

```dockerfile
```

-	Layers:
	-	`sha256:bc173816d7891fecdc059d970d7a25838c5722b6a6fce4d1a7451ed474c0afe6`  
		Last Modified: Wed, 27 May 2026 00:10:53 GMT  
		Size: 2.2 MB (2203050 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b22928624e23e3dd3bc55c37316168e74f6c633fa92dfc4670804b6540f8e94`  
		Last Modified: Wed, 27 May 2026 00:10:52 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11` - linux; arm variant v7

```console
$ docker pull hylang@sha256:a100d05457e11743a89bd51f80e4e7a3f5d706fa98ddc7ec6e28be2858f3214b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48135848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:554646b06c04e61037911e13f9cced07d8d035f5d9713d65d80db857b410a211`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:52:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:52:20 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 00:52:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:52:20 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 20 May 2026 00:52:20 GMT
ENV PYTHON_VERSION=3.11.15
# Wed, 20 May 2026 00:52:20 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Wed, 20 May 2026 01:08:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 20 May 2026 01:08:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 01:08:43 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:12:01 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:12:01 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:12:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:12:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ab322a334f34a3ecd03ce661db6651c57707541fb3b28b8db603d8f0733d3c73`  
		Last Modified: Wed, 20 May 2026 01:08:50 GMT  
		Size: 1.2 MB (1249168 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:877cdaa88e5d4a0a9ed1259c5927407d6caa1965f2fcffc141747a4ec4d023d8`  
		Last Modified: Wed, 20 May 2026 01:08:50 GMT  
		Size: 13.7 MB (13731567 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcbbd698e8de650bb8aa750832750baa544bfac8365c22aac09c38126d6f2c13`  
		Last Modified: Wed, 20 May 2026 01:08:50 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afc27744eb9bb766f5df85cfd5497fc21d2824937fff5eecf1c26d77d42f7952`  
		Last Modified: Wed, 27 May 2026 00:12:08 GMT  
		Size: 6.9 MB (6949032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:6aa7b01304173a74abbddd15d1109f32c5f6e7e1dfb0a1b871c2806e016ecdfe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92c07b6a97506ecda79afafb8f3c3b9d5dd008126cb519c12836c5cb533f2756`

```dockerfile
```

-	Layers:
	-	`sha256:2ac67f63d9908aab2fb905275eb7fc32ec706000bcaafa6511339f9924b065df`  
		Last Modified: Wed, 27 May 2026 00:12:08 GMT  
		Size: 2.2 MB (2201503 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b396d1b4cea2c693191d6b7360e950d7ec91baa3b2abf2ee25ce178418cece31`  
		Last Modified: Wed, 27 May 2026 00:12:08 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:de3baa00e9cbd23cb08400401cede3469962760c5c7319bc352e38516245870f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52680592 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7614bc8bb6f92b048557941efe82c9ce3c71b3cd93e6813dc47f52ede806a694`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:48:10 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:48:10 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:48:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:48:10 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 19 May 2026 23:48:10 GMT
ENV PYTHON_VERSION=3.11.15
# Tue, 19 May 2026 23:48:10 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Tue, 19 May 2026 23:59:35 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 19 May 2026 23:59:36 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 May 2026 23:59:36 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:11:40 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:11:40 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:11:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:11:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5eab6366d3242f4dc95b2ea53ecc515095ef214686f85c89bc1d79e62519f7bd`  
		Last Modified: Tue, 19 May 2026 23:59:44 GMT  
		Size: 1.3 MB (1274147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2c22afaf50711b565de04f683662f1730d817fa349d6b327a0a004caa1d9090`  
		Last Modified: Tue, 19 May 2026 23:59:45 GMT  
		Size: 14.3 MB (14315294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31b290acbac4c8288ee790fb5acba2fb1a68ab1abb0c28ba225a09884be43d62`  
		Last Modified: Tue, 19 May 2026 23:59:44 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34e950e7bed5df76d377c724ac1859e499905bed9d6e6aa29da67f58e7c1d438`  
		Last Modified: Wed, 27 May 2026 00:11:47 GMT  
		Size: 6.9 MB (6948983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:9dbae1489be158eff77a8e84fdc3ffc89cbca0899f6c908e23dfd647d1c03b86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209827 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd1e5ad44d1fa483edba512b917b123e57fed40030111affe9bc4def093e05ce`

```dockerfile
```

-	Layers:
	-	`sha256:a133fc77d03b8faaeadb2bff2e63dade3a27fcad6f9864d32fa9d2e8aa719ea5`  
		Last Modified: Wed, 27 May 2026 00:11:47 GMT  
		Size: 2.2 MB (2200355 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d198b78c21f4cda3afca82b66487939e3a137603a105974ee8c9a52186cb8f7`  
		Last Modified: Wed, 27 May 2026 00:11:46 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11` - linux; 386

```console
$ docker pull hylang@sha256:47c944140bb8e69cf1ba9ef803d452b92b214d0a1a035f76bd92a0d2945252ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53948050 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23da3e8fb1ea2558ae61739653cb944571bd401c03056574b9990b41909cacc8`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:55:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:55:47 GMT
ENV LANG=C.UTF-8
# Tue, 19 May 2026 23:55:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:55:47 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 19 May 2026 23:55:47 GMT
ENV PYTHON_VERSION=3.11.15
# Tue, 19 May 2026 23:55:47 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Wed, 20 May 2026 00:15:06 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 20 May 2026 00:15:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 00:15:07 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:10:40 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:10:40 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:10:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:10:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:119761ef8873242d2a8460cbec201255161ea6080d6ae4476c2591ed1a844d8b`  
		Last Modified: Wed, 20 May 2026 00:15:14 GMT  
		Size: 1.3 MB (1297830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9947a67b0fb7d4e110b750fd341ba753ac919101081614b0a833e76fb9c2a7c1`  
		Last Modified: Wed, 20 May 2026 00:15:14 GMT  
		Size: 14.4 MB (14405575 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6329f8f976654ee797bc259c28931ced0bffaa0621a431de456460ccff1dadd`  
		Last Modified: Wed, 20 May 2026 00:15:14 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71d052c1846738fe42bab6adac8f823a7f3fd9b14244630513fce7e7a14b1d92`  
		Last Modified: Wed, 27 May 2026 00:10:48 GMT  
		Size: 6.9 MB (6949061 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:8ecbd603aa79e5282eaf8780365be71ea12faa5d838706373cd3b8f697df5aff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eebedc306f049c99909520a4a6aedd4ab6195048685477b73f618b22c80d11b8`

```dockerfile
```

-	Layers:
	-	`sha256:4a1c8d03d627f6bb6d28f196f23b5ece57ca0090b45c22d4b2a464c5309cf552`  
		Last Modified: Wed, 27 May 2026 00:10:47 GMT  
		Size: 2.2 MB (2197210 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce4dcc112de581aac6345f8622e324a28ab7d4ea0cf206af74d409a0d20f3978`  
		Last Modified: Wed, 27 May 2026 00:10:47 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11` - linux; ppc64le

```console
$ docker pull hylang@sha256:75afc4e27c63617b85ba09abf9cb4cc42d93a09cfa7ace770b38145e411ed2cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.6 MB (56567169 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff467edf5a272f9ff6ffe1800e5d35caa968200886553c0ba619053bd6386fa`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 04:14:27 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 04:14:27 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 04:14:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 04:14:27 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 20 May 2026 04:14:27 GMT
ENV PYTHON_VERSION=3.11.15
# Wed, 20 May 2026 04:14:27 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Wed, 20 May 2026 05:06:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 20 May 2026 05:06:08 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 05:06:08 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:23:44 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:23:44 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:23:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:23:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbecb436bd87ce9525ad05face56651ab7d64ff771f91e10c51a20c991bf7d69`  
		Last Modified: Wed, 20 May 2026 04:33:23 GMT  
		Size: 1.3 MB (1321268 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e82b1910eb2b471d931c9dc9da707e595a37f2ca59a219c0a45dc23b455ca25`  
		Last Modified: Wed, 20 May 2026 05:06:23 GMT  
		Size: 14.7 MB (14695993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5028de87502bde68783fb549bde93175c44d18b8e00fb38e0ea026efef12743`  
		Last Modified: Wed, 20 May 2026 05:06:23 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d31a7b06d0d2305e0ff84c3988e8dbb4720322e6851c88bd0ab35011532c864`  
		Last Modified: Wed, 27 May 2026 00:24:00 GMT  
		Size: 6.9 MB (6949205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:ba891a6e7f64d526597c6d7b94a7fb5a39972db4087704a89bf8fcef21f6acc9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2213028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54436985b052102925e8e5eb72ab000b22c806559b7f175240144963882d7d20`

```dockerfile
```

-	Layers:
	-	`sha256:43f864e5fdd63cf95c4a6776ea23448af5a79b4d163000ceade72d8ef707c67a`  
		Last Modified: Wed, 27 May 2026 00:23:59 GMT  
		Size: 2.2 MB (2203640 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d330412ec50033355b626d9536bbe9d7596a207851d88eef4e01a4263f7f7977`  
		Last Modified: Wed, 27 May 2026 00:23:59 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11` - linux; riscv64

```console
$ docker pull hylang@sha256:4b31a3abad4ee0b0f2d0f30b03f5db1c15d8a15ae2721e69d9db9f8af3b09d09
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50674136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b80a93a844c37de9d70e323a97ecd6a0268b2a989e75342a9b67a59f992496e0`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Fri, 22 May 2026 03:40:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 May 2026 03:40:21 GMT
ENV LANG=C.UTF-8
# Fri, 22 May 2026 03:40:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Fri, 22 May 2026 03:40:21 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 22 May 2026 03:40:21 GMT
ENV PYTHON_VERSION=3.11.15
# Fri, 22 May 2026 03:40:21 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Fri, 22 May 2026 06:48:02 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Fri, 22 May 2026 06:48:03 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 22 May 2026 06:48:03 GMT
CMD ["python3"]
# Sun, 24 May 2026 03:24:14 GMT
ENV HY_VERSION=1.2.0
# Sun, 24 May 2026 03:24:14 GMT
ENV HYRULE_VERSION=1.0.1
# Sun, 24 May 2026 03:24:14 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sun, 24 May 2026 03:24:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64887635710bb3720fe7560b7a4d5dad0dfb67a1d1866a9325f82ee51653a45b`  
		Last Modified: Fri, 22 May 2026 05:23:49 GMT  
		Size: 1.3 MB (1261219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25b89d383be95aac86892142ff52cade70754fd5d0efdb194362b627e5438a47`  
		Last Modified: Fri, 22 May 2026 06:49:14 GMT  
		Size: 14.2 MB (14194434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1ef36bbc165033af559f396e5e64a77198d280142ef829256befad56ce35bb78`  
		Last Modified: Fri, 22 May 2026 06:49:12 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:346a68163c72be92bd30a2d08535c34f384fdafd53af42388e6cf792a7e1d77d`  
		Last Modified: Sun, 24 May 2026 03:25:20 GMT  
		Size: 6.9 MB (6940634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:6d59ba8574e20e43a0c1b0b04f2a53a05d31aed924d380dd7c2c5a2a58a2329d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203399 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b2c35d374b16f18e9033ab77adc69c0308104c88c4c16cd439d02dced5b5975`

```dockerfile
```

-	Layers:
	-	`sha256:60c334c5df6edc00eaf624a22f956f16d50d2463b92af4a5337976fdd450c970`  
		Last Modified: Sun, 24 May 2026 03:25:19 GMT  
		Size: 2.2 MB (2194011 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75ef429360d98f61727135e45309cc97694fc6469e9f9098ee179ab28f875808`  
		Last Modified: Sun, 24 May 2026 03:25:19 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11` - linux; s390x

```console
$ docker pull hylang@sha256:262d2d2b005375a6a737ef31691cb6385f713bb6864db4d0b58957a2923804eb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52468422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:577466f8f8290d24fba083c933f01d6900b3fc485abd58f93db94c6f84ed66eb`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 01:12:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 01:12:19 GMT
ENV LANG=C.UTF-8
# Wed, 20 May 2026 01:12:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 01:12:19 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 20 May 2026 01:12:19 GMT
ENV PYTHON_VERSION=3.11.15
# Wed, 20 May 2026 01:12:19 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Wed, 20 May 2026 01:30:25 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 20 May 2026 01:30:25 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 01:30:25 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:18:20 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:18:20 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:18:20 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:18:20 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0192a62718595eca6c4bd0968d9f9d85ddb1a9cd4f835b9ac8effac7bf23b312`  
		Last Modified: Wed, 20 May 2026 01:25:40 GMT  
		Size: 1.3 MB (1305792 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9454a10be2e5651b442955b5c0820edbf9d12ca7ce0fb542dbc5bef195f3c82`  
		Last Modified: Wed, 20 May 2026 01:30:38 GMT  
		Size: 14.4 MB (14367181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aea9d9d1e36b22eb0ee0fc0c2f5b1f79eaedf379e5f8a8e7d3276d27c10d2226`  
		Last Modified: Wed, 20 May 2026 01:30:38 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37e6855a42cbd0d5d39f806361b0ede783f4915a60928069ddc4798cd3c7f83f`  
		Last Modified: Wed, 27 May 2026 00:18:36 GMT  
		Size: 6.9 MB (6949275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:675237bd991987ed85ba9d5b01898c33c08ce0a864f4cd415ab86aacaf7b967f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a7edea8e8f6bf15d7e2eb5c75a9e1ccedcc6d98f055baadf89ee3592ca7d7a1`

```dockerfile
```

-	Layers:
	-	`sha256:d2839bdc41b56dfa733556c6b3bb7a4534e9a715cef14fee3752ff9311209afd`  
		Last Modified: Wed, 27 May 2026 00:18:36 GMT  
		Size: 2.2 MB (2201488 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7731f0ea7ac26e6cff07267a797c311b721f78cedf57b9ca6cc945ace8c5a469`  
		Last Modified: Wed, 27 May 2026 00:18:36 GMT  
		Size: 9.3 KB (9320 bytes)  
		MIME: application/vnd.in-toto+json
