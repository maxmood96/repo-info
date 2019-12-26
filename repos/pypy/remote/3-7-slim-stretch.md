## `pypy:3-7-slim-stretch`

```console
$ docker pull pypy@sha256:927859f0908f4f266c803a38cca0cdee80e957acecd012a3574a1d239d771cad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `pypy:3-7-slim-stretch` - linux; amd64

```console
$ docker pull pypy@sha256:16a2a2f5484c7e3088a141cbe17ccfff1822a11bf587ec3fdd579f348aba201c
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.1 MB (59062815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7b5cefde88fe87203f51e6480246770d88f00ab44d5dbb4c18f8feb3de1f769`
-	Default Command: `["pypy3"]`

```dockerfile
# Fri, 22 Nov 2019 14:59:24 GMT
ADD file:2c1f5e08834f13ccb9c2326204eb2556e03239d00171e75755c7195289374c61 in / 
# Fri, 22 Nov 2019 14:59:25 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 01:08:50 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Nov 2019 01:08:50 GMT
ENV LANG=C.UTF-8
# Sat, 23 Nov 2019 01:08:59 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libexpat1 		libffi6 		libgdbm3 		libsqlite3-0 	&& rm -rf /var/lib/apt/lists/*
# Sat, 23 Nov 2019 01:08:59 GMT
ENV PYPY_VERSION=7.2.0
# Sat, 23 Nov 2019 01:09:31 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='aa128e555ad0fe5c4c15104ae0903052bd232b6e3a73f5fe023d27b8fd0d6089' ;; 		arm64) pypyArch='aarch64'; sha256='f82dc9dc6c692417ee9727f23beae75364a5757ebdc657a2a1d0010ac3ad17ab' ;; 		i386) pypyArch='linux32'; sha256='45e99de197cb3e974cfc8d45e0076ad2066852e61e56b3eafd1237efafd2c43e' ;; 		ppc64el) pypyArch='ppc64le'; sha256='6aef73a3b68e9a6c062cadd83d3db16790960cf97401ca6f2aad2195e9b05c35' ;; 		s390x) pypyArch='s390x'; sha256='a11da8118064db102d159e9221319c428b298c4a87f26166fd6ae94be8d6ae0d' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2; 	find /usr/local/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		pypy3 --version; 		if [ -f /usr/local/lib_pypy/_ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		cd /usr/local/lib_pypy; 		pypy3 _ssl_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 	find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Sat, 23 Nov 2019 01:09:31 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 23 Nov 2019 01:09:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 23 Nov 2019 01:09:32 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 23 Nov 2019 01:09:49 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 23 Nov 2019 01:09:49 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:d599a449871ee73b960e80d176b989365dfecb4c8f337bf21e8853862403ee9b`  
		Last Modified: Fri, 22 Nov 2019 15:06:36 GMT  
		Size: 22.5 MB (22524572 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd964983d6f13a372e89fb427173503af587a6a4b734b4836d407ecb16c51dba`  
		Last Modified: Sat, 23 Nov 2019 01:11:28 GMT  
		Size: 3.3 MB (3275656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7f36d66c8f572999b7b8d8494b64548cac2a53eca01cefbe01d7e9a2937619b`  
		Last Modified: Sat, 23 Nov 2019 01:11:36 GMT  
		Size: 31.1 MB (31122500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a4a83eb3840ae9dc36756a6478e23eb74ab59a8d0a05cb4f074056d411168bb`  
		Last Modified: Sat, 23 Nov 2019 01:11:28 GMT  
		Size: 2.1 MB (2140087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:3-7-slim-stretch` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:e3ee14e045f1d4f47f4f60ab7c8513742a592089ad152b232160fd1554a037e5
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.6 MB (53619999 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cf2dd9c84a83f589fa1d70b854527dbb9369fda720c3de1dc5f5f84d2ad53fe`
-	Default Command: `["pypy3"]`

```dockerfile
# Fri, 22 Nov 2019 13:45:50 GMT
ADD file:8e4d0a1e6805c641fc9d18ebad82e4b01d85c6cb9f87d1ef47d75d150212a392 in / 
# Fri, 22 Nov 2019 13:45:53 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 21:45:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2019 21:45:01 GMT
ENV LANG=C.UTF-8
# Fri, 22 Nov 2019 21:45:18 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libexpat1 		libffi6 		libgdbm3 		libsqlite3-0 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 21:45:19 GMT
ENV PYPY_VERSION=7.2.0
# Fri, 22 Nov 2019 21:46:16 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='aa128e555ad0fe5c4c15104ae0903052bd232b6e3a73f5fe023d27b8fd0d6089' ;; 		arm64) pypyArch='aarch64'; sha256='f82dc9dc6c692417ee9727f23beae75364a5757ebdc657a2a1d0010ac3ad17ab' ;; 		i386) pypyArch='linux32'; sha256='45e99de197cb3e974cfc8d45e0076ad2066852e61e56b3eafd1237efafd2c43e' ;; 		ppc64el) pypyArch='ppc64le'; sha256='6aef73a3b68e9a6c062cadd83d3db16790960cf97401ca6f2aad2195e9b05c35' ;; 		s390x) pypyArch='s390x'; sha256='a11da8118064db102d159e9221319c428b298c4a87f26166fd6ae94be8d6ae0d' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2; 	find /usr/local/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		pypy3 --version; 		if [ -f /usr/local/lib_pypy/_ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		cd /usr/local/lib_pypy; 		pypy3 _ssl_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 	find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Fri, 22 Nov 2019 21:46:18 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Fri, 22 Nov 2019 21:46:19 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Fri, 22 Nov 2019 21:46:20 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Fri, 22 Nov 2019 21:46:55 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 22 Nov 2019 21:46:56 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:98a64bf4db7d2219b4fdd8182188d9422810dee890e997095bfb564a0482eed6`  
		Last Modified: Fri, 22 Nov 2019 13:52:17 GMT  
		Size: 20.4 MB (20385759 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:378f3b58a43c378c6aa4a2a8f76f8c07721d1027670b93f0062acfd25265c77d`  
		Last Modified: Fri, 22 Nov 2019 21:48:13 GMT  
		Size: 2.9 MB (2925945 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c58a80b25de895a44374fb1361b52b0519df4cd7ddac0c66155628f216ffdfb`  
		Last Modified: Fri, 22 Nov 2019 21:48:23 GMT  
		Size: 28.2 MB (28168398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9e01b28b9397ce2ed120fd220dbffedc8057c77e36b5617551c1933a0a941c6`  
		Last Modified: Fri, 22 Nov 2019 21:48:13 GMT  
		Size: 2.1 MB (2139897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:3-7-slim-stretch` - linux; 386

```console
$ docker pull pypy@sha256:339e8a8f68f832346019564697d4509480428b3438ff1ad2b57e26f9a781f00d
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64211537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27d5999422c8bc96c2f52562020e61c77dfa252c00c50a97a342e6bff5822234`
-	Default Command: `["pypy3"]`

```dockerfile
# Fri, 22 Nov 2019 16:54:44 GMT
ADD file:19d04f738434c76e2dbd14b48de2f0f03afa883b15f638c6ecbbf382df03567c in / 
# Fri, 22 Nov 2019 16:54:44 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:33:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Nov 2019 00:33:12 GMT
ENV LANG=C.UTF-8
# Sat, 23 Nov 2019 00:33:22 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libexpat1 		libffi6 		libgdbm3 		libsqlite3-0 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Dec 2019 22:31:30 GMT
ENV PYPY_VERSION=7.3.0
# Thu, 26 Dec 2019 22:32:34 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='d3d549e8f43de820ac3385b698b83fa59b4d7dd6cf3fe34c115f731e26ad8856' ;; 		arm64) pypyArch='aarch64'; sha256='b900241bca7152254c107a632767f49edede99ca6360b9a064141267b47ef598' ;; 		i386) pypyArch='linux32'; sha256='7045b295d38ba0b5ee65bd3f078ca249fcf1de73fedeaab2d6ad78de2eab0f0e' ;; 		ppc64el) pypyArch='ppc64le'; sha256='d6f3b701313df69483b43ebdd21b9652ae5e808b2eea5fbffe3b74b82d2e7433' ;; 		s390x) pypyArch='s390x'; sha256='0fe2f7bbf42ea88b40954d7de773a43179a44f40656f2f58201524be70699544' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2; 	find /usr/local/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		pypy3 --version; 		if [ -f /usr/local/lib_pypy/_ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		cd /usr/local/lib_pypy; 		pypy3 _ssl_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 	find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 26 Dec 2019 22:32:35 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Thu, 26 Dec 2019 22:32:35 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Thu, 26 Dec 2019 22:32:35 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Thu, 26 Dec 2019 22:33:02 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 26 Dec 2019 22:33:02 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:f26c9a85c76e393c9f2313b30e82d09f933d2dd4883620de242c7d21f8812e91`  
		Last Modified: Fri, 22 Nov 2019 17:03:03 GMT  
		Size: 23.2 MB (23152070 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:628d0cf78e46abc6f7ac686d3b6e714675e01ded5d81a161e19004c968046966`  
		Last Modified: Sat, 23 Nov 2019 00:35:51 GMT  
		Size: 3.3 MB (3322760 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a552d52935f4155fbe7fb342dc289ff4f4ab3745ad60cb459056488f9cc93190`  
		Last Modified: Thu, 26 Dec 2019 22:35:14 GMT  
		Size: 35.6 MB (35596221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c27f118382cd8909dcc2b51078cae1a332148ec99a17381c896f2bd7f04fd7e`  
		Last Modified: Thu, 26 Dec 2019 22:35:03 GMT  
		Size: 2.1 MB (2140486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:3-7-slim-stretch` - linux; ppc64le

```console
$ docker pull pypy@sha256:a37e8c33b2a763729f725ac7d06b69aac583665822a8f3b9e11b58636b067742
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.1 MB (57132636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a181de835c732e55ba7c574f6837cde150c91a1ead306fc4ebe91f40f0dcbac`
-	Default Command: `["pypy3"]`

```dockerfile
# Fri, 22 Nov 2019 14:58:56 GMT
ADD file:008b263d3f37793269f09e110a1abd704f86b507b99ae445723cf0e6a5586e1f in / 
# Fri, 22 Nov 2019 14:59:00 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 06:59:33 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Nov 2019 06:59:35 GMT
ENV LANG=C.UTF-8
# Sat, 23 Nov 2019 06:59:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libexpat1 		libffi6 		libgdbm3 		libsqlite3-0 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Dec 2019 22:14:17 GMT
ENV PYPY_VERSION=7.3.0
# Thu, 26 Dec 2019 22:16:03 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='d3d549e8f43de820ac3385b698b83fa59b4d7dd6cf3fe34c115f731e26ad8856' ;; 		arm64) pypyArch='aarch64'; sha256='b900241bca7152254c107a632767f49edede99ca6360b9a064141267b47ef598' ;; 		i386) pypyArch='linux32'; sha256='7045b295d38ba0b5ee65bd3f078ca249fcf1de73fedeaab2d6ad78de2eab0f0e' ;; 		ppc64el) pypyArch='ppc64le'; sha256='d6f3b701313df69483b43ebdd21b9652ae5e808b2eea5fbffe3b74b82d2e7433' ;; 		s390x) pypyArch='s390x'; sha256='0fe2f7bbf42ea88b40954d7de773a43179a44f40656f2f58201524be70699544' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2; 	find /usr/local/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		pypy3 --version; 		if [ -f /usr/local/lib_pypy/_ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		cd /usr/local/lib_pypy; 		pypy3 _ssl_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 	find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 26 Dec 2019 22:16:08 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Thu, 26 Dec 2019 22:16:09 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Thu, 26 Dec 2019 22:16:10 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Thu, 26 Dec 2019 22:16:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 26 Dec 2019 22:17:00 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:c02d2c3f92fbdc231ef0e07f16cfa00067d39fba564f4eef4d83d42d2b884c62`  
		Last Modified: Fri, 22 Nov 2019 15:08:29 GMT  
		Size: 22.8 MB (22800737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c431d65612ba17e2a6da4a102046447001f37d6b6758ae1531c53c52ffabd798`  
		Last Modified: Sat, 23 Nov 2019 07:04:04 GMT  
		Size: 2.9 MB (2938436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43523202507c832fe737e07bbe29c1331c848b28000539d35a23b19f29d9734b`  
		Last Modified: Thu, 26 Dec 2019 22:19:09 GMT  
		Size: 29.3 MB (29252971 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c1cdc55edacbb63a646901b54af2ec2fefaaee41bd84e75fbdea47a261c73e4`  
		Last Modified: Thu, 26 Dec 2019 22:18:58 GMT  
		Size: 2.1 MB (2140492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:3-7-slim-stretch` - linux; s390x

```console
$ docker pull pypy@sha256:9f1d6b3fbbee4aaebec35c02ac629930d0253df9b7c651766abcbd257f53b0a7
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60749072 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa0fdfb2e5c71609e5b97899f9b92a6f951a2a2ad372d28e3f82d8d7ab84b1b8`
-	Default Command: `["pypy3"]`

```dockerfile
# Fri, 22 Nov 2019 10:42:08 GMT
ADD file:5b9fe0ab2a3414cd6541119cb1e784ad8afb2d4c723b0f1ddfa7484724293253 in / 
# Fri, 22 Nov 2019 10:42:09 GMT
CMD ["bash"]
# Fri, 22 Nov 2019 12:53:22 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 22 Nov 2019 12:53:22 GMT
ENV LANG=C.UTF-8
# Fri, 22 Nov 2019 12:53:28 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libexpat1 		libffi6 		libgdbm3 		libsqlite3-0 	&& rm -rf /var/lib/apt/lists/*
# Fri, 22 Nov 2019 12:53:28 GMT
ENV PYPY_VERSION=7.2.0
# Fri, 22 Nov 2019 12:53:52 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='aa128e555ad0fe5c4c15104ae0903052bd232b6e3a73f5fe023d27b8fd0d6089' ;; 		arm64) pypyArch='aarch64'; sha256='f82dc9dc6c692417ee9727f23beae75364a5757ebdc657a2a1d0010ac3ad17ab' ;; 		i386) pypyArch='linux32'; sha256='45e99de197cb3e974cfc8d45e0076ad2066852e61e56b3eafd1237efafd2c43e' ;; 		ppc64el) pypyArch='ppc64le'; sha256='6aef73a3b68e9a6c062cadd83d3db16790960cf97401ca6f2aad2195e9b05c35' ;; 		s390x) pypyArch='s390x'; sha256='a11da8118064db102d159e9221319c428b298c4a87f26166fd6ae94be8d6ae0d' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2; 	find /usr/local/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		pypy3 --version; 		if [ -f /usr/local/lib_pypy/_ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		cd /usr/local/lib_pypy; 		pypy3 _ssl_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 	find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Fri, 22 Nov 2019 12:53:52 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Fri, 22 Nov 2019 12:53:52 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Fri, 22 Nov 2019 12:53:53 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Fri, 22 Nov 2019 12:54:05 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 22 Nov 2019 12:54:05 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:8628e24097cd41352930f9c875f9a32291ecd440d5180f25b2e5b1b4c8f628bd`  
		Last Modified: Fri, 22 Nov 2019 10:46:30 GMT  
		Size: 22.4 MB (22380089 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a18eec7a8b33ab42d98db513126f0b30ed7aeca243582fc1b8a41dbc251257b`  
		Last Modified: Fri, 22 Nov 2019 12:54:54 GMT  
		Size: 3.0 MB (3017708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b33d6e27a6354716340bca6efbfcde967335d04e3658de1d0c54f266a081146`  
		Last Modified: Fri, 22 Nov 2019 12:55:01 GMT  
		Size: 33.2 MB (33211711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:447b0236deffc835d2738f1230e88694719335a2dd0661ce3863b240afcf34a8`  
		Last Modified: Fri, 22 Nov 2019 12:54:54 GMT  
		Size: 2.1 MB (2139564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
