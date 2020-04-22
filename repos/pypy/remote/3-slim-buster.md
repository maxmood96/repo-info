## `pypy:3-slim-buster`

```console
$ docker pull pypy@sha256:c566e2c348daba9df37f255fbf62ec0081d550ea0c47e8710fddb5d483ab9c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; 386

### `pypy:3-slim-buster` - linux; amd64

```console
$ docker pull pypy@sha256:77956924dd6bb32227183be8a516b9b9142273b9ac968baa626fda0b1c31a9c4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69297480 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7eababb04672fdfd80230418a7a89f65549eca47d367204f2acca2bb85f530ff`
-	Default Command: `["pypy3"]`

```dockerfile
# Thu, 16 Apr 2020 03:22:36 GMT
ADD file:865f9041e12eb341f0a394764ddc11db49cbc8b91d4fb57c6fb1960b68b1bb41 in / 
# Thu, 16 Apr 2020 03:22:36 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 17:55:20 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 17:55:20 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 17:55:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 17:55:27 GMT
ENV PYPY_VERSION=7.3.0
# Wed, 22 Apr 2020 19:22:42 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='d3d549e8f43de820ac3385b698b83fa59b4d7dd6cf3fe34c115f731e26ad8856' ;; 		arm64) pypyArch='aarch64'; sha256='b900241bca7152254c107a632767f49edede99ca6360b9a064141267b47ef598' ;; 		i386) pypyArch='linux32'; sha256='7045b295d38ba0b5ee65bd3f078ca249fcf1de73fedeaab2d6ad78de2eab0f0e' ;; 		ppc64el) pypyArch='ppc64le'; sha256='d6f3b701313df69483b43ebdd21b9652ae5e808b2eea5fbffe3b74b82d2e7433' ;; 		s390x) pypyArch='s390x'; sha256='0fe2f7bbf42ea88b40954d7de773a43179a44f40656f2f58201524be70699544' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2; 	find /usr/local/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		pypy3 --version; 		if [ -f /usr/local/lib_pypy/_ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		cd /usr/local/lib_pypy; 		pypy3 _ssl_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 22 Apr 2020 19:22:42 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Wed, 22 Apr 2020 19:22:42 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Wed, 22 Apr 2020 19:22:42 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Wed, 22 Apr 2020 19:22:58 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 22 Apr 2020 19:22:58 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:123275d6e508d282237a22fefa5aef822b719a06496444ea89efa65da523fc4b`  
		Last Modified: Thu, 16 Apr 2020 03:31:44 GMT  
		Size: 27.1 MB (27098147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61566ac2216597d8c2a50585312c4ee2664fbb3c769f756e3c80246e904a9564`  
		Last Modified: Thu, 16 Apr 2020 17:59:27 GMT  
		Size: 2.7 MB (2741642 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b4f11c992cadd2811614c4b074dccfda7bda696ee0395a2689fae65940e7eaf`  
		Last Modified: Wed, 22 Apr 2020 19:24:53 GMT  
		Size: 37.3 MB (37290962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a07c446ccb0c6f9691a7c041d922d653d5bdf03311feb57806eb623f4eaa21f7`  
		Last Modified: Wed, 22 Apr 2020 19:24:45 GMT  
		Size: 2.2 MB (2166729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:3-slim-buster` - linux; 386

```console
$ docker pull pypy@sha256:3a679a72a0f8025397dbf19e90ae9d601102fc6a2b8b29970fcb9d10ebc30db5
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72469694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b641716707ec94ce37e63927118fb1714e230a3ea6e9c75eb19398a41fe77276`
-	Default Command: `["pypy3"]`

```dockerfile
# Thu, 16 Apr 2020 01:39:55 GMT
ADD file:ab0bbfba6c4b56420ffffc6cdddcc4592fff018f0cd07578c7dc0a5faa49df2f in / 
# Thu, 16 Apr 2020 01:39:56 GMT
CMD ["bash"]
# Thu, 16 Apr 2020 14:43:14 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 16 Apr 2020 14:43:14 GMT
ENV LANG=C.UTF-8
# Thu, 16 Apr 2020 14:43:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 16 Apr 2020 14:43:25 GMT
ENV PYPY_VERSION=7.3.0
# Wed, 22 Apr 2020 19:41:28 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='d3d549e8f43de820ac3385b698b83fa59b4d7dd6cf3fe34c115f731e26ad8856' ;; 		arm64) pypyArch='aarch64'; sha256='b900241bca7152254c107a632767f49edede99ca6360b9a064141267b47ef598' ;; 		i386) pypyArch='linux32'; sha256='7045b295d38ba0b5ee65bd3f078ca249fcf1de73fedeaab2d6ad78de2eab0f0e' ;; 		ppc64el) pypyArch='ppc64le'; sha256='d6f3b701313df69483b43ebdd21b9652ae5e808b2eea5fbffe3b74b82d2e7433' ;; 		s390x) pypyArch='s390x'; sha256='0fe2f7bbf42ea88b40954d7de773a43179a44f40656f2f58201524be70699544' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://bitbucket.org/pypy/pypy/downloads/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	tar -xjC /usr/local --strip-components=1 -f pypy.tar.bz2; 	find /usr/local/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		pypy3 --version; 		if [ -f /usr/local/lib_pypy/_ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		cd /usr/local/lib_pypy; 		pypy3 _ssl_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 22 Apr 2020 19:41:29 GMT
ENV PYTHON_PIP_VERSION=20.0.2
# Wed, 22 Apr 2020 19:41:29 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/d59197a3c169cef378a22428a3fa99d33e080a5d/get-pip.py
# Wed, 22 Apr 2020 19:41:29 GMT
ENV PYTHON_GET_PIP_SHA256=421ac1d44c0cf9730a088e337867d974b91bdce4ea2636099275071878cc189e
# Wed, 22 Apr 2020 19:41:47 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 22 Apr 2020 19:41:47 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:75bc60a98e6523be3fadd9128c1a630cb5cbd2d2d813ee5e99dc146a3de22254`  
		Last Modified: Thu, 16 Apr 2020 01:46:20 GMT  
		Size: 27.8 MB (27753976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cad3040007e4b66c35cd82634e74126d016cd75da69a883d4d69471e3de9b67c`  
		Last Modified: Thu, 16 Apr 2020 14:48:17 GMT  
		Size: 2.8 MB (2753164 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069bcd979792a3edae931ad9e43f39a8cbf2f3d167e0b290f48f34905e183195`  
		Last Modified: Wed, 22 Apr 2020 19:43:47 GMT  
		Size: 39.8 MB (39795835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e07674d205c1d015349e2b94cd81212b8d7ca48fc171771e9bcc193e86760d`  
		Last Modified: Wed, 22 Apr 2020 19:43:35 GMT  
		Size: 2.2 MB (2166719 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
