## `pypy:2-slim-bullseye`

```console
$ docker pull pypy@sha256:dfaac765cf14ab1ee0874d900131445a034add2ef8c8fde2b7b7604cb36581f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `pypy:2-slim-bullseye` - linux; amd64

```console
$ docker pull pypy@sha256:aedf0dbe27df39cf58cca50beb7f351e0ae3aa4105baeba20832e5631b79c673
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65677028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ee93ee95a76ac2f91dba2312b2f239e0b8e0dbf9bbc3b7bb1f508dbd055b70`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 23 May 2023 01:20:14 GMT
ADD file:88252a7f118b4d6f55dd5baf49dbcaa053c9d6172c652963c1151fa76f625e44 in / 
# Tue, 23 May 2023 01:20:14 GMT
CMD ["bash"]
# Tue, 23 May 2023 09:23:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 09:23:14 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 09:23:14 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 09:23:14 GMT
ENV PYPY_VERSION=7.3.11
# Tue, 23 May 2023 09:28:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-linux64.tar.bz2'; 			sha256='ba8ed958a905c0735a4cfff2875c25089954dc020e087d982b0ffa5b9da316cd'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-aarch64.tar.bz2'; 			sha256='ea924da1defe9325ef760e288b04f984614e405580f5321eb6a5c8f539bd415a'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-linux32.tar.bz2'; 			sha256='30fd245fab7068c96a75b9ff1323ac55174c64fc8c4751cceb4b7a9bedc1851e'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-s390x.tar.bz2'; 			sha256='8fe9481c473178e53266983678684a70fe0c42bafc95f1807bf3ef28770316d4'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 23 May 2023 09:28:38 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 23 May 2023 09:28:38 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 23 May 2023 09:28:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 23 May 2023 09:28:46 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:f03b40093957615593f2ed142961afb6b540507e0b47e3f7626ba5e02efbbbf1`  
		Last Modified: Tue, 23 May 2023 01:24:08 GMT  
		Size: 31.4 MB (31403586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef4426d8a39b22d45c659296da115a57c83a7bd01bec87fe57bf10c84c2f43e0`  
		Last Modified: Tue, 23 May 2023 09:30:51 GMT  
		Size: 1.1 MB (1066658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb3326c4e7cc9c4067f2dd470f1800e9558ca62a3b0723a4742a715383add16`  
		Last Modified: Tue, 23 May 2023 09:34:22 GMT  
		Size: 31.0 MB (31035647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd79a4fca05bb6a2bc90c89601cb937fc6a1b6fd7ac1327aaa436208781546cb`  
		Last Modified: Tue, 23 May 2023 09:34:17 GMT  
		Size: 2.2 MB (2171137 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:211c3d4b8ad1302f6db4e64fbca3ff8a3fb55fa95623469fa79cb824203a4720
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62334994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cdc1a6495d3d49d1d83624a3fa2575a8030bb4c73e2cc7ae59866d6444c97d5a`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 23 May 2023 00:43:15 GMT
ADD file:0fee550e337f1bd111a7ef785a9553674f25649f37deffa4aa8107ef6445d259 in / 
# Tue, 23 May 2023 00:43:15 GMT
CMD ["bash"]
# Tue, 23 May 2023 07:38:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 23 May 2023 07:38:58 GMT
ENV LANG=C.UTF-8
# Tue, 23 May 2023 07:38:58 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 23 May 2023 07:38:58 GMT
ENV PYPY_VERSION=7.3.11
# Tue, 23 May 2023 07:44:32 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-linux64.tar.bz2'; 			sha256='ba8ed958a905c0735a4cfff2875c25089954dc020e087d982b0ffa5b9da316cd'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-aarch64.tar.bz2'; 			sha256='ea924da1defe9325ef760e288b04f984614e405580f5321eb6a5c8f539bd415a'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-linux32.tar.bz2'; 			sha256='30fd245fab7068c96a75b9ff1323ac55174c64fc8c4751cceb4b7a9bedc1851e'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-s390x.tar.bz2'; 			sha256='8fe9481c473178e53266983678684a70fe0c42bafc95f1807bf3ef28770316d4'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 23 May 2023 07:44:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 23 May 2023 07:44:32 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 23 May 2023 07:44:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 23 May 2023 07:44:40 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:d981f2c20c93e1c57a46cd87bc5b9a554be5323072a0d0ab4b354aabd237bbcf`  
		Last Modified: Tue, 23 May 2023 00:46:07 GMT  
		Size: 30.1 MB (30052747 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ad14405a354f422fcd20348b3c255a6d898f3ae0652e40eaec11ee1c12b54bc`  
		Last Modified: Tue, 23 May 2023 07:46:40 GMT  
		Size: 1.1 MB (1054167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:493edaa056a3fdb1aaba6d3d95776b8a8e3793276cf0fcc6d538cae433c82d63`  
		Last Modified: Tue, 23 May 2023 07:50:01 GMT  
		Size: 29.1 MB (29056906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa4241aacb2068319b0980c8bfd7e6fffabde8a73b7ae596c97ad911ef87411`  
		Last Modified: Tue, 23 May 2023 07:49:57 GMT  
		Size: 2.2 MB (2171174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-slim-bullseye` - linux; 386

```console
$ docker pull pypy@sha256:67dc384b4118d389b81b3de8b216382eafdea6651368b1ff3546d960cb147793
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62742166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c85c8ee7c53ce8e9998fe97dfc51a0d8e8957abbe332f5bade07c4ec71779ed`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 03 May 2023 00:00:58 GMT
ADD file:caea439e2dbe0148904e3b9a0c5a843d2d0b7c196725d2b41790594e64dcdce8 in / 
# Wed, 03 May 2023 00:00:58 GMT
CMD ["bash"]
# Wed, 03 May 2023 18:01:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 03 May 2023 18:01:11 GMT
ENV LANG=C.UTF-8
# Wed, 03 May 2023 18:01:11 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 May 2023 18:01:11 GMT
ENV PYPY_VERSION=7.3.11
# Wed, 03 May 2023 18:07:34 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-linux64.tar.bz2'; 			sha256='ba8ed958a905c0735a4cfff2875c25089954dc020e087d982b0ffa5b9da316cd'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-aarch64.tar.bz2'; 			sha256='ea924da1defe9325ef760e288b04f984614e405580f5321eb6a5c8f539bd415a'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-linux32.tar.bz2'; 			sha256='30fd245fab7068c96a75b9ff1323ac55174c64fc8c4751cceb4b7a9bedc1851e'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-s390x.tar.bz2'; 			sha256='8fe9481c473178e53266983678684a70fe0c42bafc95f1807bf3ef28770316d4'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 03 May 2023 18:07:34 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 03 May 2023 18:07:34 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 03 May 2023 18:07:44 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 03 May 2023 18:07:44 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:10b34014bd1c165cc57a10e7492f17dce658513b7329319fe6c193c85bf752db`  
		Last Modified: Wed, 03 May 2023 00:05:12 GMT  
		Size: 32.4 MB (32388208 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c07eef1b5bc3ddca3a12f8e1e5a7dfbdcd6a9417cf03d7f84312647c30981e`  
		Last Modified: Wed, 03 May 2023 18:09:57 GMT  
		Size: 1.1 MB (1079130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32cb2a9a9f438eb71b6398059e62c3fd35e1542a3f72469dd7161a581efbfe8f`  
		Last Modified: Wed, 03 May 2023 18:13:41 GMT  
		Size: 27.1 MB (27103695 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aec868f9052d2d7888ecd931e2e0b7962291f066907ad57a76d857f927cfa8d3`  
		Last Modified: Wed, 03 May 2023 18:13:35 GMT  
		Size: 2.2 MB (2171133 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
