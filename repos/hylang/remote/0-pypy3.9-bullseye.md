## `hylang:0-pypy3.9-bullseye`

```console
$ docker pull hylang@sha256:34fd98e0010f0089bbfffe4a59eb1a11be6e730873b6dfbee73014766c9e2cc4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:0-pypy3.9-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:3f6f98ce350b3e4ab2e6dd8749ea77e8c6b0782d01f98d7578c3f7ac376db777
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76902698 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f44c67f476eb10922fa30e8a0170ce00293a2608e5d0e38d714e577ecb305b5f`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 12 Dec 2023 23:44:12 GMT
ADD file:bb44d67b03db8efaeb0c4171474f441d14ff35f328f13add32b289fca062fa2f in / 
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["bash"]
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYPY_VERSION=7.3.14
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-linux64.tar.bz2'; 			sha256='febd770a616641ca8419c381c7fb224e515b892551d0db49a1231397ed38859d'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-aarch64.tar.bz2'; 			sha256='14b842f32f60ce2d9d130971f9bcbdb6875824a0e78fac36806d267e0982179c'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-linux32.tar.bz2'; 			sha256='4ad89a22369a6f2f83a7d8d047e0fc4cf5597f0921fa7afa23499ed05f663503'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-s390x.tar.bz2'; 			sha256='ba2451e9081db5bc724a05530a7f98817231de83ff6fdf15bad21a4e9b6dfeae'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["pypy3"]
# Tue, 12 Dec 2023 23:44:12 GMT
ENV HY_VERSION=0.27.0
# Tue, 12 Dec 2023 23:44:12 GMT
ENV HYRULE_VERSION=0.4.0
# Tue, 12 Dec 2023 23:44:12 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b5a0d5c14ba9ece1eecd5137c468d9a123372b0af2ed2c8c4446137730c90e5b`  
		Last Modified: Tue, 19 Dec 2023 01:25:40 GMT  
		Size: 31.4 MB (31417873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c691c786198c754759303ec7071aeed1a49a11880c1024f7ca5473216d6a38a7`  
		Last Modified: Fri, 05 Jan 2024 18:54:29 GMT  
		Size: 863.2 KB (863189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63743030a4613ee1e556eaab15ea810f86bdec5fec7a8ad6004174737ce4f86a`  
		Last Modified: Fri, 05 Jan 2024 18:54:32 GMT  
		Size: 37.0 MB (37011921 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:458c03397e19549a701f37f32c1df6f786b3f0fd403ba082c4e891b20bf76ebe`  
		Last Modified: Fri, 05 Jan 2024 18:54:29 GMT  
		Size: 3.3 MB (3301908 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d2cabe0c46b07724fb62122f5fad6be569bbba9abbe3bc68eadf17c02f5d2d8`  
		Last Modified: Fri, 05 Jan 2024 19:48:02 GMT  
		Size: 4.3 MB (4307807 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:4aa0be1a6ddbfff9970f897e594a6e612b9fc4ac076f7b14b230b140f1dbde37
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3240892 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:581477ab94c111cfbd2e113a2bff11a7deff49f11a1d05008f529feb1531b464`

```dockerfile
```

-	Layers:
	-	`sha256:62a7243a117cdcfe2f7aa737a1a9c6a8db7e031e7bfa4ee931016f68dc86a6f0`  
		Last Modified: Fri, 05 Jan 2024 19:48:02 GMT  
		Size: 3.2 MB (3232279 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:492937100b4d4d5aefbb083156b91d12437052a24d83be94960d7e92fad93d5d`  
		Last Modified: Fri, 05 Jan 2024 19:48:02 GMT  
		Size: 8.6 KB (8613 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy3.9-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:737f3ab17373f8ce1eb0f7ab145918bc3ede96cd5cdd2d9a464376d917f85b13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.2 MB (73156020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f9f50f59e35b063339c4fbc344326a4a622f1dbc97053d3c53d84e855266bf`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 12 Dec 2023 23:44:12 GMT
ADD file:4dd1c5e17a5e57644787f37e8ad290baef6c93f4f112b976f19136480a293713 in / 
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["bash"]
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYPY_VERSION=7.3.14
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-linux64.tar.bz2'; 			sha256='febd770a616641ca8419c381c7fb224e515b892551d0db49a1231397ed38859d'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-aarch64.tar.bz2'; 			sha256='14b842f32f60ce2d9d130971f9bcbdb6875824a0e78fac36806d267e0982179c'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-linux32.tar.bz2'; 			sha256='4ad89a22369a6f2f83a7d8d047e0fc4cf5597f0921fa7afa23499ed05f663503'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-s390x.tar.bz2'; 			sha256='ba2451e9081db5bc724a05530a7f98817231de83ff6fdf15bad21a4e9b6dfeae'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["pypy3"]
# Tue, 12 Dec 2023 23:44:12 GMT
ENV HY_VERSION=0.27.0
# Tue, 12 Dec 2023 23:44:12 GMT
ENV HYRULE_VERSION=0.4.0
# Tue, 12 Dec 2023 23:44:12 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2244706f264b35566276550fbc21ada79613ddfff850e372b8f5113110a67c93`  
		Last Modified: Tue, 19 Dec 2023 01:45:22 GMT  
		Size: 30.1 MB (30064052 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:420960ab036904ce670019905624e65cd0a2badab83d0a7c934820a784f459c9`  
		Last Modified: Fri, 05 Jan 2024 19:28:29 GMT  
		Size: 850.6 KB (850551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70fd3f293b34e075d2f34aaeb4aa7be100b872f2aad66934d731e538d4cb44c7`  
		Last Modified: Fri, 05 Jan 2024 19:32:37 GMT  
		Size: 34.6 MB (34631768 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:45986450cac08fc1e203156f9cbc50eed04470f5edeedbccbcebf1b5493cab4b`  
		Last Modified: Fri, 05 Jan 2024 19:32:36 GMT  
		Size: 3.3 MB (3301658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79986c5a639dc4642e8299527172f9a532cea606776db56edcca9e44e5a0f670`  
		Last Modified: Fri, 05 Jan 2024 20:29:54 GMT  
		Size: 4.3 MB (4307991 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:6477e8b16b856f9ba6467e60ada99958a2d0b36186e13c60872347243c5b0131
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3218842 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7506cccec62c5237df1244d26f11bbede1f48acc9d607ccfb0937c96bfb6edf3`

```dockerfile
```

-	Layers:
	-	`sha256:64563627ad5a3d9f57a2c2adf8eb40d7798fad21e5ebca1dcfeb0b908a9aa783`  
		Last Modified: Fri, 05 Jan 2024 20:29:54 GMT  
		Size: 3.2 MB (3210195 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9634ad2128d17603e1319b674533344423ab02b907188d1504885fe33945f414`  
		Last Modified: Fri, 05 Jan 2024 20:29:54 GMT  
		Size: 8.6 KB (8647 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:0-pypy3.9-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:6227dea14fabf26183806822a91c38b277aefa32650597ac85ccfb3a0f2db949
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76141875 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a065a4921b33383ad7d09984f7bcb4528db14b65fdab82eaff5bd13125cf6c8`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 12 Dec 2023 23:44:12 GMT
ADD file:e9c344f1bffba57e46b30e3c70e4247dcf2e9d3e0484b2768f83ffd789bf3686 in / 
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["bash"]
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
ENV LANG=C.UTF-8
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYPY_VERSION=7.3.14
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-linux64.tar.bz2'; 			sha256='febd770a616641ca8419c381c7fb224e515b892551d0db49a1231397ed38859d'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-aarch64.tar.bz2'; 			sha256='14b842f32f60ce2d9d130971f9bcbdb6875824a0e78fac36806d267e0982179c'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-linux32.tar.bz2'; 			sha256='4ad89a22369a6f2f83a7d8d047e0fc4cf5597f0921fa7afa23499ed05f663503'; 			;; 		's390x') 			url='https://downloads.python.org/pypy/pypy3.9-v7.3.14-s390x.tar.bz2'; 			sha256='ba2451e9081db5bc724a05530a7f98817231de83ff6fdf15bad21a4e9b6dfeae'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.9; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Tue, 12 Dec 2023 23:44:12 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Tue, 12 Dec 2023 23:44:12 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["pypy3"]
# Tue, 12 Dec 2023 23:44:12 GMT
ENV HY_VERSION=0.27.0
# Tue, 12 Dec 2023 23:44:12 GMT
ENV HYRULE_VERSION=0.4.0
# Tue, 12 Dec 2023 23:44:12 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 12 Dec 2023 23:44:12 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e5808d881ded1b1deb8675903e6776c5a725d22c8a5c1061a96c74338f07591f`  
		Last Modified: Tue, 19 Dec 2023 01:44:31 GMT  
		Size: 32.4 MB (32402688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7cbc704eae8c3598a175c08a95927fcfc82dda45e163a1b03bca863ab7850639`  
		Last Modified: Fri, 05 Jan 2024 18:54:30 GMT  
		Size: 875.5 KB (875488 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ccbf46da6e1823b77945abb1559c1ebb59db95aef66244a4378ba83e1067356b`  
		Last Modified: Fri, 05 Jan 2024 18:54:31 GMT  
		Size: 35.3 MB (35254320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1fbdf780a2f77e9dbbc3d95260e24b60357c8c6342b2d24c0572b66731f138a`  
		Last Modified: Fri, 05 Jan 2024 18:54:30 GMT  
		Size: 3.3 MB (3301584 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4314f4341f219cdd833dab0888f82f309536071fb0208c35d63f0c72ee514d8`  
		Last Modified: Fri, 05 Jan 2024 19:48:14 GMT  
		Size: 4.3 MB (4307795 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:0-pypy3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:7d4dcff2a1e4e282d8864422ac21bf9188adb3dbc5e6f76a61984f10e7ec3e4e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.2 MB (3244176 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e4e50c101376d354058a3a56068fb462e3a89fbe4e046f1b8bce76ec97578b92`

```dockerfile
```

-	Layers:
	-	`sha256:d92702131e085c3910d5366116af31025639a2681e9b7a271bdf87e2f71095b9`  
		Last Modified: Fri, 05 Jan 2024 19:48:14 GMT  
		Size: 3.2 MB (3235595 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8c6ee479e32030bd5e1e6cc65a8b6bce8bca257504913a3a593ce06cabd9944e`  
		Last Modified: Fri, 05 Jan 2024 19:48:14 GMT  
		Size: 8.6 KB (8581 bytes)  
		MIME: application/vnd.in-toto+json
