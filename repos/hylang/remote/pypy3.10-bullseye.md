## `hylang:pypy3.10-bullseye`

```console
$ docker pull hylang@sha256:4e1da03afa2bac85d18428124f2689eabadf1116bcb2309e6c30a97e3250d8d7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:pypy3.10-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:ee84d35201b851c3aa1bade7b6cd173e68910bede2c992427ae0b1ae6b9a663f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72670721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08cd56c2a8dc5dd6f61b9e7a8a079c2d5163b433ebd4195a9c6400bd518caa20`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 24 Apr 2024 04:14:48 GMT
ADD file:49759b7a74bac875e3619e20ed5a9521101c7729f601d90976d0755d30e97499 in / 
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYPY_VERSION=7.3.16
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux64.tar.bz2'; 			sha256='404e6180d6caf9258eaab0c02c72018e9aa8eb03ab9094a0ff17ee5e3b265ac1'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-aarch64.tar.bz2'; 			sha256='fc720999bc5050e1d3706b3b6445e695cf42bfc71ebc7c88ed6bb88828b1d385'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux32.tar.bz2'; 			sha256='0df48aa780159e879ac89a805d143e4a6cd1b842f98046f5a3f865814bfaa2a4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-s390x.tar.bz2'; 			sha256='af97efe498a209ba18c7bc7d084164a9907fb3736588b6864955177e19d5216a'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["pypy3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:76956b537f14770ffd78afbe4f17016b2794c4b9b568325e8079089ea5c4e8cd`  
		Last Modified: Tue, 02 Jul 2024 01:29:27 GMT  
		Size: 31.4 MB (31422284 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db5fa142287b5e2ea1cb3fdcef8dd067eff6342e9a900fe73f28b64968bf7cbc`  
		Last Modified: Tue, 02 Jul 2024 03:24:10 GMT  
		Size: 1.1 MB (1066633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dedb707413502406462031e08f4a0f2d2592a5fc306016d38a1180194ee8086d`  
		Last Modified: Tue, 02 Jul 2024 03:24:10 GMT  
		Size: 30.5 MB (30475138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:58cab1f282c07e83465cb94a73aae106897dfc53147d3c1188632d352da481ec`  
		Last Modified: Tue, 02 Jul 2024 03:24:10 GMT  
		Size: 3.3 MB (3300894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c36dbbc5573186fff59b1adf3d27c923916757335c50248ac02f69b42326b7f9`  
		Last Modified: Thu, 11 Jul 2024 16:58:35 GMT  
		Size: 6.4 MB (6405772 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:d5bbdb16cbc06e7faffa02343c365cc9daf6202feb5b3fc71809b4832ae1f810
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2674362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4671b089202a97b8b4c50c01c3f1cce681fc3d285f86ce8c397075f926717d30`

```dockerfile
```

-	Layers:
	-	`sha256:ca61a091c94c968f6615894c4a9f073677445dc8aa71f82892fe26a2e82704e9`  
		Last Modified: Thu, 11 Jul 2024 16:58:35 GMT  
		Size: 2.7 MB (2665039 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c55c23ea8c88a93be563ad5d8207ec1da6eb276906f97e6c193d3abc32916793`  
		Last Modified: Thu, 11 Jul 2024 16:58:34 GMT  
		Size: 9.3 KB (9323 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:7bad0839c61ca7d36f850f8fd19ea573c230fc86b65138a96ecb89b80abd6681
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69617758 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59e56fd2a5beb539988618e1466fc814fe65622bec4d64c73e4d25d61a7a61af`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 24 Apr 2024 04:14:48 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYPY_VERSION=7.3.16
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux64.tar.bz2'; 			sha256='404e6180d6caf9258eaab0c02c72018e9aa8eb03ab9094a0ff17ee5e3b265ac1'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-aarch64.tar.bz2'; 			sha256='fc720999bc5050e1d3706b3b6445e695cf42bfc71ebc7c88ed6bb88828b1d385'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux32.tar.bz2'; 			sha256='0df48aa780159e879ac89a805d143e4a6cd1b842f98046f5a3f865814bfaa2a4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-s390x.tar.bz2'; 			sha256='af97efe498a209ba18c7bc7d084164a9907fb3736588b6864955177e19d5216a'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["pypy3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d13ad33c16eef01d20d5563bfb2ec4f25c0d12699b40cdab418e47b88d2f02e2`  
		Last Modified: Tue, 02 Jul 2024 00:43:04 GMT  
		Size: 30.1 MB (30069615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebd2bd797f61d8a588af0e5d37443f731d568f431e81c8e6108cfeb31b15b4c`  
		Last Modified: Tue, 02 Jul 2024 19:46:43 GMT  
		Size: 1.1 MB (1053908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f45c3a8ec08e0260fdac7aa42155a35ad062619611aa1760e2aa93acddb4271`  
		Last Modified: Tue, 02 Jul 2024 19:46:44 GMT  
		Size: 28.8 MB (28788058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:733bbebcb6ec3e1352a3c8795000245b7fdc48ced94862cd4a0718efca5a9900`  
		Last Modified: Tue, 02 Jul 2024 19:46:43 GMT  
		Size: 3.3 MB (3300549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70d93b454d61dcc6273c8cdb4eb240de67a25b86049a5e5365371c1bf0d3ce94`  
		Last Modified: Wed, 03 Jul 2024 08:19:21 GMT  
		Size: 6.4 MB (6405628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:a2a2bcbe748e33a80816d47200c0589093e27d98d1298bc1b2ff9c18b830223b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2675108 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf95fe23f8b2d15bbbefc3064e8b5e0e5eaadbebfa17cfe5ea8fbcdcd9495668`

```dockerfile
```

-	Layers:
	-	`sha256:bf377a330e2b3a0a7c37db8c42391d158f3fd2581b256cc9735e22db7d04f1b5`  
		Last Modified: Thu, 11 Jul 2024 17:04:26 GMT  
		Size: 2.7 MB (2665339 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0e62b2a39edc4a5ee7111123e23673f2d0e2e2ddbef11ca666fb725dc880a9f2`  
		Last Modified: Thu, 11 Jul 2024 17:04:25 GMT  
		Size: 9.8 KB (9769 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.10-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:493b5402518e4400a9ac0aec152b3bd581afab498bcd4200cdc09f36c7fdc6e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70006212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed06a5dc15ecc1b0e8a19f3f9b019942e51185cc6f688b8db5f67193ee191672`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 24 Apr 2024 04:14:48 GMT
ADD file:619dea132b057660136807b341227cbc3c7c9661313584d2fc0338130dc32f3e in / 
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYPY_VERSION=7.3.16
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux64.tar.bz2'; 			sha256='404e6180d6caf9258eaab0c02c72018e9aa8eb03ab9094a0ff17ee5e3b265ac1'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-aarch64.tar.bz2'; 			sha256='fc720999bc5050e1d3706b3b6445e695cf42bfc71ebc7c88ed6bb88828b1d385'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux32.tar.bz2'; 			sha256='0df48aa780159e879ac89a805d143e4a6cd1b842f98046f5a3f865814bfaa2a4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-s390x.tar.bz2'; 			sha256='af97efe498a209ba18c7bc7d084164a9907fb3736588b6864955177e19d5216a'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["pypy3"]
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HY_VERSION=0.29.0
# Wed, 10 Jul 2024 23:46:02 GMT
ENV HYRULE_VERSION=0.6.0
# Wed, 10 Jul 2024 23:46:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 10 Jul 2024 23:46:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6b5c41ccfba7fdb5c6183fbfde2e04bffba42b8f1f65b46c6b641ecf9c032ab5`  
		Last Modified: Tue, 23 Jul 2024 03:58:33 GMT  
		Size: 32.4 MB (32413808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a99d79ba3b9694cba07ce96b66e8011f22bb1c2159ad68cb7e39da4d161e923b`  
		Last Modified: Tue, 23 Jul 2024 06:11:03 GMT  
		Size: 1.1 MB (1079120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1dc8492b56337233a690fea23868b9fee1f039932b82d4dff41c3dc74c14a2a`  
		Last Modified: Tue, 23 Jul 2024 06:11:04 GMT  
		Size: 26.8 MB (26807195 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5023f3ffdf7c072dcfa004fd597c6a07236dc0cdb10c99882188bfee208db975`  
		Last Modified: Tue, 23 Jul 2024 06:11:03 GMT  
		Size: 3.3 MB (3300445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bc54f0b1ac053f339c8b1ee4c0e11286f9fb6c8e0b7a17972945fb0166c2488`  
		Last Modified: Tue, 23 Jul 2024 07:17:23 GMT  
		Size: 6.4 MB (6405644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:dc3b10a752521fc29ff4f0a2b70a274f2292db909ccd0dff86d878afcf3e77a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2694524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:84c622e89a1dfa5cec0958f7ad1e4db1ff33d39d9f2b64851fd5729d1201eae5`

```dockerfile
```

-	Layers:
	-	`sha256:acef0cfa0d020e1ae157171c8ea7d2a11a63c0fb9772e71252a95e16a6cc03de`  
		Last Modified: Tue, 23 Jul 2024 07:17:23 GMT  
		Size: 2.7 MB (2685252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5332a9de72f4e717f91e018d7702143464762f71335a6639649ab1ac766c92f2`  
		Last Modified: Tue, 23 Jul 2024 07:17:22 GMT  
		Size: 9.3 KB (9272 bytes)  
		MIME: application/vnd.in-toto+json
