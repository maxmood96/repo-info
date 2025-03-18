## `hylang:1-pypy3.10-bookworm`

```console
$ docker pull hylang@sha256:1cbac604ce5632f4a4fefadc2e8f1dd0152a3446f2c1fdd994961004e2d53e8e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:1-pypy3.10-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:88d6f586ad47f6af614966c573626ba82805b5819f3b15838e13b7e0116b9a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72641798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9833ea31fa10f5d70f1e57573ffd4bc2c96b535e6f24f01483bba71f59f1e256`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 26 Feb 2025 17:12:33 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
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
# Thu, 27 Feb 2025 17:10:02 GMT
ENV HY_VERSION=1.0.0
# Thu, 27 Feb 2025 17:10:02 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 27 Feb 2025 17:10:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 27 Feb 2025 17:10:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cbe5bc7436a25c6ff87fedc8953ae6ec05cb82ba3e18ebab229f3e6bd0fc2b06`  
		Last Modified: Mon, 17 Mar 2025 23:20:37 GMT  
		Size: 3.5 MB (3499357 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54721f0954c745ee2392535ecfe56b012ef4907216ddbc6a6c0fc21e5e8f6b25`  
		Last Modified: Mon, 17 Mar 2025 23:20:38 GMT  
		Size: 31.3 MB (31268115 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bac505869db56b113332b9df334cf03208294782c22dee593daf4f4f2b5ff59`  
		Last Modified: Mon, 17 Mar 2025 23:20:37 GMT  
		Size: 3.3 MB (3305499 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ce17520a9dce42b9642288bdf2396de19a14c069e1aaa8022cbd33d3588092b`  
		Last Modified: Tue, 18 Mar 2025 00:18:55 GMT  
		Size: 6.4 MB (6363962 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:acb7f6485db094f1de0d5eef7002e0da503d48dea6b918e72999f117a3ab96d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2417549 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b25084835e0890f1ff7547a3691d7d067b8f9713f6de546d8f29c3de34321e8`

```dockerfile
```

-	Layers:
	-	`sha256:765348a5847ff7be346c58d60e27479e9c0d52ed62a93d17d50e8fd89141349e`  
		Last Modified: Tue, 18 Mar 2025 00:18:54 GMT  
		Size: 2.4 MB (2405772 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cb621911adb0b352a8c2a5592484b19f5e1ef47608d11bcd3f5295265ca293fc`  
		Last Modified: Tue, 18 Mar 2025 00:18:54 GMT  
		Size: 11.8 KB (11777 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:908b6bac8525b02a7531440c288501daba45ea005093a8fa24c602db1b712464
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70579235 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:713923297151ef1c0327a4bd6176c62d5ce37888b6ad5e6242c77263f47ebc60`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 24 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
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
# Thu, 27 Feb 2025 17:10:02 GMT
ENV HY_VERSION=1.0.0
# Thu, 27 Feb 2025 17:10:02 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 27 Feb 2025 17:10:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 27 Feb 2025 17:10:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d51c377d94dadb60d549c51ba66d3c4eeaa8bace4935d570ee65d8d1141d38fc`  
		Last Modified: Tue, 25 Feb 2025 01:30:59 GMT  
		Size: 28.0 MB (28048425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:18428d18a198b6f029c74364726487b207e1961c00bb262c1d3d995044ca8d4b`  
		Last Modified: Thu, 27 Feb 2025 00:26:46 GMT  
		Size: 3.3 MB (3322899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b4c8ed1d447c25f3445c837be0d37265b2365ac5d37a6230a6b2d2bd632e231`  
		Last Modified: Thu, 27 Feb 2025 01:52:47 GMT  
		Size: 29.5 MB (29538568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cce16db6a4fecff2f40d276413f443d65befdd8b825e6db131bcc86742bc1b92`  
		Last Modified: Thu, 27 Feb 2025 01:52:46 GMT  
		Size: 3.3 MB (3305583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8cc1abfa674eff904a661863afe78cd8e6acd2fd1e1f0e96543a27f93f75347`  
		Last Modified: Thu, 27 Feb 2025 02:08:08 GMT  
		Size: 6.4 MB (6363760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:579e9464ca3bbb28884728fa67b1691946efbb5886ef7a92cc2b80f01ee73afc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2418191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6cf4c50d1d1a2962d8a281f33269f4d8872a9bf7696baff5ccac1b87d736650f`

```dockerfile
```

-	Layers:
	-	`sha256:90c83ccc5e53ff5fcb05b97f4f59b944d1259f33c869477547da9a176cce5968`  
		Last Modified: Thu, 27 Feb 2025 18:24:16 GMT  
		Size: 2.4 MB (2406167 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ffaf2f45ccfe353020177d510355fbb92b15fa018070585fabdaa59b11ede66`  
		Last Modified: Thu, 27 Feb 2025 18:24:15 GMT  
		Size: 12.0 KB (12024 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.10-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:3bac3eee169eccd9da95226c972c0b24410e0bfc13ed35fa60d91a3d9d2bfcb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70088562 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27c692b47fd1bb582885be4b7ca948c5bacbbc7d85eeafebf0490f62c277be93`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 26 Feb 2025 17:12:33 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
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
# Thu, 27 Feb 2025 17:10:02 GMT
ENV HY_VERSION=1.0.0
# Thu, 27 Feb 2025 17:10:02 GMT
ENV HYRULE_VERSION=0.8.0
# Thu, 27 Feb 2025 17:10:02 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 27 Feb 2025 17:10:02 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bcaee6ac5853b09627b7f4c03173ea3270305bb219e473ff0221bbf4df74f9e`  
		Last Modified: Mon, 17 Mar 2025 23:28:22 GMT  
		Size: 3.5 MB (3503453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c9a9bcdb30497b3585992e7cd111c37427ef8a262f51b740954ee16c61ec3a0`  
		Last Modified: Mon, 17 Mar 2025 23:28:22 GMT  
		Size: 27.7 MB (27726616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9988d4d42f8b27d2b0b08304b3c29674d6b888154ba12e006485da6ad3cbc244`  
		Last Modified: Mon, 17 Mar 2025 23:28:22 GMT  
		Size: 3.3 MB (3305157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4fdf901c9cbafd2cc2e8b591da80f1919497091984b653c7d7d3ef0e05d8e625`  
		Last Modified: Tue, 18 Mar 2025 00:25:02 GMT  
		Size: 6.4 MB (6363808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:fc07ccce6e360546b56ec9d659322630ae51a630d19ed1f47300f456531c9919
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2414534 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2c9be2fba7cab035fde1db0e6661551841054cdb8d0cc63383da090ee7135269`

```dockerfile
```

-	Layers:
	-	`sha256:3f3d3c01fd9ba4cb4ffe47457cdb76691d32f79d30128409b175722eddd80ada`  
		Last Modified: Tue, 18 Mar 2025 00:25:02 GMT  
		Size: 2.4 MB (2402849 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6238a1734017b0aeb8ef0066cdec16c35b7c7f2ccbfd92532f72cb999effe07c`  
		Last Modified: Tue, 18 Mar 2025 00:25:02 GMT  
		Size: 11.7 KB (11685 bytes)  
		MIME: application/vnd.in-toto+json
