## `pypy:2-slim-bookworm`

```console
$ docker pull pypy@sha256:73ea1edde8914d0c089905453abb07aacd7f6346069a4b28baf4c9906ce31d3e
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
$ docker pull pypy@sha256:52650eed9291afa7b445ca91d09c17e9d7a13d93fed6c430162e8873991074d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65233550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ff801f5676452ca3c9790139924079974ae1b4d36944e9cb448194a6777c5e9`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 26 Feb 2025 17:07:12 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 26 Feb 2025 17:07:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 17:07:12 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 26 Feb 2025 17:07:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-linux64.tar.bz2'; 			sha256='d38445508c2eaf14ebb380d9c1ded321c5ebeae31c7e66800173d83cb8ddf423'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-aarch64.tar.bz2'; 			sha256='fe89d4fd4af13f76dfe7315975003518cf176520e3ccec1544a88d174f50910e'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-linux32.tar.bz2'; 			sha256='cc52df02b6926bd8645c1651cd7f6637ce51c2f352d0fb3c6b9330d15194b409'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 26 Feb 2025 17:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 26 Feb 2025 17:07:12 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:abbb3761e6731c589098f1029bd8c374d1e362ee93cd4bf580a7f6be7b369811`  
		Last Modified: Mon, 17 Mar 2025 23:20:22 GMT  
		Size: 3.5 MB (3499330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c026575594dbbd1adc99874f977d211f7cecc4dd4f3e2072a5a413f8924c1d7d`  
		Last Modified: Mon, 17 Mar 2025 23:20:23 GMT  
		Size: 31.6 MB (31576503 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8359550ac4c7a18091bf741fc28c39c9762d80823296db028dc0a4a2940732de`  
		Last Modified: Mon, 17 Mar 2025 23:20:22 GMT  
		Size: 2.0 MB (1952852 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:0bb3896d1bb5346134402be87f01de7088143a6cf5ccbb8bff096d6ef7ab6775
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2404033 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:716e647f0a42e20ac70282e17aad357455ac9773c3e5fed653ee07f5ce9bf271`

```dockerfile
```

-	Layers:
	-	`sha256:ce3a5a7e495f62f6bc422ce640d73e6ebbdd193187ec8d38bea36793a099670c`  
		Last Modified: Mon, 17 Mar 2025 23:20:22 GMT  
		Size: 2.4 MB (2379294 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c68936cf64ab957d055f23dc5b6f9ed639f4f4096251a6a8c95e0dcab2fe41f9`  
		Last Modified: Mon, 17 Mar 2025 23:20:22 GMT  
		Size: 24.7 KB (24739 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:26084f170bf96b91ef2eeda6a6330ba2084f71c32ee51360338128dc93d6aaf5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62826662 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f699609d49b63891a37afe38290f90649f6b563376331852c1d75709acf57361`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 26 Feb 2025 17:07:12 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 26 Feb 2025 17:07:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 17:07:12 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 26 Feb 2025 17:07:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-linux64.tar.bz2'; 			sha256='d38445508c2eaf14ebb380d9c1ded321c5ebeae31c7e66800173d83cb8ddf423'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-aarch64.tar.bz2'; 			sha256='fe89d4fd4af13f76dfe7315975003518cf176520e3ccec1544a88d174f50910e'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-linux32.tar.bz2'; 			sha256='cc52df02b6926bd8645c1651cd7f6637ce51c2f352d0fb3c6b9330d15194b409'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 26 Feb 2025 17:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 26 Feb 2025 17:07:12 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08287ef3f5a9e0a28a72307a55937b861b0854bfc7d3d620d08f8d3b5278a7b`  
		Last Modified: Tue, 18 Mar 2025 02:36:31 GMT  
		Size: 3.3 MB (3322929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed29df73da2829a4aa250aafcc9c6636cb5dbb8cf6113a424e56c9f780e0d003`  
		Last Modified: Tue, 18 Mar 2025 02:36:32 GMT  
		Size: 29.5 MB (29507011 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edd94de08f82c984723e604828469e4469e76eef925a2e200fe5e1f7c5d5824`  
		Last Modified: Tue, 18 Mar 2025 02:36:31 GMT  
		Size: 2.0 MB (1952685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:f91536d9a2d6f83c8b20561d6fd6a3951de34219aec198ea4e139e8fa8ece046
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2404710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6fba40ba6aafece8b321de9d3725870601ab5d371a3d02aff7c18383118518b`

```dockerfile
```

-	Layers:
	-	`sha256:7994b7b10ac1bb1ae0d6c53fcc4f4a496b0c2d104e7ec8207e96621ee974ebe8`  
		Last Modified: Tue, 18 Mar 2025 02:36:31 GMT  
		Size: 2.4 MB (2379695 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a173ddf91a55c3bfc7a8dd9620164d16df138e2b45472ce2291da85edd239c7d`  
		Last Modified: Tue, 18 Mar 2025 02:36:30 GMT  
		Size: 25.0 KB (25015 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:11753f681e29b1f6237f8ab5bfaa43f7e731f616256574ec148e6dd3bc4d1f53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61828008 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d08afdf41d776a197094064502a4f8e3e3fb5f903bd241c2f193dfe954bc026`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 26 Feb 2025 17:07:12 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Wed, 26 Feb 2025 17:07:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 17:07:12 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 26 Feb 2025 17:07:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-linux64.tar.bz2'; 			sha256='d38445508c2eaf14ebb380d9c1ded321c5ebeae31c7e66800173d83cb8ddf423'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-aarch64.tar.bz2'; 			sha256='fe89d4fd4af13f76dfe7315975003518cf176520e3ccec1544a88d174f50910e'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-linux32.tar.bz2'; 			sha256='cc52df02b6926bd8645c1651cd7f6637ce51c2f352d0fb3c6b9330d15194b409'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 26 Feb 2025 17:07:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 26 Feb 2025 17:07:12 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4644488e6712c2d2621975c66d32b84d7922a4ee722f9d73e325dcf7084c999b`  
		Last Modified: Mon, 17 Mar 2025 23:28:07 GMT  
		Size: 3.5 MB (3503430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0edbc81a7883f09c0f67238c6045478375354c6e82bd10cb66821cdb3001bd35`  
		Last Modified: Mon, 17 Mar 2025 23:28:08 GMT  
		Size: 27.2 MB (27182474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:03bf115fd1dacade4dba9af58e8d0210ff2a4027239022463a283907aa4b014d`  
		Last Modified: Mon, 17 Mar 2025 23:28:07 GMT  
		Size: 2.0 MB (1952576 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:7f9b04968901d7d00669b339d304f218f5195b0467b52a996d1a3487dc7f0ee6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d5f6e15d1a0a245f03795630f8a0ad4dbc8c37e330cfe85b5adeb7fb4d7fb58`

```dockerfile
```

-	Layers:
	-	`sha256:abee8fe5f82584938c960458b267798a09936b5a9bbff9e21452d94cdcd5087b`  
		Last Modified: Mon, 17 Mar 2025 23:28:07 GMT  
		Size: 2.4 MB (2376377 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f09705a67f16b6bc5341dbac46f4f0d296e68745e6ed9d77136c90d877c87227`  
		Last Modified: Mon, 17 Mar 2025 23:28:07 GMT  
		Size: 24.6 KB (24643 bytes)  
		MIME: application/vnd.in-toto+json
