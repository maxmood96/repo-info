## `hylang:pypy3.11`

```console
$ docker pull hylang@sha256:9147f698c8b051156e97727959b70cf7d03df28043b414c7ee9df1208dfce4f0
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 9
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.3781; amd64
	-	windows version 10.0.20348.3566; amd64
	-	windows version 10.0.17763.7249; amd64

### `hylang:pypy3.11` - linux; amd64

```console
$ docker pull hylang@sha256:cb3d381341e2e665e7ecf60b06dbcbdce67332ed6af8268199e39d05231a4757
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73081194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2cd50912f39d1da5e67ec82a80a08540cf9be1cbcb6bda12fb8ebe0b835aaac8`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
ENV LANG=C.UTF-8
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-linux64.tar.bz2'; 			sha256='9177d9e0bb91b05f921c642cb0ff71a0f3653b5d29a42d40d6a078c15b75720f'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-aarch64.tar.bz2'; 			sha256='13207dbf81ce24e96da760b1b863627b77bb20b1fb4c95191e02a0b72383df74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-linux32.tar.bz2'; 			sha256='5c6cdafd0a0abd14ca59926ed1b6aeb13b228c18b4b46de655aae48734c731ad'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
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
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Thu, 08 May 2025 17:04:38 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65158aa610f31254e098276a5281efb0f283995218f03eeb37efdbd307cb034`  
		Last Modified: Thu, 08 May 2025 22:56:40 GMT  
		Size: 3.5 MB (3499346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ab319830b07630d324f625665fce816b1e76fd0230077df63c4bea84d81250`  
		Last Modified: Thu, 08 May 2025 22:56:41 GMT  
		Size: 34.9 MB (34924071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c77611574c84137f89c3986c983d6e809c00e18919d838aa89fb4afadc0b900`  
		Last Modified: Mon, 28 Apr 2025 22:22:31 GMT  
		Size: 6.4 MB (6430135 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:b70ab5644c0ccb78e3137edf924ef7717766621715a4fc37ec4d50f3ba00c4f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2413453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:461ccd1ff71332130949d6c723bab876eeec483c34043184801d2a64c6021654`

```dockerfile
```

-	Layers:
	-	`sha256:9c152bdc166e18e08237cd5363932d1cc39ed0c90df89b7252e9ec6b27f29db6`  
		Last Modified: Mon, 28 Apr 2025 22:22:31 GMT  
		Size: 2.4 MB (2404662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:da03ef46be37bf9d9976f664942d88df4218819c71579412a39174183537555c`  
		Last Modified: Mon, 28 Apr 2025 22:22:31 GMT  
		Size: 8.8 KB (8791 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.11` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:e0ab0dc55defe2cb93864e8644fd8c0e461aec532f7d3ab903afac4e5eb42b40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71008417 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:808fc1f4e565e1b50abd68ee39332c7e34378fe88e4f8127e070cba97fc89a1d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
ENV LANG=C.UTF-8
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-linux64.tar.bz2'; 			sha256='9177d9e0bb91b05f921c642cb0ff71a0f3653b5d29a42d40d6a078c15b75720f'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-aarch64.tar.bz2'; 			sha256='13207dbf81ce24e96da760b1b863627b77bb20b1fb4c95191e02a0b72383df74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-linux32.tar.bz2'; 			sha256='5c6cdafd0a0abd14ca59926ed1b6aeb13b228c18b4b46de655aae48734c731ad'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
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
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcc1e909dffd2137a40521edab0f8e4126324dcb9672d5d74d76f3e4905f272`  
		Last Modified: Tue, 29 Apr 2025 21:53:36 GMT  
		Size: 3.3 MB (3322963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19a2c4de81dc984e90c8ab2f34c453ddc9d75925cfdf6a14145cd6915b924f6`  
		Last Modified: Tue, 29 Apr 2025 21:53:37 GMT  
		Size: 33.2 MB (33188264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6bf0690956804acda75ad9b4407d0847140ec6f0545a7cb64859fdd66b8fa54e`  
		Last Modified: Wed, 30 Apr 2025 04:36:01 GMT  
		Size: 6.4 MB (6430568 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:43fd6b11d02240a0a0e883ced573a9171d433ba4f17dd0ef47ca32783d56ea6e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2413912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e54ac551fc3fdeede8efca44822b8325ee260b85a39117361d3cae77b8f6ff3e`

```dockerfile
```

-	Layers:
	-	`sha256:f3f85deb64b9c064562c2926c29880c3e2d5f267bd826a12b095835a780109a6`  
		Last Modified: Wed, 30 Apr 2025 04:36:01 GMT  
		Size: 2.4 MB (2404969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90ef14c806ce6d51fbdedaffccff66c1f08b619ef83b7b6210bae2323c91dfc8`  
		Last Modified: Wed, 30 Apr 2025 04:36:00 GMT  
		Size: 8.9 KB (8943 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.11` - linux; 386

```console
$ docker pull hylang@sha256:b4c6dd0e13aba6419b6ebd4e562bf7db739dd4ad2873a0f7c8a7d4737b089633
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70568411 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62143d2cccf1dc2a892e4c8b5702f337d0f729f65d114e46dcc1da6d73d910ce`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 19 Mar 2025 17:54:43 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
ENV LANG=C.UTF-8
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 19 Mar 2025 17:54:43 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 19 Mar 2025 17:54:43 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-linux64.tar.bz2'; 			sha256='9177d9e0bb91b05f921c642cb0ff71a0f3653b5d29a42d40d6a078c15b75720f'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-aarch64.tar.bz2'; 			sha256='13207dbf81ce24e96da760b1b863627b77bb20b1fb4c95191e02a0b72383df74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-linux32.tar.bz2'; 			sha256='5c6cdafd0a0abd14ca59926ed1b6aeb13b228c18b4b46de655aae48734c731ad'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 19 Mar 2025 17:54:43 GMT
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
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Thu, 08 May 2025 17:08:57 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041fac29cb36d2b6205de207f4488b4e209443d8829265d9ae6f470c8b65f04f`  
		Last Modified: Mon, 28 Apr 2025 21:56:28 GMT  
		Size: 3.5 MB (3503476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f9f7f313242759582df2cd0a6eb1816867843d0267909a302d6621fbedc173`  
		Last Modified: Mon, 28 Apr 2025 21:56:29 GMT  
		Size: 31.4 MB (31423755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2f224699c5ec85d33320f5f9c583314362ba472f06d1591194189ed2cd1fe5aa`  
		Last Modified: Mon, 28 Apr 2025 22:23:20 GMT  
		Size: 6.4 MB (6430314 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:78052f9de7df0fbf905aaab1037207f68430e5da0029029098c27f6f659f8e5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2410518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f9458f3112f3590da9fbd61217890e05bf26e664c66ae9082ab337d5b7b1386`

```dockerfile
```

-	Layers:
	-	`sha256:05025e1caaea8673b12df6bf9379e94457baad69d3237e38934a25195f66e25e`  
		Last Modified: Mon, 28 Apr 2025 22:23:20 GMT  
		Size: 2.4 MB (2401779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09c391b63fe3fbb71b1395ee7f658ae41ffea0bbfc7f57c41332b20f8319c242`  
		Last Modified: Mon, 28 Apr 2025 22:23:20 GMT  
		Size: 8.7 KB (8739 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.11` - windows version 10.0.26100.3781; amd64

```console
$ docker pull hylang@sha256:b6f7d16158c9855d4376b2b118e4ec0290dac6acc0c25b4ac22c8aa64bf43e94
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3449110191 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:112a8f1ca61e0821a58a98e8fb8869a1182e19f5c22518db46289df4d0e6ea1e`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 03:22:59 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:23:07 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:23:17 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:23:18 GMT
ENV PYPY_VERSION=7.3.19
# Fri, 18 Apr 2025 03:23:57 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'b61c7c1dbf879eda6f779c374bfbbeecd3f618ada08404705a1a19d39df48dbd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:23:57 GMT
CMD ["pypy"]
# Fri, 18 Apr 2025 04:15:03 GMT
ENV HY_VERSION=1.0.0
# Fri, 18 Apr 2025 04:15:04 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 18 Apr 2025 04:16:02 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 18 Apr 2025 04:16:03 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Thu, 23 Jan 2025 01:13:15 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Thu, 08 May 2025 17:36:06 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698affd0bf13ebc78afa954bcdd4072eaa03ed93e1c994beafacc7a7365542f7`  
		Last Modified: Thu, 08 May 2025 23:27:00 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b4538c3cd03949cf9282551119fbeeb3398ef5e46294dbf0f4d10903d50235`  
		Last Modified: Thu, 08 May 2025 23:27:00 GMT  
		Size: 354.9 KB (354861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ee02c2eaa39d88c9ca0b95ce3c1e138ac1fca03297ed038ef8f513fb62440e`  
		Last Modified: Thu, 08 May 2025 23:27:01 GMT  
		Size: 15.5 MB (15539262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a6d490d0502fc429781720f51d54322015e252f1a3d6e9661ae33f07c59a1d`  
		Last Modified: Thu, 08 May 2025 23:27:00 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026840e531edf399631323d66871247b9bf7e986eb52fff19e4163767a02cbf4`  
		Last Modified: Thu, 08 May 2025 23:27:02 GMT  
		Size: 30.7 MB (30666323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a48c31acae2a52b289ba5f5be34c9b47a584166d06f20835210f6dbf01bc4c`  
		Last Modified: Thu, 08 May 2025 23:27:00 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e4a8f6501a682c96c44f28fa990fa7018c6cbf1bc9081c59b4d3ba75d983896`  
		Last Modified: Fri, 18 Apr 2025 04:16:07 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0deded425e1f03269628edb26d14ce7e5df79166f221d990f78c209f54393865`  
		Last Modified: Fri, 18 Apr 2025 04:16:07 GMT  
		Size: 1.4 KB (1389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef256cfd4ec7d5d843138141948af93bbbc0c232eab241043dfea0eba99dac65`  
		Last Modified: Fri, 18 Apr 2025 04:16:08 GMT  
		Size: 7.4 MB (7380386 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66897d9803beadee8769ad3316895eb2b30fa7e6b46cab6e273e838280fcf535`  
		Last Modified: Fri, 18 Apr 2025 04:16:07 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.11` - windows version 10.0.20348.3566; amd64

```console
$ docker pull hylang@sha256:d690d9663a9048d274fd1fb5e664118f1ca23380a3cecdf276338fa2484938f1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327450659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0ab2f183ba8629d41fb45c7296053ee9460264aaf8c26300fc82fd280ec2d5d`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:27:53 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:28:03 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:28:16 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:28:17 GMT
ENV PYPY_VERSION=7.3.19
# Fri, 18 Apr 2025 03:28:50 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'b61c7c1dbf879eda6f779c374bfbbeecd3f618ada08404705a1a19d39df48dbd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:28:51 GMT
CMD ["pypy"]
# Fri, 18 Apr 2025 04:15:15 GMT
ENV HY_VERSION=1.0.0
# Fri, 18 Apr 2025 04:15:16 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 18 Apr 2025 04:16:10 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 18 Apr 2025 04:16:11 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Fri, 13 Dec 2024 18:51:46 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Thu, 08 May 2025 17:22:47 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db6e63c5ed26e532f8ba4909314a1ceea6a7fc0164e873d9f3f4162d2b3e699`  
		Last Modified: Thu, 08 May 2025 23:22:45 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fdb41e48d7c7cd86a2fb751c554d1017f2cf44f5fc6d06595a028866793723`  
		Last Modified: Thu, 08 May 2025 23:22:45 GMT  
		Size: 345.1 KB (345074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e07f139d4c1a7b65454d5dbc5551b814fd3028925122191633d0c9eb9e7aabe`  
		Last Modified: Thu, 08 May 2025 23:22:47 GMT  
		Size: 15.5 MB (15529087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a9a1ca262dc9b62bf08c772bd5bb9cf19886ea4489ae0468311ca847d09d8d`  
		Last Modified: Thu, 08 May 2025 23:22:46 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bced1212c91ac5cbc7270542793c5b67f1cbbe0b10fcfa6ef5361076f936adb7`  
		Last Modified: Thu, 08 May 2025 23:22:49 GMT  
		Size: 30.6 MB (30619211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee3312b4cbe080da21260b1cb85f95a2ade9737fe408899d5a16eedf5ccbcd6`  
		Last Modified: Thu, 08 May 2025 23:22:47 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da59ac9593854e1111656ac3e2c50a98dfa3625add96a2498440ca018365ff3a`  
		Last Modified: Fri, 18 Apr 2025 04:16:15 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4517bdd18b444ed1dc9eff0a9ad4f8d3e46d0026b5c9081e101f1194091b2084`  
		Last Modified: Fri, 18 Apr 2025 04:16:15 GMT  
		Size: 1.3 KB (1281 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b49b17beed52e235eb43d3e7d581328f9791025d4c7a42e178ed5d6f85cc9e36`  
		Last Modified: Fri, 18 Apr 2025 04:16:16 GMT  
		Size: 7.4 MB (7367005 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ddf3ecc741dfaa52472c57d7c44e76dc16cabd2884a4fd8b86d4dc98155eced`  
		Last Modified: Fri, 18 Apr 2025 04:16:15 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy3.11` - windows version 10.0.17763.7249; amd64

```console
$ docker pull hylang@sha256:72945aaa57fb64ecae48c029d11f3b212b3d595220cce52376319ded269e8cae
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2219277294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92bcb7b305baaa03647e14dfb950f2bf13bff4b90cb29c52a53ea6a85889b0a2`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:21:47 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:22:07 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:22:20 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:22:21 GMT
ENV PYPY_VERSION=7.3.19
# Fri, 18 Apr 2025 03:22:57 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'b61c7c1dbf879eda6f779c374bfbbeecd3f618ada08404705a1a19d39df48dbd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:22:58 GMT
CMD ["pypy"]
# Fri, 18 Apr 2025 04:22:28 GMT
ENV HY_VERSION=1.0.0
# Fri, 18 Apr 2025 04:22:30 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 18 Apr 2025 04:23:54 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 18 Apr 2025 04:23:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Fri, 13 Dec 2024 17:52:52 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Thu, 08 May 2025 17:14:51 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf5425b0d7cd2f1e945ca428bc08593d7f4e242e81909a2c13da6007189859e`  
		Last Modified: Thu, 08 May 2025 23:23:15 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb5f86e1202bb8948501d8290c42e1d0d1432e4fabed4774700ed940e483210`  
		Last Modified: Thu, 08 May 2025 23:23:16 GMT  
		Size: 326.3 KB (326331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1205a53b54b0eebee92b46c8fa0ddff1bf54d30b818842196c6d4171397e9e2`  
		Last Modified: Thu, 08 May 2025 23:23:16 GMT  
		Size: 15.5 MB (15488339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5021e4ac0f7d573d72336f635927fb068f4cd20328d198311ac7547a1a10f0d4`  
		Last Modified: Thu, 08 May 2025 23:23:16 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66686a2088e41bf0f0e9ddbbe14fc950598a7c1ea615924b1bb2a664a8780fe`  
		Last Modified: Thu, 08 May 2025 23:23:18 GMT  
		Size: 30.6 MB (30595729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2670163185a979e2b1eca98f8d592871132b46400501e992c9b4e00d5d88008f`  
		Last Modified: Thu, 08 May 2025 23:23:16 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8158597f77262407468c97707236a161f8d8a67b1c3dc61476b3c6e45e0c2fa2`  
		Last Modified: Fri, 18 Apr 2025 04:23:57 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dfde7b2bbc0ca0b03f36485b58c30ff2a242dc74ab4e5e612c41d241c302599`  
		Last Modified: Fri, 18 Apr 2025 04:23:57 GMT  
		Size: 1.4 KB (1373 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ea0d995874794d99e369688f4e84c0ba4b9aa69ba3a32a5b24719ca949b81c`  
		Last Modified: Fri, 18 Apr 2025 04:23:58 GMT  
		Size: 7.3 MB (7333087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cc5f14ab74c365adbd0d289425bac60785a65848e825e2bf1670978115b09e6`  
		Last Modified: Fri, 18 Apr 2025 04:23:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
