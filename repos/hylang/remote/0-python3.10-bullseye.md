## `hylang:0-python3.10-bullseye`

```console
$ docker pull hylang@sha256:dca4b82e1f6f67007da0f2d3aae7d3e5e31aa053e338fee5ea49a73a27c4f05e
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
$ docker pull hylang@sha256:8371d9bac70d31bb136558e7f5f77e59e8f0b261eda7fab3d766a074a07aa6df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51602650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b5544b93309a1b0a5d07cc34a98edcbde2c4cc817f17edefa948f9c0a2e9eac`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:574b112227f85a83f5d80d2523398640537475d2a56fa4c622397c466c0b552b in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Mar 2024 23:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_VERSION=3.10.14
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f7b75fe1f735933f47315080637abf01f87962d47f8636a07ff4535ed7a4a133`  
		Last Modified: Thu, 13 Jun 2024 01:26:15 GMT  
		Size: 31.4 MB (31434040 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fb769904474ac69efcbe3ca6529e9863496d804e7045697376496ab64885dc2`  
		Last Modified: Thu, 13 Jun 2024 07:24:18 GMT  
		Size: 1.1 MB (1078188 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710493390cdc3fd97157bfb1d202c0a18730656f8b07691c88b3f8e82b408474`  
		Last Modified: Thu, 13 Jun 2024 07:25:57 GMT  
		Size: 11.5 MB (11542552 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:750dde19623cb43c7f926ecc6646702102bbd7df98442acad59ee1f427de84d5`  
		Last Modified: Thu, 13 Jun 2024 07:25:56 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96feefb6843c2048a2a9672965d0f88cfce49fbb5af7102f119bb5bfa759ccc3`  
		Last Modified: Thu, 13 Jun 2024 07:25:56 GMT  
		Size: 3.4 MB (3374494 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:382b3cedef76fa479d9896923e76abf32918084e2406ad8f5ea24af8de09ae64`  
		Last Modified: Thu, 13 Jun 2024 18:32:32 GMT  
		Size: 4.2 MB (4173132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:6f45c7558e98bbf32b96af1a212f68c65de98f689c8a1a1748adaa5be0aff15f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0ed3f01855e30efb6dc0f98f84098987f9e780127903c0c45a7928715ee59e5`

```dockerfile
```

-	Layers:
	-	`sha256:a48e9bfd1583074c03d5b9821a5769311651c2ef87505dba2afbeca2bbe3b29c`  
		Last Modified: Thu, 13 Jun 2024 18:32:31 GMT  
		Size: 2.7 MB (2686184 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f4db94ba48a68d906cf44dabb71bfc0181d740c46967a9ec49f4ba3d03e064bd`  
		Last Modified: Thu, 13 Jun 2024 18:32:31 GMT  
		Size: 8.4 KB (8382 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-bullseye` - linux; arm variant v5

```console
$ docker pull hylang@sha256:40b358e894e2e01c0a8001fb7db0fd48ff1ed0da2451e7d1005b759ed95c3a26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48850848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0f124ba0a947f9649a167bfb6b158abd2ef4781bdd2e76c03aeea28a71c5dca`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 14 May 2024 00:48:50 GMT
ADD file:7a63cf2b5d16adf102fbd2452be219224667c4ea55981247f398a4a867ef96c4 in / 
# Tue, 14 May 2024 00:48:51 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Mar 2024 23:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_VERSION=3.10.14
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b6ea79e472ea80a508a2732ddeb0e19de51d3f0aaf8f0fd18c1cdd1c939d49de`  
		Last Modified: Tue, 14 May 2024 00:52:17 GMT  
		Size: 28.9 MB (28936721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3f0f3c3040a85d02b480f9db8c19a0aaf1facff8dcda11fe342738e98f422e7`  
		Last Modified: Tue, 14 May 2024 06:13:55 GMT  
		Size: 1.1 MB (1061248 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b076728b3fa257ea7d07c9312b9a1454af5b6c665518245444730fd61aa00816`  
		Last Modified: Tue, 14 May 2024 06:15:40 GMT  
		Size: 11.3 MB (11304814 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da5d98c0397d66fcea4a37b58561e54059506b795554d3f19929cf2a2d7904f3`  
		Last Modified: Tue, 14 May 2024 06:15:38 GMT  
		Size: 243.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6740cc2af67619673593cad9930163b5201c767c912915f87b1de15a29938df3`  
		Last Modified: Tue, 14 May 2024 06:15:39 GMT  
		Size: 3.4 MB (3374174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee5d1eeaa61249c42be51bdfc4011157329bfbfd0adf780f7a6388007331db21`  
		Last Modified: Wed, 29 May 2024 22:35:05 GMT  
		Size: 4.2 MB (4173648 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:0d971251ed448eaf21753413caa471b562fe05a0f6c499472d28ffd8aa5a7a8a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691704 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:469bc4f19ee07dda347c32de910aec05f5c7c4c0fb7100131709a744d400008e`

```dockerfile
```

-	Layers:
	-	`sha256:5aa4ff5560b9bc05ef955e4c73be3ec57fd410eb85cef4888e63482f5882ef70`  
		Last Modified: Wed, 29 May 2024 22:35:05 GMT  
		Size: 2.7 MB (2683301 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c5a6da0cc78061a360d24c4549f063cffa63ae7cecb33ff8679cb319432f2d28`  
		Last Modified: Wed, 29 May 2024 22:35:04 GMT  
		Size: 8.4 KB (8403 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-bullseye` - linux; arm variant v7

```console
$ docker pull hylang@sha256:da801d52e4bbbd6d87e4eca4fa1427fcb8cfef5073f6575155ae716aeb9dd997
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46069478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:538228b6974323c89e93503cdca748ad7c83051b3c795f71568f6141221f375b`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 14 May 2024 01:09:04 GMT
ADD file:b58f353e9d2a24c2c16ae0913b28705d3ecc439d60d82b5b4982780c59aae249 in / 
# Tue, 14 May 2024 01:09:04 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Mar 2024 23:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_VERSION=3.10.14
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a5c0b9604ae49509a7875b258d98493d63bdb4c1c27a70f2befa5fa4fcea1888`  
		Last Modified: Tue, 14 May 2024 01:13:30 GMT  
		Size: 26.6 MB (26594493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:266e3b43e28b4a4eb703026ed4e0c556ccd74d0464a7c2f4972661be125d2b30`  
		Last Modified: Tue, 14 May 2024 09:24:38 GMT  
		Size: 1.0 MB (1043219 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1f1edfd604e0004e72cbb4fd60d1aa2aedc768d328902d2330994870a10461a`  
		Last Modified: Tue, 14 May 2024 09:26:20 GMT  
		Size: 10.9 MB (10883686 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c099afb7433eaba83b766ce299297c2027cf2a4889670825a3abd0e844bed937`  
		Last Modified: Tue, 14 May 2024 09:26:18 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35d4246b43943bca8c08f2913350e834d1378b8bd0ba148290a9cd3d723d77bc`  
		Last Modified: Tue, 14 May 2024 09:26:19 GMT  
		Size: 3.4 MB (3374294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2599aea281b17704756f9b797acdf4b0752bf14985d8296b62f4db49c41fac21`  
		Last Modified: Thu, 30 May 2024 02:01:33 GMT  
		Size: 4.2 MB (4173542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:17a6da681e8974424b10c4ac124112cd86c5945fea19c0fdd22dca117128cc00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2693712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eea5f37addfda4b54f95afa281f3f472ec3cf7ed55793f7a904ac0e97f0a786d`

```dockerfile
```

-	Layers:
	-	`sha256:021bb42242582b197abd3aa061e85d1be8955be386aba8912ec69afadce49570`  
		Last Modified: Thu, 30 May 2024 02:01:33 GMT  
		Size: 2.7 MB (2685309 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:36eaed35723f03f262d0118694b698b0acacc6ddd1c0f109ec0df9de4609671f`  
		Last Modified: Thu, 30 May 2024 02:01:32 GMT  
		Size: 8.4 KB (8403 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:42d9c978b4b8992a4326a16ff7714666dcf9b0be965c6f36000e394f1945d162
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50320823 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c2ecfb73f9f926d07dcfded39009647d8991a791a55ba4172e0fe1f6d4701b6`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 14 May 2024 00:39:55 GMT
ADD file:0465ea1f0e8a2ee3e0f770c3b7f8e4a2b8719c624b440cabe7d7ecbe87200e7b in / 
# Tue, 14 May 2024 00:39:56 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Mar 2024 23:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_VERSION=3.10.14
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3a0037c67e2f4632684ea787f751ddb0b6af2b86113ab3b6859744b6eaf77e2f`  
		Last Modified: Tue, 14 May 2024 00:43:33 GMT  
		Size: 30.1 MB (30086908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:677786c8fd4e2bcbd58e895f7759126964177be319e2bfdc6a2d56fb732e6d59`  
		Last Modified: Tue, 14 May 2024 07:27:03 GMT  
		Size: 1.1 MB (1066080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a89d2b20543a9b0556062abdb7671c310e8bbf266d6e433b290a7c4115e390ce`  
		Last Modified: Tue, 14 May 2024 07:28:37 GMT  
		Size: 11.6 MB (11619886 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7f2da6e3ea9f46f67a787e718f540db0fe050eb69303cf74e28fb668e9d5da6`  
		Last Modified: Tue, 14 May 2024 07:28:35 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ef045fd094375ea5d1117bb745f42b25020226b0101413c29a4bddc9fd19b44a`  
		Last Modified: Tue, 14 May 2024 07:28:36 GMT  
		Size: 3.4 MB (3374482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20f22d2d04e69549b1265dc49694aec49b697abf8a9d75043eb59bc4d12a18fc`  
		Last Modified: Thu, 30 May 2024 14:47:42 GMT  
		Size: 4.2 MB (4173223 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:cc0f46aef1fe7ad0c859fe46816b1c2d35eec9df32a21d9d4877ebabf1b82fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0f38fe65b99ceb39c2a92aace1c09a65952bf2e9dd4f88741d157593e1af623`

```dockerfile
```

-	Layers:
	-	`sha256:5f5fc96dbbad1d4ccbd31a4ed5ccb21932cf136d01cd25f293d591074c9fc50d`  
		Last Modified: Thu, 30 May 2024 14:47:42 GMT  
		Size: 2.7 MB (2683319 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4eef08177f7c3384d538fd83d6ea50ce599d29f7f49c250afc4be5f9d17beb28`  
		Last Modified: Thu, 30 May 2024 14:47:41 GMT  
		Size: 8.6 KB (8647 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:2b53c3511a22a623019b3d6693ae370371f06db320c2a58acaed7232db4ffa82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52732864 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bbcaa63daa26da6d53fb39b5c75a2fd695bfc6a9ba9f17f977a3c4ee1250833d`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 25 May 2024 09:33:51 GMT
ADD file:ef80ad838dee1f170442a02f8d0808e624e7c317df766c49aec042c1f3ac4732 in / 
# Sat, 25 May 2024 09:33:51 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Mar 2024 23:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_VERSION=3.10.14
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:71e749b27156c50e0706f9267afd1ca9fb38d6272a353964948602fb62336fd8`  
		Last Modified: Thu, 13 Jun 2024 00:44:08 GMT  
		Size: 32.4 MB (32424179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a85a79839b9d40f1ee84eff63c7373f278dd95c5ed6a8727d1b64dbf38f642b0`  
		Last Modified: Thu, 13 Jun 2024 09:15:34 GMT  
		Size: 1.1 MB (1090932 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5217807c05976b7e01e3d45088f09c0b6679e0af24d47873e65642e0d424b3e`  
		Last Modified: Thu, 13 Jun 2024 09:17:23 GMT  
		Size: 11.7 MB (11669959 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa9751fdf7d0dc0e2641b43812cf2edb3093e154ca1c39954dc3a5d6717b0cc9`  
		Last Modified: Thu, 13 Jun 2024 09:17:20 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:462c9dc5107b661332a5800597da06c173dc4e4b93bd072bd43fbf331dad1287`  
		Last Modified: Thu, 13 Jun 2024 09:17:21 GMT  
		Size: 3.4 MB (3374158 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49400ac7263cbe1e5cf8fadf99f4781ade512923fa413e852d1bf620b38b7576`  
		Last Modified: Thu, 13 Jun 2024 18:32:36 GMT  
		Size: 4.2 MB (4173392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:08a223b6a080c9b5381fcf04232a60f82f4b81a4e73c608786989bfb05c5965e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7aba900ff8d80ab25357a6b539d90cc3a9891e24eb97c5c91d9844c77a9750e8`

```dockerfile
```

-	Layers:
	-	`sha256:778390ee9048699a4caf53fc0a4b252511a20b3b47baed3ed8b2745584d80a4d`  
		Last Modified: Thu, 13 Jun 2024 18:32:35 GMT  
		Size: 2.7 MB (2683290 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ce137d7141f69f13c5c88b17dd836ebf9fb30ef20cdc54d33ce1ca4d07d6c280`  
		Last Modified: Thu, 13 Jun 2024 18:32:35 GMT  
		Size: 8.4 KB (8353 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-bullseye` - linux; ppc64le

```console
$ docker pull hylang@sha256:298a50f52be1b58000a6abcb54491aa160f364f368064ccc54172626f837dbfc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.8 MB (55844087 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:151ce5feb0cc5af20552d704b64c7868b6cf929f3ac4e8121b488d0ad9a67e9d`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 14 May 2024 01:20:27 GMT
ADD file:7c74907a13931bf5f38ce8642536ee05738ba9d233424998c52fc548130034b5 in / 
# Tue, 14 May 2024 01:20:29 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Mar 2024 23:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_VERSION=3.10.14
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8fd45f8fa7e828bdb5dd8878febd6f367c5092a047db5f6ca094056a1b0c627c`  
		Last Modified: Tue, 14 May 2024 01:24:52 GMT  
		Size: 35.3 MB (35311159 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4e09fcd9c4184dfa956e22dfad7a592e9ea5e95df5d38d5e05eff8ba6c02a38`  
		Last Modified: Tue, 14 May 2024 04:48:15 GMT  
		Size: 1.1 MB (1096847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c13fded70d5d8f0d866e98f1b28550a5377b88f3201252f2e5d82056d7ad370b`  
		Last Modified: Tue, 14 May 2024 04:49:17 GMT  
		Size: 11.9 MB (11887508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40c700157212b3cc4241dd74cd56463f96710b9dc83bc53e7f4fe07b5168f628`  
		Last Modified: Tue, 14 May 2024 04:49:15 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2731f3676f3f8e555ae7764cf6331f361da2591b23302a0898c92c43dc5bbacc`  
		Last Modified: Tue, 14 May 2024 04:49:16 GMT  
		Size: 3.4 MB (3374921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:988361b6734af75dea9f34f6afd2a00e8564903cda7dc6dd908a674180d2baaf`  
		Last Modified: Thu, 30 May 2024 02:32:00 GMT  
		Size: 4.2 MB (4173408 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:50e8c6f50880cab87b52c2b49990739f26affd55541502344a4385a0f396a797
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2695807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3729fb86d76141aaa70e4a369a7e2e7592faae497ccb46e8530a6267b908d213`

```dockerfile
```

-	Layers:
	-	`sha256:7b20523efc7ddbda1cdb86a6f07b50fb27bc28a253141cc616e2569d8c5e4e53`  
		Last Modified: Thu, 30 May 2024 02:32:00 GMT  
		Size: 2.7 MB (2687436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f8a0a3a4274384f36da9b0e85012268ade5a7f720173db1eeff5024d6920a12`  
		Last Modified: Thu, 30 May 2024 02:31:59 GMT  
		Size: 8.4 KB (8371 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-python3.10-bullseye` - linux; s390x

```console
$ docker pull hylang@sha256:f70e654861c14c05b4e867f886c2513de513445c0583a50461f25e8338ac523b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49768552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:668272a397563abf82f51dc4938c23545ac5c70d21ef8b88f5989d15ffd1cbf5`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 14 May 2024 00:43:11 GMT
ADD file:bac230200161ff0b0332af3dc90dc1aba6bdeb875d95659699251b2af4eec8dc in / 
# Tue, 14 May 2024 00:43:13 GMT
CMD ["bash"]
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 21 Mar 2024 23:32:08 GMT
ENV LANG=C.UTF-8
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_VERSION=3.10.14
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--without-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_PIP_VERSION=23.0.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_SETUPTOOLS_VERSION=65.5.1
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/dbf0c85f76fb6e1ab42aa672ffca6f0a675d9ee4/public/get-pip.py
# Thu, 21 Mar 2024 23:32:08 GMT
ENV PYTHON_GET_PIP_SHA256=dfe9fd5c28dc98b5ac17979a953ea550cec37ae1b47a5116007395bfacff2ab9
# Thu, 21 Mar 2024 23:32:08 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version # buildkit
# Thu, 21 Mar 2024 23:32:08 GMT
CMD ["python3"]
# Sat, 25 May 2024 09:33:51 GMT
ENV HY_VERSION=0.29.0
# Sat, 25 May 2024 09:33:51 GMT
ENV HYRULE_VERSION=0.6.0
# Sat, 25 May 2024 09:33:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 25 May 2024 09:33:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:14d39445de105c0a8fe00b3899e9fdab7cdfbb3ff27c8b39dd9059f3264a4841`  
		Last Modified: Tue, 14 May 2024 00:48:06 GMT  
		Size: 29.7 MB (29673656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4ef64954ab5f27b054e5193a752fcac96a4a5f22e6b97b453de70c43772a3f5`  
		Last Modified: Tue, 14 May 2024 05:24:50 GMT  
		Size: 1.1 MB (1077688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:077ac79f24a2d0362584f96688c48933c536b7e86e45d38a5eb7b6e44fe6bfac`  
		Last Modified: Tue, 14 May 2024 05:26:14 GMT  
		Size: 11.5 MB (11469432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f43dd3f4b2e83113f1c6853ca72ae8074af07e7fe1eb191d4cd54b2dafec1f5d`  
		Last Modified: Tue, 14 May 2024 05:26:13 GMT  
		Size: 244.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86daa2245f7ec8c19d00c4f993be0edb81a0e49fefb1ea95c3d65502bd7c1c1c`  
		Last Modified: Tue, 14 May 2024 05:26:14 GMT  
		Size: 3.4 MB (3374307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84119c0a4b8073fdb135bcf5001e88b0d2b965c8ab6db867a68372c489776388`  
		Last Modified: Thu, 30 May 2024 00:52:26 GMT  
		Size: 4.2 MB (4173225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-python3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:6893b56da2b5f72d6bdcfee643d0533aa14eb66a1607e9e1aa68a38801035eb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2691587 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2a5a75e043b0bde2dc05648305eb340759f926677e302b3e320e97c22361d263`

```dockerfile
```

-	Layers:
	-	`sha256:54816177a9dc9592638da63bbc72f4c296dda34366558fe7678962a26f54826f`  
		Last Modified: Thu, 30 May 2024 00:52:25 GMT  
		Size: 2.7 MB (2683255 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59a93aea598894b4d2e95d7b9d09ca83d0664e429d0936efd763a2544ad25e69`  
		Last Modified: Thu, 30 May 2024 00:52:25 GMT  
		Size: 8.3 KB (8332 bytes)  
		MIME: application/vnd.in-toto+json
