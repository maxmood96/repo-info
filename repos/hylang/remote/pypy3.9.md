## `hylang:pypy3.9`

```console
$ docker pull hylang@sha256:fa2abc9295dac8d966aecfb7a2829e127a9b24f4ae9d705ec2973a921df76783
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
$ docker pull hylang@sha256:beedbfb4c3a01fe3aa2a3cf36c28efca8b6679d4a3bfff942d0f62b6486756fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71898080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fefd659fd0b405896421338aaf4e4833e055caa48a6875595bf45019dcf84c3c`
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
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-linux64.tar.bz2'; 			sha256='f062be307200bde434817e1620cebc13f563d6ab25309442c5f4d0f0d68f0912'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-aarch64.tar.bz2'; 			sha256='03e35fcba290454bb0ccf7ee57fb42d1e63108d10d593776a382c0a2fe355de0'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-linux32.tar.bz2'; 			sha256='c6209380977066c9e8b96e8258821c70f996004ce1bc8659ae83d4fd5a89ff5c'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-s390x.tar.bz2'; 			sha256='deeb5e54c36a0fd9cfefd16e63a0d5bed4f4a43e6bbc01c23f0ed8f7f1c0aaf3'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
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
	-	`sha256:55a0cb2a12fe8ba7bf76d543adac03c016e1c2e16eced289d8466c18b57f7f4d`  
		Last Modified: Wed, 10 Apr 2024 02:55:53 GMT  
		Size: 3.5 MB (3491132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a6e19ada42539e8cfdd7850ca46a4f9cd7c6daca8d289877248a420b1cdc13e5`  
		Last Modified: Wed, 10 Apr 2024 02:55:53 GMT  
		Size: 31.6 MB (31642264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c06e6c558d15b533d066f4f321a2b6fa9817a0198edc87bba1e9a5030837882c`  
		Last Modified: Wed, 10 Apr 2024 02:55:53 GMT  
		Size: 3.3 MB (3299921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e6020b534f51f2fcd688496154c0e22e600c00c3839b1ebc508eb6cc9420b83`  
		Last Modified: Wed, 10 Apr 2024 03:54:03 GMT  
		Size: 4.3 MB (4333405 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:c2267c204332c67a43e9a1b9345f7f1c5beae3d860b2be93d1c78f04db4f16e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377474 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8dccc6d265d1054a6b4f1f5d6095ca6461812d604947a61aac0f9499c5c726e`

```dockerfile
```

-	Layers:
	-	`sha256:e1aeb4016dfe6bce848c8bef2adb6bac25f9697947164ce42547ba9bc499c996`  
		Last Modified: Wed, 10 Apr 2024 03:54:03 GMT  
		Size: 2.4 MB (2367631 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a9bdf1c4a0180b00936a14814743270c3fb311c1deeb7c8bcced7e2361efb1a0`  
		Last Modified: Wed, 10 Apr 2024 03:54:03 GMT  
		Size: 9.8 KB (9843 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.9` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:1e1c9bbe6a55cb403540c9b986ae7b23f3e398d9b37faa7928d30e1df2ef5d28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.1 MB (70084434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a216422a353387e255ab61d208524b5fcae63b29bd0dd51b6f024175236defe`
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
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-linux64.tar.bz2'; 			sha256='f062be307200bde434817e1620cebc13f563d6ab25309442c5f4d0f0d68f0912'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-aarch64.tar.bz2'; 			sha256='03e35fcba290454bb0ccf7ee57fb42d1e63108d10d593776a382c0a2fe355de0'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-linux32.tar.bz2'; 			sha256='c6209380977066c9e8b96e8258821c70f996004ce1bc8659ae83d4fd5a89ff5c'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-s390x.tar.bz2'; 			sha256='deeb5e54c36a0fd9cfefd16e63a0d5bed4f4a43e6bbc01c23f0ed8f7f1c0aaf3'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
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
	-	`sha256:3f9660a12dcc60a089d80115e5b600532b8e654c96c749eebdc21591f33bffda`  
		Last Modified: Wed, 10 Apr 2024 20:39:47 GMT  
		Size: 30.0 MB (29974622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fd14679be1a6bf487698d1fdc5f34be7bf8f527695a0e3710464704ff977a99`  
		Last Modified: Wed, 10 Apr 2024 20:39:46 GMT  
		Size: 3.3 MB (3300051 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bacb539b8e05d5afe86991908cf7f9bd58c514d03ded08f75c70952c29c6bd1b`  
		Last Modified: Thu, 11 Apr 2024 10:19:20 GMT  
		Size: 4.3 MB (4333388 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:272f9219c038a968bead0514ff490980125e03fb39c116f364c46c21a2ee9da9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2377738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b8432c956d7d643bd905d6095618930912caa04bd9a2c51e9b91d84c1ba3cf38`

```dockerfile
```

-	Layers:
	-	`sha256:33495c1bbb6fbbb27c0e2dabfe7264a02bf31a8649c22c59fdbb4e9c96f010f1`  
		Last Modified: Thu, 11 Apr 2024 10:19:20 GMT  
		Size: 2.4 MB (2367852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cbcd88cb5e27a42ea72496f3638dc3f8d197ed5c1611c035bb53db24ae0976e9`  
		Last Modified: Thu, 11 Apr 2024 10:19:19 GMT  
		Size: 9.9 KB (9886 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.9` - linux; 386

```console
$ docker pull hylang@sha256:f27f28e76b962f89380b93e58ed39f80af96663d07fc19196b3d4e94eb7ce75b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69302104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c2b9e583ea5e2bc0e5fb657095c7b6a94341f2f42f505fe33e58be25306bf9`
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
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-linux64.tar.bz2'; 			sha256='f062be307200bde434817e1620cebc13f563d6ab25309442c5f4d0f0d68f0912'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-aarch64.tar.bz2'; 			sha256='03e35fcba290454bb0ccf7ee57fb42d1e63108d10d593776a382c0a2fe355de0'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-linux32.tar.bz2'; 			sha256='c6209380977066c9e8b96e8258821c70f996004ce1bc8659ae83d4fd5a89ff5c'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.15-s390x.tar.bz2'; 			sha256='deeb5e54c36a0fd9cfefd16e63a0d5bed4f4a43e6bbc01c23f0ed8f7f1c0aaf3'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
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
	-	`sha256:78428cc100261823d9bf3b76ec552d37f85bcbaa345f0e6e5f40770c05e6878a`  
		Last Modified: Wed, 10 Apr 2024 01:54:03 GMT  
		Size: 3.5 MB (3496176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69ae937da9d10aeb77ed8c43e17fe700959c4ef1f201176a2fc65973a78e0981`  
		Last Modified: Wed, 10 Apr 2024 01:54:03 GMT  
		Size: 28.0 MB (28026600 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152a3e85209d47fbaaf1656f0e2f304505d7c4af3e930a3d824137dfbf9f4311`  
		Last Modified: Wed, 10 Apr 2024 01:54:03 GMT  
		Size: 3.3 MB (3299579 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f015fc5d0e1103c78b5c4e90e75c464fa24ff3e6866b9d3de544ebf381bff795`  
		Last Modified: Wed, 10 Apr 2024 02:56:58 GMT  
		Size: 4.3 MB (4333234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.9` - unknown; unknown

```console
$ docker pull hylang@sha256:2110ae5aa402380ab02ccff767317b096f56014dad4e4970fa4c89fb0905950a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2374539 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3db47e7792552b340fcb2e3e0930d3f6a80514cade1d78e03b7a925c9bb6242`

```dockerfile
```

-	Layers:
	-	`sha256:324d4e06380b8d6c684c48e06a1c635a7f1bdbc3a935b5be6e874cb3e190eba6`  
		Last Modified: Wed, 10 Apr 2024 02:56:58 GMT  
		Size: 2.4 MB (2364747 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:117f466e58ecc0f9fc126e69ee2b6227e3b6d907fbbfd1dcffe8eba9ef180899`  
		Last Modified: Wed, 10 Apr 2024 02:56:58 GMT  
		Size: 9.8 KB (9792 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.9` - windows version 10.0.20348.2402; amd64

```console
$ docker pull hylang@sha256:14f7b8087955a35de6bbdca5233767f6b9a3b403743b87e59ee316a599e3038b
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2052017203 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:404904604cda2c0bfc020edf71d233310dfb2d758ff5832aa8bba309182e3a8a`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Fri, 05 Apr 2024 09:25:01 GMT
RUN Install update 10.0.20348.2402
# Tue, 09 Apr 2024 23:59:21 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Apr 2024 23:59:34 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 09 Apr 2024 23:59:48 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 09 Apr 2024 23:59:49 GMT
ENV PYPY_VERSION=7.3.15
# Wed, 10 Apr 2024 00:00:09 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.9-v7.3.15-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a156dad8b58570597eaaabe05663f00f80c60bc11df4a9c46d0953b6c5eb9209'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.9-v7.3.15-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 10 Apr 2024 00:00:10 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 10 Apr 2024 00:00:11 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 10 Apr 2024 00:00:34 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 10 Apr 2024 00:00:35 GMT
CMD ["pypy"]
# Wed, 10 Apr 2024 00:59:29 GMT
ENV HY_VERSION=0.28.0
# Wed, 10 Apr 2024 00:59:30 GMT
ENV HYRULE_VERSION=0.5.0
# Wed, 10 Apr 2024 01:00:25 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 10 Apr 2024 01:00:26 GMT
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
	-	`sha256:4c69ff7537838a12fa4b06949622624b26d2492574ff580a336767944f6078f0`  
		Last Modified: Wed, 10 Apr 2024 00:00:44 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5faf1e884f3ffb04ee81ee0b35a6f48f57798bed5a876a6715662470538eb861`  
		Last Modified: Wed, 10 Apr 2024 00:00:42 GMT  
		Size: 482.7 KB (482663 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22bc8574523d71bc8f2b9e34a56c6ef37abb37406bfcfa1165ac43940d566846`  
		Last Modified: Wed, 10 Apr 2024 00:00:43 GMT  
		Size: 15.5 MB (15532222 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b9b249b060d7a9713094ef98d57fcb51dff842eaca79d2f63536dd107f482b`  
		Last Modified: Wed, 10 Apr 2024 00:00:41 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5088c4eeac6d5d707a7628497198f7d5aa127584a91c46b07c7ace2ea83c4415`  
		Last Modified: Wed, 10 Apr 2024 00:00:43 GMT  
		Size: 27.6 MB (27565242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ededbebc0478fb9789ee09703d567d31cd8a9de06be40928a860bfe77fd067`  
		Last Modified: Wed, 10 Apr 2024 00:00:39 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33378418ef1be2dbc5eb47af4cb5455174cd4079307b99a178b250c898579447`  
		Last Modified: Wed, 10 Apr 2024 00:00:39 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66988d2afc03c68191df8c03f9f99157fa5227efdeb18884dee222779eb0d2c9`  
		Last Modified: Wed, 10 Apr 2024 00:00:41 GMT  
		Size: 3.9 MB (3914077 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:057c771af0274f6b50bb3e9dd3cea13386f121ae579f0148f1de21fdb78e8ab1`  
		Last Modified: Wed, 10 Apr 2024 00:00:39 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f2d3da1314efd3575fcb81cd2a1510182d15eb3d35ab1eb211361f9e2ab73d`  
		Last Modified: Wed, 10 Apr 2024 01:00:30 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aaea26b113e46be270f8bd80168ed8af352181d8e524456431b172313164770`  
		Last Modified: Wed, 10 Apr 2024 01:00:30 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84376929d393c15268b67f20515a0acce681ee32e7a600fedabc5370b57d7f72`  
		Last Modified: Wed, 10 Apr 2024 01:00:31 GMT  
		Size: 5.1 MB (5139025 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:278257ce26fae40f235a566d74b0d369d6cc8253e8ab69890b3bfc820e7244ec`  
		Last Modified: Wed, 10 Apr 2024 01:00:30 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.9` - windows version 10.0.17763.5696; amd64

```console
$ docker pull hylang@sha256:13cbfa1f6824336558a66e53b3b445de40c788e96a5b7a68c38b1888a9c84972
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2217049431 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7dc1243733fc8b5d0264b6ac12e761acaeaea7094365b339394a58013c84f6ce`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Sat, 06 Apr 2024 02:39:33 GMT
RUN Install update 10.0.17763.5696
# Tue, 09 Apr 2024 23:59:01 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 09 Apr 2024 23:59:33 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 10 Apr 2024 00:00:03 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 10 Apr 2024 00:00:03 GMT
ENV PYPY_VERSION=7.3.15
# Wed, 10 Apr 2024 00:00:45 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.9-v7.3.15-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a156dad8b58570597eaaabe05663f00f80c60bc11df4a9c46d0953b6c5eb9209'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.9-v7.3.15-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 10 Apr 2024 00:00:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 10 Apr 2024 00:00:46 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 10 Apr 2024 00:01:29 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 10 Apr 2024 00:01:30 GMT
CMD ["pypy"]
# Wed, 10 Apr 2024 01:00:55 GMT
ENV HY_VERSION=0.28.0
# Wed, 10 Apr 2024 01:00:55 GMT
ENV HYRULE_VERSION=0.5.0
# Wed, 10 Apr 2024 01:02:30 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 10 Apr 2024 01:02:31 GMT
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
	-	`sha256:2ebdd4bbfe7fb96612092cc4db3cf1bb49a76b7f6025be406e8636420842ec60`  
		Last Modified: Wed, 10 Apr 2024 00:01:36 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fa619c4882f6306f2bae5088822b01b2ac90c55a524be95243ca451a2e9fe6d`  
		Last Modified: Wed, 10 Apr 2024 00:01:36 GMT  
		Size: 483.7 KB (483737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72950ac6b9405236f550b7d9f09b395eec45a99e19562f80bfd2b491a1dba3ae`  
		Last Modified: Wed, 10 Apr 2024 00:01:37 GMT  
		Size: 15.5 MB (15525991 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bb1c01db3e01e717aad4703da0bf4e82d3136361699c3b0b9302d061df72424`  
		Last Modified: Wed, 10 Apr 2024 00:01:35 GMT  
		Size: 1.3 KB (1305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eff2deb18839a84471f7b77378b2855b48d8953470a1d00c59fd5fed85d9778`  
		Last Modified: Wed, 10 Apr 2024 00:01:37 GMT  
		Size: 27.6 MB (27573246 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e74237b39a0ffc7a93e017f5f1d1d1dca4d7c5243859b7c6923813459d50f953`  
		Last Modified: Wed, 10 Apr 2024 00:01:33 GMT  
		Size: 1.3 KB (1303 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a45ad39f7c27a8edf08fd48243c81d011b94049500d95c7482379da058777f15`  
		Last Modified: Wed, 10 Apr 2024 00:01:34 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db22bddc6ff129a76006f2165b23b5a20fada72df791376c4afa3d06e36497bc`  
		Last Modified: Wed, 10 Apr 2024 00:01:34 GMT  
		Size: 3.9 MB (3920297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e91134bb348d63d9192c428677f5609dbb59fd58f2a1fc1521b5ffd433ae5871`  
		Last Modified: Wed, 10 Apr 2024 00:01:33 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0dc1685e101b2651644ea67ab0f4ebdbcaf467fd244edf1350dcd7d9df8764c`  
		Last Modified: Wed, 10 Apr 2024 01:02:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdc53427215c130b7fe813ff503d59de49da2735933742cee6070e572b73dbb2`  
		Last Modified: Wed, 10 Apr 2024 01:02:34 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24c30df62fb7938f1700cb3e40f82cd22e8944ced9b578b386a2c98b5170b703`  
		Last Modified: Wed, 10 Apr 2024 01:02:35 GMT  
		Size: 5.1 MB (5107811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e6ebbdbb0c767a792acf29eb7c40f96a78415e4f65b11e34be33f62c78222f0`  
		Last Modified: Wed, 10 Apr 2024 01:02:35 GMT  
		Size: 1.3 KB (1307 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
