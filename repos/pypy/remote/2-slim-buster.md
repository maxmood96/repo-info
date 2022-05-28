## `pypy:2-slim-buster`

```console
$ docker pull pypy@sha256:a490e7fdf3548ef6d79af95c504e5be0661037e57a98aa45c3fcb25d0e2f09d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x

### `pypy:2-slim-buster` - linux; amd64

```console
$ docker pull pypy@sha256:8d6767296e3c3fcfd698a2af4fa3cea02235e9f437c0dedb2a149eaf2b4c2de8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.1 MB (64148993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e798d7cfc4bc4b129345992effe04f84a2cf5dfaecd58823269e7ff4e117e0e`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 11 May 2022 01:20:37 GMT
ADD file:76b454ddb7dfe4d22afae844a7e67e7e5fb4570dae2e21bbd259a1f2e5839f33 in / 
# Wed, 11 May 2022 01:20:37 GMT
CMD ["bash"]
# Wed, 11 May 2022 14:58:15 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 14:58:15 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 14:58:15 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 14:58:16 GMT
ENV PYPY_VERSION=7.3.9
# Wed, 11 May 2022 15:06:29 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-linux64.tar.bz2'; 			sha256='172a928b0096a7e00b7d58f523f57300c35c3de7f822491e2a7bc845375c23f8'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-aarch64.tar.bz2'; 			sha256='aff4e4dbab53448f662cd01acb2251571d60f836d2f48382a7d8da54ca5b3442'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-linux32.tar.bz2'; 			sha256='bbf4e7343d43c8217099a9bffeed6a1781f4b5a3e186ed1a0befca65e647aeb9'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-s390x.tar.bz2'; 			sha256='62481dd3c6472393ca05eb3a0880c96e4f5921747157607dbaa772a7369cab77'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 11 May 2022 15:06:30 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 11 May 2022 15:06:30 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 11 May 2022 15:06:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 11 May 2022 15:06:39 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:c32ce6654453d35d0b3dde45d195adeee586ffba0a683006ee06748c077c01fa`  
		Last Modified: Wed, 11 May 2022 01:25:58 GMT  
		Size: 27.1 MB (27140722 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c938c72aae9500aa635c54db4be5f094fb7b7658094fa4482bcaf326eed81167`  
		Last Modified: Wed, 11 May 2022 15:09:58 GMT  
		Size: 2.8 MB (2765139 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e773e6b04a666534e1bf6a2f028ebb62155066ffe2dc760d7976dd5831162086`  
		Last Modified: Wed, 11 May 2022 15:16:31 GMT  
		Size: 32.1 MB (32074690 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64b1f47dbafa4b6f50d864e8267a677e600c46527e0c7a5af07ad0a4ea968c36`  
		Last Modified: Wed, 11 May 2022 15:16:25 GMT  
		Size: 2.2 MB (2168442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-slim-buster` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:db5f14791d5aa94b221afc0eca96eaabfa2dd0f0ee1799c77a7568bacfdaa08b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.4 MB (60370045 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d1ecc7353a86ea6ef91d9ba1241fa1d96564bdd72740836098854e8f3edeefb`
-	Default Command: `["pypy"]`

```dockerfile
# Sat, 28 May 2022 00:41:05 GMT
ADD file:d0e42d603f275c040783ec7b6c051200815492fc35b73110234dfcd584e6cdec in / 
# Sat, 28 May 2022 00:41:05 GMT
CMD ["bash"]
# Sat, 28 May 2022 07:19:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 07:19:14 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 07:19:15 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 07:19:16 GMT
ENV PYPY_VERSION=7.3.9
# Sat, 28 May 2022 07:26:32 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-linux64.tar.bz2'; 			sha256='172a928b0096a7e00b7d58f523f57300c35c3de7f822491e2a7bc845375c23f8'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-aarch64.tar.bz2'; 			sha256='aff4e4dbab53448f662cd01acb2251571d60f836d2f48382a7d8da54ca5b3442'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-linux32.tar.bz2'; 			sha256='bbf4e7343d43c8217099a9bffeed6a1781f4b5a3e186ed1a0befca65e647aeb9'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-s390x.tar.bz2'; 			sha256='62481dd3c6472393ca05eb3a0880c96e4f5921747157607dbaa772a7369cab77'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Sat, 28 May 2022 07:26:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Sat, 28 May 2022 07:26:33 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Sat, 28 May 2022 07:26:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 28 May 2022 07:26:46 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:4931fb8ba4223cb35034141162105ee5482122692b2931eb69eec912ce64606d`  
		Last Modified: Sat, 28 May 2022 00:48:26 GMT  
		Size: 25.9 MB (25914033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ce05c34f1947a9b7dfea84ea400dfa3c309f10ef6b5452c1e7cee5c8f7b7404`  
		Last Modified: Sat, 28 May 2022 07:31:45 GMT  
		Size: 2.6 MB (2634726 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db2d4ae766da854a8bd164fce84587869259750be418b4a9d8c0011eafc6a3f6`  
		Last Modified: Sat, 28 May 2022 07:36:21 GMT  
		Size: 29.9 MB (29866688 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ff3460083e8b78c7df554493a235f7c48a8f90eb500ccb05dce6c4740282ba9`  
		Last Modified: Sat, 28 May 2022 07:36:16 GMT  
		Size: 2.0 MB (1954598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-slim-buster` - linux; 386

```console
$ docker pull pypy@sha256:6e33f9d73f275a3820fed9babf77f29cabc16211ed76905fdde0e135c97c7c58
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61674671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d83bc4fb3e33a0b9fd6f9fbb42119cfeb11d1f2c71a092ecdd3cc398e38e5b`
-	Default Command: `["pypy"]`

```dockerfile
# Sat, 28 May 2022 00:40:01 GMT
ADD file:9aea7a35c215cdd778adec1dd5213973ef9b4830110e4550f2ead85679551ee5 in / 
# Sat, 28 May 2022 00:40:01 GMT
CMD ["bash"]
# Sat, 28 May 2022 07:46:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Sat, 28 May 2022 07:46:10 GMT
ENV LANG=C.UTF-8
# Sat, 28 May 2022 07:46:11 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 May 2022 07:46:12 GMT
ENV PYPY_VERSION=7.3.9
# Sat, 28 May 2022 07:56:27 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-linux64.tar.bz2'; 			sha256='172a928b0096a7e00b7d58f523f57300c35c3de7f822491e2a7bc845375c23f8'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-aarch64.tar.bz2'; 			sha256='aff4e4dbab53448f662cd01acb2251571d60f836d2f48382a7d8da54ca5b3442'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-linux32.tar.bz2'; 			sha256='bbf4e7343d43c8217099a9bffeed6a1781f4b5a3e186ed1a0befca65e647aeb9'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-s390x.tar.bz2'; 			sha256='62481dd3c6472393ca05eb3a0880c96e4f5921747157607dbaa772a7369cab77'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Sat, 28 May 2022 07:56:27 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Sat, 28 May 2022 07:56:28 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Sat, 28 May 2022 07:56:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 28 May 2022 07:56:40 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:40837b3d848885c0b0c031d6d950b38e6a26962a5ee49704cb3ca2d2db535617`  
		Last Modified: Sat, 28 May 2022 00:47:36 GMT  
		Size: 27.8 MB (27799572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2102e83d6636305bfeb197f30a8a078cbfc1f8bfaa726f151f5aad999a992f6c`  
		Last Modified: Sat, 28 May 2022 08:02:33 GMT  
		Size: 2.8 MB (2777747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec5041ea261e395bf5988d8a9e0e8857a0bb5041b585ffb5611a7ccf143f3acd`  
		Last Modified: Sat, 28 May 2022 08:10:19 GMT  
		Size: 29.1 MB (29142799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b165e13c69bc31dd8796661bf87f62ba8c9ae35c016000881e3042d5ebe29ee`  
		Last Modified: Sat, 28 May 2022 08:10:15 GMT  
		Size: 2.0 MB (1954553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-slim-buster` - linux; s390x

```console
$ docker pull pypy@sha256:b8f1334578bbaad471205984b828ce54721e7a639bd019db421c4ee54119c605
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61821497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2358f2f87c78861e617977eb6f11234b55d2be0ff57b115c18d625b490260c74`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 11 May 2022 00:44:47 GMT
ADD file:28b1e60f65391906bebd81248a4da766172138fab99b8b9e6b18bce76afea02d in / 
# Wed, 11 May 2022 00:44:49 GMT
CMD ["bash"]
# Wed, 11 May 2022 05:31:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 11 May 2022 05:31:25 GMT
ENV LANG=C.UTF-8
# Wed, 11 May 2022 05:31:25 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 11 May 2022 05:31:26 GMT
ENV PYPY_VERSION=7.3.9
# Wed, 11 May 2022 05:35:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-linux64.tar.bz2'; 			sha256='172a928b0096a7e00b7d58f523f57300c35c3de7f822491e2a7bc845375c23f8'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-aarch64.tar.bz2'; 			sha256='aff4e4dbab53448f662cd01acb2251571d60f836d2f48382a7d8da54ca5b3442'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-linux32.tar.bz2'; 			sha256='bbf4e7343d43c8217099a9bffeed6a1781f4b5a3e186ed1a0befca65e647aeb9'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.9-s390x.tar.bz2'; 			sha256='62481dd3c6472393ca05eb3a0880c96e4f5921747157607dbaa772a7369cab77'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 11 May 2022 05:35:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 11 May 2022 05:35:55 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 11 May 2022 05:36:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 11 May 2022 05:36:09 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:bf64474a39a67000556a4502abd4584010a062b942cf8e2545d0502d38ffa150`  
		Last Modified: Wed, 11 May 2022 00:50:43 GMT  
		Size: 25.8 MB (25758738 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ae388629e4ab68082b9986b6ffcd989062288fe6ac7fd28e86ea0a8e609f7c`  
		Last Modified: Wed, 11 May 2022 05:38:09 GMT  
		Size: 2.5 MB (2457232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6d949d569d1abdecac9d13b6c4fbffcadd73f96b296f88226a34608283dec63`  
		Last Modified: Wed, 11 May 2022 05:40:31 GMT  
		Size: 31.4 MB (31436477 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c90c445d880b579e07477c7dfd39e21eb8f786378b94f059461269793c2512b0`  
		Last Modified: Wed, 11 May 2022 05:40:25 GMT  
		Size: 2.2 MB (2169050 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
