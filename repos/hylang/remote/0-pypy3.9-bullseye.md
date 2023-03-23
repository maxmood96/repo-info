## `hylang:0-pypy3.9-bullseye`

```console
$ docker pull hylang@sha256:f90b871dede36fb6b9a72d9a4bc234797a554e2d029cfe6c2b7e70775758b110
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `hylang:0-pypy3.9-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:83d917dfd2f16f722b4a966c2cfc1aaff226ed429aac9a221f7afc69a340de97
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75869216 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e6263824dd3e0512e0ae3e1ed518160d3562709939c1c48674c5ca363a40228`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 01 Mar 2023 04:09:58 GMT
ADD file:493a5b0c8d2d63a1343258b3f9aa5fcd59a93f44fe26ad9e56b094c3a08fd3be in / 
# Wed, 01 Mar 2023 04:09:59 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 13:38:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 13:38:03 GMT
ENV LANG=C.UTF-8
# Wed, 01 Mar 2023 13:38:03 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 13:38:03 GMT
ENV PYPY_VERSION=7.3.11
# Wed, 01 Mar 2023 13:38:34 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.11-linux64.tar.bz2'; 			sha256='d506172ca11071274175d74e9c581c3166432d0179b036470e3b9e8d20eae581'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.11-aarch64.tar.bz2'; 			sha256='09175dc652ed895d98e9ad63d216812bf3ee7e398d900a9bf9eb2906ba8302b9'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.11-linux32.tar.bz2'; 			sha256='0099d72c2897b229057bff7e2c343624aeabdc60d6fb43ca882bff082f1ffa48'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.11-s390x.tar.bz2'; 			sha256='e1f30f2ddbe3f446ddacd79677b958d56c07463b20171fb2abf8f9a3178b79fc'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 01 Mar 2023 13:38:35 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 01 Mar 2023 13:38:35 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 01 Mar 2023 13:38:46 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 01 Mar 2023 13:38:47 GMT
CMD ["pypy3"]
# Thu, 02 Mar 2023 02:03:44 GMT
ENV HY_VERSION=0.26.0
# Thu, 02 Mar 2023 02:03:44 GMT
ENV HYRULE_VERSION=0.3.0
# Thu, 02 Mar 2023 02:04:17 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 02 Mar 2023 02:04:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3f9582a2cbe7197f39185419c0ced2c986389f8fc6aa805e1f5c090eea6511e0`  
		Last Modified: Wed, 01 Mar 2023 04:14:23 GMT  
		Size: 31.4 MB (31411403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2c6d95e843f13867bc54ffb2aa2b46a4ee400099603b7d5c09ec77f6739a369`  
		Last Modified: Wed, 01 Mar 2023 13:47:09 GMT  
		Size: 1.1 MB (1066527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e019a4c855d394b707f64196d37d22d9b62d84e25da0cbcea7f6f23618d580d`  
		Last Modified: Wed, 01 Mar 2023 13:47:15 GMT  
		Size: 36.2 MB (36188076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f028622ddd4509797edb11c1c4b84cdaa34f340ad12123d6612ba477dbb2e6ac`  
		Last Modified: Wed, 01 Mar 2023 13:47:10 GMT  
		Size: 3.2 MB (3170665 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d3e5b8c5672672fca5b66a955e0783c3de0adccf6a80dedaae68cb97405ccc1`  
		Last Modified: Thu, 02 Mar 2023 02:11:50 GMT  
		Size: 4.0 MB (4032545 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy3.9-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:d82a5ee2318d82119593a3ca0ba77ffc5fbd365ee0b1109db01752318c25ea62
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72064918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d6197214cafc5848e9721756295ef684848bff770b60e2a552fd08f983f3f347`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 23 Mar 2023 00:45:10 GMT
ADD file:83beb883b699cd442f1dbd4baf29c23f4cd15f7a5f9f120979df16a77455c69f in / 
# Thu, 23 Mar 2023 00:45:10 GMT
CMD ["bash"]
# Thu, 23 Mar 2023 06:02:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 23 Mar 2023 06:02:54 GMT
ENV LANG=C.UTF-8
# Thu, 23 Mar 2023 06:02:54 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 23 Mar 2023 06:02:54 GMT
ENV PYPY_VERSION=7.3.11
# Thu, 23 Mar 2023 06:03:21 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.11-linux64.tar.bz2'; 			sha256='d506172ca11071274175d74e9c581c3166432d0179b036470e3b9e8d20eae581'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.11-aarch64.tar.bz2'; 			sha256='09175dc652ed895d98e9ad63d216812bf3ee7e398d900a9bf9eb2906ba8302b9'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.11-linux32.tar.bz2'; 			sha256='0099d72c2897b229057bff7e2c343624aeabdc60d6fb43ca882bff082f1ffa48'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.11-s390x.tar.bz2'; 			sha256='e1f30f2ddbe3f446ddacd79677b958d56c07463b20171fb2abf8f9a3178b79fc'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 23 Mar 2023 06:03:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 23 Mar 2023 06:03:21 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 23 Mar 2023 06:03:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 23 Mar 2023 06:03:33 GMT
CMD ["pypy3"]
# Thu, 23 Mar 2023 15:11:14 GMT
ENV HY_VERSION=0.26.0
# Thu, 23 Mar 2023 15:11:14 GMT
ENV HYRULE_VERSION=0.3.0
# Thu, 23 Mar 2023 15:11:45 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 23 Mar 2023 15:11:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:fcdb9667c46b09d1c1d058681ea4a1db41e66bbc1a71d873a0c9da4f7a92947d`  
		Last Modified: Thu, 23 Mar 2023 00:48:09 GMT  
		Size: 30.1 MB (30062700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d1e54406be8d5f44fc875b900ad3f0fcac16df20b38c231eb4ab849a94be046`  
		Last Modified: Thu, 23 Mar 2023 06:07:20 GMT  
		Size: 1.1 MB (1054057 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84891e2504931e6424cdb2d1dbfff6679c87351cc528f5861fe2d264ca4d4a0`  
		Last Modified: Thu, 23 Mar 2023 06:07:24 GMT  
		Size: 33.7 MB (33692961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24fd7143c7e1704d2c7a8555c7b283e46b1d53bb4b7a9da0fca4f55911d61b12`  
		Last Modified: Thu, 23 Mar 2023 06:07:20 GMT  
		Size: 3.2 MB (3194717 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:309cdd20715321a9d8c889c01d86960c9346780d8872560f6860b31567888ea4`  
		Last Modified: Thu, 23 Mar 2023 15:20:17 GMT  
		Size: 4.1 MB (4060483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy3.9-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:e10ba8ec8f59c363b7b0295d5875bddb6ef128d0a4bc108065ba900ef7506439
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.1 MB (75116705 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed7ac2ceb6febb8bf0b31f22ef72640b9cfe878d82145db85cfc8090841f68cb`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 01 Mar 2023 01:39:14 GMT
ADD file:7ff48f7b36d13400120a726cd394769a4c39e8424877f5b080aeb9da07eacebe in / 
# Wed, 01 Mar 2023 01:39:15 GMT
CMD ["bash"]
# Thu, 02 Mar 2023 04:12:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 02 Mar 2023 04:12:05 GMT
ENV LANG=C.UTF-8
# Thu, 02 Mar 2023 04:12:06 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 02 Mar 2023 04:12:06 GMT
ENV PYPY_VERSION=7.3.11
# Thu, 02 Mar 2023 04:12:39 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.11-linux64.tar.bz2'; 			sha256='d506172ca11071274175d74e9c581c3166432d0179b036470e3b9e8d20eae581'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.11-aarch64.tar.bz2'; 			sha256='09175dc652ed895d98e9ad63d216812bf3ee7e398d900a9bf9eb2906ba8302b9'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.11-linux32.tar.bz2'; 			sha256='0099d72c2897b229057bff7e2c343624aeabdc60d6fb43ca882bff082f1ffa48'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.11-s390x.tar.bz2'; 			sha256='e1f30f2ddbe3f446ddacd79677b958d56c07463b20171fb2abf8f9a3178b79fc'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 02 Mar 2023 04:12:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 02 Mar 2023 04:12:39 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 02 Mar 2023 04:12:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 02 Mar 2023 04:12:52 GMT
CMD ["pypy3"]
# Thu, 02 Mar 2023 05:09:48 GMT
ENV HY_VERSION=0.26.0
# Thu, 02 Mar 2023 05:09:48 GMT
ENV HYRULE_VERSION=0.3.0
# Thu, 02 Mar 2023 05:10:24 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 02 Mar 2023 05:10:24 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2b884ef8a2d2b7c2016a8d2926b5b284f2130128ee049cae31a2da609cda7257`  
		Last Modified: Wed, 01 Mar 2023 01:44:44 GMT  
		Size: 32.4 MB (32396138 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c289128b6833e31e95e22ad48341fe66d7dce2ce9ba94a5befd98b42ac0754c8`  
		Last Modified: Thu, 02 Mar 2023 04:24:13 GMT  
		Size: 1.1 MB (1078985 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:414cc0e8a0de2287e81a0a4edfca278b7b3c1a0ee11cf79d4130f1536bce0b4f`  
		Last Modified: Thu, 02 Mar 2023 04:24:20 GMT  
		Size: 34.4 MB (34439036 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b7e932403d3f882224c1a6de81931293f36e00ee68e206ed85d44fed65a8c6d`  
		Last Modified: Thu, 02 Mar 2023 04:24:13 GMT  
		Size: 3.2 MB (3170227 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8309e214262e7c6252c28a6e86ee6a809a0c2a514a1b739b69beb5c451ab3be`  
		Last Modified: Thu, 02 Mar 2023 05:22:19 GMT  
		Size: 4.0 MB (4032319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
