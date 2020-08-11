## `hylang:0-pypy`

```console
$ docker pull hylang@sha256:004655d244e0f326004027a2d5df144214e909003714790d6c7e9b76568523d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; ppc64le
	-	linux; s390x

### `hylang:0-pypy` - linux; amd64

```console
$ docker pull hylang@sha256:1f069f36199a410806293d77373943c55dfff864d27281bd77cfcf43a24c39d7
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.9 MB (70867942 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b1fdf30fb8f884bcfe473bf9a260d2ad84351656ca1242faed6707ebe11b5b`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Aug 2020 15:42:51 GMT
ADD file:3af3091e7d2bb40bc1e6550eb5ea290badc6bbf3339105626f245a963cc11450 in / 
# Tue, 04 Aug 2020 15:42:51 GMT
CMD ["bash"]
# Wed, 05 Aug 2020 06:28:23 GMT
ENV LANG=C.UTF-8
# Wed, 05 Aug 2020 06:28:29 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 05 Aug 2020 06:28:30 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 05 Aug 2020 06:28:30 GMT
ENV PYPY_VERSION=7.3.1
# Wed, 05 Aug 2020 06:30:38 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='f67cf1664a336a3e939b58b3cabfe47d893356bdc01f2e17bc912aaa6605db12' ;; 		arm64) pypyArch='aarch64'; sha256='0069bc3c1570b935f1687f5e128cf050cd7229309e48fad2a2bf2140d43ffcee' ;; 		i386) pypyArch='linux32'; sha256='2e7a818c67f3ac0708e4d8cdf1961f30cf9586b3f3ca2f215d93437c5ea4567b' ;; 		ppc64el) pypyArch='ppc64le'; sha256='089fd806629ebf79cb0cb4b0c303d8665f360903b79f0df9214b58dbc42e8231' ;; 		s390x) pypyArch='s390x'; sha256='147592888e25678c1ae1c2929dc7420b3a0990117fdb25f235cb22476b4e4b5a' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		patch 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://downloads.python.org/pypy/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		wget -O pypy-sqlite.patch 'https://foss.heptapod.net/pypy/pypy/commit/fbbe06715eb48df1a03640672d99335695d3e47c.patch'; 	awk '$1 == "diff" { yes = ($3 == "a/lib_pypy/_sqlite3.py") } yes { print }' pypy-sqlite.patch | patch --strip=1 --directory=/opt/pypy; 	rm pypy-sqlite.patch; 		ln -svT '/opt/pypy/bin/pypy3' '/usr/local/bin/pypy3'; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 11 Aug 2020 20:45:24 GMT
ENV PYTHON_PIP_VERSION=20.2.2
# Tue, 11 Aug 2020 20:45:24 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/5578af97f8b2b466f4cdbebe18a3ba2d48ad1434/get-pip.py
# Tue, 11 Aug 2020 20:45:24 GMT
ENV PYTHON_GET_PIP_SHA256=d4d62a0850fe0c2e6325b2cc20d818c580563de5a2038f917e3cb0e25280b4d1
# Tue, 11 Aug 2020 20:45:40 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 11 Aug 2020 20:45:40 GMT
CMD ["pypy3"]
# Tue, 11 Aug 2020 21:16:42 GMT
ENV HY_VERSION=0.19.0
# Tue, 11 Aug 2020 21:16:53 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Tue, 11 Aug 2020 21:16:53 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bf59529304463f62efa7179fa1a32718a611528cc4ce9f30c0d1bbc6724ec3fb`  
		Last Modified: Tue, 04 Aug 2020 15:49:09 GMT  
		Size: 27.1 MB (27092121 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba752debb3c3e0ed5c7d24db21b2548297fed7d74e1da6804f764e5c63d18fff`  
		Last Modified: Wed, 05 Aug 2020 06:31:52 GMT  
		Size: 2.7 MB (2742465 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c80b4771d05e39d1df6c82b14ae4836dcf740374ea3ef38e2abcff35a59a5e9`  
		Last Modified: Wed, 05 Aug 2020 06:32:38 GMT  
		Size: 35.7 MB (35686864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1fa6b8d461a67ec5303e8c1925a0113bcab2ce132508987ee1cbaa8616d0ed2`  
		Last Modified: Tue, 11 Aug 2020 20:46:46 GMT  
		Size: 2.4 MB (2394762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84081b075d7fd2b2aae0afcd443be8cb46b514dc878fe6d804fe490db7c591e`  
		Last Modified: Tue, 11 Aug 2020 21:19:24 GMT  
		Size: 3.0 MB (2951730 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:3cb857a8fb92b1f36fb4da4f508d387d640819c3249ffb89c7570033aa18e8e4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63288870 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:320cd3e35e7f623254c307ec33f9e1ff8f9f48a7e3811274fe526b129f511902`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Aug 2020 06:57:29 GMT
ADD file:90ba7821623ab55fc1073647cc611cc45f5e306ade734910e587021971483eec in / 
# Tue, 04 Aug 2020 06:57:31 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 09:53:00 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 09:53:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 09:53:24 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 09:53:27 GMT
ENV PYPY_VERSION=7.3.1
# Tue, 04 Aug 2020 09:56:47 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='f67cf1664a336a3e939b58b3cabfe47d893356bdc01f2e17bc912aaa6605db12' ;; 		arm64) pypyArch='aarch64'; sha256='0069bc3c1570b935f1687f5e128cf050cd7229309e48fad2a2bf2140d43ffcee' ;; 		i386) pypyArch='linux32'; sha256='2e7a818c67f3ac0708e4d8cdf1961f30cf9586b3f3ca2f215d93437c5ea4567b' ;; 		ppc64el) pypyArch='ppc64le'; sha256='089fd806629ebf79cb0cb4b0c303d8665f360903b79f0df9214b58dbc42e8231' ;; 		s390x) pypyArch='s390x'; sha256='147592888e25678c1ae1c2929dc7420b3a0990117fdb25f235cb22476b4e4b5a' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		patch 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://downloads.python.org/pypy/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		wget -O pypy-sqlite.patch 'https://foss.heptapod.net/pypy/pypy/commit/fbbe06715eb48df1a03640672d99335695d3e47c.patch'; 	awk '$1 == "diff" { yes = ($3 == "a/lib_pypy/_sqlite3.py") } yes { print }' pypy-sqlite.patch | patch --strip=1 --directory=/opt/pypy; 	rm pypy-sqlite.patch; 		ln -svT '/opt/pypy/bin/pypy3' '/usr/local/bin/pypy3'; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 11 Aug 2020 20:12:32 GMT
ENV PYTHON_PIP_VERSION=20.2.2
# Tue, 11 Aug 2020 20:12:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/5578af97f8b2b466f4cdbebe18a3ba2d48ad1434/get-pip.py
# Tue, 11 Aug 2020 20:12:33 GMT
ENV PYTHON_GET_PIP_SHA256=d4d62a0850fe0c2e6325b2cc20d818c580563de5a2038f917e3cb0e25280b4d1
# Tue, 11 Aug 2020 20:13:22 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 11 Aug 2020 20:13:26 GMT
CMD ["pypy3"]
# Tue, 11 Aug 2020 20:32:48 GMT
ENV HY_VERSION=0.19.0
# Tue, 11 Aug 2020 20:33:09 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Tue, 11 Aug 2020 20:33:09 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3742235f1882fee5cca1effc4ca0f0c7c180bbe169800a85daedcf3968b0d8f0`  
		Last Modified: Tue, 04 Aug 2020 07:04:03 GMT  
		Size: 25.8 MB (25849301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8ead8238ab6c3577178d87cecdfba4724b27518c235f3c352ca7b7232df97e0`  
		Last Modified: Tue, 04 Aug 2020 09:59:20 GMT  
		Size: 2.6 MB (2606653 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cdc4960e1ec3f88b442e3ab664683c5a1157f7aa673950b128523fe78df07e8`  
		Last Modified: Tue, 04 Aug 2020 10:00:11 GMT  
		Size: 29.5 MB (29484563 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e0e2c3c495db55f150d58aa1a43737decc3b31c92b18becf64115979c7473c1`  
		Last Modified: Tue, 11 Aug 2020 20:15:27 GMT  
		Size: 2.4 MB (2395799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e738b6a87e3f97363ba75eec1dcd5c12c27fe9c6cf8b003e6f0c898faf30f0f`  
		Last Modified: Tue, 11 Aug 2020 20:34:26 GMT  
		Size: 3.0 MB (2952554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy` - linux; 386

```console
$ docker pull hylang@sha256:4c5203d96344a00349846b8a9e589617b661db4d5e230bca4febc885a70e3690
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73846380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7fc7dbe096254fa2048b9300135ae5d398f6298c2772f5cd08092310a27d9e35`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Aug 2020 03:37:35 GMT
ADD file:cc791c21e6022a12dd1445a35f4cca9392ad8edfe34ea5852f3e87862c943628 in / 
# Tue, 04 Aug 2020 03:37:35 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 06:20:59 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 06:21:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 06:21:07 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 06:21:07 GMT
ENV PYPY_VERSION=7.3.1
# Tue, 04 Aug 2020 06:22:45 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='f67cf1664a336a3e939b58b3cabfe47d893356bdc01f2e17bc912aaa6605db12' ;; 		arm64) pypyArch='aarch64'; sha256='0069bc3c1570b935f1687f5e128cf050cd7229309e48fad2a2bf2140d43ffcee' ;; 		i386) pypyArch='linux32'; sha256='2e7a818c67f3ac0708e4d8cdf1961f30cf9586b3f3ca2f215d93437c5ea4567b' ;; 		ppc64el) pypyArch='ppc64le'; sha256='089fd806629ebf79cb0cb4b0c303d8665f360903b79f0df9214b58dbc42e8231' ;; 		s390x) pypyArch='s390x'; sha256='147592888e25678c1ae1c2929dc7420b3a0990117fdb25f235cb22476b4e4b5a' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		patch 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://downloads.python.org/pypy/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		wget -O pypy-sqlite.patch 'https://foss.heptapod.net/pypy/pypy/commit/fbbe06715eb48df1a03640672d99335695d3e47c.patch'; 	awk '$1 == "diff" { yes = ($3 == "a/lib_pypy/_sqlite3.py") } yes { print }' pypy-sqlite.patch | patch --strip=1 --directory=/opt/pypy; 	rm pypy-sqlite.patch; 		ln -svT '/opt/pypy/bin/pypy3' '/usr/local/bin/pypy3'; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 11 Aug 2020 19:46:41 GMT
ENV PYTHON_PIP_VERSION=20.2.2
# Tue, 11 Aug 2020 19:46:41 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/5578af97f8b2b466f4cdbebe18a3ba2d48ad1434/get-pip.py
# Tue, 11 Aug 2020 19:46:41 GMT
ENV PYTHON_GET_PIP_SHA256=d4d62a0850fe0c2e6325b2cc20d818c580563de5a2038f917e3cb0e25280b4d1
# Tue, 11 Aug 2020 19:46:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 11 Aug 2020 19:46:59 GMT
CMD ["pypy3"]
# Tue, 11 Aug 2020 20:06:09 GMT
ENV HY_VERSION=0.19.0
# Tue, 11 Aug 2020 20:06:19 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Tue, 11 Aug 2020 20:06:20 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:23ad22c16ab9d635a179d5d341096c34912941507b0c77ac97083b9795d8516f`  
		Last Modified: Tue, 04 Aug 2020 03:42:33 GMT  
		Size: 27.8 MB (27750435 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:808cfccc3b3781d496a79401f47d7ccd4157a669c743cd881c94902078a99e67`  
		Last Modified: Tue, 04 Aug 2020 06:23:35 GMT  
		Size: 2.8 MB (2752668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:108d41eb2fc2a10f911175802cddc87fc25ef0b15a0eece82da7a4924e5507b7`  
		Last Modified: Tue, 04 Aug 2020 06:24:13 GMT  
		Size: 38.0 MB (37997107 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:656701f458556ac1cf1cbebe007d4ec276313455157785b11337df0516d2fb31`  
		Last Modified: Tue, 11 Aug 2020 19:49:29 GMT  
		Size: 2.4 MB (2394446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8fab3ea3abf98d6ec11b381ec427ec31b23379510eb559ba9d5c654d02ed76f`  
		Last Modified: Tue, 11 Aug 2020 20:07:53 GMT  
		Size: 3.0 MB (2951724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy` - linux; ppc64le

```console
$ docker pull hylang@sha256:42d1f43b77ee6684ead7a74041dcc9f818e850fd92a4d64c4c2ce1ae7d6aff20
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69218499 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2486a0b2ddfb90796bea5846d7d688f0ef2e234c474068696d14fac61a009d4`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Aug 2020 04:45:34 GMT
ADD file:3bab6d2b62fe6a548ee28480d9eebf3251e942c4bb66362b87396b73af7aa586 in / 
# Tue, 04 Aug 2020 04:45:40 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 15:57:37 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 15:59:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 15:59:23 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 15:59:32 GMT
ENV PYPY_VERSION=7.3.1
# Tue, 04 Aug 2020 16:04:21 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='f67cf1664a336a3e939b58b3cabfe47d893356bdc01f2e17bc912aaa6605db12' ;; 		arm64) pypyArch='aarch64'; sha256='0069bc3c1570b935f1687f5e128cf050cd7229309e48fad2a2bf2140d43ffcee' ;; 		i386) pypyArch='linux32'; sha256='2e7a818c67f3ac0708e4d8cdf1961f30cf9586b3f3ca2f215d93437c5ea4567b' ;; 		ppc64el) pypyArch='ppc64le'; sha256='089fd806629ebf79cb0cb4b0c303d8665f360903b79f0df9214b58dbc42e8231' ;; 		s390x) pypyArch='s390x'; sha256='147592888e25678c1ae1c2929dc7420b3a0990117fdb25f235cb22476b4e4b5a' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		patch 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://downloads.python.org/pypy/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		wget -O pypy-sqlite.patch 'https://foss.heptapod.net/pypy/pypy/commit/fbbe06715eb48df1a03640672d99335695d3e47c.patch'; 	awk '$1 == "diff" { yes = ($3 == "a/lib_pypy/_sqlite3.py") } yes { print }' pypy-sqlite.patch | patch --strip=1 --directory=/opt/pypy; 	rm pypy-sqlite.patch; 		ln -svT '/opt/pypy/bin/pypy3' '/usr/local/bin/pypy3'; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 05 Aug 2020 04:33:07 GMT
ENV PYTHON_PIP_VERSION=20.2.1
# Wed, 05 Aug 2020 04:33:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/5578af97f8b2b466f4cdbebe18a3ba2d48ad1434/get-pip.py
# Wed, 05 Aug 2020 04:33:12 GMT
ENV PYTHON_GET_PIP_SHA256=d4d62a0850fe0c2e6325b2cc20d818c580563de5a2038f917e3cb0e25280b4d1
# Wed, 05 Aug 2020 04:34:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 05 Aug 2020 04:34:04 GMT
CMD ["pypy3"]
# Wed, 05 Aug 2020 05:38:24 GMT
ENV HY_VERSION=0.19.0
# Wed, 05 Aug 2020 05:39:20 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 05 Aug 2020 05:39:23 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0827434caf9c0b71f95b3bcbe29d60f4f887199db59b3994d9315c478def41c3`  
		Last Modified: Tue, 04 Aug 2020 04:53:24 GMT  
		Size: 30.5 MB (30517844 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0e574ade0fff998b900879bc23d853090e208ab3a97185e5228d1329f59fa7f`  
		Last Modified: Tue, 04 Aug 2020 16:08:10 GMT  
		Size: 2.9 MB (2855740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75de69cc0b5846e05b161c1bd7f3150ec531de87eff9d6cb998e9aea42e5df30`  
		Last Modified: Tue, 04 Aug 2020 16:08:17 GMT  
		Size: 30.5 MB (30499205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63114e9038e9017c61d0bac714acd0ded7a767c2e902d1a0cf8b66ebbaf869f5`  
		Last Modified: Wed, 05 Aug 2020 04:35:48 GMT  
		Size: 2.4 MB (2395169 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bda5dc55ae5aee19acdff013b1d12708736ff27c6ece82e53b77c0812c9d3eb`  
		Last Modified: Wed, 05 Aug 2020 05:45:43 GMT  
		Size: 3.0 MB (2950541 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy` - linux; s390x

```console
$ docker pull hylang@sha256:06ca6b6129006063fb946941b56cbc059a9ae124e336bc7044564782342ac240
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66121534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e271f7a80091409765f71dcc8f8e59ac2dcd189802b847d330904bf6f3a96a`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 04 Aug 2020 01:17:16 GMT
ADD file:2ffa27c57800f9370adbaecca870158ec38c3d25a58b8803e2447c5e9320c5bb in / 
# Tue, 04 Aug 2020 01:17:17 GMT
CMD ["bash"]
# Tue, 04 Aug 2020 05:46:04 GMT
ENV LANG=C.UTF-8
# Tue, 04 Aug 2020 05:46:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 04 Aug 2020 05:46:09 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 04 Aug 2020 05:46:09 GMT
ENV PYPY_VERSION=7.3.1
# Tue, 04 Aug 2020 05:46:29 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='f67cf1664a336a3e939b58b3cabfe47d893356bdc01f2e17bc912aaa6605db12' ;; 		arm64) pypyArch='aarch64'; sha256='0069bc3c1570b935f1687f5e128cf050cd7229309e48fad2a2bf2140d43ffcee' ;; 		i386) pypyArch='linux32'; sha256='2e7a818c67f3ac0708e4d8cdf1961f30cf9586b3f3ca2f215d93437c5ea4567b' ;; 		ppc64el) pypyArch='ppc64le'; sha256='089fd806629ebf79cb0cb4b0c303d8665f360903b79f0df9214b58dbc42e8231' ;; 		s390x) pypyArch='s390x'; sha256='147592888e25678c1ae1c2929dc7420b3a0990117fdb25f235cb22476b4e4b5a' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		patch 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://downloads.python.org/pypy/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		wget -O pypy-sqlite.patch 'https://foss.heptapod.net/pypy/pypy/commit/fbbe06715eb48df1a03640672d99335695d3e47c.patch'; 	awk '$1 == "diff" { yes = ($3 == "a/lib_pypy/_sqlite3.py") } yes { print }' pypy-sqlite.patch | patch --strip=1 --directory=/opt/pypy; 	rm pypy-sqlite.patch; 		ln -svT '/opt/pypy/bin/pypy3' '/usr/local/bin/pypy3'; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 11 Aug 2020 19:49:46 GMT
ENV PYTHON_PIP_VERSION=20.2.2
# Tue, 11 Aug 2020 19:49:46 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/5578af97f8b2b466f4cdbebe18a3ba2d48ad1434/get-pip.py
# Tue, 11 Aug 2020 19:49:46 GMT
ENV PYTHON_GET_PIP_SHA256=d4d62a0850fe0c2e6325b2cc20d818c580563de5a2038f917e3cb0e25280b4d1
# Tue, 11 Aug 2020 19:49:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 11 Aug 2020 19:49:58 GMT
CMD ["pypy3"]
# Tue, 11 Aug 2020 20:07:34 GMT
ENV HY_VERSION=0.19.0
# Tue, 11 Aug 2020 20:07:42 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Tue, 11 Aug 2020 20:07:42 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0c46adfa2de4a7b7eb1fe2f0cb928f9e15a4cc94b7b975f13392f397cbfb0f2c`  
		Last Modified: Tue, 04 Aug 2020 01:20:03 GMT  
		Size: 25.7 MB (25707641 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebaefa5a41b8a60f8afea4157ee2e41ad581de5ce24cd349d487956ac423a2d9`  
		Last Modified: Tue, 04 Aug 2020 05:47:44 GMT  
		Size: 2.4 MB (2432853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3ad85c5a129080464c58976764c9bddbdf28ff78476253ca76e0709d1685af`  
		Last Modified: Tue, 04 Aug 2020 05:47:51 GMT  
		Size: 32.6 MB (32634014 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5cc5cfaca51291da105dda83de6ab09df57ee44b20545ce04c0df1f5fc48a14`  
		Last Modified: Tue, 11 Aug 2020 19:50:44 GMT  
		Size: 2.4 MB (2394832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ce253c65af75ce5a97c5524d4bf273378255884c427aa4bd819ba6c5eaa730b`  
		Last Modified: Tue, 11 Aug 2020 20:09:13 GMT  
		Size: 3.0 MB (2952194 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
