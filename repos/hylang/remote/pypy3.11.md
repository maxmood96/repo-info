## `hylang:pypy3.11`

```console
$ docker pull hylang@sha256:8638a35afca7a945382fbe879a0da35d471549c512e0b07f7427087bfcd0ad87
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 9
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.3476; amd64
	-	windows version 10.0.20348.3328; amd64
	-	windows version 10.0.17763.7009; amd64

### `hylang:pypy3.11` - linux; amd64

```console
$ docker pull hylang@sha256:2679baa7b0e94707055bf17807721f762f61f7c6de2999ab522a77f41da78a00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73117950 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d382ce1fc850fe563f8e95be4a92b4e553355a706eb1e0ebec49f6e34a2cdb2c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 26 Feb 2025 17:18:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1742169600'
# Wed, 26 Feb 2025 17:18:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 17:18:43 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2025 17:18:43 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 17:18:43 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 26 Feb 2025 17:18:43 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-linux64.tar.bz2'; 			sha256='9177d9e0bb91b05f921c642cb0ff71a0f3653b5d29a42d40d6a078c15b75720f'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-aarch64.tar.bz2'; 			sha256='13207dbf81ce24e96da760b1b863627b77bb20b1fb4c95191e02a0b72383df74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-linux32.tar.bz2'; 			sha256='5c6cdafd0a0abd14ca59926ed1b6aeb13b228c18b4b46de655aae48734c731ad'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 26 Feb 2025 17:18:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 26 Feb 2025 17:18:43 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 26 Feb 2025 17:18:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 26 Feb 2025 17:18:43 GMT
CMD ["pypy3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6e909acdb790c5a1989d9cfc795fda5a246ad6664bb27b5c688e2b734b2c5fad`  
		Last Modified: Mon, 17 Mar 2025 22:17:24 GMT  
		Size: 28.2 MB (28204865 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da442eb3be45c34ab405655202111476f42275562f14c0222ad6fe3c4b355d96`  
		Last Modified: Mon, 17 Mar 2025 23:20:35 GMT  
		Size: 3.5 MB (3499351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72d6baecf416682b9bcc2db880472b2104a2bb9e60b1f3706d0238f62ce0d319`  
		Last Modified: Mon, 17 Mar 2025 23:20:35 GMT  
		Size: 31.6 MB (31629474 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b1c090e211fb77fd2fec5a9897a62e355a3043a7277b1900d31085d9eaea448`  
		Last Modified: Mon, 17 Mar 2025 23:20:35 GMT  
		Size: 3.4 MB (3354089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:110f8f375d93bd20151dcc0f2f7b97a89e7dbaad55f975d7de7061f82296c83a`  
		Last Modified: Wed, 19 Mar 2025 22:59:10 GMT  
		Size: 6.4 MB (6430171 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:8ab07b5dd5ef47b6865b72012396a4766ba2e91f158f65f9538c0d64ef251776
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2412631 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a321fd321663e614560af129d611d2e944bdba9a18815d11b4e22adc3c632f76`

```dockerfile
```

-	Layers:
	-	`sha256:658bfe59ea1592c345efff3805119dcffaa6aef02ce831b1c548734376edbb40`  
		Last Modified: Wed, 19 Mar 2025 22:59:10 GMT  
		Size: 2.4 MB (2403326 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:375afa8d4edbd58d2b5da7b00505bc31b77b67fdd86e6860fc26e9c5083a63f9`  
		Last Modified: Wed, 19 Mar 2025 22:59:10 GMT  
		Size: 9.3 KB (9305 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.11` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:48af72ea5d214164c32898c1460716b3000671b7c9e9c2721c5c1cb3acebb9ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71048428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae0d0661aca3f32d68a5a48d2cad797e264bcdb77081669db2b8fa79cd2f221e`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 26 Feb 2025 17:18:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1742169600'
# Wed, 26 Feb 2025 17:18:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 17:18:43 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2025 17:18:43 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 17:18:43 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 26 Feb 2025 17:18:43 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-linux64.tar.bz2'; 			sha256='9177d9e0bb91b05f921c642cb0ff71a0f3653b5d29a42d40d6a078c15b75720f'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-aarch64.tar.bz2'; 			sha256='13207dbf81ce24e96da760b1b863627b77bb20b1fb4c95191e02a0b72383df74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-linux32.tar.bz2'; 			sha256='5c6cdafd0a0abd14ca59926ed1b6aeb13b228c18b4b46de655aae48734c731ad'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 26 Feb 2025 17:18:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 26 Feb 2025 17:18:43 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 26 Feb 2025 17:18:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 26 Feb 2025 17:18:43 GMT
CMD ["pypy3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:d9b6365477446a79987b20560ae52637be6f54d6d2f801e16aaa0ca25dd0964b`  
		Last Modified: Mon, 17 Mar 2025 22:17:34 GMT  
		Size: 28.0 MB (28044037 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a08287ef3f5a9e0a28a72307a55937b861b0854bfc7d3d620d08f8d3b5278a7b`  
		Last Modified: Tue, 18 Mar 2025 02:36:31 GMT  
		Size: 3.3 MB (3322929 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ec07a43e3f207e9a488e59f9e0c8f7f79ab7c75413da698e7a1c1ed6c5f02f3`  
		Last Modified: Tue, 18 Mar 2025 02:39:25 GMT  
		Size: 29.9 MB (29896741 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fe5f94e6f54e95a93d8570f5af07db4f2fb8e6fd6c376e969350a46a45f2767`  
		Last Modified: Tue, 18 Mar 2025 02:39:25 GMT  
		Size: 3.4 MB (3354156 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4849f59ba31b72b08748ef5dd4f3707ee2102ce45d5d6dcbe037334c02ccf890`  
		Last Modified: Wed, 19 Mar 2025 23:24:59 GMT  
		Size: 6.4 MB (6430565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:305028bb2b5f42b13d9abdbe6ff8080ed9103816857286173cad30e6cb35fad2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2413090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:561dab3178782a7f38871d07f0c2462fcf709e29056ffa0cc328e537b6c6e1f2`

```dockerfile
```

-	Layers:
	-	`sha256:6c96506e67577ea05b95ea1cc51653856fd17b324bb0f35b51ccf43bf8c3f470`  
		Last Modified: Wed, 19 Mar 2025 23:24:59 GMT  
		Size: 2.4 MB (2403633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ae9a7b4bd974931f83cf73c42c6c8c9912aac79e12aa446d68f2b507ed333554`  
		Last Modified: Wed, 19 Mar 2025 23:24:59 GMT  
		Size: 9.5 KB (9457 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.11` - linux; 386

```console
$ docker pull hylang@sha256:88952c21ef3c1c9a7c0db980225c7b4f165c2ed5f66da71608372a7e15c2ebab
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70607238 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34243d7746af597af0b254c21683fdaa981118cccd4cda33ea8a40c78eab9b64`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 26 Feb 2025 17:18:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1742169600'
# Wed, 26 Feb 2025 17:18:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 26 Feb 2025 17:18:43 GMT
ENV LANG=C.UTF-8
# Wed, 26 Feb 2025 17:18:43 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 26 Feb 2025 17:18:43 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 26 Feb 2025 17:18:43 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-linux64.tar.bz2'; 			sha256='9177d9e0bb91b05f921c642cb0ff71a0f3653b5d29a42d40d6a078c15b75720f'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-aarch64.tar.bz2'; 			sha256='13207dbf81ce24e96da760b1b863627b77bb20b1fb4c95191e02a0b72383df74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-linux32.tar.bz2'; 			sha256='5c6cdafd0a0abd14ca59926ed1b6aeb13b228c18b4b46de655aae48734c731ad'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 26 Feb 2025 17:18:43 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 26 Feb 2025 17:18:43 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 26 Feb 2025 17:18:43 GMT
RUN set -ex; 	apt-get update; 	apt-get install -y --no-install-recommends wget; 	rm -rf /var/lib/apt/lists/*; 		wget -O get-pip.py "$PYTHON_GET_PIP_URL"; 	echo "$PYTHON_GET_PIP_SHA256 *get-pip.py" | sha256sum --check --strict -; 		pipVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._PIP_VERSION)')"; 	setuptoolsVersion="$(pypy3 -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)')"; 		pypy3 get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		"pip == $pipVersion" 		"setuptools == $setuptoolsVersion" 	; 	apt-get purge -y --auto-remove wget; 	pip --version; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' +; 	rm -f get-pip.py # buildkit
# Wed, 26 Feb 2025 17:18:43 GMT
CMD ["pypy3"]
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 17:54:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:bdeb081d427d7feac6a8c0bd36a2c34506a1aa38143fe43a5c5a8c162698a854`  
		Last Modified: Mon, 17 Mar 2025 22:17:35 GMT  
		Size: 29.2 MB (29189528 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:59615a779103470a8a6ed39f7f7506734cb29f8580cfb42119bc938e771186b2`  
		Last Modified: Mon, 17 Mar 2025 23:28:10 GMT  
		Size: 3.5 MB (3503417 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:304a6cc64ff69520f0d83e7c2d1bb191dfa59863a63671f0f9a0c8388b2a8e47`  
		Last Modified: Mon, 17 Mar 2025 23:28:11 GMT  
		Size: 28.1 MB (28130138 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5342e5cd38989013074b2ccf55dec4600c3b7b803cf876ab8a7adfa535d54fa4`  
		Last Modified: Mon, 17 Mar 2025 23:28:10 GMT  
		Size: 3.4 MB (3353805 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb9d8e685db74ed9ab62d02da27834442e4848f9ff324bcad1ee750e0c9de4d8`  
		Last Modified: Wed, 19 Mar 2025 22:59:12 GMT  
		Size: 6.4 MB (6430350 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:0ae3345bfc244aec4291e0081044814506d7e2c72f0465542972ac27f9118190
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2409694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d903e427bf189547fd6f98cab77887d247e6e06c78b67a5460957e421d30113b`

```dockerfile
```

-	Layers:
	-	`sha256:13296374232a70336263b1ccf2352bbf7b78173a9053559d8fd2191e3dab5217`  
		Last Modified: Wed, 19 Mar 2025 22:59:12 GMT  
		Size: 2.4 MB (2400443 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b17b1979ce214df83d6e2b683707fc2e6018390f05df6582335aa79bbd36a692`  
		Last Modified: Wed, 19 Mar 2025 22:59:12 GMT  
		Size: 9.3 KB (9251 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.11` - windows version 10.0.26100.3476; amd64

```console
$ docker pull hylang@sha256:a8cbf2de9921722f9056da2c8dd00ee0084a8c2d2146438676abe3e89818bf04
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.0 GB (2963138342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36e79495fcc5d168e8c3f9339db3d90a4a3f3b81258753e90203fe0bd89817f0`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Fri, 07 Mar 2025 06:08:48 GMT
RUN Install update 10.0.26100.3476
# Wed, 12 Mar 2025 18:57:16 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 18:57:23 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:57:36 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:57:36 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 12 Mar 2025 18:57:58 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'b61c7c1dbf879eda6f779c374bfbbeecd3f618ada08404705a1a19d39df48dbd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:57:59 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 12 Mar 2025 18:58:00 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 12 Mar 2025 18:58:24 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 18:58:24 GMT
CMD ["pypy"]
# Wed, 19 Mar 2025 23:05:18 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 23:05:19 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 23:06:15 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 19 Mar 2025 23:06:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:325ca01145f0fc17834eb1871e37e4a03c69b868e3eb071bf21be6413d720e5e`  
		Last Modified: Wed, 12 Mar 2025 03:14:29 GMT  
		Size: 693.3 MB (693340560 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4c06c3d6ab0d7603b86bb094d0785e1638c3cf29bb74190fa3a5a20d5a66167`  
		Last Modified: Wed, 12 Mar 2025 18:58:32 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f44920aefdd1e8b1307481ee124638101e11809e9e535d6914673de0144ab9a`  
		Last Modified: Wed, 12 Mar 2025 18:58:31 GMT  
		Size: 371.3 KB (371344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3e6e6bb19d1d5a1ed5a73b1630782cb5622899e1ec2d43c0f3979b648dcc0dd`  
		Last Modified: Wed, 12 Mar 2025 18:58:32 GMT  
		Size: 15.6 MB (15551125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3462f599941b95c39e6de56dad26b34dcb32880e0d6613e3d2d0cd404695ae4f`  
		Last Modified: Wed, 12 Mar 2025 18:58:30 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e454aa829ab3eac67f37563302ddbe3a9facd99166f7dbc3e28572a4924452a`  
		Last Modified: Wed, 12 Mar 2025 18:58:32 GMT  
		Size: 27.1 MB (27069197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a4f3a69c3eb124fa53d13113325ed0e2d275d5785c202e31afa408c0a4f64d`  
		Last Modified: Wed, 12 Mar 2025 18:58:29 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7de384a6bc1b4e571f549dfac77eae45b873ede20cf4a74ded4121cf057cdd0a`  
		Last Modified: Wed, 12 Mar 2025 18:58:29 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6f784656109e67b99e8fe4a1bdfe67f152b436dc7d8079f46acdd01c5614a40`  
		Last Modified: Wed, 12 Mar 2025 18:58:30 GMT  
		Size: 4.1 MB (4055505 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90a576a52d39b0f683d617610e2fee34c09445e39afcab19e06294d4a8000223`  
		Last Modified: Wed, 12 Mar 2025 18:58:29 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35c01f4afe63278434381660d670f65b7304cc50b3761ba57496787b271f0856`  
		Last Modified: Wed, 19 Mar 2025 23:06:19 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a77e345339c7a1c8283d425b310f2caa04da2a146a637a4166788d7c434f32d`  
		Last Modified: Wed, 19 Mar 2025 23:06:19 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d6b0e907bde793fa6687d51f81ac8d2f9f626f20d5eb1703f6bc7801bb985f3`  
		Last Modified: Wed, 19 Mar 2025 23:06:20 GMT  
		Size: 7.4 MB (7433039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d8d354893db90e0672fbb1e9b7be7df9909c1567f917ae7856fbb9678a5d9e30`  
		Last Modified: Wed, 19 Mar 2025 23:06:20 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.11` - windows version 10.0.20348.3328; amd64

```console
$ docker pull hylang@sha256:5ef90227250f67cfcfc1239efe4a004efc1d7a0bb5dfff9ca57297701f84dcc5
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2324283310 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:632e239e044903987373cc0c07acfb1eae9a2bd077beff4bacb572c8806fcf0d`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Thu, 06 Mar 2025 10:49:01 GMT
RUN Install update 10.0.20348.3328
# Wed, 12 Mar 2025 19:07:32 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 19:07:44 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:07:56 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:07:56 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 12 Mar 2025 19:08:16 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'b61c7c1dbf879eda6f779c374bfbbeecd3f618ada08404705a1a19d39df48dbd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:08:16 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 12 Mar 2025 19:08:17 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 12 Mar 2025 19:08:43 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:08:45 GMT
CMD ["pypy"]
# Wed, 19 Mar 2025 23:21:20 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 23:21:22 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 23:22:25 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 19 Mar 2025 23:22:25 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75861b2b3af9a692daa04d9c15a1c79d8a009e23ed5140003350c9b926460f09`  
		Last Modified: Tue, 11 Mar 2025 18:40:20 GMT  
		Size: 807.7 MB (807748751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ba227543ee4391dcb241e8b70e758d2c050bb03c261a0f13f1dcad80b8ac9e2`  
		Last Modified: Wed, 12 Mar 2025 19:08:49 GMT  
		Size: 1.4 KB (1355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4caefb22c542842bde5b0493fe6acef99ef03cf72c175ee6473798423e2473c1`  
		Last Modified: Wed, 12 Mar 2025 19:08:49 GMT  
		Size: 348.6 KB (348639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c50faf475f2f584f01449817384675745cd6f0101138f062185bcdb642d80cfb`  
		Last Modified: Wed, 12 Mar 2025 19:08:50 GMT  
		Size: 15.5 MB (15529605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8796e7340a4a1c79c4ade150697e40adcd87dc1334014183fda354f47853e423`  
		Last Modified: Wed, 12 Mar 2025 19:08:48 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0b85585c37c4815e5a7abe31afe852445c8bfcab78cafc86ebbcbba2185fe0`  
		Last Modified: Wed, 12 Mar 2025 19:08:51 GMT  
		Size: 27.0 MB (27027483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:338824f5ce7cb0ff660f6084c15c19f772f708e8dc4a632cd6da4ddf796cdfb4`  
		Last Modified: Wed, 12 Mar 2025 19:08:47 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:191b0c2d69e85c0f7a1aaae2a5cd81910e31bc535eaa6e97079bcab07269b4fb`  
		Last Modified: Wed, 12 Mar 2025 19:08:47 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9b4e03566ef81503bb9eae3552b141ecf19735c9ff2aaf3723a58d27ee6847f`  
		Last Modified: Wed, 12 Mar 2025 19:08:48 GMT  
		Size: 4.0 MB (4032068 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe6a3396def373d7242b8d343d093e19c1e348c6817c24a142405daaf1bcb7c`  
		Last Modified: Wed, 12 Mar 2025 19:08:48 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fff72045998aa22445fc6794afdc36e16dd4f65087a28abbf4175c3a9df2eb8`  
		Last Modified: Wed, 19 Mar 2025 23:22:28 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e366fd10876a35ca42b52f48923f1903741675defc791067fca51538214c4a9`  
		Last Modified: Wed, 19 Mar 2025 23:22:28 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2388b7804276668d7833ae59d488db2cb26cd939c2f1c0346e1a359c7a33f412`  
		Last Modified: Wed, 19 Mar 2025 23:22:29 GMT  
		Size: 7.4 MB (7393960 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:947bef663ed33cc55124aa6e41aea269c35f46c6716f48c3ae12a9b97e961f38`  
		Last Modified: Wed, 19 Mar 2025 23:22:28 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.11` - windows version 10.0.17763.7009; amd64

```console
$ docker pull hylang@sha256:f86245c2d20db0c44afd765946032ee199033b0ae1f14cbe8f1f33e3e4a3ebb4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2205854542 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cef39dc0a33cc4c068202472eed5f6bd0be1b8844911381b3dbd1621fb8c3973`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Wed, 05 Mar 2025 22:09:20 GMT
RUN Install update 10.0.17763.7009
# Wed, 12 Mar 2025 19:05:46 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 12 Mar 2025 19:06:49 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:07:07 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:07:07 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 12 Mar 2025 19:07:30 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'b61c7c1dbf879eda6f779c374bfbbeecd3f618ada08404705a1a19d39df48dbd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:07:30 GMT
ENV PYTHON_GET_PIP_URL=https://github.com/pypa/get-pip/raw/3843bff3a0a61da5b63ea0b7d34794c5c51a2f11/get-pip.py
# Wed, 12 Mar 2025 19:07:31 GMT
ENV PYTHON_GET_PIP_SHA256=95c5ee602b2f3cc50ae053d716c3c89bea62c58568f64d7d25924d399b2d5218
# Wed, 12 Mar 2025 19:07:55 GMT
RUN Write-Host ('Downloading get-pip.py ({0}) ...' -f $env:PYTHON_GET_PIP_URL); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $env:PYTHON_GET_PIP_URL -OutFile 'get-pip.py'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_GET_PIP_SHA256); 	if ((Get-FileHash 'get-pip.py' -Algorithm sha256).Hash -ne $env:PYTHON_GET_PIP_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		$pipVersion = & pypy -c 'import ensurepip; print(ensurepip._PIP_VERSION)'; 	$setuptoolsVersion = & pypy -c 'import ensurepip; print(ensurepip._SETUPTOOLS_VERSION)'; 		Write-Host ('Installing "pip == {0}", "setuptools == {1}" ...' -f $pipVersion, $setuptoolsVersion); 	pypy get-pip.py 		--disable-pip-version-check 		--no-cache-dir 		('pip == {0}' -f $pipVersion) 		('setuptools == {0}' -f $setuptoolsVersion) 	; 	Remove-Item get-pip.py -Force; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 12 Mar 2025 19:07:56 GMT
CMD ["pypy"]
# Wed, 19 Mar 2025 23:08:41 GMT
ENV HY_VERSION=1.0.0
# Wed, 19 Mar 2025 23:08:43 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 19 Mar 2025 23:10:19 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 19 Mar 2025 23:10:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77bec5e4bac3c7f6dc5d56da5ffc11e72881485b3a55330c17c915ad653f955`  
		Last Modified: Tue, 11 Mar 2025 17:48:06 GMT  
		Size: 431.4 MB (431366277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c309c2f68c631cecb534f01f1e48e492c9c21fcebdc943bdf06dcdc71fe2f63a`  
		Last Modified: Wed, 12 Mar 2025 19:08:00 GMT  
		Size: 1.3 KB (1298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1a230d6d3e67d83078f5e32d2ba948b9a18bfb86694dfba793984fa75b0e84`  
		Last Modified: Wed, 12 Mar 2025 19:08:00 GMT  
		Size: 331.0 KB (330961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b160e5c8b4d3af90f6f667e37e8374c91f7cc2cf44b7e8c16584a99c542900a`  
		Last Modified: Wed, 12 Mar 2025 19:08:01 GMT  
		Size: 15.5 MB (15498986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda55c35707e22aec7b2131537e50ee9069db134ab49ed24ec0b774650a41f91`  
		Last Modified: Wed, 12 Mar 2025 19:08:00 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f66e28ad6e62e395173b47ed3d4838998b97769fe256410781adf6b81870e4`  
		Last Modified: Wed, 12 Mar 2025 19:08:03 GMT  
		Size: 27.0 MB (27010986 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b988a7194499f0c2b46ce7f20d916d25ab1e148dc8a6ba0fe763be3b8914d66f`  
		Last Modified: Wed, 12 Mar 2025 19:07:59 GMT  
		Size: 1.3 KB (1300 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a46476eab526ea75a58197aa4685755a9f0382c223c98976d16ad8cc6ea8e41`  
		Last Modified: Wed, 12 Mar 2025 19:07:59 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f131ac7db34a4b02f8e645cd900a9623b27719554877a0c25121d4c264e07084`  
		Last Modified: Wed, 12 Mar 2025 19:07:59 GMT  
		Size: 4.0 MB (4004918 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26985d99a22f238e11eba85f60b821e81a380f00ac1a0c1301754428c6e1794e`  
		Last Modified: Wed, 12 Mar 2025 19:07:59 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3175ed58c9920f5e9f218c6ad2cfe405a0272071c61ff34543ff87967d98481a`  
		Last Modified: Wed, 19 Mar 2025 23:10:26 GMT  
		Size: 1.3 KB (1326 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79fa1ffe6546d706e554779f8eeb59c6ab50955717bebfb7b97d36f6759e02ec`  
		Last Modified: Wed, 19 Mar 2025 23:10:26 GMT  
		Size: 1.4 KB (1359 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:857eb366966ee50f455364a7eaf17d2e57872fd05f2a489e047a689d7068c0f5`  
		Last Modified: Wed, 19 Mar 2025 23:10:27 GMT  
		Size: 7.4 MB (7363534 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a7162ec6bdb792dfa0952004c84e85275ae6224fe2032a98a6f6a65097f79e9`  
		Last Modified: Wed, 19 Mar 2025 23:10:26 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
