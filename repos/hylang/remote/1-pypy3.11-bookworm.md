## `hylang:1-pypy3.11-bookworm`

```console
$ docker pull hylang@sha256:a6c43bd46df7e379d36ab2506b0aa2575f9c35abf00a4c3814fc2089788b605f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:1-pypy3.11-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:812c2371a8bcea452397b87f6bd5f1bb1a6e0877d321292ea35f691def3dec1a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73081352 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:047d09c072779cba7329f3baad6102b2ae5ee5dac9f52035674c4e516569cb43`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 18:15:04 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1745798400'
# Wed, 09 Apr 2025 18:15:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 18:15:04 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 18:15:04 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 18:15:04 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 09 Apr 2025 18:15:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-linux64.tar.bz2'; 			sha256='9177d9e0bb91b05f921c642cb0ff71a0f3653b5d29a42d40d6a078c15b75720f'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-aarch64.tar.bz2'; 			sha256='13207dbf81ce24e96da760b1b863627b77bb20b1fb4c95191e02a0b72383df74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-linux32.tar.bz2'; 			sha256='5c6cdafd0a0abd14ca59926ed1b6aeb13b228c18b4b46de655aae48734c731ad'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 09 Apr 2025 18:15:04 GMT
CMD ["pypy3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
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
	-	`sha256:a879c35e3d60648d9b82c4756cd52475d5843bb6ce06064529abe4b84d40e992`  
		Last Modified: Sat, 17 May 2025 16:47:17 GMT  
		Size: 6.4 MB (6430293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:aedb1f91c3903715f9c03f9f68396d2caa3b55afe7c8e3f9ff7d3bcd2681b4a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2413453 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb08453f4736d25886c53a4222321f19547f7bc1f7b600ef6b242c242a91b265`

```dockerfile
```

-	Layers:
	-	`sha256:9233576b844ef66c08789848262843b2b785303f9b620ca1d9dea59d126925bb`  
		Last Modified: Fri, 09 May 2025 17:36:39 GMT  
		Size: 2.4 MB (2404662 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a7b8531faa7db3ecb7f42e9ae95b7786374cdb74f523018a611a489eed28cc04`  
		Last Modified: Fri, 09 May 2025 17:36:38 GMT  
		Size: 8.8 KB (8791 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.11-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:4db545b6f33265d90688a82646ccf5c9c37c5a6129234d3989a21953c530dce8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71008263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb266fd95da8fb0946bea09607d8db8554a3d4b54df85ea2e2b14cde749ff82b`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 18:15:04 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1745798400'
# Wed, 09 Apr 2025 18:15:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 18:15:04 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 18:15:04 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 18:15:04 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 09 Apr 2025 18:15:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-linux64.tar.bz2'; 			sha256='9177d9e0bb91b05f921c642cb0ff71a0f3653b5d29a42d40d6a078c15b75720f'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-aarch64.tar.bz2'; 			sha256='13207dbf81ce24e96da760b1b863627b77bb20b1fb4c95191e02a0b72383df74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-linux32.tar.bz2'; 			sha256='5c6cdafd0a0abd14ca59926ed1b6aeb13b228c18b4b46de655aae48734c731ad'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 09 Apr 2025 18:15:04 GMT
CMD ["pypy3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:943331d8a9a9863299c02e5de6cce58602a5bc3dc564315aa886fe706376f27f`  
		Last Modified: Thu, 08 May 2025 17:04:42 GMT  
		Size: 28.1 MB (28066622 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbcc1e909dffd2137a40521edab0f8e4126324dcb9672d5d74d76f3e4905f272`  
		Last Modified: Fri, 09 May 2025 02:58:41 GMT  
		Size: 3.3 MB (3322963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e19a2c4de81dc984e90c8ab2f34c453ddc9d75925cfdf6a14145cd6915b924f6`  
		Last Modified: Mon, 19 May 2025 17:39:14 GMT  
		Size: 33.2 MB (33188264 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3bce36951bfe78fc8d6337ab90c904f6e4c36c37ca11a065b0ae6b662c925935`  
		Last Modified: Fri, 09 May 2025 19:03:57 GMT  
		Size: 6.4 MB (6430414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:c6ab6a2e4d884df68ee8aac529ade087b6f3ca3013ce2f8b5f48c950a18c93fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2413911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1425f98e5db029d42a53c67f846237e6014d6122274380e5e2e82033f7dd4c33`

```dockerfile
```

-	Layers:
	-	`sha256:b63d50bd0f64de98b8381c6f4e40a379debf5dc0ff37e814b9b2970196f05a82`  
		Last Modified: Fri, 09 May 2025 19:02:34 GMT  
		Size: 2.4 MB (2404969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:fbc79ca2dbb8dc8629e0afe7305c673f5e3e2608e1ff00181d5a1ec749f1bed7`  
		Last Modified: Fri, 09 May 2025 19:02:33 GMT  
		Size: 8.9 KB (8942 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.11-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:d833ec4464e37f716500bc5d065facfb6240fae237461bbb4b00b3fa69599421
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70568613 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f49f4c7ef1776e96fe7be987b0d08b15a352ce4d69e707ad2d7dc86d18555028`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 18:15:04 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1745798400'
# Wed, 09 Apr 2025 18:15:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 18:15:04 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 18:15:04 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 18:15:04 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 09 Apr 2025 18:15:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-linux64.tar.bz2'; 			sha256='9177d9e0bb91b05f921c642cb0ff71a0f3653b5d29a42d40d6a078c15b75720f'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-aarch64.tar.bz2'; 			sha256='13207dbf81ce24e96da760b1b863627b77bb20b1fb4c95191e02a0b72383df74'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.19-linux32.tar.bz2'; 			sha256='5c6cdafd0a0abd14ca59926ed1b6aeb13b228c18b4b46de655aae48734c731ad'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 09 Apr 2025 18:15:04 GMT
CMD ["pypy3"]
# Fri, 09 May 2025 15:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 15:36:44 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 15:36:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Fri, 09 May 2025 15:36:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Thu, 08 May 2025 17:08:57 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:041fac29cb36d2b6205de207f4488b4e209443d8829265d9ae6f470c8b65f04f`  
		Last Modified: Fri, 09 May 2025 17:35:38 GMT  
		Size: 3.5 MB (3503476 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2f9f7f313242759582df2cd0a6eb1816867843d0267909a302d6621fbedc173`  
		Last Modified: Fri, 09 May 2025 17:35:39 GMT  
		Size: 31.4 MB (31423755 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bd273bbde0ddbab6332a3ae8cc7e553eed539dc7ecbc15a2aea5135c254bf5a`  
		Last Modified: Fri, 09 May 2025 17:36:36 GMT  
		Size: 6.4 MB (6430516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:c62c1c32c41eed879dabd9864f582a2360b9c87c0bbadc8d538fd1db851135cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2410518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37b93d2b228ae45dda8076b9b8bd9053082bdf637d5b5045de2060dae655b8c`

```dockerfile
```

-	Layers:
	-	`sha256:b1808a01ac86e88ca09fe516a6180d41e4bbabb2ca58259b33dc9108c73064c8`  
		Last Modified: Fri, 09 May 2025 17:36:19 GMT  
		Size: 2.4 MB (2401779 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25c6d71cc18f71fbfbff230c34c1fdf97736f2302883b66abb30cfb00742ecc3`  
		Last Modified: Fri, 09 May 2025 17:36:19 GMT  
		Size: 8.7 KB (8739 bytes)  
		MIME: application/vnd.in-toto+json
