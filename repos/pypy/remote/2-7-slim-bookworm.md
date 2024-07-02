## `pypy:2-7-slim-bookworm`

```console
$ docker pull pypy@sha256:394fb9936d3cd5287ec5227d7a33c4986410a5e998d96c80b290b11f2f2378be
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:2-7-slim-bookworm` - linux; amd64

```console
$ docker pull pypy@sha256:7e4e79cd40beb18bdd9761288db276f17ae09ccfe469aed7757e4ef8e22f6cab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.8 MB (65838977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44176153f7dbf8cee0c8080a8d49950086ba0df482685ad7828a3217b1b2b7b6`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:13 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
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
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aceb6360c50bd3d21e56cfbdb91890b0c276c14737a95661634e541088367f01`  
		Last Modified: Tue, 02 Jul 2024 03:25:11 GMT  
		Size: 3.5 MB (3495578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d7a8ffefd6ec08beac5f0b38340d38972fca17b9b8c0fe53331d6f3f0e72a13`  
		Last Modified: Tue, 02 Jul 2024 03:25:11 GMT  
		Size: 31.3 MB (31264222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a4f9797d77f8885ba0375fa7813e2f7552484c4bd62cc9716231857409e4a79`  
		Last Modified: Tue, 02 Jul 2024 03:25:11 GMT  
		Size: 2.0 MB (1952899 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:1d7081b017cdf1ae42877b778f307bf1edb7bc50d47f3d25fc5764d8e88b05d8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369559 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2f3fc08d54bf48cad736a56a15ef8dbef7079c7551aed1fa510ba987852e4ca`

```dockerfile
```

-	Layers:
	-	`sha256:a4d351fc63344ef75dda987cbf105ccad4235b7ad7d328cb5a6258ed8483ac31`  
		Last Modified: Tue, 02 Jul 2024 03:25:10 GMT  
		Size: 2.3 MB (2346862 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:88569e8674323d2af8376272324199c0089d69e14ef4cf2136536ad7085f631c`  
		Last Modified: Tue, 02 Jul 2024 03:25:10 GMT  
		Size: 22.7 KB (22697 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:048d5ca40d49cc1234602aa9e412012ef6cf66f32762f497a2480387971bf04d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63677028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:405ec73e516610fa0d28bffe213a7c3fc482a2ee39f2e8e4d70d229dc19dd21a`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:13 GMT
ADD file:cbda549b25cd4337cd3ce345e3b66c0d3b43c247d7315906a028f98a56c41f1d in / 
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
	-	`sha256:ea235d1ccf77ca07a545b448996766dc3eca4b971b04ba39d50af69660b25751`  
		Last Modified: Tue, 02 Jul 2024 00:42:25 GMT  
		Size: 29.2 MB (29156563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3221aa1086ff363670f0e30eece54e6e018e35e6439b8293b66073f84dbaeb5f`  
		Last Modified: Tue, 02 Jul 2024 19:44:26 GMT  
		Size: 3.3 MB (3318953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:734ba5dcc8e9d8dc7c774a70a7c294425c0dab600b2ed7ff4407411b6d1af0f7`  
		Last Modified: Tue, 02 Jul 2024 19:52:34 GMT  
		Size: 29.2 MB (29248775 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8021e00073fcbd7cd24cc14895d28622ec164f1868511b2d8b2e60b63f94602f`  
		Last Modified: Tue, 02 Jul 2024 19:52:31 GMT  
		Size: 2.0 MB (1952737 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:e30753fbf9a5b9814036d859c7ff5328ef534c68f48ad842ac3f8d2bb2064c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2370220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8f3aed4b5d85844a8d37e412140d69b1ca0c3d27ac4593f8f68fa0e12430e28`

```dockerfile
```

-	Layers:
	-	`sha256:5f16f1c7104c7958027ce28afc74c9606b4cc0d4e0e8c906cc09c7c55835a97c`  
		Last Modified: Tue, 02 Jul 2024 19:52:31 GMT  
		Size: 2.3 MB (2347166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d604a614a148f2f4b6f36a852cfdd813426b79072d55dcba0b7fd779655d6675`  
		Last Modified: Tue, 02 Jul 2024 19:52:31 GMT  
		Size: 23.1 KB (23054 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:80f4f726010fbc759f513bfaf1046b2f2cfa8152b93eaf703b847a8f22ce7b43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.4 MB (62359921 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:946afbe028b3f1580b1f7a0969a27f5277284c10a4ec829ec8630a9386a21cb4`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:13 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
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
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0f9b55485a6620fed30e9a9b018cf71fedf65694b7f4a3b725aa07d3e84fc6e`  
		Last Modified: Tue, 02 Jul 2024 03:25:01 GMT  
		Size: 3.5 MB (3500262 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65423ba8b06c93a1f9e07af67d437ec2f2f2ef642995170deed3386d6b23c094`  
		Last Modified: Tue, 02 Jul 2024 03:25:02 GMT  
		Size: 26.8 MB (26762897 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:73b0018af3b3cfe0af1451dd96f1a210a57b8c23571093a546243ee77313e641`  
		Last Modified: Tue, 02 Jul 2024 03:25:01 GMT  
		Size: 2.0 MB (1952487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:3101aae55b691385b04c7fe5d1077007950a6fad60a5bd16245319c151fa62cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51e4a47ee791874576a29371ac9f90a351bef9e69e294bbface301121280fea2`

```dockerfile
```

-	Layers:
	-	`sha256:52b0fc33fd473199512383568fb97e8ef4699cae59732e9228680fff33ccf661`  
		Last Modified: Tue, 02 Jul 2024 03:25:01 GMT  
		Size: 2.3 MB (2343984 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c23e303593bc9f46959b2b8f5a2a892e0971cee0a47aab0cf94701998eb24aef`  
		Last Modified: Tue, 02 Jul 2024 03:25:01 GMT  
		Size: 22.6 KB (22644 bytes)  
		MIME: application/vnd.in-toto+json
