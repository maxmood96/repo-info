## `pypy:2-slim-bookworm`

```console
$ docker pull pypy@sha256:98877c0459f5c630a1f4fd911f2cbd474623230dd95a9453e0f0361b2bfb49ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:2-slim-bookworm` - linux; amd64

```console
$ docker pull pypy@sha256:971003c07c734db0edbd05a61715b32a0c6c60cd7e3f59fdb6f179a6678a2afa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65666820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c9203e952e35bd432d87c55b3756dfb0aaf2c6e5e244ad9d87a46aad2cc4852b`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:13 GMT
ADD file:5aaace706aa00ff97d243daa2c29f5de88f124e1b97c570634f16eef90783286 in / 
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
	-	`sha256:09f376ebb190216b0459f470e71bec7b5dfa611d66bf008492b40dcc5f1d8eae`  
		Last Modified: Tue, 14 May 2024 01:32:30 GMT  
		Size: 29.2 MB (29150411 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c757f7484cbef35e83647dbace1f8a7016b80942579e189c050f2171f737f69a`  
		Last Modified: Tue, 14 May 2024 02:57:46 GMT  
		Size: 3.3 MB (3299417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ad69c80308a8dfb0bc849af4db2c7aa29700e9f9e183eb58a2db61566a33e4b`  
		Last Modified: Tue, 14 May 2024 02:57:47 GMT  
		Size: 31.3 MB (31264155 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51808b1be4561896da24b043c2ff65a4e172e131556d23ca50d9e534e371bf7b`  
		Last Modified: Tue, 14 May 2024 02:57:46 GMT  
		Size: 2.0 MB (1952837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:735f641b9316495c7689b8b4e7f2e0be4dd423cc49ee0e88bf528f9680d79daf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1586caf1dbb608ac9f6f4d2c7078927f0e76d7494566c4f7e9b68d466a668482`

```dockerfile
```

-	Layers:
	-	`sha256:62f5beff8860b7cb57925414a62beca45032af9cefc2b351ae1b2fb46df9746d`  
		Last Modified: Tue, 14 May 2024 02:57:46 GMT  
		Size: 2.3 MB (2346834 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:463bfac21ed56c067d9d1480a3d1bdef7f27faccb76d7b54602096510178f905`  
		Last Modified: Tue, 14 May 2024 02:57:46 GMT  
		Size: 22.8 KB (22815 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:2a034eb4e97690f9f97fbe9427095b4689b11df71b98ad09c657d50c1c5c8923
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.5 MB (63503626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1b5e44e4bd067f409aca8d441e1a8df42cce10709ecdd1a0305b4bb5e536c6d7`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:13 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
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
	-	`sha256:22d97f6a5d13532e867231d23d92620a81874d51a456196be50154eeb32edc08`  
		Last Modified: Wed, 24 Apr 2024 04:14:07 GMT  
		Size: 29.2 MB (29179935 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:938dda567ea646b790d5aadf33cfc7b14e0c3c94fae3e50ca27d60677e8455f3`  
		Last Modified: Thu, 25 Apr 2024 14:36:59 GMT  
		Size: 3.1 MB (3122199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f6339592f301ab19fc0385c718cf989d44329ee913c08452ee8b136559caf34`  
		Last Modified: Fri, 26 Apr 2024 08:57:37 GMT  
		Size: 29.2 MB (29248736 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e9dab80df11eae447c1c708f62f6ac843c9441798b4a41495b6711b8d8c95e6`  
		Last Modified: Fri, 26 Apr 2024 08:57:37 GMT  
		Size: 2.0 MB (1952756 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:77334f972cf99ab2240fb00723d0fa16038be78d0c78f901cb19b5be09cb70dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad579acbdf4ad36f2b98bc57deffa4690af258f29ffb3e92a4845b1d8ad623af`

```dockerfile
```

-	Layers:
	-	`sha256:5f25b979ba7ae6ca6bc346ee992a77ebc24c0887a558ee0f2f54f28f12ed7319`  
		Last Modified: Fri, 26 Apr 2024 08:57:37 GMT  
		Size: 2.3 MB (2347053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8b844476f5cb138baa3b430c016ef4976167b6798a2b7ebbdff7860dc05fc319`  
		Last Modified: Fri, 26 Apr 2024 08:57:36 GMT  
		Size: 22.7 KB (22665 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:3584058f80d7a31335e2062be617ccf95b46fc563556586ed685a86fd3c900b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62183121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38888bce405fcf7f0d891700a55d79384f4ab4541b857e4ff40579f105f1f04`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:13 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
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
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00201f11173b169f0523d7514f4860dd0e1511ed981380dd226f761ab8649ebc`  
		Last Modified: Tue, 14 May 2024 01:55:13 GMT  
		Size: 3.3 MB (3304893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b23daad660f50d9dc65f4b0c75e70e8b39a971f3a1481cc29585876fb56b3e7b`  
		Last Modified: Tue, 14 May 2024 01:55:13 GMT  
		Size: 26.8 MB (26762971 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec8d48fd545468b594dd21938ce4c1339b4e936e3224f1ce21642450db6b551`  
		Last Modified: Tue, 14 May 2024 01:55:13 GMT  
		Size: 2.0 MB (1952619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:cb5d4268b13cc8bb90cc537f9e68d86297e4c69844e69169aac9c8282308e9ab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f64e8057034b68bd22f3b8b94ff01a63ae7650fccf534ed3c311e4fc0905e6fc`

```dockerfile
```

-	Layers:
	-	`sha256:9e99a22eb7ece589781353faf3ca2a79515046e83efea8c24c4f598d3e99418f`  
		Last Modified: Tue, 14 May 2024 01:55:13 GMT  
		Size: 2.3 MB (2343956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:396807ea9535e9aeeef5a58909a2f9684a68fb844ecf068616596e8bc44faa01`  
		Last Modified: Tue, 14 May 2024 01:55:12 GMT  
		Size: 22.8 KB (22762 bytes)  
		MIME: application/vnd.in-toto+json
