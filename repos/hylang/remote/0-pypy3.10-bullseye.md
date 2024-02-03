## `hylang:0-pypy3.10-bullseye`

```console
$ docker pull hylang@sha256:3b025187247d661ca3744e2d4e4431917c8d68b6324ae54109c572ac9e7696ec
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:0-pypy3.10-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:06b9ccd425337dc6ab6e9b932fc820b1ba3aa493d09d229bb049bea4afcbb5ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78176890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a38732ea7cd1860d3b497f034eaa4629ccf592b4b65d4cec00b9896ebfd0f245`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:5793136ecd57e1b9074c7a68cb123cdd783ece863fc1a127ef25e5f8243196b7 in / 
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
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-linux64.tar.bz2'; 			sha256='33c584e9a70a71afd0cb7dd8ba9996720b911b3b8ed0156aea298d4487ad22c3'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-aarch64.tar.bz2'; 			sha256='52146fccaf64e87e71d178dda8de63c01577ec3923073dc69e1519622bcacb74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-linux32.tar.bz2'; 			sha256='75dd58c9abd8b9d78220373148355bc3119febcf27a2c781d64ad85e7232c4aa'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-s390x.tar.bz2'; 			sha256='209e57596381e13c9914d1332f359dc4b78de06576739747eb797bdbf85062b8'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
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
	-	`sha256:70ba6f391a98e490c9cc5473568d4d1a1cfe26c367ce353173641d819982cb40`  
		Last Modified: Wed, 31 Jan 2024 22:40:40 GMT  
		Size: 31.4 MB (31417827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9e11e68766fb6d1668dc0f257e1a5bcc48ac2c5cffc72bdd6700555162713f32`  
		Last Modified: Wed, 31 Jan 2024 23:56:50 GMT  
		Size: 863.2 KB (863194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:303f5b79b669d1717dac4b22218abddb00a166c4acda9be7b9849807602dfd5c`  
		Last Modified: Wed, 31 Jan 2024 23:56:52 GMT  
		Size: 36.3 MB (36254390 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0c54d1b2c87c53a3e3d58399f7cb6e8ac5e97be7f258cd2285681442bb55de05`  
		Last Modified: Wed, 31 Jan 2024 23:56:50 GMT  
		Size: 3.3 MB (3301910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f65ed265268665583dfc7897e6b17cb830c1591784f8c7f9590641ce7eef584`  
		Last Modified: Thu, 01 Feb 2024 00:59:55 GMT  
		Size: 6.3 MB (6339569 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:675da753b21b4b262aed0648674d7b9996e48e3acafa48c28321a4b76d3e725b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3244450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b989ccdff49bd8ea240e96d90a67877cae617276c85af41994484de18895442`

```dockerfile
```

-	Layers:
	-	`sha256:59afe1329657cbdbe311d80f9555e18b6bd9054e7cb79b804d84631c734317a2`  
		Last Modified: Thu, 01 Feb 2024 00:59:54 GMT  
		Size: 3.2 MB (3234546 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fc2975622fd294ce21372ed822554d9bfdeb80877827777d9e6f22c33c08ca30`  
		Last Modified: Thu, 01 Feb 2024 00:59:53 GMT  
		Size: 9.9 KB (9904 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy3.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:6b8f87d640ded2d3be8148863bb9aed75a014e4c511c4b4b1a6aa8b0ebbba0ee
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74396884 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2313e2a84534f119bea09a338603bdc695e7e745d70590e211b96ef154d7b64`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:cd15b20717eb0882336030832e3d3e6ce8213537a76be44b281f8162903db36c in / 
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
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-linux64.tar.bz2'; 			sha256='33c584e9a70a71afd0cb7dd8ba9996720b911b3b8ed0156aea298d4487ad22c3'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-aarch64.tar.bz2'; 			sha256='52146fccaf64e87e71d178dda8de63c01577ec3923073dc69e1519622bcacb74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-linux32.tar.bz2'; 			sha256='75dd58c9abd8b9d78220373148355bc3119febcf27a2c781d64ad85e7232c4aa'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-s390x.tar.bz2'; 			sha256='209e57596381e13c9914d1332f359dc4b78de06576739747eb797bdbf85062b8'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
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
	-	`sha256:3027f1243ed994df8b91343223df47a18cef248c6db93675f3d54baa40319893`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 30.1 MB (30064334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2988e17a0a6a703a7c549da0d53fc83f6f25b391230d7647d87ac351b864432e`  
		Last Modified: Thu, 01 Feb 2024 20:34:18 GMT  
		Size: 850.5 KB (850525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f608f8d127f793b24d3bc1fb00009bdcb13280af4622cb4901997242a952753e`  
		Last Modified: Thu, 01 Feb 2024 20:34:19 GMT  
		Size: 33.8 MB (33841000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a5d6d466753529264bd52f585f33533b522737da7227176963c793ab821eb9c`  
		Last Modified: Thu, 01 Feb 2024 20:34:18 GMT  
		Size: 3.3 MB (3301551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4804f3db5add684ffc36284c3087f9c513c0d60c6a090a0fe96c2c9221c6d5bc`  
		Last Modified: Fri, 02 Feb 2024 21:35:36 GMT  
		Size: 6.3 MB (6339474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:cf8acb3871d4fc2be67284b888edc3fde2dcd1faa7de3d91fb429f625a148548
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3222416 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cbc8e711b0844a909d2bf0dde5923f6a244e4b467af5b83702b4365f0cd5ae46`

```dockerfile
```

-	Layers:
	-	`sha256:52b67815e60fb7e57bc2cc5e7beeece12b0421cafbc68fd0f227d825c64eb905`  
		Last Modified: Fri, 02 Feb 2024 21:35:36 GMT  
		Size: 3.2 MB (3212470 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:16f5d1318098a94234e645ed896bc814d46398bcd19372992cf9eb46d870c0eb`  
		Last Modified: Fri, 02 Feb 2024 21:35:36 GMT  
		Size: 9.9 KB (9946 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy3.10-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:c03e857000bb199301cd59d02d864eac1acf98170d01f8d0f00a9b6f0b905949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77378477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:338929fb2b4d032f4df89623d5c121cbae5f083691097f5a76ed6cee51f8d49f`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:0e0961062de8ea0706118b883ee7638aae4465761dec06896f1bd28b9fb4b516 in / 
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
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-linux64.tar.bz2'; 			sha256='33c584e9a70a71afd0cb7dd8ba9996720b911b3b8ed0156aea298d4487ad22c3'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-aarch64.tar.bz2'; 			sha256='52146fccaf64e87e71d178dda8de63c01577ec3923073dc69e1519622bcacb74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-linux32.tar.bz2'; 			sha256='75dd58c9abd8b9d78220373148355bc3119febcf27a2c781d64ad85e7232c4aa'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.15-s390x.tar.bz2'; 			sha256='209e57596381e13c9914d1332f359dc4b78de06576739747eb797bdbf85062b8'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
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
	-	`sha256:854acbf4b2df9e625a11c0e67025dce58b41d948bb7e5d4d5e708e25489f6e8f`  
		Last Modified: Wed, 31 Jan 2024 22:44:37 GMT  
		Size: 32.4 MB (32402507 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a15412eda3a60feefe57405e269d0e5038f408b6ad5e5dd5ea87b55948f861a0`  
		Last Modified: Wed, 31 Jan 2024 23:56:44 GMT  
		Size: 875.5 KB (875482 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b8c2539a0992d8cd7d310ffe4f9083b9d4dc856823f489b797eae9489c12668`  
		Last Modified: Wed, 31 Jan 2024 23:56:45 GMT  
		Size: 34.5 MB (34459407 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9f772f0b8b51e559a03a5c469882d623c56260603eab988f7e835251f047030`  
		Last Modified: Wed, 31 Jan 2024 23:56:44 GMT  
		Size: 3.3 MB (3301629 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:84d30353b9f4f36518a3dca31b1bc2bd089bbc0852dd41d310790b6655858576`  
		Last Modified: Thu, 01 Feb 2024 00:59:56 GMT  
		Size: 6.3 MB (6339452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:3f1d645aaae75d1016f5c4556744ac70332cb2dfd0d93de4b9b457c70adb95f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3247694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7dcf9e90d8cdce142bfd141a530c06bd4b108f332a8e39be8902b71858f03d1`

```dockerfile
```

-	Layers:
	-	`sha256:9ab22bf1217ba789db2b1cf892bf6b86b916c3050d8a273e7230933efdd4f63a`  
		Last Modified: Thu, 01 Feb 2024 00:59:56 GMT  
		Size: 3.2 MB (3237842 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:39651642af9b184c367d468349a36f8a80193e05511ef6ec24c5caa80d654095`  
		Last Modified: Thu, 01 Feb 2024 00:59:56 GMT  
		Size: 9.9 KB (9852 bytes)  
		MIME: application/vnd.in-toto+json
