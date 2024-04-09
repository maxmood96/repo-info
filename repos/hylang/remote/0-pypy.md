## `hylang:0-pypy`

```console
$ docker pull hylang@sha256:335b2cc8c4c8e243e41fe4be9db354a389fdc1bcc34a21d12bf7e0d4e197d39b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:0-pypy` - linux; amd64

```console
$ docker pull hylang@sha256:2fdb30a49a097e2590192d575dade829a7a53f59c17a605fba764ec005334978
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73131845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e6bedb1b8d829572676193113900eee0dde24f3703dade0212fc0d5c38da64f0`
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
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59d65d6289126a3093a5c248ac05b739f6f67cc3e6db895a0962f5b3ed0051ff`  
		Last Modified: Mon, 08 Apr 2024 22:00:13 GMT  
		Size: 3.5 MB (3491069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a8cd257081d899fefc63a320b1a023f0828239e1fda1075451c7ec66ce3249f`  
		Last Modified: Mon, 08 Apr 2024 22:00:13 GMT  
		Size: 30.9 MB (30875580 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae2cfdd3e06776744e0b8bae8c257519c64ea26fb58cc3568ae10316c8a8d3f5`  
		Last Modified: Mon, 08 Apr 2024 22:00:13 GMT  
		Size: 3.3 MB (3299967 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3424a8c1749d59cde3d9adf4700267786a098f480e0bc86645dc990ee4deb1e`  
		Last Modified: Mon, 08 Apr 2024 22:57:12 GMT  
		Size: 6.3 MB (6341048 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy` - unknown; unknown

```console
$ docker pull hylang@sha256:0d25303cab40ab94e1642284cd106a9cb06518e41f3fb69a69cc9e72a48b86b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2383787 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:41a919a32cbd79f9645fd84bc54c462887f9a55162ce68a5feb6a7777f0b7f48`

```dockerfile
```

-	Layers:
	-	`sha256:ea963ecbebd77149c2819a529ba45ccdaa612414740bd5223c0c26d7d95fac3a`  
		Last Modified: Mon, 08 Apr 2024 22:57:12 GMT  
		Size: 2.4 MB (2371440 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5744fb590636939001deead3c1d4902dabef9b3ba196b86de402b7714296fa05`  
		Last Modified: Mon, 08 Apr 2024 22:57:12 GMT  
		Size: 12.3 KB (12347 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:ac6b5d0950e9b0a420082f3ee6262a22a8f176cdf32864a21ee60ca21e13187c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.3 MB (71288320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e242e5903912e6dbbe745e241750d22727a63987a04d1f1c4b3cc63358e83898`
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
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34d5e967355e27afb96983147c5620f49e0324496b8add2a3f37df9021fdff0d`  
		Last Modified: Tue, 09 Apr 2024 06:37:46 GMT  
		Size: 3.3 MB (3314256 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d098f4aa0dc91de0def4ea4edc5d69693e06f9dab982e2f1c3fab06bfd04e490`  
		Last Modified: Tue, 09 Apr 2024 06:37:47 GMT  
		Size: 29.2 MB (29176578 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b4e5948aa4836e9788445faeeff2957b8a7e62fb3092dbaaee639dcea7884188`  
		Last Modified: Tue, 09 Apr 2024 06:37:46 GMT  
		Size: 3.3 MB (3299916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f626b0ec526377ae0f63819cd72e297f8c4a4c7a6d5a2d6a30bb801627bf7f99`  
		Last Modified: Tue, 09 Apr 2024 09:16:38 GMT  
		Size: 6.3 MB (6341136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy` - unknown; unknown

```console
$ docker pull hylang@sha256:89ce5a4e619473236e0f8439775e7c0c031cfd9332e6d00c56b19ad7a2da18f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2384082 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ebfe39ed8b4c7d8a69dd5a8fe8332faa40ce47210e9dbfc72c6b0bd71b31698`

```dockerfile
```

-	Layers:
	-	`sha256:8ffe048486d76d857c3fb3c50d39da062fb3d6de1afa0bc9ba38a323f5d07d30`  
		Last Modified: Tue, 09 Apr 2024 09:16:37 GMT  
		Size: 2.4 MB (2371677 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d625d7772d61e87e19df3430aa580839bcd78e69bed8a341b52aab8b11fde85f`  
		Last Modified: Tue, 09 Apr 2024 09:16:37 GMT  
		Size: 12.4 KB (12405 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy` - linux; 386

```console
$ docker pull hylang@sha256:96cfbcaef40f878f30d7ffe8e6503eb4a31217e21a0781e5fbc65dbbe2ac5c43
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70513826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:610c44c44731cf16d0b6bf020a7b7b05921105db1d692884eb6d5d22f55c250c`
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
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0a3cd8f5bb51df8a7d93dab1ade22d490fd9350a728323cdf6f9a63e97288899`  
		Last Modified: Mon, 08 Apr 2024 22:00:13 GMT  
		Size: 3.5 MB (3496213 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a489eba2dccc2eb008d1293dd8393f1d4159f2c6f677a4898909f6056203061f`  
		Last Modified: Mon, 08 Apr 2024 22:00:14 GMT  
		Size: 27.2 MB (27235134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b18307e18a43e81798a7affec250b1f234378962a7cef47d7fdaef0bfc507d3a`  
		Last Modified: Mon, 08 Apr 2024 22:00:14 GMT  
		Size: 3.3 MB (3299527 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2efcea1147453dd80ea3ce1f7bce157f1de69114976f8a6027885a957e07653d`  
		Last Modified: Mon, 08 Apr 2024 22:57:22 GMT  
		Size: 6.3 MB (6341079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy` - unknown; unknown

```console
$ docker pull hylang@sha256:71b49b4efde3a65ad8e51131ddec4eada861ea92b72695544c508039aaceba44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2380771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d2fe25f0b33f09a42e675e4ba0e105dddc902b28e04b7a567705deeb1521836`

```dockerfile
```

-	Layers:
	-	`sha256:f323845198514258fce242842d56e1fb280a4d7f17a7cf2ea455039e5dc9fd51`  
		Last Modified: Mon, 08 Apr 2024 22:57:21 GMT  
		Size: 2.4 MB (2368516 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:796be5d31cfdecff9146d933c2c7200abf210600e8952496863897c74e702fa9`  
		Last Modified: Mon, 08 Apr 2024 22:57:21 GMT  
		Size: 12.3 KB (12255 bytes)  
		MIME: application/vnd.in-toto+json
