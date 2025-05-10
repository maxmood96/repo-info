## `hylang:1-python3.14-rc-bullseye`

```console
$ docker pull hylang@sha256:f0d218bba4fe41a5d94a308e33296af14e7559ae0ce7bdcc9dce38e18ceb95f8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:1-python3.14-rc-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:7cb64fec63ddd45d72c3aa811e53935b9b1cf2ebe917795593560911738cac2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.2 MB (55240835 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cf74bbe139e634da0e8a6e52e7f6a51af53440039ed99aa4baee9a4510db5fb`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.14.0b1
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=2ddd30a77c9f62e065ce648664a254b9b0c011bcdaa8c1c2787087e644cbeb39
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b09d1f67f19cd47e69b8a3566c2050a1681a1bf96a540a3b34751333b0d583c3`  
		Last Modified: Fri, 09 May 2025 23:50:57 GMT  
		Size: 1.1 MB (1076227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4a383fe0a2986740b3014c79a6d3ab0f64a8c5773d1ccc7a745dc5c001dab1f`  
		Last Modified: Fri, 09 May 2025 23:50:58 GMT  
		Size: 18.1 MB (18073186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cb2bf0485259919da01cf4ae071cd22346ea785841a468d52e86c171764e459`  
		Last Modified: Fri, 09 May 2025 23:50:57 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23dbdc3bcef99480ee7d14897014c388a08abe0ca0bb5a78307ef4e12679b7e7`  
		Last Modified: Sat, 10 May 2025 00:08:23 GMT  
		Size: 5.8 MB (5836569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:10a4e17c28ec1361fd4b6a4e2facee25bc948aabf71a1b167c9f4bf8a54f1229
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2721653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6161c545d4982f44c7a46611e873b73a642ce1b001752510b899c6bb45f4bb0`

```dockerfile
```

-	Layers:
	-	`sha256:f9f5b92fa5623b80cdfe998629b29089cd6a22b60a89725a65ecfac980201876`  
		Last Modified: Sat, 10 May 2025 00:08:23 GMT  
		Size: 2.7 MB (2713652 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f7b99674826d057b06c4a476093890d4cb0b368a87d065a77dea42453d18d4b3`  
		Last Modified: Sat, 10 May 2025 00:08:23 GMT  
		Size: 8.0 KB (8001 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:2347497647417f7ad037da32c4fb8231f1be8a705f0d5f28802a30ce51e95415
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48525036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:057460c392805ab60df1d46a71580abd56cef5694bd89cd366bc60a035fc5778`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bullseye' '@1745798400'
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.14.0b1
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=2ddd30a77c9f62e065ce648664a254b9b0c011bcdaa8c1c2787087e644cbeb39
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:93c17983cb6e26d53fe6219e705b968f8a22ae1b4cb559618bdff5ba501ae39d`  
		Last Modified: Mon, 28 Apr 2025 21:16:22 GMT  
		Size: 25.5 MB (25542427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:098cc8ed368864e2d50e9bc3938fb245bd25c463ac61e14a06c8c19d80e699ec`  
		Last Modified: Tue, 29 Apr 2025 06:39:19 GMT  
		Size: 1.0 MB (1041643 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59197249e69140ffd53329517d429d62faced6e69115fcc9e26e494ba8c9ab9b`  
		Last Modified: Sat, 10 May 2025 01:41:28 GMT  
		Size: 16.1 MB (16103745 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f542d85b6ff8202023f02f214d1e340cc6923a13b910d60bf0537dc6b47835ba`  
		Last Modified: Sat, 10 May 2025 01:41:28 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adbcab7ae520e95bc021b9382fa925a832454b704a572111fd97048e5244aada`  
		Last Modified: Sat, 10 May 2025 07:49:39 GMT  
		Size: 5.8 MB (5836971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:1c6678c892839e63b54b89c71fa3aa305f05fda754f3cae896df73fa922cda79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2723973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:70a94445f1da6c2d5ade8e2b8aad1efc690cd3cc90dbc34d2585a5c448d15226`

```dockerfile
```

-	Layers:
	-	`sha256:8fb65b1485580392e88098bb90957c3d04d9c962b7fe357cb9d370ca3c18e217`  
		Last Modified: Sat, 10 May 2025 07:49:39 GMT  
		Size: 2.7 MB (2715897 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7dcbf9f18f1160627530d1e683b56d2a1cbe7a4535ccf9fdb4f07e9361ed0a09`  
		Last Modified: Sat, 10 May 2025 07:49:38 GMT  
		Size: 8.1 KB (8076 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:57e73f9eca62170f647ea1a92cd890fea55285571482eeba49e42f477eb316b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.0 MB (52969475 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b082daa63608f50b642ec3f67a743f595d5e6870e6203348c1fc4010a48a4463`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.14.0b1
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=2ddd30a77c9f62e065ce648664a254b9b0c011bcdaa8c1c2787087e644cbeb39
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a8e820d8ec519539a3e949b94cbdee98218a5d49aea1dfb3a4e7fe4c0758e95`  
		Last Modified: Tue, 29 Apr 2025 22:25:36 GMT  
		Size: 1.1 MB (1064047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5609f3afa9c6e58bb306039177bf9e765cd9366a0fedbf495a6a114d0a466732`  
		Last Modified: Sat, 10 May 2025 00:35:54 GMT  
		Size: 17.3 MB (17323928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35e05b5c1c246a6feabfdcad1ceefc553a0981f2d8ff2868d24b84f826482685`  
		Last Modified: Sat, 10 May 2025 00:35:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d574ffd07fea33cc2d839a901a74fed7340a2370249d2d00bb5038cb9f52415c`  
		Last Modified: Sat, 10 May 2025 04:54:35 GMT  
		Size: 5.8 MB (5836606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:a0e14355ad8c95c5fa2a69f2c5c17f31921625f32c1267fc4bcd32ae91db18a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2722016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da759e62ddd0ef93242a1989228afa246f09bd3a1a91bd5297419decda1e8005`

```dockerfile
```

-	Layers:
	-	`sha256:865b485ed0deb8f6c1144c790df57f240830499ad0f6f90bf9062edc9277e12b`  
		Last Modified: Sat, 10 May 2025 04:54:35 GMT  
		Size: 2.7 MB (2713911 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b53b4ef328416cf8e210cd69be5492815388700ea0ceab2720bf723c347fac9e`  
		Last Modified: Sat, 10 May 2025 04:54:34 GMT  
		Size: 8.1 KB (8105 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.14-rc-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:cc7632fe4bcea9d16d9e19d8284b96aaf35e7a56658b54f9aa33a61211abfd9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.9 MB (55932615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f283d8b38f79f55f825b69d018cf32b539263dec91d16b6cdc3645aa5faaa59`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 28 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
# Thu, 08 May 2025 22:27:23 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_VERSION=3.14.0b1
# Thu, 08 May 2025 22:27:23 GMT
ENV PYTHON_SHA256=2ddd30a77c9f62e065ce648664a254b9b0c011bcdaa8c1c2787087e644cbeb39
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "$gnuArch" != 'riscv64-linux-musl' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Thu, 08 May 2025 22:27:23 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 08 May 2025 22:27:23 GMT
CMD ["python3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:73bb1b80ecf1f8784ad6f92a35120b6e2306657fc7e8cbaedca1f45900f3d746`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 31.2 MB (31187893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7002e43e282c0af3ddb12306e28f2829568ddde2c7477943f160835d108d7a80`  
		Last Modified: Fri, 09 May 2025 23:59:43 GMT  
		Size: 1.1 MB (1088778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92efa73758faf0528278a70c1b290fb40ff362ef2bd91e8aa8365cdf9060ec60`  
		Last Modified: Fri, 09 May 2025 23:59:44 GMT  
		Size: 17.8 MB (17818771 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42333451a78f3b454eee130f0dbcb1f0c975641c0cdb16a36735e0d396f14327`  
		Last Modified: Fri, 09 May 2025 23:59:43 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2a5d28919abf3be683e84a9577a89d1696aef2a63d0140075427907e5538295`  
		Last Modified: Sat, 10 May 2025 00:08:31 GMT  
		Size: 5.8 MB (5836923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.14-rc-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:c7f4053e27f8725da3a24bd4a05cff2faf480149d432bbd08e9d60d7ef752470
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2718733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f67f01a7b58b8c51cbb8405cd5082d57cbf94a40d69b8b6cbc13bc623b45905`

```dockerfile
```

-	Layers:
	-	`sha256:7cf81275700e2807ae31a8e19d1e592a5a7c032725cf193c58166da782c33844`  
		Last Modified: Sat, 10 May 2025 00:08:30 GMT  
		Size: 2.7 MB (2710764 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ee0802dcece880b5a685142656fb7580aef3c1972a9009a1122ecae12973acf4`  
		Last Modified: Sat, 10 May 2025 00:08:30 GMT  
		Size: 8.0 KB (7969 bytes)  
		MIME: application/vnd.in-toto+json
