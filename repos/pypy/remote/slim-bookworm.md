## `pypy:slim-bookworm`

```console
$ docker pull pypy@sha256:4dce58b4f5feeec1b02a6ee0b4eef5113354f77bda9d960ed9cea21d96dbfbaf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:slim-bookworm` - linux; amd64

```console
$ docker pull pypy@sha256:ed3bf4cc6cd5ac66925d9078303f0c8936973a8eb2e2310603a1825acc12be16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66519217 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95fae5c7493c5240ad39c088549eaed03fc71eb2f2457f87d07d6ae5f8e7ccf7`
-	Default Command: `["pypy3"]`

```dockerfile
# Wed, 28 Aug 2024 10:12:01 GMT
ADD file:a9a95cfab16803be03e59ade41622ef5061cf90f2d034304fe4ac1ee9ff30389 in / 
# Wed, 28 Aug 2024 10:12:01 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 10:12:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 10:12:01 GMT
ENV LANG=C.UTF-8
# Wed, 28 Aug 2024 10:12:01 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 10:12:01 GMT
ENV PYPY_VERSION=7.3.17
# Wed, 28 Aug 2024 10:12:01 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.17-linux64.tar.bz2'; 			sha256='fdcdb9b24f1a7726003586503fdeb264fd68fc37fbfcea022dcfe825a7fee18b'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.17-aarch64.tar.bz2'; 			sha256='53b6e5907df869c49e4eae7aca09fba16d150741097efb245892c1477d2395f2'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.17-linux32.tar.bz2'; 			sha256='e534110e1047da37c1d586c392f74de3424f871d906a2083de6d41f2a8cc9164'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 28 Aug 2024 10:12:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 28 Aug 2024 10:12:01 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 28 Aug 2024 10:12:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 28 Aug 2024 10:12:01 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:302e3ee498053a7b5332ac79e8efebec16e900289fc1ecd1c754ce8fa047fcab`  
		Last Modified: Fri, 27 Sep 2024 04:33:11 GMT  
		Size: 29.1 MB (29126276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6d45ceb2c3f5eeba85e7b665c5692ac6c6e6cb2851a11cca6a79e5c64cb9a7dd`  
		Last Modified: Fri, 27 Sep 2024 06:03:15 GMT  
		Size: 3.5 MB (3499013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497b189029e92f9314f71425bbc4cf5e1c0124f001b2f9fe24c0f94f07ea745e`  
		Last Modified: Fri, 27 Sep 2024 06:03:16 GMT  
		Size: 30.6 MB (30592917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1e8915aee212ac3eb0316ddb7d2ce6d64c6a2458c23f6464a2427df6a9c9e72`  
		Last Modified: Fri, 27 Sep 2024 06:03:15 GMT  
		Size: 3.3 MB (3301011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:d8acbdd6b4873bb661b6a123dd46a29fa167be568dce0c4df2432c509e7f414b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2411192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3404276def6738a6d241ff0a81f1331639c52d9ecdd1a518c5899c91090dd84e`

```dockerfile
```

-	Layers:
	-	`sha256:61c9b68567b360542730a5071aac5178c2822a1b0561adc362f49eb87e197a75`  
		Last Modified: Fri, 27 Sep 2024 06:03:15 GMT  
		Size: 2.4 MB (2385947 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:db5bef92420a2efab37da52d3285286e5d464bb0ad149a332de102d2ef38b4c2`  
		Last Modified: Fri, 27 Sep 2024 06:03:15 GMT  
		Size: 25.2 KB (25245 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:ef7100a1a60db7ec51f9759ade6809a7eae5480b5e336abc83f323b49104f679
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.7 MB (64727194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:da0546589710d835a90b124853f528f7e36fad97810d056701fba9e0ce858c91`
-	Default Command: `["pypy3"]`

```dockerfile
# Wed, 28 Aug 2024 10:12:01 GMT
ADD file:06a1877f1e100122a40ed52ce771bfa7e2ab3d28323780f58f1e5b57c1e576f9 in / 
# Wed, 28 Aug 2024 10:12:01 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 10:12:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 10:12:01 GMT
ENV LANG=C.UTF-8
# Wed, 28 Aug 2024 10:12:01 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 10:12:01 GMT
ENV PYPY_VERSION=7.3.17
# Wed, 28 Aug 2024 10:12:01 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.17-linux64.tar.bz2'; 			sha256='fdcdb9b24f1a7726003586503fdeb264fd68fc37fbfcea022dcfe825a7fee18b'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.17-aarch64.tar.bz2'; 			sha256='53b6e5907df869c49e4eae7aca09fba16d150741097efb245892c1477d2395f2'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.17-linux32.tar.bz2'; 			sha256='e534110e1047da37c1d586c392f74de3424f871d906a2083de6d41f2a8cc9164'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 28 Aug 2024 10:12:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 28 Aug 2024 10:12:01 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 28 Aug 2024 10:12:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 28 Aug 2024 10:12:01 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:92c3b3500be621c72c7ac6432a9d8f731f145f4a1535361ffd3a304e55f7ccda`  
		Last Modified: Wed, 04 Sep 2024 21:42:36 GMT  
		Size: 29.2 MB (29156545 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:89ed8cf8b863a96ea1c670eb011e3e447b82f9a1b376a428f7e41ba6ce3522c9`  
		Last Modified: Thu, 05 Sep 2024 16:18:30 GMT  
		Size: 3.3 MB (3322451 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:faf01acff4355e4960de113e4d9ad6c3917bb1ed1e75b38bab834fd05c705aad`  
		Last Modified: Thu, 05 Sep 2024 16:18:31 GMT  
		Size: 28.9 MB (28947197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d66cef4ac41dbbd476a6b560e941b7a1fd203ec00aad50735d9b1603af36d902`  
		Last Modified: Thu, 05 Sep 2024 16:18:30 GMT  
		Size: 3.3 MB (3301001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:24dc491e1da50584a850eec50d7b7bc88c6d3e9e2e653be54ad1d9492927cb86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2411866 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6344bd16e0ff7ba85947024deeeb4e1e78d9dc661b705069a3731c20cd976d55`

```dockerfile
```

-	Layers:
	-	`sha256:f96bceb05c523c15abdeb22a61836244f479243f6e3d47a8bc6d639429fbdaf4`  
		Last Modified: Thu, 05 Sep 2024 16:18:30 GMT  
		Size: 2.4 MB (2386252 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f315a6f32e1aa96da53b2f2068b3e3bcfebb4f455a55e4e39cc0f2f11a5b3c0f`  
		Last Modified: Thu, 05 Sep 2024 16:18:30 GMT  
		Size: 25.6 KB (25614 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:f68966409ca9c05142c0669e8d203eb33136fdf4dad73a4ed4f8efd23371e00d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63891497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aeae06944abfb48c61f6046da1e8b4c44a8b5777a08d1cada9e30d7c5dd474ca`
-	Default Command: `["pypy3"]`

```dockerfile
# Wed, 28 Aug 2024 10:12:01 GMT
ADD file:1d96491aed0d3091aadb984e1dfe642343013348f4a1807a69e132efaed68030 in / 
# Wed, 28 Aug 2024 10:12:01 GMT
CMD ["bash"]
# Wed, 28 Aug 2024 10:12:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 10:12:01 GMT
ENV LANG=C.UTF-8
# Wed, 28 Aug 2024 10:12:01 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 10:12:01 GMT
ENV PYPY_VERSION=7.3.17
# Wed, 28 Aug 2024 10:12:01 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.17-linux64.tar.bz2'; 			sha256='fdcdb9b24f1a7726003586503fdeb264fd68fc37fbfcea022dcfe825a7fee18b'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.17-aarch64.tar.bz2'; 			sha256='53b6e5907df869c49e4eae7aca09fba16d150741097efb245892c1477d2395f2'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.17-linux32.tar.bz2'; 			sha256='e534110e1047da37c1d586c392f74de3424f871d906a2083de6d41f2a8cc9164'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 28 Aug 2024 10:12:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 28 Aug 2024 10:12:01 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 28 Aug 2024 10:12:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 28 Aug 2024 10:12:01 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:c304282df09b425e8240f53c55110ac282ba801da157a805e4fdbdf8c832b376`  
		Last Modified: Wed, 04 Sep 2024 22:48:08 GMT  
		Size: 30.1 MB (30144294 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1074bd9f27455227cf67fd6f241ebaee8db0785c99f2bf79e2db4651ba5bcbaf`  
		Last Modified: Thu, 05 Sep 2024 00:09:13 GMT  
		Size: 3.5 MB (3502366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b6f6b56c67e6d3554e6393d2189187804ef4420b5f89c7a5251965244149e1a`  
		Last Modified: Thu, 05 Sep 2024 00:09:13 GMT  
		Size: 26.9 MB (26944199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:543230f8b9baded6705cc6eb2ff88440829ff693bea0f778afe2dfbe288075aa`  
		Last Modified: Thu, 05 Sep 2024 00:09:13 GMT  
		Size: 3.3 MB (3300638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:551c920096f6663b008777a8cca89c3ca0bccbd72baf72e263a0e52d1fe2becf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2408232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:520b9259d587f24a08ffa5900ebfe7ad28f56e2842a37e07295872d3ff4a7623`

```dockerfile
```

-	Layers:
	-	`sha256:00750a308cb2306d0ef9d4a5e4f2cb651887c479c94bd999e7deedd9ef758100`  
		Last Modified: Thu, 05 Sep 2024 00:09:12 GMT  
		Size: 2.4 MB (2383045 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:61046f9aa27f28e657144e4d25d827ee907994d0319cc55098e17c6c50fef4f7`  
		Last Modified: Thu, 05 Sep 2024 00:09:12 GMT  
		Size: 25.2 KB (25187 bytes)  
		MIME: application/vnd.in-toto+json
