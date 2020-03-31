## `pypy:2-7-slim`

```console
$ docker pull pypy@sha256:adf3971dd0a047e2990c4ccd444244149e8601a1150057993b7ed604f644a770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386

### `pypy:2-7-slim` - linux; amd64

```console
$ docker pull pypy@sha256:02dd84890969e1414a859bd2c0d11b6ebcda542c19560a20b96c3420ea44c6b6
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69988499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bf3809b53ec94af372e7c419629f87a2e3a9665a8271d605632d02b0874839`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 26 Feb 2020 00:38:14 GMT
ADD file:e136713a1415b6bdfe20d8e37a2b6def6eb2c81ad08ea67b73ac1216107ab73e in / 
# Wed, 26 Feb 2020 00:38:14 GMT
CMD ["bash"]
# Wed, 26 Feb 2020 14:25:49 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2020 14:25:49 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2020 14:27:30 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libexpat1 		libffi6 		libgdbm3 		libsqlite3-0 	&& rm -rf /var/lib/apt/lists/*
# Wed, 26 Feb 2020 14:27:30 GMT
ENV PYPY_VERSION=7.3.0
# Wed, 26 Feb 2020 14:31:57 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='f4950a54378ac637da2a6defa52d6ffed96af12fcd5d74e1182fb834883c9826' ;; 		arm64) pypyArch='aarch64'; sha256='a3dd8d5e2a656849fa344dce4679d854a19bc4a096a0cf62b46a1be127a5d56c' ;; 		i386) pypyArch='linux32'; sha256='eac1308b7d523003a5f6d20f58406d52ab14611bcec750122ae513a5a35110db' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy2.7-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2; 	find /usr/local/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		pypy --version; 		if [ -f /usr/local/lib_pypy/_ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		cd /usr/local/lib_pypy; 		pypy _ssl_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 	find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 26 Feb 2020 14:31:57 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Wed, 26 Feb 2020 14:31:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Wed, 26 Feb 2020 14:31:58 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Wed, 26 Feb 2020 14:34:32 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 26 Feb 2020 14:34:33 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:ad10394a96ec2ef0a20a97cf25199c27e8251f0a596a02431d18fee7d5e4f534`  
		Last Modified: Wed, 26 Feb 2020 00:44:53 GMT  
		Size: 30.2 MB (30159549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:719c4fc830522ddb769cbf7bb72dcbabbc47e37d59919d3b002c60e20efaae2e`  
		Last Modified: Wed, 26 Feb 2020 14:37:19 GMT  
		Size: 2.8 MB (2811829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23df844299e1bca8a38f26477a6ae6e6e6146a298157be8137a1492d366ba5a`  
		Last Modified: Wed, 26 Feb 2020 14:37:27 GMT  
		Size: 34.8 MB (34833623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6b69fecfab651719eaa9f36ea9bd9456622aade59a56f6dd8e0e050b170f280`  
		Last Modified: Wed, 26 Feb 2020 14:37:19 GMT  
		Size: 2.2 MB (2183498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-7-slim` - linux; 386

```console
$ docker pull pypy@sha256:a7366e2d49088736ac9a572aa4419270d452fa82956010aec449e1f0b97dd262
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72196761 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:158234445df7ee7109e5d39af788c24483d6ebaebf1da182e04c28c8cad2362e`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 31 Mar 2020 00:40:13 GMT
ADD file:2fef3918dbc0e4a571fb5c42761c36fd7b6067f4da67b2001a1091d4991dc975 in / 
# Tue, 31 Mar 2020 00:40:14 GMT
CMD ["bash"]
# Tue, 31 Mar 2020 02:07:25 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 31 Mar 2020 02:07:25 GMT
ENV LANG=C.UTF-8
# Tue, 31 Mar 2020 02:10:01 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libexpat1 		libffi6 		libgdbm3 		libsqlite3-0 	&& rm -rf /var/lib/apt/lists/*
# Tue, 31 Mar 2020 02:10:01 GMT
ENV PYPY_VERSION=7.3.0
# Tue, 31 Mar 2020 02:16:14 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='f4950a54378ac637da2a6defa52d6ffed96af12fcd5d74e1182fb834883c9826' ;; 		arm64) pypyArch='aarch64'; sha256='a3dd8d5e2a656849fa344dce4679d854a19bc4a096a0cf62b46a1be127a5d56c' ;; 		i386) pypyArch='linux32'; sha256='eac1308b7d523003a5f6d20f58406d52ab14611bcec750122ae513a5a35110db' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy2.7-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2; 	find /usr/local/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		pypy --version; 		if [ -f /usr/local/lib_pypy/_ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		cd /usr/local/lib_pypy; 		pypy _ssl_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 	find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 31 Mar 2020 02:16:14 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Tue, 31 Mar 2020 02:16:15 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Tue, 31 Mar 2020 02:16:15 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Tue, 31 Mar 2020 02:19:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 31 Mar 2020 02:19:40 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:209ae9a5f2c1dabd03575777ed654bad317ab0b58cca07a6336d6db4679b9fdb`  
		Last Modified: Tue, 31 Mar 2020 00:46:06 GMT  
		Size: 30.3 MB (30304535 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0d4484c0a5ddcda4e46f49270c49332bc8cb0da8e902165886a763076369885`  
		Last Modified: Tue, 31 Mar 2020 02:22:36 GMT  
		Size: 4.9 MB (4919972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c766f75f4c888a26d64b50e82f0d40147c245d8b79dbf450b28211995a193f`  
		Last Modified: Tue, 31 Mar 2020 02:22:49 GMT  
		Size: 34.8 MB (34788624 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce2d2d9623d72ef972605f1e98fabbcef6a008a9463022ce5ab8b4c50dde08d`  
		Last Modified: Tue, 31 Mar 2020 02:22:36 GMT  
		Size: 2.2 MB (2183630 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
