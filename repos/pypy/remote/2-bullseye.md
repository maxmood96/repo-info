## `pypy:2-bullseye`

```console
$ docker pull pypy@sha256:86bd5649315fc4a7e0ca370a3013496f707688e88ec9e186544657104253f246
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:2-bullseye` - linux; amd64

```console
$ docker pull pypy@sha256:3fd4447e3b290f33d9633e03b7b78b053529e08a8d6be3b502610c38ace40f20
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **358.0 MB (357989112 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:65d38cb1750ad895f49b6de2014696c6a92eb6d43665a150ccf4f442721bf0e3`
-	Default Command: `["pypy"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 17:07:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 17:07:12 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 26 Feb 2025 17:07:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-linux64.tar.bz2'; 			sha256='d38445508c2eaf14ebb380d9c1ded321c5ebeae31c7e66800173d83cb8ddf423'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-aarch64.tar.bz2'; 			sha256='fe89d4fd4af13f76dfe7315975003518cf176520e3ccec1544a88d174f50910e'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-linux32.tar.bz2'; 			sha256='cc52df02b6926bd8645c1651cd7f6637ce51c2f352d0fb3c6b9330d15194b409'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 26 Feb 2025 17:07:12 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 26 Feb 2025 17:07:12 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:23eb0befa94abc6ca44ad0270547b7bc53b5bcca6a4d44d4f9fa2a658cdbaff5`  
		Last Modified: Tue, 08 Apr 2025 00:23:40 GMT  
		Size: 53.7 MB (53748529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63a7819131060d3c79e48555fb5b04fa584b86d2fb80e3ede0864c7e6bba7d87`  
		Last Modified: Tue, 08 Apr 2025 01:24:24 GMT  
		Size: 15.8 MB (15763510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da0f843b455b9b7bececb5cfeb4ba5839d4aa47845ded1258734c375304df3d0`  
		Last Modified: Tue, 08 Apr 2025 02:13:52 GMT  
		Size: 54.8 MB (54755152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b731139994e4dbd527b938ba04d372fec4d9d7302e7f454003dc0b3485c05bb1`  
		Last Modified: Tue, 08 Apr 2025 03:17:23 GMT  
		Size: 197.1 MB (197105555 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:277ab8306bc083aab1858395aed4e6c5362c55c5c0b13510f2952da011444eb4`  
		Last Modified: Tue, 08 Apr 2025 04:16:09 GMT  
		Size: 3.0 MB (2969833 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e34136cafd3b77629c665d549e0c814160a5019f99a1ddbef4947ba207115ce`  
		Last Modified: Tue, 08 Apr 2025 04:16:09 GMT  
		Size: 31.8 MB (31750511 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae6c075d6c11aa72307ad35d4570c021df06d1745f7d59d94b984a542d9ffe31`  
		Last Modified: Tue, 08 Apr 2025 04:16:09 GMT  
		Size: 1.9 MB (1896022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-bullseye` - unknown; unknown

```console
$ docker pull pypy@sha256:cc586c98c0cf41454ed4cd127888042c64e9641dd522ac8edfff75ee5228ee97
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15415258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:49b9103f8c0a7c8f1a8e469886418482f23e8eaa2f3a8ba3886a435297e1e789`

```dockerfile
```

-	Layers:
	-	`sha256:2cb97bfc9fa7aeca2c12caf1850a4b4f868e1a75b1cc44388260949773fd498d`  
		Last Modified: Tue, 08 Apr 2025 04:16:09 GMT  
		Size: 15.4 MB (15391568 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc3ab47289a4bedb74c0f82114240149ddcda77ab2a2722bc2dae98c8549f57d`  
		Last Modified: Tue, 08 Apr 2025 04:16:09 GMT  
		Size: 23.7 KB (23690 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-bullseye` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:254d5a64cf83f4886563ec35786be7574e257f3902b4cdb9be0ee3f6ab8f2bab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **347.4 MB (347429674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c62ba3577157e564723ecf35ec73d50987e2aac87fbba8b0fe5d765b0fb8e024`
-	Default Command: `["pypy"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 17:07:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 17:07:12 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 26 Feb 2025 17:07:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-linux64.tar.bz2'; 			sha256='d38445508c2eaf14ebb380d9c1ded321c5ebeae31c7e66800173d83cb8ddf423'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-aarch64.tar.bz2'; 			sha256='fe89d4fd4af13f76dfe7315975003518cf176520e3ccec1544a88d174f50910e'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-linux32.tar.bz2'; 			sha256='cc52df02b6926bd8645c1651cd7f6637ce51c2f352d0fb3c6b9330d15194b409'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 26 Feb 2025 17:07:12 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 26 Feb 2025 17:07:12 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:75f90a7fcbe0fba15646899ff45dbbdeecc9661d3b9445f4ef346d30119fe345`  
		Last Modified: Tue, 08 Apr 2025 00:23:22 GMT  
		Size: 52.3 MB (52254222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9322dad1d7c942b6794e486e4e0b838c10dfb06247f1794d20cc703ddfee969f`  
		Last Modified: Tue, 08 Apr 2025 06:03:40 GMT  
		Size: 15.7 MB (15749086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ebaef8f9f6ff21c71a0e336a0e9a00fbb65d469480593ef8d1ef507941e6f6d`  
		Last Modified: Tue, 08 Apr 2025 12:18:43 GMT  
		Size: 54.9 MB (54850009 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:848ef88a118038c35ad53e6bc0e94192e99b916044a11fb61a40b31c77edc820`  
		Last Modified: Tue, 08 Apr 2025 15:54:19 GMT  
		Size: 190.0 MB (190022174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7713eaf54c3ded8a793c6c4e0ed3aa60786dc96ae8982a9c32116257d45b81aa`  
		Last Modified: Tue, 08 Apr 2025 19:05:01 GMT  
		Size: 3.0 MB (2974533 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff46d58d9850e25a733b1952f76f662339ada0c85353450d1bf4fa9a504820e7`  
		Last Modified: Tue, 08 Apr 2025 19:06:29 GMT  
		Size: 29.7 MB (29683625 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:edcfa0669f1b7329605596d9be4158bcab19247745d011999b63d120e3d7fc5d`  
		Last Modified: Tue, 08 Apr 2025 19:06:28 GMT  
		Size: 1.9 MB (1896025 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-bullseye` - unknown; unknown

```console
$ docker pull pypy@sha256:170d2f904c52fb08c48db7fdf54e1b0b5e60ea2258b1628a4c6759584f0e9c2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15417751 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3e2fec6bbf5d8d0f533132a3fa980275baf9c4733566cc77c741f705cca4b10`

```dockerfile
```

-	Layers:
	-	`sha256:6044f2cf23eb7b484f014668b6fa09465ddc6293a2ed45c483e3f30a1644c8f1`  
		Last Modified: Tue, 08 Apr 2025 19:06:29 GMT  
		Size: 15.4 MB (15393879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:72df55db3e615c179df7a9fe98a3e674ddd73cfb86965aa2eb35495d5688a9f5`  
		Last Modified: Tue, 08 Apr 2025 19:06:28 GMT  
		Size: 23.9 KB (23872 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-bullseye` - linux; 386

```console
$ docker pull pypy@sha256:39d20794b8c08490eecc9738e1250d01e8617b969a1b77f8b160819d800997f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **359.4 MB (359391945 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae50935684767100a893d33e7a38c2ee3109aca498ab03bfc485ea8310cef629`
-	Default Command: `["pypy"]`

```dockerfile
# Fri, 28 Apr 2023 21:58:08 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1743984000'
# Fri, 28 Apr 2023 21:58:08 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 17:07:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 17:07:12 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 26 Feb 2025 17:07:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-linux64.tar.bz2'; 			sha256='d38445508c2eaf14ebb380d9c1ded321c5ebeae31c7e66800173d83cb8ddf423'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-aarch64.tar.bz2'; 			sha256='fe89d4fd4af13f76dfe7315975003518cf176520e3ccec1544a88d174f50910e'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-linux32.tar.bz2'; 			sha256='cc52df02b6926bd8645c1651cd7f6637ce51c2f352d0fb3c6b9330d15194b409'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 26 Feb 2025 17:07:12 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 26 Feb 2025 17:07:12 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 26 Feb 2025 17:07:12 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:0606c6e417e3f273e94fb33ac515dc5e3bacfec2558aa1e3ab7b9413dd31655c`  
		Last Modified: Tue, 08 Apr 2025 00:23:00 GMT  
		Size: 54.7 MB (54684465 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:10ffef4e17cbc252fc170472ff3910647beec8b91ac9abe188d6595b2087a0dc`  
		Last Modified: Tue, 08 Apr 2025 01:24:12 GMT  
		Size: 16.3 MB (16267037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:684d7ac3a47d27aefe42d135394e4d8b703fb530ab3bd2ad6ef78b8c9beaf885`  
		Last Modified: Tue, 08 Apr 2025 02:13:59 GMT  
		Size: 56.0 MB (56047217 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f57b5c68cdb07f2657d3893b6b23c64ea31a47747ad68a064ff80bc616fdb51`  
		Last Modified: Tue, 08 Apr 2025 03:26:01 GMT  
		Size: 200.0 MB (200010627 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19ef86a5017e5ff2f7797014605f917e2fe35bf841662c293cab646c7a3ff127`  
		Last Modified: Tue, 08 Apr 2025 04:11:43 GMT  
		Size: 3.1 MB (3120302 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2c06e2d194b68cc31bd00f45c1ba2b6e2e3d82289d6d7b689ab316cc5eecc87`  
		Last Modified: Tue, 08 Apr 2025 04:11:44 GMT  
		Size: 27.4 MB (27366276 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d8fa4bf61c0563048f640c2727d5f039f283740c5d1d7ef03062c4f60c5c94f`  
		Last Modified: Tue, 08 Apr 2025 04:11:43 GMT  
		Size: 1.9 MB (1896021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-bullseye` - unknown; unknown

```console
$ docker pull pypy@sha256:41a47b191314cfb3dc0335ff96cf2b5bf10591210d7106ce156e505a56653940
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.4 MB (15403497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f4ddad6c566eb3d981ed5b0a912c2360aa46ec7db73bb5ae7876673bbaeeb01`

```dockerfile
```

-	Layers:
	-	`sha256:2177138cb25c65c99abaaca87a10836f05cb6ece77fd261e5488f162d184cbcd`  
		Last Modified: Tue, 08 Apr 2025 04:11:43 GMT  
		Size: 15.4 MB (15379864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:398f463f5e9a70196674b70be4990238ec04477cbe7c6727b15393924bb08065`  
		Last Modified: Tue, 08 Apr 2025 04:11:43 GMT  
		Size: 23.6 KB (23633 bytes)  
		MIME: application/vnd.in-toto+json
