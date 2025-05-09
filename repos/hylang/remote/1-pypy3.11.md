## `hylang:1-pypy3.11`

```console
$ docker pull hylang@sha256:328e926729c6d3e8a99483dacec3cda9c3965bbc6238b490c6b3e5b21909a149
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

### `hylang:1-pypy3.11` - linux; amd64

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
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c65158aa610f31254e098276a5281efb0f283995218f03eeb37efdbd307cb034`  
		Last Modified: Mon, 28 Apr 2025 22:07:10 GMT  
		Size: 3.5 MB (3499346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3ab319830b07630d324f625665fce816b1e76fd0230077df63c4bea84d81250`  
		Last Modified: Mon, 28 Apr 2025 22:07:11 GMT  
		Size: 34.9 MB (34924071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a879c35e3d60648d9b82c4756cd52475d5843bb6ce06064529abe4b84d40e992`  
		Last Modified: Fri, 09 May 2025 17:36:39 GMT  
		Size: 6.4 MB (6430293 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11` - unknown; unknown

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

### `hylang:1-pypy3.11` - linux; arm64 variant v8

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
		Last Modified: Mon, 28 Apr 2025 21:20:37 GMT  
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
	-	`sha256:3bce36951bfe78fc8d6337ab90c904f6e4c36c37ca11a065b0ae6b662c925935`  
		Last Modified: Fri, 09 May 2025 19:02:34 GMT  
		Size: 6.4 MB (6430414 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11` - unknown; unknown

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

### `hylang:1-pypy3.11` - linux; 386

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
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
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
	-	`sha256:4bd273bbde0ddbab6332a3ae8cc7e553eed539dc7ecbc15a2aea5135c254bf5a`  
		Last Modified: Fri, 09 May 2025 17:36:19 GMT  
		Size: 6.4 MB (6430516 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11` - unknown; unknown

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

### `hylang:1-pypy3.11` - windows version 10.0.26100.3781; amd64

```console
$ docker pull hylang@sha256:72f98a92273451a596c70f78af4269899271ec310c6d8b15e2c920d79242be51
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3449139340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64d472c2814252e3a53c0378e39f0a2c5600983f90b48cd74ffc1f67072f15bc`
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
# Fri, 09 May 2025 17:35:41 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 17:35:42 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 17:36:36 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 09 May 2025 17:36:36 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86a55b9bd12cfb5d81d64963683e6d5d0ba9423233c85140eff135128a64f7ee`  
		Last Modified: Fri, 18 Apr 2025 03:15:41 GMT  
		Size: 1.2 GB (1179854238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:698affd0bf13ebc78afa954bcdd4072eaa03ed93e1c994beafacc7a7365542f7`  
		Last Modified: Fri, 18 Apr 2025 03:24:04 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2b4538c3cd03949cf9282551119fbeeb3398ef5e46294dbf0f4d10903d50235`  
		Last Modified: Fri, 18 Apr 2025 03:24:02 GMT  
		Size: 354.9 KB (354861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3ee02c2eaa39d88c9ca0b95ce3c1e138ac1fca03297ed038ef8f513fb62440e`  
		Last Modified: Fri, 18 Apr 2025 03:24:04 GMT  
		Size: 15.5 MB (15539262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8a6d490d0502fc429781720f51d54322015e252f1a3d6e9661ae33f07c59a1d`  
		Last Modified: Fri, 18 Apr 2025 03:24:02 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:026840e531edf399631323d66871247b9bf7e986eb52fff19e4163767a02cbf4`  
		Last Modified: Fri, 18 Apr 2025 03:24:06 GMT  
		Size: 30.7 MB (30666323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29a48c31acae2a52b289ba5f5be34c9b47a584166d06f20835210f6dbf01bc4c`  
		Last Modified: Fri, 18 Apr 2025 03:24:02 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2d98381df8b7f46777ce38dbdebc450835d7799460731756bf1fe0c8ffbcf58`  
		Last Modified: Fri, 09 May 2025 17:36:39 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65faa1a6674c9f89e88414d3a882ef1afcb3f24db261be523d0c19cb50574a43`  
		Last Modified: Fri, 09 May 2025 17:36:39 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c3b6b64c3d42e400b9b6c61d7b4939f4b06debe5ce8f3a6c584f4a7945c47a`  
		Last Modified: Fri, 09 May 2025 17:36:40 GMT  
		Size: 7.4 MB (7409657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf11cdbb30d0e5d18ed9f66972958b2438b7def1bb7d282eb7ebf286d58d176`  
		Last Modified: Fri, 09 May 2025 17:36:39 GMT  
		Size: 1.3 KB (1328 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-pypy3.11` - windows version 10.0.20348.3566; amd64

```console
$ docker pull hylang@sha256:d9bc3b6ec4bd31f3bb58e486baaf92f598ce204a35ab2a890768807012f225f1
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327463830 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f8852be3a9fb64ad207e02b4ede06bca81cb061fcbcf65365eb82bd276d62f0`
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
# Fri, 09 May 2025 17:31:34 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 17:31:35 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 17:33:17 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 09 May 2025 17:33:18 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0b6ee194dfee460cc53e0f761b7ff976c08380d6cd1e70cc50ff92cfa99d176`  
		Last Modified: Fri, 18 Apr 2025 03:14:44 GMT  
		Size: 811.4 MB (811390127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db6e63c5ed26e532f8ba4909314a1ceea6a7fc0164e873d9f3f4162d2b3e699`  
		Last Modified: Fri, 18 Apr 2025 03:28:57 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64fdb41e48d7c7cd86a2fb751c554d1017f2cf44f5fc6d06595a028866793723`  
		Last Modified: Fri, 18 Apr 2025 03:28:55 GMT  
		Size: 345.1 KB (345074 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e07f139d4c1a7b65454d5dbc5551b814fd3028925122191633d0c9eb9e7aabe`  
		Last Modified: Fri, 18 Apr 2025 03:28:56 GMT  
		Size: 15.5 MB (15529087 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4a9a1ca262dc9b62bf08c772bd5bb9cf19886ea4489ae0468311ca847d09d8d`  
		Last Modified: Fri, 18 Apr 2025 03:28:55 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bced1212c91ac5cbc7270542793c5b67f1cbbe0b10fcfa6ef5361076f936adb7`  
		Last Modified: Fri, 18 Apr 2025 03:28:59 GMT  
		Size: 30.6 MB (30619211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ee3312b4cbe080da21260b1cb85f95a2ade9737fe408899d5a16eedf5ccbcd6`  
		Last Modified: Fri, 18 Apr 2025 03:28:55 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:079b3d00631129609f4e2a3de6eb46f02dd49c5f084bf4565ac01f4f6012da15`  
		Last Modified: Fri, 09 May 2025 17:33:20 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f26e0b9801cd6cb811a1a0b038ddda89b0d166c5cd719b0a07fb343a004a8b`  
		Last Modified: Fri, 09 May 2025 17:33:20 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83f89c9a280e29ac7e5ace5211368862bedf2f1433f21c25046cbdf55b2e2f4a`  
		Last Modified: Fri, 09 May 2025 17:33:21 GMT  
		Size: 7.4 MB (7380171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de36629c132c209b80d28127f66a549f2f6825bb6ac59b6a42b43aa7ce9c9fe9`  
		Last Modified: Fri, 09 May 2025 17:33:20 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-pypy3.11` - windows version 10.0.17763.7249; amd64

```console
$ docker pull hylang@sha256:bbe8c41b2aaa7bea0ecf75e8f407846c6f736d1ccb3475cb8f9d76f8b239ac93
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2219303025 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ae76fefc30b52b7a6127e2b203a6a9dd8d332bc827c7c15bc97b359653578c5`
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
# Fri, 09 May 2025 17:30:47 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 17:30:48 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 17:31:54 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 09 May 2025 17:31:55 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:632102e3f287de7b6ffd6cab740fb7afe94ac8418060651b0954506aeecc48f1`  
		Last Modified: Fri, 18 Apr 2025 03:13:03 GMT  
		Size: 445.3 MB (445257460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9cf5425b0d7cd2f1e945ca428bc08593d7f4e242e81909a2c13da6007189859e`  
		Last Modified: Fri, 18 Apr 2025 03:23:04 GMT  
		Size: 1.4 KB (1356 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cb5f86e1202bb8948501d8290c42e1d0d1432e4fabed4774700ed940e483210`  
		Last Modified: Fri, 18 Apr 2025 03:23:03 GMT  
		Size: 326.3 KB (326331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1205a53b54b0eebee92b46c8fa0ddff1bf54d30b818842196c6d4171397e9e2`  
		Last Modified: Fri, 18 Apr 2025 03:23:04 GMT  
		Size: 15.5 MB (15488339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5021e4ac0f7d573d72336f635927fb068f4cd20328d198311ac7547a1a10f0d4`  
		Last Modified: Fri, 18 Apr 2025 03:23:02 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b66686a2088e41bf0f0e9ddbbe14fc950598a7c1ea615924b1bb2a664a8780fe`  
		Last Modified: Fri, 18 Apr 2025 03:23:07 GMT  
		Size: 30.6 MB (30595729 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2670163185a979e2b1eca98f8d592871132b46400501e992c9b4e00d5d88008f`  
		Last Modified: Fri, 18 Apr 2025 03:23:02 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f059e6f1aeeefa110bf9c7702b1bb5fcac8b1137b91705c1dbceaab2bb8b67cb`  
		Last Modified: Fri, 09 May 2025 17:32:00 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc908f23888052d55393691cfbc94a3a7b5e7b7d6d8019101a03825bb49f9cb`  
		Last Modified: Fri, 09 May 2025 17:32:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab1a552152a5d0e1304015919b549d10d815649f74d81019bc6db8eac6f1ae67`  
		Last Modified: Fri, 09 May 2025 17:32:01 GMT  
		Size: 7.4 MB (7358967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fea888080ee2088bef704afaf3ae22ccb3a691670b96a02993177bc5070083e`  
		Last Modified: Fri, 09 May 2025 17:32:00 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
