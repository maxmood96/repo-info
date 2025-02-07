## `pypy:3-7-slim`

```console
$ docker pull pypy@sha256:64e9b8edd114b76ce214fde29f722d4e786ff65556d8a26e85494171f75698ad
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:3-7-slim` - linux; amd64

```console
$ docker pull pypy@sha256:6b65a8785cf4aea82080fec3c1f99afcbfc43ed0574de9cfb53dab17ee70080a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.6 MB (65559307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:39923dd553fec69c2b67c81f79f36a10ee977375b37c0b7f0e1de1422358d1b3`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1738540800'
# Thu, 06 Feb 2025 11:12:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 11:12:33 GMT
ENV LANG=C.UTF-8
# Thu, 06 Feb 2025 11:12:33 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 11:12:33 GMT
ENV PYPY_VERSION=7.3.18
# Thu, 06 Feb 2025 11:12:33 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.18-linux64.tar.bz2'; 			sha256='834ccd4544bb47112a66977add7e47f30619f74061ae990876bcba95d98c27c5'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.18-aarch64.tar.bz2'; 			sha256='e843aecd48eb06b625af67891b99e3440313cfb64c6851fc37df1e5572c8ef9e'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.18-linux32.tar.bz2'; 			sha256='34ef09a481254aad0f22bf09fd7c99efb65ffef4f79f5b4222505f55f8d9c22e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Thu, 06 Feb 2025 11:12:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 06 Feb 2025 11:12:33 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 06 Feb 2025 11:12:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Thu, 06 Feb 2025 11:12:33 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:cf799a8da63a7bb7f377162d10ed737dd26b0e1174c8ac5d89a5da6c15dc7c04`  
		Last Modified: Tue, 04 Feb 2025 01:36:33 GMT  
		Size: 30.3 MB (30252588 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50dd95a8f021dfc8a6b4d3063a3e7c432d89d5c052ff8eafb6f0db38e7f850f5`  
		Last Modified: Fri, 07 Feb 2025 00:31:04 GMT  
		Size: 862.6 KB (862560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed396dc240ada8a04e1eefb93dffd6e05419c9f3425944445226a1dc6d791798`  
		Last Modified: Fri, 07 Feb 2025 00:31:04 GMT  
		Size: 31.1 MB (31137859 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7362ed838a26a4c0a55ccb0a336cb84032160119d53f1f52d78c4608734e3ea0`  
		Last Modified: Fri, 07 Feb 2025 00:31:04 GMT  
		Size: 3.3 MB (3306300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-7-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:2333d0f8eb96c968b9fddaf43c85bfa88497553193661a990f0636aec5be4169
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2723524 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3c6c083ef3ae22234a83eaeb2f7e700b2287c34d2f0468ef212946fd9856d76`

```dockerfile
```

-	Layers:
	-	`sha256:8debc345fd7aa7c55872f4067356ed8ad63323829d28268592c37f4a16d5e6d0`  
		Last Modified: Fri, 07 Feb 2025 00:31:04 GMT  
		Size: 2.7 MB (2695358 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ba7d6c4e5b35b74bbba8e522af260bba3d272441b0569a2578fb4c87022bdc49`  
		Last Modified: Fri, 07 Feb 2025 00:31:04 GMT  
		Size: 28.2 KB (28166 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:3-7-slim` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:7b4418dfcc74afe6a88f1d35c4fd8ba48ed86256d8a30bd7eb43ed7925ba7fbe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61808644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:989386c025c24dd56a3fca45cdffac9ca88c313f50206c82e95081ec569c79af`
-	Default Command: `["pypy3"]`

```dockerfile
# Wed, 28 Aug 2024 10:12:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1870371d89e1d2844b25b5a5bb5a41dba53d420ea2f0404f1ae18be4e7b4cb53`  
		Last Modified: Tue, 04 Feb 2025 12:13:25 GMT  
		Size: 849.8 KB (849790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9575dba7e837ca6a231ade14e678a5144319c8d6ecc97a97561735af2b4532`  
		Last Modified: Tue, 04 Feb 2025 12:13:26 GMT  
		Size: 28.9 MB (28907798 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93dff5e481989f65059e321f47fbdd35920d2fa6c9d1c6bbf1d545def5482691`  
		Last Modified: Tue, 04 Feb 2025 12:13:25 GMT  
		Size: 3.3 MB (3306246 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-7-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:fc62bdddaacddcfadfbb14e4f7f35af00f2767bd9dd95efd9892cd3e08633461
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2724227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:55a22ce43abd64e6c2f9d623d1a3046a76b5e10c979b2c23e5a2b90117d6ecd0`

```dockerfile
```

-	Layers:
	-	`sha256:c8f0b59033b85804a5d8c1ff4571f326517278e23339ccab0aee8a0008256a60`  
		Last Modified: Tue, 04 Feb 2025 12:13:25 GMT  
		Size: 2.7 MB (2695759 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:de23fc117bb520b3deabebfe87ee05cdea0363ba5e6278f68c2c70fcf6c9b700`  
		Last Modified: Tue, 04 Feb 2025 12:13:25 GMT  
		Size: 28.5 KB (28468 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:3-7-slim` - linux; 386

```console
$ docker pull pypy@sha256:58bd277802c3044358fa748f4015ea62b69af99d3f0a92587c88b2768fef59aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62941091 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b94fc251aa3c0ece491a12dcd0424073ebafd6fd5ccea288d27537ff2b7171`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 03 Feb 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1738540800'
# Thu, 06 Feb 2025 11:12:33 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 06 Feb 2025 11:12:33 GMT
ENV LANG=C.UTF-8
# Thu, 06 Feb 2025 11:12:33 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 06 Feb 2025 11:12:33 GMT
ENV PYPY_VERSION=7.3.18
# Thu, 06 Feb 2025 11:12:33 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.18-linux64.tar.bz2'; 			sha256='834ccd4544bb47112a66977add7e47f30619f74061ae990876bcba95d98c27c5'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.18-aarch64.tar.bz2'; 			sha256='e843aecd48eb06b625af67891b99e3440313cfb64c6851fc37df1e5572c8ef9e'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.18-linux32.tar.bz2'; 			sha256='34ef09a481254aad0f22bf09fd7c99efb65ffef4f79f5b4222505f55f8d9c22e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Thu, 06 Feb 2025 11:12:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 06 Feb 2025 11:12:33 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 06 Feb 2025 11:12:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Thu, 06 Feb 2025 11:12:33 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:af24a588b358e10d8284ac042756542ed964075987788d3d4a5fdbb6809e4de5`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 31.2 MB (31178875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:95f4cd30aaeb9876afb8a9d547e44bc23bb72d74975824870821d331956320d8`  
		Last Modified: Fri, 07 Feb 2025 00:30:21 GMT  
		Size: 874.7 KB (874672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcee03aad84951c811c60cd2ab302997b0a7c89fb7176f44664cc93e8c1a3aa2`  
		Last Modified: Fri, 07 Feb 2025 00:30:22 GMT  
		Size: 27.6 MB (27581436 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e84f8acd844b0b52ef658326478c5b9e519688de3d6977b18b0963ce2a75930`  
		Last Modified: Fri, 07 Feb 2025 00:30:21 GMT  
		Size: 3.3 MB (3306108 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-7-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:bfcc047a294a9203cb8896b94133f025c320c459f9c6f7afa5ad5c8608a18e5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2720474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:954178da6e4c0591c75309d879b06e74ab77c37028aae113367cc29995ffd5a1`

```dockerfile
```

-	Layers:
	-	`sha256:bdda47406540aa4d310c8be1e99817f65e634824dfb590f5fe1f7e3f17b198af`  
		Last Modified: Fri, 07 Feb 2025 00:30:22 GMT  
		Size: 2.7 MB (2692414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9369da7f70efd9d0d87be1ac90838d4cc751f9bd0da690aebaeb2b71a6b6852`  
		Last Modified: Fri, 07 Feb 2025 00:30:21 GMT  
		Size: 28.1 KB (28060 bytes)  
		MIME: application/vnd.in-toto+json
