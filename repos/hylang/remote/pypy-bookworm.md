## `hylang:pypy-bookworm`

```console
$ docker pull hylang@sha256:4c0f07420e95de0be6978c8a99c3646211a299194627a342b8088e213ca4524b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:pypy-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:d3993012c28a36c18813244ef56c2b7ab63eb372216b71a57af3fb5998161571
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71794348 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:502738af64042969b4d11fbc25d0508c69c6b7fe27c8fe8ece1b4e1a49c237ed`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Aug 2024 10:12:01 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:fd674058ff8f8cfa7fb8a20c006fc0128541cbbad7f7f7f28df570d08f9e4d92`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 28.2 MB (28231581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2f39a722ac233389c408844280c4dba18a22b295208a31691d7e9dd586313c`  
		Last Modified: Tue, 24 Dec 2024 22:33:54 GMT  
		Size: 3.3 MB (3306406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc6508fd7d90531e9b719df8c7abb8021ea442abc447bfdaecf142b55d0a5b64`  
		Last Modified: Tue, 24 Dec 2024 22:33:54 GMT  
		Size: 30.6 MB (30592912 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:44b35a5575b36ec08c973bef24a85f97ae4374938875f9bb4e82b9ff593a698c`  
		Last Modified: Tue, 24 Dec 2024 22:33:54 GMT  
		Size: 3.3 MB (3305440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bdae52f36d7aa27ea9788becfbd01efa717036af9de6168d0eb59676b4009144`  
		Last Modified: Thu, 09 Jan 2025 22:31:13 GMT  
		Size: 6.4 MB (6358009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:80ef22ea8cb9737b83c9ac4d8788a439a6220aec0c7c84a5b307c2a851d567b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2418732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d4b4bca144693693584d970706489c6c7be7cd64c997c5e53542369737e17a8`

```dockerfile
```

-	Layers:
	-	`sha256:14b693c2cf7ca18ede59ad3ab65e3ce3892e68a5e5e2601944018e7dbb2f3b9e`  
		Last Modified: Thu, 09 Jan 2025 22:31:13 GMT  
		Size: 2.4 MB (2406956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b0adeac24838429b34d6263c6a38a6d1a3eb29d5706c5c0ca4f356f2a42ebf98`  
		Last Modified: Thu, 09 Jan 2025 22:31:13 GMT  
		Size: 11.8 KB (11776 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:2830564f986cdfa92e7a31e43b464bf6aee360d27f69126f1f8d091e036c3777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69799433 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82c12f659641a7b6687db2fb84fe44d4470f1192f6ad86a5db5bebcfad7ba0dc`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Aug 2024 10:12:01 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1734912000'
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
	-	`sha256:f5c6876bb3d7d368455916fa98c705330bd8a8d9c080ccea8fe4c4b35a2ecb1f`  
		Last Modified: Tue, 24 Dec 2024 21:34:20 GMT  
		Size: 28.1 MB (28058723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:64cec2f141f94f6bf9839b9855f0bae5a0ecf49c9664c27959507d2f162a794a`  
		Last Modified: Wed, 25 Dec 2024 04:00:43 GMT  
		Size: 3.1 MB (3129819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:491f5bcabd41da21225b78d6f629fc136652fa5eafbcbc1bc0127b57acbec7f0`  
		Last Modified: Wed, 25 Dec 2024 04:00:43 GMT  
		Size: 28.9 MB (28947239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25815b8f0b9982413af3b9f188517988a95dae881c33d9e64a4bce6a6650d1c4`  
		Last Modified: Wed, 25 Dec 2024 04:00:43 GMT  
		Size: 3.3 MB (3305534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2063201f3073e98adcdce072c9ab4bb856a9e50d403651a2dddbf44729502fda`  
		Last Modified: Thu, 09 Jan 2025 22:56:42 GMT  
		Size: 6.4 MB (6358118 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:fa7dd4ba63289fe3028b305d725b21137472066741260f13a281898ffd7f2bc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2419384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:134de9438c7175921448b93b33206c47cee4912baf095205df7580f72c0dd296`

```dockerfile
```

-	Layers:
	-	`sha256:eb21fa2cbf47c5a638f77492b664dc00077fa2c22fba25b24ae96b99061e642b`  
		Last Modified: Thu, 09 Jan 2025 22:56:42 GMT  
		Size: 2.4 MB (2407359 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0585e43b0da829dcc36a9422dbc28b8ab2800e3f57d5e2f548e7f7fed1aa7f0c`  
		Last Modified: Thu, 09 Jan 2025 22:56:42 GMT  
		Size: 12.0 KB (12025 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:2f010c72fab1e3d6238d62d94b76a7fa15c7601305ca907d6f36d3b9d37a4a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69122440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1158ce5764bac0cea677a935aa852945d85125691ae7c889e94b49ef308ea52d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 28 Aug 2024 10:12:01 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1734912000'
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
	-	`sha256:fba9c0797a7b5bba079e0fd9d815a8878aea58430ea12c84047010f98fbe34d7`  
		Last Modified: Tue, 24 Dec 2024 21:32:20 GMT  
		Size: 29.2 MB (29205387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:54da50edab8e1ae217fbbfdf92110368f2923d0a23ed8232c88fc831a2f70344`  
		Last Modified: Tue, 24 Dec 2024 22:28:42 GMT  
		Size: 3.3 MB (3309240 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ebfb6e2f1928adf4332075a35c6516ca6ad7be70c3081a8c20b67e35ea1a3203`  
		Last Modified: Tue, 24 Dec 2024 22:28:43 GMT  
		Size: 26.9 MB (26944275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd7df073fb78754bda561dc80022b34cb50dd57c002c6642962642d66c161e2f`  
		Last Modified: Tue, 24 Dec 2024 22:28:42 GMT  
		Size: 3.3 MB (3305131 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e42cce09d932a97f68b0df2f5231824457603675a75390058a639200b43fbaad`  
		Last Modified: Thu, 09 Jan 2025 22:30:58 GMT  
		Size: 6.4 MB (6358407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:3739acfd0fbacfbfd019d2d9c5ddedad30eb7ff4aa6de4efe37cb86df79677bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2c76c52adf9e338986fec9cfae0420eeb3743d5acfa68da744510de8dadee08`

```dockerfile
```

-	Layers:
	-	`sha256:47a74683ae2bb1f13ddd771ebe0dc1a670f6bfe11710544165475d1fba98a73a`  
		Last Modified: Thu, 09 Jan 2025 22:30:58 GMT  
		Size: 2.4 MB (2404033 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4221a284808dff4f4ecf15554da60685e0be1c981d18cb94fd59bfcb2b99923`  
		Last Modified: Thu, 09 Jan 2025 22:30:57 GMT  
		Size: 11.7 KB (11685 bytes)  
		MIME: application/vnd.in-toto+json
