## `hylang:pypy3.11-trixie`

```console
$ docker pull hylang@sha256:ac25f8f3783e3fc9e0368bd98ae103e5c82a779498077aa084e8e0442581296a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:pypy3.11-trixie` - linux; amd64

```console
$ docker pull hylang@sha256:d0e5eaccd221a8dda11e5f538753b86c61a7a813908ccb41528f6342e3302345
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76522638 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8fe4f201e0ed6b4a2c15e962b42e725f4ce3a8cf7a4edfb46d0624a9cac9c7e5`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:37:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:38:30 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:38:30 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:38:30 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 24 Feb 2026 19:38:30 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 24 Feb 2026 19:38:30 GMT
CMD ["pypy3"]
# Tue, 24 Feb 2026 20:21:08 GMT
ENV HY_VERSION=1.2.0
# Tue, 24 Feb 2026 20:21:08 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 24 Feb 2026 20:21:08 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 24 Feb 2026 20:21:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a10e5423c47020112a972cdf87432de3bf0346adfb9cd58690bcc28d40ff7372`  
		Last Modified: Tue, 24 Feb 2026 19:38:41 GMT  
		Size: 1.2 MB (1220074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dae3ebb209d86269027b3b6376c5890e4e3833a426bd10e5b615a181ab35ab91`  
		Last Modified: Tue, 24 Feb 2026 19:38:42 GMT  
		Size: 37.8 MB (37839322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:356b25e9686b202d37f708a18d4fecbcc685b0859d7fde9b571711cc7ea2ebdf`  
		Last Modified: Tue, 24 Feb 2026 20:21:15 GMT  
		Size: 7.7 MB (7684610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.11-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:359e67a4761d16f32be6ee934295a14a513323df5e43960df309ec9b44c87221
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2250192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6db635ec5c4644bb083356261d98bfbf0810e9fd580f1b0bc5ccdd8b517c92ea`

```dockerfile
```

-	Layers:
	-	`sha256:a2ff0ebcff904d339e9bbde72d676b785da42e36754c94c3aa48ae35d8b00ea6`  
		Last Modified: Tue, 24 Feb 2026 20:21:15 GMT  
		Size: 2.2 MB (2238904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f8eb42e6549de75fceb17109fa14e23e6a1b6181be525c20607364218d43ba23`  
		Last Modified: Tue, 24 Feb 2026 20:21:15 GMT  
		Size: 11.3 KB (11288 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.11-trixie` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:6619b936b14e4638be3a962f2678c55fc3da212eaf58191d6945c14e50ede509
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75183336 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af0f1c32193bdf4cd6dc8569ef4672479c380fbae9f6c0717b38ad327bd815f3`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:43:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:43:50 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:43:50 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:43:50 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 24 Feb 2026 19:43:50 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 24 Feb 2026 19:43:50 GMT
CMD ["pypy3"]
# Tue, 24 Feb 2026 20:32:26 GMT
ENV HY_VERSION=1.2.0
# Tue, 24 Feb 2026 20:32:26 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 24 Feb 2026 20:32:26 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 24 Feb 2026 20:32:26 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:239e2ca73ecc49b311d3ea8c54d978d87d2cab5fa108e851698520eedeb464dd`  
		Last Modified: Tue, 24 Feb 2026 19:44:01 GMT  
		Size: 1.2 MB (1201866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2265dfe41daf5828f2e66a6ea931a0078a554c9175901fc1a7c1eeb6b91aeba7`  
		Last Modified: Tue, 24 Feb 2026 19:44:02 GMT  
		Size: 36.2 MB (36156714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:727ffc78175883fcb179eeb9f5ffce555c53f82b21b5d3ec96260122f781980b`  
		Last Modified: Tue, 24 Feb 2026 20:32:34 GMT  
		Size: 7.7 MB (7684658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.11-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:2af809f359e138a9fb26cf0bec50accf8e382d8c423882e1ff41f60e68897a19
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2250853 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a47c77961a72b3e47b38bf01442f3808d5b0b45f93a564064e8db565fd1da3f`

```dockerfile
```

-	Layers:
	-	`sha256:145c964f0e166e118939aba3bfa064fcf90ada84f2abfa5feabcddb51fbf88fa`  
		Last Modified: Tue, 24 Feb 2026 20:32:34 GMT  
		Size: 2.2 MB (2239315 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0a4585b254f64f5aebfd5be99319fcc5e8ea7416b834fe262e683ee63d2bdf85`  
		Last Modified: Tue, 24 Feb 2026 20:32:34 GMT  
		Size: 11.5 KB (11538 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy3.11-trixie` - linux; 386

```console
$ docker pull hylang@sha256:6df6cf73fd4aed86917a26d753975df2743182a60d4d77d8a0fd62e2ea22714d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74443485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b75ab09dcb0057c5820f7e33ed35e0a29aea4267550ec6d149b803b57a4525df`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Tue, 24 Feb 2026 19:34:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:34:54 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:34:54 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:34:54 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 24 Feb 2026 19:34:54 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux64.tar.bz2'; 			sha256='1410db3a7ae47603e2b7cbfd7ff6390b891b2e041c9eb4f1599f333677bccb3e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-aarch64.tar.bz2'; 			sha256='9347fe691a07fd9df17a1b186554fb9d9e6210178ffef19520a579ce1f9eb741'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.20-linux32.tar.bz2'; 			sha256='d08ce15dd61e9ace5e010b047104f0137110a258184e448ea8239472f10cf99b'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 24 Feb 2026 19:34:54 GMT
CMD ["pypy3"]
# Tue, 24 Feb 2026 20:11:33 GMT
ENV HY_VERSION=1.2.0
# Tue, 24 Feb 2026 20:11:33 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 24 Feb 2026 20:11:33 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 24 Feb 2026 20:11:33 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:964970c3fd660c784760581a283890b9d6a560fce18e32fae98ffb67d2520cde`  
		Last Modified: Tue, 24 Feb 2026 19:35:03 GMT  
		Size: 1.2 MB (1227848 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:271c1580c4a5b4586448127a7b35043b6664017e4b197c35c41155930158e83f`  
		Last Modified: Tue, 24 Feb 2026 19:35:04 GMT  
		Size: 34.2 MB (34237459 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f7906c1ab791b97171bd433a44c77e34ca53973831a4f6501eb64fdfa5289b`  
		Last Modified: Tue, 24 Feb 2026 20:11:40 GMT  
		Size: 7.7 MB (7684260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy3.11-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:fe59fbb80645422c4cf98eafcef6f929fdc05bcf03228d00fcac4d6bc7dfcd86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2247221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:95b6a56ccce18ab4fff72298e4c4198b90b5610f85408ad2dc6fbccc0ba36c3f`

```dockerfile
```

-	Layers:
	-	`sha256:4aed35eaf77c355438cb04bb63fe9c066bcce655b4eff98776277f445a37089c`  
		Last Modified: Tue, 24 Feb 2026 20:11:39 GMT  
		Size: 2.2 MB (2236023 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a0ac6cbac1fd504c8fa6e9d0df329b5454f8a8ae07515906847e127843104460`  
		Last Modified: Tue, 24 Feb 2026 20:11:39 GMT  
		Size: 11.2 KB (11198 bytes)  
		MIME: application/vnd.in-toto+json
