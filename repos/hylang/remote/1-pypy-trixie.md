## `hylang:1-pypy-trixie`

```console
$ docker pull hylang@sha256:313922246621ba5938d130cb01df2de3e7146c48c385be05f7ad73f09bbbe1cf
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:1-pypy-trixie` - linux; amd64

```console
$ docker pull hylang@sha256:cd1eafede3492d0f8491b188d4ac18c01622b48594f287cc86a1c37762f4bfa9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76087198 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b46d7d6aba0ba18cbef00f7426745ac941e05daf7b4b8c6163c3c1e63161c223`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 01:57:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:57:52 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 01:57:52 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:57:52 GMT
ENV PYPY_VERSION=7.3.23
# Wed, 24 Jun 2026 01:57:52 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-linux64.tar.bz2'; 			sha256='16f9f56e82d1f4ec95a324c1a8cacfd78afc7f0656c0a809a18725ef4391453a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-aarch64.tar.bz2'; 			sha256='5433ac0ad526aeb35025ef8509bed65cd62ea35cb9e21ac649c69a5eff4eecb6'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-linux32.tar.bz2'; 			sha256='c7e2ffb173dcadbe4708a2e606e0b705474c1c33f25a09a4084f265d538172e4'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Jun 2026 01:57:52 GMT
CMD ["pypy3"]
# Wed, 24 Jun 2026 02:46:52 GMT
ENV HY_VERSION=1.3.0
# Wed, 24 Jun 2026 02:46:52 GMT
ENV HYRULE_VERSION=1.1.0
# Wed, 24 Jun 2026 02:46:52 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 24 Jun 2026 02:46:52 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e95a6c7ea7d49b37920899b023ecd0e32796c976c1748491f76cae53ba86d13a`  
		Last Modified: Wed, 24 Jun 2026 00:28:31 GMT  
		Size: 29.8 MB (29785419 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c6d7b67025a7f6977bb2d8fac1ad018376f62b58b5937994f7d01e8fc669bc55`  
		Last Modified: Wed, 24 Jun 2026 01:58:04 GMT  
		Size: 1.2 MB (1220958 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2dbc11bdb1c9815d5f80993fbbaaf827d02d577aab8a929f2697b4482923407f`  
		Last Modified: Wed, 24 Jun 2026 01:58:05 GMT  
		Size: 37.8 MB (37754799 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0132c9665a492553f10409bc8db75aedb664636f6b36b32b53b397fe092ba645`  
		Last Modified: Wed, 24 Jun 2026 02:46:59 GMT  
		Size: 7.3 MB (7326022 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:74be19c774d8c3da5fd9c2d0c73010c99d1039338f2a2888cc38daba9d3cf217
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c93e8a1145ac9c1dc763cb7f441ba545df83bf56f98a40b4fff61a51acb99ad`

```dockerfile
```

-	Layers:
	-	`sha256:b6020472b6c3481c6080ade1dc00906dc2126fe1cbeb97933e03a12bfe37e197`  
		Last Modified: Wed, 24 Jun 2026 02:47:00 GMT  
		Size: 2.3 MB (2297679 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5f8894f29a61d7c7e229df2fc6e1c2a024e9cbcbb469e6ffc504a70c36b558b8`  
		Last Modified: Wed, 24 Jun 2026 02:46:59 GMT  
		Size: 11.3 KB (11290 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy-trixie` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:58523e5d8c33b00d76c457f6ff4be4f3c7bb09b4c194a606140d808af729a904
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74616001 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23ccda2b054564d693223daaf5582ce13e17c489d41ad49354c273e408fcf448`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1782172800'
# Wed, 24 Jun 2026 02:00:50 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:01:38 GMT
ENV LANG=C.UTF-8
# Wed, 24 Jun 2026 02:01:38 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:01:38 GMT
ENV PYPY_VERSION=7.3.23
# Wed, 24 Jun 2026 02:01:38 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-linux64.tar.bz2'; 			sha256='16f9f56e82d1f4ec95a324c1a8cacfd78afc7f0656c0a809a18725ef4391453a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-aarch64.tar.bz2'; 			sha256='5433ac0ad526aeb35025ef8509bed65cd62ea35cb9e21ac649c69a5eff4eecb6'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-linux32.tar.bz2'; 			sha256='c7e2ffb173dcadbe4708a2e606e0b705474c1c33f25a09a4084f265d538172e4'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 24 Jun 2026 02:01:38 GMT
CMD ["pypy3"]
# Wed, 24 Jun 2026 02:53:32 GMT
ENV HY_VERSION=1.3.0
# Wed, 24 Jun 2026 02:53:32 GMT
ENV HYRULE_VERSION=1.1.0
# Wed, 24 Jun 2026 02:53:32 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 24 Jun 2026 02:53:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3be819c1c8cfde074541a1d875fbf2da3642b0ec6bb39aaa2ce7d56052b67dc1`  
		Last Modified: Wed, 24 Jun 2026 00:28:21 GMT  
		Size: 30.1 MB (30148551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9592f006a65bec14402f92f058e370b0380fd9eb8e0b4527a79529bc151055b4`  
		Last Modified: Wed, 24 Jun 2026 02:01:49 GMT  
		Size: 1.2 MB (1202502 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8280f3b6d46104bccfe6cd76e0d0cd726e83dddeda365dcd7b36fa7129f3a280`  
		Last Modified: Wed, 24 Jun 2026 02:01:50 GMT  
		Size: 35.9 MB (35938784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:590687536f751c9e4faf92707bda285d8eed88dfd97908b726f426f161ed9dab`  
		Last Modified: Wed, 24 Jun 2026 02:53:40 GMT  
		Size: 7.3 MB (7326164 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:74f4dcbf60b76c71821e7d272d37971abfbef33b83cd18d91e6baa6c0ea77671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309621 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07aa8a50df37331d1034394ef6c3fe8162bcc1d5051c0d1441604aa333885c7e`

```dockerfile
```

-	Layers:
	-	`sha256:00749f6ecb36f3f56360fe593410bfea05d0e2360c8daf5472f887c436ceb203`  
		Last Modified: Wed, 24 Jun 2026 02:53:40 GMT  
		Size: 2.3 MB (2298085 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77fcf7c9ba048070283a474572af80a85412f59ee8afaab8d60411c999414619`  
		Last Modified: Wed, 24 Jun 2026 02:53:40 GMT  
		Size: 11.5 KB (11536 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy-trixie` - linux; 386

```console
$ docker pull hylang@sha256:18b81803b7429e79c9e91b49d879f9aa5a7286ded15d49f639b5c230c9651d2d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73637865 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f83b68255e6f19f254fd111f35df6c2c54d45021a35fc38340ae4c588543af4a`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 10 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1781049600'
# Thu, 11 Jun 2026 01:16:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Thu, 11 Jun 2026 01:17:09 GMT
ENV LANG=C.UTF-8
# Thu, 11 Jun 2026 01:17:09 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 11 Jun 2026 01:17:09 GMT
ENV PYPY_VERSION=7.3.23
# Thu, 11 Jun 2026 01:17:09 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-linux64.tar.bz2'; 			sha256='16f9f56e82d1f4ec95a324c1a8cacfd78afc7f0656c0a809a18725ef4391453a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-aarch64.tar.bz2'; 			sha256='5433ac0ad526aeb35025ef8509bed65cd62ea35cb9e21ac649c69a5eff4eecb6'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.23-linux32.tar.bz2'; 			sha256='c7e2ffb173dcadbe4708a2e606e0b705474c1c33f25a09a4084f265d538172e4'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Thu, 11 Jun 2026 01:17:09 GMT
CMD ["pypy3"]
# Thu, 11 Jun 2026 02:40:07 GMT
ENV HY_VERSION=1.3.0
# Thu, 11 Jun 2026 02:40:07 GMT
ENV HYRULE_VERSION=1.1.0
# Thu, 11 Jun 2026 02:40:07 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Thu, 11 Jun 2026 02:40:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:720f951a68f4f9ab464e52b53cf88cfb86bc876b3f00956d000420777ab93c0c`  
		Last Modified: Wed, 10 Jun 2026 23:40:30 GMT  
		Size: 31.3 MB (31301194 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c3fb100aef164519635acb0b17d78a85ec237d4b4c3323a0cf80dba31d3fd88b`  
		Last Modified: Thu, 11 Jun 2026 01:17:19 GMT  
		Size: 1.2 MB (1228250 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5bb8fe3add0cff6fd74d5f16a99acc3c9c08110e1bb8ed52bc78e6b5b2f7f9c3`  
		Last Modified: Thu, 11 Jun 2026 01:17:20 GMT  
		Size: 33.8 MB (33782458 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3eae47de3ca48db1e1e4c4f151b3a559b879436ad4ac2ed8937b0552881b0d46`  
		Last Modified: Thu, 11 Jun 2026 02:40:15 GMT  
		Size: 7.3 MB (7325963 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy-trixie` - unknown; unknown

```console
$ docker pull hylang@sha256:b17cdedebe61b21daf61b4b8b871fd3a784de892b6d368bfea2e33611fd56854
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305990 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:477314be58c39d3fb22697ddc2c42bd9b5506b937b7f5d61e1809608a55f752f`

```dockerfile
```

-	Layers:
	-	`sha256:b5d58043c953e017837b26c5b49013332c8e1aa486646d7dd38ca3bbc3599489`  
		Last Modified: Thu, 11 Jun 2026 02:40:15 GMT  
		Size: 2.3 MB (2294792 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b56200207539c332a5a1ad168a74e7401858e7c5103cbb1839c25791f2afb58c`  
		Last Modified: Thu, 11 Jun 2026 02:40:15 GMT  
		Size: 11.2 KB (11198 bytes)  
		MIME: application/vnd.in-toto+json
