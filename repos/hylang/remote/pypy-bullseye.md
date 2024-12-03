## `hylang:pypy-bullseye`

```console
$ docker pull hylang@sha256:272b1a84d9673819c3bf1696d8c424c06580394ac7f51be14d61122c1939452b
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
$ docker pull hylang@sha256:c335ae70ad731b0600d242eb065d23a9efa8eb662131dc4e5019b08692c91d23
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71323813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a3fbe9b3bd2b0003f62f6adbcab418adda5b43c20fb14f3e79e9ea0018a74e`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Aug 2024 10:12:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1733097600'
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
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:69fb10dc82f9580a647bd4638e741b2338cb8e2575d2be6f0bacfcada936a617`  
		Last Modified: Tue, 03 Dec 2024 01:27:21 GMT  
		Size: 30.3 MB (30252644 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f17ba5fff7d034c83cb7f7c83602401b786b2141ef7e6f798148a52168e76fb7`  
		Last Modified: Tue, 03 Dec 2024 02:16:31 GMT  
		Size: 862.6 KB (862557 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d1c6ee3680b5d894af34cdaac78f1613cce0ca30913456d5ee5e2f60441b2738`  
		Last Modified: Tue, 03 Dec 2024 02:16:32 GMT  
		Size: 30.5 MB (30544362 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a06035bd0c7a15b7c11217c50894318a1b35f4cb3fb51d113a2b31f6d27e9d44`  
		Last Modified: Tue, 03 Dec 2024 02:16:31 GMT  
		Size: 3.3 MB (3306383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4669c42665c9c149ea3ffe15453ddd62361fdcec1faf2559b30f6926ee775b8`  
		Last Modified: Tue, 03 Dec 2024 03:27:07 GMT  
		Size: 6.4 MB (6357867 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:8f47e7e462d0f558e7bc49c7aac7451a0b6e7be73d8d7058501f8cf1de76f6fc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2711750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bea52249f008d534ea4128dce111eba97cd67bf6ecac0d0d2d8f1eb4495fbee3`

```dockerfile
```

-	Layers:
	-	`sha256:7acc0747cb0ce8f420482f46cd4602725e9013686cc6b01089310b368b14dd7d`  
		Last Modified: Tue, 03 Dec 2024 03:27:07 GMT  
		Size: 2.7 MB (2702407 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d9706120a29220d662898082757b71db3d66960527dafdfc4f5427d115eb124e`  
		Last Modified: Tue, 03 Dec 2024 03:27:06 GMT  
		Size: 9.3 KB (9343 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:410404bd698665310964f54c180e2eb9c579f24defeae415fa952ae993856de0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.2 MB (68166751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f64368f52aa28a8379185da9fb787e74478e9eb1c8e5677ad2b5c195596cf8`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Aug 2024 10:12:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1733097600'
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
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8861e715dd4ae7d0bd8da39ea24d5c695bc09f0f4e43ca5221686621a10cd31b`  
		Last Modified: Tue, 03 Dec 2024 01:30:38 GMT  
		Size: 28.7 MB (28744923 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:176045cbab2937edbb0f06f393d442b96d2247cbf6e88c303f115274d926dcfc`  
		Last Modified: Tue, 03 Dec 2024 07:58:29 GMT  
		Size: 849.8 KB (849769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:47653e8bc2f8b1d2e9170e510fb7a59cdc7c0c7465be34ea3f1461cc8566bba7`  
		Last Modified: Tue, 03 Dec 2024 07:58:30 GMT  
		Size: 28.9 MB (28907760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5a61722f986acf615fc8d4e178f8b8fb11fece5e6bb079a4d7737f5b803f51d`  
		Last Modified: Tue, 03 Dec 2024 07:58:29 GMT  
		Size: 3.3 MB (3306206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6038c4f86de089d6279ed2d88c31980f9b4a1152aa5b838dfb6b2b38508d1e5b`  
		Last Modified: Tue, 03 Dec 2024 16:08:06 GMT  
		Size: 6.4 MB (6358093 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:683f554c87f47fb704c6d560ffabedeb85df9acada75302633df18f79e583f7b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2712201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e08a0626a39ff5dddbed0bbb96f133be01c576952b3077ceab8d35b1582a3cb`

```dockerfile
```

-	Layers:
	-	`sha256:b171adffcd89b7691913d2b7095c79d3c3b64ea5369c4134d85eeb712002d9ae`  
		Last Modified: Tue, 03 Dec 2024 16:08:05 GMT  
		Size: 2.7 MB (2702707 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:99a6e6605d8740363991158715e95b7ee10f00557a44c5522c5be1cb09f21767`  
		Last Modified: Tue, 03 Dec 2024 16:08:05 GMT  
		Size: 9.5 KB (9494 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:68a15f758181122a75e6cad9615e0081c34cbd227a23d6fdf62b748188f18757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68579795 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee15288443ae64fe5fb1f4e13420110d2bbc72e68637900bbc56555ec9617ead`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Aug 2024 10:12:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1733097600'
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
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HY_VERSION=1.0.0
# Tue, 08 Oct 2024 19:58:40 GMT
ENV HYRULE_VERSION=0.7.0
# Tue, 08 Oct 2024 19:58:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Oct 2024 19:58:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c321449a7780a0f6febb0c1425384629e366cd30dd2d0d9cab29fc6e33f6955c`  
		Last Modified: Tue, 03 Dec 2024 01:27:12 GMT  
		Size: 31.2 MB (31179058 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:696ba405fda8cd3cce8cc74be11903e0704fca28d75cf304bf62dade9cea7654`  
		Last Modified: Tue, 03 Dec 2024 02:30:14 GMT  
		Size: 874.7 KB (874690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b44d6dcd2a16808e36d390167d60761cb47cab442ea0f4131d12c5fe702b2cb`  
		Last Modified: Tue, 03 Dec 2024 02:30:15 GMT  
		Size: 26.9 MB (26862092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f470fb41003391213ccee2d7a44e921268869e5ec652f1b694e6f6add06c973`  
		Last Modified: Tue, 03 Dec 2024 02:30:15 GMT  
		Size: 3.3 MB (3305992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5978fe3fc51a7b625d803245414de4a01ae24ba1d5ebcb2affeba2fd3d4b8d1`  
		Last Modified: Tue, 03 Dec 2024 03:24:00 GMT  
		Size: 6.4 MB (6357963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:44ed5b3169b338fee802a73b9d96bd744ba2cf6ff029b32fc83b04ac557b12fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2708803 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea605e3a41bb2f0ead7b6ae5d6362512300089a46300d94eb76ffaf9c9a21b8`

```dockerfile
```

-	Layers:
	-	`sha256:7ab34481a4c9993c3ce30734e5f71adc3dd734ad1c662237e8af9c21855460da`  
		Last Modified: Tue, 03 Dec 2024 03:23:59 GMT  
		Size: 2.7 MB (2699512 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5b88c61e51d9060a98ebeb177bc8facd6aac2aaeca6831691916c00cd87b3b2c`  
		Last Modified: Tue, 03 Dec 2024 03:23:59 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json
