## `hylang:0-pypy3.9-bookworm`

```console
$ docker pull hylang@sha256:bd0068108559d838ef3783f919ed0ef0ed38a0bef89ecc25c43aec9e6ea74a3d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:0-pypy3.9-bookworm` - linux; amd64

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

### `hylang:0-pypy3.9-bookworm` - unknown; unknown

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

### `hylang:0-pypy3.9-bookworm` - linux; arm64 variant v8

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

### `hylang:0-pypy3.9-bookworm` - unknown; unknown

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

### `hylang:0-pypy3.9-bookworm` - linux; 386

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

### `hylang:0-pypy3.9-bookworm` - unknown; unknown

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
