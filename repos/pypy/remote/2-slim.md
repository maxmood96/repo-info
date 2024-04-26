## `pypy:2-slim`

```console
$ docker pull pypy@sha256:b5c0152f957536a055c039103b1f45bb0007d87453f486e5f6f92b1080c4912a
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
$ docker pull pypy@sha256:a18e4b395753968f475e26cf3b76d1d0c71d3acd2da869742431269d34ed3f50
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65518539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:814f431d00cbead60422bf4308e3b38f67782c759faea30311e8fe4a5bdea41e`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 24 Apr 2024 03:28:31 GMT
ADD file:0e5a7771d5c0c58072db41fa02f288def8a40f2116b48e6127f1034f848bc2cd in / 
# Wed, 24 Apr 2024 03:28:32 GMT
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
	-	`sha256:6177a7f9989f56e11ac23856a0c014002800d83111aaa3e41fb2591161a166c2`  
		Last Modified: Wed, 24 Apr 2024 03:33:23 GMT  
		Size: 31.4 MB (31434263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e0cd56e25b420c756b7255f315a897229b0bd38f89e95dd59344395dbb14e11`  
		Last Modified: Thu, 25 Apr 2024 18:53:33 GMT  
		Size: 863.2 KB (863165 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:345445c83499d880f5391dff7a5993d42d3c4f7bb2e537be12df823e48669d5f`  
		Last Modified: Thu, 25 Apr 2024 18:53:33 GMT  
		Size: 31.3 MB (31266027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:23fe20de92c61f6385a9fcc45937fa95d8b1ed99aa45b34ff575684e269fb15d`  
		Last Modified: Thu, 25 Apr 2024 18:53:33 GMT  
		Size: 2.0 MB (1955084 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:78b5c6752982c53139a1fa5de15187936c3bf3d1a57b0d7a9b20d2c870b59a3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2668567 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd3605816bbafdf97d9972549277c3fc5786ef5fc6f14ddfeb9ff445f1006bcd`

```dockerfile
```

-	Layers:
	-	`sha256:3e87ae438b894911d466e812bd85b578fc084bf252ddfbac42340375694ba3ad`  
		Last Modified: Thu, 25 Apr 2024 18:53:33 GMT  
		Size: 2.6 MB (2643335 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9ed1af43ff109e5f712bff25d469d31d31e5dff1e5140a2e232b6c3bdc3a2339`  
		Last Modified: Thu, 25 Apr 2024 18:53:33 GMT  
		Size: 25.2 KB (25232 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:727a3d0ea7fd137d34ba752bacc69dbf1eb757450ff2db2a9bc830976ae4b7c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62144070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:279311f8a8e20a55620e4cd6821e3f0bb7bfa368611443f4cc25f389d61e35ca`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 24 Apr 2024 04:07:13 GMT
ADD file:e8990741de71fcc1884f30fcd1b6c5ea411bfa752419a82e9748fcd378ca100a in / 
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
	-	`sha256:40a322c395ab3df43e27d8be65cc48139c091588ac868643a02567ca247d0c73`  
		Last Modified: Wed, 24 Apr 2024 04:14:48 GMT  
		Size: 30.1 MB (30087336 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:92a9efc716e9e8ba45d8e98be87ce069f03d16d552ff4ea367e5583df61358e1`  
		Last Modified: Thu, 25 Apr 2024 14:39:16 GMT  
		Size: 850.5 KB (850517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1340723e78a3df9c2f73b5a890fcbefba0fe4d15b8e765048081a1c6a0ffab05`  
		Last Modified: Fri, 26 Apr 2024 08:59:13 GMT  
		Size: 29.3 MB (29251176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:122e72e69bc6cc9c0ade907479d1d57d4f05ca24951be1271945dc540a00ac02`  
		Last Modified: Fri, 26 Apr 2024 08:59:12 GMT  
		Size: 2.0 MB (1955041 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:b783c442be2d6de1ac9496e5d4ea74ee980274fd51c2817e96e255ab3cfa0891
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2668663 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b5c1c59db5242e3f5901fe5090822d55f4e2a1ac26d6bd388894d58cb8498bc`

```dockerfile
```

-	Layers:
	-	`sha256:b4da374f434a3ea6df95595e16b34e5e0d21f58864a49fcaa8e06a0d1835b64e`  
		Last Modified: Fri, 26 Apr 2024 08:59:12 GMT  
		Size: 2.6 MB (2643564 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c7b02d58f86b125b57c5b72faf13ae60e772ccc132ac5a8439c4dd32f71964c`  
		Last Modified: Fri, 26 Apr 2024 08:59:12 GMT  
		Size: 25.1 KB (25099 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim` - linux; 386

```console
$ docker pull pypy@sha256:d6574fa4107621c0d989d01f1488198721ed5b58b003f232db14aa417e752733
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (62020056 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d060d1f7ece111d6da941e933c0aeef4d7cbb0f37ac00327de76ade871491ba7`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 24 Apr 2024 03:39:20 GMT
ADD file:51089e94fd65259117206f5ee6b1fd709e8c1754176d4f625ae49abbee751047 in / 
# Wed, 24 Apr 2024 03:39:20 GMT
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
	-	`sha256:112c04b2ac24eb2c6dfef961130b9b3d298e6d4b8e125bbebaa1137d773f7d7d`  
		Last Modified: Wed, 24 Apr 2024 03:44:22 GMT  
		Size: 32.4 MB (32424773 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5230591782f18b833c1d1f58cca85549a051d7d512f43dbf1d3a413c33deea4b`  
		Last Modified: Thu, 25 Apr 2024 18:52:56 GMT  
		Size: 875.5 KB (875488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:86554fc47121c2586687c3aa566abd9ac812f730ef69c8944f6b7fefa38a4ea0`  
		Last Modified: Thu, 25 Apr 2024 18:52:57 GMT  
		Size: 26.8 MB (26764857 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca10d817ea48f0bd27066dc481c64cec1c1d414c9c581ed0d945260b10e51925`  
		Last Modified: Thu, 25 Apr 2024 18:52:57 GMT  
		Size: 2.0 MB (1954938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:93fa3c5e0d9c7bbf29e07a0be06fb835fe7414bc478b60cf49de87a3e65d8e39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2665545 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc1fb0f3993ac3bed356a7d6342b53f954eae5f1e86b9751811dd6fa392e95fa`

```dockerfile
```

-	Layers:
	-	`sha256:2973505f3b0f88d937c56f9f07fb69325f21acaaba208dd927a5b771677b8d3e`  
		Last Modified: Thu, 25 Apr 2024 18:52:57 GMT  
		Size: 2.6 MB (2640406 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d67223045cea1856dc6b219bc1de2e99ad226d6920ad595de1cce49703957aac`  
		Last Modified: Thu, 25 Apr 2024 18:52:56 GMT  
		Size: 25.1 KB (25139 bytes)  
		MIME: application/vnd.in-toto+json
