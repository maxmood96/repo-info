## `python:slim-bookworm`

```console
$ docker pull python@sha256:a8deffe0831b189dfff595be7a629fe7ba674e41f48ee11cf73c0bbae90cd4a8
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

### `python:slim-bookworm` - linux; amd64

```console
$ docker pull python@sha256:77249a49ad5cf328a0e36e8d568ecfc9f45275dbbd72dc5e993b0b07553b9478
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.2 MB (44164401 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cb54302c4d59327aac59f3f6f25eeafeb365fc411964c0d850ceb2557b33ea4`
-	Default Command: `["python3"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PYTHON_VERSION=3.13.7
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PYTHON_SHA256=5462f9099dfd30e238def83c71d91897d8caa5ff6ebc7a50f14d4802cdaaa79a
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:b1badc6e50664185acfaa0ca255d8076061c2a9d881cecaaad281ae11af000ce`  
		Last Modified: Tue, 12 Aug 2025 20:44:36 GMT  
		Size: 28.2 MB (28230255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7e88bf276da094b3c1c5d62775d85ae6e63c58165a5c759570bcecf8b52a4ce3`  
		Last Modified: Fri, 15 Aug 2025 22:17:34 GMT  
		Size: 3.5 MB (3515854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d55dfff74d98ac204fa78f18533eecc39a8bd69bd9384a73572c6d09f06b11fc`  
		Last Modified: Fri, 15 Aug 2025 22:17:35 GMT  
		Size: 12.4 MB (12418042 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97853488aa5b877aa1248a8d146c75752543b00dced77518e40164d1badafd3`  
		Last Modified: Fri, 15 Aug 2025 22:17:34 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-bookworm` - unknown; unknown

```console
$ docker pull python@sha256:a71bad72d4bc59f93ad18abf56446d9b4761d9600cae4baa4edf5097abfee58e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2545789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401415b6f4f19a1bbb7b54a2e233aaa07ae3d97a265fb7082ebdcb4c11987152`

```dockerfile
```

-	Layers:
	-	`sha256:25598d7a5d1d02fb97447e0279d15a1b9f49414011e4543a823a88155cdcf71c`  
		Last Modified: Sat, 16 Aug 2025 00:07:20 GMT  
		Size: 2.5 MB (2521787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:54fac894940ff07834fd228492e0299d43f1be39559c0fae6c9fa155d459acde`  
		Last Modified: Sat, 16 Aug 2025 00:07:21 GMT  
		Size: 24.0 KB (24002 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim-bookworm` - linux; arm variant v5

```console
$ docker pull python@sha256:e7783225a15466ab6edc14cd4ce9097294c5773603c2054ef02b38344b1f31ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.8 MB (40806679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ced71b40da3f3872e7962eedf5401bd57de6531572548e98d681905aac1d849`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 08 Aug 2025 18:20:34 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1754870400'
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_VERSION=3.13.6
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_SHA256=17ba5508819d8736a14fbfc47d36e184946a877851b2e9c4b6c43acb44a3b104
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:53f325cb4b149fb7bd7e6ed7f8dfc1c5a37b5d828d75b4e6ba65a5cfd25aec56`  
		Last Modified: Tue, 12 Aug 2025 20:45:02 GMT  
		Size: 25.8 MB (25762718 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09dec5f110df2e60bbdaa736e46162e807aa8aef97e99fd2f78ad66bf2ea4b68`  
		Last Modified: Wed, 13 Aug 2025 06:43:07 GMT  
		Size: 3.1 MB (3090744 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2057f8606ddbfd9b7bbef603f148ce97ed86ecebaf50487a71eda0282cec3039`  
		Last Modified: Wed, 13 Aug 2025 07:23:05 GMT  
		Size: 12.0 MB (11952967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e6b9679ef4b7380aabaa470217828866794071aae33c8550f8dce90034f3630`  
		Last Modified: Wed, 13 Aug 2025 07:23:03 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-bookworm` - unknown; unknown

```console
$ docker pull python@sha256:64132603e9c4ec374f631e2fc705834486fe8a0e23f488bef29fa051bd67f6f7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2549703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f45bb7fdf03edc63e8d2e5ddf7908adeefcb8e0cbb8915bc3d4b5ca09d44e3d`

```dockerfile
```

-	Layers:
	-	`sha256:c4b2f2de8dd3f75cbf21d8966bbff6fd4708ea3f91a4fbbc146ea3f3badb7702`  
		Last Modified: Wed, 13 Aug 2025 09:06:40 GMT  
		Size: 2.5 MB (2525599 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff538598b05f5bd353afe41c8960383463a7b006627805a8f14ab8f681c390fb`  
		Last Modified: Wed, 13 Aug 2025 09:06:40 GMT  
		Size: 24.1 KB (24104 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim-bookworm` - linux; arm variant v7

```console
$ docker pull python@sha256:6c2c4459ec230c8f45f452d88c277916cea01f78c5d7ada278dd0ba136496b5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.4 MB (38444898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e7d1ed0a463d1bebcba13093c2b5ea2440a7e69798044d7dff8bc7bbcecb508`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 08 Aug 2025 18:20:34 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1754870400'
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_VERSION=3.13.6
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_SHA256=17ba5508819d8736a14fbfc47d36e184946a877851b2e9c4b6c43acb44a3b104
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:a8db185805c54c045d888f7030794ebee970355b2336287cac0a0e22638ffc98`  
		Last Modified: Tue, 12 Aug 2025 20:46:38 GMT  
		Size: 23.9 MB (23938929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:601b8e18476b9426c3c3ff9e8f97d4a6a1f711e63451a36bfe3e47556043eff2`  
		Last Modified: Wed, 13 Aug 2025 07:20:37 GMT  
		Size: 2.9 MB (2925400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eac38c32d8e77a8ddaa7bf65837401089cae48b64a75f7db9dc854ec96b2b30`  
		Last Modified: Wed, 13 Aug 2025 08:05:39 GMT  
		Size: 11.6 MB (11580318 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a530801104c29e103433746a319934a9720a7106acfe95c39005a8028258e44`  
		Last Modified: Wed, 13 Aug 2025 08:05:39 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-bookworm` - unknown; unknown

```console
$ docker pull python@sha256:004a5089fa627beab75be959217e46330c6892ba5baa71611b4cb976f75628db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2548137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f328f6a58cdc4736eb026f0693dd4b910d5fcbeab03daab325d131a52ccb1a86`

```dockerfile
```

-	Layers:
	-	`sha256:424848569f1df9c0c6939a61fab86036ab192991977891dae66e1cbb9f237917`  
		Last Modified: Wed, 13 Aug 2025 09:06:44 GMT  
		Size: 2.5 MB (2524032 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:608825d8c037de1c9792f28a686198f7a348d0051a8c2db79a413af4fdf633ee`  
		Last Modified: Wed, 13 Aug 2025 09:06:45 GMT  
		Size: 24.1 KB (24105 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull python@sha256:af9f3fc56d922f10d91a4de6cc24162096731e50b4500b8d4f18ebdfd282f105
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43743390 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3a386b2c3da4f29b198e7549bf2ff0fb8ae8a6437c899cb778e3bf9af1924a8`
-	Default Command: `["python3"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PYTHON_VERSION=3.13.7
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PYTHON_SHA256=5462f9099dfd30e238def83c71d91897d8caa5ff6ebc7a50f14d4802cdaaa79a
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:9a80f9a055240e1d5ffd4b99717e18b5b3e924369b9155fb0a951a7a94b2c61f`  
		Last Modified: Tue, 12 Aug 2025 22:08:02 GMT  
		Size: 28.1 MB (28082001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe697250a5eed0d0d4177115f73b2a198e5ec0cfa9dec3a31e818591130d021`  
		Last Modified: Fri, 15 Aug 2025 22:44:23 GMT  
		Size: 3.3 MB (3349172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d7ddaa183691a829909e5c8563d6d9be9da655c637eff1e7c9c89ab97425f6`  
		Last Modified: Fri, 15 Aug 2025 23:39:56 GMT  
		Size: 12.3 MB (12311968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46d0b9a5423d52fa85df9dcd86f5d619687a6d58a23cb13b3549390e0561da18`  
		Last Modified: Fri, 15 Aug 2025 23:39:55 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-bookworm` - unknown; unknown

```console
$ docker pull python@sha256:98c8dc87bef7bce8553b48dbf5dee6e5557df6875ae6768829af845e07d898d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2546189 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acd545344cdbc2668108fa9b61b70930b6e26bda47392e6ff3ec98b245305ecf`

```dockerfile
```

-	Layers:
	-	`sha256:7e98a1f4e45cd3ff240463c45656c1ade648c75288e62c60ee88d714c891dc58`  
		Last Modified: Sat, 16 Aug 2025 00:09:48 GMT  
		Size: 2.5 MB (2522052 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a079ae2f2c286248d8421b9cd4303912ce2842700093ae20d379fd506244bcf4`  
		Last Modified: Sat, 16 Aug 2025 00:09:49 GMT  
		Size: 24.1 KB (24137 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim-bookworm` - linux; 386

```console
$ docker pull python@sha256:af0660e687fe285dcc87bb27cb7eea6e249797cb95b2b06d7f34284e52cabf28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.4 MB (45386292 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0473675960e9ec369528ba49d2db59af1f1226686459e72e015912adef5946c6`
-	Default Command: `["python3"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1754870400'
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PYTHON_VERSION=3.13.7
# Thu, 14 Aug 2025 21:49:23 GMT
ENV PYTHON_SHA256=5462f9099dfd30e238def83c71d91897d8caa5ff6ebc7a50f14d4802cdaaa79a
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 14 Aug 2025 21:49:23 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:de83e1b86bff46f07bde3b82cca8622aed0b900dbeec110f1205a282d10bae64`  
		Last Modified: Tue, 12 Aug 2025 20:46:35 GMT  
		Size: 29.2 MB (29212605 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edd8f7189b48c01a1dadbfbea24631619db0a8f9a458a01d96b364d4c49356be`  
		Last Modified: Fri, 15 Aug 2025 22:20:00 GMT  
		Size: 3.5 MB (3516492 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a906baead5e3a3f73d91068d27f65f2aea8d9290b2bab38e98027d00a98ae61`  
		Last Modified: Fri, 15 Aug 2025 22:20:01 GMT  
		Size: 12.7 MB (12656945 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfcbd9d49b5e7260ccd8920ad4d057b3011a221aa06386f94ec08c9dec039e21`  
		Last Modified: Fri, 15 Aug 2025 22:19:59 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-bookworm` - unknown; unknown

```console
$ docker pull python@sha256:d9fa4891ef4ae9d0bcc65c075529e41e1205b9cc549adf009d577e37545c4268
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2542921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05b840256d8fba89a6a16133c31f929886d352e96d729c95a564834b14b209a8`

```dockerfile
```

-	Layers:
	-	`sha256:81b8bd6cace18bb56789261f45381546eb72c78ea09da94be4c0b0b5469535af`  
		Last Modified: Sat, 16 Aug 2025 00:07:32 GMT  
		Size: 2.5 MB (2518954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:abe68beb1293e8266bf7ec48d27e553f4efd75579d4c6e082c4d05e0d60da4d0`  
		Last Modified: Sat, 16 Aug 2025 00:07:33 GMT  
		Size: 24.0 KB (23967 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim-bookworm` - linux; ppc64le

```console
$ docker pull python@sha256:9c53d06d6e6e260ae057f10c9bf15e41dc3f667ba1daa8d85a62aeeb1c04d133
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48748255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a85b649d4e34bb048aecb60405db08c929b49e553f13728a3c9c3c97cc318ca1`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 08 Aug 2025 18:20:34 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1754870400'
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_VERSION=3.13.6
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_SHA256=17ba5508819d8736a14fbfc47d36e184946a877851b2e9c4b6c43acb44a3b104
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:a0acf07605078e5950db4f22a00d81ec636270d184a86cff95e60b78f012035c`  
		Last Modified: Tue, 12 Aug 2025 23:06:40 GMT  
		Size: 32.1 MB (32073420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fffce61714b8a2cb0526299f0dd1a14c8f61653b2df173b04148bab3aedd1958`  
		Last Modified: Wed, 13 Aug 2025 15:18:17 GMT  
		Size: 3.7 MB (3721150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:860f722d1e719a296293e95e81c3640a259749f3f63722ae68e267aea2b435e6`  
		Last Modified: Wed, 13 Aug 2025 15:12:48 GMT  
		Size: 13.0 MB (12953435 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c89bfb8513b7e0d3d25a3ef3cd544cb910e99ef9e67e26a6b36e2679f62eac`  
		Last Modified: Wed, 13 Aug 2025 15:12:47 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-bookworm` - unknown; unknown

```console
$ docker pull python@sha256:3bd6095151463804f47b313df10a5aae0977157c83f27f9d76e5343fbeb6e990
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2550276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4224596c6c1e6ce644866a49d80e5c487dda4602094b72073ecd0e783ef0464`

```dockerfile
```

-	Layers:
	-	`sha256:3bcb0565da4a0b8b25b780ec513e8a49b932f0cc6711e41abdda986394e9ce0a`  
		Last Modified: Wed, 13 Aug 2025 18:06:51 GMT  
		Size: 2.5 MB (2526225 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:69b6c37ec5936fcee7c70f4c78ae5ad88bd97cb188201f0021d6d974af62ce74`  
		Last Modified: Wed, 13 Aug 2025 18:06:52 GMT  
		Size: 24.1 KB (24051 bytes)  
		MIME: application/vnd.in-toto+json

### `python:slim-bookworm` - linux; s390x

```console
$ docker pull python@sha256:cbc48e80ab9ecb9fa306272e39964f7c2c485e3feabebb1f5b1b61db4613f286
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.3 MB (42324782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:607ea3ad315e58ba4ac37860f287c09afdaba052af16628278804d30fdd1a7b0`
-	Default Command: `["python3"]`

```dockerfile
# Fri, 08 Aug 2025 18:20:34 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1754870400'
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_VERSION=3.13.6
# Fri, 08 Aug 2025 18:20:34 GMT
ENV PYTHON_SHA256=17ba5508819d8736a14fbfc47d36e184946a877851b2e9c4b6c43acb44a3b104
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 08 Aug 2025 18:20:34 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:1ae61276e6df96a4fa21616b89ef0ebf78ce7e8d7e42d3264ead2281b12b910a`  
		Last Modified: Wed, 13 Aug 2025 09:16:19 GMT  
		Size: 26.9 MB (26887836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b914ea7d5b8a6c209c0b51bc492d37f21c0df11ecf535ac516eeabc736c9f3c`  
		Last Modified: Wed, 13 Aug 2025 16:50:24 GMT  
		Size: 3.2 MB (3181735 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b345a5801d1c20b6a3321465804c620aa98cd9c1c11a824aa5928435f4034590`  
		Last Modified: Wed, 13 Aug 2025 16:59:40 GMT  
		Size: 12.3 MB (12254962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bac177532844aa67e10b2cc65ec276ea0913b4dbb95d5175ed6195ea13dfe81e`  
		Last Modified: Wed, 13 Aug 2025 16:59:38 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `python:slim-bookworm` - unknown; unknown

```console
$ docker pull python@sha256:3449a2b1ac1000a212fcefa390f1fff8001e8793f6cbe1400865223133865209
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2542614 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4283be7eaaa3720aeac7bc0e1046fdc2239cc037b0766a65c6edb9581a95397`

```dockerfile
```

-	Layers:
	-	`sha256:df51d8d1d42d02487161d3b2f0d33f87749c4c75f1211af6a7a6f763b2190514`  
		Last Modified: Wed, 13 Aug 2025 18:06:56 GMT  
		Size: 2.5 MB (2518611 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04eb3e0c3e774d4444631cc2fa9667649ff3005911ef8f95ec70a3250c03a121`  
		Last Modified: Wed, 13 Aug 2025 18:06:57 GMT  
		Size: 24.0 KB (24003 bytes)  
		MIME: application/vnd.in-toto+json
