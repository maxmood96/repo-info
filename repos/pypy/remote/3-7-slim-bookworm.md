## `pypy:3-7-slim-bookworm`

```console
$ docker pull pypy@sha256:e5d9bef029a7c38f12bcdb534201e17c49e9908a5ce135f17961c7bf3a8e985e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:3-7-slim-bookworm` - linux; amd64

```console
$ docker pull pypy@sha256:20e8531bb27d9e3f387056c9c2746079408537f765d4ccbf31faec1b9cf10eb5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66798179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04c0b09bc6830fad6ee15e861ac0e1b9b53d2e4219264313878acac06670de90`
-	Default Command: `["pypy3"]`

```dockerfile
# Fri, 05 Apr 2024 21:59:23 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Fri, 05 Apr 2024 21:59:23 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:59:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:59:23 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:59:23 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:59:23 GMT
ENV PYPY_VERSION=7.3.15
# Fri, 05 Apr 2024 21:59:23 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-linux64.tar.bz2'; 			sha256='33c584e9a70a71afd0cb7dd8ba9996720b911b3b8ed0156aea298d4487ad22c3'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-aarch64.tar.bz2'; 			sha256='52146fccaf64e87e71d178dda8de63c01577ec3923073dc69e1519622bcacb74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-linux32.tar.bz2'; 			sha256='75dd58c9abd8b9d78220373148355bc3119febcf27a2c781d64ad85e7232c4aa'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-s390x.tar.bz2'; 			sha256='209e57596381e13c9914d1332f359dc4b78de06576739747eb797bdbf85062b8'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 05 Apr 2024 21:59:23 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 05 Apr 2024 21:59:23 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 05 Apr 2024 21:59:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Fri, 05 Apr 2024 21:59:23 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:13808c22b207b066ef43572e57e4fb8c6172e887dd9a918c089a174a19371b7a`  
		Last Modified: Wed, 10 Apr 2024 01:55:34 GMT  
		Size: 29.1 MB (29131358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6b0b000f75ddb2100065aa5bf172bfa10c73b5d7b3b6e173c03c87622e8c1a97`  
		Last Modified: Wed, 10 Apr 2024 02:56:03 GMT  
		Size: 3.5 MB (3491170 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b0627c55ce5d83ad3fd97fa17e5b18a0daaf0fe67ef3f1c5a39bb20bb781404f`  
		Last Modified: Wed, 10 Apr 2024 02:56:03 GMT  
		Size: 30.9 MB (30875700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46fa41f602bdf91a6f1b8a92e939714e96e808d47c5728081e8632c2afc710f6`  
		Last Modified: Wed, 10 Apr 2024 02:56:03 GMT  
		Size: 3.3 MB (3299951 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:f5ee9c4d5d27614d0f789862c814b15a4eee016ff4732453fee78430e07f486f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2387669 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eba946e2905061930648c33931d09c10391b37132efafcf0d235381a679732ea`

```dockerfile
```

-	Layers:
	-	`sha256:1affe54b927e9db2ee95068a31ed91deb80a3b8f12cf13fa50e8b1e4f8b16a8e`  
		Last Modified: Wed, 10 Apr 2024 02:56:02 GMT  
		Size: 2.4 MB (2361725 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:881143e35d87af202c922ab5e98ad022674926c8a6cc4e31c7fb83693d5c4d3b`  
		Last Modified: Wed, 10 Apr 2024 02:56:02 GMT  
		Size: 25.9 KB (25944 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:3-7-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:ef2f86ecf31275d6ca0decc9d33b95e03b9a8b0c9eba321a39b6e113d442cb2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64947184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c451a3071c16f34a4b280b0ada2f0dccabb7831640f7ae5f60914e1d36382468`
-	Default Command: `["pypy3"]`

```dockerfile
# Tue, 12 Mar 2024 00:45:36 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 12 Mar 2024 00:45:37 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:59:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:59:23 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:59:23 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:59:23 GMT
ENV PYPY_VERSION=7.3.15
# Fri, 05 Apr 2024 21:59:23 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-linux64.tar.bz2'; 			sha256='33c584e9a70a71afd0cb7dd8ba9996720b911b3b8ed0156aea298d4487ad22c3'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-aarch64.tar.bz2'; 			sha256='52146fccaf64e87e71d178dda8de63c01577ec3923073dc69e1519622bcacb74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-linux32.tar.bz2'; 			sha256='75dd58c9abd8b9d78220373148355bc3119febcf27a2c781d64ad85e7232c4aa'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-s390x.tar.bz2'; 			sha256='209e57596381e13c9914d1332f359dc4b78de06576739747eb797bdbf85062b8'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 05 Apr 2024 21:59:23 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 05 Apr 2024 21:59:23 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 05 Apr 2024 21:59:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Fri, 05 Apr 2024 21:59:23 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d5e967355e27afb96983147c5620f49e0324496b8add2a3f37df9021fdff0d`  
		Last Modified: Tue, 09 Apr 2024 06:37:46 GMT  
		Size: 3.3 MB (3314256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d098f4aa0dc91de0def4ea4edc5d69693e06f9dab982e2f1c3fab06bfd04e490`  
		Last Modified: Tue, 09 Apr 2024 06:37:47 GMT  
		Size: 29.2 MB (29176578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e5948aa4836e9788445faeeff2957b8a7e62fb3092dbaaee639dcea7884188`  
		Last Modified: Tue, 09 Apr 2024 06:37:46 GMT  
		Size: 3.3 MB (3299916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:d798e24e06ad4c9663dbc5c2c2db2e59af18f36037193f8c8aeaacdd40062658
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2389029 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1afdad0ad8c1565f0c350e80ab8198ce0298c09db577b19f1d8728468f61ec3`

```dockerfile
```

-	Layers:
	-	`sha256:215d7b3d12e762897f253365256bce0a76033a85b1d7c19510e06fc6a2cf2b99`  
		Last Modified: Tue, 09 Apr 2024 06:37:46 GMT  
		Size: 2.4 MB (2363232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8076289dadd2f150a459e95b91ad6b094fc9d6ae5f2d4854a680dddda2357a55`  
		Last Modified: Tue, 09 Apr 2024 06:37:46 GMT  
		Size: 25.8 KB (25797 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:3-7-slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:320d955caf3def3d016fb2a5d7e8c06c92a3654559a28f0f4e007a30bac3b72b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.2 MB (64172747 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8a3fe5ac14a1961aca0418b7dfe0f0825993f1f62ec8767c442ec74164fa0f17`
-	Default Command: `["pypy3"]`

```dockerfile
# Tue, 12 Mar 2024 00:57:59 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Tue, 12 Mar 2024 00:58:00 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:59:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:59:23 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:59:23 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Apr 2024 21:59:23 GMT
ENV PYPY_VERSION=7.3.15
# Fri, 05 Apr 2024 21:59:23 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-linux64.tar.bz2'; 			sha256='33c584e9a70a71afd0cb7dd8ba9996720b911b3b8ed0156aea298d4487ad22c3'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-aarch64.tar.bz2'; 			sha256='52146fccaf64e87e71d178dda8de63c01577ec3923073dc69e1519622bcacb74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-linux32.tar.bz2'; 			sha256='75dd58c9abd8b9d78220373148355bc3119febcf27a2c781d64ad85e7232c4aa'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-s390x.tar.bz2'; 			sha256='209e57596381e13c9914d1332f359dc4b78de06576739747eb797bdbf85062b8'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 05 Apr 2024 21:59:23 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 05 Apr 2024 21:59:23 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 05 Apr 2024 21:59:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Fri, 05 Apr 2024 21:59:23 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3cd8f5bb51df8a7d93dab1ade22d490fd9350a728323cdf6f9a63e97288899`  
		Last Modified: Mon, 08 Apr 2024 22:00:13 GMT  
		Size: 3.5 MB (3496213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a489eba2dccc2eb008d1293dd8393f1d4159f2c6f677a4898909f6056203061f`  
		Last Modified: Mon, 08 Apr 2024 22:00:14 GMT  
		Size: 27.2 MB (27235134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18307e18a43e81798a7affec250b1f234378962a7cef47d7fdaef0bfc507d3a`  
		Last Modified: Mon, 08 Apr 2024 22:00:14 GMT  
		Size: 3.3 MB (3299527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:cce8c8c59459b423858b264680ba999389f9c8079859d18af3898fc094bb97f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2386006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faf730bfd7ac361e1313614b06c3057c063e865689a7c87e700558ace0b68851`

```dockerfile
```

-	Layers:
	-	`sha256:a0221b28013186266aab22ed81fd6286f54bfb12e7ddb1362d77574338627d78`  
		Last Modified: Mon, 08 Apr 2024 22:00:13 GMT  
		Size: 2.4 MB (2360120 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:108df572ee7175e7902effe6d12d98e9f3c10548025baf5636ab5c63a42dc08e`  
		Last Modified: Mon, 08 Apr 2024 22:00:13 GMT  
		Size: 25.9 KB (25886 bytes)  
		MIME: application/vnd.in-toto+json
