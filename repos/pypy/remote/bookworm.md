## `pypy:bookworm`

```console
$ docker pull pypy@sha256:7d788f76fdc2729baae75ba15be2cdc531c49632c3c249a5388016b67369cc41
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:bookworm` - linux; amd64

```console
$ docker pull pypy@sha256:3867e56c6a36df33f0ed48f5cec4808bcdf4bb07d5056066653804f40e085cdb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **385.1 MB (385126649 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e8b2df39c91c0c2755668a49e8df7424f1abaaa7411b2093034065cfcf474bcf`
-	Default Command: `["pypy3"]`

```dockerfile
# Wed, 24 Apr 2024 04:14:48 GMT
ADD file:430cca9ad155514d8c818e860e66e2aeccfb6230874d4faf446a1d0c2fc1054f in / 
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYPY_VERSION=7.3.16
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux64.tar.bz2'; 			sha256='404e6180d6caf9258eaab0c02c72018e9aa8eb03ab9094a0ff17ee5e3b265ac1'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-aarch64.tar.bz2'; 			sha256='fc720999bc5050e1d3706b3b6445e695cf42bfc71ebc7c88ed6bb88828b1d385'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux32.tar.bz2'; 			sha256='0df48aa780159e879ac89a805d143e4a6cd1b842f98046f5a3f865814bfaa2a4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-s390x.tar.bz2'; 			sha256='af97efe498a209ba18c7bc7d084164a9907fb3736588b6864955177e19d5216a'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:ca4e5d6727252f0dbc207fbf283cb95e278bf562bda42d35ce6c919583a110a0`  
		Last Modified: Tue, 23 Jul 2024 05:27:34 GMT  
		Size: 49.6 MB (49554075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:30b93c12a9c9326732b35d9e3ebe57148abe33f8fa6e25ab76867410b0ccf876`  
		Last Modified: Tue, 23 Jul 2024 06:13:16 GMT  
		Size: 24.1 MB (24050796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10d643a5fa823cd013a108b2076f4d2edf1b2a921f863b533e83ea5ed8d09bd4`  
		Last Modified: Tue, 23 Jul 2024 06:13:33 GMT  
		Size: 64.1 MB (64143199 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d6dc1019d7935fe82827434da11bf96cf14e24979f8155e73b794286f10b7f05`  
		Last Modified: Tue, 23 Jul 2024 06:14:07 GMT  
		Size: 211.2 MB (211241610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5ea41889487e03b8059c4b74629d08c620369201070ced579741a0352345c79`  
		Last Modified: Tue, 23 Jul 2024 07:16:07 GMT  
		Size: 3.0 MB (2999532 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:753fef7f25bd0b4decc2103a41230ab0c48cf2b85fff9035836ee3572e1b7210`  
		Last Modified: Tue, 23 Jul 2024 07:16:07 GMT  
		Size: 29.9 MB (29900714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ad7de4a5941d1b9dd95e31a5721cfdaaf9f46f8facadb13a173b6759815a243a`  
		Last Modified: Tue, 23 Jul 2024 07:16:07 GMT  
		Size: 3.2 MB (3236723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:601c7567eed902011728557f4a0439faaa752b7817fb438880496d83a7bb10e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15794615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe908dc8f6cb59e6a96573e52482fe1fe17ea04bce631ec3154278091f5b415`

```dockerfile
```

-	Layers:
	-	`sha256:bc861c167563c35015a4337974667a25c84d5fa4b7fe697f94e2bb0c9cbf706a`  
		Last Modified: Tue, 23 Jul 2024 07:16:07 GMT  
		Size: 15.8 MB (15768209 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:75c124818324dc0277500a607b4e62668385784c3ef79d4fe799ad22d2135a65`  
		Last Modified: Tue, 23 Jul 2024 07:16:07 GMT  
		Size: 26.4 KB (26406 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:1c91cd0f8e5fb3e3a3d99b79a46edc6dc147e0a3ba10ff3fa11e4a982b0bfc2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.2 MB (374230831 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5069d44363db35da5ef5a3bc7b7508796e8ffbfd93bc5df9c1b5f1780fc1d4ec`
-	Default Command: `["pypy3"]`

```dockerfile
# Wed, 24 Apr 2024 04:14:48 GMT
ADD file:9b83dbcd468d7cfbc9032be05a5a2c5fd57bd977997fb6c7794dfed2f5bc3bcc in / 
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYPY_VERSION=7.3.16
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux64.tar.bz2'; 			sha256='404e6180d6caf9258eaab0c02c72018e9aa8eb03ab9094a0ff17ee5e3b265ac1'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-aarch64.tar.bz2'; 			sha256='fc720999bc5050e1d3706b3b6445e695cf42bfc71ebc7c88ed6bb88828b1d385'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux32.tar.bz2'; 			sha256='0df48aa780159e879ac89a805d143e4a6cd1b842f98046f5a3f865814bfaa2a4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-s390x.tar.bz2'; 			sha256='af97efe498a209ba18c7bc7d084164a9907fb3736588b6864955177e19d5216a'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:9c5ed83eaf5c33e6b2ceb5fe1b2b1300f9117a5dc5eae13b75f9f66dcce43a0f`  
		Last Modified: Tue, 23 Jul 2024 04:20:09 GMT  
		Size: 49.6 MB (49588442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0df40ff8dff06855b2dff09ca815eb5044fdfb6861e4d23120e04f07ce113184`  
		Last Modified: Tue, 23 Jul 2024 08:10:04 GMT  
		Size: 23.6 MB (23592453 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4e903e4e709d192e5547602a5978c79692063228a98585f33fb02d343bc15719`  
		Last Modified: Tue, 23 Jul 2024 08:10:20 GMT  
		Size: 64.0 MB (63994288 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adacb995432c92df6de0b5690abdd064e095988fac45631ba8fc0a0ffa9be5cc`  
		Last Modified: Tue, 23 Jul 2024 08:10:47 GMT  
		Size: 202.6 MB (202624227 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e77c4fc7d11026a262fe4f8525a379ab348c579e9fa35ac7ec22f711d9072575`  
		Last Modified: Wed, 24 Jul 2024 02:02:12 GMT  
		Size: 3.0 MB (2989013 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91935ee91aeb7d817bee18fc08623940107a9c6a6589389ce193f27d293aaad0`  
		Last Modified: Wed, 24 Jul 2024 02:02:13 GMT  
		Size: 28.2 MB (28205685 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4820d5a2c6511a120fa07af8dd644b06e5b240984e0fae14ecb38d9c3b9771e6`  
		Last Modified: Wed, 24 Jul 2024 02:02:12 GMT  
		Size: 3.2 MB (3236723 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:4ad8505c34336a0c61e209bef101bddf7e97304e9d446fd7a05e0d64f8796280
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15823608 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51a2f458fd79119c6671a6d3e750bd32be1b443b1b85a5cb8e149d369497c781`

```dockerfile
```

-	Layers:
	-	`sha256:f87d14748400fda514f7269967353cd28a6104f2f2e98c2a23cfa5f1d2c2172c`  
		Last Modified: Wed, 24 Jul 2024 02:02:13 GMT  
		Size: 15.8 MB (15796830 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:92c10916e7f2dd9a0f7d9666e0450bbff9b7cac3c4955f144452b1618084b4d7`  
		Last Modified: Wed, 24 Jul 2024 02:02:12 GMT  
		Size: 26.8 KB (26778 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:bookworm` - linux; 386

```console
$ docker pull pypy@sha256:f2dd1f88df90a8e390d17c023f2df9f3837cc394118664a452070fd953c947b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.2 MB (384174735 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560775f2e1872de234320622b97091a6b4bdca1dce8d2fd618992db7d66a7230`
-	Default Command: `["pypy3"]`

```dockerfile
# Wed, 24 Apr 2024 04:14:48 GMT
ADD file:a8c93741bcbb0ef470eccf0a179a8d218c65cb9c2f4af52edfaef8d8fa1a61b1 in / 
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["bash"]
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV LANG=C.UTF-8
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYPY_VERSION=7.3.16
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux64.tar.bz2'; 			sha256='404e6180d6caf9258eaab0c02c72018e9aa8eb03ab9094a0ff17ee5e3b265ac1'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-aarch64.tar.bz2'; 			sha256='fc720999bc5050e1d3706b3b6445e695cf42bfc71ebc7c88ed6bb88828b1d385'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-linux32.tar.bz2'; 			sha256='0df48aa780159e879ac89a805d143e4a6cd1b842f98046f5a3f865814bfaa2a4'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.16-s390x.tar.bz2'; 			sha256='af97efe498a209ba18c7bc7d084164a9907fb3736588b6864955177e19d5216a'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 24 Apr 2024 04:14:48 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 24 Apr 2024 04:14:48 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 24 Apr 2024 04:14:48 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:3bb2cdc41130b713f05d463d0764d672f6d09232a689704dcab0b37dacbdd16c`  
		Last Modified: Tue, 23 Jul 2024 03:57:27 GMT  
		Size: 50.6 MB (50579420 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fe9de7929eb5cdfbf61ec571a39b7279b074e89cbd4a3b2ca99e81badbd5dde`  
		Last Modified: Tue, 23 Jul 2024 04:48:40 GMT  
		Size: 24.9 MB (24891462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b8378865fc9e6569272faaefe1da81649f1839f35e7c990fb8ab8e8279a807ac`  
		Last Modified: Tue, 23 Jul 2024 04:49:03 GMT  
		Size: 66.0 MB (65988807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb4a7c31652ee354c7323f3315523d185b07416d8cb4bc316907ce5389dbee90`  
		Last Modified: Tue, 23 Jul 2024 04:49:51 GMT  
		Size: 210.2 MB (210156525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7dd988d5fc460c22acc83385074a3f04537c0a9ce7e879f77c3d31a59185bb8b`  
		Last Modified: Tue, 23 Jul 2024 06:11:15 GMT  
		Size: 3.1 MB (3142616 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dedc31e36129399cf3091ba75f68031080b337d11be7090d3ccf849dec271f9`  
		Last Modified: Tue, 23 Jul 2024 06:11:16 GMT  
		Size: 26.2 MB (26179102 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b451121a6c2f30d9590bdf278e96a9c25e45f5b460bda74484fa28d71772818f`  
		Last Modified: Tue, 23 Jul 2024 06:11:16 GMT  
		Size: 3.2 MB (3236803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:5afd40395e3dd56c72f9447f53cf20e51ac8eade8180ce285800206fc98883aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15773304 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbabb957b175f3a123e46ac41311996a65ef2895633951c386fe53b999954ab5`

```dockerfile
```

-	Layers:
	-	`sha256:3c20f8c4e9d368750d42e574b3c95c06c51acf4640b1289c6b5514f278ada6c2`  
		Last Modified: Tue, 23 Jul 2024 06:11:16 GMT  
		Size: 15.7 MB (15746956 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c53720774287735210d95735ae62ebab96e55607175dc322dbf2e3a5abdde276`  
		Last Modified: Tue, 23 Jul 2024 06:11:15 GMT  
		Size: 26.3 KB (26348 bytes)  
		MIME: application/vnd.in-toto+json
