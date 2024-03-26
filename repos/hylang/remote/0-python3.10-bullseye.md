## `hylang:0-python3.10-bullseye`

```console
$ docker pull hylang@sha256:167fe464eaea8cca0d30c25443daf6613397b4bb343210ad14b2b965816121d1
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

### `hylang:0-python3.10-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:931321b328c7f1bf1c335e41cacf9aa21f5df199d983804c8b290455759179d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51555509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc703016c27cf5d420c0274362b3a8eef62be0a0e564f206e61573f523916d6b`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:3cd55ecee0ffd78be95dd5842ecd3171631aaccaae50fe41f6bf60ad5be6aaa9 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.10.14
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c0edef2937fa3b888b0cc3f9f5a4db00a1be6f297be5f057a77d738f91e675a0`  
		Last Modified: Tue, 12 Mar 2024 01:26:20 GMT  
		Size: 31.4 MB (31422489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:29ff364e54a5ec5ba946a5f20c50a8bcb5b8e25fca65999d411230bbc8c201c6`  
		Last Modified: Tue, 12 Mar 2024 12:55:35 GMT  
		Size: 1.1 MB (1076597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9de5504d78b00880aebe97ed2dac249dd0f1984851ff898ed951b5afafa51fae`  
		Last Modified: Mon, 25 Mar 2024 22:27:07 GMT  
		Size: 11.5 MB (11540981 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db62856c45f6705b5209c378c97bb0b9e6acd6b4ed3d9ec91e24a45bec7726f8`  
		Last Modified: Mon, 25 Mar 2024 22:27:05 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8578aade6e2b20764f8a7308b908ba02443f83de9b19a3861b837b6340ffe26b`  
		Last Modified: Mon, 25 Mar 2024 22:27:06 GMT  
		Size: 3.4 MB (3374000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec363a5277e1dbcabb6c2288be34ecb6f02a3e0bfeb475c7c674654eaf69355e`  
		Last Modified: Mon, 25 Mar 2024 23:11:28 GMT  
		Size: 4.1 MB (4141197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:b156f6dcedb70b9b272051d9538a50b0f0aaeaaff5fb63ac452a2e622eb25f91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692044 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd27b3953c14f2579d42ed42d0bbff3e7cb8fa5e4ef4b9d92b65758d8b05725b`

```dockerfile
```

-	Layers:
	-	`sha256:7641820f56844969dc843f299124cd51a811dd5d544e6fef46988a59709c4dec`  
		Last Modified: Mon, 25 Mar 2024 23:11:28 GMT  
		Size: 2.7 MB (2682895 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d58449949c98de4e0589cf9197d6e7d91dbc50ece9ee2878684eef753b39583d`  
		Last Modified: Mon, 25 Mar 2024 23:11:27 GMT  
		Size: 9.1 KB (9149 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-bullseye` - linux; arm variant v5

```console
$ docker pull hylang@sha256:4f7465cf0f61bdcee3b9dc3e4a1f9cf23f4867450d5248f765d435a551c6cdd9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.8 MB (48802970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eaba7023703792c27375f072fd60c56231a9d4503ae2a9d5b5e8ede3ea994607`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:90e7b77db704f73ce102dcbc0f6cbe5d778409a08ca0d29224ab736a76537669 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.10.14
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5f50de7913c8d45142222ead3575799095853dd5af08b7c42fe0f070c5947afc`  
		Last Modified: Tue, 12 Mar 2024 00:52:28 GMT  
		Size: 28.9 MB (28924563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9079355558ace9e1791c1fa4b575fb402fddbc59ac1d87d7c802c81e960bd17a`  
		Last Modified: Tue, 12 Mar 2024 07:54:54 GMT  
		Size: 1.1 MB (1059921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95702dc4032b58d521a7b674140bc8825a65e12ecaa4dd43851d0227bbd8edf5`  
		Last Modified: Mon, 25 Mar 2024 21:31:02 GMT  
		Size: 11.3 MB (11303402 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8280392fc8735a7ae86a1210877b56f721a77a468007f70ca662700714d72c42`  
		Last Modified: Mon, 25 Mar 2024 21:31:00 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2db7e86639d0fed9c7e2f1761e8a624830c4d750ff628b1fa5bb07e05ccbc4af`  
		Last Modified: Mon, 25 Mar 2024 21:31:01 GMT  
		Size: 3.4 MB (3373416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:025618a3eaf3d331c2a62f223f53d163d92153e0532845d52d4fdf7c57103b7e`  
		Last Modified: Mon, 25 Mar 2024 23:14:16 GMT  
		Size: 4.1 MB (4141423 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:19dd87000fb0be17dd6db6a94c08c64d197bde7084dc32ba8d4553273cadb700
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68da72301957219cc4c71eb427bb9e65d257e7767591d27c567cf31139794760`

```dockerfile
```

-	Layers:
	-	`sha256:c92e995b0e0c35a141a885d9b02cdb5f2aa5d0bd7f59074c173ee6129320f2e5`  
		Last Modified: Mon, 25 Mar 2024 23:14:16 GMT  
		Size: 2.7 MB (2683139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fed64ff0c1bc2224c212ed0b1530bbc82da9350dd8617fe6d95a1999ae339e7a`  
		Last Modified: Mon, 25 Mar 2024 23:14:16 GMT  
		Size: 9.2 KB (9219 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:f798a1c9f25a2374c0aa6b18da03e4c78a19adcfb7e280ab178b8554083bd5be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46022312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f856e70f2855708bcb0bc5aa527618656f472f257f262814d3b298dd0c6511aa`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:f0436b046c7a5f796efae4d2d2be5a99ad212807e4aa49fc8cc372a4c4c8c4b0 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.10.14
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5b16029f28c496dabb357a7310d24f957046a925411ccd44eca962c03f85e38e`  
		Last Modified: Tue, 12 Mar 2024 01:04:23 GMT  
		Size: 26.6 MB (26582714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b356a650895887f2dff41fd74528a07c2c12caf7a8a33e48c08a3440e538e5b4`  
		Last Modified: Tue, 12 Mar 2024 06:46:06 GMT  
		Size: 1.0 MB (1042014 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf674998c64959bab093de7b308a34fc7e61f1949e5b5b564fad2897d8e6f970`  
		Last Modified: Wed, 20 Mar 2024 21:48:18 GMT  
		Size: 10.9 MB (10882483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe20923874e0852d335e2c71211d76a91c48ef95173f9a3f7c978aada965851`  
		Last Modified: Wed, 20 Mar 2024 21:48:16 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d50a5600792e1d26e690e2b522e52438494df0f3b84099b5e70dfd493120133`  
		Last Modified: Wed, 20 Mar 2024 21:48:17 GMT  
		Size: 3.4 MB (3373548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2991e277486f0fa4db3e51a5e3b0775c7d345f6fc77e5c4a5b6af5054b34022a`  
		Last Modified: Wed, 20 Mar 2024 22:51:26 GMT  
		Size: 4.1 MB (4141308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:94c2630c5172b991249dac21ad9e23e4aa1b4eb004945ae9642325dcc62ff8fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c473ba2a9d245d02136d61a5d9b445b52be1bed1fb3c7a7356afda416112a888`

```dockerfile
```

-	Layers:
	-	`sha256:548382d956338402060f8807c7d3b6a8a3dd08007c4fe067fecadb66de9659fd`  
		Last Modified: Wed, 20 Mar 2024 22:51:25 GMT  
		Size: 2.7 MB (2685147 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f9497bec523630bb93485f57d312a7e0fbd54db89eae89c9a20f90a92de4c23d`  
		Last Modified: Wed, 20 Mar 2024 22:51:25 GMT  
		Size: 9.2 KB (9219 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:b82371622845903239f2192f28861ce25d29ef84fe82e9712b06b1c4bc421641
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50269182 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67aea800ea7e3057f3b818577427036f372102b2442b94ebf7b12f13178f2291`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:e5a8bb54381b61b31ee885b2841ecde6315a03685b0e7f33f736889d8e7768a2 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.10.14
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ef2fb7c49f69b9eefb25f02b600342129757e69bb130d53b98ba46ddde18effc`  
		Last Modified: Tue, 12 Mar 2024 00:49:32 GMT  
		Size: 30.1 MB (30071116 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:532fd75d6f3a4d86fea3efa8f4b8375dda1eb2ed1a0271860026d72f44ac98f1`  
		Last Modified: Tue, 12 Mar 2024 09:46:57 GMT  
		Size: 1.1 MB (1064441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fcaa843b80d0de937d96bfedd622d2c25e3a50dd34dc6cc09b0e7c8c42b8193`  
		Last Modified: Wed, 20 Mar 2024 20:58:54 GMT  
		Size: 11.6 MB (11618313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:de370f824ceb6ecba1ef16ed7df48d75955f350e66930c5977fe30320bd14e31`  
		Last Modified: Wed, 20 Mar 2024 20:58:53 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5298d297a87d2581f276e83441e4d33d99083e284e03dc233d8f1cf31ddb5b0e`  
		Last Modified: Wed, 20 Mar 2024 20:58:54 GMT  
		Size: 3.4 MB (3373716 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972a5df0f49191225ebe825a05b5e6aa2fd8471f4ca013c7f453f0f8c01944cf`  
		Last Modified: Wed, 20 Mar 2024 22:09:28 GMT  
		Size: 4.1 MB (4141351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:f199859073a80cde2f9ed58c50a3e0574e053df5163ebee02e1c6e21915470db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7534cf0b53615fe09c9e0e286ee57fa598daadab78c77e9911d10e8366e1bf59`

```dockerfile
```

-	Layers:
	-	`sha256:31185c59b6cc61c5af1954acacd9ba1a78c3baad9835f6504f4fc325f076a410`  
		Last Modified: Wed, 20 Mar 2024 22:09:27 GMT  
		Size: 2.7 MB (2683112 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6d23c70cdb6e98e52bf28f122c8d17edb4a1272770f080e79fd16e7ed59569b5`  
		Last Modified: Wed, 20 Mar 2024 22:09:27 GMT  
		Size: 9.2 KB (9159 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:beb2d286790d52d61e4cb96fbd51545a606c9985283085d4a859c4dc9c58e5d2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52681539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6014896a65139850798b44a515d664d905836372bf25577e6c3385f2fee13ab8`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:515cf6a96eea91239bc61e64b973eb555a9299d1053e3c6cb694d8bafa627086 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.10.14
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4276507bfa4980b432cd9334306e3335cf1bbc8e6dea45aad2ae9ec091223f03`  
		Last Modified: Tue, 12 Mar 2024 01:03:30 GMT  
		Size: 32.4 MB (32407589 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6a596234db507c62688be7cac378f73d76194322f31ece74297a2d67c14ff15f`  
		Last Modified: Tue, 12 Mar 2024 13:42:01 GMT  
		Size: 1.1 MB (1089173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e1711eef69fc1cf7b972aabfff15017595a11e61deaf47c4ac5da6ce5381f0`  
		Last Modified: Mon, 25 Mar 2024 22:39:30 GMT  
		Size: 11.7 MB (11669595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4bee76767da54e4391f9142153f76be30e1f621ed73b6e84d8ee42e0ff10e0`  
		Last Modified: Mon, 25 Mar 2024 22:39:27 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aec585ed2969059a761867fd4beeb74529741122ba104f27c5fee26af591c7cc`  
		Last Modified: Mon, 25 Mar 2024 22:39:29 GMT  
		Size: 3.4 MB (3373682 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4b595c7912bff48d2e061c99f53959b4f1e1cdc5cabb18582eb990085baeddc`  
		Last Modified: Mon, 25 Mar 2024 23:11:32 GMT  
		Size: 4.1 MB (4141255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:c584d34d4c29c1088c7f2b64a303d8ad4c4333ba33c807aa148e74de98211b1f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:241bec6ae2a04875a293d563284a063b57e6efbcca45f2666581a813212e9978`

```dockerfile
```

-	Layers:
	-	`sha256:46740c1788f099bac6b82738f9b09239f8b3171ebef12ccf4da585024c136b9f`  
		Last Modified: Mon, 25 Mar 2024 23:11:32 GMT  
		Size: 2.7 MB (2680003 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40329478d9163bb5d3726f561389fa7ab85b985d053ff622ff8d0dec5ff8377b`  
		Last Modified: Mon, 25 Mar 2024 23:11:33 GMT  
		Size: 9.1 KB (9118 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-bullseye` - linux; ppc64le

```console
$ docker pull hylang@sha256:42525e416a77510a0431d01980b95683e3c32f2307d0f5a2b1cab4e0711206d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55795453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:856ef2e31b0b032d1f432b1bee9dc34ecffbaedc752a3faacab50380d6fc469e`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:0964343f3addae20bae700c2e575d45b636c3fe2dfed3d7d4b51961f487dad44 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.10.14
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2717318882616811ceb12e643b0407ce22b67c750fd90122b7150a1571991bed`  
		Last Modified: Tue, 12 Mar 2024 00:38:55 GMT  
		Size: 35.3 MB (35298007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfe7dcabc3a4bcefa4e001bbf6473eb5ac1b77e85199941282c6e3ef7ce867d5`  
		Last Modified: Tue, 12 Mar 2024 14:38:06 GMT  
		Size: 1.1 MB (1095235 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b0ae47b78739bc54406b5ff0ed9d17456c0819a949630ba8046cc063d4d3f72`  
		Last Modified: Wed, 20 Mar 2024 21:26:56 GMT  
		Size: 11.9 MB (11886455 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:016b45ff97e356ae0124359ff334d1381a5ba73ae5564472830d0facb98821db`  
		Last Modified: Wed, 20 Mar 2024 21:26:53 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5cc28b9ad3cc0a253a78e63f13b3549a5195d8946795603f7c2deb91d0e8733e`  
		Last Modified: Wed, 20 Mar 2024 21:26:55 GMT  
		Size: 3.4 MB (3374215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:816a9f3a05045b925d0cafd9742488c76259986c2c220794fcdb6ff3ee55fb61`  
		Last Modified: Wed, 20 Mar 2024 22:03:47 GMT  
		Size: 4.1 MB (4141295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:d7f36873cce0f70fd3586a0f70c0b297762b67fcc0342180ac336b35565168e7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c16c93780f100f877c2de67bc8f92a9b8dc27725cee568d4576c66881b094b5b`

```dockerfile
```

-	Layers:
	-	`sha256:27ae34ea259adacc5c85f5896d735e9469e6a09f42a412c4bf902838331b6b5f`  
		Last Modified: Wed, 20 Mar 2024 22:03:47 GMT  
		Size: 2.7 MB (2687274 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2cc8d895182ba860a1af62e9834644cee08ae05609dee1da2eda4bd437470eb2`  
		Last Modified: Wed, 20 Mar 2024 22:03:46 GMT  
		Size: 9.2 KB (9187 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-bullseye` - linux; s390x

```console
$ docker pull hylang@sha256:c8fb85cab8181c140beac215928993ad029e3e7705fe937a9925614f19af9c3d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.7 MB (49719553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954e72157f359ae2d2c5f2a2074798371c929ea39b1c5119080d88509caea7cf`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:e121f5164f2335792d17befe564e4a4caf1dec33d5039c8245ce418144782215 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_VERSION=3.10.14
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["python3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:840335d52e6c781c13aaaed8df36659831a5cb0747048da9bf578dd19a02b30e`  
		Last Modified: Tue, 12 Mar 2024 01:21:45 GMT  
		Size: 29.7 MB (29660245 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88f3413722f739c4b7935b6e1a07231dd5ab107b48e54cf5c49c765475af556a`  
		Last Modified: Tue, 12 Mar 2024 07:57:44 GMT  
		Size: 1.1 MB (1076135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99195f638913ad61beaf7fb9b4d39dc14c49a6fc9de547b0dac8cc7f5a9adefd`  
		Last Modified: Wed, 20 Mar 2024 21:46:34 GMT  
		Size: 11.5 MB (11468195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d19fa48fb1775bdb64acf68fdbccadee0102d461f33709efc6bacd4ae1c8403`  
		Last Modified: Wed, 20 Mar 2024 21:46:33 GMT  
		Size: 245.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3777b4bdef73a5b4c075ea7ae31cf67f5db860a5bb4ab72c07ddf344dc795142`  
		Last Modified: Wed, 20 Mar 2024 21:46:34 GMT  
		Size: 3.4 MB (3373610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4792f1a27ed832ebb7a0df30c6597082b22ead362d8c0b1813eb765e369221c`  
		Last Modified: Thu, 21 Mar 2024 00:58:30 GMT  
		Size: 4.1 MB (4141123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:8247c317667c25c3401db522e887348da15ccb840a37e746bd11adc3ab82880a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2692223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90da0e4d85970432c9cc636e04df5cc764842596146327a6b52971f99b0b1403`

```dockerfile
```

-	Layers:
	-	`sha256:5abcfcde47c2fcebcaa80639e577455d8ae968a9402cb33b436fcba4bb3b8f11`  
		Last Modified: Thu, 21 Mar 2024 00:58:30 GMT  
		Size: 2.7 MB (2683093 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7fd7147e591c89c86c824e8f90aba1a9151cfbad09cbe61ea97bf1a00f300628`  
		Last Modified: Thu, 21 Mar 2024 00:58:30 GMT  
		Size: 9.1 KB (9130 bytes)  
		MIME: application/vnd.in-toto+json
