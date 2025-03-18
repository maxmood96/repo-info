## `pypy:3-slim-bullseye`

```console
$ docker pull pypy@sha256:4fada5b613d248cf571815d5a6af322c2aa75eca6d80cd20c17d03e2cc2d5554
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:3-slim-bullseye` - linux; amd64

```console
$ docker pull pypy@sha256:d1d869b23a80a23e097f6be27246f9219381eb82451d0a120422c6ad71aa65a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65641466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8276c68529bb08f3d5775db4af50597b72a981421bd88bdb4fe5fea332a6ff1b`
-	Default Command: `["pypy3"]`

```dockerfile
# Wed, 26 Feb 2025 17:12:33 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1742169600'
# Wed, 26 Feb 2025 17:12:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 17:12:33 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2025 17:12:33 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 17:12:33 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 26 Feb 2025 17:12:33 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux64.tar.bz2'; 			sha256='c73ac2cc2380ac9227fd297482bf2a3e17a80618ba46db7544d535515321ec1e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-aarch64.tar.bz2'; 			sha256='af27a589178f11198e2244ab65ca510630ba97c131d7ccc4021eb5bc58de7f57'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux32.tar.bz2'; 			sha256='e63a4fcad2641ee541e852918befb513abf04ce7070f743a50778cae9f9da80e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 26 Feb 2025 17:12:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 26 Feb 2025 17:12:33 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 26 Feb 2025 17:12:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 26 Feb 2025 17:12:33 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:55147cbf65d4d152c070165835355b8ea7a090d48d81ba52cbeb9bbe8d629fc0`  
		Last Modified: Mon, 17 Mar 2025 22:17:31 GMT  
		Size: 30.3 MB (30253836 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:695958b708a9d5953136b6f7dcb9e64b431af48bac6b23004ce32a837f9acac2`  
		Last Modified: Mon, 17 Mar 2025 23:20:39 GMT  
		Size: 862.6 KB (862580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59160d5f743e79f38a40168fddb95c25422afa4d72c05546fe4d9a2a316ad042`  
		Last Modified: Mon, 17 Mar 2025 23:20:40 GMT  
		Size: 31.2 MB (31218797 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:297f99dcb4fc726ea34f4351da178890c6b0046927d85bf135fdbcc7c5841038`  
		Last Modified: Mon, 17 Mar 2025 23:20:40 GMT  
		Size: 3.3 MB (3306253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-slim-bullseye` - unknown; unknown

```console
$ docker pull pypy@sha256:b6c3e592aebe5e910e95dc9fdfc7a8ebc9e5436b15dbedd9c00ee486c5fcd1f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2716858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:54aaf50e7c70a48f96d00a02a74e9d4a494281087966e6765f37552f06f5f4c1`

```dockerfile
```

-	Layers:
	-	`sha256:9e9da1b5d32e8f78a88efe4ce682f88e7bb1fc30b9ade3f1923c7ed6569d7f93`  
		Last Modified: Mon, 17 Mar 2025 23:20:39 GMT  
		Size: 2.7 MB (2691410 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6951e91de13db64d8221874eb3be1a62bd6aebcb911f184ab238d92f9610e2c`  
		Last Modified: Mon, 17 Mar 2025 23:20:39 GMT  
		Size: 25.4 KB (25448 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:3-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:0e69d00dda3728dfd86b5fd80aa6802be5570be8267044a2132e32315e53bc53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62398201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fc583668324ac0584977c2dd31b6449ea0238c5d667a41f56c0323c32a168c59`
-	Default Command: `["pypy3"]`

```dockerfile
# Wed, 26 Feb 2025 17:12:33 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1742169600'
# Wed, 26 Feb 2025 17:12:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 17:12:33 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2025 17:12:33 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 17:12:33 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 26 Feb 2025 17:12:33 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux64.tar.bz2'; 			sha256='c73ac2cc2380ac9227fd297482bf2a3e17a80618ba46db7544d535515321ec1e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-aarch64.tar.bz2'; 			sha256='af27a589178f11198e2244ab65ca510630ba97c131d7ccc4021eb5bc58de7f57'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux32.tar.bz2'; 			sha256='e63a4fcad2641ee541e852918befb513abf04ce7070f743a50778cae9f9da80e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 26 Feb 2025 17:12:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 26 Feb 2025 17:12:33 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 26 Feb 2025 17:12:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 26 Feb 2025 17:12:33 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:6eba8885c82049d690776150810f32585aca6c3eba49f692753434bdaee447ec`  
		Last Modified: Mon, 17 Mar 2025 22:18:52 GMT  
		Size: 28.7 MB (28745923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11a581cf02ed57580c983e108e5992590a286e3db6184f7daec762199cb45b1a`  
		Last Modified: Tue, 18 Mar 2025 02:35:49 GMT  
		Size: 849.8 KB (849774 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:09ca512d8722d90451229e49730eff63fece8822260401cb4ea6add907833993`  
		Last Modified: Tue, 18 Mar 2025 02:37:29 GMT  
		Size: 29.5 MB (29496298 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a04be67448ec1d1ea2d9c3f37bbfb9d2448c32a98bfee452dfb311ae52566ed`  
		Last Modified: Tue, 18 Mar 2025 02:37:29 GMT  
		Size: 3.3 MB (3306206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-slim-bullseye` - unknown; unknown

```console
$ docker pull pypy@sha256:6fff53d233f2420763ae75a5d1293c012a65b7643a1058eadb42ccda86b7b9cb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717364 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ee129926becddd7243ecce85168440607d37f650f3ce71c815fd8399c7e3162`

```dockerfile
```

-	Layers:
	-	`sha256:326e5113f898a2baba9a2b00713661e946ebf4fbd2b4c202e71b1724b8f9c823`  
		Last Modified: Tue, 18 Mar 2025 02:37:29 GMT  
		Size: 2.7 MB (2691723 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab8612dd1908c5d279a6419484a5102b63ec2a0ba252f1e4766abb7ec319c617`  
		Last Modified: Tue, 18 Mar 2025 02:37:28 GMT  
		Size: 25.6 KB (25641 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:3-slim-bullseye` - linux; 386

```console
$ docker pull pypy@sha256:39394208555cc43ef20daf15370c7e7ff64c757fdbd203fe4a1c3af823306b8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.0 MB (63004552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0bc2a12e5241aed028f359519cac2dc7ffd3c4829f080d810849546bfe329c4d`
-	Default Command: `["pypy3"]`

```dockerfile
# Wed, 26 Feb 2025 17:12:33 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1742169600'
# Wed, 26 Feb 2025 17:12:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 17:12:33 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2025 17:12:33 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 17:12:33 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 26 Feb 2025 17:12:33 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux64.tar.bz2'; 			sha256='c73ac2cc2380ac9227fd297482bf2a3e17a80618ba46db7544d535515321ec1e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-aarch64.tar.bz2'; 			sha256='af27a589178f11198e2244ab65ca510630ba97c131d7ccc4021eb5bc58de7f57'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux32.tar.bz2'; 			sha256='e63a4fcad2641ee541e852918befb513abf04ce7070f743a50778cae9f9da80e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 26 Feb 2025 17:12:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 26 Feb 2025 17:12:33 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 26 Feb 2025 17:12:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 26 Feb 2025 17:12:33 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:e83ba34877ecae8e583197e97ef35a452a1d1b81c406023bf40d3c79d5ba9025`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 31.2 MB (31180337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4ea4391e645c55c82a00c7c2c9183cb39261d4a88a05067b51c6f5b3b9fdafe`  
		Last Modified: Mon, 17 Mar 2025 23:28:24 GMT  
		Size: 874.7 KB (874705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56bf2a0d4fa886c96d6dee41333dabd07adf6df9149310088e2ed4b60d7580f6`  
		Last Modified: Mon, 17 Mar 2025 23:28:25 GMT  
		Size: 27.6 MB (27643463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ce4889b92881ef288294b701223154b7717a6c19c42a4f2c3ae735bd2e35be2`  
		Last Modified: Mon, 17 Mar 2025 23:28:24 GMT  
		Size: 3.3 MB (3306047 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-slim-bullseye` - unknown; unknown

```console
$ docker pull pypy@sha256:eee3384bb559085aa03dee798f953a33c3411759d22d73c73b6f9daed1e150aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2713898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:558dcb69bfbd891094ae2c4854b60049c2e44ea1a208a8c0051de55bb16327ee`

```dockerfile
```

-	Layers:
	-	`sha256:107749efe232dcbe895e10ec80e47fee92b613ef64704fd278d77d753edbde8c`  
		Last Modified: Mon, 17 Mar 2025 23:28:24 GMT  
		Size: 2.7 MB (2688511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:981fd95d74e042df4047e9684a1adce3478f1e2e847a8b50a787b7ac7b75cdb3`  
		Last Modified: Mon, 17 Mar 2025 23:28:24 GMT  
		Size: 25.4 KB (25387 bytes)  
		MIME: application/vnd.in-toto+json
