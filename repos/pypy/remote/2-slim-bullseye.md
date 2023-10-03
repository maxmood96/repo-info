## `pypy:2-slim-bullseye`

```console
$ docker pull pypy@sha256:b0c863d50ca25797011137b2761319384a1344cea0234e18b3fb96dbb6964ab5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `pypy:2-slim-bullseye` - linux; amd64

```console
$ docker pull pypy@sha256:402df302fc70b14aeb2e3e515388d33ca76b72e5ed577acfe129269785bf5a4b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65696990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d999607f2c85ea2654dc61bfc1efa18cecd758fe2ab80b32b4d2209c42f8daa`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 20 Sep 2023 04:56:03 GMT
ADD file:7eb149bcaba1d7dcab06b3f9a0615ca459e9cb28459a0864f92b0037f270ba66 in / 
# Wed, 20 Sep 2023 04:56:03 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 20:42:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 20:42:39 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 20:42:39 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 20:42:39 GMT
ENV PYPY_VERSION=7.3.12
# Wed, 20 Sep 2023 20:47:49 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.12-linux64.tar.bz2'; 			sha256='1a61a2574b79466f606010f2999a2b995bd96cd085f91a78ebdd3d5c2c40e81d'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.12-aarch64.tar.bz2'; 			sha256='e04dcb6286a7b4724ec3f0e50d3cc1ba8583301dd1658c06d7f37599e4201c59'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.12-linux32.tar.bz2'; 			sha256='abf3ae477bd0e526ac6dcefe0bfa845e1535aa053342c0d641219bfcde4b9b56'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.12-s390x.tar.bz2'; 			sha256='80c0154d8b0949f9dc6a227c322abbc9590c8ae4c9f11c13bf4022aa38b82064'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 20 Sep 2023 20:47:50 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 20 Sep 2023 20:47:50 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 20 Sep 2023 20:47:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 20 Sep 2023 20:47:59 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:7dbc1adf280e1aa588c033eaa746aa6db327ee16be705740f81741f5e6945c86`  
		Last Modified: Wed, 20 Sep 2023 05:01:05 GMT  
		Size: 31.4 MB (31417711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22f7206a1bfbed6df27ad7aa8d9528a3303c6b4547a02835275fbac87392f0bb`  
		Last Modified: Wed, 20 Sep 2023 20:50:27 GMT  
		Size: 1.1 MB (1066707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7551ca908817b4c62186fbc9cd14a5c2ab1cdead68e8c3dbba976bc6bc258d01`  
		Last Modified: Wed, 20 Sep 2023 20:53:53 GMT  
		Size: 31.0 MB (31041422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cec855265d051adade1b61242678418ad1c19928bf0a7138a948ae308e6cbe3`  
		Last Modified: Wed, 20 Sep 2023 20:53:48 GMT  
		Size: 2.2 MB (2171150 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:5b877b2b2f44ff56bb760040478a895aee8f2e0629beba506e1d1a774b5bfa91
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62305446 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:143bb278f4b6c908837482a26ef01cf4b1699f3b5d8095d79b713d07150487f1`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 20 Sep 2023 02:44:28 GMT
ADD file:024479be439b4ecb37c939e68673adc72955f3345ca0e809bd13e897709e59e4 in / 
# Wed, 20 Sep 2023 02:44:28 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 16:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 16:20:01 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 16:20:01 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 20 Sep 2023 16:20:02 GMT
ENV PYPY_VERSION=7.3.12
# Wed, 20 Sep 2023 16:24:16 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.12-linux64.tar.bz2'; 			sha256='1a61a2574b79466f606010f2999a2b995bd96cd085f91a78ebdd3d5c2c40e81d'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.12-aarch64.tar.bz2'; 			sha256='e04dcb6286a7b4724ec3f0e50d3cc1ba8583301dd1658c06d7f37599e4201c59'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.12-linux32.tar.bz2'; 			sha256='abf3ae477bd0e526ac6dcefe0bfa845e1535aa053342c0d641219bfcde4b9b56'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.12-s390x.tar.bz2'; 			sha256='80c0154d8b0949f9dc6a227c322abbc9590c8ae4c9f11c13bf4022aa38b82064'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 20 Sep 2023 16:24:16 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 20 Sep 2023 16:24:16 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 20 Sep 2023 16:24:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 20 Sep 2023 16:24:25 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:fc521c5b98350f6fd8c72ace1e48558bb7b53cb3db201a2a3b42095401cd02f1`  
		Last Modified: Wed, 20 Sep 2023 02:48:13 GMT  
		Size: 30.1 MB (30062869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27ff5f15a7e7343010645ed1e4024ce0d80b6d82a0278c01cbbe9d764a18df93`  
		Last Modified: Wed, 20 Sep 2023 16:26:54 GMT  
		Size: 1.1 MB (1054117 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76cc3112c0a22f33605ae9fe48cc9515cda384bff68f8c09525f6843f5a20030`  
		Last Modified: Wed, 20 Sep 2023 16:30:16 GMT  
		Size: 29.0 MB (29017283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337401893e4cd45e5bb6e786e7d3eabc705581d6e221988ddaa2c08f23b3cc21`  
		Last Modified: Wed, 20 Sep 2023 16:30:12 GMT  
		Size: 2.2 MB (2171177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-slim-bullseye` - linux; 386

```console
$ docker pull pypy@sha256:d3f237185dd2693c4fb9932933b153139e955d8d0c3daec209f6561f5ad11707
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.6 MB (62610166 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:970eff61393b1ea306e69bbe853656d7a89f622527c08cb0d6ef87153b65b0e7`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 20 Sep 2023 00:42:18 GMT
ADD file:51db29acb4893b446fcf8a93f7fa809201b49d6ea62a009ab14002cafd3ac4a8 in / 
# Wed, 20 Sep 2023 00:42:18 GMT
CMD ["bash"]
# Wed, 20 Sep 2023 17:32:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 20 Sep 2023 17:32:17 GMT
ENV LANG=C.UTF-8
# Wed, 20 Sep 2023 17:32:17 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 03 Oct 2023 01:15:52 GMT
ENV PYPY_VERSION=7.3.13
# Tue, 03 Oct 2023 01:16:09 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-linux64.tar.bz2'; 			sha256='e41ceb5dc6c4d3a9311ed5f88edfeedbf3e8abbd1ed3c4f2e151a90a5cf4e1d7'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-aarch64.tar.bz2'; 			sha256='f1e20f833cc86a097c1f1318069fc17d01c3988678c1438fe27ed567fcb5cfd0'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-linux32.tar.bz2'; 			sha256='b727d2e759a740f45bab1e333029d001c4384b52949bcbb4bd2ad7912eae8dad'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.13-s390x.tar.bz2'; 			sha256='fbb2f3d92831c02b094f17e9609b95a6202d4bdcddae437e380ab14388d4556e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 03 Oct 2023 01:16:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 03 Oct 2023 01:16:10 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 03 Oct 2023 01:16:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 03 Oct 2023 01:16:22 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:091eb56f13f4be91ea9416e1b67e2c1f228b5e023f447dda2d3f5c56e57ff871`  
		Last Modified: Wed, 20 Sep 2023 00:47:36 GMT  
		Size: 32.4 MB (32397092 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f473ecaa78faf4830701b482b6984d96106611d8a782180c4ac474dbcf3ef778`  
		Last Modified: Wed, 20 Sep 2023 17:41:27 GMT  
		Size: 1.1 MB (1079126 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33b68a6f114d4c04f1fc62947c20013b79d62aa0709bee662b93fe4737f47867`  
		Last Modified: Tue, 03 Oct 2023 01:19:23 GMT  
		Size: 27.0 MB (26962936 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2490d0aa7f64d55b589eaa6702963cb3d51238a70b3a5265c21efd6a3902739b`  
		Last Modified: Tue, 03 Oct 2023 01:19:18 GMT  
		Size: 2.2 MB (2171012 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
