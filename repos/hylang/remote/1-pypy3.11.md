## `hylang:1-pypy3.11`

```console
$ docker pull hylang@sha256:b4ef3dc2b702cb4b7566e81e40516247640d1b5e6c73726b418896a333e9f500
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 9
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.4061; amd64
	-	windows version 10.0.20348.3692; amd64
	-	windows version 10.0.17763.7314; amd64

### `hylang:1-pypy3.11` - linux; amd64

```console
$ docker pull hylang@sha256:cd2cf2d4735c00de71534597f0a4f23b3cb40e52cafcac19698ae7665f3979c3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73080902 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3a57fd89fe28fe558168722f33d3e9f450974421a1b5209e5424f89d288dc3e`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 18:15:04 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:61320b01ae5e0798393ef25f2dc72faf43703e60ba089b07d7170acbabbf8f62`  
		Last Modified: Wed, 21 May 2025 22:27:39 GMT  
		Size: 28.2 MB (28225330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70560b6a1d2ac5ce7d475d1b19aef7b6dfdbcdb9726a97f72313c747438d1256`  
		Last Modified: Wed, 21 May 2025 23:25:09 GMT  
		Size: 3.5 MB (3500662 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:69e65b2e2b915579fcfa113bf55278ab097fe5c312ea76e806be377210309583`  
		Last Modified: Wed, 21 May 2025 23:25:10 GMT  
		Size: 34.9 MB (34924785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf4e415374323cf405025d70e63ed0497db2e8ef5d85a8becfda7ac7784ab73c`  
		Last Modified: Wed, 21 May 2025 23:44:31 GMT  
		Size: 6.4 MB (6430125 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:1b16feafde4cb770f7331950d8ca57ae0467839c1ca3f4ac03a6ccefcb17fa5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2431194 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06a0435729bcf64320ba3760665ae5260af1d05cc193203a4158eaf2f1e5ac8c`

```dockerfile
```

-	Layers:
	-	`sha256:1d23a14a798ed309320e17b299a46e79315c208fabcc92c7dfeac572e5145694`  
		Last Modified: Wed, 21 May 2025 23:44:31 GMT  
		Size: 2.4 MB (2422403 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c8bd50df6b4d80f369d43853a8874ef4caad3a7f40dde2b78b8c7f185732e1ae`  
		Last Modified: Wed, 21 May 2025 23:44:31 GMT  
		Size: 8.8 KB (8791 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.11` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:d3fb7ab8e92171198240bbe178dcdbb51e74701e763f85f2d58d3ae1b325d1c1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.0 MB (71008269 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5e3343221ef2d290a158b19194be8a7a392c51eac290594e26cd017c1f6d118b`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 18:15:04 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1747699200'
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
	-	`sha256:b16f1b16678093d11ecfece1004207a40f9bc1b7d9d1d16a070c1db552038818`  
		Last Modified: Wed, 21 May 2025 22:27:55 GMT  
		Size: 28.1 MB (28065280 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5b34c0864b21df07043a4f72f31413df551a49d5e348e13537c44e7a6bce76d6`  
		Last Modified: Thu, 22 May 2025 04:59:23 GMT  
		Size: 3.3 MB (3324368 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e61fc8410f1c3ba59c6ee0e822032640906b4c29c89b4c0487774885b5d03ef6`  
		Last Modified: Thu, 22 May 2025 04:59:23 GMT  
		Size: 33.2 MB (33188270 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b500bbca80c79ff1e1c41586588c51f3b816bfff116cba4a0da7feeea77f3810`  
		Last Modified: Thu, 22 May 2025 12:16:56 GMT  
		Size: 6.4 MB (6430351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:4482ba5f993831a13c766db9bc9be086e0640063d6b5d1e0d21b6aa37f60f64c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2431651 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e996a9f62a221c5832749e498c769ca34ac38c59759fab18780272826eff456f`

```dockerfile
```

-	Layers:
	-	`sha256:e2a79c946fde487e38716ac9c65c89dad6996b7bb1631e1c5ab2ba6c95780b64`  
		Last Modified: Thu, 22 May 2025 12:16:56 GMT  
		Size: 2.4 MB (2422710 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94d9d05a6d3169aa0a39b3b70578ee0219ca11a5e6e0e2ffdb7a97c319989131`  
		Last Modified: Thu, 22 May 2025 12:16:56 GMT  
		Size: 8.9 KB (8941 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.11` - linux; 386

```console
$ docker pull hylang@sha256:56dacd2bac063d2b4834cf38af69036f6ec4877a775e924b1858df91e0e55ba9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70567719 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f549ffec8e1f67af9d659993731c22d1e8e7d065535346d3be6ef00cd7a6b36`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 18:15:04 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1747699200'
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
	-	`sha256:7d0eb60defa1a32d12e94bc0d7c2c578881c578aeec0c1d786ef5a19c72a34ab`  
		Last Modified: Wed, 21 May 2025 22:27:56 GMT  
		Size: 29.2 MB (29207487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ebb33de2153131b801147d53b481b9fa7a057de56d7119b032228c9e4f03461`  
		Last Modified: Wed, 21 May 2025 23:22:13 GMT  
		Size: 3.5 MB (3506071 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b380731cba4b5bebd0a60646f2861fbed12e5c71391dfebe71461e525bb74cc8`  
		Last Modified: Wed, 21 May 2025 23:22:14 GMT  
		Size: 31.4 MB (31423890 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:96b96954f1360f40eec008d2bd81a9cece24d318415d153f282baf95ad3dc47c`  
		Last Modified: Wed, 21 May 2025 23:44:19 GMT  
		Size: 6.4 MB (6430271 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:062e22b902f21b152e319dfbe444822438b1a608775d160bde02a8b39829fe39
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2428301 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f74c41dcfd63bf332b319459a417c75f854957371c646ffbdc225a5875df4d1e`

```dockerfile
```

-	Layers:
	-	`sha256:beebae2cc6b8815ce5c59a875e4854e1fc7011f897b7a39260ba0b7cc0d9aa2c`  
		Last Modified: Wed, 21 May 2025 23:44:19 GMT  
		Size: 2.4 MB (2419562 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:283394278dad6cb098e66beabda7d279754ba6d3a23d3e2c8eb8739791c93177`  
		Last Modified: Wed, 21 May 2025 23:44:19 GMT  
		Size: 8.7 KB (8739 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.11` - windows version 10.0.26100.4061; amd64

```console
$ docker pull hylang@sha256:a9073796cf07018de3e0af56ce858de90609bbc29647c222503aa483556b9ed4
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 GB (3484717977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:598f9c0bdb898982cb15e5365e95248b78512fb214c9945b14f49b52fbc24bcb`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sat, 10 May 2025 01:13:32 GMT
RUN Install update 10.0.26100.4061
# Wed, 14 May 2025 21:02:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:02:14 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 14 May 2025 21:02:24 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 14 May 2025 21:02:25 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 14 May 2025 21:03:02 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'b61c7c1dbf879eda6f779c374bfbbeecd3f618ada08404705a1a19d39df48dbd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 14 May 2025 21:03:03 GMT
CMD ["pypy"]
# Wed, 14 May 2025 22:13:08 GMT
ENV HY_VERSION=1.1.0
# Wed, 14 May 2025 22:13:09 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 14 May 2025 22:14:06 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 14 May 2025 22:14:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Tue, 10 Dec 2024 22:58:14 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc834e13e71633c2d66ec6513d57c31a3157fc5933859d492ecf45fc8a7476c3`  
		Last Modified: Tue, 13 May 2025 21:56:34 GMT  
		Size: 1.2 GB (1215458626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9098833f947643744e5991c909aec1ebeb70388ef7ceb347dadb7f8bfa9b3973`  
		Last Modified: Wed, 14 May 2025 21:03:07 GMT  
		Size: 1.4 KB (1361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e207549521cc696415e0b0eee10e37aa1b50123893e918e0dbb64e3740f91e`  
		Last Modified: Wed, 14 May 2025 21:03:06 GMT  
		Size: 359.2 KB (359196 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f79419b50f409a1953c76c10e3b6d90c89d9d51926835771fc0e778ce50b7a`  
		Last Modified: Wed, 14 May 2025 21:03:07 GMT  
		Size: 15.5 MB (15537422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:699d2fd4631a03722ab9590155c1609c638b3360d097da6dfa6de3c4652b0765`  
		Last Modified: Wed, 14 May 2025 21:03:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:622466bfc71a28f5d443525ac042b3f5af8cdf3ea86006dc3d9f02260f121664`  
		Last Modified: Wed, 14 May 2025 21:03:10 GMT  
		Size: 30.7 MB (30667297 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e41d8d72424a5409b0823a7ed45892937c80b20f837df0f92abfdc6d73fa8d`  
		Last Modified: Wed, 14 May 2025 21:03:05 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0660df8f2b435b655e977631a6cb9348203b1b34872d9dc4d28a0695f2de201b`  
		Last Modified: Wed, 14 May 2025 22:14:11 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b1fe7b52f676ac162175e25a026e78f0eb26f4a68575bbc8fc10c51131fe4f`  
		Last Modified: Wed, 14 May 2025 22:14:11 GMT  
		Size: 1.3 KB (1311 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f86ec72210266bca54697f4a5796a297d3d346a10ec6b7a0723d0a1b348dfa89`  
		Last Modified: Wed, 14 May 2025 22:14:12 GMT  
		Size: 7.4 MB (7380452 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a853ecd159bdd05b2843ff8fa120a2d1ce0085ef2e257f34e204ad002dbfe7`  
		Last Modified: Wed, 14 May 2025 22:14:11 GMT  
		Size: 1.3 KB (1294 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-pypy3.11` - windows version 10.0.20348.3692; amd64

```console
$ docker pull hylang@sha256:8753a25bc48ebf085fe06ff12f9ef6edd924d0e68465f96e74a77eefd42b53f2
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327491959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b97663a5a675ebce1f96d749d3dadfae6e8aa5420d27f3c119fb79dbf047fb99`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Fri, 09 May 2025 19:38:10 GMT
RUN Install update 10.0.20348.3692
# Wed, 14 May 2025 21:06:04 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:06:15 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 14 May 2025 21:06:26 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 14 May 2025 21:06:26 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 14 May 2025 21:07:00 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'b61c7c1dbf879eda6f779c374bfbbeecd3f618ada08404705a1a19d39df48dbd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 14 May 2025 21:07:01 GMT
CMD ["pypy"]
# Wed, 14 May 2025 22:16:48 GMT
ENV HY_VERSION=1.1.0
# Wed, 14 May 2025 22:16:49 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 14 May 2025 22:17:45 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 14 May 2025 22:17:46 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:2534953f34d35976fc44cd67bfdd39fdcd9e2eaae57ada0be53d5fb936cd3a0b`  
		Last Modified: Tue, 10 Sep 2024 17:49:01 GMT  
		Size: 1.5 GB (1462192413 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f99f0856d3665c6aeede32823351187cdab09d90cb8608ff70427d552ab356b`  
		Last Modified: Tue, 13 May 2025 18:47:51 GMT  
		Size: 811.4 MB (811435715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a447df532314074c2a0ee31a25e6f05318ade4d7ad645059c532de7cd218e08f`  
		Last Modified: Wed, 14 May 2025 21:07:07 GMT  
		Size: 1.3 KB (1280 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d54caa3ebc7a9414786b065cc55008cced805c3262a860bdfdc6b1d46408702e`  
		Last Modified: Wed, 14 May 2025 21:07:06 GMT  
		Size: 346.6 KB (346618 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d026cad37f700455ad7277a1a6cd44667c58834e0baa0e1d96e2fdfd4ab93bac`  
		Last Modified: Wed, 14 May 2025 21:07:07 GMT  
		Size: 15.5 MB (15529033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1bff47f97580492e230d949d6cf248380e515eec3c11d231449ce38ea6e17e2`  
		Last Modified: Wed, 14 May 2025 21:07:06 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c347aa679a2be24727200dc9c99a57f6603a9c1294b5b85afde7ba3b8bf75af`  
		Last Modified: Wed, 14 May 2025 21:07:10 GMT  
		Size: 30.6 MB (30616274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d93d4209cae98d289ee79b61ab55d361ea7dcc2291d7d51bfbcd9e1ee58d865`  
		Last Modified: Wed, 14 May 2025 21:07:06 GMT  
		Size: 1.3 KB (1279 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c03664ab9c218f2074b38cb9c09d086a1d4751f477af3ee5ddf5aae9d7aeb9c`  
		Last Modified: Wed, 14 May 2025 22:17:48 GMT  
		Size: 1.4 KB (1362 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cf996d77abc29343bb336ceaa840b52c8b148c080c0177ff2b9207f33575339`  
		Last Modified: Wed, 14 May 2025 22:17:48 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6a065a578a74469056e140467fb5061df98f02a60b8afc2fe3852ef730dd263`  
		Last Modified: Wed, 14 May 2025 22:17:49 GMT  
		Size: 7.4 MB (7364071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a37d952e7515377df844856e79a661fed5d2d2fcbbb0e041af1536db636d26b7`  
		Last Modified: Wed, 14 May 2025 22:17:48 GMT  
		Size: 1.3 KB (1282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-pypy3.11` - windows version 10.0.17763.7314; amd64

```console
$ docker pull hylang@sha256:ee281fce666c8a146217ccc7a49a0e484978e3df59073dc9108ca23436a458fd
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2237534011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2226418637c4dc57105c1379b9b6d80e88d58504979a7bb40207af20605a9cd3`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Fri, 09 May 2025 13:51:15 GMT
RUN Install update 10.0.17763.7314
# Wed, 14 May 2025 21:03:20 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 14 May 2025 21:03:55 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Wed, 14 May 2025 21:04:15 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Wed, 14 May 2025 21:04:16 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 14 May 2025 21:04:53 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'b61c7c1dbf879eda6f779c374bfbbeecd3f618ada08404705a1a19d39df48dbd'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Wed, 14 May 2025 21:04:54 GMT
CMD ["pypy"]
# Wed, 14 May 2025 21:16:32 GMT
ENV HY_VERSION=1.1.0
# Wed, 14 May 2025 21:16:34 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 14 May 2025 21:18:06 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 14 May 2025 21:18:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:803f4a9590cb9c635813cbd0ee89190f92d5fe4c7589711cf468879e42ce02ba`  
		Last Modified: Tue, 10 Sep 2024 17:55:31 GMT  
		Size: 1.7 GB (1720268357 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a95a939635fd6bec8c1562dcdbdde2fdb64095d1be9873313939c878db6f7279`  
		Last Modified: Tue, 13 May 2025 17:48:34 GMT  
		Size: 463.4 MB (463449115 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcef82d3bc4d9a78846787b4ddcafa55833c47f0ec3e407ad06a0a405d837c8e`  
		Last Modified: Wed, 14 May 2025 21:05:00 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baa6d4758efba8694a254ab7799a6064012c9b762ed96f7fafa4883e260db5cd`  
		Last Modified: Wed, 14 May 2025 21:04:59 GMT  
		Size: 340.0 KB (340031 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6eed48995b2c8fe111e6ea2c67e86bb56c24e452148524ae75a598d89487fbb`  
		Last Modified: Wed, 14 May 2025 21:05:00 GMT  
		Size: 15.5 MB (15503001 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae25fc757102c942da738c4683627b433084b5ddbd70cc97cab5ded57789405`  
		Last Modified: Wed, 14 May 2025 21:04:58 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:531ad46908c75a82064c070fc6eb67f23651dbd8877265b8fd12a04663639d84`  
		Last Modified: Wed, 14 May 2025 21:05:03 GMT  
		Size: 30.6 MB (30615271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:890e887abae3644d0a127fb8a5060714bf8a481109183baa2c5b6a20833f835d`  
		Last Modified: Wed, 14 May 2025 21:04:58 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:374d8eb2231efd228a5b4558582eaabc4d238795142241a4b58b30fa5d0aaf1e`  
		Last Modified: Wed, 14 May 2025 21:18:10 GMT  
		Size: 1.4 KB (1380 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f5b8e7d26487f32140ed711f5133f639a1976689b69d74e6b6f768fa52d35e6`  
		Last Modified: Wed, 14 May 2025 21:18:10 GMT  
		Size: 1.4 KB (1363 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89c2f23c467341a70ef659362514089a2da973023c81d15639b1e7e687d8d550`  
		Last Modified: Wed, 14 May 2025 21:18:11 GMT  
		Size: 7.4 MB (7350282 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e47bdc3b2e64d9d8d7e8cc9ede21126dcf8b1d8d96f7459f5be9e7ead5dc8af9`  
		Last Modified: Wed, 14 May 2025 21:18:10 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
