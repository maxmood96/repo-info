## `hylang:0-pypy3.9-bookworm`

```console
$ docker pull hylang@sha256:36e009e1b0bff9f434fbb5a178b4a551f6124bc9dda04b3feeccae4a4c0809bc
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

### `hylang:0-pypy3.9-bookworm` - unknown; unknown

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

### `hylang:0-pypy3.9-bookworm` - linux; arm64 variant v8

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

### `hylang:0-pypy3.9-bookworm` - unknown; unknown

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

### `hylang:0-pypy3.9-bookworm` - linux; 386

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

### `hylang:0-pypy3.9-bookworm` - unknown; unknown

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
