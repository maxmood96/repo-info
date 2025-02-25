## `hylang:1-pypy-bullseye`

```console
$ docker pull hylang@sha256:59f7b86f40e91128a740d881e48b6675952340ac989cee31247887e06a560f84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:1-pypy-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:ed21c13878cedd366a058f1e0f65b2bd9232a06a40046a16385f93af5c5434f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71924477 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0456c7477b97bc7b6c5e5a13d3de10f8928b2dcf6f6d797297e2eac45dfc4345`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 22 Jan 2025 19:41:06 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1740355200'
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
	-	`sha256:c4ff3df84a0c586964c1da8f9b9ef42e07e8fa95825627b7d9b48b34ca9023a4`  
		Last Modified: Tue, 25 Feb 2025 01:29:38 GMT  
		Size: 30.3 MB (30253930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:824b27c173db01c4192279124de2cd36027067977e630be511276cc785e7d65c`  
		Last Modified: Tue, 25 Feb 2025 02:29:46 GMT  
		Size: 862.6 KB (862592 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31e76343c23b83ae97aba1909fa572d24b01fbe7996a8a528c1444345c03a26`  
		Last Modified: Tue, 25 Feb 2025 02:29:46 GMT  
		Size: 31.1 MB (31137927 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94c0b39dafb4620fc58db37a8381ac0cfc12b7fa7b32c4bc57b72b5ead900c35`  
		Last Modified: Tue, 25 Feb 2025 02:29:46 GMT  
		Size: 3.3 MB (3306243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1fc862b5b4bb0bd05ab6f988ea6e595dd10b87b6060f291d9434c6999c373d76`  
		Last Modified: Tue, 25 Feb 2025 03:21:48 GMT  
		Size: 6.4 MB (6363785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:26a9c1105aecd7b5666eda805bbf945fcf7d8ebdc921264e298f732b4fbccf2e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709208 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:792300e25b5b8751fb413ef66353fadd3e2d4c578ecdb9338370298bf4662668`

```dockerfile
```

-	Layers:
	-	`sha256:8d0401d5bffeb2c3c5aaebc0b16655281485a9eaf07c6b4d029dec6a01aa7189`  
		Last Modified: Tue, 25 Feb 2025 03:21:48 GMT  
		Size: 2.7 MB (2699865 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bbab6028f14e9ff2a21f7415b4619f49d6c95efea30b989d77903d6540de6858`  
		Last Modified: Tue, 25 Feb 2025 03:21:48 GMT  
		Size: 9.3 KB (9343 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:f976c4816f2aa34142f632f0b80e2dde8f58e1e7c7c626fca9ff79af470fb8b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68703290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:daae6d46348f216dd7e71197e0fb7ac59374e1936ea372b164675d49ad4c63f9`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 22 Jan 2025 19:41:06 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1738540800'
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
	-	`sha256:9225a2a808e874449ee822a282882a3c331aad2f5093c1062e16494d8bce3e9a`  
		Last Modified: Tue, 04 Feb 2025 01:38:25 GMT  
		Size: 28.7 MB (28744810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a4969a1bce34493ffc6bc24d7940543e7241420f3d3f8f43badd0c29ec743847`  
		Last Modified: Fri, 07 Feb 2025 02:45:45 GMT  
		Size: 849.8 KB (849789 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49e555933e31029a88a85a9e4528e69e8b39310436d40069c5a9262b23705aeb`  
		Last Modified: Fri, 07 Feb 2025 02:45:46 GMT  
		Size: 29.4 MB (29438481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:305ce89929535f22309e580f5554f5b1b15ad0c3f65fb60bcf12cca602302700`  
		Last Modified: Fri, 07 Feb 2025 02:45:46 GMT  
		Size: 3.3 MB (3306187 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee935f6e54578937db2cc08ac836d601497bb23e0c8a0dc781a7f944c067f869`  
		Last Modified: Fri, 07 Feb 2025 03:53:34 GMT  
		Size: 6.4 MB (6364023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:f70dd634f1c94af399d389998a36160de940c078ba04938277d1ba81b84faf02
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709660 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93d690c3cf3df542d7cc83a27eb47aff32c7223081b9812c92f7d70a4edba511`

```dockerfile
```

-	Layers:
	-	`sha256:7bea624675f53e7e23eb14d1d3b98c054be70e25497e7dd7c1ba8fb53580ade6`  
		Last Modified: Fri, 07 Feb 2025 03:53:33 GMT  
		Size: 2.7 MB (2700166 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03ae11bab166a87e4b5a53e1c44a72b93f6edf03cf620e310bd71ea168f7950f`  
		Last Modified: Fri, 07 Feb 2025 03:53:33 GMT  
		Size: 9.5 KB (9494 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:b6c6c15130da8421e3e03357396dd4740ad95180823e0ba11dcb094eef658e56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69306901 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c090d4ba7c7266fe81788f3e14ef6f0054cb8c47e35923756b71853b13e1b6c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 22 Jan 2025 19:41:06 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1740355200'
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
	-	`sha256:bef9e4bcedd5ece70d65f7a4c14a67fd26dce78a05b7abbb6b607f6ff01887ee`  
		Last Modified: Tue, 25 Feb 2025 01:29:48 GMT  
		Size: 31.2 MB (31180427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c79f7e032c0b2bd60bef1ec53fb6fb13c0c750775000c83e70292f2a7d3f2170`  
		Last Modified: Tue, 25 Feb 2025 02:14:12 GMT  
		Size: 874.7 KB (874697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3daf1affa86373e6e27c0a7a6ac4f0c04dc761ee8e1f53b8fd8395ea1564d801`  
		Last Modified: Tue, 25 Feb 2025 02:14:13 GMT  
		Size: 27.6 MB (27581495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3048f99c443d716f6c490a0d027abd6ce183792ac45bec01668399274f143a6b`  
		Last Modified: Tue, 25 Feb 2025 02:14:12 GMT  
		Size: 3.3 MB (3306251 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbec02dfd559984ca4d45f1ddb37c7f0383fe0d3b025d00a5efb8b8ba1f56912`  
		Last Modified: Tue, 25 Feb 2025 03:21:06 GMT  
		Size: 6.4 MB (6364031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:bbc296594f5fea4172e446a66d36da08a485a79f867ddb3fcff736c29d18bae7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2706262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dbeb014e663f654615c04d7c377eacc3218bd54352f737082e757c39d8a9a149`

```dockerfile
```

-	Layers:
	-	`sha256:e07b076b331c8136d529429fc06d4069f8b5a3c6ecc0ec389ebc2f82c07c2f0f`  
		Last Modified: Tue, 25 Feb 2025 03:21:05 GMT  
		Size: 2.7 MB (2696971 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e9d49a87fd05ac97c5e4bb42583fd831ddd27a0dc75b3a88e1c0f3d895f98b1d`  
		Last Modified: Tue, 25 Feb 2025 03:21:05 GMT  
		Size: 9.3 KB (9291 bytes)  
		MIME: application/vnd.in-toto+json
