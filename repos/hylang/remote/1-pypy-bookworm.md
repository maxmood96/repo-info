## `hylang:1-pypy-bookworm`

```console
$ docker pull hylang@sha256:2c469f98e2b745e561a95366ebea3fd8c8c231c76c5b909f3b619218ba244ee9
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:1-pypy-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:58e2e46254b59aa6690a60d8ece33677494aae56ddf99464f88dad5b9f014af8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73131181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca9974a54acd173732b7f08d4cc77b426f439c374405e93878a7a4baea07bd0e`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1751241600'
# Fri, 04 Jul 2025 16:11:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 16:11:27 GMT
ENV LANG=C.UTF-8
# Fri, 04 Jul 2025 16:11:27 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 16:11:27 GMT
ENV PYPY_VERSION=7.3.20
# Fri, 04 Jul 2025 16:11:27 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 04 Jul 2025 16:11:27 GMT
CMD ["pypy3"]
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HY_VERSION=1.1.0
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 08 Jul 2025 16:37:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Jul 2025 16:37:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3da95a905ed546f99c4564407923a681757d89651a388ec3f1f5e9bf5ed0b39d`  
		Last Modified: Tue, 01 Jul 2025 01:14:43 GMT  
		Size: 28.2 MB (28230143 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7b9b025206b42a63d3bae2f14b6176010d0702eef981a1792710d089ce37aade`  
		Last Modified: Mon, 07 Jul 2025 20:58:23 GMT  
		Size: 3.5 MB (3507070 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ca35457d78b43a6b39ac85c1dd60c59dcfad262b02167c1cf2b5059f19cf989`  
		Last Modified: Mon, 07 Jul 2025 20:58:26 GMT  
		Size: 35.0 MB (34958767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fb502da20c96a8ac7b7f51763fe4da0925cfe3fd0b7d4878d69220dc0a41fd8e`  
		Last Modified: Tue, 08 Jul 2025 22:55:10 GMT  
		Size: 6.4 MB (6435201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:87056a6fe61d0d8093a9bb8da3b3f46bc1f9cce4ce99be14f04527d5d1534e45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2525504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f66a15eed60ece5d2d523a7370aef6167618de13649ed78400449473b7813c70`

```dockerfile
```

-	Layers:
	-	`sha256:0be769a99fcfb5d0d56cbcf408e075c37bbf779e7df3b1c7103da5e09b1b23f1`  
		Last Modified: Tue, 08 Jul 2025 17:18:57 GMT  
		Size: 2.5 MB (2514242 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b9b704cd3c3b773da9e68b8e91c9bf5c080d45bb99992de2c737eca40e4cb990`  
		Last Modified: Tue, 08 Jul 2025 17:18:57 GMT  
		Size: 11.3 KB (11262 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:0ea44ba58504cd9af8efabb6ccebeeffced070764ee81eae47630a860bc518e5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.1 MB (71116720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f670d7785796fde66b1303504d7c8dcadbc8bb882c370041d513fd30dd5bce45`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1751241600'
# Fri, 04 Jul 2025 16:11:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 16:11:27 GMT
ENV LANG=C.UTF-8
# Fri, 04 Jul 2025 16:11:27 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 16:11:27 GMT
ENV PYPY_VERSION=7.3.20
# Fri, 04 Jul 2025 16:11:27 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 04 Jul 2025 16:11:27 GMT
CMD ["pypy3"]
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HY_VERSION=1.1.0
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 08 Jul 2025 16:37:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Jul 2025 16:37:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:37259e7330667afd74c3386d3ed869f06bd9b7714370c78e3065f4e28607cc02`  
		Last Modified: Tue, 01 Jul 2025 01:15:09 GMT  
		Size: 28.1 MB (28077678 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:131a191f7acaa76984082e9b61dbb924317dd2c6646fbb10813e86ba908ed8ee`  
		Last Modified: Tue, 08 Jul 2025 03:00:12 GMT  
		Size: 3.3 MB (3329287 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0c2c9b964bef8c3150610f905459ffc64532ae8b743b4008f91460755b9030`  
		Last Modified: Tue, 08 Jul 2025 03:00:15 GMT  
		Size: 33.3 MB (33274401 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:059ef3e387990acaa23054a674a467ebf2c37fd9d469c5ecdfd8308f5957b954`  
		Last Modified: Tue, 08 Jul 2025 05:03:01 GMT  
		Size: 6.4 MB (6435354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:a0d5d09f60ed43f0d4b90cb8a750b9d4988ef4876c51da4fd2c9313da3ec3bb8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2526156 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b32c03d26a12d1e90b8ec2ac7bd155cd7fef629a7a15d02c3919da01a84aeb2f`

```dockerfile
```

-	Layers:
	-	`sha256:e0b3231243d71f34f13768e27752c14789c8dc659526002fff9998be312cc763`  
		Last Modified: Tue, 08 Jul 2025 20:17:52 GMT  
		Size: 2.5 MB (2514645 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64c429658ef39142ceffab343578021de0bc216836ff5536465b83fa021063fe`  
		Last Modified: Tue, 08 Jul 2025 20:17:52 GMT  
		Size: 11.5 KB (11511 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:d7d48e9c2b8e0e2243797dff283d9367a0adf06c0ade341b495dbb67fb122a66
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70558464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3ea0fcdba9bbe792cd187220245c8a9644f9732b8a9ff8cdd6b7f41738f7c60a`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 30 Jun 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1751241600'
# Fri, 04 Jul 2025 16:11:27 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 04 Jul 2025 16:11:27 GMT
ENV LANG=C.UTF-8
# Fri, 04 Jul 2025 16:11:27 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 04 Jul 2025 16:11:27 GMT
ENV PYPY_VERSION=7.3.20
# Fri, 04 Jul 2025 16:11:27 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Fri, 04 Jul 2025 16:11:27 GMT
CMD ["pypy3"]
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HY_VERSION=1.1.0
# Tue, 08 Jul 2025 16:37:15 GMT
ENV HYRULE_VERSION=1.0.0
# Tue, 08 Jul 2025 16:37:15 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 08 Jul 2025 16:37:15 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:88e96ee0cb4c7106f4d6a5cdeaeb171ec22a2484245e406cb5267b2be095937c`  
		Last Modified: Tue, 01 Jul 2025 01:14:33 GMT  
		Size: 29.2 MB (29212432 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e9c5b3fdac273aea36798d705cdf198b485aed7f88550e93b624668bf6af5102`  
		Last Modified: Mon, 07 Jul 2025 20:59:43 GMT  
		Size: 3.5 MB (3509203 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d993fda75180aa33b6e30711fdf27732040a487267ccd653d1a9220f4620aa0a`  
		Last Modified: Mon, 07 Jul 2025 20:59:45 GMT  
		Size: 31.4 MB (31401617 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd73e7202e7ff4895ed43a0c7d6c22b3d55c7551753a7e63a7cde74db2339067`  
		Last Modified: Tue, 08 Jul 2025 16:59:04 GMT  
		Size: 6.4 MB (6435212 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:52b1cda27c4e30d81765f5f0685deb3be020927f14249ee913f7cb6aecbc1234
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2522532 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aa4cabfb9faf9d2c9ed358f61d75cc8bfb68727a5d2c2de5322a91b274d5ce26`

```dockerfile
```

-	Layers:
	-	`sha256:7090e264ea5838d295f2170c7b98756f5a20758c2a4c410861e395a056f70b4b`  
		Last Modified: Tue, 08 Jul 2025 17:19:05 GMT  
		Size: 2.5 MB (2511361 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f68ed257b7d00ace1db5c5c4267281e6b21c782db4e9137ec7195f39f0f62559`  
		Last Modified: Tue, 08 Jul 2025 17:19:06 GMT  
		Size: 11.2 KB (11171 bytes)  
		MIME: application/vnd.in-toto+json
