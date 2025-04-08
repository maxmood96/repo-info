## `hylang:pypy-bullseye`

```console
$ docker pull hylang@sha256:ac4a06d943696cf06e597440e63c2ffae35075f5b75fd76cf50f8627e77cc500
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:pypy-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:9a81a0abd9a0f9a1535fe869a2e5cd3d750076695bfef64b3deb445afc616da1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72212369 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf5a0bb2414308ecb8812352006fb34115dbbb54e5d923d6aeb507daee6c0771`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 26 Feb 2025 17:12:33 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
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
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b983e127c643116d446fa1b64216f464e1d06a8bfaeeb8a895c361c1bc3f5652`  
		Last Modified: Tue, 08 Apr 2025 00:23:09 GMT  
		Size: 30.3 MB (30257419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40e3f37de41f363f6c39e3cd596104f666f3e1b32ab2e0b054dd77f0c692840a`  
		Last Modified: Tue, 08 Apr 2025 01:31:34 GMT  
		Size: 1.1 MB (1066604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f80d9bcf9d03a19ff434000b74089e81de8773420710a69c967f0a33c793b35f`  
		Last Modified: Tue, 08 Apr 2025 01:31:35 GMT  
		Size: 31.2 MB (31218775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a6cf90ca4ea3ea3fa12969bf4b6a6de4a9520b5448c83133fedb13c7d9f5da4`  
		Last Modified: Tue, 08 Apr 2025 01:31:34 GMT  
		Size: 3.3 MB (3306338 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:970ea0b611339234f6ed26e6155ba0eab984ff77a6a69a72e7149fa00e31a64e`  
		Last Modified: Tue, 08 Apr 2025 02:22:40 GMT  
		Size: 6.4 MB (6363233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:c4c3dea462c0851a137496da358379fc810face78e48c9e8c15bb96d4aa7959f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4b4639a68890f32f0754256353bdeb277629cb33ec2ea47f7e37d3b1716c3d`

```dockerfile
```

-	Layers:
	-	`sha256:650592074777535105faf809a1090f4643bf2ed170498560a33eaa89119bca0f`  
		Last Modified: Tue, 08 Apr 2025 02:22:39 GMT  
		Size: 2.7 MB (2700549 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:858d3ecafe6635bc12a60a0edbfe789952f2284d66ce1664c1857ff8976175bc`  
		Last Modified: Tue, 08 Apr 2025 02:22:39 GMT  
		Size: 9.3 KB (9345 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:0410d9236e195c8740aca66176bb2198d97e900820330c6edb773fd1c99cdd69
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68761508 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb3ade72a593b4509abaa75a10d2956cdaee1d8194cf2bd70bac3d5bc6341ef1`
-	Default Command: `["hy"]`

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
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
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
	-	`sha256:aef98f04ff87f73c3ccf738a2617d3c9ca5f1d5153531d9c75e3cdccab751754`  
		Last Modified: Wed, 19 Mar 2025 23:26:29 GMT  
		Size: 6.4 MB (6363307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:8b064f54341b8d773fc006d161f546c18b185101da6c4cac02ea7c0b6d9a74e9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2708430 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcd4cc21e1042c953000c4f7102f14103976aa2b37c1eb9fe476b3daf161610b`

```dockerfile
```

-	Layers:
	-	`sha256:fdf4e1283add7ddf6df96fd98765104f2949b1410699f39080b05fe49677cf25`  
		Last Modified: Wed, 19 Mar 2025 23:26:29 GMT  
		Size: 2.7 MB (2698936 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aefc18fb74c2f44dc5fb649d1314a82d682b23dc2e31df0e1aaaf831c267e4a7`  
		Last Modified: Wed, 19 Mar 2025 23:26:28 GMT  
		Size: 9.5 KB (9494 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:ee545672f20f214f75b6fcf097f55b0dc7778c6e6e2b675a579718b60b1ea95b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.6 MB (69576352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a12f43018d8f5cb9a49985df9d04565a17584ad91c253c1e769f214d60aea843`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 26 Feb 2025 17:12:33 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
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
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c7f226a3ed9e3a783e859dc8479e50da2694130147ffb4885645e02664eedbec`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 31.2 MB (31184573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb02b4cbbe2b0d03199e40b19584fcd761bc3901dafc1f6acedf4d2ff74550c`  
		Last Modified: Tue, 08 Apr 2025 01:26:37 GMT  
		Size: 1.1 MB (1079108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e06025cdd47d100a9d5b8f16c543e041598ec451127024ef5aac53e293c6f54`  
		Last Modified: Tue, 08 Apr 2025 01:26:38 GMT  
		Size: 27.6 MB (27643501 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:36dac6d64bd86b7e223e6541ec07540afa58059790fc544fa77ed3bce376ca0e`  
		Last Modified: Tue, 08 Apr 2025 01:26:37 GMT  
		Size: 3.3 MB (3306064 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04fdc75e842d9bfa6b11f42b8ce149fbef0fe4f84641a0f6bc7394a3ba2d68be`  
		Last Modified: Tue, 08 Apr 2025 02:21:28 GMT  
		Size: 6.4 MB (6363106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:b2f42b8261685c08953fed8616cecc04b17112c90d5c31e259859a0f17a24ae9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2706947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d8ecc2d4c86b143f5165f98ad114d6e3c6001ebf5d04a2b7174452a6304409c7`

```dockerfile
```

-	Layers:
	-	`sha256:2b6082e56e85329c93d73f13d91692113da3c9371188ea3c405b189de5078ff0`  
		Last Modified: Tue, 08 Apr 2025 02:21:27 GMT  
		Size: 2.7 MB (2697655 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25ae412bb1a18e9adb1c201d808ff00094a054e962fcdbc6eab16c9536089896`  
		Last Modified: Tue, 08 Apr 2025 02:21:27 GMT  
		Size: 9.3 KB (9292 bytes)  
		MIME: application/vnd.in-toto+json
