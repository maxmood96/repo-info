## `pypy:2-7-slim-buster`

```console
$ docker pull pypy@sha256:de3cc67a4e0551910cbf544d8d3fe22f39cd2a5f8b7b7cedffe06d9d4c71f49f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `pypy:2-7-slim-buster` - linux; amd64

```console
$ docker pull pypy@sha256:89d5c5ac29da3499a5063956ee2c3451684419e9a4ff8edccffaa60c18067f8e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.2 MB (63216386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3d6eb4cb57d592e5c3d114010e2cbb27a62e49f20a39840707bef5392fa199a`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 21 Dec 2022 01:20:52 GMT
ADD file:660e0093a3da49e4ca41260d09d585754ccb1eff8974c4b0dd4456b76ddbbc9a in / 
# Wed, 21 Dec 2022 01:20:52 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 12:27:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 12:27:42 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 12:27:43 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 12:27:43 GMT
ENV PYPY_VERSION=7.3.10
# Wed, 21 Dec 2022 12:32:48 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.10-linux64.tar.bz2'; 			sha256='461fb6df524208af9e94ffb16989f628b585bdb4b9e97d81e668899fc3a064a3'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.10-aarch64.tar.bz2'; 			sha256='274342f0e75e99d60ba7a0cfb0e13792e7664163e01450d2f7f2f7825603a0ae'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.10-linux32.tar.bz2'; 			sha256='0b17132f62d2a0c3c4572c57eb53820f25611afad71f3d6a310202942baed6e1'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.10-s390x.tar.bz2'; 			sha256='0fac1ec1e05c70941f758be05d40ce7ffe6a42c0416e70b55d40a7523e3e70ae'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 21 Dec 2022 12:32:49 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 21 Dec 2022 12:32:49 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 21 Dec 2022 12:32:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 21 Dec 2022 12:32:58 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:b52ebda398ed2c4602ea06056f78d45a59474ee4e2a020967251ba082424e7e2`  
		Last Modified: Wed, 21 Dec 2022 01:25:17 GMT  
		Size: 27.1 MB (27140331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c53196de6ca370b219a4ecf8a674e83f11bbca627c09782ee4fe2dbafaa785fb`  
		Last Modified: Wed, 21 Dec 2022 12:36:24 GMT  
		Size: 2.8 MB (2768007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a4f8fe779388e3032fa47215e5792eaf25aa2eb28bb3c56eee4e9c1b038eeb`  
		Last Modified: Wed, 21 Dec 2022 12:39:57 GMT  
		Size: 31.1 MB (31138548 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a6a1a6b0249f53cef16c9081925451b1438c83ba4e9cc106e8ce619643c657`  
		Last Modified: Wed, 21 Dec 2022 12:39:52 GMT  
		Size: 2.2 MB (2169500 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-7-slim-buster` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:f4fb85080d51d65e8c731ce152ce828a9cf833eabb92b49af8cdafd255e3387d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.9 MB (59870358 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21dddce742b09ee9c59f7d6f8b35659aecec7ddd93d6b0c941b8e4191d404ba`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 21 Dec 2022 01:40:02 GMT
ADD file:51788132818f0e1cbed57cd022358b0564ec0d9cab6d33e5ef53902645d53c98 in / 
# Wed, 21 Dec 2022 01:40:02 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 08:20:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 08:20:58 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 08:20:58 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 08:20:58 GMT
ENV PYPY_VERSION=7.3.10
# Wed, 21 Dec 2022 08:25:25 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.10-linux64.tar.bz2'; 			sha256='461fb6df524208af9e94ffb16989f628b585bdb4b9e97d81e668899fc3a064a3'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.10-aarch64.tar.bz2'; 			sha256='274342f0e75e99d60ba7a0cfb0e13792e7664163e01450d2f7f2f7825603a0ae'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.10-linux32.tar.bz2'; 			sha256='0b17132f62d2a0c3c4572c57eb53820f25611afad71f3d6a310202942baed6e1'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.10-s390x.tar.bz2'; 			sha256='0fac1ec1e05c70941f758be05d40ce7ffe6a42c0416e70b55d40a7523e3e70ae'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 21 Dec 2022 08:25:25 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 21 Dec 2022 08:25:25 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 21 Dec 2022 08:25:33 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 21 Dec 2022 08:25:33 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:eb4ce5bba15e4b6fd353d7fc222fbe9c71d6881cefe1e10384c6c358d4b4eb90`  
		Last Modified: Wed, 21 Dec 2022 01:43:52 GMT  
		Size: 25.9 MB (25914906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ead31ef8ff29964d0407040c3aa08583f162b3e925e39a93c542326b1f9d6504`  
		Last Modified: Wed, 21 Dec 2022 08:29:08 GMT  
		Size: 2.6 MB (2636521 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022bb23bdc5c5a1c21b609cd8b0e89f8db4a982955e67431df53d2ac15a508a3`  
		Last Modified: Wed, 21 Dec 2022 08:32:25 GMT  
		Size: 29.1 MB (29149553 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2b593ef457f02a6221a3875cf0129390711a2cb26f35930a2aa41519f2e3269`  
		Last Modified: Wed, 21 Dec 2022 08:32:21 GMT  
		Size: 2.2 MB (2169378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-7-slim-buster` - linux; 386

```console
$ docker pull pypy@sha256:f714f646b2efd92cefa338438edede9f8c6b00f960fc7558640976ba8faad871
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.5 MB (59513517 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89076de96b051a318c0de6c06db863a94c8b594b00c77d76ab6cd5e2c864d116`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 21 Dec 2022 01:39:45 GMT
ADD file:48a2a0e6cb166df412bb4f6ad30537c66bc6be97ce4c8fc582fd5ac8c6129b5a in / 
# Wed, 21 Dec 2022 01:39:46 GMT
CMD ["bash"]
# Wed, 21 Dec 2022 06:24:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 21 Dec 2022 06:24:05 GMT
ENV LANG=C.UTF-8
# Wed, 21 Dec 2022 06:24:06 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 21 Dec 2022 06:24:07 GMT
ENV PYPY_VERSION=7.3.10
# Wed, 21 Dec 2022 06:28:19 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.10-linux64.tar.bz2'; 			sha256='461fb6df524208af9e94ffb16989f628b585bdb4b9e97d81e668899fc3a064a3'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.10-aarch64.tar.bz2'; 			sha256='274342f0e75e99d60ba7a0cfb0e13792e7664163e01450d2f7f2f7825603a0ae'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.10-linux32.tar.bz2'; 			sha256='0b17132f62d2a0c3c4572c57eb53820f25611afad71f3d6a310202942baed6e1'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.10-s390x.tar.bz2'; 			sha256='0fac1ec1e05c70941f758be05d40ce7ffe6a42c0416e70b55d40a7523e3e70ae'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 21 Dec 2022 06:28:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 21 Dec 2022 06:28:20 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 21 Dec 2022 06:28:31 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 21 Dec 2022 06:28:32 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:9099d8a02dc0a7901931d2811fa3078b18ecd3a40a156cbcfd91629126463f80`  
		Last Modified: Wed, 21 Dec 2022 01:45:34 GMT  
		Size: 27.8 MB (27798412 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede92b78a95bb9625d9dc015b50cc60c777da2aa8eb240f5148ea5f8ff307148`  
		Last Modified: Wed, 21 Dec 2022 06:33:32 GMT  
		Size: 2.8 MB (2781006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00e504136f622238cd6bef9cf05c1062185b12b27683f819d89f4d731d763c69`  
		Last Modified: Wed, 21 Dec 2022 06:36:13 GMT  
		Size: 27.0 MB (26978836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6208865851d2ff5db23565c66755b1f3d7180b77aa3a7d9b056ebaa4c412abf4`  
		Last Modified: Wed, 21 Dec 2022 06:36:09 GMT  
		Size: 2.0 MB (1955263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
