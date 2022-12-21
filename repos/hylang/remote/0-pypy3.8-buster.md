## `hylang:0-pypy3.8-buster`

```console
$ docker pull hylang@sha256:6b701a10a6b917e7f07a6f58309d6943a72a7e8b8a61e9c757b79dadc6349061
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `hylang:0-pypy3.8-buster` - linux; amd64

```console
$ docker pull hylang@sha256:1c6bcc155335a314da409047cbcb63de8d0f05c5a2efd6512e87e816e20757c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74055090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f69aa58698a6d0c0de481069e2e183bbac0dae0dcb825db4112e84f617d80c15`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:52 GMT
ADD file:660e0093a3da49e4ca41260d09d585754ccb1eff8974c4b0dd4456b76ddbbc9a in / 
# Wed, 21 Dec 2022 01:20:52 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 12:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:27:42 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 12:27:43 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 12:27:43 GMT
ENV PYPY_VERSION=7.3.10
# Wed, 21 Dec 2022 12:31:00 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.10-linux64.tar.bz2'; 			sha256='ceef6496fd4ab1c99e3ec22ce657b8f10f8bb77a32427fadfb5e1dd943806011'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.10-aarch64.tar.bz2'; 			sha256='e4caa1a545f22cfee87d5b9aa6f8852347f223643ad7d2562e0b2a2f4663ad98'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.10-linux32.tar.bz2'; 			sha256='b70ed7fdc73a74ebdc04f07439f7bad1a849aaca95e26b4a74049d0e483f071c'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.10-s390x.tar.bz2'; 			sha256='c294f8e815158388628fe77ac5b8ad6cd93c8db1359091fa02d41cf6da4d61a1'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.8; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 21 Dec 2022 12:31:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 21 Dec 2022 12:31:01 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 21 Dec 2022 12:31:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 21 Dec 2022 12:31:13 GMT
CMD ["pypy3"]
# Wed, 21 Dec 2022 15:40:16 GMT
ENV HY_VERSION=0.25.0
# Wed, 21 Dec 2022 15:40:16 GMT
ENV HYRULE_VERSION=0.2.1
# Wed, 21 Dec 2022 15:40:49 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 21 Dec 2022 15:40:49 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b52ebda398ed2c4602ea06056f78d45a59474ee4e2a020967251ba082424e7e2`  
		Last Modified: Wed, 21 Dec 2022 01:25:17 GMT  
		Size: 27.1 MB (27140331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53196de6ca370b219a4ecf8a674e83f11bbca627c09782ee4fe2dbafaa785fb`  
		Last Modified: Wed, 21 Dec 2022 12:36:24 GMT  
		Size: 2.8 MB (2768007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fd014540c5b7cdc17c1cc81dd8331b7be3912664191b8e05dede973aff3ed9`  
		Last Modified: Wed, 21 Dec 2022 12:38:05 GMT  
		Size: 36.9 MB (36944736 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d840970a6992d8326c2c64f7c56aa4f2e15ee4d7f246114043d846f9f11793a0`  
		Last Modified: Wed, 21 Dec 2022 12:37:59 GMT  
		Size: 3.2 MB (3168385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b860dd2a8e2d1e56fd68ad8ba9c96307555722b57f82cd50fcafd49ce2f65b16`  
		Last Modified: Wed, 21 Dec 2022 15:47:19 GMT  
		Size: 4.0 MB (4033631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy3.8-buster` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:df703cba848041726dd5ca97a0f28ed756f199dd6c43b94e13cc8a03d8b4a7f4
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69825141 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16084163377fa05ab40293048c548b9f77a080b3d7b2149e116ffd81474b547b`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 06 Dec 2022 01:40:34 GMT
ADD file:764288ad3920160093c500e1a7277f174a656030bbe3a0511e7925e84495b6ee in / 
# Tue, 06 Dec 2022 01:40:34 GMT
CMD ["bash"]
# Tue, 06 Dec 2022 06:43:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 06 Dec 2022 06:43:01 GMT
ENV LANG=C.UTF-8
# Tue, 06 Dec 2022 06:43:02 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 07 Dec 2022 02:14:41 GMT
ENV PYPY_VERSION=7.3.10
# Wed, 07 Dec 2022 02:17:22 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.10-linux64.tar.bz2'; 			sha256='ceef6496fd4ab1c99e3ec22ce657b8f10f8bb77a32427fadfb5e1dd943806011'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.10-aarch64.tar.bz2'; 			sha256='e4caa1a545f22cfee87d5b9aa6f8852347f223643ad7d2562e0b2a2f4663ad98'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.10-linux32.tar.bz2'; 			sha256='b70ed7fdc73a74ebdc04f07439f7bad1a849aaca95e26b4a74049d0e483f071c'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.10-s390x.tar.bz2'; 			sha256='c294f8e815158388628fe77ac5b8ad6cd93c8db1359091fa02d41cf6da4d61a1'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.8; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 07 Dec 2022 02:17:22 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 07 Dec 2022 02:17:22 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 07 Dec 2022 02:17:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 07 Dec 2022 02:17:33 GMT
CMD ["pypy3"]
# Wed, 07 Dec 2022 03:12:58 GMT
ENV HY_VERSION=0.25.0
# Wed, 07 Dec 2022 03:12:58 GMT
ENV HYRULE_VERSION=0.2.1
# Wed, 07 Dec 2022 03:13:28 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 07 Dec 2022 03:13:29 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b473b36a3d93c888196b326b1aad1f802bb6a9fa6fcbc5d2614d99a67899d587`  
		Last Modified: Tue, 06 Dec 2022 01:44:33 GMT  
		Size: 25.9 MB (25914951 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a595762d6a0d837db708fcca80bc60000933890bef34c5a89442b2a59193c587`  
		Last Modified: Tue, 06 Dec 2022 06:53:25 GMT  
		Size: 2.6 MB (2636484 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d290fe7fe4cf91e213510b98f5b22c12e7a8f4f7612ba3894c44dde05f02c26`  
		Last Modified: Wed, 07 Dec 2022 02:24:12 GMT  
		Size: 34.1 MB (34071992 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57c962d7a17a64e0fd0629a2d6caa293c1217aac28ce35e2f1d571d32b318558`  
		Last Modified: Wed, 07 Dec 2022 02:24:08 GMT  
		Size: 3.2 MB (3167905 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:41d3f38d71597b587f55a196cfef7fc4e8710f0d2aae664a630b190ad8407569`  
		Last Modified: Wed, 07 Dec 2022 03:18:07 GMT  
		Size: 4.0 MB (4033809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy3.8-buster` - linux; 386

```console
$ docker pull hylang@sha256:e69c328ca4d140b894defc637907032c467bc3508fa7b89f3d5f3728eaa5f01f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.3 MB (75331522 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1c48088224a7c2d1e4256a6da28c082737ba32c62669b83afebacb3aa488824`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:45 GMT
ADD file:48a2a0e6cb166df412bb4f6ad30537c66bc6be97ce4c8fc582fd5ac8c6129b5a in / 
# Wed, 21 Dec 2022 01:39:46 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 06:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 06:24:05 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 06:24:06 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 06:24:07 GMT
ENV PYPY_VERSION=7.3.10
# Wed, 21 Dec 2022 06:26:51 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.10-linux64.tar.bz2'; 			sha256='ceef6496fd4ab1c99e3ec22ce657b8f10f8bb77a32427fadfb5e1dd943806011'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.10-aarch64.tar.bz2'; 			sha256='e4caa1a545f22cfee87d5b9aa6f8852347f223643ad7d2562e0b2a2f4663ad98'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.10-linux32.tar.bz2'; 			sha256='b70ed7fdc73a74ebdc04f07439f7bad1a849aaca95e26b4a74049d0e483f071c'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.10-s390x.tar.bz2'; 			sha256='c294f8e815158388628fe77ac5b8ad6cd93c8db1359091fa02d41cf6da4d61a1'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.8; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 21 Dec 2022 06:26:51 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 21 Dec 2022 06:26:52 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 21 Dec 2022 06:27:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 21 Dec 2022 06:27:08 GMT
CMD ["pypy3"]
# Wed, 21 Dec 2022 17:54:47 GMT
ENV HY_VERSION=0.25.0
# Wed, 21 Dec 2022 17:54:48 GMT
ENV HYRULE_VERSION=0.2.1
# Wed, 21 Dec 2022 17:55:30 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 21 Dec 2022 17:55:31 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9099d8a02dc0a7901931d2811fa3078b18ecd3a40a156cbcfd91629126463f80`  
		Last Modified: Wed, 21 Dec 2022 01:45:34 GMT  
		Size: 27.8 MB (27798412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede92b78a95bb9625d9dc015b50cc60c777da2aa8eb240f5148ea5f8ff307148`  
		Last Modified: Wed, 21 Dec 2022 06:33:32 GMT  
		Size: 2.8 MB (2781006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd82256de8caa185266c477fbebfea9373c8db189f0dabd38c933033bf7b7f8c`  
		Last Modified: Wed, 21 Dec 2022 06:34:51 GMT  
		Size: 37.8 MB (37766898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a128972f35b2bfa46c4edf99c371021ae6fba56fc21de9a8a3caaf84ada3c74`  
		Last Modified: Wed, 21 Dec 2022 06:34:45 GMT  
		Size: 3.0 MB (2951711 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97010467611ac5a6e7de0bff33e191a59d71be97e76cf7b02cb35e89e9e76fd1`  
		Last Modified: Wed, 21 Dec 2022 18:05:59 GMT  
		Size: 4.0 MB (4033495 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
