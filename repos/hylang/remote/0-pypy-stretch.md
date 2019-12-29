## `hylang:0-pypy-stretch`

```console
$ docker pull hylang@sha256:a3956b2adabf48842668de77ff6f3059e4fe4f3ee9917e6bc9cbef794c68b01b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hylang:0-pypy-stretch` - linux; amd64

```console
$ docker pull hylang@sha256:28b0c164674a8dd8aafcc69c30a6ceb23f0c14c29dab537a23842fdb6e371d11
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65154130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99d68dec6564e173eaa64a43ff220c1de3adb31304dc95fcbe48fd33cc32eac3`
-	Default Command: `["hy"]`

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
# Thu, 26 Dec 2019 23:16:23 GMT
ENV PYPY_VERSION=7.3.0
# Thu, 26 Dec 2019 23:17:09 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='d3d549e8f43de820ac3385b698b83fa59b4d7dd6cf3fe34c115f731e26ad8856' ;; 		arm64) pypyArch='aarch64'; sha256='b900241bca7152254c107a632767f49edede99ca6360b9a064141267b47ef598' ;; 		i386) pypyArch='linux32'; sha256='7045b295d38ba0b5ee65bd3f078ca249fcf1de73fedeaab2d6ad78de2eab0f0e' ;; 		ppc64el) pypyArch='ppc64le'; sha256='d6f3b701313df69483b43ebdd21b9652ae5e808b2eea5fbffe3b74b82d2e7433' ;; 		s390x) pypyArch='s390x'; sha256='0fe2f7bbf42ea88b40954d7de773a43179a44f40656f2f58201524be70699544' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2; 	find /usr/local/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		pypy3 --version; 		if [ -f /usr/local/lib_pypy/_ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		cd /usr/local/lib_pypy; 		pypy3 _ssl_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 	find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 26 Dec 2019 23:17:10 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Thu, 26 Dec 2019 23:17:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Thu, 26 Dec 2019 23:17:10 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Thu, 26 Dec 2019 23:17:35 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 26 Dec 2019 23:17:36 GMT
CMD ["pypy3"]
# Fri, 27 Dec 2019 04:18:09 GMT
ENV HY_VERSION=0.17.0
# Fri, 27 Dec 2019 04:18:23 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 27 Dec 2019 04:18:23 GMT
CMD ["hy"]
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
	-	`sha256:0f8ec35f1b5e106ff5bbcc3542af79750b244601a8709abf55ce32b0785a1c56`  
		Last Modified: Thu, 26 Dec 2019 23:20:09 GMT  
		Size: 34.3 MB (34263986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62700c0a9e6c4823d402074faa9ec70af12408dbccef6ce450f36b28537fa7d4`  
		Last Modified: Thu, 26 Dec 2019 23:20:01 GMT  
		Size: 2.1 MB (2140659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4cd285cb55b62155c8d003f6534428f1a74160bd74949684014aa1067f68e03`  
		Last Modified: Fri, 27 Dec 2019 04:19:40 GMT  
		Size: 2.9 MB (2949257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy-stretch` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:3f5a265a42fc932ef0af0089556aafae12ea6b6e8836979d320f81a4cec49e89
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.8 MB (56830573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:468f809d5dba71d8b02fe622273a5f1e5a6261b6f8fcc7a0f0f0096de6b1e3da`
-	Default Command: `["hy"]`

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
# Thu, 26 Dec 2019 22:53:34 GMT
ENV PYPY_VERSION=7.3.0
# Thu, 26 Dec 2019 22:54:45 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='d3d549e8f43de820ac3385b698b83fa59b4d7dd6cf3fe34c115f731e26ad8856' ;; 		arm64) pypyArch='aarch64'; sha256='b900241bca7152254c107a632767f49edede99ca6360b9a064141267b47ef598' ;; 		i386) pypyArch='linux32'; sha256='7045b295d38ba0b5ee65bd3f078ca249fcf1de73fedeaab2d6ad78de2eab0f0e' ;; 		ppc64el) pypyArch='ppc64le'; sha256='d6f3b701313df69483b43ebdd21b9652ae5e808b2eea5fbffe3b74b82d2e7433' ;; 		s390x) pypyArch='s390x'; sha256='0fe2f7bbf42ea88b40954d7de773a43179a44f40656f2f58201524be70699544' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2; 	find /usr/local/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		pypy3 --version; 		if [ -f /usr/local/lib_pypy/_ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		cd /usr/local/lib_pypy; 		pypy3 _ssl_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 	find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 26 Dec 2019 22:54:48 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Thu, 26 Dec 2019 22:54:49 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Thu, 26 Dec 2019 22:54:50 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Thu, 26 Dec 2019 22:55:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 26 Dec 2019 22:55:28 GMT
CMD ["pypy3"]
# Fri, 27 Dec 2019 01:53:05 GMT
ENV HY_VERSION=0.17.0
# Fri, 27 Dec 2019 01:53:35 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 27 Dec 2019 01:53:36 GMT
CMD ["hy"]
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
	-	`sha256:30108d8f767fecbaf6ce9e03c5b7b0f1d9b6fbd6645caa618602d7e51f362a32`  
		Last Modified: Thu, 26 Dec 2019 22:56:44 GMT  
		Size: 28.4 MB (28428543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ea55c4b690f859ab2a54efa10bad7252a011ddb6bbe1e6134f1938efabb046`  
		Last Modified: Thu, 26 Dec 2019 22:56:33 GMT  
		Size: 2.1 MB (2140221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6d39384ee182df2ca896ac0cb42e14db4108e75b7923ce6da4cdf10e96a1151`  
		Last Modified: Fri, 27 Dec 2019 01:56:47 GMT  
		Size: 3.0 MB (2950105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy-stretch` - linux; 386

```console
$ docker pull hylang@sha256:e5b39de01b9b65bc936166c42cdc8e0e14b274325253ba97c47d2b837e4a4be4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67160996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e65207373914eec80c74a35168c6c8488cfd0a13bca6e49975e0889221eebd`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 28 Dec 2019 04:42:05 GMT
ADD file:d43798bcf0e72b342c261b8585dde072d9363d19fab4b8d9f08f15db189f287b in / 
# Sat, 28 Dec 2019 04:42:05 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 14:57:32 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 14:57:32 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 14:57:42 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libexpat1 		libffi6 		libgdbm3 		libsqlite3-0 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 14:57:42 GMT
ENV PYPY_VERSION=7.3.0
# Sat, 28 Dec 2019 14:58:18 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='d3d549e8f43de820ac3385b698b83fa59b4d7dd6cf3fe34c115f731e26ad8856' ;; 		arm64) pypyArch='aarch64'; sha256='b900241bca7152254c107a632767f49edede99ca6360b9a064141267b47ef598' ;; 		i386) pypyArch='linux32'; sha256='7045b295d38ba0b5ee65bd3f078ca249fcf1de73fedeaab2d6ad78de2eab0f0e' ;; 		ppc64el) pypyArch='ppc64le'; sha256='d6f3b701313df69483b43ebdd21b9652ae5e808b2eea5fbffe3b74b82d2e7433' ;; 		s390x) pypyArch='s390x'; sha256='0fe2f7bbf42ea88b40954d7de773a43179a44f40656f2f58201524be70699544' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2; 	find /usr/local/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		pypy3 --version; 		if [ -f /usr/local/lib_pypy/_ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		cd /usr/local/lib_pypy; 		pypy3 _ssl_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 	find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Sat, 28 Dec 2019 14:58:18 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 28 Dec 2019 14:58:18 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 28 Dec 2019 14:58:19 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 28 Dec 2019 14:58:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 28 Dec 2019 14:58:40 GMT
CMD ["pypy3"]
# Sun, 29 Dec 2019 00:15:16 GMT
ENV HY_VERSION=0.17.0
# Sun, 29 Dec 2019 00:15:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sun, 29 Dec 2019 00:15:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2cb401c016d2f9802d5ef9cf6c6dc07251e9f87757a0de0a8df318fb7f00385c`  
		Last Modified: Sat, 28 Dec 2019 04:47:36 GMT  
		Size: 23.2 MB (23152142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f52ff72781e0cb47c754e667648b880a0f67101686b56d9dd1f0308928dbdeb`  
		Last Modified: Sat, 28 Dec 2019 15:01:09 GMT  
		Size: 3.3 MB (3322713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c6b6d735fa5b706100c89a3b1cc47ae25d725dedc0b47457fcb67bb2e8868a7`  
		Last Modified: Sat, 28 Dec 2019 15:01:21 GMT  
		Size: 35.6 MB (35596229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f13e6718211d4eaa28712307fd902ba90ceaaf80e20e071c5ed9337d47269448`  
		Last Modified: Sat, 28 Dec 2019 15:01:08 GMT  
		Size: 2.1 MB (2140472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82f96c48911a6e50957b0c373087b3b531adec7d2f0cb3268b4ce3b8d6134f6`  
		Last Modified: Sun, 29 Dec 2019 00:18:06 GMT  
		Size: 2.9 MB (2949440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy-stretch` - linux; ppc64le

```console
$ docker pull hylang@sha256:6ee6f4b6e70c391f21cd69ff1373f710019f328867ba1c255692ccc10309e153
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.1 MB (60083171 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e8a66eca5675b52e995122733d34cb41a878bcb1a7b57ee4b6c7411d1cda2be`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 28 Dec 2019 04:23:21 GMT
ADD file:a1ee5955ff3ede8df9558f4bec0c7962d54c43374f857e1da7e2639ddf82a9f1 in / 
# Sat, 28 Dec 2019 04:23:24 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 14:24:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 14:24:52 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 14:25:11 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libexpat1 		libffi6 		libgdbm3 		libsqlite3-0 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 14:25:13 GMT
ENV PYPY_VERSION=7.3.0
# Sat, 28 Dec 2019 14:26:29 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='d3d549e8f43de820ac3385b698b83fa59b4d7dd6cf3fe34c115f731e26ad8856' ;; 		arm64) pypyArch='aarch64'; sha256='b900241bca7152254c107a632767f49edede99ca6360b9a064141267b47ef598' ;; 		i386) pypyArch='linux32'; sha256='7045b295d38ba0b5ee65bd3f078ca249fcf1de73fedeaab2d6ad78de2eab0f0e' ;; 		ppc64el) pypyArch='ppc64le'; sha256='d6f3b701313df69483b43ebdd21b9652ae5e808b2eea5fbffe3b74b82d2e7433' ;; 		s390x) pypyArch='s390x'; sha256='0fe2f7bbf42ea88b40954d7de773a43179a44f40656f2f58201524be70699544' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2; 	find /usr/local/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		pypy3 --version; 		if [ -f /usr/local/lib_pypy/_ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		cd /usr/local/lib_pypy; 		pypy3 _ssl_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 	find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Sat, 28 Dec 2019 14:26:32 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 28 Dec 2019 14:26:35 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 28 Dec 2019 14:26:37 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 28 Dec 2019 14:27:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 28 Dec 2019 14:27:24 GMT
CMD ["pypy3"]
# Sun, 29 Dec 2019 01:46:06 GMT
ENV HY_VERSION=0.17.0
# Sun, 29 Dec 2019 01:46:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sun, 29 Dec 2019 01:46:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:af52e7ef6e83efadeae17be91daa6ecf61b7dfb39709c29be9b24876e60c0e36`  
		Last Modified: Sat, 28 Dec 2019 04:33:19 GMT  
		Size: 22.8 MB (22800791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726be2ccb991dbc9c941fbe88c5f880cf4710ef3c3fca9ed447e2e27bf343660`  
		Last Modified: Sat, 28 Dec 2019 14:29:11 GMT  
		Size: 2.9 MB (2938436 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c213f5d600e4919ceddcd067aa917a9979a9eb5847405ce1f090e147a9f8d0d`  
		Last Modified: Sat, 28 Dec 2019 14:29:18 GMT  
		Size: 29.3 MB (29252683 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f9801cae5c57718d0576f02bb593a43c6930ed0fdfeb9bbef2b80a77afaaf32`  
		Last Modified: Sat, 28 Dec 2019 14:29:11 GMT  
		Size: 2.1 MB (2140403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68406cd1c1ebd0efab093f763afb856372573855c72b7d7513f8d7177f9a6b2e`  
		Last Modified: Sun, 29 Dec 2019 01:51:06 GMT  
		Size: 3.0 MB (2950858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy-stretch` - linux; s390x

```console
$ docker pull hylang@sha256:442480205f05156b65d7d46404248c3e0066d0530f14b4a0e16a07478ec19df4
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63789524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef9c990ae9b3f0180f6419935f21daf7f19224ce194910cf72abb430f7fd2038`
-	Default Command: `["hy"]`

```dockerfile
# Sat, 28 Dec 2019 04:43:21 GMT
ADD file:f5d0e8fb7b76fc65fc5a0951e7d647f26d110f5c92d4effe2ada348f661c87af in / 
# Sat, 28 Dec 2019 04:43:21 GMT
CMD ["bash"]
# Sat, 28 Dec 2019 05:03:29 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 28 Dec 2019 05:03:29 GMT
ENV LANG=C.UTF-8
# Sat, 28 Dec 2019 09:47:25 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libexpat1 		libffi6 		libgdbm3 		libsqlite3-0 	&& rm -rf /var/lib/apt/lists/*
# Sat, 28 Dec 2019 09:47:25 GMT
ENV PYPY_VERSION=7.3.0
# Sat, 28 Dec 2019 09:47:47 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='d3d549e8f43de820ac3385b698b83fa59b4d7dd6cf3fe34c115f731e26ad8856' ;; 		arm64) pypyArch='aarch64'; sha256='b900241bca7152254c107a632767f49edede99ca6360b9a064141267b47ef598' ;; 		i386) pypyArch='linux32'; sha256='7045b295d38ba0b5ee65bd3f078ca249fcf1de73fedeaab2d6ad78de2eab0f0e' ;; 		ppc64el) pypyArch='ppc64le'; sha256='d6f3b701313df69483b43ebdd21b9652ae5e808b2eea5fbffe3b74b82d2e7433' ;; 		s390x) pypyArch='s390x'; sha256='0fe2f7bbf42ea88b40954d7de773a43179a44f40656f2f58201524be70699544' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2; 	find /usr/local/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		pypy3 --version; 		if [ -f /usr/local/lib_pypy/_ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		cd /usr/local/lib_pypy; 		pypy3 _ssl_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 	find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Sat, 28 Dec 2019 09:47:48 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Sat, 28 Dec 2019 09:47:48 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Sat, 28 Dec 2019 09:47:48 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Sat, 28 Dec 2019 09:48:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Sat, 28 Dec 2019 09:48:01 GMT
CMD ["pypy3"]
# Sat, 28 Dec 2019 10:56:03 GMT
ENV HY_VERSION=0.17.0
# Sat, 28 Dec 2019 10:56:12 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Sat, 28 Dec 2019 10:56:12 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9498763e47873a85a1a6b3ba1f12b6936fcd769bb6b0d094c36c0dd6435bb902`  
		Last Modified: Sat, 28 Dec 2019 04:46:38 GMT  
		Size: 22.4 MB (22380154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77a381cb14a0f5584ebe98f977fffb19f4ccb96292e3c50f02dbd3db0b81a5ff`  
		Last Modified: Sat, 28 Dec 2019 09:48:43 GMT  
		Size: 3.0 MB (3017735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c56c270815660d91166aa9a698d1e28e3120ebc4993588e6b2bd85ba917585e`  
		Last Modified: Sat, 28 Dec 2019 09:48:49 GMT  
		Size: 33.3 MB (33302618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ddad620556a9badcc7dbeb65b5a56130509fb40b32c0829e75c2c762f453580`  
		Last Modified: Sat, 28 Dec 2019 09:48:43 GMT  
		Size: 2.1 MB (2139915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea3a59c95974dcb6ba683ee0956501dd31a8b40a027e5281a406b6d394cbac5`  
		Last Modified: Sat, 28 Dec 2019 10:57:49 GMT  
		Size: 2.9 MB (2949102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
