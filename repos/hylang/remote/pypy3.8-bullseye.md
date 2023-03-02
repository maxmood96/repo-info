## `hylang:pypy3.8-bullseye`

```console
$ docker pull hylang@sha256:a718e8786eeb1833ff4ff7c51fa99634d0cd98e6d6f2c7baa0cd41b4ed01722d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `hylang:pypy3.8-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:e198588763c8c997a6a38e5d995771f6b02063fa86b4fdbe5e0d94fba0779301
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.7 MB (75668839 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b81d551ce9f726e8635425b76db5fa02771d3913ddcd420b0512fd4693e85201`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 09 Feb 2023 03:20:20 GMT
ADD file:3ea7c69e4bfac2ebb6f86baaedab31827c86a594dba8080a49928e211ad3c7a0 in / 
# Thu, 09 Feb 2023 03:20:20 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 14:55:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 14:55:21 GMT
ENV LANG=C.UTF-8
# Thu, 09 Feb 2023 14:55:21 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 14:55:21 GMT
ENV PYPY_VERSION=7.3.11
# Thu, 09 Feb 2023 14:58:56 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.11-linux64.tar.bz2'; 			sha256='470330e58ac105c094041aa07bb05676b06292bc61409e26f5c5593ebb2292d9'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.11-aarch64.tar.bz2'; 			sha256='9a2fa0b8d92b7830aa31774a9a76129b0ff81afbd22cd5c41fbdd9119e859f55'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.11-linux32.tar.bz2'; 			sha256='a79b31fce8f5bc1f9940b6777134189a1d3d18bda4b1c830384cda90077c9176'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.11-s390x.tar.bz2'; 			sha256='eab7734d86d96549866f1cba67f4f9c73c989f6a802248beebc504080d4c3fcd'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.8; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 09 Feb 2023 14:58:57 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 09 Feb 2023 14:58:57 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 09 Feb 2023 14:59:08 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 09 Feb 2023 14:59:08 GMT
CMD ["pypy3"]
# Thu, 09 Feb 2023 15:30:58 GMT
ENV HY_VERSION=0.26.0
# Thu, 09 Feb 2023 15:30:58 GMT
ENV HYRULE_VERSION=0.3.0
# Thu, 09 Feb 2023 15:31:31 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 09 Feb 2023 15:31:31 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bb263680fed18eecdc67f885094df6f589bafc19004839d7fdf141df236a61aa`  
		Last Modified: Thu, 09 Feb 2023 03:25:13 GMT  
		Size: 31.4 MB (31411810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63ce33c5baf5bc0d3ff49cf9c22ec1c4a77589fd745ae5d56ca13549c382b82f`  
		Last Modified: Thu, 09 Feb 2023 15:04:31 GMT  
		Size: 1.1 MB (1066501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9e1ff8ae45912ef451f8b492f335d0d1f740c876c0840e7de4b9bea2ab6c647`  
		Last Modified: Thu, 09 Feb 2023 15:06:38 GMT  
		Size: 35.9 MB (35891366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c0346c227bf1c8a728f3fd9e02547ba5237edcbf99e7cd5cb7fa10be315bc88`  
		Last Modified: Thu, 09 Feb 2023 15:06:33 GMT  
		Size: 3.2 MB (3170600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc621b184ce0158e63a5f2a0b6ec0bb2463d20501dbe8253ed0874287128c2ba`  
		Last Modified: Thu, 09 Feb 2023 15:38:21 GMT  
		Size: 4.1 MB (4128562 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.8-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:c53fa7d42ab1451b0abb31f9c97d0ea6d54416be9dd6d1be20a059e679d7bebb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.8 MB (71845057 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d19168d48291da070ffedc1b6aefe919b1260a967d5df1939aafcda3f135e69e`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 01 Mar 2023 02:20:39 GMT
ADD file:9dc5c6fb6431df80107eddb76fb18256d6f4a06b4b22f9a7c4bcd58476068186 in / 
# Wed, 01 Mar 2023 02:20:39 GMT
CMD ["bash"]
# Wed, 01 Mar 2023 09:37:28 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Wed, 01 Mar 2023 09:37:28 GMT
ENV LANG=C.UTF-8
# Wed, 01 Mar 2023 09:37:28 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 01 Mar 2023 09:37:29 GMT
ENV PYPY_VERSION=7.3.11
# Wed, 01 Mar 2023 09:40:48 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.11-linux64.tar.bz2'; 			sha256='470330e58ac105c094041aa07bb05676b06292bc61409e26f5c5593ebb2292d9'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.11-aarch64.tar.bz2'; 			sha256='9a2fa0b8d92b7830aa31774a9a76129b0ff81afbd22cd5c41fbdd9119e859f55'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.11-linux32.tar.bz2'; 			sha256='a79b31fce8f5bc1f9940b6777134189a1d3d18bda4b1c830384cda90077c9176'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.11-s390x.tar.bz2'; 			sha256='eab7734d86d96549866f1cba67f4f9c73c989f6a802248beebc504080d4c3fcd'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.8; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Wed, 01 Mar 2023 09:40:48 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 01 Mar 2023 09:40:48 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 01 Mar 2023 09:40:59 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Wed, 01 Mar 2023 09:41:00 GMT
CMD ["pypy3"]
# Wed, 01 Mar 2023 20:29:44 GMT
ENV HY_VERSION=0.26.0
# Wed, 01 Mar 2023 20:29:44 GMT
ENV HYRULE_VERSION=0.3.0
# Wed, 01 Mar 2023 20:30:17 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 01 Mar 2023 20:30:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:66dbba0fb1b568cc3ffd53409ba2f9f82995ab7f80e379338f3f36e4dcd223be`  
		Last Modified: Wed, 01 Mar 2023 02:24:17 GMT  
		Size: 30.1 MB (30062814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3518646ce4a40714303b2693f143fbc507b90732e3f4e9941db488366fc24f`  
		Last Modified: Wed, 01 Mar 2023 09:46:04 GMT  
		Size: 1.1 MB (1054047 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ad335d6f6418cda22c89af39e69be08bb3e99b0c57e3a6c1de4638c2664dca`  
		Last Modified: Wed, 01 Mar 2023 09:48:05 GMT  
		Size: 33.4 MB (33428966 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d202517932fab233c86365bf6b851ae41e90d2588550e1dae9b82757f7b57d21`  
		Last Modified: Wed, 01 Mar 2023 09:48:01 GMT  
		Size: 3.2 MB (3170398 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3d262d17c7fb38e7fa9a344c3f4ad239bd45d9d4cde01c6b692412c3a0b1b41`  
		Last Modified: Wed, 01 Mar 2023 20:37:38 GMT  
		Size: 4.1 MB (4128832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.8-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:7d64e2de3c8ffa5efb2eebfdaf982839a6670509f6506c3e80ac3e9b7f1604ed
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.3 MB (74338955 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:394fe6124a0266efae8ed0598865e3456b282e618e187eeea4907bba244c2ea4`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 09 Feb 2023 05:12:53 GMT
ADD file:7740abd3129d33122ce51153c0b6c3323b9cbe9ea0e81672e16b2d7b210d24e3 in / 
# Thu, 09 Feb 2023 05:12:53 GMT
CMD ["bash"]
# Thu, 09 Feb 2023 12:47:53 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 09 Feb 2023 12:47:54 GMT
ENV LANG=C.UTF-8
# Thu, 09 Feb 2023 12:47:55 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Feb 2023 12:47:56 GMT
ENV PYPY_VERSION=7.3.11
# Thu, 09 Feb 2023 12:52:22 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.11-linux64.tar.bz2'; 			sha256='470330e58ac105c094041aa07bb05676b06292bc61409e26f5c5593ebb2292d9'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.11-aarch64.tar.bz2'; 			sha256='9a2fa0b8d92b7830aa31774a9a76129b0ff81afbd22cd5c41fbdd9119e859f55'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.11-linux32.tar.bz2'; 			sha256='a79b31fce8f5bc1f9940b6777134189a1d3d18bda4b1c830384cda90077c9176'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.8-v7.3.11-s390x.tar.bz2'; 			sha256='eab7734d86d96549866f1cba67f4f9c73c989f6a802248beebc504080d4c3fcd'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.8; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 09 Feb 2023 12:52:22 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 09 Feb 2023 12:52:23 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 09 Feb 2023 12:52:39 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 09 Feb 2023 12:52:39 GMT
CMD ["pypy3"]
# Sat, 25 Feb 2023 07:15:36 GMT
ENV HY_VERSION=0.26.0
# Sat, 25 Feb 2023 07:15:36 GMT
ENV HYRULE_VERSION=0.3.0
# Sat, 25 Feb 2023 07:16:13 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Sat, 25 Feb 2023 07:16:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:20744f4988404b1dee2cd438157b288d16a89da472583c0f04332ed389b258f8`  
		Last Modified: Thu, 09 Feb 2023 05:18:42 GMT  
		Size: 32.4 MB (32396875 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31df3a210cd60162c971c6bd3748a1946ca31757d6d90f75eea3775ae6d6dce7`  
		Last Modified: Thu, 09 Feb 2023 13:01:16 GMT  
		Size: 874.3 KB (874301 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27e2593843f43ca54736fbc05b1f4058c93eed7e32b70f869e7af6743f3b0ca4`  
		Last Modified: Thu, 09 Feb 2023 13:03:48 GMT  
		Size: 34.0 MB (33987416 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:858e1a8d4729397178dd8c615df5335cc7c530f1eae8f32d8527d75205c5847f`  
		Last Modified: Thu, 09 Feb 2023 13:03:43 GMT  
		Size: 3.0 MB (2951478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d00946dbcad2fbe8d9dc47bfc1214563bf8658f502d3efb4dd2344b5c021f540`  
		Last Modified: Sat, 25 Feb 2023 07:30:49 GMT  
		Size: 4.1 MB (4128885 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
