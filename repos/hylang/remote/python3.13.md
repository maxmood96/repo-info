## `hylang:python3.13`

```console
$ docker pull hylang@sha256:79ddb0e502736dc9d77dcdb9cc553647b6eefeb505fb931a1aaa2665dde0fe92
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 17
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
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `hylang:python3.13` - linux; amd64

```console
$ docker pull hylang@sha256:8239bec81cd41a4627d16440502927ecfdc96e730cdbe5cdad883b7cfacec69b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (50037581 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8eafab06bdfd2e398d59cb310e3d8b6f313424cd55a1b56e17bfb5100bd7be73`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_VERSION=3.13.3
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7dcea32b97a8d11b6f8ba1d13f9a8dd7e31446045c39d80840fe08c393ee153`  
		Last Modified: Mon, 28 Apr 2025 22:16:48 GMT  
		Size: 3.5 MB (3511552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a1581175bc90f0247823da3e8a5c5c8f6d4f06815a8adf79029865fc0503a22`  
		Last Modified: Mon, 28 Apr 2025 22:16:48 GMT  
		Size: 12.6 MB (12593672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a0fab52da990205075e4a9b2962efc46e6b16b539b831243b989e70683b24c`  
		Last Modified: Mon, 28 Apr 2025 22:16:47 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73f7ec6cd38284137d51f6c7fd14a1ceac635b3af9cdaf45ed9f718ec24b2483`  
		Last Modified: Mon, 28 Apr 2025 23:11:57 GMT  
		Size: 5.7 MB (5704467 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:b30b2eac710c6b4c2af13fd18eaf90ad51c84017908dc79cb063c0918113945f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2431900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cca65488cd7db34de77157cfa3fcc15187f69c5350aa87ae9af26f8d7fd5686e`

```dockerfile
```

-	Layers:
	-	`sha256:330951a2bd37f69b03a8f77022d67f7c7c320ad5ae4f1d9d5095c1ff02822ea1`  
		Last Modified: Mon, 28 Apr 2025 23:11:57 GMT  
		Size: 2.4 MB (2420233 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a99205963a1d6224f399912dec6215dcc01acffe5afcfecdfaf1d576b7567b4f`  
		Last Modified: Mon, 28 Apr 2025 23:11:57 GMT  
		Size: 11.7 KB (11667 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; arm variant v5

```console
$ docker pull hylang@sha256:971cfcc5674b8d82ca37c9d282d5ff25d91ee8cb54e680669e489f793a603837
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.7 MB (46680378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55e465f4f2245a7689ab400b5638efac9c289192587a11187d416050d35eacbe`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1745798400'
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_VERSION=3.13.3
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3bc532ff9d2a2a12c6cfc746359843257a240960865aea7ecb10c71e0b93ec78`  
		Last Modified: Mon, 28 Apr 2025 21:07:56 GMT  
		Size: 25.8 MB (25757836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4b8d512a04fed6149402cb65a83d9920655b3fcbdaf346d2eca33197082bfab`  
		Last Modified: Tue, 29 Apr 2025 01:56:41 GMT  
		Size: 3.1 MB (3082287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65a521e64a7d65d691e7ef484919a6e07115bf51009bbd9210827892725ff0d`  
		Last Modified: Tue, 29 Apr 2025 02:16:08 GMT  
		Size: 12.1 MB (12135444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd380ea39272d16881ac31e9aea24c470dc38fe82bfd7f802023cdb1eaa8a5a7`  
		Last Modified: Tue, 29 Apr 2025 02:16:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:149e01d65c859eeea70083fb496ca9c891af45a019c7ac02a02b74d00266edb0`  
		Last Modified: Tue, 29 Apr 2025 05:20:07 GMT  
		Size: 5.7 MB (5704561 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:9a71fac479b4ac1c63764a1e1da8294ad5f2202624a0a219546c8a3b1486d3ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2435672 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0e8fa5f55c4b17ceba887c8013f8ac9a8e38d99584c9430a04db7fc4db66adb`

```dockerfile
```

-	Layers:
	-	`sha256:9e18656e1b5be121b738a2e169cf7041af1f9b2e83de1c65690ef4fe2616bf2c`  
		Last Modified: Tue, 29 Apr 2025 05:20:07 GMT  
		Size: 2.4 MB (2423833 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0ffc9afc0c5c8f677205af3f80b8aded493320be45b3bd245b348a0401b53d0`  
		Last Modified: Tue, 29 Apr 2025 05:20:06 GMT  
		Size: 11.8 KB (11839 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; arm variant v7

```console
$ docker pull hylang@sha256:b35c9ebe976ca632e0edac29825a280b264748e6f3ba3d691e3927f6f18855c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.3 MB (44334610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75d467bfef6f62df864b7ebd8cebc8367dfde14a2971e8293f062268313e060f`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1743984000'
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_VERSION=3.13.3
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:addc1be20d0979aa781d79a726ebf749adbc030186e63a44319274194e89cfa3`  
		Last Modified: Tue, 08 Apr 2025 00:23:15 GMT  
		Size: 23.9 MB (23937867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ff87432d7bca9497a2a3b7ba7cb157001ef0e6746189919b84276dd6e4f646`  
		Last Modified: Tue, 08 Apr 2025 10:21:32 GMT  
		Size: 2.9 MB (2914851 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:afb451ccb023e2bf6caf0ea20a9ed2128798c4129c0e17a00e6568be3ed86943`  
		Last Modified: Wed, 09 Apr 2025 06:01:38 GMT  
		Size: 11.8 MB (11762470 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df91e808e50f00d72cb121d2f73ebe6522b169a582e9af1cc07f2b8182bd826`  
		Last Modified: Wed, 09 Apr 2025 06:01:37 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f331289338f284fa7e7ba78b7ce82938997e20f998b52d6862c0588aa41ba21c`  
		Last Modified: Wed, 09 Apr 2025 12:06:48 GMT  
		Size: 5.7 MB (5719172 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:0b813465be561992f19d356c5d96e38c13f55735b6954833faa290f6eb1e14b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2434413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86ae2bf61eb79451a642fbf5b7818b40d820db22c0a34b62c36e21ce68ab1842`

```dockerfile
```

-	Layers:
	-	`sha256:10b9947ecaa12a69498605e7b98e6a147ae8dca9e5ff0018adb348893419553a`  
		Last Modified: Wed, 09 Apr 2025 12:06:48 GMT  
		Size: 2.4 MB (2422574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ca7babce77e840584f6ffa745bf1fa8eac6c3b2d5cc3fe2d79076db667e3505`  
		Last Modified: Wed, 09 Apr 2025 12:06:47 GMT  
		Size: 11.8 KB (11839 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:5bf8b63fb687ceff97066c69894c43ddfdea8c73dfdf7870edc2d929f70d577c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49602970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fcec8114da3014d8eb7b4a4787f70f7565d12ab505e6da9cbbe58eda22e6755`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_VERSION=3.13.3
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c3e456f51e049e4e783c232b11cc2d1e7d9e29bf290d3f3bdaa1ec0a3cd40c`  
		Last Modified: Tue, 08 Apr 2025 08:31:44 GMT  
		Size: 3.3 MB (3332064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c45306463e3deef37f6769f93d4730dd7bb72f1c709f7816c164cacf5f5afb0d`  
		Last Modified: Wed, 09 Apr 2025 02:37:01 GMT  
		Size: 12.5 MB (12485107 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbac49ccae39b8da9f98c7f37a8b7642f73e9bc94805c6cf30832d47fc5b3b30`  
		Last Modified: Wed, 09 Apr 2025 02:37:01 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f9bd1a67de3a6f01e30182cfa59b502d6282b47fab23650f1b9e1c55c417bb45`  
		Last Modified: Wed, 09 Apr 2025 13:50:44 GMT  
		Size: 5.7 MB (5719229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:f1f77c97c5424bee22ea5b4910819f7de19b522f0538abd57bf2034d40615fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2432556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c82790bff02ef0d5af762ba207649e439789d2355301e2500cf2fad4699bb05`

```dockerfile
```

-	Layers:
	-	`sha256:ec0bc90db0037a18d0aab7d506b3e3b9ce8b3adb021dd2b4a6815e7b39ef8c41`  
		Last Modified: Wed, 09 Apr 2025 13:50:44 GMT  
		Size: 2.4 MB (2420642 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bd146eb2483c173b74f86a8ebb55977a62223e1d539aa985b9b65ac0a431cadb`  
		Last Modified: Wed, 09 Apr 2025 13:50:44 GMT  
		Size: 11.9 KB (11914 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; 386

```console
$ docker pull hylang@sha256:2e9624e0b5fb8dab9faaa50d53c74ea130313deceb45d261573c1e5135356493
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51261943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:925b29a7edb26160ae2719f06ae896e5524cfdd476fbe5d10f1fbc16d73e26f7`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_VERSION=3.13.3
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94f7c872907b40c9e91ac516b77977af31384408f6b49c6393265bf2bebd0b8`  
		Last Modified: Mon, 28 Apr 2025 22:13:09 GMT  
		Size: 3.5 MB (3509870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9127b4c22bbe062aecf0251903c6ddede0647a9eafb1f35c22813f40402757e3`  
		Last Modified: Mon, 28 Apr 2025 22:13:09 GMT  
		Size: 12.8 MB (12836482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8e45b149b167ee1599b83186ec1c4659d099b712d2773f7171a350735fe97b7`  
		Last Modified: Mon, 28 Apr 2025 22:13:08 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:616e39d5e5c6eb7826ef21d839adfd4ef19fdf9c3be57f3fe8816b24f8f12b5c`  
		Last Modified: Mon, 28 Apr 2025 23:11:51 GMT  
		Size: 5.7 MB (5704475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:150e21951fdd71f5802457001be5d875c4743f39c9d42269d750c11d5541a149
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2428871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69528f01b3e6c90b2ea43a25236f02b357392612b637405ff2b0949456d15dec`

```dockerfile
```

-	Layers:
	-	`sha256:e8ead177b9cce09c8575956b3aa943776b4b968b7a9602927fe3260cac9c8cae`  
		Last Modified: Mon, 28 Apr 2025 23:11:51 GMT  
		Size: 2.4 MB (2417296 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b182de41b2cbba86b5079e4a0aa2ad4a06ccc6c673c41cfd7a127f924d49676a`  
		Last Modified: Mon, 28 Apr 2025 23:11:51 GMT  
		Size: 11.6 KB (11575 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; ppc64le

```console
$ docker pull hylang@sha256:daf1266faf12ea22d0935bedc4b8bfeb5867d02f0ca7e81df67fbcb304cb1bac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.6 MB (54623516 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69671aa3c15541995d8c3afc69456babaf653cf3726cb44dd29ec0a5feb745ea`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1745798400'
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_VERSION=3.13.3
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a53e75e229cd115b5249f6e60d40785f1bfff9e7ccc2df65672a6f67afd0e348`  
		Last Modified: Mon, 28 Apr 2025 21:22:04 GMT  
		Size: 32.1 MB (32068443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3d6c16baf714d9177bd1d08486c3ddb883b965702060f70a81c900cfc1ebd7d`  
		Last Modified: Tue, 29 Apr 2025 02:09:28 GMT  
		Size: 3.7 MB (3713691 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf87da31d8c17fc17331064f8b9412d5ae05a97e591e73b28a5ffd97bca0b0df`  
		Last Modified: Tue, 29 Apr 2025 02:27:41 GMT  
		Size: 13.1 MB (13136340 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ae8ddae915719f150cd1a799804ec3b099f915b72a4dd2c60ee5f8373602777`  
		Last Modified: Tue, 29 Apr 2025 02:27:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:68ceec82afef3ed9a5ee2e00d47bd14a6ecbdac5aba4cf2904c689209b9bf36b`  
		Last Modified: Tue, 29 Apr 2025 07:40:32 GMT  
		Size: 5.7 MB (5704793 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:f04991b2f75b5bcdd2d1474f8ec52a0e674c64b100b5823dacf9fa9221d737f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2436426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502ece863ab9af8a83bdbacf6826d9295d6a723633b99124225eabb8b78e0384`

```dockerfile
```

-	Layers:
	-	`sha256:93054cdcb2398e6ca419c8c28ddad9ebb0608d98d864c0f1c3a4d2c559dcac5a`  
		Last Modified: Tue, 29 Apr 2025 07:40:31 GMT  
		Size: 2.4 MB (2424643 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e7d73366616ec46e1e5e8924904f0edf1f413716ea07ca784fd946ff00f1762f`  
		Last Modified: Tue, 29 Apr 2025 07:40:31 GMT  
		Size: 11.8 KB (11783 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; s390x

```console
$ docker pull hylang@sha256:ad3ce4396c5476608f0648abf9de38caa8a294f838e9f850a62565ca5e2d1160
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48197763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef981b103ec6fe573cd8d5a80375c06bbb1062f65c80b6e340fe7093f9bcc4ae`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1745798400'
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_VERSION=3.13.3
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYTHON_SHA256=40f868bcbdeb8149a3149580bb9bfd407b3321cd48f0be631af955ac92c0e041
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["python3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2fb020f3caf1bc1659faa36e1595ae5ea71b8a94867ff23421b5ce8ca15030f4`  
		Last Modified: Mon, 28 Apr 2025 21:08:21 GMT  
		Size: 26.9 MB (26884867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e711f4af4984c210542ee4eacac85aa5e16905f1668fe313f8e2d2e05a596a16`  
		Last Modified: Tue, 29 Apr 2025 01:44:05 GMT  
		Size: 3.2 MB (3173146 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a6c1bba6c6d7b9eeceea3cea1741df76f02d70a06710838d7282d1cbc3ebec1`  
		Last Modified: Tue, 29 Apr 2025 01:44:06 GMT  
		Size: 12.4 MB (12435074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b594497a6dfdffc630f274c446a5371069e08da2d804bbf6854072dfe6dfcf8e`  
		Last Modified: Tue, 29 Apr 2025 01:44:05 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbcec8fed181ecaacbb04b85e81d33cd0cf352ce36930ec7dd97de8505c6bbb7`  
		Last Modified: Tue, 29 Apr 2025 04:42:44 GMT  
		Size: 5.7 MB (5704428 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:ba3a5e1cd552a85c46a689389bf3124c3501a5e34c811511b17bc66357441741
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2431615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272d954a124db1ff2052e4254ac60019111d05db9e9c7c456da53479ccdb3f98`

```dockerfile
```

-	Layers:
	-	`sha256:ee8b2b0138897441b589b3d427c27f2cfb1269605b464c429aa905a5cc1fe596`  
		Last Modified: Tue, 29 Apr 2025 04:42:43 GMT  
		Size: 2.4 MB (2419949 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bf111c4933f87cfdcbc5fca35bb5b455a78182ad98d1b943e878e2b134129686`  
		Last Modified: Tue, 29 Apr 2025 04:42:43 GMT  
		Size: 11.7 KB (11666 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - windows version 10.0.26100.3781; amd64

```console
$ docker pull hylang@sha256:174b92879b0a16df32aae6a613217dfab6a94a4a60641597bbadb293163c46b1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3463278144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:564475c52bf52c95ed8d82cbec89ded7cb883d0825fe1be289fa14a9b3645bef`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 03:24:17 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:24:18 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 18 Apr 2025 03:24:19 GMT
ENV PYTHON_VERSION=3.13.3
# Fri, 18 Apr 2025 03:24:19 GMT
ENV PYTHON_SHA256=698f2df46e1a3dd92f393458eea77bd94ef5ff21f0d5bf5cf676f3d28a9b4b6c
# Fri, 18 Apr 2025 03:24:57 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:24:58 GMT
CMD ["python"]
# Fri, 18 Apr 2025 04:14:33 GMT
ENV HY_VERSION=1.0.0
# Fri, 18 Apr 2025 04:14:34 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 18 Apr 2025 04:15:17 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 18 Apr 2025 04:15:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa470e9074390ec167bc3a82987154e4a32c3f9036403ffb17c9bd1d4514468f`  
		Last Modified: Fri, 18 Apr 2025 03:25:01 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40282cd09726b8ef3fbea2d34110de8a9e1bad741fabc6e1bb353a0ad01e363c`  
		Last Modified: Fri, 18 Apr 2025 03:25:00 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cae9ec3de4311b52eb1311d95bc9dd08df51a3e3b35092f60176068b22a88ff`  
		Last Modified: Fri, 18 Apr 2025 03:25:00 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d682e3ff50c67bc438d4018fc0cdd69cc831c44705a1b1a243060797b162772`  
		Last Modified: Fri, 18 Apr 2025 03:25:00 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf81aed8923009be145b3f559d2c48262182ba4348baca43996a7ef435cbe010`  
		Last Modified: Fri, 18 Apr 2025 03:25:06 GMT  
		Size: 59.4 MB (59400277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3452cbf9481cc5e1d82bb1f46849eb2f9b60f9ce7149c104ea4bacaa7e732c4b`  
		Last Modified: Fri, 18 Apr 2025 03:25:00 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a17c0c52ebf5a38a40e7acb89a83593076db8f94eb97ab30e01c5990bd6e150`  
		Last Modified: Fri, 18 Apr 2025 04:15:20 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e7e579ce15a6fd2caeefb2472eecece066c71a854048caa472acc3a2f960f93`  
		Last Modified: Fri, 18 Apr 2025 04:15:20 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cd4c33dd436e41604c7bda4cc0402f79df6373b5d8d3c02ccf968fad180c707`  
		Last Modified: Fri, 18 Apr 2025 04:15:21 GMT  
		Size: 8.7 MB (8706052 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f7c27f4032093e17af87e91359c4345d394299d07257679d0eb9d59d1a6dab`  
		Last Modified: Fri, 18 Apr 2025 04:15:20 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.13` - windows version 10.0.20348.3566; amd64

```console
$ docker pull hylang@sha256:ed14e65888d4513b287ca42387418c51c1ab27a6da14e670620e0a171cec4313
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2341338251 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbc95210c949ab9e5ac231565630ddc7c56760ba2893528ed53d9b2f6ea53dda`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:31:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:31:25 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 18 Apr 2025 03:31:26 GMT
ENV PYTHON_VERSION=3.13.3
# Fri, 18 Apr 2025 03:31:27 GMT
ENV PYTHON_SHA256=698f2df46e1a3dd92f393458eea77bd94ef5ff21f0d5bf5cf676f3d28a9b4b6c
# Fri, 18 Apr 2025 03:32:17 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:32:18 GMT
CMD ["python"]
# Fri, 18 Apr 2025 04:16:20 GMT
ENV HY_VERSION=1.0.0
# Fri, 18 Apr 2025 04:16:20 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 18 Apr 2025 04:16:54 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 18 Apr 2025 04:16:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:704650a8a28ca17ca00d876625fdc0f84dbcefad10ac48197742f584dbb72c8a`  
		Last Modified: Fri, 18 Apr 2025 03:32:22 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8e791e7ad1db1b287e759b5c5affb1ff58410f18d284bf535a37aca0a9f57bd`  
		Last Modified: Fri, 18 Apr 2025 03:32:21 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8753e93d7b7fe6bd41a177a320c9e1a7f29950a758f5cc8810f02ba4bf06573`  
		Last Modified: Fri, 18 Apr 2025 03:32:21 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22dc93b6b2ffe80d6091fb548574c227d03d7debb1bed35b6002ff6e23f6a1aa`  
		Last Modified: Fri, 18 Apr 2025 03:32:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:590a16674286b05d15af077c948073ebe416991eab4c3485573250cf16e5df0a`  
		Last Modified: Fri, 18 Apr 2025 03:32:25 GMT  
		Size: 59.2 MB (59215920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:693c223e2d8b0e7064074ef7e60c2a77e14491cfdddb41902d092ff32cdf8abf`  
		Last Modified: Fri, 18 Apr 2025 03:32:21 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf65f1b39f2dea80a221400790a95dd46996876a895e6acba95714aaed28f41`  
		Last Modified: Fri, 18 Apr 2025 04:16:58 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfbe754919a494d2377898a0cd5a8ffdf23bd4331ae238a2432cad9d16d33946`  
		Last Modified: Fri, 18 Apr 2025 04:16:58 GMT  
		Size: 1.3 KB (1344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1346bfc5d6ff28b08596941786c4a2abc54e4d1e9ef04e7a9c731896644d2e2`  
		Last Modified: Fri, 18 Apr 2025 04:16:59 GMT  
		Size: 8.5 MB (8529467 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b2d344651a50ae6a0dfd13273e2be8dd82180bc1c1d2be438c090b1d67ae17b`  
		Last Modified: Fri, 18 Apr 2025 04:16:58 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.13` - windows version 10.0.17763.7249; amd64

```console
$ docker pull hylang@sha256:90653b55da84a15825c461b6f00613bb39c546d6e1ac3693f2602c14e3a0aaa5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2230575912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:210692f5166ac17157c188d8a9baf67e2839fff85412a177e1ca09ef0be9b288`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:27:58 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:28:00 GMT
ENV PYTHONIOENCODING=UTF-8
# Fri, 18 Apr 2025 03:28:01 GMT
ENV PYTHON_VERSION=3.13.3
# Fri, 18 Apr 2025 03:28:02 GMT
ENV PYTHON_SHA256=698f2df46e1a3dd92f393458eea77bd94ef5ff21f0d5bf5cf676f3d28a9b4b6c
# Fri, 18 Apr 2025 03:29:31 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:29:32 GMT
CMD ["python"]
# Fri, 18 Apr 2025 04:16:30 GMT
ENV HY_VERSION=1.0.0
# Fri, 18 Apr 2025 04:16:32 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 18 Apr 2025 04:17:32 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 18 Apr 2025 04:17:33 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9633b53defe0dac299279815ed77f8d3d6c7ad5c3bb3d26aed3162ffc52e33ab`  
		Last Modified: Fri, 18 Apr 2025 03:29:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca59b04cc9b3686e468452237ced5c053c347e073c428ac8ce572b82d2851570`  
		Last Modified: Fri, 18 Apr 2025 03:29:35 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e2681ab4903568593a9c8fb3a50932b5049ca76b82c7a0f4c60f3fecbaa697b`  
		Last Modified: Fri, 18 Apr 2025 03:29:35 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24901045858d0bca98183ffe2409845fc6ef6ba939ff0deba8dc700c16a04c9f`  
		Last Modified: Fri, 18 Apr 2025 03:29:35 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9661ccf7d32211502d2b53423eb5b1100a83d3071361b3f9947e7e1acbb7313`  
		Last Modified: Fri, 18 Apr 2025 03:29:40 GMT  
		Size: 57.9 MB (57876206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a014ac89f9b82bffd01f03d55ded7bedb9432b73646a868be0a87537f5b59ac`  
		Last Modified: Fri, 18 Apr 2025 03:29:35 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47ac4ba91f25f388399a774c232fa6b8e664bf915ac7d30ff256eb173e74a4a3`  
		Last Modified: Fri, 18 Apr 2025 04:17:35 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94abe3f2fed3a0ab953b40929a7be4f84ebe812a11c8e4c00a1397e20ec5aa37`  
		Last Modified: Fri, 18 Apr 2025 04:17:35 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:798b66f79ba1c709eb954e348a395479615456669601085ec78a2534ea5d408e`  
		Last Modified: Fri, 18 Apr 2025 04:17:36 GMT  
		Size: 7.2 MB (7163525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:616849e39f777f23e0d2a49345253a5f04ea00220b8b6aea9d7c291d0f0e6b73`  
		Last Modified: Fri, 18 Apr 2025 04:17:35 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
