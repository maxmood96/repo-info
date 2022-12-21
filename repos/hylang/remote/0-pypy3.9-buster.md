## `hylang:0-pypy3.9-buster`

```console
$ docker pull hylang@sha256:3307858480aaaee806b72acce5942c94f894d090c05753bc9748b1b311fcffe9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `hylang:0-pypy3.9-buster` - linux; amd64

```console
$ docker pull hylang@sha256:2f71f401daacbd8a6e57e93ebd077cfea8b78def90d1823b37b8faecb3ac0473
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74365741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30fe16168a8484dc585ce11be0ab0137e060edac31b0d11ee3136de73662cf39`
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
# Wed, 21 Dec 2022 12:28:14 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-linux64.tar.bz2'; 			sha256='95cf99406179460d63ddbfe1ec870f889d05f7767ce81cef14b88a3a9e127266'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-aarch64.tar.bz2'; 			sha256='657a04fd9a5a992a2f116a9e7e9132ea0c578721f59139c9fb2083775f71e514'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-linux32.tar.bz2'; 			sha256='b6db59613b9a1c0c1ab87bc103f52ee95193423882dc8a848b68850b8ba59cc5'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-s390x.tar.bz2'; 			sha256='ca6525a540cf0c682d1592ae35d3fbc97559a97260e4b789255cc76dde7a14f0'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 21 Dec 2022 12:28:14 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 21 Dec 2022 12:28:14 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 21 Dec 2022 12:28:27 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 21 Dec 2022 12:28:27 GMT
CMD ["pypy3"]
# Wed, 21 Dec 2022 15:39:02 GMT
ENV HY_VERSION=0.25.0
# Wed, 21 Dec 2022 15:39:02 GMT
ENV HYRULE_VERSION=0.2.1
# Wed, 21 Dec 2022 15:39:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 21 Dec 2022 15:39:32 GMT
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
	-	`sha256:3c070cd9c87a3aee087e5228abebbb339fe60d64ddaafb88642aedb27bb8159c`  
		Last Modified: Wed, 21 Dec 2022 12:36:31 GMT  
		Size: 37.2 MB (37241755 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efd927128462ebb61db145eafe7f4ab3e6591717b1a615f9a499a18c064607d4`  
		Last Modified: Wed, 21 Dec 2022 12:36:24 GMT  
		Size: 3.2 MB (3168274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d57f4d11d78f135552e218174585ee49dce989056c56c74a46babd754904062`  
		Last Modified: Wed, 21 Dec 2022 15:46:46 GMT  
		Size: 4.0 MB (4047374 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy3.9-buster` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:b951fba7d0b3f70aeacf4e2a3e99f677ecda2d347ae7532274b9ccdb879dfecd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70111476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92dced3dfca96edfe9e9df0edc434a8d6a86e985df7d667200be9da065555144`
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
# Wed, 07 Dec 2022 02:15:07 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-linux64.tar.bz2'; 			sha256='95cf99406179460d63ddbfe1ec870f889d05f7767ce81cef14b88a3a9e127266'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-aarch64.tar.bz2'; 			sha256='657a04fd9a5a992a2f116a9e7e9132ea0c578721f59139c9fb2083775f71e514'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-linux32.tar.bz2'; 			sha256='b6db59613b9a1c0c1ab87bc103f52ee95193423882dc8a848b68850b8ba59cc5'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-s390x.tar.bz2'; 			sha256='ca6525a540cf0c682d1592ae35d3fbc97559a97260e4b789255cc76dde7a14f0'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 07 Dec 2022 02:15:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 07 Dec 2022 02:15:08 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 07 Dec 2022 02:15:19 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 07 Dec 2022 02:15:19 GMT
CMD ["pypy3"]
# Wed, 07 Dec 2022 03:11:49 GMT
ENV HY_VERSION=0.25.0
# Wed, 07 Dec 2022 03:11:49 GMT
ENV HYRULE_VERSION=0.2.1
# Wed, 07 Dec 2022 03:12:17 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 07 Dec 2022 03:12:17 GMT
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
	-	`sha256:57fd289229dfa6ef869e10885c3faaab1f6bf1287630305d6d2b0938ab6dba4a`  
		Last Modified: Wed, 07 Dec 2022 02:22:48 GMT  
		Size: 34.3 MB (34344831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d82065577af43278fb389ddd4ec7e37a7eccc8a1506ed372029cc927219f79b`  
		Last Modified: Wed, 07 Dec 2022 02:22:44 GMT  
		Size: 3.2 MB (3168013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa45b8be62cd7f8c2c4eea76e48fa67d3d06d11491b76dceaa263829ee0d46f2`  
		Last Modified: Wed, 07 Dec 2022 03:17:33 GMT  
		Size: 4.0 MB (4047197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy3.9-buster` - linux; 386

```console
$ docker pull hylang@sha256:5da70c004763c7f9e0ce4151f0057046c9519ac8672ceca6ab76f1c88a838480
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.6 MB (75576442 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b05ca158a3f00a26a0afafaf61c2e7081d7edd5acc1f7ad07599be57500ad5b`
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
# Wed, 21 Dec 2022 06:24:40 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-linux64.tar.bz2'; 			sha256='95cf99406179460d63ddbfe1ec870f889d05f7767ce81cef14b88a3a9e127266'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-aarch64.tar.bz2'; 			sha256='657a04fd9a5a992a2f116a9e7e9132ea0c578721f59139c9fb2083775f71e514'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-linux32.tar.bz2'; 			sha256='b6db59613b9a1c0c1ab87bc103f52ee95193423882dc8a848b68850b8ba59cc5'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.10-s390x.tar.bz2'; 			sha256='ca6525a540cf0c682d1592ae35d3fbc97559a97260e4b789255cc76dde7a14f0'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 21 Dec 2022 06:24:40 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 21 Dec 2022 06:24:41 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 21 Dec 2022 06:24:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 21 Dec 2022 06:24:57 GMT
CMD ["pypy3"]
# Wed, 21 Dec 2022 17:53:04 GMT
ENV HY_VERSION=0.25.0
# Wed, 21 Dec 2022 17:53:04 GMT
ENV HYRULE_VERSION=0.2.1
# Wed, 21 Dec 2022 17:53:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 21 Dec 2022 17:53:43 GMT
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
	-	`sha256:a96b7e81aaeb25031693f266f9a51b8296dcb04134e1bf695029dbe3691a868f`  
		Last Modified: Wed, 21 Dec 2022 06:33:38 GMT  
		Size: 38.0 MB (37998334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d82bacb91495222b7aa85601889880d032046f7e471ddd4aed223051b45db2c9`  
		Last Modified: Wed, 21 Dec 2022 06:33:32 GMT  
		Size: 3.0 MB (2951729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d811fc4623affccac354a062a7e81aa192d10073a5cd4423272213619ee28da`  
		Last Modified: Wed, 21 Dec 2022 18:05:16 GMT  
		Size: 4.0 MB (4046961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
