## `hylang:pypy3.9`

```console
$ docker pull hylang@sha256:26740612293d129a6af3bdb77b01b38a6c044c29330f1233e6e29d771b393ec7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.20348.2402; amd64
	-	windows version 10.0.17763.5696; amd64

### `hylang:pypy3.9` - linux; amd64

```console
$ docker pull hylang@sha256:db04b67c18b3916ff69b8392df6ab94d9ccd53d0e75fb2c6be2bb61244dcf4e1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.2 MB (70187992 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e773e983ae97f5918dd8b74d010e568779cc6bae751c9f2a7c92bf176b29ca3d`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYPY_VERSION=7.3.16
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-linux64.tar.bz2'; 			sha256='16f9c5b808c848516e742986e826b833cdbeda09ad8764e8704595adbe791b23'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-aarch64.tar.bz2'; 			sha256='de3f2ed3581b30555ac0dd3e4df78a262ec736a36fb2e8f28259f8539b278ef4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-linux32.tar.bz2'; 			sha256='583b6d6dd4e8c07cbc04da04a7ec2bdfa6674825289c2378c5e018d5abe779ea'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-s390x.tar.bz2'; 			sha256='7a56ebb27dba3110dc1ff52d8e0449cdb37fe5c2275f7faf11432e4e164833ba'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["pypy3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:234c0d9f05c152215864977e79dffa974aab0b5f01a8c249aa11165dccb89f94`  
		Last Modified: Thu, 25 Apr 2024 18:53:05 GMT  
		Size: 3.3 MB (3299433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c27386a3103593468b99f9e6f334aae9e9a332ccef82228766246ddd7f5042`  
		Last Modified: Thu, 25 Apr 2024 18:53:06 GMT  
		Size: 30.9 MB (30879877 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4b44ab4ce6638ef895eb03d89d804d4ea2ee9dcf2d4a946223e60cce1a0b1c2`  
		Last Modified: Thu, 25 Apr 2024 18:53:05 GMT  
		Size: 2.9 MB (2912366 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f811e77aae3ec93e8a6343273aa23cd093b5734b6b22e53f5e4308ad6027d2`  
		Last Modified: Thu, 25 Apr 2024 19:52:40 GMT  
		Size: 3.9 MB (3945837 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:a1a46058cf2ddea498c8e056b3fb239ddeacf0826c47d456c8abedf29b5390e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377594 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c006464381322cc62a18feb61cd8ac20dc8e66229d4179a94640d341d0733019`

```dockerfile
```

-	Layers:
	-	`sha256:301a6cf1107996184a37aea654637f33eb11b169b9fd61a4ec455b9b0bbf9e20`  
		Last Modified: Thu, 25 Apr 2024 19:52:40 GMT  
		Size: 2.4 MB (2367747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3da62aa739aaadcf01f86d7d54af242ab9aeefb5bde89d450f886fdf4d7007bb`  
		Last Modified: Thu, 25 Apr 2024 19:52:40 GMT  
		Size: 9.8 KB (9847 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.9` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:bfe09b5927be6da5d94598384e97e1c7d19bfb888873ca6ba64c1b2cf3ba7887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68336541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3248aee232411622eac6643b596888b0c2cd60bf57f3789d3fec0a0d154ade1`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:ea7004fb788ab5cf1604d6e71153c48d99b75fbd1810e78a8c79faff11fe6771 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYPY_VERSION=7.3.16
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-linux64.tar.bz2'; 			sha256='16f9c5b808c848516e742986e826b833cdbeda09ad8764e8704595adbe791b23'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-aarch64.tar.bz2'; 			sha256='de3f2ed3581b30555ac0dd3e4df78a262ec736a36fb2e8f28259f8539b278ef4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-linux32.tar.bz2'; 			sha256='583b6d6dd4e8c07cbc04da04a7ec2bdfa6674825289c2378c5e018d5abe779ea'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-s390x.tar.bz2'; 			sha256='7a56ebb27dba3110dc1ff52d8e0449cdb37fe5c2275f7faf11432e4e164833ba'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["pypy3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
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
	-	`sha256:a96c69adbdaf4f56ca65e2514ff7568ae0fdf282c29d6bd255cb31595b7c0669`  
		Last Modified: Fri, 26 Apr 2024 08:30:12 GMT  
		Size: 29.2 MB (29175722 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:00863b232db38cf6cf2bb2f6e6ab65bf1015468e6c3c3c668b08551624e4baa8`  
		Last Modified: Fri, 26 Apr 2024 08:30:11 GMT  
		Size: 2.9 MB (2912668 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b8938e934ba9e485ce6e69407a238e461933b8d886b964c4eda755f0aecc9ac`  
		Last Modified: Fri, 26 Apr 2024 12:40:55 GMT  
		Size: 3.9 MB (3946017 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:a8ca5d13d10236bfabda8f95a6d6e29ef258151dfa0d6fddb9049f541e4be5f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0640e493005b2a47a2945ba293cef3129712bfa598c64b6bb63ca5689306b28`

```dockerfile
```

-	Layers:
	-	`sha256:c1488279d467b5e5d150e0f2be4765afacba88bf43ed4d202eaedc3a5cdfa2a9`  
		Last Modified: Fri, 26 Apr 2024 12:40:54 GMT  
		Size: 2.4 MB (2367968 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:714f4d964b609dfd43f5bffc06a8e435ab7b4931e5f0e0897ab4cd1c93eb7174`  
		Last Modified: Fri, 26 Apr 2024 12:40:54 GMT  
		Size: 9.9 KB (9890 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.9` - linux; 386

```console
$ docker pull hylang@sha256:c3615da2097d4b2d3173b65066b4280688076bc655cb59c466fe0cdccdcec881
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.6 MB (67614666 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:106a5fb7789ed83614cf7d3393eb78b7b13347ad760be664fd8f21f1db133588`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:252f04703c9ed01e5aa32f764c7d751f0a3b17ed9ef1961cd1972aa8453b5cf3 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYPY_VERSION=7.3.16
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-linux64.tar.bz2'; 			sha256='16f9c5b808c848516e742986e826b833cdbeda09ad8764e8704595adbe791b23'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-aarch64.tar.bz2'; 			sha256='de3f2ed3581b30555ac0dd3e4df78a262ec736a36fb2e8f28259f8539b278ef4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-linux32.tar.bz2'; 			sha256='583b6d6dd4e8c07cbc04da04a7ec2bdfa6674825289c2378c5e018d5abe779ea'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.16-s390x.tar.bz2'; 			sha256='7a56ebb27dba3110dc1ff52d8e0449cdb37fe5c2275f7faf11432e4e164833ba'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["pypy3"]
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HY_VERSION=0.28.0
# Fri, 05 Jan 2024 23:20:01 GMT
ENV HYRULE_VERSION=0.5.0
# Fri, 05 Jan 2024 23:20:01 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7075ead1c5d56dc11510b76b25c291657dc73ecf7daad5361939429487745b9a`  
		Last Modified: Tue, 14 May 2024 00:51:58 GMT  
		Size: 30.2 MB (30162638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61d6073854f0897424edcb3cbcd0b1f5e1e30323a85521f3f6978d4ac76552ed`  
		Last Modified: Tue, 14 May 2024 01:55:20 GMT  
		Size: 3.3 MB (3304866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c77c5836676846ab6066adc4c4a27e2e43a2dea3a6a5ef2a408b2208ff543d3c`  
		Last Modified: Tue, 14 May 2024 01:55:21 GMT  
		Size: 27.3 MB (27288986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:613b4b20d6d332d53008501579b087d3f29838f7e339cf5148e26e08f6ca0368`  
		Last Modified: Tue, 14 May 2024 01:55:20 GMT  
		Size: 2.9 MB (2912095 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:229ec15a7c595e5a4022deea0c77270ccaa9e55ec0f42b79e221153a9b47915a`  
		Last Modified: Tue, 14 May 2024 02:58:39 GMT  
		Size: 3.9 MB (3946081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:7e056606fce2fd41ac9ec1ad9a10f226a68255b701c91fdff355e44520da579e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2374659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f671dd2e61757ebf61c8109595ebe5dba8fe3a6675ba468ed7e3d0d3341ca033`

```dockerfile
```

-	Layers:
	-	`sha256:c7a0b8216d61e465da9f4f25a3ee28ac73a7f3db9e76bc87c4137562fcfd619b`  
		Last Modified: Tue, 14 May 2024 02:58:39 GMT  
		Size: 2.4 MB (2364863 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0f09c26f08b815471106baa35d16f8cba4e60f99688e4ae8dd260583eabc84d9`  
		Last Modified: Tue, 14 May 2024 02:58:38 GMT  
		Size: 9.8 KB (9796 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.9` - windows version 10.0.20348.2402; amd64

```console
$ docker pull hylang@sha256:a25d79241abc51b916c1704b7a3cbc5eab5b9370bff8ac79befca346ad6b4e0d
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2050230951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcebddddc6c3c4c169d9419e98074e357a3ca86df78703bdf100386ce0b51c93`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Thu, 25 Apr 2024 18:52:39 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 25 Apr 2024 18:54:52 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Thu, 25 Apr 2024 18:55:53 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Thu, 25 Apr 2024 18:55:53 GMT
ENV PYPY_VERSION=7.3.16
# Thu, 25 Apr 2024 18:56:37 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.9-v7.3.16-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '06ec12a5e964dc0ad33e6f380185a4d295178dce6d6df512f508e7aee00a1323'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.9-v7.3.16-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Thu, 25 Apr 2024 18:56:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 25 Apr 2024 18:56:38 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 25 Apr 2024 18:57:02 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Thu, 25 Apr 2024 18:57:03 GMT
CMD ["pypy"]
# Thu, 25 Apr 2024 19:53:06 GMT
ENV HY_VERSION=0.28.0
# Thu, 25 Apr 2024 19:53:07 GMT
ENV HYRULE_VERSION=0.5.0
# Thu, 25 Apr 2024 19:54:09 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 25 Apr 2024 19:54:10 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:197484daab96ebaf9683bc9230fb0043a8780d2afef249baa386f372a548b76a`  
		Last Modified: Tue, 09 Apr 2024 18:00:52 GMT  
		Size: 610.8 MB (610774836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0414c2a6a40ac977f22d537d9921e9eb50e65fe451a68ee38248c08272a54521`  
		Last Modified: Thu, 25 Apr 2024 18:57:07 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139953c0489d6f01af769411d8f2a7a1042a3e1ee78a2329567a12fa04e035db`  
		Last Modified: Thu, 25 Apr 2024 18:57:07 GMT  
		Size: 502.5 KB (502459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:39910ad6949a64068c45cbdd212105ea6964c6071019b8f56fd14fede16bb722`  
		Last Modified: Thu, 25 Apr 2024 18:57:08 GMT  
		Size: 15.5 MB (15509622 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70b82409f94d7511de5988253c8f97d9c4fc9615a7a89f163efe1f9ae4d4f9da`  
		Last Modified: Thu, 25 Apr 2024 18:57:07 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ae0d922e753fcbde114601010f8aa0ecd061649b01715415725afd6298b0c47`  
		Last Modified: Thu, 25 Apr 2024 18:57:09 GMT  
		Size: 26.7 MB (26728556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55f16dff5511ecefda307210526a4b7ca626bd74e4687b7c4574b4aeac5074b0`  
		Last Modified: Thu, 25 Apr 2024 18:57:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:404d09acf68c576aef47739b415d6088fce3e55c306b8b2b6526f12548ce462c`  
		Last Modified: Thu, 25 Apr 2024 18:57:06 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e2f35ff15d9262ade5226ce54cf0322785048e36f2b1f671c1e756a652bce0b`  
		Last Modified: Thu, 25 Apr 2024 18:57:06 GMT  
		Size: 3.5 MB (3492198 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb3169854d9656064fe72787e5320077e498a03c5c81ee7dd145ec140b87c80f`  
		Last Modified: Thu, 25 Apr 2024 18:57:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60941a53e088363c2dc1325b66fd81b0512b68bf6b37a7dea2137f41e0943b10`  
		Last Modified: Thu, 25 Apr 2024 19:54:14 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43650f6a6b7f4766fb3255d0fb6e46f183f718cca6adf6a209153d58c1816cb6`  
		Last Modified: Thu, 25 Apr 2024 19:54:14 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0365ad38c522c98968131e7ea39a4d4c6019126caed995068b7bdda41b5205e4`  
		Last Modified: Thu, 25 Apr 2024 19:54:15 GMT  
		Size: 4.6 MB (4614167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e67a7bbd69ad02501e107129417336b2cdfe6b68e6687aa88f4e28b5e39ee496`  
		Last Modified: Thu, 25 Apr 2024 19:54:14 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.9` - windows version 10.0.17763.5696; amd64

```console
$ docker pull hylang@sha256:7566855ffbef978b595ade4007afdbdaacec8e92f506ed4b9aef01067d85dd97
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2215285972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65ccbef69914332775f321c08b8a50fcb6ae4c87688f1cb8f3f42f273818f8f4`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Thu, 25 Apr 2024 18:53:33 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 25 Apr 2024 18:54:19 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Thu, 25 Apr 2024 18:54:58 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Thu, 25 Apr 2024 18:54:59 GMT
ENV PYPY_VERSION=7.3.16
# Thu, 25 Apr 2024 18:55:42 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.9-v7.3.16-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '06ec12a5e964dc0ad33e6f380185a4d295178dce6d6df512f508e7aee00a1323'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.9-v7.3.16-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Thu, 25 Apr 2024 18:55:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 25 Apr 2024 18:55:44 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 25 Apr 2024 18:56:24 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Thu, 25 Apr 2024 18:56:25 GMT
CMD ["pypy"]
# Thu, 25 Apr 2024 19:53:16 GMT
ENV HY_VERSION=0.28.0
# Thu, 25 Apr 2024 19:53:18 GMT
ENV HYRULE_VERSION=0.5.0
# Thu, 25 Apr 2024 19:56:04 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Thu, 25 Apr 2024 19:56:05 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e920b78002850882cc637991bf16e3cd3fdd45576cf3e930819c98f6b43518d3`  
		Last Modified: Tue, 09 Apr 2024 17:26:42 GMT  
		Size: 513.8 MB (513807602 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aca2e0d3d7f2ac1d3009f18ca29e987bca3886bd2e74af58ba15135495b7d993`  
		Last Modified: Thu, 25 Apr 2024 18:56:32 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc4e5a2923220816a77dea7254202bdf69c3ce4dbdde69179e3e27a176ab609f`  
		Last Modified: Thu, 25 Apr 2024 18:56:32 GMT  
		Size: 495.1 KB (495114 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b3ecfefdf2e38e0e8724b8b1f9d1d250ea46a289794a77ef0da68d4c098c08`  
		Last Modified: Thu, 25 Apr 2024 18:56:33 GMT  
		Size: 15.5 MB (15527556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a4964efbaa1826956e6b8640b40802ce87b8a0fd52798527fbad7dfec99abfb`  
		Last Modified: Thu, 25 Apr 2024 18:56:31 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d34fd3bbcf3099179165c7a29d9532bc3ad8eca4efb457db886cd78036b9fb84`  
		Last Modified: Thu, 25 Apr 2024 18:56:32 GMT  
		Size: 26.7 MB (26731932 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df56ec8be44728a4ac7adf12a619c865d3f68f0e1d13a370a2ecc9045438b9da`  
		Last Modified: Thu, 25 Apr 2024 18:56:29 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:989e8806db5bd103820f834b24cab876a3c366df3742759d75a00e6f6af69823`  
		Last Modified: Thu, 25 Apr 2024 18:56:29 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00a65250cbb5634ae1d389e0acdb52d4ae47b65138ebc31c3ce14e7e92fa73a3`  
		Last Modified: Thu, 25 Apr 2024 18:56:30 GMT  
		Size: 3.5 MB (3491676 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb9caed9c3913d073dc293c0814d3e059eefa9201e24d1ac67a4508693527925`  
		Last Modified: Thu, 25 Apr 2024 18:56:29 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e5449118ebd4a9ae06f6761e736e333e7ab44d01c321a96e21e64e33471b01`  
		Last Modified: Thu, 25 Apr 2024 19:56:07 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efa4cc21b88c74cb822b8fd7c604ad6701bb5e92b8e74f4c8db0066700ac5af8`  
		Last Modified: Thu, 25 Apr 2024 19:56:07 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b8c4cbfc200d7d5ad12f76e0b7933430ee8cf15ee05ad738666a9b95eb3098`  
		Last Modified: Thu, 25 Apr 2024 19:56:08 GMT  
		Size: 4.6 MB (4601266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf5fdefe5cd11b491588a0b1d3fc289c8edeffe4b9fd86399501684c354400e`  
		Last Modified: Thu, 25 Apr 2024 19:56:07 GMT  
		Size: 1.3 KB (1301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
