## `hylang:0-pypy-bookworm`

```console
$ docker pull hylang@sha256:6c0a4909ac3f1a56124e30b0f46845fc8f28e09b822c6c3d6fbf8ab33399e40d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:0-pypy-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:a7a033ce16ebc064b99737ddff0a52ac5b9424d60c425275e57c0487955aef78
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73139222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3bbf646af0da5aa308c67b39164f0bea30afc90e31e4836d4d6fd9b0710ec03`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:d4bb05cb4d403a78b4ab5cd8d620330659d5aeb25f847d104ebc02c3a0f32624 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYPY_VERSION=7.3.15
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-linux64.tar.bz2'; 			sha256='33c584e9a70a71afd0cb7dd8ba9996720b911b3b8ed0156aea298d4487ad22c3'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-aarch64.tar.bz2'; 			sha256='52146fccaf64e87e71d178dda8de63c01577ec3923073dc69e1519622bcacb74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-linux32.tar.bz2'; 			sha256='75dd58c9abd8b9d78220373148355bc3119febcf27a2c781d64ad85e7232c4aa'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-s390x.tar.bz2'; 			sha256='209e57596381e13c9914d1332f359dc4b78de06576739747eb797bdbf85062b8'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
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
	-	`sha256:b7e123cbd4ba168653a8316b0c4dae98a4faf54eecbe614daf8a48bc8f171b43`  
		Last Modified: Wed, 10 Apr 2024 03:54:05 GMT  
		Size: 6.3 MB (6341043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:b8666fc51a41737317af708fd76ace5768676a6c192565616c582e602d39a2b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382503 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9dc1185d53bf6d0913e57278922f6a71da4c1efbdea45b3d36095ca0ecfc96d2`

```dockerfile
```

-	Layers:
	-	`sha256:4a013eff6837dbef1984615f7b9ca8818f6b1916537fe36530ffd2c7fb6ad1c9`  
		Last Modified: Wed, 10 Apr 2024 03:54:05 GMT  
		Size: 2.4 MB (2370156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:eb0f6dd8032dcfa02c65e9d5f6a8c624e161eb4a9b85bdd59fc378bbf192a018`  
		Last Modified: Wed, 10 Apr 2024 03:54:05 GMT  
		Size: 12.3 KB (12347 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:9e492945a0d547cf21cf19103220b8de2b060ccc2782773e0cfeff12f534485d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71294059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2c6d6679562bfcc773e3964d25366858c40fa5ea733441e18150849a142766a`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYPY_VERSION=7.3.15
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-linux64.tar.bz2'; 			sha256='33c584e9a70a71afd0cb7dd8ba9996720b911b3b8ed0156aea298d4487ad22c3'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-aarch64.tar.bz2'; 			sha256='52146fccaf64e87e71d178dda8de63c01577ec3923073dc69e1519622bcacb74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-linux32.tar.bz2'; 			sha256='75dd58c9abd8b9d78220373148355bc3119febcf27a2c781d64ad85e7232c4aa'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-s390x.tar.bz2'; 			sha256='209e57596381e13c9914d1332f359dc4b78de06576739747eb797bdbf85062b8'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
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
	-	`sha256:26070551e657534bdf420d43107e85b972b2e8c212413bbbe5d192bd2692c0a7`  
		Last Modified: Wed, 10 Apr 2024 00:44:06 GMT  
		Size: 29.2 MB (29162157 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a1d936c7793b384216c3c6d49661bd9ff81003956fe6b84c8378be4c2d2e22bf`  
		Last Modified: Wed, 10 Apr 2024 20:37:37 GMT  
		Size: 3.3 MB (3314216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:42f9b21eba3f90285755353cf280e8213325cb1f53d872cadef39331a200edd8`  
		Last Modified: Wed, 10 Apr 2024 20:37:37 GMT  
		Size: 29.2 MB (29176595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60da22f7d2bc045a38834e9835954f7de04a575013cfb3c6925c8adfa06f5769`  
		Last Modified: Wed, 10 Apr 2024 20:37:37 GMT  
		Size: 3.3 MB (3299974 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a094b2099cee6faef255ce5133f9e39957dc7ff5b55381da7c960132831d582`  
		Last Modified: Thu, 11 Apr 2024 10:17:31 GMT  
		Size: 6.3 MB (6341117 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:8c1bfbabf19504f4dc0d7100625eaa5aa3f19cee06fa37337b4b31797fa85988
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2382797 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ad138af030c4657c54d07a2d0a1cf122ab064ce0da0b8e624cef4bb3c7a41ca`

```dockerfile
```

-	Layers:
	-	`sha256:72f7ac2e499fc23c7a2f1d74b745b378c3f30d87dd2639fb4ee2c92e0a61bd9b`  
		Last Modified: Thu, 11 Apr 2024 10:17:31 GMT  
		Size: 2.4 MB (2370393 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03a8c871396d3c2ec1e717be811b2a34e2d630333fd62983cc8be5647828f1ec`  
		Last Modified: Thu, 11 Apr 2024 10:17:30 GMT  
		Size: 12.4 KB (12404 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:91f968da8b590efee7b82cd7e52372bfc38328e4303ac5e898d411fbad82c91b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70518560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bc9e6aaec691b4de79fdb2dfb0f26c9f37488dc9fb807de0e09bbe592e794c5d`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:d160efeeb02e2200784dd8312a13a11d9d791581efc7756ed999f76c79445b54 in / 
# Fri, 05 Jan 2024 23:20:01 GMT
CMD ["bash"]
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Jan 2024 23:20:01 GMT
ENV LANG=C.UTF-8
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 05 Jan 2024 23:20:01 GMT
ENV PYPY_VERSION=7.3.15
# Fri, 05 Jan 2024 23:20:01 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-linux64.tar.bz2'; 			sha256='33c584e9a70a71afd0cb7dd8ba9996720b911b3b8ed0156aea298d4487ad22c3'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-aarch64.tar.bz2'; 			sha256='52146fccaf64e87e71d178dda8de63c01577ec3923073dc69e1519622bcacb74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-linux32.tar.bz2'; 			sha256='75dd58c9abd8b9d78220373148355bc3119febcf27a2c781d64ad85e7232c4aa'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-s390x.tar.bz2'; 			sha256='209e57596381e13c9914d1332f359dc4b78de06576739747eb797bdbf85062b8'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
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
	-	`sha256:8a3830119a16769024de35d2dfa3d32147da5ea747ec336166bdca1049655803`  
		Last Modified: Wed, 10 Apr 2024 01:02:04 GMT  
		Size: 30.1 MB (30146515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34ab7dfa52ecec3a42aa027e3f4e3781dbaf0b36d8d849d398e10b3761a1a2b9`  
		Last Modified: Wed, 10 Apr 2024 01:52:52 GMT  
		Size: 3.5 MB (3496189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77dd586997448628496586092375c90cf7d8b16989e18941f42ff04c5f5b1fc6`  
		Last Modified: Wed, 10 Apr 2024 01:52:53 GMT  
		Size: 27.2 MB (27235164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:75894151f6a0e12a316d87abccb5c7683dd1f70fb16f9339964a3c4c6e5a51a7`  
		Last Modified: Wed, 10 Apr 2024 01:52:52 GMT  
		Size: 3.3 MB (3299542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:65d76d8e5c177b1330a75c3983429cfb6ed0b974d3ac813f5f1ac2195cb7af8f`  
		Last Modified: Wed, 10 Apr 2024 02:57:12 GMT  
		Size: 6.3 MB (6341150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:171cb9b0b2ce2c4f5db36ae8d163d62e3eb7b2f2a3de34a7f10680f462b45883
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2379486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:670a488fa4e9ecb2e4c7c1a44c28d24845ab011d14333f1793cd5bde9a793b2b`

```dockerfile
```

-	Layers:
	-	`sha256:74241a67870212e69035cf9ad73770c55d00c5f1fec7017ef79f07019d527124`  
		Last Modified: Wed, 10 Apr 2024 02:57:11 GMT  
		Size: 2.4 MB (2367232 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2bd7c361698e3059dc49bbcd659ffab9734d518bf7357ac0628adf05ea22a2cf`  
		Last Modified: Wed, 10 Apr 2024 02:57:11 GMT  
		Size: 12.3 KB (12254 bytes)  
		MIME: application/vnd.in-toto+json
