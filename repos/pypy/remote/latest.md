## `pypy:latest`

```console
$ docker pull pypy@sha256:a742053a4feb55bea34e0ca029a8d0dd1ad66b703f4ed612e2673c19c8257c3a
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

### `pypy:latest` - linux; amd64

```console
$ docker pull pypy@sha256:7b46b8fd5a2c25529cef38f49c5ba8eccaa5660604ee2288b8985c2d8b190957
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.8 MB (358756855 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6c3e1980da06fc6e5e4a6d61f3b0875797ce9047d3579ab0394aba990d51b7f`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 25 Dec 2023 11:12:03 GMT
ADD file:35f7caaedc3b6f725dee87eb8d1f2727c04cb21062b5eb7f59801dafced61993 in / 
# Mon, 25 Dec 2023 11:12:03 GMT
CMD ["bash"]
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Dec 2023 11:12:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV LANG=C.UTF-8
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYPY_VERSION=7.3.14
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux64.tar.bz2'; 			sha256='a83879891dc0a6c1504da0954fba1125b21a2591782897231a8168100ea72b94'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-aarch64.tar.bz2'; 			sha256='fbef65dfc69dcd6006d843553d268b331f1b13dfc3938492bd35f0f477b5bcf4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux32.tar.bz2'; 			sha256='d37e7c7a03bed5dceca2ab7f821ad7655808cccf6908155f78f0effd811b7f4f'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-s390x.tar.bz2'; 			sha256='363e87ad3b6547cc68981c665cf049449bed44cf9e49cabbbcc61df73ea2d40b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:e455cf41eadb2f19f014361006086cdc5b3de16f3d13bd1d586be63e66c7fc63`  
		Last Modified: Thu, 11 Jan 2024 02:42:47 GMT  
		Size: 55.1 MB (55057723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e4531da2f06f2911a5e67446c1ec507acb336afe7130741c6ed12ce442b730f`  
		Last Modified: Thu, 11 Jan 2024 04:45:42 GMT  
		Size: 15.8 MB (15765113 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:55c23b7d6528239a16f11d6e650e9a9fdb7039721df42b6ca01777fe34c2b116`  
		Last Modified: Thu, 11 Jan 2024 04:45:57 GMT  
		Size: 54.6 MB (54601205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d92159de95ca6028dff92254cdede6b16274470e653943871542fceec95bdf5`  
		Last Modified: Thu, 11 Jan 2024 04:46:29 GMT  
		Size: 196.9 MB (196898008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f5e4d99743d28f4a61aae556016f66ea4e567ad1a2ac39ab769d10b691a6986`  
		Last Modified: Fri, 12 Jan 2024 00:38:29 GMT  
		Size: 3.0 MB (2969776 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31da796b4166e8c9bfcadb2da6c4f92afebc01839d1abc4b0521a3796aef7cfc`  
		Last Modified: Fri, 12 Jan 2024 00:38:30 GMT  
		Size: 30.2 MB (30228710 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:27a96f20b64b74935255dd419ce5e79b3b7444b116b840552937bf30c4f68b36`  
		Last Modified: Fri, 12 Jan 2024 00:38:29 GMT  
		Size: 3.2 MB (3236320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:latest` - unknown; unknown

```console
$ docker pull pypy@sha256:972647d98ce8752b19b18aa250363bb050c9fdcace51d9e19b6e9a95fea6e3e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13262458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3a12510a0e5247e100e295aa19a97a08d1de2902b98794293c15ec24075a220c`

```dockerfile
```

-	Layers:
	-	`sha256:106f8b766ea24db058f19db17acb2b3f643a680cb6dd40e4e93484664d8b2ba1`  
		Last Modified: Fri, 12 Jan 2024 00:38:29 GMT  
		Size: 13.2 MB (13232826 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5293a1306967303fbfd4f9c0cacd9d87a467de5097abf826d0a19acd0c7d212a`  
		Last Modified: Fri, 12 Jan 2024 00:38:29 GMT  
		Size: 29.6 KB (29632 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:latest` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:5fdc66ae4112632e4e96323178b65d67967c742b13a21aff66874439ed5778c5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.8 MB (348768540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f22807db8e6c68571251ff44d90a6795472f3e2266437342f5930eb9f3111ef3`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 25 Dec 2023 11:12:03 GMT
ADD file:8fb65cadfd211811589ee046d0fbd69d1fe11461b0c0c154a7650bf97307b857 in / 
# Mon, 25 Dec 2023 11:12:03 GMT
CMD ["bash"]
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Dec 2023 11:12:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV LANG=C.UTF-8
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYPY_VERSION=7.3.14
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux64.tar.bz2'; 			sha256='a83879891dc0a6c1504da0954fba1125b21a2591782897231a8168100ea72b94'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-aarch64.tar.bz2'; 			sha256='fbef65dfc69dcd6006d843553d268b331f1b13dfc3938492bd35f0f477b5bcf4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux32.tar.bz2'; 			sha256='d37e7c7a03bed5dceca2ab7f821ad7655808cccf6908155f78f0effd811b7f4f'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-s390x.tar.bz2'; 			sha256='363e87ad3b6547cc68981c665cf049449bed44cf9e49cabbbcc61df73ea2d40b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:cf83973c4a096cce9f37c421ad6f19cf1ebf7ae4d8ea98dac4913bd2aef08d1c`  
		Last Modified: Thu, 11 Jan 2024 02:44:25 GMT  
		Size: 53.7 MB (53707847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:aebf2a961043d6b9dd703d0a485e216a2e302edf2e2525f7f410987d26905e71`  
		Last Modified: Thu, 11 Jan 2024 09:35:03 GMT  
		Size: 15.8 MB (15750711 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:826044e8ec1545c4af5dfe71ab63bce600198330f150aa968074bb86e78cd154`  
		Last Modified: Thu, 11 Jan 2024 09:35:17 GMT  
		Size: 54.7 MB (54699869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb605b1d0205817191fda1aebbfb24bc89220d168a2231b4a4b44c0c48e4e627`  
		Last Modified: Thu, 11 Jan 2024 09:35:43 GMT  
		Size: 189.8 MB (189834619 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb727f089a3bed1c31c6cb5d77bf0d46f9a442a51846c857e446bb0dcbf199be`  
		Last Modified: Fri, 12 Jan 2024 17:17:50 GMT  
		Size: 3.0 MB (2974184 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:db0edc6de140cd7f68b19e09932cf786cb010d49f4f442df80ac2859f75e9fe1`  
		Last Modified: Fri, 12 Jan 2024 17:17:50 GMT  
		Size: 28.6 MB (28565099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:acdfacd401972d857c007b2adcd92c8f7679713378d760b9b0fa88e6e3d84914`  
		Last Modified: Fri, 12 Jan 2024 17:17:50 GMT  
		Size: 3.2 MB (3236211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:latest` - unknown; unknown

```console
$ docker pull pypy@sha256:c7a90eba2635eae42ba2e9c4b01a16aa0d45c4fce3f3fb58cad20a218823ae1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13264227 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89f3aee240cd9efcb898b22c369d731a183e44ba88aea7d31e77dc15b0327fd9`

```dockerfile
```

-	Layers:
	-	`sha256:f68a71774265b8257cbe6fc46f827fb2db655e187de21b71d770054b936a50e9`  
		Last Modified: Fri, 12 Jan 2024 17:17:50 GMT  
		Size: 13.2 MB (13235219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2fd48fe39b842239a8816b98842f01d9a69341e66b38a0ff6a472a145db2e7da`  
		Last Modified: Fri, 12 Jan 2024 17:17:49 GMT  
		Size: 29.0 KB (29008 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:latest` - linux; 386

```console
$ docker pull pypy@sha256:1b0a934e3f44a60f94a2f38fe97ee68f4669aed045659a1787e1d4a6b53fa432
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **360.9 MB (360946383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a3781a18b1f51457fbf85339e5da34f31269b31770c3d00d107368af64887eb`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 25 Dec 2023 11:12:03 GMT
ADD file:5ec37a8451203256eba8b114f21ff297f9b2e0b420ec7f0c50658a448ffc8f7b in / 
# Mon, 25 Dec 2023 11:12:03 GMT
CMD ["bash"]
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Dec 2023 11:12:03 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV LANG=C.UTF-8
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYPY_VERSION=7.3.14
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux64.tar.bz2'; 			sha256='a83879891dc0a6c1504da0954fba1125b21a2591782897231a8168100ea72b94'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-aarch64.tar.bz2'; 			sha256='fbef65dfc69dcd6006d843553d268b331f1b13dfc3938492bd35f0f477b5bcf4'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-linux32.tar.bz2'; 			sha256='d37e7c7a03bed5dceca2ab7f821ad7655808cccf6908155f78f0effd811b7f4f'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.14-s390x.tar.bz2'; 			sha256='363e87ad3b6547cc68981c665cf049449bed44cf9e49cabbbcc61df73ea2d40b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Mon, 25 Dec 2023 11:12:03 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Mon, 25 Dec 2023 11:12:03 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Mon, 25 Dec 2023 11:12:03 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:9b04188f89c4a7eaa549c59c16834ec81012244afac6c52196bafd2cd4486602`  
		Last Modified: Thu, 11 Jan 2024 02:43:42 GMT  
		Size: 56.0 MB (56046385 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d75db71c7ec6ec0e64a32b92dfa4a3127698f085f1df99e2c6187447f2433d41`  
		Last Modified: Thu, 11 Jan 2024 04:43:06 GMT  
		Size: 16.3 MB (16269099 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b09cf67a662b504a2881d65a2e7b39a4b9acc7384a9f90c2583665bde0fde79`  
		Last Modified: Thu, 11 Jan 2024 04:43:28 GMT  
		Size: 55.9 MB (55940001 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af36f551206d5f517da5a527abcaf80125ea57bbb76f0bde20a26a83bd03185d`  
		Last Modified: Thu, 11 Jan 2024 04:44:16 GMT  
		Size: 199.8 MB (199824822 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec819d6556442bf761b072eef1d863b985102fe35301b4be86c6190015505c9a`  
		Last Modified: Fri, 12 Jan 2024 00:40:40 GMT  
		Size: 3.1 MB (3120264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b9fb89eb5884e5c1d33169a9bcaab1faa576912aee19ed5308803b9af84391a`  
		Last Modified: Fri, 12 Jan 2024 00:40:41 GMT  
		Size: 26.5 MB (26509429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458e056a5807fe2409f0ebaf57add473e11261d75a8a4fc573077228a3a9d3cb`  
		Last Modified: Fri, 12 Jan 2024 00:40:40 GMT  
		Size: 3.2 MB (3236383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:latest` - unknown; unknown

```console
$ docker pull pypy@sha256:103d0085fa6e5d3febe4341cdae16cd894f2d46dc27815b57c1a03f2a66dbaed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **13.3 MB (13251209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f440e2e9aa8fd76208f63a56d8590b9ea2f7bf11296975477bfad59cf7aaee81`

```dockerfile
```

-	Layers:
	-	`sha256:600d0698e05f1e14b637b6080921a2d9bf186d08ac62e98318b707072972ed6c`  
		Last Modified: Fri, 12 Jan 2024 00:40:41 GMT  
		Size: 13.2 MB (13221679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2ce9a3065978ada87ee778139a855eab60fd1d03c179b129cc0f635e54167d96`  
		Last Modified: Fri, 12 Jan 2024 00:40:41 GMT  
		Size: 29.5 KB (29530 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:latest` - windows version 10.0.20348.2227; amd64

```console
$ docker pull pypy@sha256:fd81869599441e82f6a315442f8eeabd5ceb0fc1a4e5c8e17920431044cf8456
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.9 GB (1946904312 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dba215c7ddfbb19f61010da7ea097d091fd1dcddc1953a934db5009014187e4d`
-	Default Command: `["pypy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:55:20 GMT
RUN Apply image 10.0.20348.1787
# Thu, 04 Jan 2024 03:43:51 GMT
RUN Install update 10.0.20348.2227
# Thu, 11 Jan 2024 00:02:25 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Thu, 11 Jan 2024 00:02:40 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:02:57 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:02:59 GMT
ENV PYPY_VERSION=7.3.14
# Thu, 11 Jan 2024 00:03:19 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.10-v7.3.14-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '1713edd310f400935fe9a9f8fa0fd9da1a405eaf7b69564d00f437fb498327f8'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.10-v7.3.14-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:03:20 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 11 Jan 2024 00:03:21 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 11 Jan 2024 00:03:45 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:03:45 GMT
CMD ["pypy"]
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
	-	`sha256:c88df14b1ca940183d9da68888326e47ee72b5cc64f2781f79490603be74e044`  
		Last Modified: Thu, 11 Jan 2024 00:03:54 GMT  
		Size: 1.3 KB (1338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f3144ab10451dbc0146b06fc3ef591df952a929bdf1d999c172a7d4340d834`  
		Last Modified: Thu, 11 Jan 2024 00:03:53 GMT  
		Size: 481.8 KB (481836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e861214ff08e0de8c72facc8cfb8421bf422336c811c0de19d26e2a3b7f51f6d`  
		Last Modified: Thu, 11 Jan 2024 00:03:55 GMT  
		Size: 15.5 MB (15533847 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ef308c6ee61cacc687ff619da52d05077a102015ced3c9522cb53ff32f60dfb`  
		Last Modified: Thu, 11 Jan 2024 00:03:53 GMT  
		Size: 1.4 KB (1385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d22708379b02fcd9171552a618d04c549277db4fb08ef2d372b0a3e1f19a2861`  
		Last Modified: Thu, 11 Jan 2024 00:03:54 GMT  
		Size: 26.8 MB (26755988 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc55525bde698de55b5d8fb96ec5720a43fdf490023629f91990c2154c001053`  
		Last Modified: Thu, 11 Jan 2024 00:03:51 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f384eb19ed8142f06400b3031405baacdfcf36d0c39ec912a3540e0262dcbb7f`  
		Last Modified: Thu, 11 Jan 2024 00:03:51 GMT  
		Size: 1.3 KB (1299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37aab0b91aac98a6965fbf6300047a43ef4582d6ea41a14c83196ccba35d0b9d`  
		Last Modified: Thu, 11 Jan 2024 00:03:52 GMT  
		Size: 3.9 MB (3913357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:899a8d53a1d61ed4371c32cec9f2acb58341861b9aa2c4ae8380bd2b31a777cc`  
		Last Modified: Thu, 11 Jan 2024 00:03:51 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:latest` - windows version 10.0.17763.5329; amd64

```console
$ docker pull pypy@sha256:5fd23ae661e5efe1b42559da6d701b78af93d45212a6f08a7244938e25b9f7cf
```

-	Docker Version: 24.0.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2116416629 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7ca6b34ae1711830a55c9a799a56dd7edd4926b921caeec6a1c2930bfe6ed758`
-	Default Command: `["pypy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 08 Jun 2023 12:58:24 GMT
RUN Apply image 10.0.17763.4499
# Tue, 02 Jan 2024 22:50:56 GMT
RUN Install update 10.0.17763.5329
# Wed, 10 Jan 2024 23:59:22 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 10 Jan 2024 23:59:47 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:00:13 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:00:14 GMT
ENV PYPY_VERSION=7.3.14
# Thu, 11 Jan 2024 00:00:49 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.10-v7.3.14-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '1713edd310f400935fe9a9f8fa0fd9da1a405eaf7b69564d00f437fb498327f8'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.10-v7.3.14-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:00:50 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 11 Jan 2024 00:00:50 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 11 Jan 2024 00:01:29 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Thu, 11 Jan 2024 00:01:30 GMT
CMD ["pypy"]
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
	-	`sha256:6f846b088e434523607089c8ba46598f340e978dc1be5cfcaff97a7b83b539cd`  
		Last Modified: Thu, 11 Jan 2024 00:01:38 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dcefd56535b029a351156cebe2e9d1bad709a9f3ad6a270cd0252b557697eb6`  
		Last Modified: Thu, 11 Jan 2024 00:01:37 GMT  
		Size: 490.4 KB (490367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cfbd105f0645e87ee5c617b8a9bc6721a925d3df1ec3694c988511a26d99190`  
		Last Modified: Thu, 11 Jan 2024 00:01:38 GMT  
		Size: 15.5 MB (15520210 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1acd088ab3f2d5ba89f4ab0ee4cff216ec55f49715ecd2d49480a47755e391`  
		Last Modified: Thu, 11 Jan 2024 00:01:36 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9437ea681f79c91cc62470b2a6cfd34ae59af554f23ecff428f2d639aad9676b`  
		Last Modified: Thu, 11 Jan 2024 00:01:38 GMT  
		Size: 26.8 MB (26762043 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8da865f13ef2bbaccd49d0302e46dd1a227fd2387e9d7ce123eebec7a3fa7185`  
		Last Modified: Thu, 11 Jan 2024 00:01:34 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:294ee2c16f28c64454fc14469589fb6fb6cefafcc5d96dfb2748ccfecb458452`  
		Last Modified: Thu, 11 Jan 2024 00:01:34 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:570faef7d2f625df0ea1139baf0f6e61d3bac54b584af821c479a6e715bd699c`  
		Last Modified: Thu, 11 Jan 2024 00:01:35 GMT  
		Size: 3.9 MB (3914954 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d475cabefa672dc08384d97626017cdada71c70356dd96fc948aaebd94a8844`  
		Last Modified: Thu, 11 Jan 2024 00:01:34 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
