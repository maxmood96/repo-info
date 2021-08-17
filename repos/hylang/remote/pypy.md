## `hylang:pypy`

```console
$ docker pull hylang@sha256:4350310af1e27f1a6050f06dd54fea7a46fdaca34d883e373b2e7c0a8bba3662
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 5
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x
	-	windows version 10.0.17763.2114; amd64

### `hylang:pypy` - linux; amd64

```console
$ docker pull hylang@sha256:82311ea9843026d421d1753a28883f36d1d0f1843140e14d438eaf8775ab6bce
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74253763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26e90ff3dafa26a8d5f352a8b6086d0bea05a958ea4c0a1bd2e7629895c45028`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 17 Aug 2021 01:24:06 GMT
ADD file:87b4e60fe3af680c6815448374365a44e9ea461bc8ade2960b4639c25aed3ba9 in / 
# Tue, 17 Aug 2021 01:24:06 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 08:50:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 08:50:36 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 08:50:36 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 08:50:37 GMT
ENV PYPY_VERSION=7.3.5
# Tue, 17 Aug 2021 08:51:13 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux64.tar.bz2'; 			sha256='9000db3e87b54638e55177e68cbeb30a30fe5d17b6be48a9eb43d65b3ebcfc26'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-aarch64.tar.bz2'; 			sha256='85d83093b3ef5b863f641bc4073d057cc98bb821e16aa9361a5ff4898e70e8ee'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux32.tar.bz2'; 			sha256='3dd8b565203d372829e53945c599296fa961895130342ea13791b17c84ed06c4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-s390x.tar.bz2'; 			sha256='dffdf5d73613be2c6809dc1a3cf3ee6ac2f3af015180910247ff24270b532ed5'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 17 Aug 2021 08:51:13 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Tue, 17 Aug 2021 08:51:14 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 17 Aug 2021 08:51:14 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 17 Aug 2021 08:51:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 17 Aug 2021 08:51:32 GMT
CMD ["pypy3"]
# Tue, 17 Aug 2021 17:04:43 GMT
ENV HY_VERSION=1.0a3
# Tue, 17 Aug 2021 17:04:59 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Tue, 17 Aug 2021 17:04:59 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e1acddbe380c63f0de4b77d3f287b7c81cd9d89563a230692378126b46ea6546`  
		Last Modified: Tue, 17 Aug 2021 01:30:21 GMT  
		Size: 27.1 MB (27145985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b8bda9c5f588bf59d1532ad316ff9c06bf36ab501190f275ce41a88b030b7f`  
		Last Modified: Tue, 17 Aug 2021 08:53:46 GMT  
		Size: 2.8 MB (2757666 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:352286221f179fe43e2612600e0774385a9af3e36a9fc33d429662ca1a5655b7`  
		Last Modified: Tue, 17 Aug 2021 08:53:54 GMT  
		Size: 38.6 MB (38586660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c2e5c42cc61d8e4e9fad51deef78b7ab3ce1403b2e9175699d409ec37d31091d`  
		Last Modified: Tue, 17 Aug 2021 08:53:46 GMT  
		Size: 2.6 MB (2598385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b1379f2ed83a9c506dd303ccf36e8fef5c51d37a5038be88153254bbe7c683a`  
		Last Modified: Tue, 17 Aug 2021 17:08:20 GMT  
		Size: 3.2 MB (3165067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:ed6b4846ba7795fbb54abe392ae91b8eafb2d6978db5db2fbe4fabdb300eadee
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69642870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4de782d1818d67202c44ba89d6cc1cefcd97be4e24d77cea3ad7004778b2445`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 17 Aug 2021 01:46:31 GMT
ADD file:a62249c8d6f38120ba61478f35ce3cc947234ac504859ced66532a60de786609 in / 
# Tue, 17 Aug 2021 01:46:31 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 07:35:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 07:35:49 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 07:35:49 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 07:35:49 GMT
ENV PYPY_VERSION=7.3.5
# Tue, 17 Aug 2021 07:36:20 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux64.tar.bz2'; 			sha256='9000db3e87b54638e55177e68cbeb30a30fe5d17b6be48a9eb43d65b3ebcfc26'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-aarch64.tar.bz2'; 			sha256='85d83093b3ef5b863f641bc4073d057cc98bb821e16aa9361a5ff4898e70e8ee'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux32.tar.bz2'; 			sha256='3dd8b565203d372829e53945c599296fa961895130342ea13791b17c84ed06c4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-s390x.tar.bz2'; 			sha256='dffdf5d73613be2c6809dc1a3cf3ee6ac2f3af015180910247ff24270b532ed5'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 17 Aug 2021 07:36:20 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Tue, 17 Aug 2021 07:36:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 17 Aug 2021 07:36:21 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 17 Aug 2021 07:36:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 17 Aug 2021 07:36:37 GMT
CMD ["pypy3"]
# Tue, 17 Aug 2021 13:25:14 GMT
ENV HY_VERSION=1.0a3
# Tue, 17 Aug 2021 13:25:26 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Tue, 17 Aug 2021 13:25:26 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:64ac1a72c06aa20e6c3b2e37ce66ddf902187eb683a427a477895f158a930e31`  
		Last Modified: Tue, 17 Aug 2021 01:54:22 GMT  
		Size: 25.9 MB (25915072 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76bab942138fc1fd68c083353a35a2d7ff0d49799cc7acd226b474a290bd5aee`  
		Last Modified: Tue, 17 Aug 2021 07:40:00 GMT  
		Size: 2.6 MB (2626272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:706592b91113cfda96cacf1cf98b5031f1d453dae83accbd1d3b20e47e61cb96`  
		Last Modified: Tue, 17 Aug 2021 07:40:07 GMT  
		Size: 35.3 MB (35338360 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:adf4815fd62af1e91d4619c2791116a317863db719416135089e12a9e1106684`  
		Last Modified: Tue, 17 Aug 2021 07:40:00 GMT  
		Size: 2.6 MB (2598030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcb0cb3d209ba99f34556ab44d64ec0c73d4a2ca4e758e85335ebc35c27ca42d`  
		Last Modified: Tue, 17 Aug 2021 13:29:40 GMT  
		Size: 3.2 MB (3165136 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy` - linux; 386

```console
$ docker pull hylang@sha256:405964e4082159554d7dcd2dcfc84b1722b0ea9ebf0d72600793b9e781bf3dbc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76915023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dada6df7c72e62d6336df5080d162d9791a41e2e1d79051940958ca93b642eb0`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 22 Jul 2021 00:39:50 GMT
ADD file:cb657a3d01f25bf815677ce223e8802d054f11aeb95f85b160982277916637bd in / 
# Thu, 22 Jul 2021 00:39:51 GMT
CMD ["bash"]
# Thu, 22 Jul 2021 15:24:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 22 Jul 2021 15:24:37 GMT
ENV LANG=C.UTF-8
# Thu, 22 Jul 2021 15:24:38 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 22 Jul 2021 15:24:38 GMT
ENV PYPY_VERSION=7.3.5
# Thu, 22 Jul 2021 15:25:14 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux64.tar.bz2'; 			sha256='9000db3e87b54638e55177e68cbeb30a30fe5d17b6be48a9eb43d65b3ebcfc26'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-aarch64.tar.bz2'; 			sha256='85d83093b3ef5b863f641bc4073d057cc98bb821e16aa9361a5ff4898e70e8ee'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux32.tar.bz2'; 			sha256='3dd8b565203d372829e53945c599296fa961895130342ea13791b17c84ed06c4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-s390x.tar.bz2'; 			sha256='dffdf5d73613be2c6809dc1a3cf3ee6ac2f3af015180910247ff24270b532ed5'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 22 Jul 2021 15:25:15 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Thu, 22 Jul 2021 15:25:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 22 Jul 2021 15:25:15 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 22 Jul 2021 15:25:29 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 22 Jul 2021 15:25:30 GMT
CMD ["pypy3"]
# Thu, 22 Jul 2021 23:55:14 GMT
ENV HY_VERSION=1.0a3
# Thu, 22 Jul 2021 23:55:29 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 22 Jul 2021 23:55:29 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:fa9d06db5f4195bd51665a89e08e2e7db25636ac28ab162fe876ae0a53093fe5`  
		Last Modified: Thu, 22 Jul 2021 00:46:36 GMT  
		Size: 27.8 MB (27797459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47b32ec7f2564d4cb5d38f860212b972f98c828f781a4e805ec220a1b14a0ae`  
		Last Modified: Thu, 22 Jul 2021 15:30:38 GMT  
		Size: 2.8 MB (2769392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d939a00d60ec366bbd5b7f533a79aac804d3e7f1d7cbabe35cd2dae80c3e82d6`  
		Last Modified: Thu, 22 Jul 2021 15:30:48 GMT  
		Size: 40.6 MB (40585163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5c4e6dee1e4deef22df36f811356aa80966a558fa9f53f558b91e5300fb04ba`  
		Last Modified: Thu, 22 Jul 2021 15:30:38 GMT  
		Size: 2.6 MB (2598046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78af76992d5276f865b0e38bc275d4cfbde940cfc61c7c01e88916d0d301aeb`  
		Last Modified: Fri, 23 Jul 2021 00:03:12 GMT  
		Size: 3.2 MB (3164963 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy` - linux; s390x

```console
$ docker pull hylang@sha256:3acf545f5276679699723a1e1a7df511dc37604f607035c43670f78a3a16aaab
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69592562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cad75ff194befdfacf5c0ceecec55d6b7a696fc30d0ac33632c56c419bd62788`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 17 Aug 2021 01:49:55 GMT
ADD file:f99acf07eb8c42cc90080a195bbcdb18850a1d7a333b385d5d8ebe31c9e9f783 in / 
# Tue, 17 Aug 2021 01:49:59 GMT
CMD ["bash"]
# Tue, 17 Aug 2021 06:08:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 17 Aug 2021 06:08:53 GMT
ENV LANG=C.UTF-8
# Tue, 17 Aug 2021 06:08:53 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 17 Aug 2021 06:08:54 GMT
ENV PYPY_VERSION=7.3.5
# Tue, 17 Aug 2021 06:09:32 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux64.tar.bz2'; 			sha256='9000db3e87b54638e55177e68cbeb30a30fe5d17b6be48a9eb43d65b3ebcfc26'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-aarch64.tar.bz2'; 			sha256='85d83093b3ef5b863f641bc4073d057cc98bb821e16aa9361a5ff4898e70e8ee'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux32.tar.bz2'; 			sha256='3dd8b565203d372829e53945c599296fa961895130342ea13791b17c84ed06c4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-s390x.tar.bz2'; 			sha256='dffdf5d73613be2c6809dc1a3cf3ee6ac2f3af015180910247ff24270b532ed5'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 17 Aug 2021 06:09:39 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Tue, 17 Aug 2021 06:09:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 17 Aug 2021 06:09:40 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 17 Aug 2021 06:09:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 17 Aug 2021 06:09:58 GMT
CMD ["pypy3"]
# Tue, 17 Aug 2021 12:52:07 GMT
ENV HY_VERSION=1.0a3
# Tue, 17 Aug 2021 12:52:14 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Tue, 17 Aug 2021 12:52:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ed4fb22ab70391b36e4b9f97e34387c33652dc2b91b5f0c7ef4ada070bfd32c3`  
		Last Modified: Tue, 17 Aug 2021 01:58:12 GMT  
		Size: 25.8 MB (25760856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5d0c8986e40fd97daf48e09b229566bd39f534f893e91b7aa18c31b2484034e`  
		Last Modified: Tue, 17 Aug 2021 06:11:34 GMT  
		Size: 2.5 MB (2452404 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81648b697c008949ab5f5018cdb64f1d0c1057d647a73afbaa7012fb307e159d`  
		Last Modified: Tue, 17 Aug 2021 06:11:41 GMT  
		Size: 35.6 MB (35616088 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:237859206cd226c9a17486a2cfe32cd317400a0363318850b952f3808eb96a21`  
		Last Modified: Tue, 17 Aug 2021 06:11:35 GMT  
		Size: 2.6 MB (2598273 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24539713603d92db98706e9c5520385a4d5e67b1bfef1a58a059089395d2a96d`  
		Last Modified: Tue, 17 Aug 2021 12:55:04 GMT  
		Size: 3.2 MB (3164941 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy` - windows version 10.0.17763.2114; amd64

```console
$ docker pull hylang@sha256:bf8c37362fb8e8509e73d7c303dee0fc5e50b5392ab69108bd9ef8132798d811
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2735940365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88dd6425859ad81786ce263e14c43bb49f3fc35e232e001a880883a92ab6654`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 05 Aug 2021 19:44:34 GMT
RUN Install update 1809-amd64
# Wed, 11 Aug 2021 12:16:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 11 Aug 2021 12:17:46 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 11 Aug 2021 12:18:58 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 11 Aug 2021 12:19:01 GMT
ENV PYPY_VERSION=7.3.5
# Wed, 11 Aug 2021 12:20:38 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.7-v7.3.5-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '072bd22427178dc4e65d961f50281bd2f56e11c4e4d9f16311c703f69f46ae24'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.7-v7.3.5-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy3 --version") ...'; 	pypy3 --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 11 Aug 2021 12:20:42 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Wed, 11 Aug 2021 12:20:46 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 11 Aug 2021 12:20:49 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 11 Aug 2021 12:22:52 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host ('Installing "pip == {0}" ...' -f $env:PYTHON_PIP_VERSION); 	pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $env:PYTHON_PIP_VERSION) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 11 Aug 2021 12:22:56 GMT
CMD ["pypy3"]
# Wed, 11 Aug 2021 22:50:32 GMT
ENV HY_VERSION=1.0a3
# Wed, 11 Aug 2021 22:52:07 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 11 Aug 2021 22:52:09 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c67ded6868b61d392a0c096f911563fd6bc0bc3ed4fe401d077b3718a1b0cdaf`  
		Size: 967.7 MB (967665054 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:f5be68d5dab08a1dcc52a6ee52dd4901e4d6a384f0df3a12cba3d53649f7c602`  
		Last Modified: Wed, 11 Aug 2021 13:29:37 GMT  
		Size: 1.4 KB (1425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e73b47f81d7a6322e065ef2905458038c02de517590ec6c473f8a5959424c913`  
		Last Modified: Wed, 11 Aug 2021 22:31:32 GMT  
		Size: 357.4 KB (357388 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6675de547a415473239d82f2721d9e7dddfec0372242e4a01668a0d707baccb`  
		Last Modified: Wed, 11 Aug 2021 22:31:34 GMT  
		Size: 15.5 MB (15494160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03723f17157e71ae53f3514ab61d79afb79913a01bc161dfc61eb671c20ca040`  
		Last Modified: Wed, 11 Aug 2021 22:31:31 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86280b3fb05d68909452446ad6665af848e678f451b10a878e8700cfa833d9f`  
		Last Modified: Wed, 11 Aug 2021 22:31:42 GMT  
		Size: 27.0 MB (26997758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17584b7db226c002e211b7650b6ff5749f7ce0e1046d6054b3f2b2c23ab7a4a1`  
		Last Modified: Wed, 11 Aug 2021 22:31:28 GMT  
		Size: 1.4 KB (1392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:038104a0c71db7b1a93be6cf9c397d8882b349cba478c27026963b5d80006228`  
		Last Modified: Wed, 11 Aug 2021 22:31:28 GMT  
		Size: 1.4 KB (1436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:832479b17ab1f83ecc57d0d7a289226a2d2a29ba6ef9d18fc0794163c7d73bb6`  
		Last Modified: Wed, 11 Aug 2021 22:31:28 GMT  
		Size: 1.4 KB (1403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b68d766b187344414a5462d2dceae4794371ba4615f1371a3b0577192ac69808`  
		Last Modified: Wed, 11 Aug 2021 22:31:33 GMT  
		Size: 2.9 MB (2937884 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6e3043b453534413a90bc26c4f95217aea32cd6a077114ff966b4fc791250f2`  
		Last Modified: Wed, 11 Aug 2021 22:31:28 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba2507296fbd0ea2b3145dfb18672131ef42a0af08be9144595ad8f41bbab7a5`  
		Last Modified: Wed, 11 Aug 2021 22:52:53 GMT  
		Size: 1.4 KB (1417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be9a347505407b5461d03e89217ff062d5eea5c383da5d1b957d3c738b6b2ff`  
		Last Modified: Wed, 11 Aug 2021 22:52:54 GMT  
		Size: 4.1 MB (4143954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c4b2125050c4b78ef1acc1208f90631e389d323ed331e0aa9e0d945c5620152`  
		Last Modified: Wed, 11 Aug 2021 22:52:53 GMT  
		Size: 1.4 KB (1423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
