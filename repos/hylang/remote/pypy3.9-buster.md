## `hylang:pypy3.9-buster`

```console
$ docker pull hylang@sha256:e60b54d6788663e9c719a5fcb4b69aaeb49875f5e14d232388776fe6ba009dc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386
	-	linux; s390x

### `hylang:pypy3.9-buster` - linux; amd64

```console
$ docker pull hylang@sha256:13099f4db3dac26e23f107db5116322cdab3243c2a4dd4abba9c94cffafd6f68
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72625985 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:401af0515edd80d698b3e6c84716849f1757d8994b696e983f927c8a20bca977`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 17 Mar 2022 04:04:26 GMT
ADD file:7f5787c324936e09d339f9426eec4a0120431e2a4b6ccb0db28b94d61f074ab2 in / 
# Thu, 17 Mar 2022 04:04:27 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 08:21:25 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 08:21:25 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 08:21:25 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Mar 2022 08:21:25 GMT
ENV PYPY_VERSION=7.3.8
# Fri, 18 Mar 2022 08:21:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.8-linux64.tar.bz2'; 			sha256='129a055032bba700cd1d0acacab3659cf6b7180e25b1b2f730e792f06d5b3010'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.8-aarch64-portable.tar.bz2'; 			sha256='b7282bc4484bceae5bc4cc04e05ee4faf51cb624c8fc7a69d92e5fdf0d0c96aa'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.8-linux32.tar.bz2'; 			sha256='a0d18e4e73cc655eb02354759178b8fb161d3e53b64297d05e2fff91f7cf862d'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.8-s390x.tar.bz2'; 			sha256='37b596bfe76707ead38ffb565629697e9b6fa24e722acc3c632b41ec624f5d95'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Fri, 18 Mar 2022 08:21:58 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 18 Mar 2022 08:21:58 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 18 Mar 2022 08:22:09 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 18 Mar 2022 08:22:10 GMT
CMD ["pypy3"]
# Fri, 18 Mar 2022 22:21:51 GMT
ENV HY_VERSION=1.0a4
# Fri, 18 Mar 2022 22:21:51 GMT
ENV HYRULE_VERSION=0.1
# Fri, 18 Mar 2022 22:21:56 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Fri, 18 Mar 2022 22:21:56 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a4b007099961706d45bdb3eb0a3aab719916c3e36d6da7577b0c9060260e65f8`  
		Last Modified: Thu, 17 Mar 2022 04:10:54 GMT  
		Size: 27.2 MB (27153828 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28fe96ae6894434397f7dd0028d4fdf220122b40d493de80b3639a72e529b29`  
		Last Modified: Fri, 18 Mar 2022 08:32:47 GMT  
		Size: 2.8 MB (2757946 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad77b4b5a46d2d3240815a653b751f393334516ac392675a59bfacd34aaf344b`  
		Last Modified: Fri, 18 Mar 2022 08:32:54 GMT  
		Size: 37.2 MB (37244764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb6d6b2b1ca8e2cc997abd7b69f0d11379849afae691f61f32f51a133d499e3`  
		Last Modified: Fri, 18 Mar 2022 08:32:47 GMT  
		Size: 2.6 MB (2635189 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3556aeb0f693a6cba245ea5e315f82471c4ae8b7c5f0647bb1f0dc59bf3eddfd`  
		Last Modified: Fri, 18 Mar 2022 22:25:18 GMT  
		Size: 2.8 MB (2834258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.9-buster` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:41e189640e174c4f192cda1fcd5a9562e08f7383e7f8ff339a6b7435fab43c78
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.9 MB (67939684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23a07dcaab6f70ec38dd971e06340bbeba61514da73c4b414de5c01726d909c2`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 17 Mar 2022 03:22:22 GMT
ADD file:1c7d8cedf5dc79c676acebde5252ecd3005088a9f29e5e6be547f659f41efb1f in / 
# Thu, 17 Mar 2022 03:22:22 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 00:08:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 00:08:06 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 00:08:07 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Mar 2022 00:08:08 GMT
ENV PYPY_VERSION=7.3.8
# Fri, 18 Mar 2022 00:08:44 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.8-linux64.tar.bz2'; 			sha256='129a055032bba700cd1d0acacab3659cf6b7180e25b1b2f730e792f06d5b3010'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.8-aarch64-portable.tar.bz2'; 			sha256='b7282bc4484bceae5bc4cc04e05ee4faf51cb624c8fc7a69d92e5fdf0d0c96aa'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.8-linux32.tar.bz2'; 			sha256='a0d18e4e73cc655eb02354759178b8fb161d3e53b64297d05e2fff91f7cf862d'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.8-s390x.tar.bz2'; 			sha256='37b596bfe76707ead38ffb565629697e9b6fa24e722acc3c632b41ec624f5d95'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Fri, 18 Mar 2022 00:08:44 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 18 Mar 2022 00:08:45 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 18 Mar 2022 00:09:00 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 18 Mar 2022 00:09:01 GMT
CMD ["pypy3"]
# Fri, 18 Mar 2022 06:49:34 GMT
ENV HY_VERSION=1.0a4
# Fri, 18 Mar 2022 06:49:34 GMT
ENV HYRULE_VERSION=0.1
# Fri, 18 Mar 2022 06:49:40 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Fri, 18 Mar 2022 06:49:41 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c9277cac12165646c33f028489f2a5be3f70745382f4385cd9ed12fcc8cec183`  
		Last Modified: Thu, 17 Mar 2022 03:29:27 GMT  
		Size: 25.9 MB (25923233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0cb40d484223565238a3899f6e3d3bba4db27355cd2a2d82b19baa8d90de31`  
		Last Modified: Fri, 18 Mar 2022 00:24:04 GMT  
		Size: 2.6 MB (2626701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6628cb5f62fe292c0ee0d0b2181edb1204d5dc8e4f7f5cf634963429618aeb0d`  
		Last Modified: Fri, 18 Mar 2022 00:24:10 GMT  
		Size: 34.1 MB (34132032 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:44da25ef580e16875306cf96d8e871d1698f5d32a34f238408485a6117e9455a`  
		Last Modified: Fri, 18 Mar 2022 00:24:04 GMT  
		Size: 2.4 MB (2423433 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3c44bbeff4da16df2cc8bde48111b8ffbea16781c77ccdf3df8403f5ced8e8a`  
		Last Modified: Fri, 18 Mar 2022 06:55:05 GMT  
		Size: 2.8 MB (2834285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.9-buster` - linux; 386

```console
$ docker pull hylang@sha256:dc9b5a44ba935a35d5a28bec01171bdd22e039cc2572f63b17594accb657ce8d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.8 MB (74834134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:322ce3810fa472d3aa837c35a80cf1c50d9c2a0e330155cbad391fa02701dec5`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 29 Mar 2022 00:42:26 GMT
ADD file:bcf3d504dc285de8b639c7f4017c41a4593a6c2aa6f046c9be79e587d05b5120 in / 
# Tue, 29 Mar 2022 00:42:27 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:28:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:28:01 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:28:02 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:28:03 GMT
ENV PYPY_VERSION=7.3.8
# Tue, 29 Mar 2022 17:28:36 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.8-linux64.tar.bz2'; 			sha256='129a055032bba700cd1d0acacab3659cf6b7180e25b1b2f730e792f06d5b3010'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.8-aarch64-portable.tar.bz2'; 			sha256='b7282bc4484bceae5bc4cc04e05ee4faf51cb624c8fc7a69d92e5fdf0d0c96aa'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.8-linux32.tar.bz2'; 			sha256='a0d18e4e73cc655eb02354759178b8fb161d3e53b64297d05e2fff91f7cf862d'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.8-s390x.tar.bz2'; 			sha256='37b596bfe76707ead38ffb565629697e9b6fa24e722acc3c632b41ec624f5d95'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 29 Mar 2022 17:28:36 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 29 Mar 2022 17:28:37 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 29 Mar 2022 17:28:51 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 29 Mar 2022 17:28:52 GMT
CMD ["pypy3"]
# Tue, 29 Mar 2022 23:01:15 GMT
ENV HY_VERSION=1.0a4
# Tue, 29 Mar 2022 23:01:15 GMT
ENV HYRULE_VERSION=0.1
# Tue, 29 Mar 2022 23:01:21 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 29 Mar 2022 23:01:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:65b92490caa5e2c0588fab60d39315a2a8c09aa8ea0fe208d23f6984a47ecc03`  
		Last Modified: Tue, 29 Mar 2022 00:50:02 GMT  
		Size: 27.8 MB (27801252 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:233e5959675f3ed65989a324abc0c6349cc5b162d62ab68997dc30e78dcc3684`  
		Last Modified: Tue, 29 Mar 2022 17:44:18 GMT  
		Size: 2.8 MB (2777530 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cad9e5cafad507c2751ab4692e7a8a15cdcf7529adefc4b88f4eb5ad789fecb`  
		Last Modified: Tue, 29 Mar 2022 17:44:24 GMT  
		Size: 39.0 MB (38997807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d10392d414df51c8d010341ada899a940990022ccdaa78226cb636af7328a373`  
		Last Modified: Tue, 29 Mar 2022 17:44:18 GMT  
		Size: 2.4 MB (2423514 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d15d0f48679916c1ee6b32ad3f258a8a17eebe0324e9a760d0d06f0344b677`  
		Last Modified: Tue, 29 Mar 2022 23:09:25 GMT  
		Size: 2.8 MB (2834031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.9-buster` - linux; s390x

```console
$ docker pull hylang@sha256:d735ec26596d3645a6f242d595756a63233d44bdbf475fa23227443b1c4f7df3
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.8 MB (68790061 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2004959a444f73fb72d5585bace91add47394b8cf5247d26270de15d01958ccf`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 17 Mar 2022 03:07:30 GMT
ADD file:4342e1d9db757e91953273ac7120c9d6004d38281f9cea830898b4f35ca43517 in / 
# Thu, 17 Mar 2022 03:07:32 GMT
CMD ["bash"]
# Thu, 17 Mar 2022 18:07:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Thu, 17 Mar 2022 18:07:36 GMT
ENV LANG=C.UTF-8
# Thu, 17 Mar 2022 18:07:36 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 17 Mar 2022 18:07:36 GMT
ENV PYPY_VERSION=7.3.8
# Thu, 17 Mar 2022 18:08:00 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.8-linux64.tar.bz2'; 			sha256='129a055032bba700cd1d0acacab3659cf6b7180e25b1b2f730e792f06d5b3010'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.8-aarch64-portable.tar.bz2'; 			sha256='b7282bc4484bceae5bc4cc04e05ee4faf51cb624c8fc7a69d92e5fdf0d0c96aa'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.8-linux32.tar.bz2'; 			sha256='a0d18e4e73cc655eb02354759178b8fb161d3e53b64297d05e2fff91f7cf862d'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.8-s390x.tar.bz2'; 			sha256='37b596bfe76707ead38ffb565629697e9b6fa24e722acc3c632b41ec624f5d95'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Thu, 17 Mar 2022 18:08:02 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Thu, 17 Mar 2022 18:08:02 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Thu, 17 Mar 2022 18:08:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Thu, 17 Mar 2022 18:08:13 GMT
CMD ["pypy3"]
# Thu, 17 Mar 2022 20:44:48 GMT
ENV HY_VERSION=1.0a4
# Thu, 17 Mar 2022 20:44:48 GMT
ENV HYRULE_VERSION=0.1
# Thu, 17 Mar 2022 20:44:52 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Thu, 17 Mar 2022 20:44:52 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6f8a08956872b0f67802da3a67e007322eb963a60e0dadd736077f3ece414e1f`  
		Last Modified: Thu, 17 Mar 2022 03:13:18 GMT  
		Size: 25.8 MB (25769076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6d1788693a74d6af4c72d0963a7bcf2f42218c0d5484dcfbe9ba65f63561fcf`  
		Last Modified: Thu, 17 Mar 2022 18:12:35 GMT  
		Size: 2.5 MB (2452785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea152ba232ac8380b7baa79e73f0887c3d0b7d644d817bd449b8bb01613f1735`  
		Last Modified: Thu, 17 Mar 2022 18:12:41 GMT  
		Size: 35.1 MB (35099054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75feeae37929bc1f7e6991728df5dc3eebfc3be09ab5d46a1fac1c98478b2718`  
		Last Modified: Thu, 17 Mar 2022 18:12:35 GMT  
		Size: 2.6 MB (2634964 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e393d7dc2e4ec272631119e4fd0ef1a042131c639a354654322e0c232b0d7199`  
		Last Modified: Thu, 17 Mar 2022 20:48:43 GMT  
		Size: 2.8 MB (2834182 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
