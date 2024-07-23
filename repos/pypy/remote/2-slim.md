## `pypy:2-slim`

```console
$ docker pull pypy@sha256:eaf3e2af47adfcfadbf2fe844cf0a074e454594c861bb9e7f15ccb2b1bafc437
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:2-slim` - linux; amd64

```console
$ docker pull pypy@sha256:deb18cede3d9fe6a57926d93b4d6ee3106826a421b43eebe4f5044fcc4d1ed32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65715923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52a75af7de22aedd507aa6950a207c2c068c0a4e57b4a0a5ba6f90f0ee477a3`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:13 GMT
ADD file:258da966e49fd81eb3befac4ebcc023feb92794e891d5c9ca9b61084c7a209d5 in / 
# Wed, 24 Apr 2024 04:07:13 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:07:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 04:07:13 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PYPY_VERSION=7.3.16
# Wed, 24 Apr 2024 04:07:13 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-linux64.tar.bz2'; 			sha256='04b2fceb712d6f811274825b8a471ee392d3d1b53afc83eb3f42439ce00d8e07'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-aarch64.tar.bz2'; 			sha256='be44e65dd8c00d2388b2580dbe2af6a5179f951a8f4979efc74360f92f3c7e96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-linux32.tar.bz2'; 			sha256='a19712d7a6bd4f6d113e352c5271803c583b5129b76a357d387b1fa85204f8e5'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-s390x.tar.bz2'; 			sha256='09eb70b932e6aac484cf4b5f2de5845f71589f2cbb53e5ed37a497613b43cd53'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 24 Apr 2024 04:07:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 24 Apr 2024 04:07:13 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:5de87e84afeec60e41fb003112c283b04a73e50c8d579c88bd21d668fd688485`  
		Last Modified: Tue, 23 Jul 2024 05:28:31 GMT  
		Size: 31.4 MB (31428330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ca80578ea1522cfbeadd006c4408af94cc9ea5e0b97121debb28f0535f484b3`  
		Last Modified: Tue, 23 Jul 2024 07:15:52 GMT  
		Size: 1.1 MB (1066591 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:461f155721a0b2561246bc370673e5f9d40a2908d89fc8fe7b1c6e36744ba036`  
		Last Modified: Tue, 23 Jul 2024 07:15:53 GMT  
		Size: 31.3 MB (31265931 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c86549986ee0767e5a5457343b9130a60ef18191c42b0cc1eaa864d4186470fb`  
		Last Modified: Tue, 23 Jul 2024 07:15:52 GMT  
		Size: 2.0 MB (1955071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:e753d275b889f9f318656d7ba41fe39708cd57b9c601bc09217c0de19e5c9707
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2689852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eda9ff41159cf6cfa52bae6aeb92237da29cb4e7cf452154f0cdd026dbb96d38`

```dockerfile
```

-	Layers:
	-	`sha256:642f16d9411ac364f7d351f592a4966d5c48793f326c1ebea1ab10b3e3400e89`  
		Last Modified: Tue, 23 Jul 2024 07:15:52 GMT  
		Size: 2.7 MB (2664735 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1f7c3f2d6ab7701b0f782b2c3205ca39dcbd7bb045be8e7343bf0855e80772ff`  
		Last Modified: Tue, 23 Jul 2024 07:15:52 GMT  
		Size: 25.1 KB (25117 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:a14becf0ef6d3c081a11d22a24df041d1c2c7e468614a6d581d9c56ebaad84be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62329695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d63b91867bf31215bb5f03557793020bab365b800ff873af83f04bbbdac0df35`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:13 GMT
ADD file:17d80cdc7d7b37786a32ac4e261c7d17cd4d80248ae39f9574ab5a6bf6a2707c in / 
# Wed, 24 Apr 2024 04:07:13 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:07:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 04:07:13 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PYPY_VERSION=7.3.16
# Wed, 24 Apr 2024 04:07:13 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-linux64.tar.bz2'; 			sha256='04b2fceb712d6f811274825b8a471ee392d3d1b53afc83eb3f42439ce00d8e07'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-aarch64.tar.bz2'; 			sha256='be44e65dd8c00d2388b2580dbe2af6a5179f951a8f4979efc74360f92f3c7e96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-linux32.tar.bz2'; 			sha256='a19712d7a6bd4f6d113e352c5271803c583b5129b76a357d387b1fa85204f8e5'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-s390x.tar.bz2'; 			sha256='09eb70b932e6aac484cf4b5f2de5845f71589f2cbb53e5ed37a497613b43cd53'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 24 Apr 2024 04:07:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 24 Apr 2024 04:07:13 GMT
CMD ["pypy"]
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
	-	`sha256:2ce5452df35dc0dbe29d3f03c1f5f4f04009f699d643012102adf9aa270f0a65`  
		Last Modified: Tue, 02 Jul 2024 19:54:10 GMT  
		Size: 29.3 MB (29251161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbb3bed864f7c019bf52ae0ba967270e76cd5f4a873b0868b6e0f7b5b481e6fa`  
		Last Modified: Tue, 02 Jul 2024 19:54:09 GMT  
		Size: 2.0 MB (1955011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:1c9a1ebf67b216d9b556d8e6d49adcec63dc398c3f689d0ea0d24e36b3d2fd36
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2669307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e301972d0bb0f3ef9be1465c7941ef0459beb4972be4bbd9fd0b55d65c40c987`

```dockerfile
```

-	Layers:
	-	`sha256:72c246add9c967f914509de52372054511de29b7eaafd7ef038a353295e2e98e`  
		Last Modified: Tue, 02 Jul 2024 19:54:09 GMT  
		Size: 2.6 MB (2643737 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b226659e720253d16bc03ad4d351da6777be99f08260c722dee9d5f7dd3241a9`  
		Last Modified: Tue, 02 Jul 2024 19:54:09 GMT  
		Size: 25.6 KB (25570 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim` - linux; 386

```console
$ docker pull pypy@sha256:0d9c2a6a7a58d5c9a7fb558d722f2a2325d3651660ec928456e14f0ebf7c31e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62212703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e066c6b2154ad83d29333957891d4d35ef3a1f5684bcdf4f04f65b11d4338826`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:13 GMT
ADD file:619dea132b057660136807b341227cbc3c7c9661313584d2fc0338130dc32f3e in / 
# Wed, 24 Apr 2024 04:07:13 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:07:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 04:07:13 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PYPY_VERSION=7.3.16
# Wed, 24 Apr 2024 04:07:13 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-linux64.tar.bz2'; 			sha256='04b2fceb712d6f811274825b8a471ee392d3d1b53afc83eb3f42439ce00d8e07'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-aarch64.tar.bz2'; 			sha256='be44e65dd8c00d2388b2580dbe2af6a5179f951a8f4979efc74360f92f3c7e96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-linux32.tar.bz2'; 			sha256='a19712d7a6bd4f6d113e352c5271803c583b5129b76a357d387b1fa85204f8e5'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.16-s390x.tar.bz2'; 			sha256='09eb70b932e6aac484cf4b5f2de5845f71589f2cbb53e5ed37a497613b43cd53'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 24 Apr 2024 04:07:13 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 24 Apr 2024 04:07:13 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 24 Apr 2024 04:07:13 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:6b5c41ccfba7fdb5c6183fbfde2e04bffba42b8f1f65b46c6b641ecf9c032ab5`  
		Last Modified: Tue, 23 Jul 2024 03:58:33 GMT  
		Size: 32.4 MB (32413808 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4912081f336596f18ecc39af8c778b1452cd28258cb4e90721f00ad2c115cb86`  
		Last Modified: Tue, 23 Jul 2024 06:10:51 GMT  
		Size: 1.1 MB (1079142 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f69ade4144e7daef2d400531c944ca3e32ce5b3002f66f44e8c4a59d15276413`  
		Last Modified: Tue, 23 Jul 2024 06:10:52 GMT  
		Size: 26.8 MB (26764819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:820bff7824df185c6dd063c784966c6c3d0c80580d4d3669a4b1810b0ea13bc2`  
		Last Modified: Tue, 23 Jul 2024 06:10:51 GMT  
		Size: 2.0 MB (1954934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:e680bcb46e8de258f398ff81e74393e870ca5a5294c647bc7c455d00ba884c1e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2686830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2fcd32bda34b4a35a3b822955f8af239b9a05bd9e54cc9466b0e060626f72dfc`

```dockerfile
```

-	Layers:
	-	`sha256:6cdc882097d4ea176cad8a9772e5b069b923c484ef8066de034303e4a8a06474`  
		Last Modified: Tue, 23 Jul 2024 06:10:51 GMT  
		Size: 2.7 MB (2661806 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1d07e98916b82bb28b385bbe1d787a8d5645471c41954c6b863ed89aee3fadc`  
		Last Modified: Tue, 23 Jul 2024 06:10:51 GMT  
		Size: 25.0 KB (25024 bytes)  
		MIME: application/vnd.in-toto+json
