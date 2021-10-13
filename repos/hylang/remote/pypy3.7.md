## `hylang:pypy3.7`

```console
$ docker pull hylang@sha256:c0fcb1179e9d4f10932a088917ee79c6115d0b0d4c8eea2cdc6db93069f189a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	windows version 10.0.17763.2237; amd64

### `hylang:pypy3.7` - linux; amd64

```console
$ docker pull hylang@sha256:b05e880ea7906928978606f673302da319d3b4315510d38b9892de29d7021957
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.4 MB (75366718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12cab5c7da635d321cd7618c6f9c02d5cffc254a222515782e675377bd6378eb`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 12 Oct 2021 01:20:42 GMT
ADD file:16dc2c6d1932194edec28d730b004fd6deca3d0f0e1a07bc5b8b6e8a1662f7af in / 
# Tue, 12 Oct 2021 01:20:42 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 16:07:44 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 16:07:44 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 16:07:44 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 16:07:45 GMT
ENV PYPY_VERSION=7.3.5
# Tue, 12 Oct 2021 16:08:22 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux64.tar.bz2'; 			sha256='9000db3e87b54638e55177e68cbeb30a30fe5d17b6be48a9eb43d65b3ebcfc26'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-aarch64.tar.bz2'; 			sha256='85d83093b3ef5b863f641bc4073d057cc98bb821e16aa9361a5ff4898e70e8ee'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux32.tar.bz2'; 			sha256='3dd8b565203d372829e53945c599296fa961895130342ea13791b17c84ed06c4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-s390x.tar.bz2'; 			sha256='dffdf5d73613be2c6809dc1a3cf3ee6ac2f3af015180910247ff24270b532ed5'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 12 Oct 2021 16:08:23 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 12 Oct 2021 16:08:23 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 12 Oct 2021 16:08:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 12 Oct 2021 16:08:44 GMT
CMD ["pypy3"]
# Tue, 12 Oct 2021 17:41:36 GMT
ENV HY_VERSION=1.0a3
# Tue, 12 Oct 2021 17:41:45 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Tue, 12 Oct 2021 17:41:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7d63c13d9b9b6ec5f05a2b07daadacaa9c610d01102a662ae9b1d082105f1ffa`  
		Last Modified: Tue, 12 Oct 2021 01:26:05 GMT  
		Size: 31.4 MB (31357311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed35c7420899dc2a554276761fec7776c759be3ab1dc2b373bed21cf08006be6`  
		Last Modified: Tue, 12 Oct 2021 16:16:25 GMT  
		Size: 1.1 MB (1065980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b20a0f1f060b7c6e51eb7b96bf5dabf0b81beff118707f1dd96e5cd58d699f2`  
		Last Modified: Tue, 12 Oct 2021 16:16:35 GMT  
		Size: 37.5 MB (37507989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8d8c4c85994ed5b21203db72f632562558716a919832822721897da73fdc87`  
		Last Modified: Tue, 12 Oct 2021 16:16:26 GMT  
		Size: 2.4 MB (2370239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a99c768fa7cc8b8cc914f5d69df46e1cb2a0aa309f54b2b3e0ee12e8d080b7`  
		Last Modified: Tue, 12 Oct 2021 17:45:44 GMT  
		Size: 3.1 MB (3065199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.7` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:c113fa8610ea491a54c3dcd54c1b04be0d4c84d8ef6aae84b22cd8ef07423cbf
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.8 MB (70793684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea40f9057edd309b64b8d2a7058cd212cd49789af0bc97879dd18f3adec3fb19`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 12 Oct 2021 01:41:18 GMT
ADD file:d84144ad575672cd6cc8a00c8e5a88ab0545348f040fc249ea5fcf8193b2bce6 in / 
# Tue, 12 Oct 2021 01:41:18 GMT
CMD ["bash"]
# Wed, 13 Oct 2021 16:39:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 13 Oct 2021 16:39:55 GMT
ENV LANG=C.UTF-8
# Wed, 13 Oct 2021 16:39:56 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 13 Oct 2021 16:39:57 GMT
ENV PYPY_VERSION=7.3.5
# Wed, 13 Oct 2021 16:40:23 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux64.tar.bz2'; 			sha256='9000db3e87b54638e55177e68cbeb30a30fe5d17b6be48a9eb43d65b3ebcfc26'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-aarch64.tar.bz2'; 			sha256='85d83093b3ef5b863f641bc4073d057cc98bb821e16aa9361a5ff4898e70e8ee'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux32.tar.bz2'; 			sha256='3dd8b565203d372829e53945c599296fa961895130342ea13791b17c84ed06c4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-s390x.tar.bz2'; 			sha256='dffdf5d73613be2c6809dc1a3cf3ee6ac2f3af015180910247ff24270b532ed5'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 13 Oct 2021 16:40:23 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 13 Oct 2021 16:40:24 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 13 Oct 2021 16:40:38 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 13 Oct 2021 16:40:39 GMT
CMD ["pypy3"]
# Wed, 13 Oct 2021 16:58:57 GMT
ENV HY_VERSION=1.0a3
# Wed, 13 Oct 2021 16:59:07 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 13 Oct 2021 16:59:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a9eb63951c1c2ee8efcc12b696928fee3741a2d4eae76f2da3e161a5d90548bf`  
		Last Modified: Tue, 12 Oct 2021 01:48:13 GMT  
		Size: 30.0 MB (30043906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:244bad71c45dd865aa32743cd1ff31b180595e799db39b4954c7a6928b9ba8ae`  
		Last Modified: Wed, 13 Oct 2021 16:48:39 GMT  
		Size: 1.1 MB (1053927 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f1c073152109e04b18681fb8fd74219ad46b7acd8e0248c71d6d4acab996f4`  
		Last Modified: Wed, 13 Oct 2021 16:48:45 GMT  
		Size: 34.5 MB (34476651 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ebfcacda63ee664869f72e534c4c1d705517c96c9d5662d2a74b8c5f14c1207`  
		Last Modified: Wed, 13 Oct 2021 16:48:39 GMT  
		Size: 2.2 MB (2154860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d689397ebe5cdc18f8f13311ac0b4f5000c54d792ad0f012c118b1cfb7f658c9`  
		Last Modified: Wed, 13 Oct 2021 17:06:54 GMT  
		Size: 3.1 MB (3064340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.7` - linux; 386

```console
$ docker pull hylang@sha256:39bf6484555145374d62db89fd4af6194249c26d25f6aaa7bbaf6e1a41dc9e3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75716356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69bee8f5bb17fb394e7a0de27b14c98b3b0fdd70464b50d28634ac73fabc9fd3`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 12 Oct 2021 01:39:47 GMT
ADD file:42196ffa4c70af8d9f1e7b74edb3bb92d47296acf989adf615e8208230f8bd0c in / 
# Tue, 12 Oct 2021 01:39:47 GMT
CMD ["bash"]
# Tue, 12 Oct 2021 09:51:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Oct 2021 09:51:57 GMT
ENV LANG=C.UTF-8
# Tue, 12 Oct 2021 09:51:57 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Oct 2021 09:51:57 GMT
ENV PYPY_VERSION=7.3.5
# Tue, 12 Oct 2021 09:52:31 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux64.tar.bz2'; 			sha256='9000db3e87b54638e55177e68cbeb30a30fe5d17b6be48a9eb43d65b3ebcfc26'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-aarch64.tar.bz2'; 			sha256='85d83093b3ef5b863f641bc4073d057cc98bb821e16aa9361a5ff4898e70e8ee'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-linux32.tar.bz2'; 			sha256='3dd8b565203d372829e53945c599296fa961895130342ea13791b17c84ed06c4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.5-s390x.tar.bz2'; 			sha256='dffdf5d73613be2c6809dc1a3cf3ee6ac2f3af015180910247ff24270b532ed5'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 12 Oct 2021 09:52:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 12 Oct 2021 09:52:32 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 12 Oct 2021 09:52:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 12 Oct 2021 09:52:48 GMT
CMD ["pypy3"]
# Wed, 13 Oct 2021 02:29:57 GMT
ENV HY_VERSION=1.0a3
# Wed, 13 Oct 2021 02:30:12 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 13 Oct 2021 02:30:13 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:87318d165b5c0fdf05c8ccf97d83084f56b4608075a3335b1a46c76295b82753`  
		Last Modified: Tue, 12 Oct 2021 01:47:39 GMT  
		Size: 32.4 MB (32370344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92e56cd7d03192db8b2e7e5fc40267a5319da47f0a28fcfeb91b2309b27db20f`  
		Last Modified: Tue, 12 Oct 2021 10:02:16 GMT  
		Size: 1.1 MB (1078385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea053a8c803b8846bdd69fb7952c1ce8fa0689b1955b23a1580e747468fb287`  
		Last Modified: Tue, 12 Oct 2021 10:02:28 GMT  
		Size: 36.8 MB (36832308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0556c169f353bcf7eb80f638b1de967b97dcdc79c5080f6021124fdef6b752`  
		Last Modified: Tue, 12 Oct 2021 10:02:16 GMT  
		Size: 2.4 MB (2369895 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2122acbdaf585fc3b0cf69632e04e190957a024739fc9de1d28c0da9b6233109`  
		Last Modified: Wed, 13 Oct 2021 02:38:04 GMT  
		Size: 3.1 MB (3065424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.7` - windows version 10.0.17763.2237; amd64

```console
$ docker pull hylang@sha256:ea66b43780ace0ede5ea512c18ebe34b6168aea6e8493cf3cd8ec2005b2e9f62
```

-	Docker Version: 20.10.8
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 GB (2736026709 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c6260d88fb04794a20e5eff21c3ae1638837316775b015a05cfe6bb04e91d1`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 07 May 2020 05:09:25 GMT
RUN Apply image 1809-RTM-amd64
# Thu, 07 Oct 2021 08:25:51 GMT
RUN Install update 1809-amd64
# Wed, 13 Oct 2021 12:02:56 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 13 Oct 2021 12:04:48 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 13 Oct 2021 12:06:13 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 13 Oct 2021 12:06:14 GMT
ENV PYPY_VERSION=7.3.5
# Wed, 13 Oct 2021 12:08:07 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.7-v7.3.5-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '072bd22427178dc4e65d961f50281bd2f56e11c4e4d9f16311c703f69f46ae24'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.7-v7.3.5-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy3 --version") ...'; 	pypy3 --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 13 Oct 2021 12:08:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 13 Oct 2021 12:08:10 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 13 Oct 2021 12:10:45 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 13 Oct 2021 12:10:47 GMT
CMD ["pypy3"]
# Wed, 13 Oct 2021 18:09:15 GMT
ENV HY_VERSION=1.0a3
# Wed, 13 Oct 2021 18:11:09 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION)
# Wed, 13 Oct 2021 18:11:10 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4612f6d0b889cad0ed0292fae3a0b0c8a9e49aff6dea8eb049b2386d9b07986f`  
		Size: 1.7 GB (1718332879 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:c0698cf91ebd6bcfb319be6a50421b356d6a3dbbd213d9b2b9dca0f837d7a999`  
		Size: 968.0 MB (967985917 bytes)  
		MIME: application/vnd.docker.image.rootfs.foreign.diff.tar.gzip
	-	`sha256:cc0c4e719f418d49c6a0fb87abd2e0e480c5b6fec1bacc3077cacfad9b4ab3e0`  
		Last Modified: Wed, 13 Oct 2021 12:18:09 GMT  
		Size: 1.4 KB (1399 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a3bdf70816ac16df25478dbbccc6214bf88a0b692485f62ab5c8786d6712f0`  
		Last Modified: Wed, 13 Oct 2021 12:18:06 GMT  
		Size: 346.8 KB (346768 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41276917c6b2081d9aae93760066800018afb849c5db8de79720a2e590568b57`  
		Last Modified: Wed, 13 Oct 2021 12:18:10 GMT  
		Size: 15.5 MB (15492096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63b2b5ed6d4612d08b20865bdbfbb33c049b17934dd241f2b9c895a85236e921`  
		Last Modified: Wed, 13 Oct 2021 12:18:06 GMT  
		Size: 1.4 KB (1426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:504111d5dd740084a1c05cfc4d7f758c4f772dc7d2352395c11fa895ecf30af0`  
		Last Modified: Wed, 13 Oct 2021 12:18:13 GMT  
		Size: 27.0 MB (26990288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc99b45ee0494ede40be04f813352678812207f85dae6ba04e8fce921c2fc04`  
		Last Modified: Wed, 13 Oct 2021 12:18:04 GMT  
		Size: 1.4 KB (1366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d400a68d104aa0d47b8d33bc7806cf24febaf3d3284f78bdd075d15d1e4ab31c`  
		Last Modified: Wed, 13 Oct 2021 12:18:03 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:032543b33fbd636ae2fb0d0ba03e6c21a9613649a21150342e6cb7b7d82cc2ad`  
		Last Modified: Wed, 13 Oct 2021 12:18:07 GMT  
		Size: 2.8 MB (2824508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0727f8066b2add9b492cbe6e791c49c0e9e19a806e84d472378cb84e7017731e`  
		Last Modified: Wed, 13 Oct 2021 12:18:03 GMT  
		Size: 1.3 KB (1276 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28dbd675827f7f622da0aecfa94721692d6ba8dfadf7271fbb143e6fab64cd15`  
		Last Modified: Wed, 13 Oct 2021 18:12:15 GMT  
		Size: 1.4 KB (1441 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61e32d5568b5641b8de300f10b33dbb46db9431efedd35f76221d92600cfaabf`  
		Last Modified: Wed, 13 Oct 2021 18:12:19 GMT  
		Size: 4.0 MB (4044630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:182546fad9cb0ec37426aa827c5d867dfb568ef9d5574d5a4e44c187f47bc244`  
		Last Modified: Wed, 13 Oct 2021 18:12:15 GMT  
		Size: 1.4 KB (1415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
