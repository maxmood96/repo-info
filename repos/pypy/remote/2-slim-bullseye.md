## `pypy:2-slim-bullseye`

```console
$ docker pull pypy@sha256:29dcbc5d5bbc5390fb31f19bb2e937664649cf29b6ce09080ab884e32f14b954
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:2-slim-bullseye` - linux; amd64

```console
$ docker pull pypy@sha256:08558def841e3ac794e2b2766c18a71a1b90e2f2b03353f25a8669387d530651
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65695891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b48c00cfbc26568332fe43fb0ae41b2a69651d0976560083c25ca45a1a41eda6`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 15 Jan 2024 17:07:12 GMT
ADD file:40ad95eaf61b2797e8d2282bc2388bce34c3c24ed78e694695a8c3dbcd3ddbbb in / 
# Mon, 15 Jan 2024 17:07:12 GMT
CMD ["bash"]
# Mon, 15 Jan 2024 17:07:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jan 2024 17:07:12 GMT
ENV LANG=C.UTF-8
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PYPY_VERSION=7.3.15
# Mon, 15 Jan 2024 17:07:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-linux64.tar.bz2'; 			sha256='e857553bdc4f25ba9670a5c173a057a9ff71262d5c5da73a6ddef9d7dc5d4f5e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-aarch64.tar.bz2'; 			sha256='31b41fca7280636d7818713b7a0fab8f34ece9c82cc88e51d305d43b3e6306d6'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-linux32.tar.bz2'; 			sha256='cb5c1da62a8ca31050173c4f6f537bc3ff316026895e5f1897b9bb526babae79'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-s390x.tar.bz2'; 			sha256='eb442279ec3f1eb17da296e38b531d3ca50c6418eab208a020bca4646a1dea46'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 15 Jan 2024 17:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 15 Jan 2024 17:07:12 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:5d0aeceef7eeb53c3f853fb229ea7fd13a5a56f4ba371ca48f0477493046b702`  
		Last Modified: Tue, 13 Feb 2024 00:42:47 GMT  
		Size: 31.4 MB (31422425 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6fac0cac18482d2030c25ed7dd0c7509a119f11b8c883dd5761b837e528851b`  
		Last Modified: Tue, 13 Feb 2024 01:54:38 GMT  
		Size: 1.1 MB (1066597 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6b305bc3c86387f1529fc0f75f2bca8107f2fcbe64daa9f5b648220f4bd0088`  
		Last Modified: Tue, 13 Feb 2024 01:54:39 GMT  
		Size: 31.3 MB (31251791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:74ca41b4d8d9b874f22c0e6b75302db86a5b15e4ed8af4991d3bd7200edcf28f`  
		Last Modified: Tue, 13 Feb 2024 01:54:38 GMT  
		Size: 2.0 MB (1955078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bullseye` - unknown; unknown

```console
$ docker pull pypy@sha256:152fd4a5b642500e633f224aaff03284785147c8c576d81b514e96e7ae7eaa00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2312857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:133dc664e794ccadba52d4acef11a227bea2378909ab69c28d740c09809115ef`

```dockerfile
```

-	Layers:
	-	`sha256:1b3ab99cc0e7160113d17e47a4939de7adeb5992d474fc6840530c2d91f792f2`  
		Last Modified: Tue, 13 Feb 2024 01:54:38 GMT  
		Size: 2.3 MB (2287651 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2b52a0896efafdc849d589616787a9c3c5430759b8cbbf125b7b6ef36c77dfc`  
		Last Modified: Tue, 13 Feb 2024 01:54:38 GMT  
		Size: 25.2 KB (25206 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-bullseye` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:132a5a1d4a9f8a4696722d97fbdc58fe6d450af0f3a39b07c82d53d315ca4ec1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.3 MB (62314975 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd98b3e080ebc9f5f507a47133d693d28f9115cbe0de3d700e0d0063adfdc885`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 15 Jan 2024 17:07:12 GMT
ADD file:ef14ef2abd4725ea6056637e44d9261e2b025853230ea45636b67a735b3d4918 in / 
# Mon, 15 Jan 2024 17:07:12 GMT
CMD ["bash"]
# Mon, 15 Jan 2024 17:07:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jan 2024 17:07:12 GMT
ENV LANG=C.UTF-8
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PYPY_VERSION=7.3.15
# Mon, 15 Jan 2024 17:07:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-linux64.tar.bz2'; 			sha256='e857553bdc4f25ba9670a5c173a057a9ff71262d5c5da73a6ddef9d7dc5d4f5e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-aarch64.tar.bz2'; 			sha256='31b41fca7280636d7818713b7a0fab8f34ece9c82cc88e51d305d43b3e6306d6'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-linux32.tar.bz2'; 			sha256='cb5c1da62a8ca31050173c4f6f537bc3ff316026895e5f1897b9bb526babae79'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-s390x.tar.bz2'; 			sha256='eb442279ec3f1eb17da296e38b531d3ca50c6418eab208a020bca4646a1dea46'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 15 Jan 2024 17:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 15 Jan 2024 17:07:12 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:abd2c048cba46f85ffcdbd38202d0906c11ea93d39d8ac934411570844119d08`  
		Last Modified: Tue, 13 Feb 2024 00:45:38 GMT  
		Size: 30.1 MB (30071077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6868da6856b05e2a62ae909c37c8a08e473185337a3151da8832579385002845`  
		Last Modified: Wed, 14 Feb 2024 07:55:34 GMT  
		Size: 1.1 MB (1053925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:15ba66499dc0d3c504fa4dc3d58f9fc5c9810544699ac25d2b24d1601bb8033f`  
		Last Modified: Wed, 14 Feb 2024 08:02:50 GMT  
		Size: 29.2 MB (29234901 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acd78a2b98f0bf38b89492d01be43b637d21e03042398e821916cf92fa6be42c`  
		Last Modified: Wed, 14 Feb 2024 08:02:49 GMT  
		Size: 2.0 MB (1955072 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bullseye` - unknown; unknown

```console
$ docker pull pypy@sha256:8e541677f41bcbdd839f9b8c66d70e0ddb75cb3116ae48e81557e8c62076bf59
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2313061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19d91516299aae013039c0d26c4b418e9854075fc2d5d3446449a3ce80dac5dd`

```dockerfile
```

-	Layers:
	-	`sha256:f9da73b7045fd49c643b993bc04232ef85767298ba51d876cee8ca0f76a73fe6`  
		Last Modified: Wed, 14 Feb 2024 08:02:49 GMT  
		Size: 2.3 MB (2287988 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:52fd6bc519329c6c4db3ec6ad0e257ab070966ec362c788440d82062e9e4e543`  
		Last Modified: Wed, 14 Feb 2024 08:02:49 GMT  
		Size: 25.1 KB (25073 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-bullseye` - linux; 386

```console
$ docker pull pypy@sha256:133227f5ad1c7329e27bb9e7a6bb0087584c9f9c1bd3074d1648a16f5fd83186
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62191805 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f1a43a9b40018e2d54f87297f43cc2a465b1adc9ab73e055be31c0a1b35f1f9`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 15 Jan 2024 17:07:12 GMT
ADD file:9eaee5af136d095dc1dac0ffce0fde09d8f1bd02ff7cb65ee67e00b2a66f34f7 in / 
# Mon, 15 Jan 2024 17:07:12 GMT
CMD ["bash"]
# Mon, 15 Jan 2024 17:07:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 15 Jan 2024 17:07:12 GMT
ENV LANG=C.UTF-8
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PYPY_VERSION=7.3.15
# Mon, 15 Jan 2024 17:07:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-linux64.tar.bz2'; 			sha256='e857553bdc4f25ba9670a5c173a057a9ff71262d5c5da73a6ddef9d7dc5d4f5e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-aarch64.tar.bz2'; 			sha256='31b41fca7280636d7818713b7a0fab8f34ece9c82cc88e51d305d43b3e6306d6'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-linux32.tar.bz2'; 			sha256='cb5c1da62a8ca31050173c4f6f537bc3ff316026895e5f1897b9bb526babae79'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-s390x.tar.bz2'; 			sha256='eb442279ec3f1eb17da296e38b531d3ca50c6418eab208a020bca4646a1dea46'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 15 Jan 2024 17:07:12 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 15 Jan 2024 17:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 15 Jan 2024 17:07:12 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:1ac8173b08d16f9f136fb0e3ee39999cef7495f924ecb43f3ca4a4eea267cc88`  
		Last Modified: Tue, 13 Feb 2024 00:44:36 GMT  
		Size: 32.4 MB (32407443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2f46a3d49c59b21b17959079c66a443500da9927207ecf8f21629b76a1ce95`  
		Last Modified: Tue, 13 Feb 2024 01:54:44 GMT  
		Size: 1.1 MB (1079154 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca81dba4d14ac53e5edbe5a0cb0d678d4e34ba30fe88fe7ca2f4a973b2c740f3`  
		Last Modified: Tue, 13 Feb 2024 01:54:44 GMT  
		Size: 26.8 MB (26750229 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2b6c5886edfb3a315495f8554b9f4c2f32fe67dc5bdd421f294319bcb58f554c`  
		Last Modified: Tue, 13 Feb 2024 01:54:44 GMT  
		Size: 2.0 MB (1954979 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bullseye` - unknown; unknown

```console
$ docker pull pypy@sha256:f761b499fc79092076845b5e192cb9a5b949c66f3a86b03307e0e134a0c3bc22
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309943 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d28ffac9a7c46406fa6cc85e6bbef23675334bd6e0c54b0ebd49577efc5154e3`

```dockerfile
```

-	Layers:
	-	`sha256:42ca144916fc4aade2b94a213358c52366c3a913aa4b73587bcfa7d61dc8f05c`  
		Last Modified: Tue, 13 Feb 2024 01:54:44 GMT  
		Size: 2.3 MB (2284830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8fb004717c3be530d845fe8dd5abcbde57b84affbd72df08413fc410276af8e7`  
		Last Modified: Tue, 13 Feb 2024 01:54:44 GMT  
		Size: 25.1 KB (25113 bytes)  
		MIME: application/vnd.in-toto+json
