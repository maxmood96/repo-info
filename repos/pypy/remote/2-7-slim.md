## `pypy:2-7-slim`

```console
$ docker pull pypy@sha256:54e994ee2cfedad295c3c881a8ad90cf895916701836fa137b4cb9e8bfb05766
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `pypy:2-7-slim` - linux; amd64

```console
$ docker pull pypy@sha256:00d031c8548074844c6ed64eb77ebcd5ed17b5e5e47a79a5d6aa81a0c7f27765
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.6 MB (64552459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa39519c7e9fbc8f5fb41f23ee6669a7852a25d7505dc766f92e8dc11f28390c`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 09 Feb 2021 02:20:55 GMT
ADD file:d5c41bfaf15180481d8606f50799297e3f49b8a258c7c2cd988ab2bf0013272d in / 
# Tue, 09 Feb 2021 02:20:56 GMT
CMD ["bash"]
# Thu, 18 Feb 2021 23:33:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Feb 2021 23:33:06 GMT
ENV LANG=C.UTF-8
# Thu, 18 Feb 2021 23:33:06 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Feb 2021 23:33:07 GMT
ENV PYPY_VERSION=7.3.3
# Thu, 18 Feb 2021 23:36:37 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.3-linux64.tar.bz2'; 			sha256='f412b602ccd6912ddee0e7523e0e38f4b2c7a144449c2cad078cffbdb66fd7b1'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.3-aarch64.tar.bz2'; 			sha256='23b145b7cfbaeefb6ee76fc8216c83b652ab1daffac490558718edbbd60082d8'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.3-linux32.tar.bz2'; 			sha256='bfbc81874b137837a8ba8c517b97de29f5a336f7ec500c52f2bfdbd3580d1703'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		patch 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 18 Feb 2021 23:36:37 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Thu, 18 Feb 2021 23:36:37 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 18 Feb 2021 23:36:37 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 18 Feb 2021 23:36:52 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 18 Feb 2021 23:36:52 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:45b42c59be334ecda0daaa139b2f7d310e45c564c5f12263b1b8e68ec9e810ed`  
		Last Modified: Tue, 09 Feb 2021 02:26:39 GMT  
		Size: 27.1 MB (27095142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0fadefae635d359139799f191ef45075984b7d362e8fdc80a531ff11a7c8ee7`  
		Last Modified: Thu, 18 Feb 2021 23:38:26 GMT  
		Size: 2.8 MB (2757361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22e8ca9aa0e03a33ee6abe2691ab3c787592f70572934e56d13b41d24f9c54cc`  
		Last Modified: Thu, 18 Feb 2021 23:40:12 GMT  
		Size: 32.5 MB (32461062 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1857f9d7843a5629a22c706eb3086ac8e1b684ab60eb9ba1b565b8700eeff58f`  
		Last Modified: Thu, 18 Feb 2021 23:40:04 GMT  
		Size: 2.2 MB (2238894 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-7-slim` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:8cd9e292c408fd144d1f609a9d16726f97dd6ef71b137d1f06d03347014a382d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56256806 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:edb9addc2b63e58837d55abf49661c980f533919765759adb088d7f61438fc71`
-	Default Command: `["pypy"]`

```dockerfile
# Fri, 12 Mar 2021 01:53:53 GMT
ADD file:6130ddc0a939dd72c0614de4aa77de47aa16fe211274bacb31995aa1a0526164 in / 
# Fri, 12 Mar 2021 01:53:56 GMT
CMD ["bash"]
# Fri, 12 Mar 2021 13:53:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Fri, 12 Mar 2021 13:53:29 GMT
ENV LANG=C.UTF-8
# Fri, 12 Mar 2021 13:53:30 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 12 Mar 2021 13:53:30 GMT
ENV PYPY_VERSION=7.3.3
# Fri, 12 Mar 2021 14:00:29 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.3-linux64.tar.bz2'; 			sha256='f412b602ccd6912ddee0e7523e0e38f4b2c7a144449c2cad078cffbdb66fd7b1'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.3-aarch64.tar.bz2'; 			sha256='23b145b7cfbaeefb6ee76fc8216c83b652ab1daffac490558718edbbd60082d8'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.3-linux32.tar.bz2'; 			sha256='bfbc81874b137837a8ba8c517b97de29f5a336f7ec500c52f2bfdbd3580d1703'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		patch 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Fri, 12 Mar 2021 14:00:31 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Fri, 12 Mar 2021 14:00:32 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 12 Mar 2021 14:00:33 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 12 Mar 2021 14:01:04 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 12 Mar 2021 14:01:07 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:706ee5d0a6b53d9257cbea22d8409fb22c867ab3a001c65f6b8bfd37dace0e58`  
		Last Modified: Fri, 12 Mar 2021 02:01:39 GMT  
		Size: 25.9 MB (25856512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea6066cc2e1a9243c318aaa83f9a37f6c96902f9d8713f039f255dfbfc74f819`  
		Last Modified: Fri, 12 Mar 2021 14:02:43 GMT  
		Size: 2.6 MB (2626142 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a27751f74f1277f232c11d90b2af5d35802b0324dcf71d2b34560597ea4e3a07`  
		Last Modified: Fri, 12 Mar 2021 14:05:07 GMT  
		Size: 25.5 MB (25534366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab614c3af85c299004b230a2be3213f8cadd74a603222a127aea0f8177767a1`  
		Last Modified: Fri, 12 Mar 2021 14:04:56 GMT  
		Size: 2.2 MB (2239786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `pypy:2-7-slim` - linux; 386

```console
$ docker pull pypy@sha256:ef24adcafacb556f06c8194fa40c552d03d80761d4616850a4607aa099616a61
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62706447 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f3d66b74129260e68e5a10ba1c6a727eb1253bb38759063bda8ced95e44e8aa`
-	Default Command: `["pypy"]`

```dockerfile
# Tue, 09 Feb 2021 02:39:47 GMT
ADD file:61c31b1037672781ed0ecbc080ee3d49c83af49f5578b011544513fa9625698d in / 
# Tue, 09 Feb 2021 02:39:47 GMT
CMD ["bash"]
# Thu, 18 Feb 2021 23:39:55 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 18 Feb 2021 23:39:55 GMT
ENV LANG=C.UTF-8
# Thu, 18 Feb 2021 23:39:55 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 18 Feb 2021 23:39:55 GMT
ENV PYPY_VERSION=7.3.3
# Thu, 18 Feb 2021 23:43:55 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.3-linux64.tar.bz2'; 			sha256='f412b602ccd6912ddee0e7523e0e38f4b2c7a144449c2cad078cffbdb66fd7b1'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.3-aarch64.tar.bz2'; 			sha256='23b145b7cfbaeefb6ee76fc8216c83b652ab1daffac490558718edbbd60082d8'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.3-linux32.tar.bz2'; 			sha256='bfbc81874b137837a8ba8c517b97de29f5a336f7ec500c52f2bfdbd3580d1703'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		patch 		wget 		libexpat1 		libncurses5 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib-python -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 18 Feb 2021 23:43:55 GMT
ENV PYTHON_PIP_VERSION=20.3.4
# Thu, 18 Feb 2021 23:43:55 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 18 Feb 2021 23:43:55 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 18 Feb 2021 23:44:10 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $PYTHON_PIP_VERSION" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 18 Feb 2021 23:44:11 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:27cbb00346a16ea900c1049a2e5b47942c586c377179e098382c8ca1c8e87966`  
		Last Modified: Tue, 09 Feb 2021 02:45:51 GMT  
		Size: 27.8 MB (27752731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f6f64dc70898e3d1b0a2893a17cb9b35505dd9b72d8dea0519f161a1f90382a`  
		Last Modified: Thu, 18 Feb 2021 23:45:37 GMT  
		Size: 2.8 MB (2769461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06426664ee1624128c0070a7d7cdfe3d246c5b77aa24b71219588e454e61ecc5`  
		Last Modified: Thu, 18 Feb 2021 23:47:33 GMT  
		Size: 29.9 MB (29945469 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcdd694413251b411732da9426597708cfb03ee689029a246649b132d4a259d4`  
		Last Modified: Thu, 18 Feb 2021 23:47:23 GMT  
		Size: 2.2 MB (2238786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
