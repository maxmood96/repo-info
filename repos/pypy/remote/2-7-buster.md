## `pypy:2-7-buster`

```console
$ docker pull pypy@sha256:1c282020def18567e2361a9492e9c806afadc88e15142571aa83cf6741f2ffb2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `pypy:2-7-buster` - linux; amd64

```console
$ docker pull pypy@sha256:738af8c3c9029d9830b40229145f70b6d188d2154f7f9e9f2e9284a800007e6f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **348.8 MB (348778750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2b6c43938d11f66c5794665a9a433aa48e830c1a4cc2612c33d716689561fba5`
-	Default Command: `["pypy"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:33 GMT
ADD file:dc52371b5f4608e5887e8c657ff951d1895e0047960f44b153c4a55ebf1726d5 in / 
# Thu, 09 Feb 2023 03:20:33 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 09:12:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:12:26 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 09 Feb 2023 09:12:47 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 09:13:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 14:56:20 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 14:56:20 GMT
ENV LANG=C.UTF-8
# Thu, 09 Feb 2023 14:56:20 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 14:56:20 GMT
ENV PYPY_VERSION=7.3.11
# Thu, 09 Feb 2023 15:01:45 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-linux64.tar.bz2'; 			sha256='ba8ed958a905c0735a4cfff2875c25089954dc020e087d982b0ffa5b9da316cd'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-aarch64.tar.bz2'; 			sha256='ea924da1defe9325ef760e288b04f984614e405580f5321eb6a5c8f539bd415a'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-linux32.tar.bz2'; 			sha256='30fd245fab7068c96a75b9ff1323ac55174c64fc8c4751cceb4b7a9bedc1851e'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-s390x.tar.bz2'; 			sha256='8fe9481c473178e53266983678684a70fe0c42bafc95f1807bf3ef28770316d4'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 09 Feb 2023 15:01:45 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 09 Feb 2023 15:01:45 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 09 Feb 2023 15:01:50 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 09 Feb 2023 15:01:51 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:b2404786f3febb4866f85b0c8f52b0b0b94dfdb6543e94cd65f961c68f325ff7`  
		Last Modified: Thu, 09 Feb 2023 03:25:32 GMT  
		Size: 50.4 MB (50449613 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e97ef50ee5a8f962aeac812883159a9ffe3f00819fcb446f0b1fc87d7060e16e`  
		Last Modified: Thu, 09 Feb 2023 09:19:04 GMT  
		Size: 7.9 MB (7861254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfb1477a1a0e7cfeb697ce3d2aae0e31f6af42409c4581a3c23e0df0b832da6f`  
		Last Modified: Thu, 09 Feb 2023 09:19:04 GMT  
		Size: 10.0 MB (10001378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:838447eff6a7c0b7b49fd5248bd06fe00feedb8f836c346bf3a58c0516a9502d`  
		Last Modified: Thu, 09 Feb 2023 09:19:21 GMT  
		Size: 51.9 MB (51869925 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61f659024e304142fe11bb0455df68c5526e9bd397bffc0af9947e8d09078b28`  
		Last Modified: Thu, 09 Feb 2023 09:19:53 GMT  
		Size: 191.9 MB (191923525 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14eb760bd2798157aa51c1ddce5cf93e8725d65351915745bf5665268169837f`  
		Last Modified: Thu, 09 Feb 2023 15:05:18 GMT  
		Size: 3.2 MB (3190883 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:52b1de9ca747cf107d3e9ff0de8ed5d068a055de68aeefbc3e36e3715ea70418`  
		Last Modified: Thu, 09 Feb 2023 15:08:50 GMT  
		Size: 31.6 MB (31585581 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0082fff8608c80d0151900bb4b9e977eab9729b1561254d1c3af689907c274c`  
		Last Modified: Thu, 09 Feb 2023 15:08:44 GMT  
		Size: 1.9 MB (1896591 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-7-buster` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:46ff476b839fa95390d6a9c963825874f4c1e382f60942bd7e91d9bb98fec404
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **337.4 MB (337371114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b596499cd1d9965a159694f95ed647503d7a7743b0c35c137e9aab428becd2`
-	Default Command: `["pypy"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:46 GMT
ADD file:bf5b2f8cbddd98de6093dde190b043c3e2b58a5063d1acec0aba091e7d203dbd in / 
# Wed, 01 Mar 2023 02:20:47 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 02:50:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:50:50 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Wed, 01 Mar 2023 02:51:07 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 02:52:26 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 09:38:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 09:38:19 GMT
ENV LANG=C.UTF-8
# Wed, 01 Mar 2023 09:38:19 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 09:38:19 GMT
ENV PYPY_VERSION=7.3.11
# Wed, 01 Mar 2023 09:43:11 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-linux64.tar.bz2'; 			sha256='ba8ed958a905c0735a4cfff2875c25089954dc020e087d982b0ffa5b9da316cd'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-aarch64.tar.bz2'; 			sha256='ea924da1defe9325ef760e288b04f984614e405580f5321eb6a5c8f539bd415a'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-linux32.tar.bz2'; 			sha256='30fd245fab7068c96a75b9ff1323ac55174c64fc8c4751cceb4b7a9bedc1851e'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-s390x.tar.bz2'; 			sha256='8fe9481c473178e53266983678684a70fe0c42bafc95f1807bf3ef28770316d4'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 01 Mar 2023 09:43:11 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 01 Mar 2023 09:43:11 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 01 Mar 2023 09:43:17 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 01 Mar 2023 09:43:17 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:06cfbde07ccb39d53563bd87f3c2b50f04ddd0c8f6cd52be3c7089a3413688e1`  
		Last Modified: Wed, 01 Mar 2023 02:24:34 GMT  
		Size: 49.2 MB (49240002 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a788623352140f16227efacfe9a8b497cf91ee63fa69554615640474975ca5`  
		Last Modified: Wed, 01 Mar 2023 02:57:17 GMT  
		Size: 7.7 MB (7731356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12086fb08985806514ae1e77eef44a12e303bd44b113e62dac28b16b778fc797`  
		Last Modified: Wed, 01 Mar 2023 02:57:17 GMT  
		Size: 10.0 MB (10003642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9afc4bf76406adbdc8533ba0c416f2aac77ca7db02bb6d380eaeeb778f56c5d4`  
		Last Modified: Wed, 01 Mar 2023 02:57:32 GMT  
		Size: 52.2 MB (52192055 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e7fd78b041bf9263b5362da19c99f8256c7954621d32679777cd6fcd99d86a`  
		Last Modified: Wed, 01 Mar 2023 02:57:57 GMT  
		Size: 183.5 MB (183499167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97dd8669d914297daa5725bf0cafc4254ab31e3ab353cf9e477312bb25489903`  
		Last Modified: Wed, 01 Mar 2023 09:46:49 GMT  
		Size: 3.2 MB (3196571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0a6bd9a38f9907e6f5b685fc2b67e8344ac55264bb1560b8b4da93414ecf05a`  
		Last Modified: Wed, 01 Mar 2023 09:50:08 GMT  
		Size: 29.6 MB (29611735 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd19fbe22e092beb0c5cc5379ef7de3e79cb101a63e0715d224fa955b568a48e`  
		Last Modified: Wed, 01 Mar 2023 09:50:04 GMT  
		Size: 1.9 MB (1896586 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-7-buster` - linux; 386

```console
$ docker pull pypy@sha256:b74c1470d8a87e37164221d6052c206237b62b82bdaf30463c417f90b031576f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **353.7 MB (353679804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe60d99c46cfa48bfe22d3684691c505d65166bf80108a4b24462dff9b9800e0`
-	Default Command: `["pypy"]`

```dockerfile
# Thu, 09 Feb 2023 05:13:04 GMT
ADD file:043d1820efa588dcc60e5d9c340fd1edcd43f2988435e6284844a71d4b082dc7 in / 
# Thu, 09 Feb 2023 05:13:05 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 12:19:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		netbase 		wget 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:19:34 GMT
RUN set -ex; 	if ! command -v gpg > /dev/null; then 		apt-get update; 		apt-get install -y --no-install-recommends 			gnupg 			dirmngr 		; 		rm -rf /var/lib/apt/lists/*; 	fi
# Thu, 09 Feb 2023 12:19:55 GMT
RUN apt-get update && apt-get install -y --no-install-recommends 		git 		mercurial 		openssh-client 		subversion 				procps 	&& rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:21:07 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		autoconf 		automake 		bzip2 		dpkg-dev 		file 		g++ 		gcc 		imagemagick 		libbz2-dev 		libc6-dev 		libcurl4-openssl-dev 		libdb-dev 		libevent-dev 		libffi-dev 		libgdbm-dev 		libglib2.0-dev 		libgmp-dev 		libjpeg-dev 		libkrb5-dev 		liblzma-dev 		libmagickcore-dev 		libmagickwand-dev 		libmaxminddb-dev 		libncurses5-dev 		libncursesw5-dev 		libpng-dev 		libpq-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		libtool 		libwebp-dev 		libxml2-dev 		libxslt-dev 		libyaml-dev 		make 		patch 		unzip 		xz-utils 		zlib1g-dev 				$( 			if apt-cache show 'default-libmysqlclient-dev' 2>/dev/null | grep -q '^Version:'; then 				echo 'default-libmysqlclient-dev'; 			else 				echo 'libmysqlclient-dev'; 			fi 		) 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:49:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		tcl 		tk 	; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:49:07 GMT
ENV LANG=C.UTF-8
# Thu, 09 Feb 2023 12:49:08 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 12:49:09 GMT
ENV PYPY_VERSION=7.3.11
# Thu, 09 Feb 2023 12:56:06 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-linux64.tar.bz2'; 			sha256='ba8ed958a905c0735a4cfff2875c25089954dc020e087d982b0ffa5b9da316cd'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-aarch64.tar.bz2'; 			sha256='ea924da1defe9325ef760e288b04f984614e405580f5321eb6a5c8f539bd415a'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-linux32.tar.bz2'; 			sha256='30fd245fab7068c96a75b9ff1323ac55174c64fc8c4751cceb4b7a9bedc1851e'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.11-s390x.tar.bz2'; 			sha256='8fe9481c473178e53266983678684a70fe0c42bafc95f1807bf3ef28770316d4'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 09 Feb 2023 12:56:07 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 09 Feb 2023 12:56:08 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 09 Feb 2023 12:56:16 GMT
RUN set -ex; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 09 Feb 2023 12:56:17 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:ee55492a1c0f9dc3f2620641096fc2d501a92c463492dd5598f15a6634c4d8bd`  
		Last Modified: Thu, 09 Feb 2023 05:19:04 GMT  
		Size: 51.2 MB (51207786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9c639a1af4be5a14cb0b7f03cd6e9a248f9b1a901145d74ef1197bd5f120659`  
		Last Modified: Thu, 09 Feb 2023 12:26:32 GMT  
		Size: 8.0 MB (8028080 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89b8e5198a8c3096e3eb1d43c0c95bb285a45e9ab6ec4bf86a6dd44f027fc503`  
		Last Modified: Thu, 09 Feb 2023 12:26:32 GMT  
		Size: 10.1 MB (10128155 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee671ffc16b62b20253916742257a5597e1117488577c8516f6d4dd330310870`  
		Last Modified: Thu, 09 Feb 2023 12:26:50 GMT  
		Size: 53.5 MB (53469294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32ad87c9cc1e383920aed72b139acb67776966100d0f108310b743a087e39750`  
		Last Modified: Thu, 09 Feb 2023 12:27:23 GMT  
		Size: 198.4 MB (198444592 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da574be6196f2c652fba68d455e9a15485458c8f63c691023ae16543cc437db`  
		Last Modified: Thu, 09 Feb 2023 13:02:14 GMT  
		Size: 3.1 MB (3089668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65ba3b9dcb2979ea81c4f6ac7d195771f64c982d753d6fd8089fa8a2755b9130`  
		Last Modified: Thu, 09 Feb 2023 13:06:26 GMT  
		Size: 27.4 MB (27416407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a34c835112bb7945959f7a953299db13de46c4f64dc2f095b889a692b19eb80`  
		Last Modified: Thu, 09 Feb 2023 13:06:22 GMT  
		Size: 1.9 MB (1895822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
