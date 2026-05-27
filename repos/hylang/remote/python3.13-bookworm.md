## `hylang:python3.13-bookworm`

```console
$ docker pull hylang@sha256:eca113d5e9f7ba2a6c3145dfa3519bd2a880e26181d5a161ecda921402dccd38
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

### `hylang:python3.13-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:8279448240702b8c69305fa5e8cff7b546b0dd2effbff26ce54bce25c62409e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49620376 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bde045524b6e77cd242ee6e8d31ee0a5c4f57c15aa3a5385c2ecef0605a9e07c`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:41:15 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:41:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:41:15 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 May 2026 23:41:15 GMT
ENV PYTHON_VERSION=3.13.13
# Tue, 19 May 2026 23:41:15 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Tue, 19 May 2026 23:50:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 19 May 2026 23:50:49 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 May 2026 23:50:49 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:11:43 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:11:43 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:11:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:11:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:068fedd6b0f109b8186d00d49327b6fc6747c428fd3c9a8739424ff5f38d7531`  
		Last Modified: Tue, 19 May 2026 22:36:36 GMT  
		Size: 28.2 MB (28233543 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f59d65eb126bdbbfafbdc6551ec22d189bcf11e4c4f556e1cb95f03dd424f5c`  
		Last Modified: Tue, 19 May 2026 23:50:56 GMT  
		Size: 3.5 MB (3519874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59dae010ffdc12f24a794eec2ca47e675613b78a165c26b389ea7f670919f998`  
		Last Modified: Tue, 19 May 2026 23:50:56 GMT  
		Size: 12.5 MB (12506022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36d1aa696f899174752f594312e62a77a068b3f1a7a751bffafecdff61b55dcb`  
		Last Modified: Tue, 19 May 2026 23:50:56 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:253746c7f2c720348c0dd85158f6cd022c666e66bc3d00e4997829ffd25ddf68`  
		Last Modified: Wed, 27 May 2026 00:11:51 GMT  
		Size: 5.4 MB (5360687 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:511dbcc7634f4e71f11c2397ee462b725f6e51636d62b7645d91235c97ad9ea4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a96e9ac23025223d80960a8ddc58fb7b43b3bf86977886725a9751f1b89c800f`

```dockerfile
```

-	Layers:
	-	`sha256:81ac1e0a515bd79d27530258590065350f6dc3fd5358fae287a71797818e4c3d`  
		Last Modified: Wed, 27 May 2026 00:11:51 GMT  
		Size: 2.5 MB (2530796 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8800f5b44be0b8dc9e3d27681263e9a2e0b309a0978d43ec8f67ad2c00ef9a0e`  
		Last Modified: Wed, 27 May 2026 00:11:50 GMT  
		Size: 8.1 KB (8079 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:b1f5ff26e96c020bf37c5f1274710e02af60bdafc57c17bd777836da4f7fd13a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46260526 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96d03f8dd10d141db9415171aac3ce16f5fca5478e35f64c95a6e8b21dd6f750`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:16:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:16:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:16:26 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 May 2026 00:16:26 GMT
ENV PYTHON_VERSION=3.13.13
# Wed, 20 May 2026 00:16:26 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Wed, 20 May 2026 00:34:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 20 May 2026 00:34:46 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 00:34:46 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:09:57 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:09:57 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:09:57 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:09:57 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3e5afa2eeb01167c187727ebcf5bb90554d4e6dd21fe61f1f694b128ceb15ac1`  
		Last Modified: Tue, 19 May 2026 22:36:20 GMT  
		Size: 25.8 MB (25768291 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31a83fbda4a2ec7fc1bf1a1b749a18d74cfd0eecf031fb270a5b8d49109af46b`  
		Last Modified: Wed, 20 May 2026 00:34:53 GMT  
		Size: 3.1 MB (3093146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09375048c03c37487df9c8874f17e3c8f8e281a75d7c36d7483e4df81e784f02`  
		Last Modified: Wed, 20 May 2026 00:34:54 GMT  
		Size: 12.0 MB (12038221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b9f17709a857ac941f76ad2fd292d3271530d20c0c5189489c73cdd526f6a53d`  
		Last Modified: Wed, 20 May 2026 00:34:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68094ece4ae2550912da42c622685fe389883b85d0060449008c2e8311b3217e`  
		Last Modified: Wed, 27 May 2026 00:10:04 GMT  
		Size: 5.4 MB (5360619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:ad9fd12fe87701bb5e8a431b0a3ff0358b2351a86154e64ae841017c4f03328b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2542767 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e79f6a88cd3cb2a07ac81cfc658aac8edc241c213be4d9c0b86b4e2fb1997b31`

```dockerfile
```

-	Layers:
	-	`sha256:f30032f462a5879a179594eb5024b93cfd6e4bdf564dba9c6be9d1cdf738b94a`  
		Last Modified: Wed, 27 May 2026 00:10:04 GMT  
		Size: 2.5 MB (2534608 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb48d08cfab552b1b390d4dcc588c3f70847708054473fb7220689fdc0df1e31`  
		Last Modified: Wed, 27 May 2026 00:10:04 GMT  
		Size: 8.2 KB (8159 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:5d2cee1a4c9170929591e19732f446447415c829fe9ec9046f08c5237e96dce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43899799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f14c7a61094e15915be213e141254eba493f343ee048d151e75c84ea4f1670f6`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:51:15 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:51:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:51:15 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 May 2026 00:51:15 GMT
ENV PYTHON_VERSION=3.13.13
# Wed, 20 May 2026 00:51:15 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Wed, 20 May 2026 01:12:45 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 20 May 2026 01:12:45 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 01:12:45 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:11:06 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:11:06 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:11:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:11:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:af86988b12731b7fa2ac73fa1c3f6ab4510a6641d04afb18df09600383bc399d`  
		Last Modified: Tue, 19 May 2026 22:36:05 GMT  
		Size: 23.9 MB (23941643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9943eb9c3fccb4e8d7be848d07f617f38c6e90572c6008db90f44e12dacbb9d3`  
		Last Modified: Wed, 20 May 2026 01:12:53 GMT  
		Size: 2.9 MB (2928545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b10a69aea68e0f96901c60bc23b9203d8eec98493884eca8ce1559b40ecaaa0`  
		Last Modified: Wed, 20 May 2026 01:12:53 GMT  
		Size: 11.7 MB (11668625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:010b6da2ec523b364a8ae6e8b08a8a1119d309bc6ddd6434ef9f61649bd62dd4`  
		Last Modified: Wed, 20 May 2026 01:12:52 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b602a106494693c3ad406e92e322c21e5d5e2bf1a61c9158a65d335688fd232`  
		Last Modified: Wed, 27 May 2026 00:11:13 GMT  
		Size: 5.4 MB (5360737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:b4e521197e0ae66382c0b77597d3bec7260477bad6f12a7034049e0e5095d8f3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2541200 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c924786b32df96e5677d03746f8157cd85a345efa98e161d3f5a60fc9737e42`

```dockerfile
```

-	Layers:
	-	`sha256:9f0d1cfca13b311cc5d58740e0171a8788fc8a226afa6257f0e0ce03e28a5385`  
		Last Modified: Wed, 27 May 2026 00:11:13 GMT  
		Size: 2.5 MB (2533041 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:82d4bfcd08cc3876da8c719cd5db5a0ceaf17131f6156e286560de9ea721edfd`  
		Last Modified: Wed, 27 May 2026 00:11:13 GMT  
		Size: 8.2 KB (8159 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:3209ef9cceae44237bc6de324468cec9cae90ddfd07c055350189123687b924f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.2 MB (49234531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08679445a729529362c16adb1f936737695a459e045cd2a0d241345db627d0bf`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1779062400'
# Tue, 19 May 2026 23:44:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:44:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 19 May 2026 23:44:20 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 19 May 2026 23:44:20 GMT
ENV PYTHON_VERSION=3.13.13
# Tue, 19 May 2026 23:44:20 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Tue, 19 May 2026 23:58:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 19 May 2026 23:58:26 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 May 2026 23:58:26 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:11:20 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:11:20 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:11:20 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:11:20 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f400d36d7784570c9fb7558e367d2b5d38e8b2f1d6faee041815acea7f87e669`  
		Last Modified: Tue, 19 May 2026 22:36:40 GMT  
		Size: 28.1 MB (28115043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c25ba0749ef3a82f5ef8d1ec0faa92c0ef39b97d67d4bfe13ed99a0ac757ec03`  
		Last Modified: Tue, 19 May 2026 23:58:35 GMT  
		Size: 3.4 MB (3351830 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fa1415133f17333dc45075a2a9ec73d04e8856502d2f2bee4e812d3aa99ea07`  
		Last Modified: Tue, 19 May 2026 23:58:35 GMT  
		Size: 12.4 MB (12406922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bea3e78864a8889b7fe3bf62966bebbf6e332b9446fce80803c012a5d81d66bf`  
		Last Modified: Tue, 19 May 2026 23:58:35 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91038600d7a2bbb2f935f1a04237984438547eeb2ee0ed0765e89d1c7f7895fa`  
		Last Modified: Wed, 27 May 2026 00:11:28 GMT  
		Size: 5.4 MB (5360486 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:a1bcf0c505c7961015d1b1e5a99ef1197b3d5e79a401a132efc3cf1e5a3cde0b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2539242 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d3fecdc9bc19ad337f79c63a992270ecdb314193ac3370775c28ec7986a6189`

```dockerfile
```

-	Layers:
	-	`sha256:315538fb171e53a9a044e8125a0920ad13750f5132c294b3d4f96e9dc2da6b37`  
		Last Modified: Wed, 27 May 2026 00:11:27 GMT  
		Size: 2.5 MB (2531061 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64598271c140a07f9bf12a9d4ae1c5a34b8e68c9d2b7f83eacd395fd7353c3c7`  
		Last Modified: Wed, 27 May 2026 00:11:27 GMT  
		Size: 8.2 KB (8181 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:7661ffae3ec4d0084e4676c20bd1bfa8d47e9e0ac56a5254c549c4b707b39f02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.8 MB (50752887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eb86744ff43140b89949cd7dc6ae0b33fd68f25e5a6247a4948078c518aff2b`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1775433600'
# Tue, 07 Apr 2026 01:59:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:59:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:59:21 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 07 Apr 2026 01:59:21 GMT
ENV PYTHON_VERSION=3.13.12
# Tue, 07 Apr 2026 01:59:21 GMT
ENV PYTHON_SHA256=2a84cd31dd8d8ea8aaff75de66fc1b4b0127dd5799aa50a64ae9a313885b4593
# Tue, 07 Apr 2026 02:10:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 07 Apr 2026 02:10:56 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 07 Apr 2026 02:10:56 GMT
CMD ["python3"]
# Tue, 07 Apr 2026 02:56:42 GMT
ENV HY_VERSION=1.2.0
# Tue, 07 Apr 2026 02:56:42 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 07 Apr 2026 02:56:42 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 07 Apr 2026 02:56:42 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2686573d3309fb5ec86398e0f20a729a351a259d4d793edf6cb41a0ef910fccb`  
		Last Modified: Tue, 07 Apr 2026 00:10:58 GMT  
		Size: 29.2 MB (29221768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dfbe15c4df92f37285824d4b8461ee0b78e941d51dba80e51373b96386401dc`  
		Last Modified: Tue, 07 Apr 2026 02:11:03 GMT  
		Size: 3.5 MB (3518071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1312b870cdaa46a6ea733b7c56557b3419ccfae72ae7f8e57a192dc3dca30e14`  
		Last Modified: Tue, 07 Apr 2026 02:11:03 GMT  
		Size: 12.7 MB (12716514 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9dc6fe7ffb736cba773db56a21e56856a534a0629b7a5819f2adda036ec7358a`  
		Last Modified: Tue, 07 Apr 2026 02:11:03 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:537a5a7deab2d4044a5e2fc23e0fdf6e32633c3c54f0eac3832e712010dee617`  
		Last Modified: Tue, 07 Apr 2026 02:56:48 GMT  
		Size: 5.3 MB (5296285 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:b8e82c18d9c129ff43c43b0e6581e87efad3daa47f92660c944bf5fc0858b013
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2535984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7207269ae4a4d4b4900b6ff240a23bc3fd571bc20c067cea53822f04f0e2e3d0`

```dockerfile
```

-	Layers:
	-	`sha256:fcc97af40062008772ce00b464d07390045b0e6cc3b83faba0d87ba78d8ee17f`  
		Last Modified: Tue, 07 Apr 2026 02:56:48 GMT  
		Size: 2.5 MB (2527937 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:835ad397f31cf1763d5bb1fa3b572ccddead79be632105061cda5d16647f8b70`  
		Last Modified: Tue, 07 Apr 2026 02:56:48 GMT  
		Size: 8.0 KB (8047 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:6c03d5ab8c29e73294e8684f02d60f95a183e13e38617f5251638d0e96daba55
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.2 MB (54205294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:981ea552f96e761b08e26c21c16b3023de94cbfce36e7fd430ffc4285225723a`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 02:54:07 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 02:54:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 02:54:07 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 May 2026 02:54:07 GMT
ENV PYTHON_VERSION=3.13.13
# Wed, 20 May 2026 02:54:07 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Wed, 20 May 2026 04:47:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 20 May 2026 04:47:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 04:47:55 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:21:02 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:21:02 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:21:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:21:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:562cecbb5aa529d280e58ef1f95f14cdcd37a90c5ea9181798a78377e934e6e7`  
		Last Modified: Tue, 19 May 2026 22:35:14 GMT  
		Size: 32.1 MB (32075742 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:656be72c102b00f533067cbc2d9437f945c4e7bfd322feb0c3a1cccb673dd5ba`  
		Last Modified: Wed, 20 May 2026 03:33:50 GMT  
		Size: 3.7 MB (3725042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:279117a2cc03a21136cdb676fc01d15f951b8cf01c3199e1a78cb8912117d2b8`  
		Last Modified: Wed, 20 May 2026 04:48:10 GMT  
		Size: 13.0 MB (13043512 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:295561b271a1b8a769208dd88e5f01a52f17469d57e9bf73fbd3e54ef014408e`  
		Last Modified: Wed, 20 May 2026 04:48:09 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6a00011bdbdbb7fcadb2d7e358b39d783b82b9f2c3ee9409907349eb93a3808`  
		Last Modified: Wed, 27 May 2026 00:21:17 GMT  
		Size: 5.4 MB (5360749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:43ba62a1e533aa236d9dec447e88183d75ca96a9fa5db64bb26413da509f084d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2543357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb3ace63271c59738aeb1b67e3711f8deb5b6ac9328079fc01922f779f7118dd`

```dockerfile
```

-	Layers:
	-	`sha256:4c69d95ea9faec6975de64d93fa4c25d370bff8f8e8926ff24e02336cbe2db6e`  
		Last Modified: Wed, 27 May 2026 00:21:17 GMT  
		Size: 2.5 MB (2535234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bfd4ecc74cefdbf2c2bc4d12f0ddfa6d5c871008d032a59d07f0c3c11d71a7fe`  
		Last Modified: Wed, 27 May 2026 00:21:17 GMT  
		Size: 8.1 KB (8123 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:9f78cee4809463e5f5210f6901b825faaaf5d7798e15862f8997a13f4b937e54
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47780280 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95dd757427830b545d11698bbfd2c2433c64a794ab885242109e1cdd6f93beaf`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1779062400'
# Wed, 20 May 2026 00:59:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:59:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 20 May 2026 00:59:38 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 20 May 2026 00:59:38 GMT
ENV PYTHON_VERSION=3.13.13
# Wed, 20 May 2026 00:59:38 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Wed, 20 May 2026 01:20:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 20 May 2026 01:20:56 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 01:20:56 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:16:22 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:16:22 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:16:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:16:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d5e0676594538bc23596fec84864fdfc1967950a13d798821e9073e432129029`  
		Last Modified: Tue, 19 May 2026 22:35:41 GMT  
		Size: 26.9 MB (26888597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3cc3b40ae0abc7d79db803a5d5f6b8363ddd984965d9be43d17b3b4e4d351706`  
		Last Modified: Wed, 20 May 2026 01:15:07 GMT  
		Size: 3.2 MB (3184026 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1caac896e73e3a5c953b9430b2ab650d75209bbedc8b163cabc02812e209e6ca`  
		Last Modified: Wed, 20 May 2026 01:21:09 GMT  
		Size: 12.3 MB (12346329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bb7707d00841de7413f0ccce627b926ecbbff10cbe88aa1383e53f7e9ad8430`  
		Last Modified: Wed, 20 May 2026 01:21:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20bf409c4f433f51c5d933eadbe8d808e4cf0cff331c04bc3539051a47d9c329`  
		Last Modified: Wed, 27 May 2026 00:16:36 GMT  
		Size: 5.4 MB (5361078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:02ae7b19ad344dda76ac14e4dc9f967ff37caa37557155501cb36738af463965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2535699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:292915a911cc557e491bcdf15a170bdc989841ff12f18676781fed656c2a3aaa`

```dockerfile
```

-	Layers:
	-	`sha256:e880a73284f5f68a7c983f8ff7e46e3e4202ab729ea47676c8b5bf460b354f45`  
		Last Modified: Wed, 27 May 2026 00:16:36 GMT  
		Size: 2.5 MB (2527620 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09b632709ae53124e458de38038efb3fd5209f4ce56f193be554f1f07f7bcd94`  
		Last Modified: Wed, 27 May 2026 00:16:36 GMT  
		Size: 8.1 KB (8079 bytes)  
		MIME: application/vnd.in-toto+json
