## `pypy:2-slim-buster`

```console
$ docker pull pypy@sha256:34260b0ce3ff93ac44922e595fdb18753cfa3c13396d1429927743b2bfae8305
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `pypy:2-slim-buster` - linux; amd64

```console
$ docker pull pypy@sha256:bed742579235bbb94006bbd4fb2feb4193eea123cabaf083d79f42b950f547d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.4 MB (69399444 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2e839bc0b4ab81add398d5f75f2ae91618d7ddb7348d5dda32b6a0bcf18810c5`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 07:02:40 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 07:02:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 07:02:53 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Feb 2021 07:02:54 GMT
ENV PYPY_VERSION=7.3.3
# Tue, 09 Feb 2021 07:03:25 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='f412b602ccd6912ddee0e7523e0e38f4b2c7a144449c2cad078cffbdb66fd7b1' ;; 		arm64) pypyArch='aarch64'; sha256='23b145b7cfbaeefb6ee76fc8216c83b652ab1daffac490558718edbbd60082d8' ;; 		i386) pypyArch='linux32'; sha256='bfbc81874b137837a8ba8c517b97de29f5a336f7ec500c52f2bfdbd3580d1703' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://downloads.python.org/pypy/pypy2.7-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -svT '/opt/pypy/bin/pypy' '/usr/local/bin/pypy'; 		pypy --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 09 Feb 2021 07:03:26 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Tue, 09 Feb 2021 07:03:26 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 09 Feb 2021 07:03:26 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 09 Feb 2021 07:03:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 09 Feb 2021 07:03:43 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9282d2b6dbcd2a6663580984249860605d637eb0b52d735c13d3ec6bba70bb05`  
		Last Modified: Tue, 09 Feb 2021 07:10:05 GMT  
		Size: 2.8 MB (2757351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89d3952e9ca73b7d3df2757922deeb28393ead36987b74131b7e58e955567b5`  
		Last Modified: Tue, 09 Feb 2021 07:10:13 GMT  
		Size: 37.3 MB (37304565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a5f750164360fe09e2a28e7322fcb72656db09098bba7823eaff35afa4065f`  
		Last Modified: Tue, 09 Feb 2021 07:10:05 GMT  
		Size: 2.2 MB (2242386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-slim-buster` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:0f709358da5d97225d7232f79a7628852dafe9e7f8f038de6ce7a9ad2120a04a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.7 MB (61710951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53a0ab6f134d683ed85a746f1ba4adfb10cebc45467398cbbbb90c1fc078ae31`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 09 Feb 2021 02:41:10 GMT
ADD file:d906dedaf14d8e3874b46787f7a1dbf268bc124c4e1dd32f13f3079e12f22238 in / 
# Tue, 09 Feb 2021 02:41:13 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 14:44:12 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 14:44:23 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 14:44:24 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Feb 2021 14:44:25 GMT
ENV PYPY_VERSION=7.3.3
# Tue, 09 Feb 2021 14:45:11 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='f412b602ccd6912ddee0e7523e0e38f4b2c7a144449c2cad078cffbdb66fd7b1' ;; 		arm64) pypyArch='aarch64'; sha256='23b145b7cfbaeefb6ee76fc8216c83b652ab1daffac490558718edbbd60082d8' ;; 		i386) pypyArch='linux32'; sha256='bfbc81874b137837a8ba8c517b97de29f5a336f7ec500c52f2bfdbd3580d1703' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://downloads.python.org/pypy/pypy2.7-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -svT '/opt/pypy/bin/pypy' '/usr/local/bin/pypy'; 		pypy --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 09 Feb 2021 14:45:12 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Tue, 09 Feb 2021 14:45:13 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 09 Feb 2021 14:45:14 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 09 Feb 2021 14:45:42 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 09 Feb 2021 14:45:43 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:83c5cfdaa5385ea6fc4d31e724fd4dc5d74de847a7bdd968555b8f2c558dac0e`  
		Last Modified: Tue, 09 Feb 2021 02:47:27 GMT  
		Size: 25.9 MB (25851449 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1950c49622c7888036a1c6d11a0bbca33ccb519c05e43d1015fab879cbb0319d`  
		Last Modified: Tue, 09 Feb 2021 14:54:02 GMT  
		Size: 2.6 MB (2625965 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec6243f6769662c215207e5ffe4c6899f1cd36cfceb7a3fadd42b081f4680b4`  
		Last Modified: Tue, 09 Feb 2021 14:54:12 GMT  
		Size: 31.0 MB (30990039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ff98c6840bad73e004072059cb8a66064e0ad2d7504389d10874038c4a7afa5`  
		Last Modified: Tue, 09 Feb 2021 14:54:03 GMT  
		Size: 2.2 MB (2243498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-slim-buster` - linux; 386

```console
$ docker pull pypy@sha256:72bbf606f206b18a0026d313b6040d8c9dd5f340d9ebbee68a9d3134fb95903a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.2 MB (72154411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c531be8bcc6a38360a0574bc799c798809cc2528ee506c1da97e52588c99796d`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Tue, 09 Feb 2021 19:57:22 GMT
ENV LANG=C.UTF-8
# Tue, 09 Feb 2021 19:57:30 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 09 Feb 2021 19:57:31 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 09 Feb 2021 19:57:31 GMT
ENV PYPY_VERSION=7.3.3
# Tue, 09 Feb 2021 19:58:13 GMT
RUN set -ex; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		amd64) pypyArch='linux64'; sha256='f412b602ccd6912ddee0e7523e0e38f4b2c7a144449c2cad078cffbdb66fd7b1' ;; 		arm64) pypyArch='aarch64'; sha256='23b145b7cfbaeefb6ee76fc8216c83b652ab1daffac490558718edbbd60082d8' ;; 		i386) pypyArch='linux32'; sha256='bfbc81874b137837a8ba8c517b97de29f5a336f7ec500c52f2bfdbd3580d1703' ;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "https://downloads.python.org/pypy/pypy2.7-v${PYPY_VERSION}-${pypyArch}.tar.bz2" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum -c; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -svT '/opt/pypy/bin/pypy' '/usr/local/bin/pypy'; 		pypy --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy _lzma_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 09 Feb 2021 19:58:13 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Tue, 09 Feb 2021 19:58:14 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 09 Feb 2021 19:58:14 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 09 Feb 2021 19:58:37 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends 		wget 	; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip==$PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 09 Feb 2021 19:58:38 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ca0edcfa28bb595c9cf9e25e61469073e67daf5ce8b4e76d1549931d8600c10`  
		Last Modified: Tue, 09 Feb 2021 20:05:34 GMT  
		Size: 2.8 MB (2769421 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c5e1ca75d8727bfbb87ccdd5a44954e6ca973f6528ba5c999a1dc21a2b84e5f`  
		Last Modified: Tue, 09 Feb 2021 20:05:47 GMT  
		Size: 39.4 MB (39390054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6eb40cae560ce554ba4e4847b86160b18e0d2bb8d282e20c6a3354ffea780f57`  
		Last Modified: Tue, 09 Feb 2021 20:05:34 GMT  
		Size: 2.2 MB (2242205 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
