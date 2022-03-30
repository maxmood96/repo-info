## `hylang:pypy3.7-bullseye`

```console
$ docker pull hylang@sha256:abc45a268da2d7b07cb4c49e0d92832f7ea865f397e6bf572e9938d1d5103e17
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 3
	-	linux; amd64
	-	linux; arm64 variant v8
	-	linux; 386

### `hylang:pypy3.7-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:a00c19826548b1e618f361fb55c793a6f1dc16579de9f6cf27e875e80f071998
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.8 MB (72767076 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74e950693eb745583f4f254d6f19618799e4ae393822def6e064b1e5725fdb4`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 29 Mar 2022 00:22:18 GMT
ADD file:966d3669b40f5fbaecee1ecbeb58debe19001076da5d94717080d55efbc25971 in / 
# Tue, 29 Mar 2022 00:22:19 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 18:13:59 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 18:13:59 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 18:14:00 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 18:14:00 GMT
ENV PYPY_VERSION=7.3.8
# Tue, 29 Mar 2022 18:20:32 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.8-linux64.tar.bz2'; 			sha256='409085db79a6d90bfcf4f576dca1538498e65937acfbe03bd4909bdc262ff378'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.8-aarch64-portable.tar.bz2'; 			sha256='639c76f128a856747aee23a34276fa101a7a157ea81e76394fbaf80b97dcf2f2'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.8-linux32.tar.bz2'; 			sha256='38429ec6ea1aca391821ee4fbda7358ae86de4600146643f2af2fe2c085af839'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.8-s390x.tar.bz2'; 			sha256='5c2cd3f7cf04cb96f6bcc6b02e271f5d7275867763978e66651b8d1605ef3141'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 29 Mar 2022 18:20:33 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 29 Mar 2022 18:20:33 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 29 Mar 2022 18:20:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 29 Mar 2022 18:20:43 GMT
CMD ["pypy3"]
# Wed, 30 Mar 2022 14:01:12 GMT
ENV HY_VERSION=1.0a4
# Wed, 30 Mar 2022 14:01:12 GMT
ENV HYRULE_VERSION=0.1
# Wed, 30 Mar 2022 14:01:18 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Wed, 30 Mar 2022 14:01:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c229119241af7b23b121052a1cae4c03e0a477a72ea6a7f463ad7623ff8f274b`  
		Last Modified: Tue, 29 Mar 2022 00:27:16 GMT  
		Size: 31.4 MB (31378457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4c5f06096be7051e1473e3f0a584b8f472d494b7c0a0cddefcbc4e7e8444cc`  
		Last Modified: Tue, 29 Mar 2022 18:26:18 GMT  
		Size: 1.1 MB (1066217 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:821cc9b21f43833bc091e21aceecdc6b6bcdf75e573d2d23d7a6d0544a563859`  
		Last Modified: Tue, 29 Mar 2022 18:30:37 GMT  
		Size: 35.4 MB (35401697 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a66e6b8534f108bc183c558d682ff6e053d66b538f8c816e5fd6fc82d1f821`  
		Last Modified: Tue, 29 Mar 2022 18:30:31 GMT  
		Size: 2.4 MB (2371762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf675febee6e324ce8bd1bdd7dbd5b605768ef49c6480e2b464f9ae31f862d2b`  
		Last Modified: Wed, 30 Mar 2022 14:07:25 GMT  
		Size: 2.5 MB (2548943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.7-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:5b948d50996d45f0eb644dfa04d1f3f4bbf8f658b3d5d772de1921529203cb5d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68357122 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a03b3eb537a899a029fa83d22dbd37715221a393f96c56ee28fd401d374de65`
-	Default Command: `["hy"]`

```dockerfile
# Thu, 17 Mar 2022 03:21:57 GMT
ADD file:e52e032f1ace6abd44b3647d43c1b8ae30bac6de804eef09c6ccd793057996fd in / 
# Thu, 17 Mar 2022 03:21:58 GMT
CMD ["bash"]
# Fri, 18 Mar 2022 00:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Fri, 18 Mar 2022 00:06:11 GMT
ENV LANG=C.UTF-8
# Fri, 18 Mar 2022 00:06:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 18 Mar 2022 00:06:13 GMT
ENV PYPY_VERSION=7.3.8
# Fri, 18 Mar 2022 00:14:08 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.8-linux64.tar.bz2'; 			sha256='409085db79a6d90bfcf4f576dca1538498e65937acfbe03bd4909bdc262ff378'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.8-aarch64-portable.tar.bz2'; 			sha256='639c76f128a856747aee23a34276fa101a7a157ea81e76394fbaf80b97dcf2f2'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.8-linux32.tar.bz2'; 			sha256='38429ec6ea1aca391821ee4fbda7358ae86de4600146643f2af2fe2c085af839'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.8-s390x.tar.bz2'; 			sha256='5c2cd3f7cf04cb96f6bcc6b02e271f5d7275867763978e66651b8d1605ef3141'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Fri, 18 Mar 2022 00:14:08 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 18 Mar 2022 00:14:09 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 18 Mar 2022 00:14:21 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Fri, 18 Mar 2022 00:14:22 GMT
CMD ["pypy3"]
# Fri, 18 Mar 2022 06:50:15 GMT
ENV HY_VERSION=1.0a4
# Fri, 18 Mar 2022 06:50:16 GMT
ENV HYRULE_VERSION=0.1
# Fri, 18 Mar 2022 06:50:22 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Fri, 18 Mar 2022 06:50:22 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:32252aec0777ac025a158bc2a8317650a4f2a0a875387011b1165013874f8723`  
		Last Modified: Thu, 17 Mar 2022 03:28:36 GMT  
		Size: 30.1 MB (30063013 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b29e28f3b6592a1077fba71808cf5f544fd04feb4cd65db2beb492a2af87596`  
		Last Modified: Fri, 18 Mar 2022 00:23:06 GMT  
		Size: 849.9 KB (849880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f27360ce8ab9c923ca4a808276f6055c738618ecf9eb89d5e17c3570b6723284`  
		Last Modified: Fri, 18 Mar 2022 00:27:52 GMT  
		Size: 32.7 MB (32738791 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:072c4bdb088d97486013fe25191fc3b62429e83733b0b2969d024dd46c21dba5`  
		Last Modified: Fri, 18 Mar 2022 00:27:46 GMT  
		Size: 2.2 MB (2156134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a90111ec4e0cda4906ca6e802b5f34847a226512f5fb9b1b2231a7b574e55b4a`  
		Last Modified: Fri, 18 Mar 2022 06:55:51 GMT  
		Size: 2.5 MB (2549304 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.7-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:639343d3957219523c190e4d1685fc024c9650848e02453303ab47e184791d7f
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.5 MB (72472771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90741e6b38e791358afd2c1f347d6f973160309b983121f8a96d95d1a2ea040f`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 29 Mar 2022 00:42:01 GMT
ADD file:d093057c080a13cc4370d0e786857751004b8cd3c93368742512abbee4f1de83 in / 
# Tue, 29 Mar 2022 00:42:01 GMT
CMD ["bash"]
# Tue, 29 Mar 2022 17:26:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/*
# Tue, 29 Mar 2022 17:26:06 GMT
ENV LANG=C.UTF-8
# Tue, 29 Mar 2022 17:26:07 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 29 Mar 2022 17:26:08 GMT
ENV PYPY_VERSION=7.3.8
# Tue, 29 Mar 2022 17:34:01 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.8-linux64.tar.bz2'; 			sha256='409085db79a6d90bfcf4f576dca1538498e65937acfbe03bd4909bdc262ff378'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.8-aarch64-portable.tar.bz2'; 			sha256='639c76f128a856747aee23a34276fa101a7a157ea81e76394fbaf80b97dcf2f2'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.8-linux32.tar.bz2'; 			sha256='38429ec6ea1aca391821ee4fbda7358ae86de4600146643f2af2fe2c085af839'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.7-v7.3.8-s390x.tar.bz2'; 			sha256='5c2cd3f7cf04cb96f6bcc6b02e271f5d7275867763978e66651b8d1605ef3141'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib_pypy; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { print $(NF-1) }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +
# Tue, 29 Mar 2022 17:34:01 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 29 Mar 2022 17:34:02 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 29 Mar 2022 17:34:14 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py
# Tue, 29 Mar 2022 17:34:15 GMT
CMD ["pypy3"]
# Tue, 29 Mar 2022 23:01:57 GMT
ENV HY_VERSION=1.0a4
# Tue, 29 Mar 2022 23:01:58 GMT
ENV HYRULE_VERSION=0.1
# Tue, 29 Mar 2022 23:02:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION"
# Tue, 29 Mar 2022 23:02:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:fec59da75229f638ca2878278d3859a1a8b73a20d5c0c043354eb37129ebb8bf`  
		Last Modified: Tue, 29 Mar 2022 00:49:10 GMT  
		Size: 32.4 MB (32389518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4bbda215d1a060cee485119134b79bed9bab91b0e247f757fa5b3f8a1248118`  
		Last Modified: Tue, 29 Mar 2022 17:43:18 GMT  
		Size: 873.8 KB (873843 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db850d5c97dcc6329f34e693b1e687620d5636c047be577772b111318f5ae079`  
		Last Modified: Tue, 29 Mar 2022 17:48:16 GMT  
		Size: 34.5 MB (34503492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:397ba1c88ad8712258e4e510ca31075b53799345d0b8da3588dc4337aa9f74b1`  
		Last Modified: Tue, 29 Mar 2022 17:48:11 GMT  
		Size: 2.2 MB (2156049 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75b65e35595171eaacfbe260e5dc2b625777d3ac826820c4f9167e60b9dacba5`  
		Last Modified: Tue, 29 Mar 2022 23:10:13 GMT  
		Size: 2.5 MB (2549869 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
