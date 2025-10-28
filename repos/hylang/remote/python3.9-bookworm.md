## `hylang:python3.9-bookworm`

```console
$ docker pull hylang@sha256:5f03a2890c569367461de9ff274b9ed02a0c73ba101ca74b23526b0be294676e
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `hylang:python3.9-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:8574c55b1ac6807faac562c39150286615a06079cef5457fab8777d7c2b856cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50909887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eefc30a8e347c4246b384fbad1e8861ce88d53fa9ad8ba34a8caaf7bf16f197f`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 09 Oct 2025 17:36:41 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1760918400'
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 17:36:41 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_VERSION=3.9.24
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_SHA256=668391afabd5083faafa4543753d190f82f33ce6ba22d6e9ac728b43644b278a
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
CMD ["python3"]
# Tue, 28 Oct 2025 19:06:02 GMT
ENV HY_VERSION=1.1.0
# Tue, 28 Oct 2025 19:06:02 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 28 Oct 2025 19:06:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 28 Oct 2025 19:06:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:abe1fea375429ba91b23776f15f53da4ed790fa2b779b40d20f21e69bd66de5a`  
		Last Modified: Tue, 21 Oct 2025 00:19:19 GMT  
		Size: 28.2 MB (28228321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e24ec81a6071d319bf86b73e8ee38089e05a03f65dabbfb2db74b476a7d6f1c`  
		Last Modified: Tue, 21 Oct 2025 02:15:36 GMT  
		Size: 3.5 MB (3515852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c4b480485f861afce02881afe8a045f0c4ea34de348141991072b12981352bc`  
		Last Modified: Tue, 21 Oct 2025 02:15:37 GMT  
		Size: 15.4 MB (15448859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b161df0c2003425a26d2a8226ffda2829f9f5aa67f82d3751bf0612bc633f494`  
		Last Modified: Tue, 21 Oct 2025 02:15:36 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ddf33d28ea243fd847444ea04e1e0cde8a9f55cb482f763b1e12ab273fd8eba`  
		Last Modified: Tue, 28 Oct 2025 19:07:19 GMT  
		Size: 3.7 MB (3716606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:40cd412a7344799d83cb61e94b439b11feb2d2ff92e7d95e52c5a5960fa4ec97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2631036 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:208fe0f007273bd9da70bef22affb16dbba969a16736b739fbdc5ce074be7125`

```dockerfile
```

-	Layers:
	-	`sha256:742febb44d1af1ca8f879e7470bedf1057c9f4a6271063de8c841f7f4b5fbffa`  
		Last Modified: Tue, 28 Oct 2025 20:28:04 GMT  
		Size: 2.6 MB (2622954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca18ba9ee004ef84e9c065814e1e3bd6d7a35f36d3277c585f9ba9a0948fbad0`  
		Last Modified: Tue, 28 Oct 2025 20:28:04 GMT  
		Size: 8.1 KB (8082 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-bookworm` - linux; arm variant v5

```console
$ docker pull hylang@sha256:e1d1f9a0768c16efb91d50bd42b3167f4341c05d9ea7a87d3a36b220c3e9b542
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47445118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef971afca38583a91eb885de667936a609edb41d32ca834f0866e83a8b1a7653`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 09 Oct 2025 17:36:41 GMT
RUN # debian.sh --arch 'armel' out/ 'bookworm' '@1760918400'
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 17:36:41 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_VERSION=3.9.24
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_SHA256=668391afabd5083faafa4543753d190f82f33ce6ba22d6e9ac728b43644b278a
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
CMD ["python3"]
# Tue, 28 Oct 2025 19:08:02 GMT
ENV HY_VERSION=1.1.0
# Tue, 28 Oct 2025 19:08:02 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 28 Oct 2025 19:08:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 28 Oct 2025 19:08:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f982c9691d15a93fba0c1226ca85169d870439f0b6119d1ec61ec73d2a7dc8c3`  
		Last Modified: Tue, 21 Oct 2025 00:19:59 GMT  
		Size: 25.8 MB (25757495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce106c441870f718ab7f81b29f889217aca1ca0840cb4dc41bbac4ef66fea12f`  
		Last Modified: Tue, 21 Oct 2025 03:17:54 GMT  
		Size: 3.1 MB (3090710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9866723b1f9c25be1196623ebcda0f95e90e511be9f8ea748255cd74843a63c1`  
		Last Modified: Tue, 21 Oct 2025 03:17:56 GMT  
		Size: 14.9 MB (14879898 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3924520592fe3812a2faef98fdb16315cf30d6d994e0949754fc41e1dcabb5f3`  
		Last Modified: Tue, 21 Oct 2025 03:17:53 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e78791035ee96c972af7d46564e7cab4466494cf3b5878960a3e5fc759afd5e`  
		Last Modified: Tue, 28 Oct 2025 19:08:19 GMT  
		Size: 3.7 MB (3716766 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:de1aa4919d6055dc18cc9de59d2b33f3b1e0a12e7e0028b9b8c11c123c111032
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2634935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65f44856a0ba4cd0b05c975b7860be001528ecc7b3f5da24fec9ff72eea49656`

```dockerfile
```

-	Layers:
	-	`sha256:89e2f8fffff9ce703d2e22e8238be7fa0f6114548445a368d5e1af2d4386d8c8`  
		Last Modified: Tue, 28 Oct 2025 20:28:10 GMT  
		Size: 2.6 MB (2626774 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f666238da83a7ef68782028aad5211c869aca95c38ea5ce21a29b191a96c725`  
		Last Modified: Tue, 28 Oct 2025 20:28:10 GMT  
		Size: 8.2 KB (8161 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-bookworm` - linux; arm variant v7

```console
$ docker pull hylang@sha256:01336ba54aa08e1f8de210e64df5d9ea25c109a50d3f4c8181415c6fcdd3e9b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.0 MB (45049803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1708112978b2683f9fa45411eaa514f7c422b1156af296a525b17d4553ec7fa`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 09 Oct 2025 17:36:41 GMT
RUN # debian.sh --arch 'armhf' out/ 'bookworm' '@1760918400'
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 17:36:41 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_VERSION=3.9.24
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_SHA256=668391afabd5083faafa4543753d190f82f33ce6ba22d6e9ac728b43644b278a
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
CMD ["python3"]
# Tue, 28 Oct 2025 19:08:23 GMT
ENV HY_VERSION=1.1.0
# Tue, 28 Oct 2025 19:08:23 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 28 Oct 2025 19:08:23 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 28 Oct 2025 19:08:23 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4f520125372ffa3e5f64f19eebfdfce1c8314446e9e3ab2629f5c13cacbd8345`  
		Last Modified: Tue, 21 Oct 2025 00:20:18 GMT  
		Size: 23.9 MB (23934023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b7d6a9281e2b0d8fba6ebe487b82aa33108ec800f3708f0db5b3d34d4579cc71`  
		Last Modified: Tue, 21 Oct 2025 03:54:15 GMT  
		Size: 2.9 MB (2925444 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1892ed8961dace397efcca05cae38747c11771d2ad8ffaf26415715e3f9e1155`  
		Last Modified: Tue, 21 Oct 2025 03:54:15 GMT  
		Size: 14.5 MB (14473274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aaca26d509f9780af6d2c48a22cf2531166f97f63dcee9729db3b100bbaef84b`  
		Last Modified: Tue, 21 Oct 2025 03:54:14 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f90bab726ec4e200a0036476bc268c102bd20aeda8d99d7ec45e7bda19e22c9`  
		Last Modified: Tue, 28 Oct 2025 19:08:38 GMT  
		Size: 3.7 MB (3716814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:04e7c677b4673e0ae1b52e8c4ed711d5603f9f081e1dd323e482d7ebcb8c766d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2633385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f760a78801410d4965c800bbdcf09d6c0c8d88595a511a2446f4c27b766cdb`

```dockerfile
```

-	Layers:
	-	`sha256:ad8e9ccd8e1ffbfb6b0209526354bb4ceed0501089dc4742772f1bf2e08835db`  
		Last Modified: Tue, 28 Oct 2025 20:28:14 GMT  
		Size: 2.6 MB (2625223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fb019330230c130fd4d7941b01227abe3f2a1da19c3861a5cc4240339a2c35a2`  
		Last Modified: Tue, 28 Oct 2025 20:28:15 GMT  
		Size: 8.2 KB (8162 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:e3dbb0fa859bf6f04e689fd01961e7d8e0734ed79484613731649cf4d8975c4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50534775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0226d6f90f9c6d8ff550410a2e84a545a7f9a1a3908e682923de674a43dbbb5`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 09 Oct 2025 17:36:41 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1760918400'
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 17:36:41 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_VERSION=3.9.24
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_SHA256=668391afabd5083faafa4543753d190f82f33ce6ba22d6e9ac728b43644b278a
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
CMD ["python3"]
# Tue, 28 Oct 2025 19:07:44 GMT
ENV HY_VERSION=1.1.0
# Tue, 28 Oct 2025 19:07:44 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 28 Oct 2025 19:07:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 28 Oct 2025 19:07:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:21b7accdc53fc02b56a5c1cccd412be04189e5a5e674fd092ffbedc72596be91`  
		Last Modified: Tue, 21 Oct 2025 00:18:57 GMT  
		Size: 28.1 MB (28102190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d10f3e7b4a0634dd66f6a4ee8d59a75475b02a744ee78423d668a8e4de41571f`  
		Last Modified: Tue, 21 Oct 2025 02:22:40 GMT  
		Size: 3.3 MB (3349143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:691f6b1cfb46871276a1ebeef39dffe174633352612756223a7b197f52ae0807`  
		Last Modified: Tue, 21 Oct 2025 02:22:43 GMT  
		Size: 15.4 MB (15366373 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfc3b2ea427d134d67ea97e087f2f7416e883acb93a291624ae3c36fcdbec5fa`  
		Last Modified: Tue, 21 Oct 2025 02:22:39 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e7947d7f7caed6d2ad2e6b2c32955499d2ea5795433a33eeae0f1785a0e37ae1`  
		Last Modified: Tue, 28 Oct 2025 19:07:57 GMT  
		Size: 3.7 MB (3716819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:f2ad5f7804fe3d49af25aee52879f7c82ad0d526c48267b115b76399d48f3f7a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2631413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:089c6411ca9b49ad1e1858102d08ccdb26dd7f008d2ca0b3e2cc8522aba712ea`

```dockerfile
```

-	Layers:
	-	`sha256:09f53a4d08470c7ee1e829578a41f139995ecbb45cb7fa7870eb22ded7451956`  
		Last Modified: Tue, 28 Oct 2025 20:28:20 GMT  
		Size: 2.6 MB (2623227 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:066da2303f267830cb3d9109507d398083d07e0c9fa229c276bcbfc007152960`  
		Last Modified: Tue, 28 Oct 2025 20:28:20 GMT  
		Size: 8.2 KB (8186 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:a4ff4201b18badcfa1ba3c17c40782d2e36d41729e53b29c3e5c22e8badf91bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52140246 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:886f4d0e8f45a53c9bf8d8b452fce0e8ba2c1b400f03f9775ed3cf2605644ded`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 09 Oct 2025 17:36:41 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1760918400'
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 17:36:41 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_VERSION=3.9.24
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_SHA256=668391afabd5083faafa4543753d190f82f33ce6ba22d6e9ac728b43644b278a
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
CMD ["python3"]
# Tue, 28 Oct 2025 19:08:21 GMT
ENV HY_VERSION=1.1.0
# Tue, 28 Oct 2025 19:08:21 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 28 Oct 2025 19:08:21 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 28 Oct 2025 19:08:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9af2454a4583e64377534c708d303465636c37f3e4623cd4ad3bce1a1fedbfca`  
		Last Modified: Tue, 21 Oct 2025 00:20:33 GMT  
		Size: 29.2 MB (29209678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fe71a9237e50b07ff23adeb594e788a3145aadde43111cd6fad4e269ab7ee33`  
		Last Modified: Tue, 21 Oct 2025 02:16:18 GMT  
		Size: 3.5 MB (3516466 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c112d527c5ceadc89aeaa9405569fd2005c1cc606af91829a1b9138fc4422cdc`  
		Last Modified: Tue, 21 Oct 2025 02:16:19 GMT  
		Size: 15.7 MB (15697177 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90edf8f098a4b1805b433f77b96546c7eb5c60ab049893657212df58b69cadd4`  
		Last Modified: Tue, 21 Oct 2025 02:16:18 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8cd52fbe2ca4dc459abea64a1e7bee0a48910698237dbba26bfe0ef101c75fc`  
		Last Modified: Tue, 28 Oct 2025 19:08:33 GMT  
		Size: 3.7 MB (3716676 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:1db462c7707626486122dd6856c4bc9895bd0e6827208a66d82fcebda13ad7a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2628155 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a938d03f18f6328783fad1d5946591852b9a839a434d33bf38c502518ebb913`

```dockerfile
```

-	Layers:
	-	`sha256:8120990794ec538c6c160b82a214d51f95ca24838237681b0cf1d2d725ddab52`  
		Last Modified: Tue, 28 Oct 2025 20:28:26 GMT  
		Size: 2.6 MB (2620105 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ff621cdc62d2ee4fa89cf28a5f2e1c77b55419e23e7b8e4f3650ef7d282b7f61`  
		Last Modified: Tue, 28 Oct 2025 20:28:27 GMT  
		Size: 8.1 KB (8050 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-bookworm` - linux; mips64le

```console
$ docker pull hylang@sha256:e557b686fe99b9312115ab119dc7812632a95ad624e3bb452cf745f174a54e79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50286201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5c226359a3fc5b6c05b73ca466728e1b5b4635ba87869a5a036bab2588cd7ca4`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 09 Oct 2025 17:36:41 GMT
RUN # debian.sh --arch 'mips64el' out/ 'bookworm' '@1760918400'
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 17:36:41 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_VERSION=3.9.24
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_SHA256=668391afabd5083faafa4543753d190f82f33ce6ba22d6e9ac728b43644b278a
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
CMD ["python3"]
# Tue, 28 Oct 2025 19:09:20 GMT
ENV HY_VERSION=1.1.0
# Tue, 28 Oct 2025 19:09:20 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 28 Oct 2025 19:09:20 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 28 Oct 2025 19:09:20 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:67737a113ff8fe4461be953b475f1930d91e20d222e9a1f4e55ddb9bf4c2c6de`  
		Last Modified: Tue, 21 Oct 2025 00:19:57 GMT  
		Size: 28.5 MB (28513717 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa4c67a01f3172343ffe3b86db1f6cf88004c56d39001267eb62980d75ae2d31`  
		Last Modified: Tue, 21 Oct 2025 22:33:21 GMT  
		Size: 2.9 MB (2915711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0845a5c0c0850ab5a8351cbf003c67a73051f7525eb7117e62e440eed0666048`  
		Last Modified: Wed, 22 Oct 2025 00:10:11 GMT  
		Size: 15.1 MB (15139299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ab31cad3e277ae417339a124a90c92f97a6c599c2ea9bb77c4f562c60a75475`  
		Last Modified: Tue, 21 Oct 2025 22:33:30 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b24e59bded4b3571fdeaacbfcd06e95cde52561a527eb2efc2aed11725cc60ac`  
		Last Modified: Tue, 28 Oct 2025 19:09:51 GMT  
		Size: 3.7 MB (3717225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:2684d018492ca8d979ac7334983ffbc2de35cc56e96b5f37dc5400faa0f90208
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.9 KB (7933 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1794a1d2a0dce678ebd06ff10484a2c1591d2b0036a1d47a88a299c87a958aac`

```dockerfile
```

-	Layers:
	-	`sha256:26e6392550abe6251a71e819da6b1d685df5bb2021a798e7abd6bb503121e3c0`  
		Last Modified: Tue, 28 Oct 2025 20:28:31 GMT  
		Size: 7.9 KB (7933 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-bookworm` - linux; ppc64le

```console
$ docker pull hylang@sha256:8a31d73a7bda3d29b7b73d7f067e704c8715b1c1f15fcebc1ec84830668084dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55562977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a633bb939bf21c45364a2954e04c64b518a6746416cf8b03f2964222be883fd`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 09 Oct 2025 17:36:41 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'bookworm' '@1760918400'
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 17:36:41 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_VERSION=3.9.24
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_SHA256=668391afabd5083faafa4543753d190f82f33ce6ba22d6e9ac728b43644b278a
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
CMD ["python3"]
# Tue, 28 Oct 2025 19:38:49 GMT
ENV HY_VERSION=1.1.0
# Tue, 28 Oct 2025 19:38:49 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 28 Oct 2025 19:38:49 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 28 Oct 2025 19:38:49 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5a28d569c39dc949a4743122d7b5ec2d2e0664f1276c801bf984a711d80f2a1d`  
		Last Modified: Tue, 21 Oct 2025 03:26:43 GMT  
		Size: 32.1 MB (32068780 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d0c4b6ec612adb7e1d7e704a1e65bfb2f4954e5e33a947003c2c65e37bcef3`  
		Last Modified: Tue, 21 Oct 2025 13:03:37 GMT  
		Size: 3.7 MB (3721150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a5d7db6e492ba24073016c8674ab40a61e38b01a85ffd7f6a72e59171876566`  
		Last Modified: Tue, 21 Oct 2025 14:20:44 GMT  
		Size: 16.1 MB (16055802 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750c7f96e05fa5dea0fed540c2724cfbb60846d76bd4a2488e8d1732d5c772af`  
		Last Modified: Tue, 21 Oct 2025 14:20:43 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ffd93db82d77643ec1b134669899bf9f70564ab44fd398a2540b80ee3f93a0`  
		Last Modified: Tue, 28 Oct 2025 19:39:11 GMT  
		Size: 3.7 MB (3716996 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:2595b125df6a9db47fef95e421434b5aa4a0afb581dc45e94f500829728ac78f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2635585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35630c58d4f63900d93689ddc83a262628432d82449e63d32c6b2db21e268d95`

```dockerfile
```

-	Layers:
	-	`sha256:7ed26c56e966de28ebcb9791258f4e5cb86b38e8e7e169ef284249bd656fed42`  
		Last Modified: Tue, 28 Oct 2025 20:28:34 GMT  
		Size: 2.6 MB (2627460 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97e141391f92c13afefa6f8d05e5095f43263014a3c96e85534efc0d6edab986`  
		Last Modified: Tue, 28 Oct 2025 20:28:35 GMT  
		Size: 8.1 KB (8125 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.9-bookworm` - linux; s390x

```console
$ docker pull hylang@sha256:cbcab11486883e7909899669a14e14216a639242156f0de2e0e44ccbf4349a92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49021203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3afe2af62f5a70bd1ec62f08186579e5e2ee3c78ab7f21861559cfb8cd974200`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 09 Oct 2025 17:36:41 GMT
RUN # debian.sh --arch 's390x' out/ 'bookworm' '@1760918400'
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Oct 2025 17:36:41 GMT
ENV LANG=C.UTF-8
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_VERSION=3.9.24
# Thu, 09 Oct 2025 17:36:41 GMT
ENV PYTHON_SHA256=668391afabd5083faafa4543753d190f82f33ce6ba22d6e9ac728b43644b278a
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Oct 2025 17:36:41 GMT
CMD ["python3"]
# Tue, 28 Oct 2025 19:29:51 GMT
ENV HY_VERSION=1.1.0
# Tue, 28 Oct 2025 19:29:51 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 28 Oct 2025 19:29:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 28 Oct 2025 19:29:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:43b0f588b497b17691a3547afa4ae41853829cffde6930e6425ddae4a3f89278`  
		Last Modified: Tue, 21 Oct 2025 00:21:28 GMT  
		Size: 26.9 MB (26884356 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd0870b6a7cdee4395386021762639cf787d0374c1e379d3ee7e450f8daaa8b5`  
		Last Modified: Tue, 21 Oct 2025 20:04:14 GMT  
		Size: 3.2 MB (3181856 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26a126f72b68901a4abb7f9e59faf4eb11350102fea4041128fa635186cc8d7f`  
		Last Modified: Tue, 21 Oct 2025 20:59:53 GMT  
		Size: 15.2 MB (15238020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:90a516dd5c9159f8bc8c3cf18ef4004ebbabbad3e2402a4c78d7affa206fcf7d`  
		Last Modified: Tue, 21 Oct 2025 20:59:51 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:183ff325f89a27b975420d99bb59a394b9debdaf08dddf58c9a736b138559ee4`  
		Last Modified: Tue, 28 Oct 2025 19:30:18 GMT  
		Size: 3.7 MB (3716720 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.9-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:99345fcf63fc244029aa4b704ecd3c5028012cbb03d58ece2c6f45d06d96ceca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 MB (2627852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dec6864f65ae85b18460f095312515133f8e2a6a15e0122d5842be7fe069b179`

```dockerfile
```

-	Layers:
	-	`sha256:51d45bd89d13b2fdd5b5cc6166fe73802af3e1f88b102a18c5c2d81134368c26`  
		Last Modified: Tue, 28 Oct 2025 20:28:39 GMT  
		Size: 2.6 MB (2619770 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75f6e727b6e81b034aa805562550906d978aea7ed1f4a9b1c367c4990b6446f9`  
		Last Modified: Tue, 28 Oct 2025 20:28:40 GMT  
		Size: 8.1 KB (8082 bytes)  
		MIME: application/vnd.in-toto+json
