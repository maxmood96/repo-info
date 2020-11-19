## `hylang:pypy3.6`

```console
$ docker pull hylang@sha256:6beffa8c83887f216e04d48c9f6d2c48d274a741da90899d29bc0f2e1b512951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x

### `hylang:pypy3.6` - linux; amd64

```console
$ docker pull hylang@sha256:fcd064fde8d6803746995cc2099940a542c95b230bab01cdfd56f959cc14923e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (70953195 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:37b23b17fa782e617ed02b18271e7d73586f6fdf4a7e191e914382ced6d6310c`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 13 Oct 2020 01:39:05 GMT
ADD file:0dc53e7886c35bc21ae6c4f6cedda54d56ae9c9e9cd367678f1a72e68b3c43d4 in / 
# Tue, 13 Oct 2020 01:39:05 GMT
CMD ["bash"]
# Tue, 13 Oct 2020 18:06:25 GMT
ENV LANG=C.UTF-8
# Tue, 13 Oct 2020 18:06:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 13 Oct 2020 18:06:37 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 13 Oct 2020 18:06:37 GMT
ENV PYPY_VERSION=7.3.2
# Tue, 13 Oct 2020 18:09:15 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='d7a91f179076aaa28115ffc0a81e46c6a787785b2bc995c926fe3b02f0e9ad83' ;; 		arm64) pypyArch='aarch64'; sha256='164d6a0503c83dd328e1a6bf7fcb2b2e977c1d27c6fcc491a7174fd37bc32a12' ;; 		i386) pypyArch='linux32'; sha256='6fa871dedf5e60372231362d2ccb0f28f623d42267cabb49be11a3e10bee2726' ;; 		s390x) pypyArch='s390x'; sha256='16afbaa245c016c054d9300c19433efcc76c50664ff2c86d913ff76ed0a729dc' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://downloads.python.org/pypy/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -svT '/opt/pypy/bin/pypy3' '/usr/local/bin/pypy3'; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 20 Oct 2020 17:42:09 GMT
ENV PYTHON_PIP_VERSION=20.2.4
# Tue, 03 Nov 2020 21:30:52 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/fa7dc83944936bf09a0e4cb5d5ec852c0d256599/get-pip.py
# Tue, 03 Nov 2020 21:30:52 GMT
ENV PYTHON_GET_PIP_SHA256=6e0bb0a2c2533361d7f297ed547237caf1b7507f197835974c0dd7eba998c53c
# Tue, 03 Nov 2020 21:31:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 03 Nov 2020 21:31:09 GMT
CMD ["pypy3"]
# Tue, 03 Nov 2020 21:51:38 GMT
ENV HY_VERSION=0.19.0
# Tue, 03 Nov 2020 21:51:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Tue, 03 Nov 2020 21:51:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bb79b6b2107fea8e8a47133a660b78e3a546998fcf0427be39ac9a0af4a97e90`  
		Last Modified: Tue, 13 Oct 2020 01:48:17 GMT  
		Size: 27.1 MB (27092228 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:795c3da30e6387f289f1aeef1a99487dac12aa189a7feb30b9fd1035ddf063f0`  
		Last Modified: Tue, 13 Oct 2020 18:13:07 GMT  
		Size: 2.7 MB (2742479 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337492ae3dbc7ffb86d11ce6e6395c2efdeced40ee12c8326fb0dd835d591a86`  
		Last Modified: Tue, 13 Oct 2020 18:14:33 GMT  
		Size: 35.8 MB (35778078 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d4690e243b05b4eae0d2cdf45e49cc802638cc4b6b98348f44f41df67dac784`  
		Last Modified: Tue, 03 Nov 2020 21:33:40 GMT  
		Size: 2.4 MB (2396039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67b0393c4d98dedb0ee906afe901027836f4c9cbf9ce6aa586a313cf44d60f22`  
		Last Modified: Tue, 03 Nov 2020 21:54:39 GMT  
		Size: 2.9 MB (2944371 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.6` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:6d65819281548c77c0aa2effb8abe3179496a2dccd4b7cca9d7d1b2f6d907274
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.4 MB (63362732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:46ee2a4e470977a2e8c0d762d47eca24bcabedf6b9385e904e7c8f01226e067c`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 17 Nov 2020 20:23:31 GMT
ADD file:a70d8c01f8f04f36038968567af779883f3b5ba3147b662b7d170d80418bc23c in / 
# Tue, 17 Nov 2020 20:23:32 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 06:14:12 GMT
ENV LANG=C.UTF-8
# Wed, 18 Nov 2020 06:14:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 06:14:24 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Nov 2020 06:14:25 GMT
ENV PYPY_VERSION=7.3.2
# Wed, 18 Nov 2020 06:18:37 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='d7a91f179076aaa28115ffc0a81e46c6a787785b2bc995c926fe3b02f0e9ad83' ;; 		arm64) pypyArch='aarch64'; sha256='164d6a0503c83dd328e1a6bf7fcb2b2e977c1d27c6fcc491a7174fd37bc32a12' ;; 		i386) pypyArch='linux32'; sha256='6fa871dedf5e60372231362d2ccb0f28f623d42267cabb49be11a3e10bee2726' ;; 		s390x) pypyArch='s390x'; sha256='16afbaa245c016c054d9300c19433efcc76c50664ff2c86d913ff76ed0a729dc' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://downloads.python.org/pypy/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -svT '/opt/pypy/bin/pypy3' '/usr/local/bin/pypy3'; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 18 Nov 2020 06:18:39 GMT
ENV PYTHON_PIP_VERSION=20.2.4
# Wed, 18 Nov 2020 06:18:39 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/fa7dc83944936bf09a0e4cb5d5ec852c0d256599/get-pip.py
# Wed, 18 Nov 2020 06:18:41 GMT
ENV PYTHON_GET_PIP_SHA256=6e0bb0a2c2533361d7f297ed547237caf1b7507f197835974c0dd7eba998c53c
# Wed, 18 Nov 2020 06:19:16 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 18 Nov 2020 06:19:18 GMT
CMD ["pypy3"]
# Thu, 19 Nov 2020 02:53:07 GMT
ENV HY_VERSION=0.19.0
# Thu, 19 Nov 2020 02:53:35 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Thu, 19 Nov 2020 02:53:37 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:29ade854e0dcedde295dd89890d45271e9df839e42124558eb5283508ca70f5c`  
		Last Modified: Tue, 17 Nov 2020 20:32:02 GMT  
		Size: 25.9 MB (25862532 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32d488c40d6fb7d62c9b295053c74a83901cee290b51460f3461d44ec5a8c39b`  
		Last Modified: Wed, 18 Nov 2020 06:24:05 GMT  
		Size: 2.6 MB (2606475 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff3c01b80e541cc96c39eb6eb4b0cf6732eabc225e450e548cb08d7b483cc4c8`  
		Last Modified: Wed, 18 Nov 2020 06:25:27 GMT  
		Size: 29.6 MB (29550972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9449c7c8387d130b4ac99301a02c12c075d7d98650f38fa1ef0d6cdc5df24a2`  
		Last Modified: Wed, 18 Nov 2020 06:25:18 GMT  
		Size: 2.4 MB (2397342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:713b4f34939fe409e37ca5845f6fd87f545b74860a6bd989d29a04c2c07e4081`  
		Last Modified: Thu, 19 Nov 2020 02:56:13 GMT  
		Size: 2.9 MB (2945411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.6` - linux; 386

```console
$ docker pull hylang@sha256:0c36b825622a2d5c26e16bd4b3c699deb9e0ca7c9a347bf86bd65f0c4ae652b0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73931871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b6b64d9b0fd0f1637434aa94e5a8d1c567a95b90c9a2632fb6d7dce6d6dfdf5`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 17 Nov 2020 20:19:58 GMT
ADD file:b17dfa607fcb298beb9c58bfbb8b9b0743ceb385875776c56269db2506840edf in / 
# Tue, 17 Nov 2020 20:19:58 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 03:13:00 GMT
ENV LANG=C.UTF-8
# Wed, 18 Nov 2020 03:13:13 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 03:13:13 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Nov 2020 03:13:14 GMT
ENV PYPY_VERSION=7.3.2
# Wed, 18 Nov 2020 03:16:20 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='d7a91f179076aaa28115ffc0a81e46c6a787785b2bc995c926fe3b02f0e9ad83' ;; 		arm64) pypyArch='aarch64'; sha256='164d6a0503c83dd328e1a6bf7fcb2b2e977c1d27c6fcc491a7174fd37bc32a12' ;; 		i386) pypyArch='linux32'; sha256='6fa871dedf5e60372231362d2ccb0f28f623d42267cabb49be11a3e10bee2726' ;; 		s390x) pypyArch='s390x'; sha256='16afbaa245c016c054d9300c19433efcc76c50664ff2c86d913ff76ed0a729dc' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://downloads.python.org/pypy/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -svT '/opt/pypy/bin/pypy3' '/usr/local/bin/pypy3'; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 18 Nov 2020 03:16:20 GMT
ENV PYTHON_PIP_VERSION=20.2.4
# Wed, 18 Nov 2020 03:16:21 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/fa7dc83944936bf09a0e4cb5d5ec852c0d256599/get-pip.py
# Wed, 18 Nov 2020 03:16:21 GMT
ENV PYTHON_GET_PIP_SHA256=6e0bb0a2c2533361d7f297ed547237caf1b7507f197835974c0dd7eba998c53c
# Wed, 18 Nov 2020 03:16:48 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 18 Nov 2020 03:16:49 GMT
CMD ["pypy3"]
# Wed, 18 Nov 2020 16:42:18 GMT
ENV HY_VERSION=0.19.0
# Wed, 18 Nov 2020 16:42:29 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 18 Nov 2020 16:42:29 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e8e82c9fb36b8f3a9b8f18fe1d88e4d425d5c45968e3f2e94cdbb1255feb4878`  
		Last Modified: Tue, 17 Nov 2020 20:26:45 GMT  
		Size: 27.8 MB (27766186 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c05892d420f6daa83bbb25bbc544c83d49916a4491a2eac5e112a2b74543774`  
		Last Modified: Wed, 18 Nov 2020 03:21:06 GMT  
		Size: 2.8 MB (2752685 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6356b71e31e984d0fd533874d2d409f37e73b384fa46fb69da093b2e14bb8533`  
		Last Modified: Wed, 18 Nov 2020 03:22:41 GMT  
		Size: 38.1 MB (38072799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca1fd2f43ecb808052e8d69a356ed56db5c2a36f556ebf33d6d2980e1bff2eed`  
		Last Modified: Wed, 18 Nov 2020 03:22:19 GMT  
		Size: 2.4 MB (2395729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6c8af28d90edb061fbb010a2cf63846ae68cde5bc32947934388436b543966`  
		Last Modified: Wed, 18 Nov 2020 16:44:33 GMT  
		Size: 2.9 MB (2944472 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.6` - linux; s390x

```console
$ docker pull hylang@sha256:22cfbcb197cef0dbbd318107cb243b582659e976f0ca544292f8b1f12b4fa3a8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66223063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f42767e6a843c0e549d9c74d096c964648423e822ea0f4ad9f241cc4db8f336`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 17 Nov 2020 20:18:29 GMT
ADD file:4a3215d1c9b4afb58053c4fff8d121547890c2a71bc027992f7f960551c6acb1 in / 
# Tue, 17 Nov 2020 20:18:34 GMT
CMD ["bash"]
# Wed, 18 Nov 2020 08:45:21 GMT
ENV LANG=C.UTF-8
# Wed, 18 Nov 2020 08:45:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 18 Nov 2020 08:45:35 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 18 Nov 2020 08:45:36 GMT
ENV PYPY_VERSION=7.3.2
# Wed, 18 Nov 2020 08:46:31 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='d7a91f179076aaa28115ffc0a81e46c6a787785b2bc995c926fe3b02f0e9ad83' ;; 		arm64) pypyArch='aarch64'; sha256='164d6a0503c83dd328e1a6bf7fcb2b2e977c1d27c6fcc491a7174fd37bc32a12' ;; 		i386) pypyArch='linux32'; sha256='6fa871dedf5e60372231362d2ccb0f28f623d42267cabb49be11a3e10bee2726' ;; 		s390x) pypyArch='s390x'; sha256='16afbaa245c016c054d9300c19433efcc76c50664ff2c86d913ff76ed0a729dc' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://downloads.python.org/pypy/pypy3.6-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -svT '/opt/pypy/bin/pypy3' '/usr/local/bin/pypy3'; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 18 Nov 2020 08:46:34 GMT
ENV PYTHON_PIP_VERSION=20.2.4
# Wed, 18 Nov 2020 08:46:34 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/fa7dc83944936bf09a0e4cb5d5ec852c0d256599/get-pip.py
# Wed, 18 Nov 2020 08:46:35 GMT
ENV PYTHON_GET_PIP_SHA256=6e0bb0a2c2533361d7f297ed547237caf1b7507f197835974c0dd7eba998c53c
# Wed, 18 Nov 2020 08:47:03 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 18 Nov 2020 08:47:04 GMT
CMD ["pypy3"]
# Wed, 18 Nov 2020 22:14:56 GMT
ENV HY_VERSION=0.19.0
# Wed, 18 Nov 2020 22:15:08 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION"
# Wed, 18 Nov 2020 22:15:09 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c0d5e3cc51c0b20d3f68226f5332c9a9c2b17cce2f362ec742d4ed325ff7b530`  
		Last Modified: Tue, 17 Nov 2020 20:23:43 GMT  
		Size: 25.7 MB (25721143 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06da4eaae71448d5d56df06e497bf2c86e3c9a4ac05e252edab32b6109df773a`  
		Last Modified: Wed, 18 Nov 2020 08:51:09 GMT  
		Size: 2.4 MB (2432839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c925c0494fdcaa71c6cde8a3854824e0e4371055eb75ae10c60e3d34cb7fac5`  
		Last Modified: Wed, 18 Nov 2020 08:51:16 GMT  
		Size: 32.7 MB (32727561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a660e09e7b0fde9bb39644b82a404e8b50e6f670eba4590b0090ff87f467d8a9`  
		Last Modified: Wed, 18 Nov 2020 08:51:08 GMT  
		Size: 2.4 MB (2396445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2440f78fcd705a5f53ecd21a490e8345d55ab22935c9e5271d9f1a1e82130598`  
		Last Modified: Wed, 18 Nov 2020 22:19:41 GMT  
		Size: 2.9 MB (2945075 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
