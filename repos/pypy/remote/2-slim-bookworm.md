## `pypy:2-slim-bookworm`

```console
$ docker pull pypy@sha256:956a3a48e139515358eed8dea08db61ee2f527ff2e00dd9320ee3697b6bf89b2
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:2-slim-bookworm` - linux; amd64

```console
$ docker pull pypy@sha256:d76b79bece691aaa523ac32ccfdcf6591563702ada508e4983ff87035fe4105d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.7 MB (65652380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4616c8e020234f5b505d7ec04549d029a4684c721cbcb5cd121fb02b2ec20f3e`
-	Default Command: `["pypy"]`

```dockerfile
# Fri, 05 Apr 2024 21:59:23 GMT
ADD file:4b1be1de1a1e5aa608c688cad2824587262081866180d7368feb79d33ca05953 in / 
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
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-linux64.tar.bz2'; 			sha256='e857553bdc4f25ba9670a5c173a057a9ff71262d5c5da73a6ddef9d7dc5d4f5e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-aarch64.tar.bz2'; 			sha256='31b41fca7280636d7818713b7a0fab8f34ece9c82cc88e51d305d43b3e6306d6'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-linux32.tar.bz2'; 			sha256='cb5c1da62a8ca31050173c4f6f537bc3ff316026895e5f1897b9bb526babae79'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-s390x.tar.bz2'; 			sha256='eb442279ec3f1eb17da296e38b531d3ca50c6418eab208a020bca4646a1dea46'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 05 Apr 2024 21:59:23 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 05 Apr 2024 21:59:23 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 05 Apr 2024 21:59:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Fri, 05 Apr 2024 21:59:23 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:b0a0cf830b12453b7e15359a804215a7bcccd3788e2bcecff2a03af64bbd4df7`  
		Last Modified: Wed, 24 Apr 2024 03:32:41 GMT  
		Size: 29.2 MB (29150479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a18f7249b2a2eec69d660c4d126083c77792b6a0b3a1cec8325dc1f847649dbf`  
		Last Modified: Wed, 24 Apr 2024 05:07:19 GMT  
		Size: 3.3 MB (3299439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9126a941f560602190ff826d7f6f86a572f3788bcf2e4fc26015e5b7ed47cc1`  
		Last Modified: Wed, 24 Apr 2024 05:07:19 GMT  
		Size: 31.2 MB (31249638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e97d2386b6e7d9e9c94fbf4b7b43249785d9e786b06d67a1a360d528a8ebfcc0`  
		Last Modified: Wed, 24 Apr 2024 05:07:19 GMT  
		Size: 2.0 MB (1952824 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:3a539bf04c7855a951861dd7d9fdf7c2a9805d7dd4f48ae8032480a5a6b0a07a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0c69214c00b366d81a5631a798056ef8993a566c636ce4c35a28ec5336867a3`

```dockerfile
```

-	Layers:
	-	`sha256:74640fe4642e4ee63f5bb1ee9747c6f7e73d0b4df65fc6022fe6ccaa545d623b`  
		Last Modified: Wed, 24 Apr 2024 05:07:19 GMT  
		Size: 2.3 MB (2346824 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:23e81604aad666f4f7bf01dd5b49e6e94b5c3487828da832a1370941822f3d05`  
		Last Modified: Wed, 24 Apr 2024 05:07:19 GMT  
		Size: 22.8 KB (22815 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:dfbfd4bbfe42850d567189d3a0aa5416846e6645d88fc89f5e1220add6fab843
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63661610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d85bc8f6144ccfd5332af74496fe64bd2da38a8037634946ceb0e76a51e010e`
-	Default Command: `["pypy"]`

```dockerfile
# Fri, 05 Apr 2024 21:59:23 GMT
ADD file:c7462f37a5f52b19cd37c5f448dd8959421f489eccea6afa5483d10692994ff6 in / 
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
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-linux64.tar.bz2'; 			sha256='e857553bdc4f25ba9670a5c173a057a9ff71262d5c5da73a6ddef9d7dc5d4f5e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-aarch64.tar.bz2'; 			sha256='31b41fca7280636d7818713b7a0fab8f34ece9c82cc88e51d305d43b3e6306d6'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-linux32.tar.bz2'; 			sha256='cb5c1da62a8ca31050173c4f6f537bc3ff316026895e5f1897b9bb526babae79'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-s390x.tar.bz2'; 			sha256='eb442279ec3f1eb17da296e38b531d3ca50c6418eab208a020bca4646a1dea46'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 05 Apr 2024 21:59:23 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 05 Apr 2024 21:59:23 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 05 Apr 2024 21:59:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Fri, 05 Apr 2024 21:59:23 GMT
CMD ["pypy"]
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
	-	`sha256:f7c8cf0303fed928568ade2e6e885f5e9663543a8a0b81691978dc738ce73a5d`  
		Last Modified: Wed, 10 Apr 2024 20:41:31 GMT  
		Size: 29.2 MB (29232443 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d381591e2dcd57591a66625fa392833e84cefbb86632a27ac6364361faacb99d`  
		Last Modified: Wed, 10 Apr 2024 20:41:30 GMT  
		Size: 2.0 MB (1952794 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:3166aa837579fac51be6a871420c23497d816430125f725699c31dd0af8b1bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2369612 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e3f74c8e7b2701b1b909de8e6b134d3e496cb56563987d2008fa36a54b95088`

```dockerfile
```

-	Layers:
	-	`sha256:1e20e50420e8684e89818c0d69eb0e8e7f10455f1a48e090acbd3eb76ea79205`  
		Last Modified: Wed, 10 Apr 2024 20:41:30 GMT  
		Size: 2.3 MB (2346951 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0cda41f290b2a9b8c098ad9c6d42d87ddc81eb353947a0610b29b71cf8f82c88`  
		Last Modified: Wed, 10 Apr 2024 20:41:29 GMT  
		Size: 22.7 KB (22661 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:cdbfd54d7f4941ad0b48eb691c1ac10d2da7b59ad6b82f106bbf6f62e9e6e9a8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.2 MB (62168727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:42554b237a5fe9aabf576518ebf4e96c894df8210ed424091e5b3e878d09577f`
-	Default Command: `["pypy"]`

```dockerfile
# Fri, 05 Apr 2024 21:59:23 GMT
ADD file:104afc54fe81c235eceb94cef0c07d1e8032f01fb7c450dffd4e251671d445ba in / 
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
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-linux64.tar.bz2'; 			sha256='e857553bdc4f25ba9670a5c173a057a9ff71262d5c5da73a6ddef9d7dc5d4f5e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-aarch64.tar.bz2'; 			sha256='31b41fca7280636d7818713b7a0fab8f34ece9c82cc88e51d305d43b3e6306d6'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-linux32.tar.bz2'; 			sha256='cb5c1da62a8ca31050173c4f6f537bc3ff316026895e5f1897b9bb526babae79'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.15-s390x.tar.bz2'; 			sha256='eb442279ec3f1eb17da296e38b531d3ca50c6418eab208a020bca4646a1dea46'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 05 Apr 2024 21:59:23 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 05 Apr 2024 21:59:23 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 05 Apr 2024 21:59:23 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Fri, 05 Apr 2024 21:59:23 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:af3150ac61338e2036c167b18f712ab80fd82f6b215de3e4732cb6defbd8bcb2`  
		Last Modified: Wed, 24 Apr 2024 03:43:36 GMT  
		Size: 30.2 MB (30163183 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5888a8fd3f14a8329abac24a31dd7f8a4ba44db07211f3119a86a88b38643707`  
		Last Modified: Wed, 24 Apr 2024 05:07:29 GMT  
		Size: 3.3 MB (3304876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:240821d127688fde4dc7f2f227054f75ce0ab06afbcd50e5405be131287df266`  
		Last Modified: Wed, 24 Apr 2024 05:07:29 GMT  
		Size: 26.7 MB (26748136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bca63a59a9c7b32fb3ce0df1299f498c53cbf5e5ae8eeb56f3232825ff2e826`  
		Last Modified: Wed, 24 Apr 2024 05:07:29 GMT  
		Size: 2.0 MB (1952532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:12864911a55cc6f9402a102d8348a6676b27753dcc45e6b1e0ad0ed95004b8ce
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2366707 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1691827b1489920af9dabb1d822cc9c14da2c12bc9c4a91837c3c3bb6272e357`

```dockerfile
```

-	Layers:
	-	`sha256:a11bfcc0e1d14bf558d954f0797f93f30c219bae9e48660066648cd0db2c2e24`  
		Last Modified: Wed, 24 Apr 2024 05:07:29 GMT  
		Size: 2.3 MB (2343946 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ca7df76ba0173376b5874083e8a1a8d203753406d6138accb50d06149b324dfb`  
		Last Modified: Wed, 24 Apr 2024 05:07:28 GMT  
		Size: 22.8 KB (22761 bytes)  
		MIME: application/vnd.in-toto+json
