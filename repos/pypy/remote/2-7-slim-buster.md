## `pypy:2-7-slim-buster`

```console
$ docker pull pypy@sha256:6f5a84952e3e2a00a2897e6970d9c6faafe2dfb9a38b2b29a881cc6895041a93
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x

### `pypy:2-7-slim-buster` - linux; amd64

```console
$ docker pull pypy@sha256:a90a21b4180f298a66df0c815492bd468f69ee6db944e9c55eb8b5708ca8ea1b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64148594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bda8debdbc0e6ca28cde13b7b4a889ef0590c979daf80e68024ac74fcfa75968`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 12 Jul 2022 01:20:32 GMT
ADD file:7f2320197e75c5169402827ce0c47d93629331875d76b9f0ddd389244747eccd in / 
# Tue, 12 Jul 2022 01:20:33 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 10:03:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 10:03:42 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 10:03:42 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 10:03:42 GMT
ENV PYPY_VERSION=7.3.9
# Tue, 12 Jul 2022 10:11:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-linux64.tar.bz2'; 			sha256='172a928b0096a7e00b7d58f523f57300c35c3de7f822491e2a7bc845375c23f8'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-aarch64.tar.bz2'; 			sha256='aff4e4dbab53448f662cd01acb2251571d60f836d2f48382a7d8da54ca5b3442'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-linux32.tar.bz2'; 			sha256='bbf4e7343d43c8217099a9bffeed6a1781f4b5a3e186ed1a0befca65e647aeb9'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-s390x.tar.bz2'; 			sha256='62481dd3c6472393ca05eb3a0880c96e4f5921747157607dbaa772a7369cab77'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 12 Jul 2022 10:11:46 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 12 Jul 2022 10:11:46 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 12 Jul 2022 10:11:56 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 12 Jul 2022 10:11:56 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:ac2fb615420c18b61e0693f2569a3d38e3b9b58456b691bac44405e08389a591`  
		Last Modified: Tue, 12 Jul 2022 01:25:22 GMT  
		Size: 27.1 MB (27139850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b96d52db46d3fec6f9af3a2d6aee7f3896a262c0bb204ad5b3f8e5b902fcd5a`  
		Last Modified: Tue, 12 Jul 2022 10:15:21 GMT  
		Size: 2.8 MB (2765517 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea7bbb75fffeeab63a781dfa9400a32e443a01abc07db25da2d44ac8e371e7a`  
		Last Modified: Tue, 12 Jul 2022 10:22:31 GMT  
		Size: 32.1 MB (32074732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baf232ae56e2aef0da3fa8f80880eb7655642f4df04d06d74f0b9e9f1666ce3c`  
		Last Modified: Tue, 12 Jul 2022 10:22:26 GMT  
		Size: 2.2 MB (2168495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-7-slim-buster` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:8ee64d43d37f7df2233bc74c6456d125ca77dffde861762e7824833c0cb8c9c0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60370299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96167069ee98beab6a8a844df99c5dfdf499b9109678f661da501b7fde45b4af`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 12 Jul 2022 00:41:02 GMT
ADD file:d6b43ca12a2cc7f73a66ace962f04878f02eab9345172028d77c21d3dc94fe0c in / 
# Tue, 12 Jul 2022 00:41:03 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 09:25:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 09:25:49 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 09:25:50 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 09:25:51 GMT
ENV PYPY_VERSION=7.3.9
# Tue, 12 Jul 2022 09:35:58 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-linux64.tar.bz2'; 			sha256='172a928b0096a7e00b7d58f523f57300c35c3de7f822491e2a7bc845375c23f8'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-aarch64.tar.bz2'; 			sha256='aff4e4dbab53448f662cd01acb2251571d60f836d2f48382a7d8da54ca5b3442'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-linux32.tar.bz2'; 			sha256='bbf4e7343d43c8217099a9bffeed6a1781f4b5a3e186ed1a0befca65e647aeb9'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-s390x.tar.bz2'; 			sha256='62481dd3c6472393ca05eb3a0880c96e4f5921747157607dbaa772a7369cab77'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 12 Jul 2022 09:35:58 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 12 Jul 2022 09:35:59 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 12 Jul 2022 09:36:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 12 Jul 2022 09:36:16 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:8bd5501da4f4b37ad7488bd0eafa32d8927de3bf1e32747545810f2ca65429ed`  
		Last Modified: Tue, 12 Jul 2022 00:47:14 GMT  
		Size: 25.9 MB (25914236 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:519d1561526d1ddbd49a4e6ead88e10406235b7ff04dde9605f5c4b9f9248ff0`  
		Last Modified: Tue, 12 Jul 2022 09:42:01 GMT  
		Size: 2.6 MB (2634787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:580f1a4dd66694b8345403010e2b67bdf95fa554f5e47202a4349412fd0253b7`  
		Last Modified: Tue, 12 Jul 2022 09:49:19 GMT  
		Size: 29.9 MB (29866716 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9413e10c07e8a70370bad724f6aa33c537d99130d2e5abf9e1947906ad2ffb38`  
		Last Modified: Tue, 12 Jul 2022 09:49:14 GMT  
		Size: 2.0 MB (1954560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-7-slim-buster` - linux; 386

```console
$ docker pull pypy@sha256:95fa1719db40c5b31c30c6a269ac6a601b9bc2607804d69e612d3c67a8d41657
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61674743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ae8007904fd008fcb392fde3cb698dc5a323b721d914a90e377cf081cce278b`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 12 Jul 2022 00:39:54 GMT
ADD file:127048950e335136312b4abd45e2f6dbcdbf1641675573278ae97951686fc50a in / 
# Tue, 12 Jul 2022 00:39:55 GMT
CMD ["bash"]
# Tue, 12 Jul 2022 14:57:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 12 Jul 2022 14:57:15 GMT
ENV LANG=C.UTF-8
# Tue, 12 Jul 2022 14:57:16 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Jul 2022 14:57:17 GMT
ENV PYPY_VERSION=7.3.9
# Tue, 12 Jul 2022 15:07:29 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-linux64.tar.bz2'; 			sha256='172a928b0096a7e00b7d58f523f57300c35c3de7f822491e2a7bc845375c23f8'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-aarch64.tar.bz2'; 			sha256='aff4e4dbab53448f662cd01acb2251571d60f836d2f48382a7d8da54ca5b3442'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-linux32.tar.bz2'; 			sha256='bbf4e7343d43c8217099a9bffeed6a1781f4b5a3e186ed1a0befca65e647aeb9'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-s390x.tar.bz2'; 			sha256='62481dd3c6472393ca05eb3a0880c96e4f5921747157607dbaa772a7369cab77'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 12 Jul 2022 15:07:29 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 12 Jul 2022 15:07:30 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 12 Jul 2022 15:07:41 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 12 Jul 2022 15:07:42 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:3f7bc4b396f6bcb2720b727a14ac5d6a9809a1d7c1a3363baea1fe8d8c6249ff`  
		Last Modified: Tue, 12 Jul 2022 00:46:09 GMT  
		Size: 27.8 MB (27799525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06000652c2eb0f8e31998f21a3a40bddfd71017addf0e9fb3d60ea467b5fa9ab`  
		Last Modified: Tue, 12 Jul 2022 15:13:38 GMT  
		Size: 2.8 MB (2777849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fa09df22afce28bba1cced55488d64b5a73450167c972ecdda5d18d7a64ebcc`  
		Last Modified: Tue, 12 Jul 2022 15:21:16 GMT  
		Size: 29.1 MB (29142847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bde557af84437844a4cefbc55b33089d263d71ef334aacb8be22dd6e009a92c6`  
		Last Modified: Tue, 12 Jul 2022 15:21:11 GMT  
		Size: 2.0 MB (1954522 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-7-slim-buster` - linux; s390x

```console
$ docker pull pypy@sha256:73d8ee462c66edc7e24eb9855241f322c0be49a0724e4efaf210d48be2ba666e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61821734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c9e6d3b536e0ab2a7d483f0c460dc0f110bd6d82cf79bd07238abb90465aa6d`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 02 Aug 2022 00:42:56 GMT
ADD file:e455828726a550da92d8fc424a6d7694b6be24a8ca52a6152e2ee89d4f7269d0 in / 
# Tue, 02 Aug 2022 00:42:58 GMT
CMD ["bash"]
# Tue, 02 Aug 2022 08:09:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 02 Aug 2022 08:09:01 GMT
ENV LANG=C.UTF-8
# Tue, 02 Aug 2022 08:09:01 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 02 Aug 2022 08:09:02 GMT
ENV PYPY_VERSION=7.3.9
# Tue, 02 Aug 2022 08:13:22 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-linux64.tar.bz2'; 			sha256='172a928b0096a7e00b7d58f523f57300c35c3de7f822491e2a7bc845375c23f8'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-aarch64.tar.bz2'; 			sha256='aff4e4dbab53448f662cd01acb2251571d60f836d2f48382a7d8da54ca5b3442'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-linux32.tar.bz2'; 			sha256='bbf4e7343d43c8217099a9bffeed6a1781f4b5a3e186ed1a0befca65e647aeb9'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-s390x.tar.bz2'; 			sha256='62481dd3c6472393ca05eb3a0880c96e4f5921747157607dbaa772a7369cab77'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 02 Aug 2022 08:13:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 02 Aug 2022 08:13:24 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 02 Aug 2022 08:13:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 02 Aug 2022 08:13:37 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:42614a0fa81c110340e6a5a5db155f27bbb6fa8c1e2421b2c2c5f148ea18f35d`  
		Last Modified: Tue, 02 Aug 2022 00:48:34 GMT  
		Size: 25.8 MB (25758761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6be9c495a23d0b3f7620490c0a2c5136c0167f23d6cdd3a538dc6aed3fb68052`  
		Last Modified: Tue, 02 Aug 2022 08:15:35 GMT  
		Size: 2.5 MB (2457495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e50c14c6c2e0451eac5a63c06715d0c8f76e6549a221e52b5f65b99042ca9b8`  
		Last Modified: Tue, 02 Aug 2022 08:17:51 GMT  
		Size: 31.4 MB (31436466 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bb6db7cad3a39710e3267803caf32bf962442c397ab3e26ae31914b65a7b5f`  
		Last Modified: Tue, 02 Aug 2022 08:17:46 GMT  
		Size: 2.2 MB (2169012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
