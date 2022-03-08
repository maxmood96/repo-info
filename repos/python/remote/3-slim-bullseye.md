## `python:3-slim-bullseye`

```console
$ docker pull python@sha256:908e1ac05c08f1d52c7dd0eefd127c0f85351aa2798c3170b691e672ac1e965b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 7
	-	linux; amd64
	-	linux; arm variant v5
	-	linux; arm variant v7
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `python:3-slim-bullseye` - linux; amd64

```console
$ docker pull python@sha256:bb41290f37c7c96cfddff5bb3f2ad8bddbf499a94cdcc07916c7363e42612fbf
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46299037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91da1efb265c9cc4e493e44005cb5b075082821ff19ee344ae00e540296c779c`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 01 Mar 2022 02:13:29 GMT
ADD file:d48a85028743f16ed927507322e3e3beee187fbfadd0b781d4b89de197c64b5b in / 
# Tue, 01 Mar 2022 02:13:29 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 02:21:10 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Mar 2022 02:21:10 GMT
ENV LANG=C.UTF-8
# Wed, 02 Mar 2022 02:21:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 02:21:23 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 02 Mar 2022 03:33:04 GMT
ENV PYTHON_VERSION=3.10.2
# Wed, 02 Mar 2022 03:48:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 02 Mar 2022 03:48:31 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Wed, 02 Mar 2022 03:48:31 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Wed, 02 Mar 2022 03:48:31 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 02 Mar 2022 03:48:31 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/2caf84b14febcda8077e59e9b8a6ef9a680aa392/public/get-pip.py
# Wed, 02 Mar 2022 03:48:31 GMT
ENV PYTHON_GET_PIP_SHA256=7c5239cea323cadae36083079a5ee6b2b3d56f25762a0c060d2867b89e5e06c5
# Wed, 02 Mar 2022 03:48:43 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 02 Mar 2022 03:48:43 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:f7a1c6dad28192bd417b78079d6ddc03cbca6d5ea46bba12769b235b6353c00c`  
		Last Modified: Tue, 01 Mar 2022 02:19:23 GMT  
		Size: 31.4 MB (31366396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c59ec44e08abbd071efa42d226c5bdb8396ee193a53e02c4232296ef855372`  
		Last Modified: Wed, 02 Mar 2022 05:58:33 GMT  
		Size: 1.1 MB (1075916 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d87688ad24ef168e105068280a296bbb7e70647be7fb64a788b69e35271a216e`  
		Last Modified: Wed, 02 Mar 2022 06:00:22 GMT  
		Size: 11.2 MB (11219380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0db4d52e41af9884b9b4048c06a7276acdf22602b80b7cf1de28c8fe3b1a38e0`  
		Last Modified: Wed, 02 Mar 2022 06:00:20 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021faa0f7dcc8e31282d53c140b0e629c628409be3e9c4f10abd31c2874c08b8`  
		Last Modified: Wed, 02 Mar 2022 06:00:21 GMT  
		Size: 2.6 MB (2637110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-slim-bullseye` - linux; arm variant v5

```console
$ docker pull python@sha256:587283f011b74b0c91eae710010429828a5aa5b859b5212441c38f4fbf258e8a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.4 MB (43415424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0e906bebcaca55479df93df337c46b0f0d797e32a1920aa41751d2ee911924e`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:53 GMT
ADD file:eb61ee802e5118b26e1fec2c7fc58e34de0de54a5fd47dc6318c11a039ef528f in / 
# Tue, 01 Mar 2022 02:02:53 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 17:32:08 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 17:32:09 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 17:32:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 17:32:28 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 01 Mar 2022 19:23:48 GMT
ENV PYTHON_VERSION=3.10.2
# Tue, 01 Mar 2022 19:52:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 01 Mar 2022 19:52:57 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Tue, 01 Mar 2022 19:52:57 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Tue, 01 Mar 2022 19:52:58 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 01 Mar 2022 19:52:58 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/2caf84b14febcda8077e59e9b8a6ef9a680aa392/public/get-pip.py
# Tue, 01 Mar 2022 19:52:59 GMT
ENV PYTHON_GET_PIP_SHA256=7c5239cea323cadae36083079a5ee6b2b3d56f25762a0c060d2867b89e5e06c5
# Tue, 01 Mar 2022 19:53:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 01 Mar 2022 19:53:31 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:4aa6e26b4dfdac27e5b5e15b7ebf4366149755a79dd653a5b68d9d93dd94c695`  
		Last Modified: Tue, 01 Mar 2022 02:18:33 GMT  
		Size: 28.9 MB (28909528 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dfb765ddcf868286aae388a54f7f7a5dee147972844794d14ff82c63e4205e2`  
		Last Modified: Wed, 02 Mar 2022 00:14:04 GMT  
		Size: 1.1 MB (1059088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9f43742f7b7ebeec9e699644c9085914d992bd8314bc5a7b4c0b6909b18b918`  
		Last Modified: Wed, 02 Mar 2022 00:14:11 GMT  
		Size: 10.8 MB (10809774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d1cc7766fbdb041f67463fbf9cff413b3644b96bdc26666748fe62b20b622ce`  
		Last Modified: Wed, 02 Mar 2022 00:14:04 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40d5252b02c3f1947e44e2fb4949fcd72404b125e661c1376ec0207f9e8e76ef`  
		Last Modified: Wed, 02 Mar 2022 00:14:06 GMT  
		Size: 2.6 MB (2636799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-slim-bullseye` - linux; arm variant v7

```console
$ docker pull python@sha256:50b423904f340bac927f3e5b1755cbca668ae2e1a1374e920bbe7cad76767b87
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.6 MB (40567943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:659d4f8038d3d72988622bd87dcb6a7cea52b1bbdb35f6e14581e01a61a775d9`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 01 Mar 2022 02:02:56 GMT
ADD file:c6b519323fd1fa09b9f8c8608778872e8fa6208cb0b42aaccdef4479a469f5f4 in / 
# Tue, 01 Mar 2022 02:02:57 GMT
CMD ["bash"]
# Wed, 02 Mar 2022 04:01:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 02 Mar 2022 04:01:07 GMT
ENV LANG=C.UTF-8
# Wed, 02 Mar 2022 04:01:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 02 Mar 2022 04:01:24 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 02 Mar 2022 06:52:15 GMT
ENV PYTHON_VERSION=3.10.2
# Wed, 02 Mar 2022 07:27:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Wed, 02 Mar 2022 07:27:02 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Wed, 02 Mar 2022 07:27:03 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Wed, 02 Mar 2022 07:27:03 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Wed, 02 Mar 2022 07:27:03 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/2caf84b14febcda8077e59e9b8a6ef9a680aa392/public/get-pip.py
# Wed, 02 Mar 2022 07:27:04 GMT
ENV PYTHON_GET_PIP_SHA256=7c5239cea323cadae36083079a5ee6b2b3d56f25762a0c060d2867b89e5e06c5
# Wed, 02 Mar 2022 07:27:31 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Wed, 02 Mar 2022 07:27:32 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:59dbb2ac3829352dd707e28e037734c9fbdef5b03aea31e3929ddcead949afee`  
		Last Modified: Tue, 01 Mar 2022 02:19:09 GMT  
		Size: 26.6 MB (26565105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0155a4d1b528faafa9afc56ec5962f56891dc2d8347a05530a298c9e9e4172bc`  
		Last Modified: Wed, 02 Mar 2022 12:54:42 GMT  
		Size: 1.0 MB (1041342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1047d3f790ebd9ea95640dc8fc0e37a5d46333a8f09713a2c9b882d32fed53e`  
		Last Modified: Wed, 02 Mar 2022 12:58:14 GMT  
		Size: 10.3 MB (10324515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a75b31469ab21b858fcd0323f9e86488005dc5429edef6f30c50e2c0c3ea0a9`  
		Last Modified: Wed, 02 Mar 2022 12:58:07 GMT  
		Size: 238.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e8b623bf429913afc999450f4c0c254ebecd338065627bfd0fe753b0760dc2`  
		Last Modified: Wed, 02 Mar 2022 12:58:10 GMT  
		Size: 2.6 MB (2636743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull python@sha256:b5d7918de29b66d1110b0f364869a168e6258d21d590969293a97b654134799e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.8 MB (44817424 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9e68febf1bc8a024de359953ebda6bd45088c377e5d64225b3fd253d9b793b6`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 01 Mar 2022 02:11:29 GMT
ADD file:9816c9c29627693c34afda4fa5e1a5e8a0f5aa3c5d5cfd920a4d89c77aab997d in / 
# Tue, 01 Mar 2022 02:11:30 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 19:18:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 19:18:20 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 19:18:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 19:18:27 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 01 Mar 2022 20:12:05 GMT
ENV PYTHON_VERSION=3.10.2
# Tue, 01 Mar 2022 20:22:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 01 Mar 2022 20:22:05 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Tue, 01 Mar 2022 20:22:06 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Tue, 01 Mar 2022 20:22:07 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 08 Mar 2022 03:02:56 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/38e54e5de07c66e875c11a1ebbdb938854625dd8/public/get-pip.py
# Tue, 08 Mar 2022 03:02:57 GMT
ENV PYTHON_GET_PIP_SHA256=e235c437e5c7d7524fbce3880ca39b917a73dc565e0c813465b7a7a329bb279a
# Tue, 08 Mar 2022 03:03:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 08 Mar 2022 03:03:10 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:279a020076a7fbddfc996e4c55e605a8f322810c3eca21cdedbcb06beb0e1305`  
		Last Modified: Tue, 01 Mar 2022 02:18:24 GMT  
		Size: 30.1 MB (30057008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:035530c613019c233e8c92570cc5d166a19b90cab677f02cd842b59f494d70f6`  
		Last Modified: Tue, 01 Mar 2022 21:56:28 GMT  
		Size: 1.1 MB (1064031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b85998afdfc0b0d5e327ae2623a8064ea924075cbd74d332f4b131f4c4ab362`  
		Last Modified: Tue, 01 Mar 2022 21:58:15 GMT  
		Size: 11.3 MB (11273716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6460f37570b3ac68f371943939eebb41b76aea95f2a561b9a8b8a8df888d28e`  
		Last Modified: Tue, 01 Mar 2022 21:58:13 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f84e01cf6f0a12e10531cb9d30ddbd83ebfd27e091d8ed6b2c401b42376b052a`  
		Last Modified: Tue, 08 Mar 2022 03:14:01 GMT  
		Size: 2.4 MB (2422433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-slim-bullseye` - linux; 386

```console
$ docker pull python@sha256:0b42e34b86d28598646dc14ea95806f2708b0c3de4b2d77a765f1ed845574f92
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47442021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f6da2c5c0140bbad3009a71c2c137518660be3cd1ab3cf7b24d9b3a56b6ca28`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 01 Mar 2022 02:07:32 GMT
ADD file:e92ab504d4c0d3bd63da83254e6ca400b607c32e0f5037039648559b91770870 in / 
# Tue, 01 Mar 2022 02:07:33 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 22:16:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 22:16:47 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 22:16:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 22:16:52 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 01 Mar 2022 23:39:36 GMT
ENV PYTHON_VERSION=3.10.2
# Tue, 01 Mar 2022 23:56:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 01 Mar 2022 23:56:17 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Tue, 01 Mar 2022 23:56:17 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Tue, 01 Mar 2022 23:56:17 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 08 Mar 2022 03:37:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/38e54e5de07c66e875c11a1ebbdb938854625dd8/public/get-pip.py
# Tue, 08 Mar 2022 03:37:33 GMT
ENV PYTHON_GET_PIP_SHA256=e235c437e5c7d7524fbce3880ca39b917a73dc565e0c813465b7a7a329bb279a
# Tue, 08 Mar 2022 03:37:46 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 08 Mar 2022 03:37:46 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:04a87e821be7e4b29d48011b7aa4ff884ca57fd36995cb3b99fd2fc24ac562d8`  
		Last Modified: Tue, 01 Mar 2022 02:15:51 GMT  
		Size: 32.4 MB (32377389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b63dcfb8da56cf07b5cffd0becf1ed7f576ad2d4a3614d661c1965326792adfc`  
		Last Modified: Wed, 02 Mar 2022 02:37:31 GMT  
		Size: 1.1 MB (1088320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c03bf1d550ef00a7a19f6641928ac62de27443e14629fb092e913f775341128e`  
		Last Modified: Wed, 02 Mar 2022 02:40:04 GMT  
		Size: 11.3 MB (11339369 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f725cfe500362d7cc7a875bd7fc626927db22653dd324a728583821a78fac8`  
		Last Modified: Wed, 02 Mar 2022 02:40:00 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead0d13eec3e0cfe0dcd758406706f7a6faccf2215b3c98e1a27af9cefc7417a`  
		Last Modified: Tue, 08 Mar 2022 03:48:45 GMT  
		Size: 2.6 MB (2636707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-slim-bullseye` - linux; ppc64le

```console
$ docker pull python@sha256:19dc75f46086bfc0e14b8cad406f69ebdb11a83fb4a56c5e6fc2b56f90e88350
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.6 MB (50598682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4daac94397177ad6a380ac806d66ee0fc1202e34ec7023b3de82055c46fc3045`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 01 Mar 2022 02:05:07 GMT
ADD file:fc0989685aecf50ec36795d73893c30d9ddd4f946f8c5f4a6d10963f8ab41168 in / 
# Tue, 01 Mar 2022 02:05:12 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 18:07:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 18:07:31 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 18:07:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 18:08:00 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 01 Mar 2022 20:00:35 GMT
ENV PYTHON_VERSION=3.10.2
# Tue, 01 Mar 2022 20:25:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 01 Mar 2022 20:26:06 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Tue, 01 Mar 2022 20:26:08 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Tue, 01 Mar 2022 20:26:10 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 01 Mar 2022 20:26:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/2caf84b14febcda8077e59e9b8a6ef9a680aa392/public/get-pip.py
# Tue, 01 Mar 2022 20:26:16 GMT
ENV PYTHON_GET_PIP_SHA256=7c5239cea323cadae36083079a5ee6b2b3d56f25762a0c060d2867b89e5e06c5
# Tue, 01 Mar 2022 20:27:09 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 01 Mar 2022 20:27:13 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:1dde9239ed493e1fe68971baa3f162c734ef0f461ad109e48aeb5b56daa55cc2`  
		Last Modified: Tue, 01 Mar 2022 02:15:19 GMT  
		Size: 35.3 MB (35272910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c5391f225a5ead3b2bf21c8101e6393e8a70f0aaf1b4419ab0b3922c1438674`  
		Last Modified: Tue, 01 Mar 2022 23:53:38 GMT  
		Size: 1.1 MB (1094447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a31da6ecdf93e05a00023037d05d451cddcee4bb1c67a2843088bfe3660b46f7`  
		Last Modified: Tue, 01 Mar 2022 23:58:35 GMT  
		Size: 11.6 MB (11592611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1309afe35616b3c0c78be94bc72afaf767919fc3c649196335fb6bd21bbce577`  
		Last Modified: Tue, 01 Mar 2022 23:58:33 GMT  
		Size: 236.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0197653db782f6eaf80714776a086d7eeba950f355e1e21e624a70ee361cd52f`  
		Last Modified: Tue, 01 Mar 2022 23:58:34 GMT  
		Size: 2.6 MB (2638478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `python:3-slim-bullseye` - linux; s390x

```console
$ docker pull python@sha256:fd7069fa7226f5969891bcea824062a0e331e1604e79f371f7a64cb6569feeed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.4 MB (44380560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a73f567ef3d4761937092a493b875642a535b99ca5fb4ddf02820bf56add5e28`
-	Default Command: `["python3"]`

```dockerfile
# Tue, 01 Mar 2022 02:01:56 GMT
ADD file:d869ad3392a4e752c2f73d08a4cc13594c94bfc050bd037db0ca9827a0207072 in / 
# Tue, 01 Mar 2022 02:01:58 GMT
CMD ["bash"]
# Tue, 01 Mar 2022 10:32:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 01 Mar 2022 10:32:10 GMT
ENV LANG=C.UTF-8
# Tue, 01 Mar 2022 10:32:14 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 01 Mar 2022 10:32:14 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 01 Mar 2022 11:14:04 GMT
ENV PYTHON_VERSION=3.10.2
# Tue, 01 Mar 2022 11:23:00 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg dirmngr 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	command -v gpgconf > /dev/null && gpgconf --kill all || :; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-lto 		--with-system-expat 		--with-system-ffi 		--without-ensurepip 	; 	nproc="$(nproc)"; 	make -j "$nproc" 		LDFLAGS="-Wl,--strip-all" 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name '*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		python3 --version
# Tue, 01 Mar 2022 11:23:01 GMT
RUN set -eux; 	for src in idle3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "/usr/local/bin/$src" "/usr/local/bin/$dst"; 	done
# Tue, 01 Mar 2022 11:23:01 GMT
ENV PYTHON_PIP_VERSION=21.2.4
# Tue, 01 Mar 2022 11:23:01 GMT
ENV PYTHON_SETUPTOOLS_VERSION=58.1.0
# Tue, 01 Mar 2022 11:23:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/2caf84b14febcda8077e59e9b8a6ef9a680aa392/public/get-pip.py
# Tue, 01 Mar 2022 11:23:02 GMT
ENV PYTHON_GET_PIP_SHA256=7c5239cea323cadae36083079a5ee6b2b3d56f25762a0c060d2867b89e5e06c5
# Tue, 01 Mar 2022 11:23:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum -c -; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 		python get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		"pip==$PYTHON_PIP_VERSION" 		"setuptools==$PYTHON_SETUPTOOLS_VERSION" 	; 	rm -f get-pip.py; 		pip --version
# Tue, 01 Mar 2022 11:23:11 GMT
CMD ["python3"]
```

-	Layers:
	-	`sha256:f81abce72636770dac4258df46a31beeb6ad81dfddd5b7c9c3fa6942ea074922`  
		Last Modified: Tue, 01 Mar 2022 02:07:33 GMT  
		Size: 29.6 MB (29647132 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8e2d1576afb1f1f1a821f4c7327ae75bce0954c56bc387b877c8b773f4ec6fe`  
		Last Modified: Tue, 01 Mar 2022 12:40:55 GMT  
		Size: 1.1 MB (1075376 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc89a3af2704d39080f290171a678626aa25d592f9823b135316b9f801f5cbc1`  
		Last Modified: Tue, 01 Mar 2022 12:41:44 GMT  
		Size: 11.0 MB (11021056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b11f83a491b048236301522f2335e37b762dcde7f9ebb7e435487245dad95c`  
		Last Modified: Tue, 01 Mar 2022 12:41:43 GMT  
		Size: 235.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20a08e640c77fa028997589d26636846c5174c86b6dd0d49609a7c5e766a3be1`  
		Last Modified: Tue, 01 Mar 2022 12:41:43 GMT  
		Size: 2.6 MB (2636761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
