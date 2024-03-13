## `hylang:pypy3.10-bookworm`

```console
$ docker pull hylang@sha256:9c2c3955a67801fc5bea80e15d33e3de3950f47984b2b27570b2ef8c43055794
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:pypy3.10-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:55d8ff38b4d3161020e21df25f8296341518cb4d831ba6cd10b07877bf750216
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **79.1 MB (79062444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be99a582ffb1ff67ae6f99f67b5705e0c42aa48322e5b7f5bd35d67e5423ee3b`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
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
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae252ffda1ab4c3263090273a1f4a9992b4d39064fdcd4b4e5697b58f88c862d`  
		Last Modified: Tue, 12 Mar 2024 01:56:34 GMT  
		Size: 3.5 MB (3491099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:937405b7be2f78f7346e5d11e8b808d944b469fae96e23cfce1786a1dd500f2c`  
		Last Modified: Tue, 12 Mar 2024 01:56:35 GMT  
		Size: 36.8 MB (36798738 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39b917a06af1f4583d7981492d99ef2a8e37fe30556d6f77765ffef1ef9343d9`  
		Last Modified: Tue, 12 Mar 2024 01:56:34 GMT  
		Size: 3.3 MB (3307443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af787374c50094b083ee7fbb0b297b70af74bdb73d465049e6aaa6fbc7518b5b`  
		Last Modified: Tue, 12 Mar 2024 02:55:45 GMT  
		Size: 6.3 MB (6340983 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:3805567f03ea08364fd985b64700148d7950c387a8ba0a93f9bdb676ab227eb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3636276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58855d983f60f4b435d8d5c5b5bc684ffd1bdf9622a0c30c3a3a4a6c65b779ae`

```dockerfile
```

-	Layers:
	-	`sha256:718b31b13dea3f57674a2a1db967201532b044347d5e4028e823ed4a7222ec49`  
		Last Modified: Tue, 12 Mar 2024 02:55:44 GMT  
		Size: 3.6 MB (3623929 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a54fe7cb4b085c968dea40298006a0961e57556279107abf0ad5cd67fa9143cc`  
		Last Modified: Tue, 12 Mar 2024 02:55:45 GMT  
		Size: 12.3 KB (12347 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:e05dad68b8abdf26435ed018781099c402dd80ee2fd72f13d9ef59e8da8e759b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76234372 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef0cab7bd5df898ac67b364a88bdfca781e7687f30c80be59addaa859fba2e2`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
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
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcfb93e825a16e0d271c676caebb253ccf356982d58451544200c9f3239de5ad`  
		Last Modified: Wed, 13 Mar 2024 04:14:31 GMT  
		Size: 3.3 MB (3314179 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34eccdf0652845dd9d3ea0d8fdfec0aa842f0f096f368970359737de29112254`  
		Last Modified: Wed, 13 Mar 2024 04:14:32 GMT  
		Size: 34.1 MB (34115217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6979a9a2f3a04b008678010ed6d27094299a9b1640f48254341c152713cf4543`  
		Last Modified: Wed, 13 Mar 2024 04:14:31 GMT  
		Size: 3.3 MB (3307517 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:369ebbcea77dab7784fc93f7cbc4362ae9bec91634f3c1832688c50c9d6099af`  
		Last Modified: Wed, 13 Mar 2024 08:53:55 GMT  
		Size: 6.3 MB (6341025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:d825d4de033649eb48be0f5ea09f444246dab5549c9582754e7c858ae47932e0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3607505 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cefc5849ddbcc55ef41fe7440fd4b52de02936f72905372ea3990dfbe9308c12`

```dockerfile
```

-	Layers:
	-	`sha256:d8b2668238500ed74554b41b2d23f4977fd57ef465761de0e8acb92bd9d7fd2c`  
		Last Modified: Wed, 13 Mar 2024 08:53:54 GMT  
		Size: 3.6 MB (3595100 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2e5be15e10a701a5789ee4f2a62fb4aac917c9f4bfdec3ad35eafa19f869c586`  
		Last Modified: Wed, 13 Mar 2024 08:53:54 GMT  
		Size: 12.4 KB (12405 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.10-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:53395d419d56f528f3e140e1d76cd00d44b1df198a26677125f82387457fee4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75905957 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b64a18b3c3568f9c086bf780ab6a5c6533f072472f439153e6ca84cb392b72d0`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
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
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0c9c445abbd34661b79bef6b18d368c150732337cc87137b908f9a45dff797b`  
		Last Modified: Tue, 12 Mar 2024 01:56:40 GMT  
		Size: 3.5 MB (3496207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d686d6136478970ebad90fcd943682be1cbef7986dcd029261484b1497490e7`  
		Last Modified: Tue, 12 Mar 2024 01:56:40 GMT  
		Size: 32.6 MB (32619553 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:99ee48f5524a61d90356abf428f09d9be96d27a1dd7928b5c73be6758f303665`  
		Last Modified: Tue, 12 Mar 2024 01:56:40 GMT  
		Size: 3.3 MB (3307273 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:28b2f8ee0b3d36c18b855fa92b4bfcd7f01ad3af62b26c7a621930aeb80b820b`  
		Last Modified: Tue, 12 Mar 2024 02:55:51 GMT  
		Size: 6.3 MB (6341051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:4e5d438a8bf5785a922b3a84fb9e61cd338dc1619298cf0694aade333c732593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.6 MB (3630040 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:04d3706a56bca9ebc0669cad5d648132d86926d5c1eb15bc09741e6a8f51ae3d`

```dockerfile
```

-	Layers:
	-	`sha256:0c389bd4e1018c225b5585a4fad1afb53d9eb46fd798854b19d6d41dd5abbcc7`  
		Last Modified: Tue, 12 Mar 2024 02:55:51 GMT  
		Size: 3.6 MB (3617786 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:686533193d5917067d174d488939fdd7a5b8174e45908cd973196f04288aecb4`  
		Last Modified: Tue, 12 Mar 2024 02:55:51 GMT  
		Size: 12.3 KB (12254 bytes)  
		MIME: application/vnd.in-toto+json
