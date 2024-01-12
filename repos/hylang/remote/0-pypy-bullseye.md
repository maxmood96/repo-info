## `hylang:0-pypy-bullseye`

```console
$ docker pull hylang@sha256:4c2068cce5c0b9382911df3a36a7043bd3fc1a3b5d2355745532f84db1bb6839
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:0-pypy-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:16ba77b60709fcc4e77d40f576dd068de0ae205c4d8ba152df742d7f2caa19b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.2 MB (78163104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5546414cc5a848d8e468d3ef1218d6d0ff8adc8181f27a1d320049740e7ca49e`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 25 Dec 2023 11:12:03 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
# Mon, 25 Dec 2023 11:12:03 GMT
CMD ["bash"]
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV LANG=C.UTF-8
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYPY_VERSION=7.3.14
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux64.tar.bz2'; 			sha256='a83879891dc0a6c1504da0954fba1125b21a2591782897231a8168100ea72b94'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-aarch64.tar.bz2'; 			sha256='fbef65dfc69dcd6006d843553d268b331f1b13dfc3938492bd35f0f477b5bcf4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux32.tar.bz2'; 			sha256='d37e7c7a03bed5dceca2ab7f821ad7655808cccf6908155f78f0effd811b7f4f'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-s390x.tar.bz2'; 			sha256='363e87ad3b6547cc68981c665cf049449bed44cf9e49cabbbcc61df73ea2d40b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
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
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7245419d8299d9369bfe75def6511afab5be9bac88c28ccf3d0a9705b735698`  
		Last Modified: Fri, 12 Jan 2024 00:39:51 GMT  
		Size: 863.2 KB (863186 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cda7041d652d83c044037cf65b6316c3c48853a95eae8c5077f227d006af6843`  
		Last Modified: Fri, 12 Jan 2024 00:39:52 GMT  
		Size: 36.2 MB (36240628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87105b9afea894a8fc6e70eaed4229dae72e8cafe652f1542631d8ed6f7ccd5d`  
		Last Modified: Fri, 12 Jan 2024 00:39:51 GMT  
		Size: 3.3 MB (3301905 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4704b8c6f10407b09a39bc781fd476ab4c688022632ef6e01d277dd32abc346d`  
		Last Modified: Fri, 12 Jan 2024 00:57:46 GMT  
		Size: 6.3 MB (6339430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:89f5bb14c7504c2605e2a9c5d8db3b2b6321539300275379e7d70eaa51dd7ede
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3243495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e76742db9ccc72e8248577a9e2b3072eec8c03e6cbe19b83d24a47741ed7a2d`

```dockerfile
```

-	Layers:
	-	`sha256:8aa61f94f9797b72ff3685e9f2d153f2b683795c6d71c49043dd1f6fe3103100`  
		Last Modified: Fri, 12 Jan 2024 00:57:45 GMT  
		Size: 3.2 MB (3233591 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:08b3e5ef4799f804c366e3be182d484e9c29fbaa79f08351feb7e1cac9eebbc2`  
		Last Modified: Fri, 12 Jan 2024 00:57:46 GMT  
		Size: 9.9 KB (9904 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:5ac01b7b40d35053efc87a7fb8d43d174e042f5376426b16ed52f3d581fe2c89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74417083 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c86bff33ee13b7e97456effbba8fd32af6de79f0ab35f6f062f87950d1faffef`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 19 Dec 2023 01:41:25 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 19 Dec 2023 01:41:25 GMT
CMD ["bash"]
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV LANG=C.UTF-8
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYPY_VERSION=7.3.14
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux64.tar.bz2'; 			sha256='a83879891dc0a6c1504da0954fba1125b21a2591782897231a8168100ea72b94'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-aarch64.tar.bz2'; 			sha256='fbef65dfc69dcd6006d843553d268b331f1b13dfc3938492bd35f0f477b5bcf4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux32.tar.bz2'; 			sha256='d37e7c7a03bed5dceca2ab7f821ad7655808cccf6908155f78f0effd811b7f4f'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-s390x.tar.bz2'; 			sha256='363e87ad3b6547cc68981c665cf049449bed44cf9e49cabbbcc61df73ea2d40b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
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
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420960ab036904ce670019905624e65cd0a2badab83d0a7c934820a784f459c9`  
		Last Modified: Fri, 05 Jan 2024 19:28:29 GMT  
		Size: 850.6 KB (850551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1a7212fe75cc995400db83106e053c1da8b82ec6cfdc488c7af1eef6a82e934d`  
		Last Modified: Fri, 05 Jan 2024 19:28:30 GMT  
		Size: 33.9 MB (33861079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcb9251b8fdbc9a8a02af15bb995c3d257b9b6a1d2b3dd4ef0b57a1f482fe2c5`  
		Last Modified: Fri, 05 Jan 2024 19:28:29 GMT  
		Size: 3.3 MB (3301727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0c16596c09f852039c1a9f18713b5532ff9e8f3fc54780b27de1adb056180d7`  
		Last Modified: Sat, 06 Jan 2024 04:02:51 GMT  
		Size: 6.3 MB (6339674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:0aae734a038c3c8b6b10f8fcaa5373adc0eee27b6538695de3be37e6350056df
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3220820 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8836b6edd58f64482ef11382488f54ec5940829e15b59ce4ae4839c06d68e4f`

```dockerfile
```

-	Layers:
	-	`sha256:6f65b613c37f0a643d05eeb8c0b070bda04de65815620571549d363e1f82a736`  
		Last Modified: Sat, 06 Jan 2024 04:02:51 GMT  
		Size: 3.2 MB (3211515 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f87e8af51e636e08f2240c2367c3e1134ec01e79b550af4f56c01d47e2fabecb`  
		Last Modified: Sat, 06 Jan 2024 04:02:50 GMT  
		Size: 9.3 KB (9305 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:6e031995876e982de508a326f3aff150bfe6ff3f99838aa629e19b8ad0dd43a7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.4 MB (77373126 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10ca1db7cb5dabdcf3c58ff242dda586a290699b4f8098cc5420b749aa5f3951`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 25 Dec 2023 11:12:03 GMT
ADD file:ed1ce84cc05c621c3311366a5ef8f9ed36bdff95d75ee1564c10e7a20f993b61 in / 
# Mon, 25 Dec 2023 11:12:03 GMT
CMD ["bash"]
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV LANG=C.UTF-8
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYPY_VERSION=7.3.14
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux64.tar.bz2'; 			sha256='a83879891dc0a6c1504da0954fba1125b21a2591782897231a8168100ea72b94'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-aarch64.tar.bz2'; 			sha256='fbef65dfc69dcd6006d843553d268b331f1b13dfc3938492bd35f0f477b5bcf4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux32.tar.bz2'; 			sha256='d37e7c7a03bed5dceca2ab7f821ad7655808cccf6908155f78f0effd811b7f4f'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-s390x.tar.bz2'; 			sha256='363e87ad3b6547cc68981c665cf049449bed44cf9e49cabbbcc61df73ea2d40b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
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
	-	`sha256:d19cbf7b148868960150824d1e6f8ebc5f6d7542a422061491e92178f7db879b`  
		Last Modified: Thu, 11 Jan 2024 02:44:06 GMT  
		Size: 32.4 MB (32402672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:060478fe5adfe7f08c42740bdb3b06520003e78cc7e0ad9c72daa7815e0df3b5`  
		Last Modified: Fri, 12 Jan 2024 00:40:48 GMT  
		Size: 875.5 KB (875476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:544081ae373f6dc17ece894352ca42f82c4b32f827dfa03716de291978f01245`  
		Last Modified: Fri, 12 Jan 2024 00:40:49 GMT  
		Size: 34.5 MB (34454034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf333c0a0c387c690ad919c466638d4064bf51dd58a21641839428698e5f77a8`  
		Last Modified: Fri, 12 Jan 2024 00:40:48 GMT  
		Size: 3.3 MB (3301526 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93c908043d1484e6372316741bf8252141c0c2aeb03f274bd64298c943fdf2b8`  
		Last Modified: Fri, 12 Jan 2024 00:57:27 GMT  
		Size: 6.3 MB (6339418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:b859233e9d48d5a5c1af0d4b1314eed83d4302b5d2319eb15bb30dc0eeeb0ffa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3246739 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8404ad4714c3ec390e2982361bffa74432cbce1830d66467630b32a3d111dd32`

```dockerfile
```

-	Layers:
	-	`sha256:d962779ff5938a6022eea8161de147be6fb67bb9ec433afae3137bb428ed4ea9`  
		Last Modified: Fri, 12 Jan 2024 00:57:27 GMT  
		Size: 3.2 MB (3236887 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55570eea61a4cd3e36271e1a1b70f3dd463005d00ce3d2bcfc475691ca733bee`  
		Last Modified: Fri, 12 Jan 2024 00:57:27 GMT  
		Size: 9.9 KB (9852 bytes)  
		MIME: application/vnd.in-toto+json
