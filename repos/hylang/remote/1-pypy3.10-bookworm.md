## `hylang:1-pypy3.10-bookworm`

```console
$ docker pull hylang@sha256:068a24abc46a57e7e0654cfa3f26297f41b8f558d09549c69105db44c7010d84
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:1-pypy3.10-bookworm` - linux; amd64

```console
$ docker pull hylang@sha256:15e7014367b0da55906d6a3453bd9846cd707aa5104c20054acebfa1ab7a7b64
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72605557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b3b6592ca04c5d6bd6a4d9bc1c1fb7b762ef72796801d5e49ffd4754ba9d0f2d`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 18:15:04 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1749513600'
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
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:dad67da3f26bce15939543965e09c4059533b025f707aad72ed3d3f3a09c66f8`  
		Last Modified: Tue, 10 Jun 2025 23:26:09 GMT  
		Size: 28.2 MB (28230129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38601bdf7bd2de89b7291c8ed439c6d45201416f865cf5cad285656a8b833042`  
		Last Modified: Wed, 11 Jun 2025 00:04:28 GMT  
		Size: 3.5 MB (3500610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2821a1ef984ad8b6b00b854378bde355879f7edb06da49e2ba83a00ce0649c52`  
		Last Modified: Wed, 11 Jun 2025 00:09:05 GMT  
		Size: 34.5 MB (34510696 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:422d498ca4849537b2b3fcfaf53a9d515f592c22b3d6f60dba9dd3a89866f469`  
		Last Modified: Wed, 11 Jun 2025 12:16:51 GMT  
		Size: 6.4 MB (6364122 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:ae01cfdaaf1f8bfe5d00566823ca293638bb0c1fa7f2a4c1359c43e0028c820a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2524123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:94b464d8e3d00de9c2d8c336886e77576258480bc55d963430021855c0426c5f`

```dockerfile
```

-	Layers:
	-	`sha256:9b229edc501e35a6fa9b1f5c0663f5fea7e2a4d421dd34c8f34786c6af49afa8`  
		Last Modified: Wed, 11 Jun 2025 02:17:50 GMT  
		Size: 2.5 MB (2512860 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d641cae8f71943e398607fa2bb6c0c98ed6a34086c05d509f5267bb951c4ff2`  
		Last Modified: Wed, 11 Jun 2025 02:17:51 GMT  
		Size: 11.3 KB (11263 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.10-bookworm` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:79d274481f986bb285d1831d276828a405b7f7ebee34d10ba9b3a240ded4d01e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70543926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8de158402b51320a38c415fe5c844a8cfe95268925a2183eb230d8d4a8bfcd70`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 18:15:04 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1749513600'
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
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:34ef2a75627f6089e01995bfd3b3786509bbdc7cfb4dbc804b642e195340dbc9`  
		Last Modified: Tue, 10 Jun 2025 22:48:42 GMT  
		Size: 28.1 MB (28077675 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c31cfba902c4f6d2a5fad746d73f53324951d835a806e9483ec49148962a55a3`  
		Last Modified: Wed, 11 Jun 2025 05:13:40 GMT  
		Size: 3.3 MB (3324416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce2c7a16a93cc04b4bf858e7856d84733a8c7aa76aa721b68c06fbfdab0dfe45`  
		Last Modified: Wed, 11 Jun 2025 07:59:40 GMT  
		Size: 32.8 MB (32777534 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a9804b8a1967f9d2bb07691c7f2a7f8c44229624ae4bed7304a593ae20f246ba`  
		Last Modified: Wed, 11 Jun 2025 13:21:55 GMT  
		Size: 6.4 MB (6364301 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:b0612c3b22c99fc8417ab866cda242d292a2183d2c766be48d02574de9d53aaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2524774 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34ad4e792e90827be6544b27ab741c4ebdfe08899c8cc230c8424454b5a8e4c4`

```dockerfile
```

-	Layers:
	-	`sha256:51d0b365f6eb528d4347ccef3115fd9da314a9c561cf3e6dbe55f52f895e07e2`  
		Last Modified: Wed, 11 Jun 2025 14:17:40 GMT  
		Size: 2.5 MB (2513263 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2f7e30664df5e671691e0c035195f7e716c2c0ee913d77f3ac0e5833e8ba7827`  
		Last Modified: Wed, 11 Jun 2025 14:17:41 GMT  
		Size: 11.5 KB (11511 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.10-bookworm` - linux; 386

```console
$ docker pull hylang@sha256:7c9f3c6f258acfc87125979e6ed3db47aefc21cd4fe601b06eb5da83c2e834c9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70049257 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1d9add37cf743e1c70b78d3bef43b17241eada96b4dcb2d80bd9715ea7bb27cd`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 18:15:04 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1749513600'
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
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HY_VERSION=1.1.0
# Wed, 04 Jun 2025 21:00:47 GMT
ENV HYRULE_VERSION=1.0.0
# Wed, 04 Jun 2025 21:00:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 04 Jun 2025 21:00:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c3d46fed134488b3ee18c12cb308c8d5520b8c647122c392f9fb76e3e1e2fc61`  
		Last Modified: Tue, 10 Jun 2025 22:47:25 GMT  
		Size: 29.2 MB (29212433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a38fc281b74a5f12a97a0abbf6bca55399d7d4078695d0328072eb2fe87f5103`  
		Last Modified: Tue, 10 Jun 2025 23:51:22 GMT  
		Size: 3.5 MB (3506098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b42df67dcea3117bb1dd1e4daccce95ce5cdc3e60c929668ac5d7c01704b1e14`  
		Last Modified: Wed, 11 Jun 2025 00:06:48 GMT  
		Size: 31.0 MB (30966520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85a551d4d0879af9ab932c1576379541d6fb9e0ab5b96b9d655cddab92ff4fd6`  
		Last Modified: Wed, 11 Jun 2025 12:17:47 GMT  
		Size: 6.4 MB (6364206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.10-bookworm` - unknown; unknown

```console
$ docker pull hylang@sha256:1fed36c81bf2bf14051442235807a0258c9aa3d50fd88bcd796b78bca89e8dd6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2521148 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b66a5e7ea2f0517a615f717f9034d28e302bdf3a614ccd1cdcf4de4a45f22f3`

```dockerfile
```

-	Layers:
	-	`sha256:ba62ce785c34881dc0a51adcacbbd86ae5aa01630406c2a404cc13621c748efa`  
		Last Modified: Wed, 11 Jun 2025 02:17:59 GMT  
		Size: 2.5 MB (2509979 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:58b708f8592b8e33f84d674c427d8d83c2317770fb3e1a39635cd40a59e3ee53`  
		Last Modified: Wed, 11 Jun 2025 02:17:59 GMT  
		Size: 11.2 KB (11169 bytes)  
		MIME: application/vnd.in-toto+json
