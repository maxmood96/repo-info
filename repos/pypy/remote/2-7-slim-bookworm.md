## `pypy:2-7-slim-bookworm`

```console
$ docker pull pypy@sha256:01f98f98a616f16ecb6e11013a1cbc44c6514b0e203a02ea87832fc015192ae2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `pypy:2-7-slim-bookworm` - linux; amd64

```console
$ docker pull pypy@sha256:825a948810c5db41606ff8e2c39e0664862059ece5b61c5dd9afe8f2b86d43c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65660498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a8b9eb4fdc40507692fd628929d215cd06633be0404c4f1737826d8ba5009e4`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 11 Oct 2023 18:34:50 GMT
ADD file:55ad846fa191e603f48090eae0e4a7149c4066b94406593ec1898ad2c3347937 in / 
# Wed, 11 Oct 2023 18:34:51 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 02:52:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 02:52:57 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 02:52:57 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 02:56:36 GMT
ENV PYPY_VERSION=7.3.13
# Thu, 12 Oct 2023 02:56:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-linux64.tar.bz2'; 			sha256='e41ceb5dc6c4d3a9311ed5f88edfeedbf3e8abbd1ed3c4f2e151a90a5cf4e1d7'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-aarch64.tar.bz2'; 			sha256='f1e20f833cc86a097c1f1318069fc17d01c3988678c1438fe27ed567fcb5cfd0'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-linux32.tar.bz2'; 			sha256='b727d2e759a740f45bab1e333029d001c4384b52949bcbb4bd2ad7912eae8dad'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-s390x.tar.bz2'; 			sha256='fbb2f3d92831c02b094f17e9609b95a6202d4bdcddae437e380ab14388d4556e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 12 Oct 2023 02:56:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 12 Oct 2023 02:56:51 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 12 Oct 2023 02:57:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 12 Oct 2023 02:57:00 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:a378f10b321842c3042cdeff4f6997f34f4cb21f2eff27704b7f6193ab7b5fea`  
		Last Modified: Wed, 11 Oct 2023 18:39:34 GMT  
		Size: 29.1 MB (29149874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca7a35ec99b84224f62697cfb0da82b2e424c41659c7003182e565e0d22252a`  
		Last Modified: Thu, 12 Oct 2023 02:58:33 GMT  
		Size: 3.5 MB (3494482 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f0737585cb2f75ce5e8c440ae07959984ce311885bb2323dd81dbb3dade938`  
		Last Modified: Thu, 12 Oct 2023 03:00:50 GMT  
		Size: 30.9 MB (30856771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3baa367edd0b80024fdd005800800566ef06cacc5ff5ee8aec24aad4ceddd4`  
		Last Modified: Thu, 12 Oct 2023 03:00:45 GMT  
		Size: 2.2 MB (2159371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-7-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:ec8ea5d195521947968ac40c283c6a003b95ac750ac2addd1a247e2c4c00b525
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63524396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:080376fe8c81420ab57c0637ac0867ac67b658c20e45724df6ceab89c5dac08d`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 11 Oct 2023 18:24:51 GMT
ADD file:5c81bfc00a28feb4079c0daa743f829a6a5bbc1a9d40a890cb49e420539a7f15 in / 
# Wed, 11 Oct 2023 18:24:51 GMT
CMD ["bash"]
# Thu, 12 Oct 2023 03:38:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 12 Oct 2023 03:38:34 GMT
ENV LANG=C.UTF-8
# Thu, 12 Oct 2023 03:38:34 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 12 Oct 2023 03:50:22 GMT
ENV PYPY_VERSION=7.3.13
# Thu, 12 Oct 2023 03:50:34 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-linux64.tar.bz2'; 			sha256='e41ceb5dc6c4d3a9311ed5f88edfeedbf3e8abbd1ed3c4f2e151a90a5cf4e1d7'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-aarch64.tar.bz2'; 			sha256='f1e20f833cc86a097c1f1318069fc17d01c3988678c1438fe27ed567fcb5cfd0'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-linux32.tar.bz2'; 			sha256='b727d2e759a740f45bab1e333029d001c4384b52949bcbb4bd2ad7912eae8dad'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-s390x.tar.bz2'; 			sha256='fbb2f3d92831c02b094f17e9609b95a6202d4bdcddae437e380ab14388d4556e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 12 Oct 2023 03:50:34 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 12 Oct 2023 03:50:34 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 12 Oct 2023 03:50:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 12 Oct 2023 03:50:42 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:1bc163a14ea6a886d1d0f9a9be878b1ffd08a9311e15861137ccd85bb87190f9`  
		Last Modified: Wed, 11 Oct 2023 18:28:28 GMT  
		Size: 29.2 MB (29179284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0f6a52ae08bd34e6b587a3267612d191904c5ca3f09aad77f727c166770e732`  
		Last Modified: Thu, 12 Oct 2023 03:52:50 GMT  
		Size: 3.3 MB (3317549 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:910c6fce267b7f26c922df2f88e5268bedbeae534a99cea01aa1e01ad09c80b9`  
		Last Modified: Thu, 12 Oct 2023 03:56:06 GMT  
		Size: 28.9 MB (28868048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1b21089e572d8c051b3311754a269de3ef958c86d411738cf02b735cf631bf5`  
		Last Modified: Thu, 12 Oct 2023 03:56:03 GMT  
		Size: 2.2 MB (2159515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-7-slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:b72ce601eaf3a840eb0b26759b14e3846562d5898025f66902c74ee67c5e5f7c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62741780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0776cc034db5c3fa945f77af738e6006d5ee0da282ebbc34c6e11aca22d6823`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 20 Sep 2023 00:41:55 GMT
ADD file:efe81f7066129aa6293627bfe4ea78b957897ba5ede951970156fccf1dbcde88 in / 
# Wed, 20 Sep 2023 00:41:56 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 17:30:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:30:20 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 17:30:20 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 01:14:45 GMT
ENV PYPY_VERSION=7.3.13
# Tue, 03 Oct 2023 01:15:02 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-linux64.tar.bz2'; 			sha256='e41ceb5dc6c4d3a9311ed5f88edfeedbf3e8abbd1ed3c4f2e151a90a5cf4e1d7'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-aarch64.tar.bz2'; 			sha256='f1e20f833cc86a097c1f1318069fc17d01c3988678c1438fe27ed567fcb5cfd0'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-linux32.tar.bz2'; 			sha256='b727d2e759a740f45bab1e333029d001c4384b52949bcbb4bd2ad7912eae8dad'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-s390x.tar.bz2'; 			sha256='fbb2f3d92831c02b094f17e9609b95a6202d4bdcddae437e380ab14388d4556e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 03 Oct 2023 01:15:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 03 Oct 2023 01:15:02 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 03 Oct 2023 01:15:15 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 03 Oct 2023 01:15:15 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:6ac07f93e07a1bad4555e13bd8efd06169988669fc88df95f4bf296a2b44523d`  
		Last Modified: Wed, 20 Sep 2023 00:46:48 GMT  
		Size: 30.1 MB (30141894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10b7970c0edcfc60991a83d7041a2193d42704f5cfd894072c0a61f43fd7319d`  
		Last Modified: Wed, 20 Sep 2023 17:40:26 GMT  
		Size: 3.5 MB (3492701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b69c910430aa3a9e1d2bb8608e02082a1c1d5a4103d34e38cc4dc4a7a009345`  
		Last Modified: Tue, 03 Oct 2023 01:18:25 GMT  
		Size: 26.9 MB (26949705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b0170ac7d0078c216bd55a4f26e1620d94fda8a9b4343ed0e1104a8c8083149`  
		Last Modified: Tue, 03 Oct 2023 01:18:19 GMT  
		Size: 2.2 MB (2157480 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
