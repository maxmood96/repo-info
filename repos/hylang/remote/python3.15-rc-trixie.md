## `hylang:python3.15-rc-trixie`

```console
$ docker pull hylang@sha256:28da2531a053abe5de412d03d8878a4c0fc194e0294543748f7f653cf2644c7c
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

### `hylang:python3.15-rc-trixie` - linux; amd64

```console
$ docker pull hylang@sha256:2214e25f395e35d2a5301ece5fa033ca3acb267a633092e149c6c510279612fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49792662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2acfec0b65d94a0462a4b204de522df510fbbf596ce7f6a39bd1d34ac9dce2b0`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:39:46 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:39:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:39:46 GMT
ENV PYTHON_VERSION=3.15.0b1
# Tue, 19 May 2026 23:39:46 GMT
ENV PYTHON_SHA256=d4d52ccfa1d727ef5235fbb7d70fa1dbacf10b8b3760db622875da05acbe437c
# Tue, 19 May 2026 23:47:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 19 May 2026 23:47:14 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 May 2026 23:47:14 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:11:12 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:11:12 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:11:12 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:11:12 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5b4d6ff92fc4e14e911b7753c954fac965d48c40fe1075758d284148ccace970`  
		Last Modified: Tue, 19 May 2026 22:37:05 GMT  
		Size: 29.8 MB (29779926 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:244a7245146989f95cb0f84865f274f38aadd2a2f8401f87fdf2904b129201f5`  
		Last Modified: Tue, 19 May 2026 23:47:22 GMT  
		Size: 1.3 MB (1293280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf6fd34dcdca7a5bd354cfdbbbfcaa0314d7cdb15a69098c9b36aa430bbcf7ba`  
		Last Modified: Tue, 19 May 2026 23:47:23 GMT  
		Size: 12.9 MB (12879282 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4219fb56d120da0caa7b1884baceba17c4a31f12f75e29e8fb7ec1ad1270a49`  
		Last Modified: Tue, 19 May 2026 23:47:22 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89b2c788dc96c98a7a2aaf6a5d19b6d21f193f8be59bd32cf8e5d54f46faf2ab`  
		Last Modified: Wed, 27 May 2026 00:11:19 GMT  
		Size: 5.8 MB (5839925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:941071c40a1587b55582b66327f015bcda7ef3c209e4a0b819f4294ac5b4c37f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2af859e2097af5c3518593892f414bf188ff329b6ba592a7847b653c3276c93d`

```dockerfile
```

-	Layers:
	-	`sha256:4c8d73dfc50da32c7a687e20d9ff6602c2e8b280afed3982e95833c50fef690f`  
		Last Modified: Wed, 27 May 2026 00:11:19 GMT  
		Size: 2.2 MB (2154353 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4751270e9546a38102fb8cd88271d8d1c4a308362e747db7c6796cdcc11a7a68`  
		Last Modified: Wed, 27 May 2026 00:11:19 GMT  
		Size: 9.3 KB (9315 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-trixie` - linux; arm variant v5

```console
$ docker pull hylang@sha256:b5eb4b074c8e27010a7eadab8624d42a5802c25c954edd3e5a7af936069af05a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.6 MB (47641865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef267f85a7bb3b3e3612471f083cabbb9cc51174ff0b847470878e890365b28c`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:10:34 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:10:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:10:34 GMT
ENV PYTHON_VERSION=3.15.0b1
# Wed, 20 May 2026 00:10:34 GMT
ENV PYTHON_SHA256=d4d52ccfa1d727ef5235fbb7d70fa1dbacf10b8b3760db622875da05acbe437c
# Wed, 20 May 2026 00:20:59 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 20 May 2026 00:20:59 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 00:20:59 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:09:16 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:09:16 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:09:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:09:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:37dea77b903ae642229487445fa64e20dcf83d60070467f9c7581fb71a2dd8a8`  
		Last Modified: Tue, 19 May 2026 22:36:45 GMT  
		Size: 28.0 MB (27953869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8001176fa9378ae003e0ce85b21c9a5e19e50283cd52decbc72c64dea1ab8a02`  
		Last Modified: Wed, 20 May 2026 00:21:07 GMT  
		Size: 1.3 MB (1276421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1ed99b6a6847f99982e881294e06e364c76c8b6d9ae3a48c471bed61ebc7408`  
		Last Modified: Wed, 20 May 2026 00:21:07 GMT  
		Size: 12.6 MB (12571335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fbe55e720c4dd2ff678763f0abec7f6b845696a791f3f71cd1efc8b5aef41cc`  
		Last Modified: Wed, 20 May 2026 00:21:07 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:868e775582979f7324f735936bfa1b6a925ff190f05089851bf2c3d37084355f`  
		Last Modified: Wed, 27 May 2026 00:09:23 GMT  
		Size: 5.8 MB (5839991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:556990b679578e6ff99366655e9c041b06ba2a92f00601ecc7a2607fbb5b63bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2166782 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1715435c357b7854d981cfafe8ddf72c82c61769354adc64208667ccdc4d8972`

```dockerfile
```

-	Layers:
	-	`sha256:08faf045e12c7199dfadc0fdea5abe6a93429b95578e9480e7e0836634eb927d`  
		Last Modified: Wed, 27 May 2026 00:09:23 GMT  
		Size: 2.2 MB (2157354 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:377cf3365364ea4655eef1d9a17911c35c1fa681a0cd74052b223f2fcc473dcf`  
		Last Modified: Wed, 27 May 2026 00:09:23 GMT  
		Size: 9.4 KB (9428 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-trixie` - linux; arm variant v7

```console
$ docker pull hylang@sha256:8443b96de9fb3756426952fb573518287a325b8d05b14eea6447f359a224055e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.8 MB (45777940 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6919e270fa1d344c7935b7b909a0de050100fb51b954c80122e24feb072e6c1`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:47:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:47:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:47:26 GMT
ENV PYTHON_VERSION=3.15.0b1
# Wed, 20 May 2026 00:47:26 GMT
ENV PYTHON_SHA256=d4d52ccfa1d727ef5235fbb7d70fa1dbacf10b8b3760db622875da05acbe437c
# Wed, 20 May 2026 00:58:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 20 May 2026 00:58:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 00:58:53 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:09:42 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:09:42 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:09:42 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:09:42 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5748b9c3873e7576b494d1d035f8385ff895b681d07cacf1540b737c38c00c8d`  
		Last Modified: Tue, 19 May 2026 22:36:18 GMT  
		Size: 26.2 MB (26205831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0ef81f2c9cf2ac301c3a488feda9251ec1bd48cca684c431ddadd2aeb7dc20`  
		Last Modified: Wed, 20 May 2026 00:59:01 GMT  
		Size: 1.2 MB (1249138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33e854a74b74b642e6a6f4ba0ae96042fe18852e73b2b11bb79cf0ff25456d69`  
		Last Modified: Wed, 20 May 2026 00:59:01 GMT  
		Size: 12.5 MB (12482856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6510a87dba46f9fb9456466838879fd1cf2d71143d07743e2a2a9045da6f33a1`  
		Last Modified: Wed, 20 May 2026 00:59:01 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f987ce99c52bc47aeeb6f64e73b1137471421226212bacde013071530e41cea`  
		Last Modified: Wed, 27 May 2026 00:09:49 GMT  
		Size: 5.8 MB (5839865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:a45ec5b2edb42c553f286d26b1e9a00bc632be18bcfa0f0996135d5a945ec5ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165234 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a30589fb615a8885adb0f58725a4525aa5c56fdcd0448a7dee873a15f55f80da`

```dockerfile
```

-	Layers:
	-	`sha256:a7345184329643dc352a7f064e0010d69cf4318c503e70683f36ac0181b773a3`  
		Last Modified: Wed, 27 May 2026 00:09:49 GMT  
		Size: 2.2 MB (2155807 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa78180a61f8e4f6939be7fb2831e4204acf224fe6a052c63fdb2a70a0d94cfd`  
		Last Modified: Wed, 27 May 2026 00:09:49 GMT  
		Size: 9.4 KB (9427 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-trixie` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:571863f8dec3245afca560c44cb31ab7afbc5b1d9baab2d901e0a8ff2e314381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50039393 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd85d9fd163b3cdfb4382d7b0228345f64f03dd02cc9a3a0cb4d14315eec3b07`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:43:45 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:43:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:43:45 GMT
ENV PYTHON_VERSION=3.15.0b1
# Tue, 19 May 2026 23:43:45 GMT
ENV PYTHON_SHA256=d4d52ccfa1d727ef5235fbb7d70fa1dbacf10b8b3760db622875da05acbe437c
# Tue, 19 May 2026 23:51:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 19 May 2026 23:51:32 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 May 2026 23:51:32 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:10:49 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:10:49 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:10:49 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:10:49 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:cda3d70ae7d7c3d0b3b57a99a2085f9d93e919a846913dc6517a420b348c123d`  
		Last Modified: Tue, 19 May 2026 22:36:58 GMT  
		Size: 30.1 MB (30141919 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9067680695c61a588528cdce30779fa8ef16de26d6f51d7cd47368edcdd11b54`  
		Last Modified: Tue, 19 May 2026 23:51:40 GMT  
		Size: 1.3 MB (1274161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e6e64b6c8063b609986cacfa427fd315478f9e3f4b56ca93ffa1906f0bc30fe4`  
		Last Modified: Tue, 19 May 2026 23:51:41 GMT  
		Size: 12.8 MB (12783321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9b7c15a97388cb6800f0d755a8589d637707ccd37eb6b389ea5fd257759bb49`  
		Last Modified: Tue, 19 May 2026 23:51:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a311c2e1fef3db210f88ead6ee4e6be41957a1750802b74ce42c1ba661bfa359`  
		Last Modified: Wed, 27 May 2026 00:10:56 GMT  
		Size: 5.8 MB (5839743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:92505561d5211d2b7f18265984a59ab5223d043e5ac608238708b940cacb5ba2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2164127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8541ffaf7577b0f642e8209ed6236935fac1f4fa770705622b6ca1ce8d3e4b5`

```dockerfile
```

-	Layers:
	-	`sha256:e4134a4203b4f81d545f79a3adbec039c2628e5de43ef5ce88b58cf56359c385`  
		Last Modified: Wed, 27 May 2026 00:10:56 GMT  
		Size: 2.2 MB (2154659 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0ed14fa321938f20409190f22d693f138c3e873c0d75324451311673fcef0b97`  
		Last Modified: Wed, 27 May 2026 00:10:56 GMT  
		Size: 9.5 KB (9468 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-trixie` - linux; 386

```console
$ docker pull hylang@sha256:a4305bf57c33a0a32a529cc3be9b12aeead5b81cc38b1fdbd76988570ed6c8ff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.2 MB (51213093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:331d9d2aeee5f99bd0cc30390676584a7088350831e6c3a6b07ec97e295e5738`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1779062400'
# Tue, 19 May 2026 23:35:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 19 May 2026 23:35:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 19 May 2026 23:35:00 GMT
ENV PYTHON_VERSION=3.15.0b1
# Tue, 19 May 2026 23:35:00 GMT
ENV PYTHON_SHA256=d4d52ccfa1d727ef5235fbb7d70fa1dbacf10b8b3760db622875da05acbe437c
# Tue, 19 May 2026 23:55:27 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 19 May 2026 23:55:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 19 May 2026 23:55:27 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:10:41 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:10:41 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:10:41 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:10:41 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:05ced853378773a7168a29bae2e2f29a846f0a56beb260fd47a509a5e4ac966a`  
		Last Modified: Tue, 19 May 2026 22:37:18 GMT  
		Size: 31.3 MB (31295335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20abee171af05d7bf5d4b9f9e317c31e15f6dd96cc54e9e185cfe070c019d0ba`  
		Last Modified: Tue, 19 May 2026 23:55:34 GMT  
		Size: 1.3 MB (1297873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bfe3c7b31c2d4077bb0651b18b5a9474411b7f9c977194b1c8ed68a869bfe38`  
		Last Modified: Tue, 19 May 2026 23:55:35 GMT  
		Size: 12.8 MB (12779460 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92be0310dfae53383fe979a2b8cc115d55279870cc9acc86606aa3e09e200c43`  
		Last Modified: Tue, 19 May 2026 23:55:34 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ae2cf6abe298d3db3b3746c63f7bf8898d5fbbfa740fb5f8de6836d7550398`  
		Last Modified: Wed, 27 May 2026 00:10:48 GMT  
		Size: 5.8 MB (5840175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:b5daa25ec0856199e6ad51fb810cdc516d04aa48eabc0d4852f58c09673049b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2160778 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e2dfee9477daf65285f90ceeebc47471dbed0d5f906e6548072188989be5174`

```dockerfile
```

-	Layers:
	-	`sha256:56ac701f7a858fd74f76acf80f23233f6a3f595cefdaa348671162ea0ec28b87`  
		Last Modified: Wed, 27 May 2026 00:10:48 GMT  
		Size: 2.2 MB (2151514 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:48afb80418619d64f2a861ecac9896ba0bd6fbb3d418b95dc8a80bbdd728062d`  
		Last Modified: Wed, 27 May 2026 00:10:48 GMT  
		Size: 9.3 KB (9264 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-trixie` - linux; ppc64le

```console
$ docker pull hylang@sha256:fc27586bfe727322409ac4cd50ea390d3ef97b3acd195004889ea099913b06cc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (54038540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:31907dbc4ac59e3a664ef188e5ad9d0297c9f116ac2ef93385f7a832312e196e`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 02:52:51 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 02:52:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 02:52:51 GMT
ENV PYTHON_VERSION=3.15.0b1
# Wed, 20 May 2026 02:52:51 GMT
ENV PYTHON_SHA256=d4d52ccfa1d727ef5235fbb7d70fa1dbacf10b8b3760db622875da05acbe437c
# Wed, 20 May 2026 03:15:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 20 May 2026 03:15:35 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 03:15:35 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:17:51 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:17:51 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:17:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:17:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4dea3595b4b879a8f487420dc7e601b4fe79f2769fed7f891c99b52fea019c27`  
		Last Modified: Tue, 19 May 2026 22:37:58 GMT  
		Size: 33.6 MB (33600453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0bf42993f8ddcb8239db7203cca564245875086e6cd25916329cda86b12722c`  
		Last Modified: Wed, 20 May 2026 03:15:49 GMT  
		Size: 1.3 MB (1321276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5d5520afd1eb62b3c07cbcd4502b2d68086ad120b9b5d488fe3bae982923a9b`  
		Last Modified: Wed, 20 May 2026 03:15:49 GMT  
		Size: 13.3 MB (13276600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01cae083a6c51cc59bb93b4ec919a4199defa296ac12118b060c88557a59a45c`  
		Last Modified: Wed, 20 May 2026 03:15:49 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d453d28250c461b6ba896a56c1e3e372171aac048ea13a6db06be8f687e07dd`  
		Last Modified: Wed, 27 May 2026 00:18:04 GMT  
		Size: 5.8 MB (5839961 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:1e663de35a407b1b0a80e4d017ad8a4a249224ae7438801efa39ff12f9e94e93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2167328 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0ba878992e6f8c7355b95e88a0198f3386e1c52e3917abf79dc28bdc610f9db`

```dockerfile
```

-	Layers:
	-	`sha256:4b1d438a66a61010bc8cc31f3a03eb7b0d2e5c07980e5911f37c7f14aeac4fba`  
		Last Modified: Wed, 27 May 2026 00:18:04 GMT  
		Size: 2.2 MB (2157944 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f665d61cfb749a033ee48ba7f84875a59f114a78781c5405b3d07367eaef491f`  
		Last Modified: Wed, 27 May 2026 00:18:04 GMT  
		Size: 9.4 KB (9384 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-trixie` - linux; riscv64

```console
$ docker pull hylang@sha256:fbb35146b5cf7cc0fa64e5656b46792545e3da8b61154cb05a93955251d0f964
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48253995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:688cb8f8e496ff22abb37bd4191426012cb7408d65d76214fa933b8c6c9ba051`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1779062400'
# Thu, 21 May 2026 22:49:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 May 2026 22:49:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 21 May 2026 22:49:23 GMT
ENV PYTHON_VERSION=3.15.0b1
# Thu, 21 May 2026 22:49:23 GMT
ENV PYTHON_SHA256=d4d52ccfa1d727ef5235fbb7d70fa1dbacf10b8b3760db622875da05acbe437c
# Fri, 22 May 2026 00:30:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 22 May 2026 00:30:10 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 22 May 2026 00:30:10 GMT
CMD ["python3"]
# Thu, 28 May 2026 11:43:58 GMT
ENV HY_VERSION=1.3.0
# Thu, 28 May 2026 11:43:58 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 28 May 2026 11:43:58 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 28 May 2026 11:43:58 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:58bbe80817efb8a686096088d2ce9bfdbe0120904c9ea14d905c0e6d847d3ffd`  
		Last Modified: Tue, 19 May 2026 23:51:26 GMT  
		Size: 28.3 MB (28277598 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1903f08bd509a376c3c8569e83e6ede0ced718aecf8dc410b5f415b30e27b9ba`  
		Last Modified: Fri, 22 May 2026 00:31:18 GMT  
		Size: 1.3 MB (1261204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bf4546b29b8d45dd290e1d0b7604be49c0fc9322845d59465019b0fe41d7040`  
		Last Modified: Fri, 22 May 2026 00:31:20 GMT  
		Size: 12.9 MB (12874147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a223d7ab21649f4e1e0954c22221c03000ef6422cc0c32dde2773b4c299c9940`  
		Last Modified: Fri, 22 May 2026 00:31:18 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938f603f86b78697cc8832068f6252de0c256e67373525a3f942278a8df8fa5c`  
		Last Modified: Thu, 28 May 2026 11:44:59 GMT  
		Size: 5.8 MB (5840796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:7619bc1fc1ae50147092e7c1d452eec356126446de31963e4da8f46d48d08201
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157699 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e7ac083d8fcb33bf63fe9e1a2611a3ab5a446cd78b1b0c9dbc97122ec5d2c4`

```dockerfile
```

-	Layers:
	-	`sha256:2dec59bab62076d0e503d8e545862f0d8ba141243f44bebcdca638bac7f371c6`  
		Last Modified: Thu, 28 May 2026 11:44:59 GMT  
		Size: 2.1 MB (2148315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5fb8e966bce213279027e1c69b88da6462e38743315825dde8d9f3c4976a5acd`  
		Last Modified: Thu, 28 May 2026 11:44:58 GMT  
		Size: 9.4 KB (9384 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.15-rc-trixie` - linux; s390x

```console
$ docker pull hylang@sha256:97c3da68fecdbd21471c326e5b80a045bb6feba4ede6d1def21cc13024b5be74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49938068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:760fae05c3cbbc95203c0d22e8f755acd8209fe4aacd5ff936d753a1ee3753f1`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 18 May 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1779062400'
# Wed, 20 May 2026 00:54:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 May 2026 00:54:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 20 May 2026 00:54:09 GMT
ENV PYTHON_VERSION=3.15.0b1
# Wed, 20 May 2026 00:54:09 GMT
ENV PYTHON_SHA256=d4d52ccfa1d727ef5235fbb7d70fa1dbacf10b8b3760db622875da05acbe437c
# Wed, 20 May 2026 01:03:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 20 May 2026 01:03:09 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 20 May 2026 01:03:09 GMT
CMD ["python3"]
# Wed, 27 May 2026 00:13:29 GMT
ENV HY_VERSION=1.3.0
# Wed, 27 May 2026 00:13:29 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 27 May 2026 00:13:29 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 27 May 2026 00:13:29 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3a7bf300ab749fc8aaa5ec872160f889b9f1fd11db31bb5e8fe4d9ec131347b0`  
		Last Modified: Tue, 19 May 2026 22:36:59 GMT  
		Size: 29.8 MB (29845924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95c55e8da344ca0a9062ba67a8736995c67428322450bd2c4f2f5e9b30cbe939`  
		Last Modified: Wed, 20 May 2026 01:03:21 GMT  
		Size: 1.3 MB (1305778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0862981464b200ef50fd0005314a6eddf93adf8cb609f8fba613b64aa519f68b`  
		Last Modified: Wed, 20 May 2026 01:03:21 GMT  
		Size: 12.9 MB (12945954 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a8f4cbad6eccec5ee01450affe27feaec15b30df7308de36878fc8d487b7df7`  
		Last Modified: Wed, 20 May 2026 01:03:21 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2adb815c9aa498f808b73e9ba7681b99609ffceac7147850276a92554d0e9363`  
		Last Modified: Wed, 27 May 2026 00:13:49 GMT  
		Size: 5.8 MB (5840163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.15-rc-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:476379300e94109861e2081363e6ec29376f0bc0a2f9c3f3e2441b6ceb6cecdf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:77f3944e1e422e63962d41015e268969e6278647b77a302fd824fa4a53842394`

```dockerfile
```

-	Layers:
	-	`sha256:fdd5861a147523942e307f6172231735248defb463a437c4893651f7bccf22e6`  
		Last Modified: Wed, 27 May 2026 00:13:49 GMT  
		Size: 2.2 MB (2155792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72126ca7708e06024a98db84a5b6996f99935015611edb174aad860074c7ec2a`  
		Last Modified: Wed, 27 May 2026 00:13:49 GMT  
		Size: 9.3 KB (9316 bytes)  
		MIME: application/vnd.in-toto+json
