## `hylang:1-pypy3.10`

```console
$ docker pull hylang@sha256:318ef34e0fcb0a4c1e51ebbc6e242878e81b97826715348d6f00f27221d6ddfd
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

### `hylang:1-pypy3.10` - linux; amd64

```console
$ docker pull hylang@sha256:16036774b43c85b9ced266e4b2b18299a896f623d27767cfe7d964210f865e8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72601658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:894bf442b5b45960242b32b8410d5f45592804903d7b0a750e2e74982e9a111c`
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
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux64.tar.bz2'; 			sha256='c73ac2cc2380ac9227fd297482bf2a3e17a80618ba46db7544d535515321ec1e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-aarch64.tar.bz2'; 			sha256='af27a589178f11198e2244ab65ca510630ba97c131d7ccc4021eb5bc58de7f57'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux32.tar.bz2'; 			sha256='e63a4fcad2641ee541e852918befb513abf04ce7070f743a50778cae9f9da80e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
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
	-	`sha256:834d017745d134dc27292cde14481beeb9f0c7e9b1860d7d730f84f876c36c9b`  
		Last Modified: Mon, 28 Apr 2025 22:02:11 GMT  
		Size: 3.5 MB (3499346 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1cf580513c289900f44a93e3e04d0f68927a7ebc975b3bacd27de0b06816f32c`  
		Last Modified: Mon, 28 Apr 2025 22:02:12 GMT  
		Size: 34.5 MB (34510211 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8343fd478883d2a73fa330d742594c71adeaf753e873b206933ea6face99dd20`  
		Last Modified: Fri, 09 May 2025 17:38:27 GMT  
		Size: 6.4 MB (6364459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.10` - unknown; unknown

```console
$ docker pull hylang@sha256:e95898efc65095afc38e665c2e4549c36332e4efd16ade9885459df737693022
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2418371 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:14a5831817ead0273db9fdc423252b394aaac27fe1e7cb33b94ff28d03c33428`

```dockerfile
```

-	Layers:
	-	`sha256:ec0a14912f37f6924580bc7ab991fe124be2a972f75e317d132a881d09dca7c9`  
		Last Modified: Fri, 09 May 2025 17:38:26 GMT  
		Size: 2.4 MB (2407108 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0904646819f80ee9786f921207ae53ab373148749630c0b06fb2523d86cde8e3`  
		Last Modified: Fri, 09 May 2025 17:38:25 GMT  
		Size: 11.3 KB (11263 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.10` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:65372cd9426d031b2357bb6af55778ef0ccceb24b1d1afd8fa4893b8d660945d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70531620 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57790edb16b9b5c4e76ecd6e38ee963c6d6654dc2c7a35f172bc2258d11ca30a`
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
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux64.tar.bz2'; 			sha256='c73ac2cc2380ac9227fd297482bf2a3e17a80618ba46db7544d535515321ec1e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-aarch64.tar.bz2'; 			sha256='af27a589178f11198e2244ab65ca510630ba97c131d7ccc4021eb5bc58de7f57'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux32.tar.bz2'; 			sha256='e63a4fcad2641ee541e852918befb513abf04ce7070f743a50778cae9f9da80e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
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
	-	`sha256:a659fd38d987edd545ad2e83774e01639ad15824134622db2656060563900ac3`  
		Last Modified: Tue, 29 Apr 2025 21:54:30 GMT  
		Size: 32.8 MB (32777529 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ac7e2d2d6c92dcb84dd4c0e2e12fca11cbf7836f715acf40342091e02b8e801`  
		Last Modified: Fri, 09 May 2025 19:03:19 GMT  
		Size: 6.4 MB (6364506 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.10` - unknown; unknown

```console
$ docker pull hylang@sha256:bd853c0495c7844729a8402b9b220505af54100f6b3919daf8cee6455b7b892c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2419022 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91270b44f234f8800c205f01f92099dba6659e8c886540c9e1cb0b3453fa5285`

```dockerfile
```

-	Layers:
	-	`sha256:cd52db6e11cf180d1f36a944e5f7082de8a078dd0aaac6e142bb19a850367320`  
		Last Modified: Fri, 09 May 2025 19:03:19 GMT  
		Size: 2.4 MB (2407511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:739b183984797c58d04dcc2d3849e80dafb2a497257cf57e360c568411e8aa57`  
		Last Modified: Fri, 09 May 2025 19:03:18 GMT  
		Size: 11.5 KB (11511 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.10` - linux; 386

```console
$ docker pull hylang@sha256:a04a25966f7a78d49dd83329860432417d4021ad969da6ac10b95c5be13bdd77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70045496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5f3ab0aafd8c80408e62f10681f836abf53360388c29ab2bb0518d0e8e68327a`
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
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux64.tar.bz2'; 			sha256='c73ac2cc2380ac9227fd297482bf2a3e17a80618ba46db7544d535515321ec1e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-aarch64.tar.bz2'; 			sha256='af27a589178f11198e2244ab65ca510630ba97c131d7ccc4021eb5bc58de7f57'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.10-v7.3.19-linux32.tar.bz2'; 			sha256='e63a4fcad2641ee541e852918befb513abf04ce7070f743a50778cae9f9da80e'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.10; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
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
	-	`sha256:f9946aa2e61aa88cff6568e15cd9cf227711dea9d16a0e36669d7a05facc0e9b`  
		Last Modified: Mon, 28 Apr 2025 21:56:30 GMT  
		Size: 3.5 MB (3503472 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:763d60629c06adce6c084d3fe5c82ce4326a4bedfc809becfd236b8874c60e7c`  
		Last Modified: Mon, 28 Apr 2025 21:56:31 GMT  
		Size: 31.0 MB (30966634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ee0fb4121723654f95a84b95bed4690a1c0843d2ef0e9bb510b116ca5e6d0db0`  
		Last Modified: Fri, 09 May 2025 17:36:27 GMT  
		Size: 6.4 MB (6364524 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.10` - unknown; unknown

```console
$ docker pull hylang@sha256:41b45991e91fee3aa826c55316eb51d95ba5ab31e83f4124f0d245724e961d5b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2415356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1846e0d2671a5ea536d88d1f4301fb4555517fdd657441e79040afc4b2b5d70b`

```dockerfile
```

-	Layers:
	-	`sha256:92beb31b7f8898513e29177b3b584d6fbe3f0a7dfbf5bfdac1eebdaab12e56bf`  
		Last Modified: Fri, 09 May 2025 17:36:27 GMT  
		Size: 2.4 MB (2404185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aac75ba20acc3522f49055d2750ef5039a3dce2b61a20a57c10e6236e6a0c25`  
		Last Modified: Fri, 09 May 2025 17:36:27 GMT  
		Size: 11.2 KB (11171 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.10` - windows version 10.0.26100.3781; amd64

```console
$ docker pull hylang@sha256:3914c64625b0d0d772f8034548af64cfd3919aeb86a41d49ff63db576c1b91cb
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.4 GB (3448743006 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cddc37e9600b50d301a301230fe5d8aae0ff08cd2e92701433aac524b1438acc`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Tue, 15 Apr 2025 10:03:37 GMT
RUN Install update 10.0.26100.3781
# Fri, 18 Apr 2025 03:23:24 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:23:31 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:23:42 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:23:42 GMT
ENV PYPY_VERSION=7.3.19
# Fri, 18 Apr 2025 03:24:18 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.10-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'c0d07bba6c8fb4e5804f4a8b3f8ef07cc3d89f6ad1db42a45ffb9be60bbb7cc2'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.10-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:24:19 GMT
CMD ["pypy"]
# Fri, 09 May 2025 17:36:44 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 17:36:45 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 17:37:39 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 09 May 2025 17:37:40 GMT
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
	-	`sha256:fa908c9f290ab95181fd0a67c7a5fc7f3185bc0e8c4f268da4761d5d13b2e644`  
		Last Modified: Fri, 18 Apr 2025 03:24:27 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f9dc684dae6e1520a3bf075361f6f546d9dea37d9fa1e53c5eec3d027344184`  
		Last Modified: Fri, 18 Apr 2025 03:24:24 GMT  
		Size: 368.7 KB (368737 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450a51b4830f9cc22ba367161c374312307d4914d6c6e798bbc8148d8ad4381f`  
		Last Modified: Fri, 18 Apr 2025 03:24:25 GMT  
		Size: 15.5 MB (15542481 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3eb531bcab613070f64d0ebb890faa219e217cb471146727c6eed9c2b8e7d33`  
		Last Modified: Fri, 18 Apr 2025 03:24:23 GMT  
		Size: 1.4 KB (1377 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f8ec59d64bccd02c308b80a549c92bf8fdbd1a70c8155bcef5bece35c861a23`  
		Last Modified: Fri, 18 Apr 2025 03:24:28 GMT  
		Size: 30.3 MB (30316645 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bb7d851f30002475ba77bb61a44b4ec5c1ece9483de8186de6ccd610e9dad9c`  
		Last Modified: Fri, 18 Apr 2025 03:24:23 GMT  
		Size: 1.3 KB (1317 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d50b2b585b8c518a5201fe17806e7f64f5737a966d85a3c6a0ec754a39c42ffb`  
		Last Modified: Fri, 09 May 2025 17:37:44 GMT  
		Size: 1.4 KB (1367 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1358e1d047bb06f9eb7baf369280ec438f96ec11ebf833fa4cf798914062bb78`  
		Last Modified: Fri, 09 May 2025 17:37:44 GMT  
		Size: 1.4 KB (1351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f62b92cfe88c338df59f52f0137c4e7c2b6651bc2b71307471a1ebca1faa565`  
		Last Modified: Fri, 09 May 2025 17:37:45 GMT  
		Size: 7.3 MB (7345802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b26282ef3483e1c76e7e5bc9000c7feac92746d336c54d18de56e92f9f487136`  
		Last Modified: Fri, 09 May 2025 17:37:44 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-pypy3.10` - windows version 10.0.20348.3566; amd64

```console
$ docker pull hylang@sha256:746a417836a6402712662d0cb220a79f457024fc23cae5f00d6d7e582769a70e
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 GB (2327034970 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8226c034ee85272b5f2a5a107b0b84fc3ca8c7d172310976ab8acf157711c6c7`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 00:01:38 GMT
RUN Apply image 10.0.20348.2700
# Wed, 16 Apr 2025 03:49:18 GMT
RUN Install update 10.0.20348.3566
# Fri, 18 Apr 2025 03:26:06 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:26:16 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:26:26 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:26:27 GMT
ENV PYPY_VERSION=7.3.19
# Fri, 18 Apr 2025 03:26:58 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.10-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'c0d07bba6c8fb4e5804f4a8b3f8ef07cc3d89f6ad1db42a45ffb9be60bbb7cc2'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.10-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:26:59 GMT
CMD ["pypy"]
# Fri, 09 May 2025 17:30:57 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 17:30:58 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 17:32:14 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 09 May 2025 17:32:15 GMT
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
	-	`sha256:10c433f36be387bab6cd58098fab96fafc81754566604422bb8ce498b95b6f79`  
		Last Modified: Fri, 18 Apr 2025 03:27:06 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6689384bdd3137c06df1dfafda54f1a31ca58fc5ca86e78ddf9f346aa87eac9a`  
		Last Modified: Fri, 18 Apr 2025 03:27:04 GMT  
		Size: 345.3 KB (345298 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:758dc2ed79c912d466852c10ed2f83c336bc6c29b7078fa9714ceb07e4620c55`  
		Last Modified: Fri, 18 Apr 2025 03:27:05 GMT  
		Size: 15.5 MB (15529144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca38a46d01872d672cbb9ee8d8a31675fbc37fcc82f86b8ffd94cb910bebde73`  
		Last Modified: Fri, 18 Apr 2025 03:27:04 GMT  
		Size: 1.3 KB (1283 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b063df898ee9aed5b60d789617200ffa1c1fd470c7cdb6747dbc1c5a74edd624`  
		Last Modified: Fri, 18 Apr 2025 03:27:08 GMT  
		Size: 30.3 MB (30263565 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d266264537a4e7ecaa0eee95143bede245a8dfea18182fb09108d69369c0de8c`  
		Last Modified: Fri, 18 Apr 2025 03:27:04 GMT  
		Size: 1.3 KB (1278 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e49e514e6cac6a8a125669394055529cb31b6ed79caad89ab0d6f5d6d40d0e0`  
		Last Modified: Fri, 09 May 2025 17:32:19 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b75e3e9c87092bc798ca49426d0a205f6f7ff2d2df54891ee81dbc892d211d1d`  
		Last Modified: Fri, 09 May 2025 17:32:19 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:095ebf413f66f7dd7cfedded9de92b97e6d068e7b285aea71d401e80c65725b7`  
		Last Modified: Fri, 09 May 2025 17:32:21 GMT  
		Size: 7.3 MB (7306609 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:978faf33ecf01999451dd60fabf6fa544256bc6f7605d6be80fe69fa3d9f6c1c`  
		Last Modified: Fri, 09 May 2025 17:32:19 GMT  
		Size: 1.4 KB (1387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-pypy3.10` - windows version 10.0.17763.7249; amd64

```console
$ docker pull hylang@sha256:b46202409e997610d743c7896ecdc7e77286cdda60f02aea85082bd8638df6a7
```

-	Docker Version: 27.5.1
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2218947724 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c69a22d6b461cbf958e65daaf73047e39f21fd8825348952037c2dc987db0caa`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Fri, 06 Sep 2024 01:15:31 GMT
RUN Apply image 10.0.17763.6293
# Tue, 15 Apr 2025 01:47:49 GMT
RUN Install update 10.0.17763.7249
# Fri, 18 Apr 2025 03:24:07 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Fri, 18 Apr 2025 03:24:36 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:24:51 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:24:52 GMT
ENV PYPY_VERSION=7.3.19
# Fri, 18 Apr 2025 03:25:33 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.10-v7.3.19-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'c0d07bba6c8fb4e5804f4a8b3f8ef07cc3d89f6ad1db42a45ffb9be60bbb7cc2'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.10-v7.3.19-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Fri, 18 Apr 2025 03:25:34 GMT
CMD ["pypy"]
# Fri, 09 May 2025 17:31:47 GMT
ENV HY_VERSION=1.1.0
# Fri, 09 May 2025 17:31:49 GMT
ENV HYRULE_VERSION=1.0.0
# Fri, 09 May 2025 17:33:27 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Fri, 09 May 2025 17:33:28 GMT
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
	-	`sha256:bcc4fb98826135d52ce1f95ca92ce2d88a500f54c7fedd6b06a1f8e8e9ed2ad7`  
		Last Modified: Fri, 18 Apr 2025 03:25:39 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b864fb56703722e675dc8423ab0ba67280fbc11156710d0a61656430848bd48`  
		Last Modified: Fri, 18 Apr 2025 03:25:37 GMT  
		Size: 337.1 KB (337110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da84b6bb8e338359fcc14930caba779460ca0ca379685c52effc5d42ce9acd9a`  
		Last Modified: Fri, 18 Apr 2025 03:25:39 GMT  
		Size: 15.5 MB (15500109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27800dd143e465243fdce6b4d88d416c5834994610c857d9b8af11c5e9e5cd7f`  
		Last Modified: Fri, 18 Apr 2025 03:25:37 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:150fbea98227e61929bb6e6eba71bf0fc2bee10aeb59878ee3726998a6d6ae8c`  
		Last Modified: Fri, 18 Apr 2025 03:25:41 GMT  
		Size: 30.3 MB (30281242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33555dbd995478b0b216fffe82e2cf941986c82596e52303b4292e6475e28de6`  
		Last Modified: Fri, 18 Apr 2025 03:25:37 GMT  
		Size: 1.3 KB (1277 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98e7e032ff2a25ccca1e6bc311391ea48e4e6d8892f0efcd893c7c55ee2f8b10`  
		Last Modified: Fri, 09 May 2025 17:33:33 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a948d217b9e02352c727345b9e28a8f0824159797a02919ac7667245213f4d5`  
		Last Modified: Fri, 09 May 2025 17:33:32 GMT  
		Size: 1.3 KB (1327 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bd4153d2fceabb15cb58b108224a1dc7b27e270511ac03ad9563811c0cabf6f`  
		Last Modified: Fri, 09 May 2025 17:33:34 GMT  
		Size: 7.3 MB (7295689 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4137b8ce9210282c936cd880ea15671488d1a20d9c34ab87ec5460c93b704353`  
		Last Modified: Fri, 09 May 2025 17:33:33 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
