## `hylang:1-pypy`

```console
$ docker pull hylang@sha256:f3925bd97c26ddc8b38226d1f2e26115f4c53ba64cf0027cce7ec9d28f530e2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `hylang:1-pypy` - linux; amd64

```console
$ docker pull hylang@sha256:84f12cc2a492241da210d9fed25133f249aaf9f06152d483fd86d059af896e9d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.0 MB (71967960 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d98402a2d322e8716a5aa98d20d45168d138cfe31897de2ed94dcfcc501f7a6`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Aug 2024 10:12:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1736726400'
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
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:af302e5c37e9dc1dbe2eadc8f5059d82a914066b541b0d1a6daa91d0cc55057d`  
		Last Modified: Tue, 14 Jan 2025 01:33:13 GMT  
		Size: 28.2 MB (28212417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f244e8378a2fb3e652eacc00199723a81c135147885e83801007a145ea792d86`  
		Last Modified: Tue, 14 Jan 2025 02:41:05 GMT  
		Size: 3.5 MB (3499344 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e3538308e61fc080b9f4c56a42e6d5bf2294510822c6efde4d4b4670b985ed38`  
		Last Modified: Tue, 14 Jan 2025 02:41:05 GMT  
		Size: 30.6 MB (30592943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba07aee32b2a6f392371a7d07630a2fdd61095b9ffe4f70e4f33f3290aa1945e`  
		Last Modified: Tue, 14 Jan 2025 02:41:05 GMT  
		Size: 3.3 MB (3305496 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3cc14abcc0bb50ca06b6e837e443ecaff02d60b8f0b3e56716e17a9adba3b3`  
		Last Modified: Tue, 14 Jan 2025 03:20:20 GMT  
		Size: 6.4 MB (6357760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy` - unknown; unknown

```console
$ docker pull hylang@sha256:527fd9e0b3ef5129c004a859706cc2ff18276bc575af1aa32bcabfce0eb3b6d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2418733 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb876b58e80dac8b9a6fdc27af5746a25789f935ae8fcf941e88f8f8712a9ae`

```dockerfile
```

-	Layers:
	-	`sha256:dfef15ae196539737e77af4a22c4d840bd0933d8f96b18fc5855d92999e79de0`  
		Last Modified: Tue, 14 Jan 2025 03:20:20 GMT  
		Size: 2.4 MB (2406956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b79157d8ad63324a17f7a9f6279034ca9991d12660179fee720b24ac5aebcf98`  
		Last Modified: Tue, 14 Jan 2025 03:20:20 GMT  
		Size: 11.8 KB (11777 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:c09e8aa5fd27cf907a3832a0d3b3b44e958868ca3716937811ae6c0020a27226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (69974381 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d517dda0280f824fa4a4224b6baadb71507ec5e13d64bbf81f94a1517f0783c0`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Aug 2024 10:12:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1736726400'
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
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7ce705000c390df8b2edde0e8b9c65a6677da4503a8f8fd89b355a3f827a275f`  
		Last Modified: Tue, 14 Jan 2025 01:35:55 GMT  
		Size: 28.0 MB (28041031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf8a8427e8c7ea1c7d6ff549c644b9a0ab326666d4e21a0c2fe276b5de045dc6`  
		Last Modified: Tue, 14 Jan 2025 09:11:20 GMT  
		Size: 3.3 MB (3322860 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52f3c2c903f62b9b8d888d92668114acfa2e3a476613d6673216ec3096c59312`  
		Last Modified: Tue, 14 Jan 2025 09:11:20 GMT  
		Size: 28.9 MB (28947193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10b54f32ab25ebd0fbe08a8cdbf75e8d3ee981daf7b0694444b6fc59f50086ea`  
		Last Modified: Tue, 14 Jan 2025 09:11:20 GMT  
		Size: 3.3 MB (3305443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0da9a90c4279608cb0b90c7157b56470bc5ccfc3afa0dbce0d63d2e979dcc816`  
		Last Modified: Tue, 14 Jan 2025 16:44:32 GMT  
		Size: 6.4 MB (6357854 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy` - unknown; unknown

```console
$ docker pull hylang@sha256:6e623588db0f20637a3669562e75eb36e8ef4aa88fcefef526687c9ac4e6be16
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2419384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:590f622e23e7ecbd4c80503f9af5a11fd4a7aee4edd4a332caad22aea2b06554`

```dockerfile
```

-	Layers:
	-	`sha256:8a6b19faef5f6c222bbea2ed8186ea94555e3dbcf9a43c692ff6d022dd3bef7d`  
		Last Modified: Tue, 14 Jan 2025 16:44:30 GMT  
		Size: 2.4 MB (2407359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2113b7171c54fce43fca8bdab44772f6da4b7904db5eec3dc14446db8d7b4613`  
		Last Modified: Tue, 14 Jan 2025 16:44:29 GMT  
		Size: 12.0 KB (12025 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy` - linux; 386

```console
$ docker pull hylang@sha256:2694171b66a180961f4e1cf9c79443cec5fc18492b0b845162cceaaf6cbde317
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69298374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3f59f512115ddb22e5c9a0fcaf6cc51f40668138cf7e880e54038345c6add1d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Aug 2024 10:12:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1736726400'
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
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HY_VERSION=1.0.0
# Wed, 08 Jan 2025 17:56:16 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 08 Jan 2025 17:56:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 08 Jan 2025 17:56:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:57fff88fb79736a903f46d7ab2546a9d83e4b9cf9032f766ea3c92eb06acbcca`  
		Last Modified: Tue, 14 Jan 2025 01:33:46 GMT  
		Size: 29.2 MB (29187595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b76ffa1e6c19956991196e4c1f568315a5fa3b0858cac698985423072f635ac5`  
		Last Modified: Tue, 14 Jan 2025 02:35:20 GMT  
		Size: 3.5 MB (3503452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26de7d43db50cc7dfe3a1f5700b661ae0dbd707e7e9902fd7cf6839020957700`  
		Last Modified: Tue, 14 Jan 2025 02:35:21 GMT  
		Size: 26.9 MB (26944221 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4791efd22489b24cab412443249beb2cc1c33befe68f33c9e0535aa4b447870c`  
		Last Modified: Tue, 14 Jan 2025 02:35:20 GMT  
		Size: 3.3 MB (3305156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16959d277eedc077b1da25b511e20348ffd964f5c3cd8e9580472cf04b1b123f`  
		Last Modified: Tue, 14 Jan 2025 03:25:23 GMT  
		Size: 6.4 MB (6357950 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy` - unknown; unknown

```console
$ docker pull hylang@sha256:c990b1ea7cf6ad845ed58900228849373f657e05eb66b5a25d6de9ee6d411045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ace5597cbecbface978e5b9f106754d34bca51b6865645e424d811708c620a8b`

```dockerfile
```

-	Layers:
	-	`sha256:34e2aa2b1a71d95dd5c3fd467860c8755dc48afa0392aa76ef833a2ea02c45ca`  
		Last Modified: Tue, 14 Jan 2025 03:25:23 GMT  
		Size: 2.4 MB (2404033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:91379332b152c897fc1da046a0abe2ca2dcd3f0a3323bd09a1e1b0682b2f917e`  
		Last Modified: Tue, 14 Jan 2025 03:25:22 GMT  
		Size: 11.7 KB (11684 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy` - windows version 10.0.20348.3091; amd64

```console
$ docker pull hylang@sha256:f751bcdc4bd69426932297ac0a08a1e787d5d6b72a6f6251605c461243302f2c
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2316000819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f635c54170f41b5bc7e68e51a7c0eb4acb7f4215b6e53e23c2da693fbbbecaf`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Tue, 14 Jan 2025 23:37:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:37:47 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:37:57 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:37:58 GMT
ENV PYPY_VERSION=7.3.17
# Tue, 14 Jan 2025 23:38:16 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.10-v7.3.17-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'cab794a03ddda26238c72942ea6f225612e0dc17c76cac6652da83a95024e6e8'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.10-v7.3.17-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:38:17 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 14 Jan 2025 23:38:17 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 14 Jan 2025 23:38:41 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:38:41 GMT
CMD ["pypy"]
# Wed, 15 Jan 2025 18:10:22 GMT
ENV HY_VERSION=1.0.0
# Wed, 15 Jan 2025 18:10:23 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 15 Jan 2025 18:11:16 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 15 Jan 2025 18:11:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:679cdfdfd4584aaa036b97cd5f84dd99a029c1521533bc2a51b70841c34af452`  
		Last Modified: Tue, 14 Jan 2025 23:38:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa6ffb09e1ad022204141133cd645a7a10165af4405985a49fbe163a10fff71f`  
		Last Modified: Tue, 14 Jan 2025 23:38:45 GMT  
		Size: 349.0 KB (348966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a820580ef5777d45d340f52895c07005d6c1e4e3cf834d0c39c4949bd3b5f13`  
		Last Modified: Tue, 14 Jan 2025 23:38:47 GMT  
		Size: 15.5 MB (15528516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e3cefb77381c55595a3d3ea13099b51dd219f4aac492d460b05ae26b66aeb24`  
		Last Modified: Tue, 14 Jan 2025 23:38:45 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df9ec63ac0a33a35417be39869ab1359c6253899d74c932578f81d196ef8945`  
		Last Modified: Tue, 14 Jan 2025 23:38:48 GMT  
		Size: 26.4 MB (26428431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:541cfdfdedef5e3ce53cc8f33bee1c9cd3a5a6336e9cf3d837ebbb04273fb4c9`  
		Last Modified: Tue, 14 Jan 2025 23:38:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5ad8641b3d3f68ab426266c5dd3b52d012a20a84fd4839bcf52b3d7d20ad80f`  
		Last Modified: Tue, 14 Jan 2025 23:38:44 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d754fe0482660af9e2c54a1878093af223551d043aeb87b5f1244aa151f9a912`  
		Last Modified: Tue, 14 Jan 2025 23:38:45 GMT  
		Size: 3.9 MB (3930348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233f49cf014ea45344d38e9f8538b22c4c63ec585f777434a8b5cf4726efb6c1`  
		Last Modified: Tue, 14 Jan 2025 23:38:44 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2f49f194e7e8f74c2cd3486473870e31326996442c1cd2762b06dc5923fb54f`  
		Last Modified: Wed, 15 Jan 2025 18:11:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f839ef876552178244fa5487d3adc405bbe375de50f73bf4ee6325b03deb71`  
		Last Modified: Wed, 15 Jan 2025 18:11:19 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1256fd8a295a8f7c3cbc220667841d63e869044615302d1e0b4416f9dc9e57d9`  
		Last Modified: Wed, 15 Jan 2025 18:11:20 GMT  
		Size: 7.4 MB (7368988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6c3a3067e3fc27cdb898e9aa81e4c9d59213684ef3a2e5957ffd49df025f35c`  
		Last Modified: Wed, 15 Jan 2025 18:11:19 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-pypy` - windows version 10.0.17763.6775; amd64

```console
$ docker pull hylang@sha256:be9cb9dce778196b86db6f9193ba99ff7d50d26b16e6e1f1b80283f25b26a881
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2175696202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:48869b7050afa42c647188508a21b03dab51db0b158ec7e397802e471057be35`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Tue, 14 Jan 2025 23:38:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Jan 2025 23:38:28 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:38:44 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:38:45 GMT
ENV PYPY_VERSION=7.3.17
# Tue, 14 Jan 2025 23:39:09 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.10-v7.3.17-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'cab794a03ddda26238c72942ea6f225612e0dc17c76cac6652da83a95024e6e8'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.10-v7.3.17-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:39:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 14 Jan 2025 23:39:11 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 14 Jan 2025 23:39:37 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 14 Jan 2025 23:39:38 GMT
CMD ["pypy"]
# Wed, 15 Jan 2025 18:05:44 GMT
ENV HY_VERSION=1.0.0
# Wed, 15 Jan 2025 18:05:45 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 15 Jan 2025 18:07:13 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 15 Jan 2025 18:07:13 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c47674fbe80c93a961e8e1d2f35f76651483d189585aeb0a65fc64996acbe40e`  
		Last Modified: Tue, 14 Jan 2025 23:39:46 GMT  
		Size: 1.4 KB (1390 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a11f809650e94b8c103ce484af82006f02f1bb305627fa02e72afdc1cd0f03d7`  
		Last Modified: Tue, 14 Jan 2025 23:39:45 GMT  
		Size: 329.8 KB (329819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:753f1c97b06fa9a5cd8ab1d315e8457823ab44adbf0eb5a628cacb1564c831ad`  
		Last Modified: Tue, 14 Jan 2025 23:39:46 GMT  
		Size: 15.5 MB (15501473 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7ce9a980ebfec3b0d491d63d775866c2fbbc405e1850834d570fccbcf3bd69`  
		Last Modified: Tue, 14 Jan 2025 23:39:45 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea57ee5984f5cc3c820dc1f86618d20509644ab16385c0f229fe217f255935b3`  
		Last Modified: Tue, 14 Jan 2025 23:39:47 GMT  
		Size: 26.4 MB (26445001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9901c9effc5b81fec33bc56e5f3d1b06c9dc3c9856953a35cb2ec7b0d961e7a`  
		Last Modified: Tue, 14 Jan 2025 23:39:43 GMT  
		Size: 1.4 KB (1372 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:854543b220a5509cd5fc412356a3502c85cfa27a0e07169ccf82a9dca6c82e43`  
		Last Modified: Tue, 14 Jan 2025 23:39:43 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf234c0b58c9ab751b844ea52ce5d96f928f2d2cb837e21cfaa4f7812b408e3e`  
		Last Modified: Tue, 14 Jan 2025 23:39:44 GMT  
		Size: 3.9 MB (3918471 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46a92bf9524b5ec6a7fd5a14cfaac2d3e4803c1216dd1a0e67c5560deb83066b`  
		Last Modified: Tue, 14 Jan 2025 23:39:43 GMT  
		Size: 1.4 KB (1395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5b88f43a05e799fa7925223cf61fd859b9030b95b4867bd4037764fc754237a`  
		Last Modified: Wed, 15 Jan 2025 18:07:16 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e24f939e28b160f5521820020301a640f832802ef2b20f790c9cc8922216750b`  
		Last Modified: Wed, 15 Jan 2025 18:07:16 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c425a31617555f344ca4525a1ddd2383eaf525d096f3136dc868be0b60c6898`  
		Last Modified: Wed, 15 Jan 2025 18:07:17 GMT  
		Size: 7.3 MB (7278500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:851ac1dd24ffa381c55d9c61830e34e6135053f162b0868cc7d8e5c3cbd35dc9`  
		Last Modified: Wed, 15 Jan 2025 18:07:16 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
