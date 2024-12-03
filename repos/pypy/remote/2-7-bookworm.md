## `pypy:2-7-bookworm`

```console
$ docker pull pypy@sha256:7588977e39bfaa232ed71a478a015839290d5e30fa6eb862d062f0399e3d679b
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
$ docker pull pypy@sha256:9a2051d76ea04f6c2481ea208a7f1fadec11ce5b52e3d7c77d84c9a50a03fa5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **384.5 MB (384474290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1cbd9501d6ce503f661474d477dbc28b07d3c8ab8ead29495ca5acde88ff4bd`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 10:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 10:07:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PYPY_VERSION=7.3.17
# Wed, 28 Aug 2024 10:07:11 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.17-linux64.tar.bz2'; 			sha256='9f3497f87b3372d17e447369e0016a4bec99a6b4d2a59aba774a25bfe4353474'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.17-aarch64.tar.bz2'; 			sha256='a8df5ce1650f4756933f8780870c91a0a40e7c9870d74629bf241392bcb5c2e3'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.17-linux32.tar.bz2'; 			sha256='a3aa0867cc837a34941047ece0fbb6ca190410fae6ad35fae4999d03bf178750'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 28 Aug 2024 10:07:11 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 28 Aug 2024 10:07:11 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:fdf894e782a221820acf469d425b802be26aedb5e5d26ea80a650ff6a974d488`  
		Last Modified: Tue, 03 Dec 2024 01:27:13 GMT  
		Size: 48.5 MB (48497210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bd71677db44bb63b94de61b6f1f95d5540b4ba2d6a8a6bc4d19f422b25e0c2b`  
		Last Modified: Tue, 03 Dec 2024 02:28:49 GMT  
		Size: 23.9 MB (23865876 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:551df7f94f9c131f2fec0e8063142411365f0a1c88b935b9fac22be91af227e0`  
		Last Modified: Tue, 03 Dec 2024 03:17:14 GMT  
		Size: 64.4 MB (64391508 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce82e98d553dd62ca6a12bebfe83992ae9f9ae2748275e74b66a68cc094f868b`  
		Last Modified: Tue, 03 Dec 2024 04:31:20 GMT  
		Size: 211.3 MB (211306121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f68f248591a440ca40ec436ebc7bb823b641210b421410d59a2b54ab517e2a0a`  
		Last Modified: Tue, 03 Dec 2024 05:14:39 GMT  
		Size: 3.0 MB (2999440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a327328ced09e53c105904f7a90af3a079da492369dd6ed3a862abd3bec4203`  
		Last Modified: Tue, 03 Dec 2024 05:14:40 GMT  
		Size: 31.5 MB (31518123 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72dea753c2eb1893f1db5bde7888cb28093165786d22b5f7777ee3543223b874`  
		Last Modified: Tue, 03 Dec 2024 05:14:39 GMT  
		Size: 1.9 MB (1896012 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:366f145839dfd89289a1dccf4efa93d791cb8cbdb8605b6c0f4c2a5d1e08e1dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15840151 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4585de4105826a3c28cfe3359f2f820961c0730b3ac59ca0a166967660adab44`

```dockerfile
```

-	Layers:
	-	`sha256:8acb7ffbc7f7b30cbc3d1fe0f5c17d9c2bbff19e4894151dbc056d0b5054d3cb`  
		Last Modified: Tue, 03 Dec 2024 05:14:39 GMT  
		Size: 15.8 MB (15816461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:67b9915c28ac1508c6c3523f0697ee5fc4581d5e7ba8ca21a345faa3ca113b2c`  
		Last Modified: Tue, 03 Dec 2024 05:14:38 GMT  
		Size: 23.7 KB (23690 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:26f3342a408b46a7b4cbbb6a888b51a6f199f95231ffc8d26207111d1e90a7c0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **374.6 MB (374584530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:de2136e24fc70fa5dc061b8ea1696ee24cd7d5d933200b185d4a82a6bc65d30e`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
ADD rootfs.tar.xz / # buildkit
# Wed, 10 May 2023 23:29:59 GMT
CMD ["bash"]
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 10:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 10:07:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PYPY_VERSION=7.3.17
# Wed, 28 Aug 2024 10:07:11 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.17-linux64.tar.bz2'; 			sha256='9f3497f87b3372d17e447369e0016a4bec99a6b4d2a59aba774a25bfe4353474'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.17-aarch64.tar.bz2'; 			sha256='a8df5ce1650f4756933f8780870c91a0a40e7c9870d74629bf241392bcb5c2e3'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.17-linux32.tar.bz2'; 			sha256='a3aa0867cc837a34941047ece0fbb6ca190410fae6ad35fae4999d03bf178750'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 28 Aug 2024 10:07:11 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 28 Aug 2024 10:07:11 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:1a3f1864ec54b1398987bbe673e93d8b09842ecd51e86ab87d64857b70d188b1`  
		Last Modified: Tue, 12 Nov 2024 00:56:20 GMT  
		Size: 49.6 MB (49587201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:464f864cfaa846fbe1b8a889827404e18374f805d29d77c288a813ae8c4f6d91`  
		Last Modified: Tue, 12 Nov 2024 11:16:03 GMT  
		Size: 23.6 MB (23598253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bc6ea9985d6735252067a2041e797c0dedef261a9695671fa4ef7891a96e4b5`  
		Last Modified: Wed, 13 Nov 2024 02:41:57 GMT  
		Size: 64.3 MB (64347700 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9cbd322119a1fd6eb9df75f74273f9136ccdf6317336352e605b41d5e5cf941f`  
		Last Modified: Wed, 13 Nov 2024 08:02:33 GMT  
		Size: 202.7 MB (202679406 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f33fef02f6d95f9135d3b52888016edc729e0b2cc23fa40d6ddd2a8df1c56779`  
		Last Modified: Wed, 13 Nov 2024 14:02:12 GMT  
		Size: 3.0 MB (2989332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01336e074f964af3781a1b7f0dabef6b63b93543de619c6a88ab8158cabb5d9e`  
		Last Modified: Wed, 13 Nov 2024 14:04:19 GMT  
		Size: 29.5 MB (29486604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3732ba416419ab2a34d338274160b059db1c1d4ba03e48f6785940f5599ea794`  
		Last Modified: Wed, 13 Nov 2024 14:04:18 GMT  
		Size: 1.9 MB (1896034 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:c8191108f85993f3cccf39d2bbb6d08e56059cae0f6c81e72e59b3e43f1a14d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.9 MB (15870184 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eec8bc3a98f259fddd20601ecee78d38cd401c0c541ed607852a07436e765822`

```dockerfile
```

-	Layers:
	-	`sha256:ed65fb5f9bfea432e39d251dcb2cdebf02faa56aa8c2930ba5afe5bfdd06e802`  
		Last Modified: Wed, 13 Nov 2024 14:04:18 GMT  
		Size: 15.8 MB (15846312 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:241cb81b5684cc76a5f901f7e6a024645ee51110692250db4273d8012605a586`  
		Last Modified: Wed, 13 Nov 2024 14:04:17 GMT  
		Size: 23.9 KB (23872 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:1fd86f946679d0059dc9082de08ca20f6247607db23148698029a62588c0327c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **382.7 MB (382681419 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c7f54a38d47abcd68a250d4d9bf27711e391d9fa1bfe0b0c8032cb42e7b112b`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 10 May 2023 23:29:59 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1733097600'
# Wed, 10 May 2023 23:29:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		sq 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 09 Jan 2024 01:14:25 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		default-libmysqlclient-dev 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 10:07:11 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 28 Aug 2024 10:07:11 GMT
ENV LANG=C.UTF-8
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PYPY_VERSION=7.3.17
# Wed, 28 Aug 2024 10:07:11 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.17-linux64.tar.bz2'; 			sha256='9f3497f87b3372d17e447369e0016a4bec99a6b4d2a59aba774a25bfe4353474'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.17-aarch64.tar.bz2'; 			sha256='a8df5ce1650f4756933f8780870c91a0a40e7c9870d74629bf241392bcb5c2e3'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.17-linux32.tar.bz2'; 			sha256='a3aa0867cc837a34941047ece0fbb6ca190410fae6ad35fae4999d03bf178750'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 28 Aug 2024 10:07:11 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 28 Aug 2024 10:07:11 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 28 Aug 2024 10:07:11 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:53769c348e57d646b1ec110dabf9d81a3f570afdb3b8216d1178515e4ea4ce1f`  
		Last Modified: Tue, 03 Dec 2024 01:27:09 GMT  
		Size: 49.5 MB (49476152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b0c73f75a815ce87bbf2841b694fdc4c29bcd072480b8752e8e91f0b59097b`  
		Last Modified: Tue, 03 Dec 2024 03:23:49 GMT  
		Size: 24.7 MB (24706896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a2cf0351f309a0cf554972555b46b2ed97868d801e25eeed28a9f742a5e555c`  
		Last Modified: Tue, 03 Dec 2024 04:29:18 GMT  
		Size: 66.2 MB (66211191 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:adec659d61840fa9345456f332914b715e5d645a246d8ebd23b1c1c4b49b4996`  
		Last Modified: Tue, 03 Dec 2024 05:13:33 GMT  
		Size: 210.2 MB (210222547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1f4c56265eb09b9d98d174387726d9e8411a6de5f573448d2deb6eadfb0c4ef5`  
		Last Modified: Tue, 03 Dec 2024 06:13:40 GMT  
		Size: 3.1 MB (3142670 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:834e48db3e792f742fbb4604156d55c30b84899d41d037e3484335fcb97c4c8b`  
		Last Modified: Tue, 03 Dec 2024 06:13:40 GMT  
		Size: 27.0 MB (27025928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:550db507c9cb269163380e8326a12e545fc31f421d129401eea6abed0e70e493`  
		Last Modified: Tue, 03 Dec 2024 06:13:39 GMT  
		Size: 1.9 MB (1896035 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:5b38446fc0bab7ce1548fe6a291dec8dad6d7316118e1dbda5de485bdf7fb512
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **15.8 MB (15818635 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c77a0b1748d1d7c74e9f1bdb0e9670070be9aa5bbff537f6c5109028918eaad1`

```dockerfile
```

-	Layers:
	-	`sha256:310b3b94cbb02166bef9d9f696c7ea23155ea796a4a76fafc246084eb0e01480`  
		Last Modified: Tue, 03 Dec 2024 06:13:40 GMT  
		Size: 15.8 MB (15795001 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f832cc617fb7d67ed6e145a8e80e9c5b3a98e3b31e088d64133d0c500e69578`  
		Last Modified: Tue, 03 Dec 2024 06:13:39 GMT  
		Size: 23.6 KB (23634 bytes)  
		MIME: application/vnd.in-toto+json
