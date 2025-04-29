## `pypy:2-7-slim-bookworm`

```console
$ docker pull pypy@sha256:d010d23871dcd69a6c0d35c5c0acc84815ac378add661ef0c8ec0e66f3a379ab
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:2-7-slim-bookworm` - linux; amd64

```console
$ docker pull pypy@sha256:e531bb2266b49f8528e1cb0877ff517c6f8c4788bdd49537b603bd0a723f3f76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.2 MB (65199760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2872e4d4ffcd66000f3424024d07ca4b9b2f13da6ac04688d6af971950979f6`
-	Default Command: `["pypy"]`

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
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-linux64.tar.bz2'; 			sha256='d38445508c2eaf14ebb380d9c1ded321c5ebeae31c7e66800173d83cb8ddf423'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-aarch64.tar.bz2'; 			sha256='fe89d4fd4af13f76dfe7315975003518cf176520e3ccec1544a88d174f50910e'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-linux32.tar.bz2'; 			sha256='cc52df02b6926bd8645c1651cd7f6637ce51c2f352d0fb3c6b9330d15194b409'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 09 Apr 2025 18:15:04 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:254e724d77862dc53abbd3bf0e27f9d2f64293909cdd3d0aad6a8fe5a6680659`  
		Last Modified: Mon, 28 Apr 2025 21:08:01 GMT  
		Size: 28.2 MB (28227642 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dac60bf5ba7719405354c7b3f008b6801b127cdfa1c44e7b93d3c145497d0706`  
		Last Modified: Mon, 28 Apr 2025 22:02:07 GMT  
		Size: 3.5 MB (3499319 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f4cb5079906c60d16041190a369f8b68b44aa94fecb1e173ac4eeace4c502a`  
		Last Modified: Mon, 28 Apr 2025 22:02:08 GMT  
		Size: 33.5 MB (33472799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:3b372dabd8d91a821a320b56004b3610cd9b26dada1b9b62501b7ed654f5411b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2401336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a1a60cab92e323238a99d7a0d59342651745ce5eb08e4f42d350f918da7eb23e`

```dockerfile
```

-	Layers:
	-	`sha256:b90b521255d4e93b1aff78d8ca539574375e0cfb79607edbf52af6d02edb80c0`  
		Last Modified: Mon, 28 Apr 2025 22:02:07 GMT  
		Size: 2.4 MB (2380630 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8f17a1b6e5a64bc2915a6082633281ad2199c7b71dbea84e24892271d7bc0016`  
		Last Modified: Mon, 28 Apr 2025 22:02:06 GMT  
		Size: 20.7 KB (20706 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:9f626d19d5932bf4a56c8fcd88071288805f4a5fa4de65321700aaeef3d941d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.8 MB (62792386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75c871f9c1e3b67a1e9bc06010629677a56f039cb7027e6024ebe8502903744c`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 07 Apr 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1743984000'
# Wed, 09 Apr 2025 18:15:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 09 Apr 2025 18:15:04 GMT
ENV LANG=C.UTF-8
# Wed, 09 Apr 2025 18:15:04 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 09 Apr 2025 18:15:04 GMT
ENV PYPY_VERSION=7.3.19
# Wed, 09 Apr 2025 18:15:04 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-linux64.tar.bz2'; 			sha256='d38445508c2eaf14ebb380d9c1ded321c5ebeae31c7e66800173d83cb8ddf423'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-aarch64.tar.bz2'; 			sha256='fe89d4fd4af13f76dfe7315975003518cf176520e3ccec1544a88d174f50910e'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-linux32.tar.bz2'; 			sha256='cc52df02b6926bd8645c1651cd7f6637ce51c2f352d0fb3c6b9330d15194b409'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 09 Apr 2025 18:15:04 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:16c9c4a8e9eef856231273efbb42a473740e8d50d74d35e6aedd04ff69fe161f`  
		Last Modified: Tue, 08 Apr 2025 00:23:04 GMT  
		Size: 28.1 MB (28066320 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:06d05e4cff2a664f6a67d495184f7b4a56038cfd03b22492e76175e4bba1d997`  
		Last Modified: Wed, 09 Apr 2025 21:14:57 GMT  
		Size: 3.3 MB (3322906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2aaf5b35591acf1661c5d7a5b323ff66fb80e5183c4ba6a30053165ad8a9d10`  
		Last Modified: Wed, 09 Apr 2025 21:20:36 GMT  
		Size: 31.4 MB (31403160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:938535ee6b5f75776c5f1496b646dabcb2844a4b1f045c5f426cd240cb8ca352
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2402002 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d22f9e5ba73007f8865227e3e9e307818ba8f46eda49d960aae56dddedfad1c7`

```dockerfile
```

-	Layers:
	-	`sha256:a1508d2c500b373e01a17e6c1ec20e19195e8370915f95ce5ceb1067c99e9957`  
		Last Modified: Wed, 09 Apr 2025 21:20:35 GMT  
		Size: 2.4 MB (2381031 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:056764b91bdf9f4c2ac3ef8c0ec9771d634f960f9f483cafc87244b34ed7ea33`  
		Last Modified: Wed, 09 Apr 2025 21:20:35 GMT  
		Size: 21.0 KB (20971 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:a5f3962da58f3cef9875c1107530638a3bdfe0e8cd8acea519a14febc4699c77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **61.8 MB (61793290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4160e68e903c3df2f675254979b58f75656a989add9cb2439e7436e03aa04367`
-	Default Command: `["pypy"]`

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
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-linux64.tar.bz2'; 			sha256='d38445508c2eaf14ebb380d9c1ded321c5ebeae31c7e66800173d83cb8ddf423'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-aarch64.tar.bz2'; 			sha256='fe89d4fd4af13f76dfe7315975003518cf176520e3ccec1544a88d174f50910e'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.19-linux32.tar.bz2'; 			sha256='cc52df02b6926bd8645c1651cd7f6637ce51c2f352d0fb3c6b9330d15194b409'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libexpat1 		libncurses5 		libncursesw6 		libsqlite3-0 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 09 Apr 2025 18:15:04 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:ad2e653a01d32a9a8676730797453c924f9d10fe1414178e7a26c35132c3691e`  
		Last Modified: Mon, 28 Apr 2025 21:08:11 GMT  
		Size: 29.2 MB (29210866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2f5566717e66782c3478a6330abbbd68ca7ba27a21c27dd50a20f3dacd5dbac`  
		Last Modified: Mon, 28 Apr 2025 21:56:29 GMT  
		Size: 3.5 MB (3503471 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f766422fcad01ca98006d45a02530053c287554ba51f9f8d6c2cfe8041ed4bd6`  
		Last Modified: Mon, 28 Apr 2025 21:56:29 GMT  
		Size: 29.1 MB (29078953 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:df4660425348b6259a1fa328639280fa7d801b8236e276563080318b2ac6b289
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.4 MB (2398327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1bfb812254c7316f86af23cdd67a18215bd4988c39a0a912d09891b28d557677`

```dockerfile
```

-	Layers:
	-	`sha256:903dd1990f3f85a08cd30b441381d79fea93fb7e0bcfcf11dec9826cfbfe7c1e`  
		Last Modified: Mon, 28 Apr 2025 21:56:29 GMT  
		Size: 2.4 MB (2377713 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6af26bbaa6fad2dfcf843568abd65acfa5456b520817ffb2524a0accfe003c7`  
		Last Modified: Mon, 28 Apr 2025 21:56:29 GMT  
		Size: 20.6 KB (20614 bytes)  
		MIME: application/vnd.in-toto+json
