## `pypy:slim`

```console
$ docker pull pypy@sha256:5ca1297a74d63a9d4302c00bbae61f7bb687a00d82272802f0b13ff3949b75c8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x

### `pypy:slim` - linux; amd64

```console
$ docker pull pypy@sha256:171f3cdb85c732958b040d6f7510ff6e034088656dffd35be727ad5c2c55075f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67947476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82b9cbc064f4c9f62748c2fec5d891a5b00bf1d2e81616609cf62fd2087cc953`
-	Default Command: `["pypy3"]`

```dockerfile
# Fri, 11 Dec 2020 02:06:10 GMT
ADD file:3a7bff4e139bcacc5831fd70a035c130a91b5da001dd91c08b2acd635c7064e8 in / 
# Fri, 11 Dec 2020 02:06:10 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 19:21:03 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 19:21:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 19:21:10 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Dec 2020 19:21:10 GMT
ENV PYPY_VERSION=7.3.3
# Fri, 11 Dec 2020 19:22:31 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='4fb85fdd516482cab727bb9473b066ff8fb672940dedf7ccc32bf92957d29e0a' ;; 		arm64) pypyArch='aarch64'; sha256='bc82cf7f0182b942a2cfad4a0d167f364bfbf18f434e100a2fe62bc88547ac9b' ;; 		i386) pypyArch='linux32'; sha256='f183c61e66fd2c536a65695bd7ff770748c2884c235a589b9c6ac63690770c69' ;; 		s390x) pypyArch='s390x'; sha256='0de9c33ff3500c6e7fd273d0a6d341bc839b0298f697c4d6fe141f2b54c5c3e2' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://downloads.python.org/pypy/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -svT '/opt/pypy/bin/pypy3' '/usr/local/bin/pypy3'; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Fri, 11 Dec 2020 19:22:31 GMT
ENV PYTHON_PIP_VERSION=20.3.1
# Fri, 11 Dec 2020 19:22:31 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/91630a4867b1f93ba0a12aa81d0ec4ecc1e7eeb9/get-pip.py
# Fri, 11 Dec 2020 19:22:32 GMT
ENV PYTHON_GET_PIP_SHA256=d48ae68f297cac54db17e4107b800faae0e5210131f9f386c30c0166bf8d81b7
# Fri, 11 Dec 2020 19:22:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 11 Dec 2020 19:22:48 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:6ec7b7d162b24bd6df88abde89ceb6d7bbc2be927f025c9dd061af2b0c328cfe`  
		Last Modified: Fri, 11 Dec 2020 02:12:26 GMT  
		Size: 27.1 MB (27099295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:862ff65907287da7787a1512d3d8837f7bea201508670fdaa8a0edbd815e629c`  
		Last Modified: Fri, 11 Dec 2020 19:25:08 GMT  
		Size: 2.7 MB (2742693 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6509f8f75bdfe6a2bfa071a33dcca1b6429f19a2be6ef768a59d65d761fa61d`  
		Last Modified: Fri, 11 Dec 2020 19:25:49 GMT  
		Size: 35.7 MB (35694261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09bc1219df187efefd298c4f018e90c678d05ccca6c647809d12bc0aa190870c`  
		Last Modified: Fri, 11 Dec 2020 19:25:43 GMT  
		Size: 2.4 MB (2411227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:slim` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:4eb92b6be8cc4d555c0bc9109fbd89568f8998729c533231aabd8976b723faf8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.3 MB (60346040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba7d4f07cd386b14aa5969cb01fb8add9e266406a3dffdce897fa24fc21a5ae`
-	Default Command: `["pypy3"]`

```dockerfile
# Fri, 11 Dec 2020 02:45:53 GMT
ADD file:a5a2f039c00bc638b88cefdff4c3cd1865b4d415bf80c4fe6b496d975af7cc1f in / 
# Fri, 11 Dec 2020 02:45:57 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 16:52:14 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 16:52:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 16:52:30 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Dec 2020 16:52:31 GMT
ENV PYPY_VERSION=7.3.3
# Fri, 11 Dec 2020 16:55:54 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='4fb85fdd516482cab727bb9473b066ff8fb672940dedf7ccc32bf92957d29e0a' ;; 		arm64) pypyArch='aarch64'; sha256='bc82cf7f0182b942a2cfad4a0d167f364bfbf18f434e100a2fe62bc88547ac9b' ;; 		i386) pypyArch='linux32'; sha256='f183c61e66fd2c536a65695bd7ff770748c2884c235a589b9c6ac63690770c69' ;; 		s390x) pypyArch='s390x'; sha256='0de9c33ff3500c6e7fd273d0a6d341bc839b0298f697c4d6fe141f2b54c5c3e2' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://downloads.python.org/pypy/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -svT '/opt/pypy/bin/pypy3' '/usr/local/bin/pypy3'; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Fri, 11 Dec 2020 16:56:00 GMT
ENV PYTHON_PIP_VERSION=20.3.1
# Fri, 11 Dec 2020 16:56:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/91630a4867b1f93ba0a12aa81d0ec4ecc1e7eeb9/get-pip.py
# Fri, 11 Dec 2020 16:56:05 GMT
ENV PYTHON_GET_PIP_SHA256=d48ae68f297cac54db17e4107b800faae0e5210131f9f386c30c0166bf8d81b7
# Fri, 11 Dec 2020 16:56:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 11 Dec 2020 16:56:50 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:c9648d7fcbb6d597cf33916d8fcd207fde8ec05d764b4480d4f3e884e142a902`  
		Last Modified: Fri, 11 Dec 2020 02:53:14 GMT  
		Size: 25.9 MB (25856191 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f827548d2e9ffb879dc53392f8b6e3b31acc4faef6c0274f311cee165c7492f6`  
		Last Modified: Fri, 11 Dec 2020 17:00:07 GMT  
		Size: 2.6 MB (2606496 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97da6e3285517e9b5b978da6105f91e27eb3d911871e2b73487004fa654f5399`  
		Last Modified: Fri, 11 Dec 2020 17:01:11 GMT  
		Size: 29.5 MB (29471058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f93495180296d27d33acbd23293fcf5e77116c4a15b4b87552398343042033e4`  
		Last Modified: Fri, 11 Dec 2020 17:01:02 GMT  
		Size: 2.4 MB (2412295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:slim` - linux; 386

```console
$ docker pull pypy@sha256:2b7f0eade80e911f84a0519c4acaf8535c17e951b863c6cf4d311a938aad6bf1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70916172 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52043c9a91426cb789954e9fbb264e40020d1ce59ba4112359b9d4301dc8731`
-	Default Command: `["pypy3"]`

```dockerfile
# Fri, 11 Dec 2020 02:03:07 GMT
ADD file:a0879774b23f70c4db7f7b04736cca142beb0b22e93f5952364ca990a1675552 in / 
# Fri, 11 Dec 2020 02:03:08 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 22:18:45 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 22:18:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 22:18:55 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Dec 2020 22:18:55 GMT
ENV PYPY_VERSION=7.3.3
# Fri, 11 Dec 2020 22:21:36 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='4fb85fdd516482cab727bb9473b066ff8fb672940dedf7ccc32bf92957d29e0a' ;; 		arm64) pypyArch='aarch64'; sha256='bc82cf7f0182b942a2cfad4a0d167f364bfbf18f434e100a2fe62bc88547ac9b' ;; 		i386) pypyArch='linux32'; sha256='f183c61e66fd2c536a65695bd7ff770748c2884c235a589b9c6ac63690770c69' ;; 		s390x) pypyArch='s390x'; sha256='0de9c33ff3500c6e7fd273d0a6d341bc839b0298f697c4d6fe141f2b54c5c3e2' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://downloads.python.org/pypy/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -svT '/opt/pypy/bin/pypy3' '/usr/local/bin/pypy3'; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Fri, 11 Dec 2020 22:21:36 GMT
ENV PYTHON_PIP_VERSION=20.3.1
# Fri, 11 Dec 2020 22:21:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/91630a4867b1f93ba0a12aa81d0ec4ecc1e7eeb9/get-pip.py
# Fri, 11 Dec 2020 22:21:37 GMT
ENV PYTHON_GET_PIP_SHA256=d48ae68f297cac54db17e4107b800faae0e5210131f9f386c30c0166bf8d81b7
# Fri, 11 Dec 2020 22:21:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 11 Dec 2020 22:21:57 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:cfec07a090788e68b692f30d34e11dc7af0f1c8112fbc846e8e40e24faf882d7`  
		Last Modified: Fri, 11 Dec 2020 02:09:41 GMT  
		Size: 27.8 MB (27757584 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7afc78f63aaea6458a1464eb07ba0cdb68d083175bebee11d5d502b846e12b1a`  
		Last Modified: Fri, 11 Dec 2020 22:25:40 GMT  
		Size: 2.8 MB (2752978 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:335377511c8ea3b6078dce069427f74b41c903fd2fab3afba4ed19e1f5fd6f45`  
		Last Modified: Fri, 11 Dec 2020 22:26:58 GMT  
		Size: 38.0 MB (37994743 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d689a89d57dfab12988df6900634326a46798790575f63b6c2c3f8ea9f99c8e6`  
		Last Modified: Fri, 11 Dec 2020 22:26:46 GMT  
		Size: 2.4 MB (2410867 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:slim` - linux; s390x

```console
$ docker pull pypy@sha256:efb2c73c43bd7a2e4a683445658eb44b39f6ba634d118329618591b324163d3e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63202461 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99295a0db6d357d5aa93061567faf7f3df9f99689ea2fb3c7d337538e30c9ede`
-	Default Command: `["pypy3"]`

```dockerfile
# Fri, 11 Dec 2020 02:12:11 GMT
ADD file:db86ce5a1665b6d8ac734c54ac249a811c58484f569b935b14772445962428aa in / 
# Fri, 11 Dec 2020 02:12:15 GMT
CMD ["bash"]
# Fri, 11 Dec 2020 16:19:47 GMT
ENV LANG=C.UTF-8
# Fri, 11 Dec 2020 16:20:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Fri, 11 Dec 2020 16:20:01 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 11 Dec 2020 16:20:02 GMT
ENV PYPY_VERSION=7.3.3
# Fri, 11 Dec 2020 16:20:48 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='4fb85fdd516482cab727bb9473b066ff8fb672940dedf7ccc32bf92957d29e0a' ;; 		arm64) pypyArch='aarch64'; sha256='bc82cf7f0182b942a2cfad4a0d167f364bfbf18f434e100a2fe62bc88547ac9b' ;; 		i386) pypyArch='linux32'; sha256='f183c61e66fd2c536a65695bd7ff770748c2884c235a589b9c6ac63690770c69' ;; 		s390x) pypyArch='s390x'; sha256='0de9c33ff3500c6e7fd273d0a6d341bc839b0298f697c4d6fe141f2b54c5c3e2' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://downloads.python.org/pypy/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -svT '/opt/pypy/bin/pypy3' '/usr/local/bin/pypy3'; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Fri, 11 Dec 2020 16:20:54 GMT
ENV PYTHON_PIP_VERSION=20.3.1
# Fri, 11 Dec 2020 16:20:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/91630a4867b1f93ba0a12aa81d0ec4ecc1e7eeb9/get-pip.py
# Fri, 11 Dec 2020 16:20:55 GMT
ENV PYTHON_GET_PIP_SHA256=d48ae68f297cac54db17e4107b800faae0e5210131f9f386c30c0166bf8d81b7
# Fri, 11 Dec 2020 16:21:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 11 Dec 2020 16:21:14 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:f4cf10ca9f31aab0854647d7878dc4db838e93b892b843dde3db24f2e909a106`  
		Last Modified: Fri, 11 Dec 2020 02:17:07 GMT  
		Size: 25.7 MB (25713957 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1873488019a5a723e31f96e4bfefafcfd2bf9df4c7cbd724308f1aaaa9205d3`  
		Last Modified: Fri, 11 Dec 2020 16:25:26 GMT  
		Size: 2.4 MB (2432982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2792abcfee60efeb3ae7dc16b0480f596e1400364109fc4a24fb4bc7d93ddc74`  
		Last Modified: Fri, 11 Dec 2020 16:25:33 GMT  
		Size: 32.6 MB (32643947 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aa7bb28261118f424126d05a62de9dcb6a22e726949bf538092f612662d4c57`  
		Last Modified: Fri, 11 Dec 2020 16:25:26 GMT  
		Size: 2.4 MB (2411575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
