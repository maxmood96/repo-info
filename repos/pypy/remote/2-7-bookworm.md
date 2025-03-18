## `pypy:2-7-bookworm`

```console
$ docker pull pypy@sha256:322dd30db8965f53626e1b681d7538115bfb853070028f3e3ae1e63d407e0b9c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:2-7-bookworm` - linux; amd64

```console
$ docker pull pypy@sha256:5fa4b57187072eb867fb0cd0b90f944af365cd1262f9676be05dd67868a5736d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.9 MB (384881245 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b67202fdcff1209906be84bba3785274ad292bcbdd5a35d3069634041fb8abb`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:7cd785773db44407e20a679ce5439222e505475eed5b99f1910eb2cda51729ab`  
		Last Modified: Mon, 17 Mar 2025 22:17:15 GMT  
		Size: 48.5 MB (48467838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:091eb8249475f42de217265c501e0186f0a3ea7490ef7f51458c30db91fb3cac`  
		Last Modified: Mon, 17 Mar 2025 23:13:26 GMT  
		Size: 24.0 MB (24011136 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255774e0027b72d2327719e78dbad5ad8c9cf446d055e45be7fc149418470bae`  
		Last Modified: Tue, 18 Mar 2025 00:18:51 GMT  
		Size: 64.4 MB (64396484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:353e14e5cc47664fba714a7da288001d90427c705494847ac773f5cc08199451`  
		Last Modified: Tue, 18 Mar 2025 01:13:51 GMT  
		Size: 211.4 MB (211352566 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5415b0f09708f5e293562a9315516c69c9eeefe466d8908add1c833ee65d392f`  
		Last Modified: Tue, 18 Mar 2025 03:19:38 GMT  
		Size: 3.0 MB (2999535 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58d33e7881fb499ec3ee43911266c33928f019553c60d90b8f2a144a613c57c`  
		Last Modified: Tue, 18 Mar 2025 03:19:38 GMT  
		Size: 31.8 MB (31757655 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5ab900c1acd8d0e85180030c3984bcca6a699d91708667b28cecbe990cf8a49`  
		Last Modified: Tue, 18 Mar 2025 03:19:38 GMT  
		Size: 1.9 MB (1896031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:fc01eba2201f14148e36465e1b700bc462400afa4e23cd5ea6ae65a6a56feba6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15814935 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e67e6aa1979c974daea4e361212f50a4ab40ad2a103a27cba90f3d8cf336908e`

```dockerfile
```

-	Layers:
	-	`sha256:09680dddb4ce00df7ba7f3ba78ffdeaec075119a0b8dd2754037e4c6155bb683`  
		Last Modified: Tue, 18 Mar 2025 03:19:38 GMT  
		Size: 15.8 MB (15788907 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7775dd3c7f86508f181246200a5747f55ac4107320e9d7cc9f427ce2679441a3`  
		Last Modified: Tue, 18 Mar 2025 03:19:37 GMT  
		Size: 26.0 KB (26028 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:ec746712faecfc1707006ae9d222b2dce31aaeb9d6ebd2b30fbacaca8cd19d7c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **373.6 MB (373554151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08b3e4687cd85fdbacfad395fd1e794787d598bbb8918731f3629cda36af5a50`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1740355200'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:52daf8b0f06f2fdaeb7dec4b92086a6e762488b98364a36c7abb3737d5423d3a`  
		Last Modified: Tue, 25 Feb 2025 01:30:45 GMT  
		Size: 48.3 MB (48308008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5701e2b5d2b168acc741a9ff3fdb127561218f08a68ad5dcc08b3d94a22fc9e`  
		Last Modified: Tue, 25 Feb 2025 05:41:44 GMT  
		Size: 23.6 MB (23598275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:31d7468eece796ba37139bc942f068fc99cb7503eb828f59370c3421cca7d528`  
		Last Modified: Tue, 25 Feb 2025 11:54:02 GMT  
		Size: 64.4 MB (64354380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07b751934b2d539e08bbeb74286bd83b8e643f22567925a547678fa8b235fa38`  
		Last Modified: Tue, 25 Feb 2025 15:21:42 GMT  
		Size: 202.7 MB (202714510 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63c5fe28ef2f2266e044f5f6abb9a35bf6454c86211eddf915fa9855fccf7e79`  
		Last Modified: Thu, 27 Feb 2025 00:22:12 GMT  
		Size: 3.0 MB (2989463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58b5e83dd5658c97360f451dea416bc903955c81352094511c093f70410c771`  
		Last Modified: Thu, 27 Feb 2025 00:30:46 GMT  
		Size: 29.7 MB (29693495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef29f0527a620920d441cb5ea4a2545f136f4846052920cf22c61b039bc5fea`  
		Last Modified: Thu, 27 Feb 2025 00:30:45 GMT  
		Size: 1.9 MB (1896020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:f313acdb88b93b8a4041d7fcf933eaa63ce9d3c9772f34a3ee24882e6a365e2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15848363 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4523f2ac269840acd5027fcf288d6a06a6a766e9639c5124c052788f789b7fb4`

```dockerfile
```

-	Layers:
	-	`sha256:59ceba164efa60122a5abfe1071467a063fee002d6769ff3e96f54cfcc264f88`  
		Last Modified: Thu, 27 Feb 2025 00:30:45 GMT  
		Size: 15.8 MB (15822055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e59fcc96b7b0438c563b98861f9ba65dd3112ce6592a62df2160c562e94b3aca`  
		Last Modified: Thu, 27 Feb 2025 00:30:44 GMT  
		Size: 26.3 KB (26308 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:3abff1128a3e49579faa084fa7a4ade00d8b2b5f50dde662da5b6bcd0a4526a1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **383.2 MB (383249119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d86fffe6049d60956a16b453c5eeb3a03280a38596ba838d67ca7d7eefb4e3f9`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
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
	-	`sha256:7d82d447b005d877f296e10ab5f7eb61d0566163a6af327fd0114426987fef46`  
		Last Modified: Mon, 17 Mar 2025 22:17:57 GMT  
		Size: 49.5 MB (49454480 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10bac27a676efda08e5b5aa398d8105182245c036138383494ad65da58e29e4`  
		Last Modified: Mon, 17 Mar 2025 23:32:45 GMT  
		Size: 24.8 MB (24846980 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1eb868ed69ff5115af5ee8fc248b3921cbc2936c23ef4556d264cc6842793cd`  
		Last Modified: Tue, 18 Mar 2025 00:18:53 GMT  
		Size: 66.2 MB (66237259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e05e85a9740664efbffa28a6c9ab5ff6e64e564bd74dda762da2a13fc614b3`  
		Last Modified: Tue, 18 Mar 2025 01:13:58 GMT  
		Size: 210.3 MB (210299811 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:135811c380108cb8b093e697a796e2acafcc5406347a2812bfbc1e7650f8d48b`  
		Last Modified: Tue, 18 Mar 2025 03:18:30 GMT  
		Size: 3.1 MB (3142586 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:48d903a2913ba22f334741f157269f2b971d0b118c2a774a18651a070781335b`  
		Last Modified: Tue, 18 Mar 2025 03:18:30 GMT  
		Size: 27.4 MB (27371968 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:989124646f9fb1c73427d8d28409cb2439840b74ba19c77bb0ae92b134ca5a83`  
		Last Modified: Tue, 18 Mar 2025 03:18:30 GMT  
		Size: 1.9 MB (1896035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:39d189f8fe60bc7274e4259399fd73e17f773ad9a84d26792c524aa73c5697ca
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15793355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4cf7ebcf784aaf3a0d88e95a4adef8c8cb33b77b535dbee1b52c63988f90c1de`

```dockerfile
```

-	Layers:
	-	`sha256:91f8142c09f3cfcc144f7a45296a355d92e5bb79c4139a784efe0977110bc0d2`  
		Last Modified: Tue, 18 Mar 2025 03:18:30 GMT  
		Size: 15.8 MB (15767421 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:11ee819809d9aced73d189b749bc5aef5ef80dfdfb73bb86b105196d74c1a618`  
		Last Modified: Tue, 18 Mar 2025 03:18:29 GMT  
		Size: 25.9 KB (25934 bytes)  
		MIME: application/vnd.in-toto+json
