## `hylang:pypy3.9-bullseye`

```console
$ docker pull hylang@sha256:8f1383bcd9a0da7a7a7666f3efa867e17205404282e6a1746d1d67e8c3cedc8b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:pypy3.9-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:74093ca3570ffe7f4c81deb52683e2db41ab645ab1240f10722ce25afa7c0922
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76933486 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:128f696dd8596fe94c2e4039d3acd4a89c47de6b5370c1ca69917c9ae972d085`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:bd961ef3fd78ceb8ce13f43a6b265e2bef640dfff887462b8ceb73a1d4637401 in / 
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
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-linux64.tar.bz2'; 			sha256='f062be307200bde434817e1620cebc13f563d6ab25309442c5f4d0f0d68f0912'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-aarch64.tar.bz2'; 			sha256='03e35fcba290454bb0ccf7ee57fb42d1e63108d10d593776a382c0a2fe355de0'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-linux32.tar.bz2'; 			sha256='c6209380977066c9e8b96e8258821c70f996004ce1bc8659ae83d4fd5a89ff5c'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-s390x.tar.bz2'; 			sha256='deeb5e54c36a0fd9cfefd16e63a0d5bed4f4a43e6bbc01c23f0ed8f7f1c0aaf3'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
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
	-	`sha256:0e0969fcaa8240e1eeb53f9f5d4ddd1bf89a2c9971c9cbe455eba0e66eeefb53`  
		Last Modified: Thu, 11 Jan 2024 02:43:09 GMT  
		Size: 31.4 MB (31417955 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1c220d434f048355c02dce83904afdce51fcb7f65c1b8ad08db617d8e05763c`  
		Last Modified: Tue, 16 Jan 2024 23:55:57 GMT  
		Size: 863.2 KB (863185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31f8e6bee06483599baac80cdb94e7ce83a2175b90b0405c217a8dbb25c467be`  
		Last Modified: Tue, 16 Jan 2024 23:55:58 GMT  
		Size: 37.0 MB (37018307 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0b92020f791628fd6a044d1899dc6d3fe0345131c4b8671537b1f2e71a26b7b6`  
		Last Modified: Tue, 16 Jan 2024 23:55:57 GMT  
		Size: 3.3 MB (3302039 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e264d99ef10e926aa90014cb0ebe1c63edec9818cf3386d04561cbd1dc143799`  
		Last Modified: Wed, 17 Jan 2024 00:48:09 GMT  
		Size: 4.3 MB (4332000 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:43ff91aa7509f0045942f4623c8032abb42f2cd80fe5a4dada08dba9df547da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3240891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c589c0dcb3f07597e7f6596edcbfe480f025c771827543b20903e5b3a8f6bb26`

```dockerfile
```

-	Layers:
	-	`sha256:592a6aac612d7d656b29ac74b9550994c0b33897688a231b0723d64253b987f0`  
		Last Modified: Wed, 17 Jan 2024 00:48:09 GMT  
		Size: 3.2 MB (3232279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:76ae01bb887249bb2fe097f2d97c8683d8bc0503a25b1f152e6f13dfabbc1b5d`  
		Last Modified: Wed, 17 Jan 2024 00:48:09 GMT  
		Size: 8.6 KB (8612 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.9-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:4abccd3e0b4ec6ee5bff51eaff441c1e1eaf025fd3b8f50526caa0eff4d3de56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73179931 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dada0841e44368894fefb9c2512b90de41e81a5d344e13c8f59814faaf909d88`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 25 Dec 2023 11:23:57 GMT
ADD file:cc4e0e6a7b230ab75567cf842e75faa905aeab802405e89a4302d912db6bc5d9 in / 
# Mon, 25 Dec 2023 11:23:57 GMT
CMD ["bash"]
# Mon, 25 Dec 2023 11:23:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Dec 2023 11:23:57 GMT
ENV LANG=C.UTF-8
# Mon, 25 Dec 2023 11:23:57 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Dec 2023 11:23:57 GMT
ENV PYPY_VERSION=7.3.14
# Mon, 25 Dec 2023 11:23:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-linux64.tar.bz2'; 			sha256='febd770a616641ca8419c381c7fb224e515b892551d0db49a1231397ed38859d'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-aarch64.tar.bz2'; 			sha256='14b842f32f60ce2d9d130971f9bcbdb6875824a0e78fac36806d267e0982179c'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-linux32.tar.bz2'; 			sha256='4ad89a22369a6f2f83a7d8d047e0fc4cf5597f0921fa7afa23499ed05f663503'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-s390x.tar.bz2'; 			sha256='ba2451e9081db5bc724a05530a7f98817231de83ff6fdf15bad21a4e9b6dfeae'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 25 Dec 2023 11:23:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 25 Dec 2023 11:23:57 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 25 Dec 2023 11:23:57 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 25 Dec 2023 11:23:57 GMT
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
	-	`sha256:5ae20c369ec182f5275f874054411f9bfb3f8132ff52a9c1d08d4ae15494d01c`  
		Last Modified: Thu, 11 Jan 2024 02:44:48 GMT  
		Size: 30.1 MB (30064010 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bbc69f332518033786bc6e3a7549c0365ae671ea795bd550fb697d4d9e870ae4`  
		Last Modified: Fri, 12 Jan 2024 17:19:00 GMT  
		Size: 850.5 KB (850535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9726b8dd44d23fb92dcf766c2987343bd864a1572d17af8675b0dca80c25d710`  
		Last Modified: Fri, 12 Jan 2024 17:23:20 GMT  
		Size: 34.6 MB (34631689 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd055429a19c0b48b0dc4e9b6c5a3cecad25eb178a1426c143d825e69f621c42`  
		Last Modified: Fri, 12 Jan 2024 17:23:19 GMT  
		Size: 3.3 MB (3301664 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ecd8c393e1bf2af76c14f4f429b2718dcdbae5e535bcb2b01ce0b259d73b7093`  
		Last Modified: Fri, 12 Jan 2024 21:40:44 GMT  
		Size: 4.3 MB (4332033 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:a1f96af51430ba3454deb3e04ffc295bd145d8de3da30311e62966561c5bc4ae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3218842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95da3d36136d35787a4c1ebf703fe69fb7f3db36a243dcbd3d4d83534689ff3b`

```dockerfile
```

-	Layers:
	-	`sha256:e763342029becf763c622df522e45493a3edf936a9d69a0aec15fedf59a94c9d`  
		Last Modified: Fri, 12 Jan 2024 21:40:44 GMT  
		Size: 3.2 MB (3210195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:728c44a712a5b35db02d2780e94af3c5c7e0ed995e72dc214dfb9e5e20e57ac7`  
		Last Modified: Fri, 12 Jan 2024 21:40:44 GMT  
		Size: 8.6 KB (8647 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.9-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:9ad1163a45ba0263dbb55218a3d2f65849f6fe7c66e37c4f3d960b546c62b046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.2 MB (76161500 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df2d47120c1a8d61edb90c8c9837345de461e4b3ea1b376af83f7f6f8717572`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:ed1ce84cc05c621c3311366a5ef8f9ed36bdff95d75ee1564c10e7a20f993b61 in / 
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
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-linux64.tar.bz2'; 			sha256='f062be307200bde434817e1620cebc13f563d6ab25309442c5f4d0f0d68f0912'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-aarch64.tar.bz2'; 			sha256='03e35fcba290454bb0ccf7ee57fb42d1e63108d10d593776a382c0a2fe355de0'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-linux32.tar.bz2'; 			sha256='c6209380977066c9e8b96e8258821c70f996004ce1bc8659ae83d4fd5a89ff5c'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-s390x.tar.bz2'; 			sha256='deeb5e54c36a0fd9cfefd16e63a0d5bed4f4a43e6bbc01c23f0ed8f7f1c0aaf3'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
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
	-	`sha256:d19cbf7b148868960150824d1e6f8ebc5f6d7542a422061491e92178f7db879b`  
		Last Modified: Thu, 11 Jan 2024 02:44:06 GMT  
		Size: 32.4 MB (32402672 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0d611ef1dee079caa5f2e5d5743a68b31f99779bca8e37a5a1cb5f3bd41a154`  
		Last Modified: Tue, 16 Jan 2024 23:55:59 GMT  
		Size: 875.5 KB (875504 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37fd7a41b4b5352b1785b094ccc1649f4b659dfe0f42dfa604ae5457e4556172`  
		Last Modified: Tue, 16 Jan 2024 23:56:00 GMT  
		Size: 35.3 MB (35250044 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b4dd7d893c7b67114dd86072a78ea532791d2302ef75536cc1b95cab4991b8e`  
		Last Modified: Tue, 16 Jan 2024 23:55:59 GMT  
		Size: 3.3 MB (3301495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e800c07b4faa5b2e29ddfc71e2af571c596615db4e9266476625b88ea9dd55`  
		Last Modified: Wed, 17 Jan 2024 00:48:17 GMT  
		Size: 4.3 MB (4331785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:7e4722b615401872ca314486d3a849746bf75ff2465f11ecae645c87880f46dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3244176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:05e2960238534e6487109f99e776abb8ed997549048d6d4e6bec2ab726f45e18`

```dockerfile
```

-	Layers:
	-	`sha256:b41e2472261ba5237c3d5c049dc7c0d57bd7d55856e91bf1e02c827c15275e69`  
		Last Modified: Wed, 17 Jan 2024 00:48:17 GMT  
		Size: 3.2 MB (3235595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:26d57659f91d9c6030c940f27615376f08e75f0e797259e451680de4d5c23b1b`  
		Last Modified: Wed, 17 Jan 2024 00:48:17 GMT  
		Size: 8.6 KB (8581 bytes)  
		MIME: application/vnd.in-toto+json
