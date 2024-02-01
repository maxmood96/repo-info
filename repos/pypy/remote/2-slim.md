## `pypy:2-slim`

```console
$ docker pull pypy@sha256:782cad81903c85cb2c7d11ef227afffef9bdc4f837f1e5a055228c096b92ccb5
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
$ docker pull pypy@sha256:c09090ae0c854de895678dd318f238813854326da081d36907f6ab1f2efdadb1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.5 MB (65487929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a653c1862f2b224f5910b9960385def1dffd196f49c4500b3b690ce0febd438a`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 15 Jan 2024 17:07:12 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
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
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:167e4ca279bc61178200d6160b2dff17af1cf4575bed06752369fccccc02f2db`  
		Last Modified: Thu, 01 Feb 2024 00:06:13 GMT  
		Size: 863.2 KB (863182 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee54c00275a9903a79de9bc1af0b6b3f21f90cd274c421ac14bf20ff0ccfc92e`  
		Last Modified: Thu, 01 Feb 2024 00:06:13 GMT  
		Size: 31.3 MB (31251777 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:02a9dd6293b81b3971de0b85869b97e82b18423e511efeeefed4fb25ac8d7d2d`  
		Last Modified: Thu, 01 Feb 2024 00:06:13 GMT  
		Size: 2.0 MB (1955143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:9ba4ab3863109809c7cd67dccce852dae008f9023c7a63b1b9763b11089e38a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3911c840201d8033b85dc083eaf6f31bdd589c45f6406b8ec9716979823cfa`

```dockerfile
```

-	Layers:
	-	`sha256:d9a2b128db78227eb655254b35dbebfa3e59dfbd10fd6e308b62e9b4f89ade68`  
		Last Modified: Thu, 01 Feb 2024 00:06:13 GMT  
		Size: 2.2 MB (2195885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:089a2cfe3fb7935c605e7424bf706bd0d2afde03e59e7cdd71b82553a4ba0bf7`  
		Last Modified: Thu, 01 Feb 2024 00:06:12 GMT  
		Size: 25.2 KB (25203 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:3f9c3cec14f3f201c4b8d0680262742dc3b5136c74c8afae96a84be325d0496d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.1 MB (62104760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9c960a89874b055b7eb84982669d68114677686e7c7cf0a346c1c8df81ffa609`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 15 Jan 2024 17:07:12 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
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
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2988e17a0a6a703a7c549da0d53fc83f6f25b391230d7647d87ac351b864432e`  
		Last Modified: Thu, 01 Feb 2024 20:34:18 GMT  
		Size: 850.5 KB (850525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c0d87593366063f11d4b1c632cd46617c284f74ca167739de9169910c63187c1`  
		Last Modified: Thu, 01 Feb 2024 20:37:57 GMT  
		Size: 29.2 MB (29234894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00d787358b72a393baa120ca52b24da5ae251d2ac8cc8d9b08b112172f648c77`  
		Last Modified: Thu, 01 Feb 2024 20:37:56 GMT  
		Size: 2.0 MB (1955007 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:960a60c85a91135ecfad6c91683342bb52a6ce5f45e15d37299f1eeeda4d9059
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2221291 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f2e8230b9d9254a282f56522cdf4ad307554be01719bc583f2d96b5cbfd918d`

```dockerfile
```

-	Layers:
	-	`sha256:350f6a8c9b37bfc0d92fab6008c1d93efc34ac31a70dfc1979cb7d9131a9bf50`  
		Last Modified: Thu, 01 Feb 2024 20:37:56 GMT  
		Size: 2.2 MB (2196222 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c38e6f85f8bae6b7c9b964d0cc729bf5c0947b15f798e9bb203503b3f0716f87`  
		Last Modified: Thu, 01 Feb 2024 20:37:56 GMT  
		Size: 25.1 KB (25069 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim` - linux; 386

```console
$ docker pull pypy@sha256:17ad57a756cedc247b280df552da0e87a838d990df4467a1421559ea2082b64d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.0 MB (61983201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd211b87024ee84a4c37bdb3567b93f848c592346bf330c19d93c6368b8dae8b`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 15 Jan 2024 17:07:12 GMT
ADD file:0e0961062de8ea0706118b883ee7638aae4465761dec06896f1bd28b9fb4b516 in / 
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
	-	`sha256:854acbf4b2df9e625a11c0e67025dce58b41d948bb7e5d4d5e708e25489f6e8f`  
		Last Modified: Wed, 31 Jan 2024 22:44:37 GMT  
		Size: 32.4 MB (32402507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27b12363d1734619f972bb0cea51d7ec194bc2b118f464f319dadea7f68206a3`  
		Last Modified: Thu, 01 Feb 2024 00:05:50 GMT  
		Size: 875.5 KB (875502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e507eeb8c25af4ffea6d0f3618a5ef57b572e0a5f3ce030525cf4942e46d14da`  
		Last Modified: Thu, 01 Feb 2024 00:05:50 GMT  
		Size: 26.8 MB (26750225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d61e27f75858478f642a0542ce72283f9381586f2c4c137f4c45a5345e80214`  
		Last Modified: Thu, 01 Feb 2024 00:05:49 GMT  
		Size: 2.0 MB (1954967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim` - unknown; unknown

```console
$ docker pull pypy@sha256:29b4d9f7357d5fd463ac137de4680722625f328341d7406259f2e46fa79078b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2218174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21649eba33c4a56a8a9d5b2fbea19555d8710d62379f43ac547070fa4dc66710`

```dockerfile
```

-	Layers:
	-	`sha256:7280cd31dd23df4239e4f718c8a43d0ce39f2fbf90fb6bde8663ebc98886a795`  
		Last Modified: Thu, 01 Feb 2024 00:05:49 GMT  
		Size: 2.2 MB (2193064 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbacd24afd990a16f8438190bab2a835682537829e402713a8d50ccad0808b53`  
		Last Modified: Thu, 01 Feb 2024 00:05:49 GMT  
		Size: 25.1 KB (25110 bytes)  
		MIME: application/vnd.in-toto+json
