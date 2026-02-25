## `hylang:bookworm`

```console
$ docker pull hylang@sha256:eac8a8400ce4bcddd74d93cda73ee45f7e2f5df4d325aad8d010405e7a45b3b2
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

### `hylang:bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:641325005bfe5c5b7a8878fb88edc80bbe61e5d7483dfc076f71e0254160e54c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50187808 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9afdc3eeb0b294f98dd15d29e805a724a60add1e2a6f73eb5e68ffc983aa92c3`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:38:50 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:38:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:38:50 GMT
ENV PYTHON_VERSION=3.14.3
# Tue, 24 Feb 2026 19:38:50 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Tue, 24 Feb 2026 19:49:14 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 24 Feb 2026 19:49:14 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 24 Feb 2026 19:49:14 GMT
CMD ["python3"]
# Tue, 24 Feb 2026 20:20:36 GMT
ENV HY_VERSION=1.2.0
# Tue, 24 Feb 2026 20:20:36 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 24 Feb 2026 20:20:36 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 24 Feb 2026 20:20:36 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55bff9a44beb6d8b5d5a228c7808714cfac6fd628ce662296f38e4877b0f7613`  
		Last Modified: Tue, 24 Feb 2026 19:49:23 GMT  
		Size: 3.5 MB (3517368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:17532182a864ddb74f61e95888e05e8163fdca3a3c3610291e3f6aa866e25d6d`  
		Last Modified: Tue, 24 Feb 2026 19:49:23 GMT  
		Size: 12.9 MB (12916393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b9b1f95dff106904bc4c66deca9907faa78d7738b4633bd834fd6fdd5d038a6`  
		Last Modified: Tue, 24 Feb 2026 19:49:22 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79df41db5eb9a1502885adb2b8d77be1dfa1cdab35ee1d958355c752bc1a79c0`  
		Last Modified: Tue, 24 Feb 2026 20:20:43 GMT  
		Size: 5.5 MB (5517519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:f50434272d4b92eb631fdd1faf5b14350aafa9b5800a1f79db1e69f310db12b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2541259 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c2c510fdd945dfce7e2bed1c0c5569b971c35c042a510f425fd4d2284acbb34`

```dockerfile
```

-	Layers:
	-	`sha256:04c19103ea5a89c2983dcfabd6609741e58fd8c1f0fe00276b0b775a23a14c3d`  
		Last Modified: Tue, 24 Feb 2026 20:20:43 GMT  
		Size: 2.5 MB (2532000 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:79ba23f1765f3b5027faed95791c7cf19e59c328e29a001e87ea781a0057dbb7`  
		Last Modified: Tue, 24 Feb 2026 20:20:42 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:4c67a35cedb5ada9bbdf139a75dd641ee00f9232b4fb1292a3feb05fbaaae5d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46817639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ad48bd6d1066da9e2a288b2fb47eb0853e83de8f2fcd449d375f398d1bfa3cc`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:13:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:13:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:13:20 GMT
ENV PYTHON_VERSION=3.14.3
# Tue, 24 Feb 2026 20:13:20 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Tue, 24 Feb 2026 20:33:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 24 Feb 2026 20:33:58 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 24 Feb 2026 20:33:58 GMT
CMD ["python3"]
# Tue, 24 Feb 2026 21:52:04 GMT
ENV HY_VERSION=1.2.0
# Tue, 24 Feb 2026 21:52:04 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 24 Feb 2026 21:52:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 24 Feb 2026 21:52:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0355804b1a863607635e8e60f82ed6fec21aeb11cd0f281ea39f54208fab3bb7`  
		Last Modified: Tue, 24 Feb 2026 18:41:57 GMT  
		Size: 25.8 MB (25765637 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47013528c794733e45d74256288d655a2c7a94617416bbfeb8ecde3d205d2cd7`  
		Last Modified: Tue, 24 Feb 2026 20:34:06 GMT  
		Size: 3.1 MB (3091869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543ba93ab7a9951b51b97757ef2d614e981633668a6f0becac965ebee237bac6`  
		Last Modified: Tue, 24 Feb 2026 20:34:06 GMT  
		Size: 12.4 MB (12442082 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f90702c9e0051a57c0557f170c9ee63b56607ec39bb5e06ca0ea2bfca80499ac`  
		Last Modified: Tue, 24 Feb 2026 20:34:05 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bd1035dde882ce04181ec16d568723e081f95ce9f8004812d5273ed4170650e`  
		Last Modified: Tue, 24 Feb 2026 21:52:11 GMT  
		Size: 5.5 MB (5517801 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:f1e7cd268cfd55c03c849d5bd50e7c89690170321c3842222d00a7373a754487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2545215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba401d0fb7310477512980042998f3b352742754174d3b21914fab31358c8c70`

```dockerfile
```

-	Layers:
	-	`sha256:9e153e3a37506dabbc523e2e4db6a8b4efd52e49048d7fcd25b8302f7e982f36`  
		Last Modified: Tue, 24 Feb 2026 21:52:10 GMT  
		Size: 2.5 MB (2535844 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:78262b1d71bf88e319e04de65f08f9e71ebbf938127c46fcb9f551d708ba982f`  
		Last Modified: Tue, 24 Feb 2026 21:52:10 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:0f6445c2d06c8fb64582fbd8896a540381f1867d62f1ceb66c88b1f0426504b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44432867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02c34bd3e6b589161f6ae5330d2ffb9932607691b9d8801ab2677af30bb1b8f7`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 20:48:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 20:48:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 20:48:02 GMT
ENV PYTHON_VERSION=3.14.3
# Tue, 24 Feb 2026 20:48:02 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Tue, 24 Feb 2026 21:07:49 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 24 Feb 2026 21:07:49 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 24 Feb 2026 21:07:49 GMT
CMD ["python3"]
# Tue, 24 Feb 2026 21:58:08 GMT
ENV HY_VERSION=1.2.0
# Tue, 24 Feb 2026 21:58:08 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 24 Feb 2026 21:58:08 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 24 Feb 2026 21:58:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e991e6a97912f9d551e1c8d4ec0c8f2bf9f2df075f1c7862e9a2c3c9d650bc7b`  
		Last Modified: Tue, 24 Feb 2026 18:42:03 GMT  
		Size: 23.9 MB (23941398 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:43a46bf1f817622d69ca53bfa2921423ca7a655bac2059315470f846e00fd0a9`  
		Last Modified: Tue, 24 Feb 2026 21:07:56 GMT  
		Size: 2.9 MB (2926376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b31f3fc2a8c9d7d8fada2425f93e40850d22926535deaca35e495515d1ef802`  
		Last Modified: Tue, 24 Feb 2026 21:07:56 GMT  
		Size: 12.0 MB (12047146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c9d5513beadb193be195808ea8a05485f2ed7a6280ba771a87b4253880e178f`  
		Last Modified: Tue, 24 Feb 2026 21:07:56 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e500d0096a3e5f302103907b9efdb37e122b000bf83405caf2cf8a665996870`  
		Last Modified: Tue, 24 Feb 2026 21:58:15 GMT  
		Size: 5.5 MB (5517697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:5001398cfce45a83277efedd48b1c6a52941e9f1c5f3652b6180bb5dacf652ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2543648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fd6cb8dc14d47f823343d02e6191b03f0460051b71e8e191011d2bae8231c6c`

```dockerfile
```

-	Layers:
	-	`sha256:f3afd6b840413dff07ba19b9af2dc20faf4f9b5b156e5685bd24309f740f17ce`  
		Last Modified: Tue, 24 Feb 2026 21:58:15 GMT  
		Size: 2.5 MB (2534277 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d8a48395f6bfd81a95cd89a0540b99f53a5965890ec1916edacf3749947da483`  
		Last Modified: Tue, 24 Feb 2026 21:58:15 GMT  
		Size: 9.4 KB (9371 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:70c4f2f5f4d7076644c508196b6b9db3110aa8e2624c6950785780436b3a7df9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49788726 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97faed78513a1b9418cc96da75b2895ecba0597a501cc8b858509a19512b686c`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:44:13 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:44:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:44:13 GMT
ENV PYTHON_VERSION=3.14.3
# Tue, 24 Feb 2026 19:44:13 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Tue, 24 Feb 2026 19:57:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 24 Feb 2026 19:57:47 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 24 Feb 2026 19:57:47 GMT
CMD ["python3"]
# Tue, 24 Feb 2026 21:36:10 GMT
ENV HY_VERSION=1.2.0
# Tue, 24 Feb 2026 21:36:10 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 24 Feb 2026 21:36:10 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 24 Feb 2026 21:36:10 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4590fee761a858ff75078422c49c98b50811c1a002fba015f08e9a95274dd40`  
		Last Modified: Tue, 24 Feb 2026 19:57:56 GMT  
		Size: 3.3 MB (3349685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:888a3647af6ae6e1ce25e7f5cf96e7dbd237ff66b26907a3a44033e4d6caa291`  
		Last Modified: Tue, 24 Feb 2026 19:57:56 GMT  
		Size: 12.8 MB (12805098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ef3d9e065fbd944770166e89b4428fced2ba068c888f7803d57ff512c1bc9e`  
		Last Modified: Tue, 24 Feb 2026 19:57:56 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5c449be6c0538e16abecb355537e350acb50f40040c495957149337bb396b7b3`  
		Last Modified: Tue, 24 Feb 2026 21:36:17 GMT  
		Size: 5.5 MB (5517612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:fcd0b5acdc316edf38e9a8c7a2542d01c068132fca515d8eeeb1101cba1ae492
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2541723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5270cfeeea3c9d2e6cfb847fbcffd9ccea95dcd28b3469905629bc18b603c99d`

```dockerfile
```

-	Layers:
	-	`sha256:cfa5bd93246a16613694183f5f0cea069622ccef2f60bd6b1d783909a7f6d307`  
		Last Modified: Tue, 24 Feb 2026 21:36:17 GMT  
		Size: 2.5 MB (2532313 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:43d898b50e5ac9ce8f6e2aa3e3bd5743198597a063fab6b9dec6a6f1bc84a6c1`  
		Last Modified: Tue, 24 Feb 2026 21:36:17 GMT  
		Size: 9.4 KB (9410 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:bookworm` - linux; 386

```console
$ docker pull hylang@sha256:667918e9be5bb20c9be888eb4dc392ffa9af4f477c27adcbb35ef5061b3f1f59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.4 MB (51446151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:11740cc0572ef716c110c36cb6c4855d3d6a42ccdf02ad5b78efff487dcb3efd`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:35:28 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:35:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:35:28 GMT
ENV PYTHON_VERSION=3.14.3
# Tue, 24 Feb 2026 19:35:28 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Tue, 24 Feb 2026 19:49:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 24 Feb 2026 19:49:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 24 Feb 2026 19:49:07 GMT
CMD ["python3"]
# Tue, 24 Feb 2026 20:12:32 GMT
ENV HY_VERSION=1.2.0
# Tue, 24 Feb 2026 20:12:32 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 24 Feb 2026 20:12:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 24 Feb 2026 20:12:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bab6f574391274ab5dcfab8bda32d58ff3363c5f6d8b329979ceac5bd4afee6d`  
		Last Modified: Tue, 24 Feb 2026 18:42:08 GMT  
		Size: 29.2 MB (29221705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1c37349d76284c78b62d21180eb7133adca5148a1ac315ee24de60ddab0327f1`  
		Last Modified: Tue, 24 Feb 2026 19:49:15 GMT  
		Size: 3.5 MB (3518044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f2516a0d15a9c944438cd9c796e6c3358d68d7174be48b2fa5992d24522d3c`  
		Last Modified: Tue, 24 Feb 2026 19:49:15 GMT  
		Size: 13.2 MB (13188423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ce09df8d36903cca118924d05c90f9238bdd70d1542e315825a3fdf4389e8af`  
		Last Modified: Tue, 24 Feb 2026 19:49:15 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee12c98b56e324f6efe312bd613654dc29259962818518de7080b88347482a0f`  
		Last Modified: Tue, 24 Feb 2026 20:12:39 GMT  
		Size: 5.5 MB (5517729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:b08b7b153bb2a50354a3c1abd7b3137d1e58fac87982f80958909024db08a70a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dd621801fd35b60e24547127213b7b63020196428d9ceee22ee5d9374d40f49`

```dockerfile
```

-	Layers:
	-	`sha256:06e9ebd7b35aae6f2dea1a34fda32964b999679b3ce0cf6c6f0104ac69bb31f8`  
		Last Modified: Tue, 24 Feb 2026 20:12:39 GMT  
		Size: 2.5 MB (2529147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c099b7b683d21eef672196cc2cc809a5a0f1067ec219db8976bfbe0d6ab7e569`  
		Last Modified: Tue, 24 Feb 2026 20:12:39 GMT  
		Size: 9.2 KB (9207 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:7b5d3a532f7d56928a2aa5ee6940f73946682ea384a166efdb2c66f11d079c90
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.8 MB (54840988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35ebba674c73e06d850cdef597ef1012e887867cd1808476b1827b2390fff785`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 02 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1769990400'
# Tue, 03 Feb 2026 07:00:45 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Feb 2026 07:00:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Feb 2026 07:00:45 GMT
ENV PYTHON_VERSION=3.14.3
# Tue, 03 Feb 2026 07:00:45 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Wed, 04 Feb 2026 21:24:47 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 04 Feb 2026 21:24:49 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 04 Feb 2026 21:24:49 GMT
CMD ["python3"]
# Thu, 05 Feb 2026 01:34:39 GMT
ENV HY_VERSION=1.2.0
# Thu, 05 Feb 2026 01:34:39 GMT
ENV HYRULE_VERSION=1.0.1
# Thu, 05 Feb 2026 01:34:39 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 05 Feb 2026 01:34:39 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7910825c7ec7b68916beacd9af906d34dec10e730af19f67c87aa4e2ee440381`  
		Last Modified: Tue, 03 Feb 2026 01:12:56 GMT  
		Size: 32.1 MB (32068712 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56ae8754b0913212f675dbe39082cd4139a8d3f2eda5d83fad89de6a33a5f448`  
		Last Modified: Tue, 03 Feb 2026 07:26:25 GMT  
		Size: 3.7 MB (3722258 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:151fc1d8c1fec84425459b2c871efcab8f1d3238343ee1dfc7268b13a33e9005`  
		Last Modified: Wed, 04 Feb 2026 21:25:09 GMT  
		Size: 13.5 MB (13476958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3927e65e80c8b903cb44a7565d614faecd7f661e0352a1c4c267e1d834f5ef0`  
		Last Modified: Wed, 04 Feb 2026 21:25:08 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd224cf14c8e8dc46076a26c7076dc3374f0eb18301489260deaf88c39e8b51c`  
		Last Modified: Thu, 05 Feb 2026 01:34:54 GMT  
		Size: 5.6 MB (5572809 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:ac253f3381953a0fde2d3d72ce73097467385ad6e537120f0c2e6a3c1fd39709
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2545789 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fa150178c1fb721b81c5a777ac19082bda8cebadc617a30a7db06b6f02ad2cd`

```dockerfile
```

-	Layers:
	-	`sha256:5a7ae759a05731f2bf243f566ce340b29abe8d2a7da1980fd0ed28487e3029ae`  
		Last Modified: Thu, 05 Feb 2026 01:34:54 GMT  
		Size: 2.5 MB (2536462 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:70f3bb04196546b1b1d7fa381607d55f63ee25eeab2d81c61c8183c530e5c37a`  
		Last Modified: Thu, 05 Feb 2026 01:34:54 GMT  
		Size: 9.3 KB (9327 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:799703bb0a1030914c90bb3e6e4da3b6640738de5f99fcac685369db252c1504
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48340325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13301d13bd4a178576642bda01d52443e185482598083ade5f80d5d627680528`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 22:05:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 22:05:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 22:05:54 GMT
ENV PYTHON_VERSION=3.14.3
# Tue, 24 Feb 2026 22:05:54 GMT
ENV PYTHON_SHA256=a97d5549e9ad81fe17159ed02c68774ad5d266c72f8d9a0b5a9c371fe85d902b
# Tue, 24 Feb 2026 22:27:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libzstd-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 24 Feb 2026 22:27:31 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 24 Feb 2026 22:27:31 GMT
CMD ["python3"]
# Wed, 25 Feb 2026 01:19:33 GMT
ENV HY_VERSION=1.2.0
# Wed, 25 Feb 2026 01:19:33 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 25 Feb 2026 01:19:33 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 25 Feb 2026 01:19:33 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9bef76beebe598b8ff14a041376f35899cceaeb51a5810f860a721170c7db85e`  
		Last Modified: Tue, 24 Feb 2026 18:41:34 GMT  
		Size: 26.9 MB (26891524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0742ed0e9445733c35a806d7c59ff38710972138587c5032aef5cbe34a48d0c3`  
		Last Modified: Tue, 24 Feb 2026 22:27:52 GMT  
		Size: 3.2 MB (3182787 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7adae8711c0697d092c1f5f29137477cfa8315d05e65c41313728649061dcd`  
		Last Modified: Tue, 24 Feb 2026 22:27:53 GMT  
		Size: 12.7 MB (12747788 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73ab726913aefe5beb9f9ae6bef92f57ea4af2107dba76df4feddbf99dfd78c2`  
		Last Modified: Tue, 24 Feb 2026 22:27:52 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d32d372afcc78f3926670aa5a8569b5f83dde3ef7f50f9b2338cb0bc538ce30`  
		Last Modified: Wed, 25 Feb 2026 01:19:59 GMT  
		Size: 5.5 MB (5517976 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:10a783eff26e09cef9f0e42900b1bb6bc1c3614a95143074ce466cc32350f6ec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2538083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96aa90670070a415d86ada804945f98b01b3944741b72af81dcb6a238400b426`

```dockerfile
```

-	Layers:
	-	`sha256:cda45175a8f59bc7a2c92c41744f68c65f95cdf5c0cb1a1b9e2d06ced0be2ae3`  
		Last Modified: Wed, 25 Feb 2026 01:19:59 GMT  
		Size: 2.5 MB (2528824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28be76cae8a32abf2fc00a3eb2d748a73f0a7d6fa9b08aed31f914cbfe8aca36`  
		Last Modified: Wed, 25 Feb 2026 01:19:59 GMT  
		Size: 9.3 KB (9259 bytes)  
		MIME: application/vnd.in-toto+json
