## `pypy:2-7-slim-jessie`

```console
$ docker pull pypy@sha256:a4ecfeac36cf57072023eec8674ca49a08dbed505144b4c58ddf7b87b3004421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386

### `pypy:2-7-slim-jessie` - linux; amd64

```console
$ docker pull pypy@sha256:95077b9c5fd5606ce5e016365e76c797ae3572a7ecb791e23a4ada7eee666b50
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69988821 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea28df5dfb361797818685a19e5cfaecb06a053586abf90105d99f66a635b43`
-	Default Command: `["pypy"]`

```dockerfile
# Sat, 01 Feb 2020 17:21:22 GMT
ADD file:7bddae780bfc4ce751148aec0e77e665e08c4c031b4e054a9f6b0e9920498285 in / 
# Sat, 01 Feb 2020 17:21:22 GMT
CMD ["bash"]
# Sun, 02 Feb 2020 06:41:12 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sun, 02 Feb 2020 06:41:12 GMT
ENV LANG=C.UTF-8
# Sun, 02 Feb 2020 06:43:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libexpat1 		libffi6 		libgdbm3 		libsqlite3-0 	&& rm -rf /var/lib/apt/lists/*
# Sun, 02 Feb 2020 06:43:03 GMT
ENV PYPY_VERSION=7.3.0
# Sun, 02 Feb 2020 06:47:33 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='f4950a54378ac637da2a6defa52d6ffed96af12fcd5d74e1182fb834883c9826' ;; 		arm64) pypyArch='aarch64'; sha256='a3dd8d5e2a656849fa344dce4679d854a19bc4a096a0cf62b46a1be127a5d56c' ;; 		i386) pypyArch='linux32'; sha256='eac1308b7d523003a5f6d20f58406d52ab14611bcec750122ae513a5a35110db' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy2.7-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2; 	find /usr/local/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		pypy --version; 		if [ -f /usr/local/lib_pypy/_ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		cd /usr/local/lib_pypy; 		pypy _ssl_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 	find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Sun, 02 Feb 2020 06:47:34 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Wed, 05 Feb 2020 23:38:47 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Wed, 05 Feb 2020 23:38:47 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Wed, 05 Feb 2020 23:41:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 05 Feb 2020 23:41:07 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:6f2295d35e78f75bc28bbc7b81c7a49bcc54eea446127fc14035418dd3d32456`  
		Last Modified: Sat, 01 Feb 2020 17:26:47 GMT  
		Size: 30.2 MB (30159539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfd6b2a8a21502c7db0a2909ec8d9f240cd32b9abe839e6fbfd415ab3d11be15`  
		Last Modified: Sun, 02 Feb 2020 06:53:40 GMT  
		Size: 2.8 MB (2811858 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27d75e6a0ad096240d08d2281327e8dcd4d0a608ca84317331e2c653b81012d5`  
		Last Modified: Sun, 02 Feb 2020 06:53:50 GMT  
		Size: 34.8 MB (34833855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfd7e0d16d37654aeab8331638af39b397dfa16acc57143ce553d8e7219b4f5f`  
		Last Modified: Wed, 05 Feb 2020 23:42:36 GMT  
		Size: 2.2 MB (2183569 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-7-slim-jessie` - linux; 386

```console
$ docker pull pypy@sha256:e9282ac40ee063f9dadf6c0a94ab1f123e0f66fbb7634076117463b82331c7af
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72196733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e904df41cd4f0050c48f99311e51fbf430c04573a5ebd2ae19f319f0073d77c9`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 26 Feb 2020 00:32:49 GMT
ADD file:461678302b53245e7da21eb00da4b637c44c16b9f1ea8b26c293c09d16cf6484 in / 
# Wed, 26 Feb 2020 00:32:49 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 11:10:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 11:10:54 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 11:13:51 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libexpat1 		libffi6 		libgdbm3 		libsqlite3-0 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 11:13:52 GMT
ENV PYPY_VERSION=7.3.0
# Wed, 26 Feb 2020 11:21:01 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='f4950a54378ac637da2a6defa52d6ffed96af12fcd5d74e1182fb834883c9826' ;; 		arm64) pypyArch='aarch64'; sha256='a3dd8d5e2a656849fa344dce4679d854a19bc4a096a0cf62b46a1be127a5d56c' ;; 		i386) pypyArch='linux32'; sha256='eac1308b7d523003a5f6d20f58406d52ab14611bcec750122ae513a5a35110db' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy2.7-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2; 	find /usr/local/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		pypy --version; 		if [ -f /usr/local/lib_pypy/_ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		cd /usr/local/lib_pypy; 		pypy _ssl_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 	find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 26 Feb 2020 11:21:01 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Wed, 26 Feb 2020 11:21:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Wed, 26 Feb 2020 11:21:02 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Wed, 26 Feb 2020 11:24:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 26 Feb 2020 11:24:52 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:65e414d7e49a526c536bc2da24146128fcd893eac421bb7a1be5ead50f5c2a98`  
		Last Modified: Wed, 26 Feb 2020 00:39:10 GMT  
		Size: 30.3 MB (30304519 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b39f90b199d60b76554a4380bb89cf368361f35e6cd8385edcb4c8678fda3e1`  
		Last Modified: Wed, 26 Feb 2020 11:28:41 GMT  
		Size: 4.9 MB (4920009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f60b62c7cb65f40f16601a8b3a5834002e3161d468b0ac9f2488b364d941a603`  
		Last Modified: Wed, 26 Feb 2020 11:28:57 GMT  
		Size: 34.8 MB (34788659 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ba889d00bee776eb25d2948ff28fb64e2d672ceb600ced1cd157bd537b4bc39`  
		Last Modified: Wed, 26 Feb 2020 11:28:40 GMT  
		Size: 2.2 MB (2183546 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
