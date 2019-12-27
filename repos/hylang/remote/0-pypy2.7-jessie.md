## `hylang:0-pypy2.7-jessie`

```console
$ docker pull hylang@sha256:a9e8113400c9a6cc2d29fe4a4ffa38070ff07698772bc411c9006b71e43662b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386

### `hylang:0-pypy2.7-jessie` - linux; amd64

```console
$ docker pull hylang@sha256:40b2863555272a6c23658ee6a2555779c7850790f5ebb8c5d54a0ba6047440bf
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72470991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:444e51753d893162126890fed8c8ecb5701ef6a7894e09c0d9935fe91dffccae`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 22 Nov 2019 14:56:04 GMT
ADD file:41e78f98c436ed4f05c337e67e10439bb860bbea86c78368cc0e80100026cf40 in / 
# Fri, 22 Nov 2019 14:56:04 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:59:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Nov 2019 00:59:21 GMT
ENV LANG=C.UTF-8
# Sat, 23 Nov 2019 01:01:15 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libexpat1 		libffi6 		libgdbm3 		libsqlite3-0 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Dec 2019 23:08:14 GMT
ENV PYPY_VERSION=7.3.0
# Thu, 26 Dec 2019 23:12:53 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='f4950a54378ac637da2a6defa52d6ffed96af12fcd5d74e1182fb834883c9826' ;; 		arm64) pypyArch='aarch64'; sha256='a3dd8d5e2a656849fa344dce4679d854a19bc4a096a0cf62b46a1be127a5d56c' ;; 		i386) pypyArch='linux32'; sha256='eac1308b7d523003a5f6d20f58406d52ab14611bcec750122ae513a5a35110db' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy2.7-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2; 	find /usr/local/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		pypy --version; 		if [ -f /usr/local/lib_pypy/_ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		cd /usr/local/lib_pypy; 		pypy _ssl_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 	find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 26 Dec 2019 23:12:54 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Thu, 26 Dec 2019 23:12:54 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Thu, 26 Dec 2019 23:12:54 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Thu, 26 Dec 2019 23:15:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 26 Dec 2019 23:15:27 GMT
CMD ["pypy"]
# Fri, 27 Dec 2019 04:18:27 GMT
ENV HY_VERSION=0.17.0
# Fri, 27 Dec 2019 04:18:34 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 27 Dec 2019 04:18:34 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:02d147d362835efa14b8a83e3b4a7dd20dd53dd0ba1619316a691acb9e614c13`  
		Last Modified: Fri, 22 Nov 2019 15:03:20 GMT  
		Size: 30.2 MB (30159468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:739e238c2628b72e5b5fc22a054b55be6c60fdc578b99c2539b5267891464028`  
		Last Modified: Sat, 23 Nov 2019 01:10:40 GMT  
		Size: 2.8 MB (2811806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a8339f98ebb2138f89ed84f9088fb4b10a946dfb7442dd61f468e9bac81436f`  
		Last Modified: Thu, 26 Dec 2019 23:19:27 GMT  
		Size: 34.8 MB (34834078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f45eb516ed2408efa87016bc569d1ac3018913e309597c5352fcc6e3519877`  
		Last Modified: Thu, 26 Dec 2019 23:19:16 GMT  
		Size: 2.2 MB (2162153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42c90fd3abbe75ab29e2d6914594d62d4af1fe42d9ec1327f001a2430419e4fa`  
		Last Modified: Fri, 27 Dec 2019 04:19:47 GMT  
		Size: 2.5 MB (2503486 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy2.7-jessie` - linux; 386

```console
$ docker pull hylang@sha256:355791d1c71c2dbf5e26a1a65f7948ed4980b908ad7303d28dbbc928d5f51cc3
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.7 MB (74678948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:96fa4e4211f335a260f011657fafb1447835c0b4c12cdc45ebdb7e9fcda31134`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 22 Nov 2019 16:51:12 GMT
ADD file:1f7e88c23b6592ff21924a70ace43e8fc04f335f7ac1a66cd670fb2354971101 in / 
# Fri, 22 Nov 2019 16:51:12 GMT
CMD ["bash"]
# Sat, 23 Nov 2019 00:19:11 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 23 Nov 2019 00:19:11 GMT
ENV LANG=C.UTF-8
# Sat, 23 Nov 2019 00:22:14 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		ca-certificates 		libexpat1 		libffi6 		libgdbm3 		libsqlite3-0 	&& rm -rf /var/lib/apt/lists/*
# Thu, 26 Dec 2019 22:19:10 GMT
ENV PYPY_VERSION=7.3.0
# Thu, 26 Dec 2019 22:26:29 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='f4950a54378ac637da2a6defa52d6ffed96af12fcd5d74e1182fb834883c9826' ;; 		arm64) pypyArch='aarch64'; sha256='a3dd8d5e2a656849fa344dce4679d854a19bc4a096a0cf62b46a1be127a5d56c' ;; 		i386) pypyArch='linux32'; sha256='eac1308b7d523003a5f6d20f58406d52ab14611bcec750122ae513a5a35110db' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy2.7-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2; 	find /usr/local/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		pypy --version; 		if [ -f /usr/local/lib_pypy/_ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		cd /usr/local/lib_pypy; 		pypy _ssl_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 	find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 26 Dec 2019 22:26:29 GMT
ENV PYTHON_PIP_VERSION=19.3.1
# Thu, 26 Dec 2019 22:26:29 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/ffe826207a010164265d9cc807978e3604d18ca0/get-pip.py
# Thu, 26 Dec 2019 22:26:30 GMT
ENV PYTHON_GET_PIP_SHA256=b86f36cc4345ae87bfd4f10ef6b2dbfa7a872fbff70608a1e43944d283fd0eee
# Thu, 26 Dec 2019 22:30:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 26 Dec 2019 22:30:27 GMT
CMD ["pypy"]
# Fri, 27 Dec 2019 01:34:41 GMT
ENV HY_VERSION=0.17.0
# Fri, 27 Dec 2019 01:34:48 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Fri, 27 Dec 2019 01:34:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2f932a0e4a53f737c635c9f57f47f35c873b5af5539e695d348cf3b6ea6e6f9f`  
		Last Modified: Fri, 22 Nov 2019 16:59:05 GMT  
		Size: 30.3 MB (30304773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31825f80a2f0ede8882558d9d4b93e64e7f83b807192abed4b0c0cf85426411e`  
		Last Modified: Sat, 23 Nov 2019 00:35:15 GMT  
		Size: 4.9 MB (4920023 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b3012ae0bd981f08eff116ab9781ebd611b6c42a7a763f5d9e5c34693b504bf`  
		Last Modified: Thu, 26 Dec 2019 22:34:26 GMT  
		Size: 34.8 MB (34788704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e45efbd087800c7e02fff517c4e118d2068f82b19fd16e2a96c0cb7ed29e1299`  
		Last Modified: Thu, 26 Dec 2019 22:34:14 GMT  
		Size: 2.2 MB (2162026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aac49b1558edb89e7d703b7c46a04a6646fb90d04824602ae9936de9239d6804`  
		Last Modified: Fri, 27 Dec 2019 01:37:09 GMT  
		Size: 2.5 MB (2503422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
