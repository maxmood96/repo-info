## `hylang:1-python3.9`

```console
$ docker pull hylang@sha256:6bdf8345b7672dd1ee1d972dca47a3e1d2416dc39f8780c2023b233c093ede20
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

### `hylang:1-python3.9` - linux; amd64

```console
$ docker pull hylang@sha256:865d0f83922108b9b762cd1f6bc0990222ef52f8ad1129ea4558f54ffaa56925
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (51045424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:816e5048fb4b44bf4338457346fd92d3c9a4151ed0649cd2d68be8a66a708d01`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 09 Sep 2024 17:16:05 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.9.20
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HY_VERSION=1.0.0
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HYRULE_VERSION=0.7.0
# Mon, 23 Sep 2024 18:27:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 23 Sep 2024 18:27:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c0965d3919510b506d8856ebc050a96e996c7dae96e4fb420882dbe7e037e67`  
		Last Modified: Fri, 27 Sep 2024 06:06:08 GMT  
		Size: 3.5 MB (3511345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fdeeec85abbad3878f2008f9445f15a19a5a224d1b7e7715ac6b923072333e57`  
		Last Modified: Fri, 27 Sep 2024 06:06:09 GMT  
		Size: 14.7 MB (14738267 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:62a08b8dd4f53ad5493dabf2af00ccde91abb3771fb2187040bcf2fe94a7ced7`  
		Last Modified: Fri, 27 Sep 2024 06:06:08 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:573cae4583e2e85f38bec876bc75c8c5328a47aa9e24a37506394422f5d3faac`  
		Last Modified: Fri, 27 Sep 2024 07:04:57 GMT  
		Size: 3.7 MB (3669288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:6ddf322672d0bd867b9e0d870102128bc05f2ed13ca3a17055a6b2d8d3817f9e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466995 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986cc36d0aa657201b439c97a8edd4e5261ac38f03d4134c03f617bcd62c8492`

```dockerfile
```

-	Layers:
	-	`sha256:b79da688ad5d7873b589e0214298431a68185e475b30b9f0ea751e3d18bf80c8`  
		Last Modified: Fri, 27 Sep 2024 07:04:57 GMT  
		Size: 2.5 MB (2457853 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d24e17151a3899a0f245e09e56b32698abbf9f378e209a92778f9054aa2a3dd7`  
		Last Modified: Fri, 27 Sep 2024 07:04:57 GMT  
		Size: 9.1 KB (9142 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9` - linux; arm variant v5

```console
$ docker pull hylang@sha256:11098e03b75a5ffcb6c45a41ecd82c1dba98b3786937d96f11d4b54cf25958e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47914174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af9c277502412f0c8da2155c618b044ad470bbc1e126d371cf966a9f5aa3e0ff`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 09 Sep 2024 17:16:05 GMT
ADD file:91b876c600b7d3198bc98296224f6861440f56fcbd15a2188c95a8785b94061a in / 
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.9.20
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HY_VERSION=1.0.0
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HYRULE_VERSION=0.7.0
# Mon, 23 Sep 2024 18:27:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 23 Sep 2024 18:27:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:75a20c44e8becd141ba586ea413a1649251437a207502d4f8ad23d208f013e60`  
		Last Modified: Fri, 27 Sep 2024 03:21:44 GMT  
		Size: 26.9 MB (26887302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8075bb6924c8f332258acd98846e39160fce6f2c56f0f99cba1eadf1b2ae788`  
		Last Modified: Fri, 27 Sep 2024 15:04:52 GMT  
		Size: 3.1 MB (3081880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:940b1cbcefd12a1f45a30a658a26eb8f536e46713204dd3bb3f4155173afb5cd`  
		Last Modified: Fri, 27 Sep 2024 15:57:00 GMT  
		Size: 14.3 MB (14275225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faec14985e60b55848dfc96a3b56dece003faa5357c9837f83b214b2bd464552`  
		Last Modified: Fri, 27 Sep 2024 15:56:59 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacc1eccb84e82856bd2b7c5d6d413a36f514df0fa723e79500d157ffbe01442`  
		Last Modified: Fri, 27 Sep 2024 18:14:55 GMT  
		Size: 3.7 MB (3669519 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:5006bdb633bd857af598a2f51b56bcd7796ec60ae35702b82f34f7335fa5806d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2470554 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:081849879f72c240ab99459f624ac603ff39d85e292b66ce2bc48d9d98a49cf9`

```dockerfile
```

-	Layers:
	-	`sha256:653712365556c0ce1222edfd2649a59fed69acbfad560c7dfb03150f988726db`  
		Last Modified: Fri, 27 Sep 2024 18:14:55 GMT  
		Size: 2.5 MB (2461292 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ec0fc4cc008153da2b3fbd58fbfe8628803160cc9963a172a5ca2fbf20178947`  
		Last Modified: Fri, 27 Sep 2024 18:14:54 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9` - linux; arm variant v7

```console
$ docker pull hylang@sha256:8edc124ac0d417e6080750c5f0a9f291256b92f3c114647d32dd5cbac4574023
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.2 MB (45188910 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f415a9ad74b14dd0e48b6769048fa5266e48e18a42c430f8f97d0feaf66397`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 09 Sep 2024 17:16:05 GMT
ADD file:7eec8434e7851a0c9296426e66771b108dd584ea08a7e2aaec3ec3077c58bf89 in / 
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.9.20
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HY_VERSION=1.0.0
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HYRULE_VERSION=0.7.0
# Mon, 23 Sep 2024 18:27:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 23 Sep 2024 18:27:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2136499185ba9023c6db11bbc836b6c428da7969aa7db3ccaac576a10052c9ce`  
		Last Modified: Fri, 27 Sep 2024 05:17:12 GMT  
		Size: 24.7 MB (24718145 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9b9537205d3d033529058c3e264bb15c8fe23f0c53b9135fe96c602495550c84`  
		Last Modified: Fri, 27 Sep 2024 16:53:02 GMT  
		Size: 2.9 MB (2914358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a488f28544d52ebd73f87b997ff4d8a0014eae5618639d52eb751a1829f0f95b`  
		Last Modified: Fri, 27 Sep 2024 18:00:38 GMT  
		Size: 13.9 MB (13886706 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b269237a9788ecdb4bf93033aff4cfa7497767b3cf6e3f4de9113b61a3ef7548`  
		Last Modified: Fri, 27 Sep 2024 18:00:37 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f1527abe9c671ae96ac8278686b0a2fba7ba15b53ba455bff47bf852211cca9`  
		Last Modified: Sat, 28 Sep 2024 06:38:04 GMT  
		Size: 3.7 MB (3669453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:118fed2d297329fdadb842fe6abb42f976999935212ccdd1d0809ff3853a74c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2469421 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e52a96761b97677fb521abcc01623e6c692220dec37e7940635b6e1dac454414`

```dockerfile
```

-	Layers:
	-	`sha256:1cecaf1297144e17f63ac32258e7d68d3f0265d33319e504950fb9ca82464d9c`  
		Last Modified: Sat, 28 Sep 2024 06:38:04 GMT  
		Size: 2.5 MB (2460159 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3f801bd879c1d58ca5c2298df94c742b3eb66c2a524a2b6fb9482d7fd8f5035`  
		Last Modified: Sat, 28 Sep 2024 06:38:03 GMT  
		Size: 9.3 KB (9262 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:6d03131b5e029aead3b0128019f029889352adac61091b59ea90b7e951a021c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50868282 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a4adbef4f70241d9617568566a752c7e49349b9fd7041ba8107695c4e1e7104`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 09 Sep 2024 17:16:05 GMT
ADD file:28df1cb6a6576d40b5226851d0a6a76ffd5d1c94644ee441490b74a90f29f425 in / 
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.9.20
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HY_VERSION=1.0.0
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HYRULE_VERSION=0.7.0
# Mon, 23 Sep 2024 18:27:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 23 Sep 2024 18:27:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:14c9d9d199323cbf0a4c2347a8af85f2875c1f2c26a1558fd34dfca7a26cff22`  
		Last Modified: Fri, 27 Sep 2024 04:40:53 GMT  
		Size: 29.2 MB (29156369 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d847ad1879f2202660d37d9bedf1b8986116079d578b010e46b6917facf23dd5`  
		Last Modified: Fri, 27 Sep 2024 20:37:46 GMT  
		Size: 3.3 MB (3331450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d020595b077c82c862bcf7a0981420ba252567bf0fdbd292d1d2286fc599b8b`  
		Last Modified: Fri, 27 Sep 2024 22:06:57 GMT  
		Size: 14.7 MB (14710960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b3b6b7b048eccdc8b78e16eeaaaf992dcb37e174a030e00229050c094f174d2`  
		Last Modified: Fri, 27 Sep 2024 22:06:56 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da43f19f93603e9eb5caa5a1effd7687c98a98efcbb4ef56727c9a68085ae3a`  
		Last Modified: Sat, 28 Sep 2024 02:10:58 GMT  
		Size: 3.7 MB (3669254 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:a8959e66e35b37eea90554261dd0e87333468b94e46c0fe4bb578e96df28cf87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2467760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c13d2f4ec1a065810dc5f3953705239dcc3338aae7606b6219eb7ab99a7e7da3`

```dockerfile
```

-	Layers:
	-	`sha256:3a365defeaedb11fc4ee84a85828575001eb8672081599681d880d6b2d1c2e87`  
		Last Modified: Sat, 28 Sep 2024 02:10:58 GMT  
		Size: 2.5 MB (2458175 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:12bb1687acfaea352b23dc5ba4d3399d5a226ef7f9d8c2ab66b161783770f24d`  
		Last Modified: Sat, 28 Sep 2024 02:10:57 GMT  
		Size: 9.6 KB (9585 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9` - linux; 386

```console
$ docker pull hylang@sha256:a1a92faab620c8943d8f7c5cbbd7a9ff4e79b8c1fdabfe808d200068a8246f4f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52324487 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90b37020a87fcc4153f96019a948dc322d56335ffe6099c7e90e046beb50347c`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 09 Sep 2024 17:16:05 GMT
ADD file:7ad74dd13b6c84de2920c6d09de06e914d0b78ba06ae75260d6e6ff344a4b024 in / 
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.9.20
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HY_VERSION=1.0.0
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HYRULE_VERSION=0.7.0
# Mon, 23 Sep 2024 18:27:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 23 Sep 2024 18:27:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c953524ed27d53ce5e7d4e7487137789de73f4058e96b05284eefbcae1b47c26`  
		Last Modified: Fri, 27 Sep 2024 07:27:04 GMT  
		Size: 30.1 MB (30144216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2121b2de3c5cc284c51efb1b1df232714dc75352b21ee0ace4e996b8b61df2b1`  
		Last Modified: Fri, 27 Sep 2024 09:12:34 GMT  
		Size: 3.5 MB (3509570 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a695880ffdc803216af40c822afd9b2a19f95253c702bfbeee55bebb7e43b9a8`  
		Last Modified: Fri, 27 Sep 2024 09:12:35 GMT  
		Size: 15.0 MB (15001100 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f927668f76d900cd4c6c023c8d1db745f2d2048d5ad5e5deefc7037d803380e5`  
		Last Modified: Fri, 27 Sep 2024 09:12:34 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5a65f4667b12146a26c17f2b345a1b04861aad9099e73ff97d29f890f584740`  
		Last Modified: Fri, 27 Sep 2024 10:02:44 GMT  
		Size: 3.7 MB (3669352 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:589962f283674ec2a23c4e78a74922571916671d260cbf472fe6835e48d5a5bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2464017 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:396219324a52ceecce1342b85c35b98b451209d55ea7ef6d07bbfd60da02e830`

```dockerfile
```

-	Layers:
	-	`sha256:66c9aa7d4a735241b3850570713df01783c823551250eb5b9746053874100968`  
		Last Modified: Fri, 27 Sep 2024 10:02:44 GMT  
		Size: 2.5 MB (2454927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f5e1f320e2529e3069dde8efe4c90b3520769da708bcda2a51b34e8da0b0f18`  
		Last Modified: Fri, 27 Sep 2024 10:02:43 GMT  
		Size: 9.1 KB (9090 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9` - linux; mips64le

```console
$ docker pull hylang@sha256:86421de2e324d8177659bdaf34d921dc32db540df0041e453aae432c53711664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50222221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a01d3ddad055143b6978ff60c1e5be4a24def463ba4553fe95f0533297c8c5c`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 09 Sep 2024 17:16:05 GMT
ADD file:673970f358f62b6b095139e9647b41b9af839d4e01f7698755b040f471ff80b2 in / 
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.9.20
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HY_VERSION=1.0.0
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HYRULE_VERSION=0.7.0
# Mon, 23 Sep 2024 18:27:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 23 Sep 2024 18:27:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:75358c79454e0fed44aa25dd323536443b4a1230fc432aa226620e470d72cf5f`  
		Last Modified: Fri, 27 Sep 2024 09:11:36 GMT  
		Size: 29.1 MB (29124858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:071169cbd4bb8cf211b9d63239ea57efbaf0e00ce3e8658c671c9d1813cfc4e7`  
		Last Modified: Sat, 28 Sep 2024 11:05:36 GMT  
		Size: 2.9 MB (2906542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f04289a3a24bdeaf8867652bbbffb64188c255d7d6d83c8d607ddde59b117389`  
		Last Modified: Sat, 28 Sep 2024 11:05:37 GMT  
		Size: 14.5 MB (14520509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:307e18d6a402f9653d849d2d3568eab058c2f346f439382d3065f0700cd1b140`  
		Last Modified: Sat, 28 Sep 2024 11:05:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5cdf90e94795fa346dbee48c87214c3d553cb9a5f8f560c97dc680b3a0d610a`  
		Last Modified: Sat, 28 Sep 2024 20:43:48 GMT  
		Size: 3.7 MB (3670063 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:c4d73064e583af957460fddbe4c7224e94d739466cf15959b928841747b22f4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **9.0 KB (9037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c401476f589849f208222cc25527d28f8128b06888593be0fa7072d17687ec49`

```dockerfile
```

-	Layers:
	-	`sha256:4ec42ef9eff6b9e2088c198ea74419ad4fb8c8aefd28c3e5c639a846e46da128`  
		Last Modified: Sat, 28 Sep 2024 20:43:47 GMT  
		Size: 9.0 KB (9037 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9` - linux; ppc64le

```console
$ docker pull hylang@sha256:efaec2064a4b931fb2c6c8c0a8a70de80ae662c9963d10271df557a87f4c9cb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55828856 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f957e00197dcda3dd093d87ed558feb08b2935ef5e3554466bf61d5787fc9847`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 09 Sep 2024 17:16:05 GMT
ADD file:13ecda46acf717bc6e96c8ad429d6c14016514befca636a168655d0e5c9c4fbd in / 
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.9.20
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HY_VERSION=1.0.0
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HYRULE_VERSION=0.7.0
# Mon, 23 Sep 2024 18:27:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 23 Sep 2024 18:27:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c0db683897d16fe6e2869a351dbd5deac2268d5820d4b3c1cf93ec3bd69cafb5`  
		Last Modified: Fri, 27 Sep 2024 05:36:18 GMT  
		Size: 33.1 MB (33122163 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5bb5019efc480f5fb0358ab25a57f0034b24a330a06ae0ef55e7b136a109b2e`  
		Last Modified: Fri, 27 Sep 2024 23:36:50 GMT  
		Size: 3.7 MB (3712395 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:680523f84b5b1cb217d60b8026525b2a3186b638cc71352fb365aefd4b50f49e`  
		Last Modified: Sat, 28 Sep 2024 00:27:28 GMT  
		Size: 15.3 MB (15324555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31ebc5922c8c6997cc379b33727391cab51a7bc493bb93fedb8512a8078a828c`  
		Last Modified: Sat, 28 Sep 2024 00:27:27 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3946b4edd4094f74c2de370d1d1407a3d518e581e3bfb3af16fa5d1f08adbba6`  
		Last Modified: Sat, 28 Sep 2024 05:39:53 GMT  
		Size: 3.7 MB (3669494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:7c5bc718e66d1a6ab33b4ce881d62cdf8c4aaef149e847c5abf4485ec47d3220
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2471502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d7ffa04f56ab404f5d920928a7a322f9f36e674bffc8dd22de34db84bb75c94b`

```dockerfile
```

-	Layers:
	-	`sha256:139258ce6a29c843952e7cdc1fbf17840cf5f9d41d59fe7a35402d4dee5a42ed`  
		Last Modified: Sat, 28 Sep 2024 05:39:52 GMT  
		Size: 2.5 MB (2462280 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e367b94a696c622a070ac1058262c9c34a7304db3db6b09752ac620b0a5a392a`  
		Last Modified: Sat, 28 Sep 2024 05:39:52 GMT  
		Size: 9.2 KB (9222 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.9` - linux; s390x

```console
$ docker pull hylang@sha256:4d1a696e8178d0c24eb1e9d8ef91a877ba51001219898343666e6b247eaf5bcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48962847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2690c64e52e605e28903341488b9e6e240cdf7e8fc9b5d540a32093cd4144a1f`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 09 Sep 2024 17:16:05 GMT
ADD file:ee3c94adee604dbcaddf5d6c372b1f325a4443f66bd717dedf1ff7d9fb1ba116 in / 
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.9.20
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HY_VERSION=1.0.0
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HYRULE_VERSION=0.7.0
# Mon, 23 Sep 2024 18:27:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 23 Sep 2024 18:27:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:eca1e192de25fb56826ff7ed14b2e1532a49c27a08147a6249506eafd8ab4472`  
		Last Modified: Fri, 27 Sep 2024 02:47:22 GMT  
		Size: 27.5 MB (27490024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739ffdee8334417299439f55092bd31a485def6973bb5bbd65ae744f87a38325`  
		Last Modified: Fri, 27 Sep 2024 16:21:18 GMT  
		Size: 3.2 MB (3172548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fe1eaf6cfad33ddcc04a26daed4a94fb4a3a02278db0913ce014cc4c0ad9c80`  
		Last Modified: Fri, 27 Sep 2024 17:00:13 GMT  
		Size: 14.6 MB (14630642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:531902484767453464f63438e1a7e9eaf6724236d6624f012f92ada998e43823`  
		Last Modified: Fri, 27 Sep 2024 17:00:13 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3aa88c88813d040ac2a895777fbe4b901c2c40d54053468b45a6e3f698168027`  
		Last Modified: Fri, 27 Sep 2024 18:36:04 GMT  
		Size: 3.7 MB (3669384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:2a844db776f235c8f2c1147769c87d1bcea3054c5db858bd7f34d2303910010a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2466820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe2fe094a5a391036cbb58659c6d2048ba91fbb4dd03dfb7de8a0d620b4e97d`

```dockerfile
```

-	Layers:
	-	`sha256:7515ab71a3a7c399fcaad5675bc74510db291256cbb65ae78bae4bae8091679c`  
		Last Modified: Fri, 27 Sep 2024 18:36:04 GMT  
		Size: 2.5 MB (2457666 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a09e793b73c179c77467bc143216855f70fee7eba035b22c917b1027c609b8ce`  
		Last Modified: Fri, 27 Sep 2024 18:36:04 GMT  
		Size: 9.2 KB (9154 bytes)  
		MIME: application/vnd.in-toto+json
