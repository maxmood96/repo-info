## `hylang:pypy`

```console
$ docker pull hylang@sha256:b6e289fd665b1ea8cd2961d5d901571712bf1442ff6473a6403d6ca013d7b617
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 9
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.2894; amd64
	-	windows version 10.0.20348.3091; amd64
	-	windows version 10.0.17763.6775; amd64

### `hylang:pypy` - linux; amd64

```console
$ docker pull hylang@sha256:dc9f2d1080232c23dd95de4ee537ea339d7f59ad92c07eb606a32bfdfe3404a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72568173 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4714c1d03b612c2ce44e1f230a87867ecc3543718be6e53194252dd1c9da7c79`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 22 Jan 2025 19:41:06 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1738540800'
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYPY_VERSION=7.3.18
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.18-linux64.tar.bz2'; 			sha256='834ccd4544bb47112a66977add7e47f30619f74061ae990876bcba95d98c27c5'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.18-aarch64.tar.bz2'; 			sha256='e843aecd48eb06b625af67891b99e3440313cfb64c6851fc37df1e5572c8ef9e'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.18-linux32.tar.bz2'; 			sha256='34ef09a481254aad0f22bf09fd7c99efb65ffef4f79f5b4222505f55f8d9c22e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["pypy3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c29f5b76f736a8b555fd191c48d6581bb918bcd605a7cbcc76205dd6acff3260`  
		Last Modified: Tue, 04 Feb 2025 01:36:21 GMT  
		Size: 28.2 MB (28212303 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777f4149ba6f138cc89ffde9643c7a4f15377a702ad557ac3081af06e4c0855e`  
		Last Modified: Fri, 07 Feb 2025 00:31:18 GMT  
		Size: 3.5 MB (3499345 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f75a6b68c6030713805464ec33901b8b71fc3de69e0d9a8eb50527f351ae22b`  
		Last Modified: Fri, 07 Feb 2025 00:31:19 GMT  
		Size: 31.2 MB (31187263 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a210fddc6757e0147703ca3b958a029f032f83c9c5300ebb41501ebd3c0911e`  
		Last Modified: Fri, 07 Feb 2025 00:31:18 GMT  
		Size: 3.3 MB (3305462 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e58d37e1446c6a66f83f496c7582d7589e467d646bee2f85b6d676cd1cd06742`  
		Last Modified: Fri, 07 Feb 2025 01:28:39 GMT  
		Size: 6.4 MB (6363800 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy` - unknown; unknown

```console
$ docker pull hylang@sha256:37458296328bb0efee9d77c5d9f62c05a0c9fc8b46587620d0ab0b0c0feb8fac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2418753 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:10a9c1129bfc1dc57401ff81dbeecf841a3d362cb83180bdc4149730a67f422e`

```dockerfile
```

-	Layers:
	-	`sha256:f353c275b7d9287bef8e7affa79ba4836039c188839148fc5a77746abf1dbb3c`  
		Last Modified: Fri, 07 Feb 2025 01:28:38 GMT  
		Size: 2.4 MB (2406976 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7bf4c1b2399c73b5dd5e349b6edbf6b28086bb43ad1180256edd620f5fca3e7`  
		Last Modified: Fri, 07 Feb 2025 01:28:38 GMT  
		Size: 11.8 KB (11777 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:fe0caea2fc3552b751f85e0fc7fc63d536e736a006df185cb02f9548a98be647
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70511694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0363196ed70e544c158f208ed43ffe5cb5c9bbc7acf698a885190dd2ebe1e416`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 22 Jan 2025 19:41:06 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1738540800'
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYPY_VERSION=7.3.18
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.18-linux64.tar.bz2'; 			sha256='834ccd4544bb47112a66977add7e47f30619f74061ae990876bcba95d98c27c5'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.18-aarch64.tar.bz2'; 			sha256='e843aecd48eb06b625af67891b99e3440313cfb64c6851fc37df1e5572c8ef9e'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.18-linux32.tar.bz2'; 			sha256='34ef09a481254aad0f22bf09fd7c99efb65ffef4f79f5b4222505f55f8d9c22e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["pypy3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4d2547c084994a809c138e688fbe4ee14eedbc6e2defc5b1c680edd16e291473`  
		Last Modified: Tue, 04 Feb 2025 01:37:53 GMT  
		Size: 28.0 MB (28040881 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:497bdedcf866b13dbcbbcd2f62d3716bc7a9d042292f32733123efec170975ee`  
		Last Modified: Fri, 07 Feb 2025 02:43:35 GMT  
		Size: 3.3 MB (3322844 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3b7700c08b21ee91b653e90da2903d27055fd857024b92374aef9e42c534797`  
		Last Modified: Fri, 07 Feb 2025 02:43:36 GMT  
		Size: 29.5 MB (29478386 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d52a021b7ce27ceaf82061ccd73b91c7794550f5fb11d3c2eadc070d0d61518`  
		Last Modified: Fri, 07 Feb 2025 02:43:35 GMT  
		Size: 3.3 MB (3305617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d990b16d6ca65220b5a6ddc253716fed8feccbab9c0894527d0fb6149395ae`  
		Last Modified: Fri, 07 Feb 2025 03:52:46 GMT  
		Size: 6.4 MB (6363966 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy` - unknown; unknown

```console
$ docker pull hylang@sha256:7a86a5203ed5c7420419b8180c5c014165e7dd5eb39d784a68d419699365c503
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2419404 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53206da95a35dff0ec8be00cf406f42de20161b335643a33d4a750f18da03012`

```dockerfile
```

-	Layers:
	-	`sha256:7b744426ab2b3f94ca03c9a61f45be5919c32212aed9fa780961d6976497c8d5`  
		Last Modified: Fri, 07 Feb 2025 03:52:46 GMT  
		Size: 2.4 MB (2407379 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a92b629c0816e9e7f98ba10658e125d9db7ac8c2b4522d7db93fa2d5ed5c537`  
		Last Modified: Fri, 07 Feb 2025 03:52:45 GMT  
		Size: 12.0 KB (12025 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy` - linux; 386

```console
$ docker pull hylang@sha256:1e1b575e7f19cf4875c67ecc7abe18864b3ada30aad0de5cba2a2a0257126630
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70024717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79f56179573b65d4d2af16d4a561c915ce94e35e874d1cc92336803771de1e9d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 22 Jan 2025 19:41:06 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1738540800'
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
ENV LANG=C.UTF-8
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYPY_VERSION=7.3.18
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.18-linux64.tar.bz2'; 			sha256='834ccd4544bb47112a66977add7e47f30619f74061ae990876bcba95d98c27c5'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.18-aarch64.tar.bz2'; 			sha256='e843aecd48eb06b625af67891b99e3440313cfb64c6851fc37df1e5572c8ef9e'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.18-linux32.tar.bz2'; 			sha256='34ef09a481254aad0f22bf09fd7c99efb65ffef4f79f5b4222505f55f8d9c22e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 22 Jan 2025 19:41:06 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 22 Jan 2025 19:41:06 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["pypy3"]
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HY_VERSION=1.0.0
# Wed, 22 Jan 2025 19:41:06 GMT
ENV HYRULE_VERSION=0.8.0
# Wed, 22 Jan 2025 19:41:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Jan 2025 19:41:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:017cfe64ccac2698a7d3db6bf1a688fb7b86a5a050f5bb9dea3b18feac6a9231`  
		Last Modified: Tue, 04 Feb 2025 01:36:34 GMT  
		Size: 29.2 MB (29187456 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f55cfdcbc9d568675b19ed25d8c69a93b756aeec5c1e80e09cf6476f4face8b7`  
		Last Modified: Fri, 07 Feb 2025 01:28:43 GMT  
		Size: 3.5 MB (3503429 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7adc7e4b4297d427ebc4b057de8b8735229d1fae3930120d74c4b6de577b59ca`  
		Last Modified: Fri, 07 Feb 2025 01:28:44 GMT  
		Size: 27.7 MB (27664925 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b3e350f42764f9098d058f6adb0c09e8f7a7b48d4bef17e8d57a0327eabc8be`  
		Last Modified: Fri, 07 Feb 2025 01:28:43 GMT  
		Size: 3.3 MB (3305073 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f3a52e6f82f43e048529ae62e9c3ec29c0ca1ef918983eab800659b31dd4dac`  
		Last Modified: Fri, 07 Feb 2025 02:08:52 GMT  
		Size: 6.4 MB (6363834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy` - unknown; unknown

```console
$ docker pull hylang@sha256:0329d23db735166a7f5dd538aa04b88485fe150a30e694886d74ddced096829a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415738 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbe0a0d14df92163a9e858995a31a79e8ed0a54f68095f3aa74bf5fde6c96131`

```dockerfile
```

-	Layers:
	-	`sha256:e7ee08e1e0d1a4c65779738dec8256edaf2c336f816347b32db1a5cf274f0ec3`  
		Last Modified: Fri, 07 Feb 2025 02:08:51 GMT  
		Size: 2.4 MB (2404053 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:799e90a7d659cfaf328480f4dec78065aae1593e9a0baff9b9e0ea079366f859`  
		Last Modified: Fri, 07 Feb 2025 02:08:51 GMT  
		Size: 11.7 KB (11685 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy` - windows version 10.0.26100.2894; amd64

```console
$ docker pull hylang@sha256:8e755fc8590cee3463888ff7d6e625fda6ddde2de7619ed1242c6880b8d07235
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.6 GB (2554336278 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510d2b00e1ba31944917661448e0721d973437aa9a1174ac9cd2bd87404cda5c`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Mon, 13 Jan 2025 03:08:16 GMT
RUN Install update 10.0.26100.2894
# Fri, 07 Feb 2025 00:30:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 07 Feb 2025 00:31:00 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Fri, 07 Feb 2025 00:31:10 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Fri, 07 Feb 2025 00:31:10 GMT
ENV PYPY_VERSION=7.3.18
# Fri, 07 Feb 2025 00:31:29 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.10-v7.3.18-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'e7ae89c5d45efcc927425281c870d0ce62cd624628f869cb0a25a0647e39a7be'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.10-v7.3.18-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 07 Feb 2025 00:31:30 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 07 Feb 2025 00:31:30 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 07 Feb 2025 00:31:53 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 07 Feb 2025 00:31:54 GMT
CMD ["pypy"]
# Fri, 07 Feb 2025 01:32:27 GMT
ENV HY_VERSION=1.0.0
# Fri, 07 Feb 2025 01:32:27 GMT
ENV HYRULE_VERSION=0.8.0
# Fri, 07 Feb 2025 01:33:23 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 07 Feb 2025 01:33:24 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19fa0da9c657652b5d0879f62221964dd2e8f7c37691ba99bce37494e109b27e`  
		Last Modified: Tue, 14 Jan 2025 18:53:06 GMT  
		Size: 285.0 MB (284970427 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c4cb14dec3e0ab9251bd7ea553ea042daa7de499d243774be71290c0ef7e5fb`  
		Last Modified: Fri, 07 Feb 2025 00:32:01 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e6d70908d1a9924c2cf0562ce6aaa0dfe5dc037d4d8841dd213a16a73f9902`  
		Last Modified: Fri, 07 Feb 2025 00:32:00 GMT  
		Size: 390.7 KB (390694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68ed5108ce45f33de4882799916f500ac872dc7734af38d90d55f52a6cb363ec`  
		Last Modified: Fri, 07 Feb 2025 00:32:01 GMT  
		Size: 15.6 MB (15571478 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71621da484ea549c590b8dd7a49f79c16421451bfe921c204b33c2418cb40cb0`  
		Last Modified: Fri, 07 Feb 2025 00:32:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d731ed93233b4c7df8cc51b0c450340e8095a160c9547a3e739007773cedb902`  
		Last Modified: Fri, 07 Feb 2025 00:32:01 GMT  
		Size: 26.8 MB (26766231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b18fa7dbc6aa3ec7a66f01471c66a69d6d7a5bb10788c9370dbb03c97123ff`  
		Last Modified: Fri, 07 Feb 2025 00:31:58 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9815e81d638b5843a1756c5bbb03431de09d74726252e36a8714bfe552167de5`  
		Last Modified: Fri, 07 Feb 2025 00:31:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7862cf9f48ef367b8680051b29ce806714b19f60f879d54e17de5a429dec3c63`  
		Last Modified: Fri, 07 Feb 2025 00:31:59 GMT  
		Size: 4.0 MB (3971085 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b7f3fbaf3804ccd82ba77a3405f4a23c72b883da73f527afd2a66c0adea702f`  
		Last Modified: Fri, 07 Feb 2025 00:31:58 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb800cad5d59beae9e2e0dc5775404f9c8e66e0325e31f4ba1924bc3e0cd7fd4`  
		Last Modified: Fri, 07 Feb 2025 01:33:29 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9802d9db724aa9085285bd0fd2620686c7f48cc0473c81ed7c89fa488e3db76`  
		Last Modified: Fri, 07 Feb 2025 01:33:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01de75021a26a1e9771d7b7c36d3713854e254d9f57995ac22bf9506e73ab702`  
		Last Modified: Fri, 07 Feb 2025 01:33:30 GMT  
		Size: 7.3 MB (7348841 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37e6ed812452930fb2fbb3208daf72559cc09d277b6d6592a9cd65a63013936d`  
		Last Modified: Fri, 07 Feb 2025 01:33:29 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy` - windows version 10.0.20348.3091; amd64

```console
$ docker pull hylang@sha256:420919de045c9afbad06f58a7ae9ee63c0b8fdc3e70a332949392f2feabbfec0
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2316264078 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57df5c3498b7a53f931fe0122477bf6005feb27fd7bd01f977afed363d91de55`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Sun, 12 Jan 2025 10:10:43 GMT
RUN Install update 10.0.20348.3091
# Fri, 07 Feb 2025 01:27:42 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 07 Feb 2025 01:28:33 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Fri, 07 Feb 2025 01:29:03 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Fri, 07 Feb 2025 01:29:03 GMT
ENV PYPY_VERSION=7.3.18
# Fri, 07 Feb 2025 01:29:27 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.10-v7.3.18-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'e7ae89c5d45efcc927425281c870d0ce62cd624628f869cb0a25a0647e39a7be'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.10-v7.3.18-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 07 Feb 2025 01:29:28 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 07 Feb 2025 01:29:28 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 07 Feb 2025 01:29:52 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 07 Feb 2025 01:29:52 GMT
CMD ["pypy"]
# Fri, 07 Feb 2025 02:08:56 GMT
ENV HY_VERSION=1.0.0
# Fri, 07 Feb 2025 02:08:57 GMT
ENV HYRULE_VERSION=0.8.0
# Fri, 07 Feb 2025 02:10:48 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 07 Feb 2025 02:10:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:440cf16a6c1eb5c6c232aa5e54099878e9ddb01fb83b65139ec4e2618d1e00de`  
		Last Modified: Tue, 14 Jan 2025 18:44:16 GMT  
		Size: 800.2 MB (800192842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e924e29d56378a8848d89a719682b293e77c9ca6074c88d2c9326d9a17ab9d3a`  
		Last Modified: Fri, 07 Feb 2025 01:30:01 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77e858e74b0a6a67536b970b6f904a199308322d7f0631dc4a475806365315ab`  
		Last Modified: Fri, 07 Feb 2025 01:30:01 GMT  
		Size: 361.6 KB (361600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28c2aa2d8b713194f18da5c7ac37f211bbd7aaebb37c83b2598762b47c3fd2f4`  
		Last Modified: Fri, 07 Feb 2025 01:30:01 GMT  
		Size: 15.5 MB (15545135 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ef4092db5ec15864cf33f659ea35b54a3160ee63b1df3aec915bc3353d0c4b`  
		Last Modified: Fri, 07 Feb 2025 01:29:59 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb949ece6555e5480ceb85bda8e12ada48917db3a3a9c6cc2e3d00cc8f921f4`  
		Last Modified: Fri, 07 Feb 2025 01:30:01 GMT  
		Size: 26.7 MB (26713444 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9f9a9f92e5d813f3f6166937be0e53f07e1602a7a466c6efb0a3d805de1be0`  
		Last Modified: Fri, 07 Feb 2025 01:29:57 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465de4794c3996e347e1c6c7309b0bff422dfecb3e2b461113d247360c3fa075`  
		Last Modified: Fri, 07 Feb 2025 01:29:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b435ddccf92bd814a790266c049a8a21d79e90c691eea27b7123f8b0b0091fb2`  
		Last Modified: Fri, 07 Feb 2025 01:29:58 GMT  
		Size: 3.9 MB (3930108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63368a9bb861943729445d4790ce2facbae5a7c56e543a898d98fc4f8a551e73`  
		Last Modified: Fri, 07 Feb 2025 01:29:57 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aebed113dcd8c0f609f947d43f817deaead4f0f8cadcc552a0cb568078b0eecb`  
		Last Modified: Fri, 07 Feb 2025 02:10:51 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b35b76add73db37466b2f595c9b0af81b3ad38399704d92a4397a6869893e0a6`  
		Last Modified: Fri, 07 Feb 2025 02:10:51 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96e79ec4691461ca647376eb8d6a7ca232acf6c9f55984abf9aca5e6eeca4027`  
		Last Modified: Fri, 07 Feb 2025 02:10:52 GMT  
		Size: 7.3 MB (7318204 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3244dc35e8a95bdf9c94c66398556f97aa3df2eb2194f4cd21206650c5335a82`  
		Last Modified: Fri, 07 Feb 2025 02:10:51 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy` - windows version 10.0.17763.6775; amd64

```console
$ docker pull hylang@sha256:16393376160a04b6a3df01ddfa6a33a9065461cab4990cce732ceeb1bc7bc84b
```

-	Docker Version: 26.1.3
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2175981730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ccad89db3e4ec0f7b0f0ebe35dd04b53bdbcbd8787e125807d8b2dcb3456a64e`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Thu, 09 Jan 2025 09:46:25 GMT
RUN Install update 10.0.17763.6775
# Fri, 07 Feb 2025 01:27:37 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 07 Feb 2025 01:28:50 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Fri, 07 Feb 2025 01:29:24 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Fri, 07 Feb 2025 01:29:24 GMT
ENV PYPY_VERSION=7.3.18
# Fri, 07 Feb 2025 01:30:08 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.10-v7.3.18-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'e7ae89c5d45efcc927425281c870d0ce62cd624628f869cb0a25a0647e39a7be'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.10-v7.3.18-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 07 Feb 2025 01:30:09 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Fri, 07 Feb 2025 01:30:09 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Fri, 07 Feb 2025 01:30:34 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 07 Feb 2025 01:30:35 GMT
CMD ["pypy"]
# Fri, 07 Feb 2025 02:08:46 GMT
ENV HY_VERSION=1.0.0
# Fri, 07 Feb 2025 02:08:48 GMT
ENV HYRULE_VERSION=0.8.0
# Fri, 07 Feb 2025 02:10:40 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 07 Feb 2025 02:10:40 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09e6adf68d473b439b895dbef289349826f793d13a35d136c1e4a98b09d23cd4`  
		Last Modified: Tue, 14 Jan 2025 18:52:24 GMT  
		Size: 401.9 MB (401943816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a242273f77f21b19fb0b06c5daf5b41d7bbe4c7882e59253cca0b31535ff6c28`  
		Last Modified: Fri, 07 Feb 2025 01:30:39 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9922594747aa456c3887b0696a71843e9fca370ba23e4fe9caa17cb3422b241`  
		Last Modified: Fri, 07 Feb 2025 01:30:38 GMT  
		Size: 339.1 KB (339106 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7ab090bfa606c5893ed3ac874b9e378dd8f36c743fe97813b59c8884da4e75a`  
		Last Modified: Fri, 07 Feb 2025 01:30:39 GMT  
		Size: 15.5 MB (15514577 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b868c627f6ea2c43fd313ce328482a58bd298f4a56c1c0727196719798a441aa`  
		Last Modified: Fri, 07 Feb 2025 01:30:38 GMT  
		Size: 1.3 KB (1297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b52a6d59f85f0547f0d67de1286764dff4ee44f296736983879ba4f2630ad902`  
		Last Modified: Fri, 07 Feb 2025 01:30:41 GMT  
		Size: 26.7 MB (26698597 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ffb8d94c7011d703cb0f0ced55a9bf2b57697a8e876e8da5f37eb2b1e4cd0043`  
		Last Modified: Fri, 07 Feb 2025 01:30:37 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b24d1329b93c1da33fc7fb130c7fe85d20800cb3f2d5f9740085f29e3e49d5fb`  
		Last Modified: Fri, 07 Feb 2025 01:30:37 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:daa94e4486f8199b9cd9a761207237bf44f98ec0015cb2a529b2295aefaf6979`  
		Last Modified: Fri, 07 Feb 2025 01:30:38 GMT  
		Size: 3.9 MB (3913910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03604f20a1c663811a99fa6d66ba60aa01de6485025ae6c724a9e4fc1f773a7b`  
		Last Modified: Fri, 07 Feb 2025 01:30:37 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40dd46e642a73b95b9da9a3a47f60f93c7ab103ac5fc45ff8ddfdab490bdaed3`  
		Last Modified: Fri, 07 Feb 2025 02:10:45 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d1ec51888e2851db6bb2dbce2ac5ad631883122d490beb3e42d275621f9b075`  
		Last Modified: Fri, 07 Feb 2025 02:10:45 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2ea41516dd5dbe662d11ad2c1b1ea89768cd1620ed04fee8f0e60593e121042`  
		Last Modified: Fri, 07 Feb 2025 02:10:46 GMT  
		Size: 7.3 MB (7292976 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a32a662888d9bd462ad0b3ba644fb60c1db846e4f5a762192859856de367a6`  
		Last Modified: Fri, 07 Feb 2025 02:10:45 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
