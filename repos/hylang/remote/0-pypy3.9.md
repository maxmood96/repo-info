## `hylang:0-pypy3.9`

```console
$ docker pull hylang@sha256:aafb47060445618fdd949db88535b52270cb0f98bbae7ccf711635a5e26d2fa8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.20348.2227; amd64
	-	windows version 10.0.17763.5329; amd64

### `hylang:0-pypy3.9` - linux; amd64

```console
$ docker pull hylang@sha256:71648cff3abf6b826bc3e47f8ff747e8086f137e0965ab069a55a7819acaeeea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.7 MB (77653779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c8f3b142c5847128cdad7d68d640da44a6e8efca44732b13ab88614deb982e7d`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:af0f4e41d68b67ca88a1ce6297326159e18e27670d7bfc0bf5804a4e2b268cc8 in / 
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
	-	`sha256:c57ee5000d61345aa3ee6684794a8110328e2274d9a5ae7855969d1a26394463`  
		Last Modified: Wed, 31 Jan 2024 22:39:55 GMT  
		Size: 29.2 MB (29150465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca4263b737353ac11a48b6951205ee32d7aadb5f76053126bb54f370fc4188ae`  
		Last Modified: Wed, 31 Jan 2024 23:56:49 GMT  
		Size: 3.3 MB (3299193 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b5b93dd363976677a08c886b6f19d7386a4c079902712914c22598c51339533e`  
		Last Modified: Wed, 31 Jan 2024 23:56:49 GMT  
		Size: 37.6 MB (37565616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46c4f710d32b265d15bd240101d677ab5a37fc3bd5d0821ee735b28502931258`  
		Last Modified: Wed, 31 Jan 2024 23:56:49 GMT  
		Size: 3.3 MB (3306666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c57ff505cabf27971db4b3823e028a058bd9536ca90f7a5239b86e841d8792c`  
		Last Modified: Thu, 01 Feb 2024 01:01:49 GMT  
		Size: 4.3 MB (4331839 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:91a8031f5da4a11a3ad6c413f2096da68f6efce5e8d7dc8ca97c82b0f79a89c2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3158440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1df3511eb8a01b05ff1aa3500a8c8e31a2043c1832b17229d1cbdea259e58fe3`

```dockerfile
```

-	Layers:
	-	`sha256:175b44ac1faebd42f295ddd5490b506c21d5dd7ddb815a796dbdea35ea871aee`  
		Last Modified: Thu, 01 Feb 2024 01:01:49 GMT  
		Size: 3.1 MB (3148596 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f58100b5c32d65f15317156af83a7882d2f1180db9e7cf9df741ee8eb003013b`  
		Last Modified: Thu, 01 Feb 2024 01:01:48 GMT  
		Size: 9.8 KB (9844 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy3.9` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:d319fccc6f22dbacd88cf1347bc5def97684612777817465e6b0f22298413dcd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.9 MB (74852600 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eaa7326496f311fe507619ce4402137cf19b82cd40c10b5a0cebf177aeabf46`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
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
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d72751968e6b6313c75b348364b838e9bc7179ddc497de0f3145cc747d08c16`  
		Last Modified: Thu, 01 Feb 2024 20:33:09 GMT  
		Size: 3.1 MB (3122086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6c46872b104643701c2b18172152bea45c2fe7b0b57c5f9efd1ff36935c08abb`  
		Last Modified: Thu, 01 Feb 2024 20:35:27 GMT  
		Size: 34.9 MB (34910944 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:052e4b42ac41f53927c2bcc79b9893e8c28234b5bf7ec5123a2a196abf761bd1`  
		Last Modified: Thu, 01 Feb 2024 20:35:26 GMT  
		Size: 3.3 MB (3306608 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1955c277463d5634348bc311b5b8d0e39e0595c0453961c75c0f894dd1bf6672`  
		Last Modified: Fri, 02 Feb 2024 21:36:35 GMT  
		Size: 4.3 MB (4332130 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:3f17e1817ca6043ab0fd1b62e647043a43ee6d4550274d2794472c192c9c840b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.1 MB (3133665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c2735f0ed5d9ecad488874157d8a46780a4c13318688b9e35574b18a7a782036`

```dockerfile
```

-	Layers:
	-	`sha256:6727d90ebeb49bc08bc20331bebc2a93e88638de1206dd7a9478203ddcb56d40`  
		Last Modified: Fri, 02 Feb 2024 21:36:35 GMT  
		Size: 3.1 MB (3123779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:637b77b92b10beeabbf1729a3763f1a00682abd3688f81149e795ccd83e4d2e3`  
		Last Modified: Fri, 02 Feb 2024 21:36:34 GMT  
		Size: 9.9 KB (9886 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy3.9` - linux; 386

```console
$ docker pull hylang@sha256:54c913aae7449b9dd768d093348c694c02fbc6ea4588b98e239c233b7913160d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74518198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b1405a57d92869d6bb00d1b648a37efd675d6d643b914ecd1d0c8c747318914`
-	Default Command: `["hy"]`

```dockerfile
# Fri, 05 Jan 2024 23:20:01 GMT
ADD file:540e2de73452bd162dd7f630bf29f60e7d2e4a7a5d32a495bedf8ad390b59d7f in / 
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
	-	`sha256:34ef135b45f33052e8e5bca668f9a45a938944a9cf3fb73a46f54a7bf11f091b`  
		Last Modified: Wed, 31 Jan 2024 22:43:46 GMT  
		Size: 30.2 MB (30165018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56afbdc661ec40cc7c6d91eb59a70704499b502ebf37fa7f999234a8463fa80c`  
		Last Modified: Wed, 31 Jan 2024 23:56:58 GMT  
		Size: 3.3 MB (3304741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee05a7823ccdadafda8740a194ec1fbfadca6d9fd2fd49f42022034abdeb6091`  
		Last Modified: Wed, 31 Jan 2024 23:56:59 GMT  
		Size: 33.4 MB (33410024 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:739268a567f8b54de2af612e3af41b4bdab2ac6f3d92045df41725bac097183d`  
		Last Modified: Wed, 31 Jan 2024 23:56:58 GMT  
		Size: 3.3 MB (3306422 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5695ce71f82c714055daaa2936a713699c2def4ae7f0ec5665619e7361ef6a68`  
		Last Modified: Thu, 01 Feb 2024 01:00:11 GMT  
		Size: 4.3 MB (4331993 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:3024295699510c215e42616a4bea8f3cf1ca0fabfe40c7f6fd6f08b22538ca01
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3152708 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716073f472ef0a2a83e15ac566aabfa170be7dfeb9577d05d701bbccd7886eb6`

```dockerfile
```

-	Layers:
	-	`sha256:3adea2e510bf9384466b2069c29ed2852ea365abde3921f9b0e8ace0bfef87eb`  
		Last Modified: Thu, 01 Feb 2024 01:00:11 GMT  
		Size: 3.1 MB (3142917 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2a94d9eee1b186c4a370693e6fec47a44c7ab61ad5a90888d507dbad1263e970`  
		Last Modified: Thu, 01 Feb 2024 01:00:11 GMT  
		Size: 9.8 KB (9791 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy3.9` - windows version 10.0.20348.2227; amd64

```console
$ docker pull hylang@sha256:f9f028945747aa97c4a54fe4932c6fd72f702be9dd06aa6f0cc9f42ce12b9a46
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (1952908783 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd18b11e3efdaaa008deda33f1dc68f455298530e759c98f8cab20fdd44ab3d2`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Tue, 16 Jan 2024 23:58:45 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 16 Jan 2024 23:58:53 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 16 Jan 2024 23:59:02 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 16 Jan 2024 23:59:03 GMT
ENV PYPY_VERSION=7.3.15
# Tue, 16 Jan 2024 23:59:21 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.9-v7.3.15-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a156dad8b58570597eaaabe05663f00f80c60bc11df4a9c46d0953b6c5eb9209'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.9-v7.3.15-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 16 Jan 2024 23:59:22 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 16 Jan 2024 23:59:23 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 16 Jan 2024 23:59:44 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 16 Jan 2024 23:59:45 GMT
CMD ["pypy"]
# Wed, 17 Jan 2024 00:55:15 GMT
ENV HY_VERSION=0.28.0
# Wed, 17 Jan 2024 00:55:16 GMT
ENV HYRULE_VERSION=0.5.0
# Wed, 17 Jan 2024 00:56:14 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 17 Jan 2024 00:56:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:7c76e5cf7755ce357ffb737715b0da6799a50ea468cc252c094f4d915d426b3f`  
		Last Modified: Tue, 13 Jun 2023 17:55:32 GMT  
		Size: 1.4 GB (1388598786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a97a84f9ecb04e6f34ca7d17667bf0abbd83ea39301725226a2352330b4402d3`  
		Last Modified: Tue, 09 Jan 2024 18:44:13 GMT  
		Size: 511.6 MB (511613854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e00452a1070e759d3ca4a95365e16bb1867c3cdcf57d82a438d5867ee6a847c5`  
		Last Modified: Tue, 16 Jan 2024 23:59:52 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce886381b02044e8a1d042bbb847c1c5456f13b1f58f091f417b0a3521639d6a`  
		Last Modified: Tue, 16 Jan 2024 23:59:52 GMT  
		Size: 488.1 KB (488058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a62a464dabb74f7529295c33fd2895d91f3719881b048029c4ca340979cd2e4`  
		Last Modified: Tue, 16 Jan 2024 23:59:53 GMT  
		Size: 15.5 MB (15540472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d79be8cdb064c3b9b386c999bb6a75b31033dad9ec54609e9bc42a09821f0cc4`  
		Last Modified: Tue, 16 Jan 2024 23:59:52 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:235ad6a5eee9f35e68492928da0a4ac2fdd61ce56a3f3cbbda1acbf7a5089bfa`  
		Last Modified: Tue, 16 Jan 2024 23:59:53 GMT  
		Size: 27.6 MB (27581903 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8667f2296339db4bf0d6500528ba7d6794b89bc789544981a27b5f98a717a41c`  
		Last Modified: Tue, 16 Jan 2024 23:59:49 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deda35a3ee78c246c968826f259491972c91005322cf1f1f7b1ab00cbe054790`  
		Last Modified: Tue, 16 Jan 2024 23:59:49 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:516ebcdae6507a6b5cc2e9d0d57f17e6c23a2c1d61eeb85e971073eba593405c`  
		Last Modified: Tue, 16 Jan 2024 23:59:50 GMT  
		Size: 3.9 MB (3927342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:600601f226b87dc441e6b11a6385c92bfac2645d74bb56e1c67957e91025160f`  
		Last Modified: Tue, 16 Jan 2024 23:59:49 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14442a82a872a78b2d64bb01c21d9ffefbd022b247393209871138124fefa8c1`  
		Last Modified: Wed, 17 Jan 2024 00:56:19 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aed3a9c9d56bbfc476920e5b8b69b9419c7478166c39a09950f4fbe86d54ab6`  
		Last Modified: Wed, 17 Jan 2024 00:56:18 GMT  
		Size: 1.4 KB (1396 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92f673b0108cad70f1dcedacaa687f8ccb9e119efaea9b83e3a09750f0cf7757`  
		Last Modified: Wed, 17 Jan 2024 00:56:20 GMT  
		Size: 5.1 MB (5147824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26f3c35c7dc66d540e9442b2d33515158126f41deba9fd1b02414cec22f0cdb4`  
		Last Modified: Wed, 17 Jan 2024 00:56:19 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:0-pypy3.9` - windows version 10.0.17763.5329; amd64

```console
$ docker pull hylang@sha256:1c8d36421f2de7c9d1f2def25439dc37457c6929d10b0f6fd70c2b25cbcc31ac
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2122340127 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cafa1d85ddbb21efb968f204950eb41f11c4f8c1a4d62517bd0243bf0727652e`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 17 Jan 2024 00:18:38 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 17 Jan 2024 00:20:29 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 17 Jan 2024 00:21:03 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 17 Jan 2024 00:21:04 GMT
ENV PYPY_VERSION=7.3.15
# Wed, 17 Jan 2024 00:21:44 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.9-v7.3.15-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a156dad8b58570597eaaabe05663f00f80c60bc11df4a9c46d0953b6c5eb9209'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.9-v7.3.15-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 17 Jan 2024 00:21:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 17 Jan 2024 00:21:46 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 17 Jan 2024 00:22:25 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 17 Jan 2024 00:22:26 GMT
CMD ["pypy"]
# Wed, 17 Jan 2024 00:56:21 GMT
ENV HY_VERSION=0.28.0
# Wed, 17 Jan 2024 00:56:23 GMT
ENV HYRULE_VERSION=0.5.0
# Wed, 17 Jan 2024 00:57:58 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 17 Jan 2024 00:57:59 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c9226d61d3bdbf9f09821b32f5878623b8daaa5fb4f875cb63c199f87a26d57e`  
		Last Modified: Tue, 13 Jun 2023 18:25:35 GMT  
		Size: 1.7 GB (1650620357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9da94e8356538054b9b2e3023814100ffe07d42ee8f8dec0ad82a450371abd52`  
		Last Modified: Tue, 09 Jan 2024 18:22:46 GMT  
		Size: 419.1 MB (419102156 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0392cf644bf5d4e63b9d2d7fd94df9f0a8a49ce69c277eeee3eee89199a3603`  
		Last Modified: Wed, 17 Jan 2024 00:22:31 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d72e853e0f55db9c7c0d13571981b2b79197f3884322a3902726da6535967eaf`  
		Last Modified: Wed, 17 Jan 2024 00:22:30 GMT  
		Size: 493.6 KB (493619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd4153db4b7b6edbe0e906c46fa6278aa361cbdd1d7871a559025091a2ab9163`  
		Last Modified: Wed, 17 Jan 2024 00:22:31 GMT  
		Size: 15.5 MB (15522902 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e393f1bf90954fcc5cf96f4fb93a7cd1043eb72a2bbfc48a207a71146a81c0c`  
		Last Modified: Wed, 17 Jan 2024 00:22:30 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87e197778f307375a523c988848f35d122221e4a6a56a999031831b07e8fcb35`  
		Last Modified: Wed, 17 Jan 2024 00:22:33 GMT  
		Size: 27.6 MB (27576958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc18a5899caf6fbf9bd254b94eb7d22a813accd9dea719cb79d042b9515c2492`  
		Last Modified: Wed, 17 Jan 2024 00:22:29 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50bc2cd79bc24841db6d3e00645aadc2f3e525c44064ac9e8e08b07929f8b20`  
		Last Modified: Wed, 17 Jan 2024 00:22:29 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1959bdff94d59a0f731cddba8887d5449433a9cdbd14cdb111d71b83521572`  
		Last Modified: Wed, 17 Jan 2024 00:22:30 GMT  
		Size: 3.9 MB (3916896 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c2425a6940a1592bc6497a101c69be666b495c6ae7966c20b407d703a67bf17`  
		Last Modified: Wed, 17 Jan 2024 00:22:29 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd611c331385fd4e121ed33022d28ee079155cbf7ee3b654ce2c023346a88419`  
		Last Modified: Wed, 17 Jan 2024 00:58:03 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9474e91fe787aace25e1dbbb010009300b996b2fd756153e69a9dda9d385dd38`  
		Last Modified: Wed, 17 Jan 2024 00:58:03 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:649a5f5a2dfa64abfdc275f26d5e3e1be6248cf20313c94656af0ba44475f873`  
		Last Modified: Wed, 17 Jan 2024 00:58:04 GMT  
		Size: 5.1 MB (5096819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02d84ea02a1af2d5bcd107d7a905c0f81a21e282496d7381ad61c7b610df0eb1`  
		Last Modified: Wed, 17 Jan 2024 00:58:03 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
