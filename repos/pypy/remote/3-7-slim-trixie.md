## `pypy:3-7-slim-trixie`

```console
$ docker pull pypy@sha256:9a2b873c10c9768e0f56d05244ba8e88237f3c90ffd7bc926e91ff39831d3e28
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:3-7-slim-trixie` - linux; amd64

```console
$ docker pull pypy@sha256:b85bf821973eab90d47eb4c295085fe3cc93c0fe9eaee2e19dfea07c574de893
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.1 MB (68067325 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:037f31abfa902bda2e918b348ce633e3c5115e700661e5229b41fd8b6cd25f1b`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:56:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:57:21 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:57:21 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:57:21 GMT
ENV PYPY_VERSION=7.3.21
# Mon, 16 Mar 2026 22:57:21 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux64.tar.bz2'; 			sha256='43f27af8ee6673932493f2696ab407321cbf79dbed94c03d8b39e603f8f5f765'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-aarch64.tar.bz2'; 			sha256='6141f5c64dd96faf87e0a3f7f362521eadd26d5e3f851f90fc386a72208f8c18'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux32.tar.bz2'; 			sha256='0c449ff3f20589e331f163807a0200a9bf5dd375c95f513a0f60bf7524795f02'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 16 Mar 2026 22:57:21 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f8ae8bd647a9b2a889c59c19ac04aa54e3776a48f6a0074f14679598a0466a5a`  
		Last Modified: Mon, 16 Mar 2026 22:57:32 GMT  
		Size: 1.2 MB (1220850 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79985414c3b7bee48e27ebf46d62006bde1bd6cd6708e492e7720543e50741c6`  
		Last Modified: Mon, 16 Mar 2026 22:57:33 GMT  
		Size: 37.1 MB (37070975 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-7-slim-trixie` - unknown; unknown

```console
$ docker pull pypy@sha256:55cc78eac186557378ad7c9fd73281d83ab23c0cbcbb1187361ad43634ace852
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2316294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b68748375f2b409615f41231dc66de764efc21d7752effa29c34b1fcdfb6977`

```dockerfile
```

-	Layers:
	-	`sha256:8367c9e4128fb18eb4e19b5e245b306704a94a49b4d2bf2f6ff3c7a898725236`  
		Last Modified: Mon, 16 Mar 2026 22:57:32 GMT  
		Size: 2.3 MB (2290658 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4b34c5dc98ce46201bd4cc57f84c2dc03b70aa5549baba040f96f32a62a149c`  
		Last Modified: Mon, 16 Mar 2026 22:57:31 GMT  
		Size: 25.6 KB (25636 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:3-7-slim-trixie` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:5c028733f24f4ee09f08fd219dd72171a35b96ef820bafb8634c3b7cdf5cf381
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66647015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb8caf4d50ea0b9c31cd88dafbcf462e17f71a02683dc79db846f6b9ecfe5f0b`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:59:04 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:59:55 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:59:55 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:59:55 GMT
ENV PYPY_VERSION=7.3.21
# Mon, 16 Mar 2026 22:59:55 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux64.tar.bz2'; 			sha256='43f27af8ee6673932493f2696ab407321cbf79dbed94c03d8b39e603f8f5f765'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-aarch64.tar.bz2'; 			sha256='6141f5c64dd96faf87e0a3f7f362521eadd26d5e3f851f90fc386a72208f8c18'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux32.tar.bz2'; 			sha256='0c449ff3f20589e331f163807a0200a9bf5dd375c95f513a0f60bf7524795f02'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 16 Mar 2026 22:59:55 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11017598a828aa88a309a3be183a9e8a637ec9ddb9c595dd3a1377845a095e83`  
		Last Modified: Mon, 16 Mar 2026 23:00:11 GMT  
		Size: 1.2 MB (1202313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5385ce3727f31eaca756eb36bbb8ecb7fdb092fc28da7418ad82b103ebb49202`  
		Last Modified: Mon, 16 Mar 2026 23:00:12 GMT  
		Size: 35.3 MB (35306286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-7-slim-trixie` - unknown; unknown

```console
$ docker pull pypy@sha256:6555f35942efa97c185d3ece4de9a9805f76022afd339b39c30b34f2fee7f26c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2317020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e15535cd0f80833b7aa61cb4a2907b42526c9230e138e725c68a67036144db7a`

```dockerfile
```

-	Layers:
	-	`sha256:cc593da71573d52a174cffccf9bd0150b3ca23eec804cffb7801a1aa68492a0f`  
		Last Modified: Mon, 16 Mar 2026 23:00:10 GMT  
		Size: 2.3 MB (2291096 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f50a3c4ca2104e8f5ecf00ed9847a42995004bd06047882d5fee506e51c2764c`  
		Last Modified: Mon, 16 Mar 2026 23:00:10 GMT  
		Size: 25.9 KB (25924 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:3-7-slim-trixie` - linux; 386

```console
$ docker pull pypy@sha256:1f429eca511153c434b3ded574598ae4a91513227d0615d40c3275bf08c97a0a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.9 MB (65918550 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1aaba6cece55fc98b71576d38c9d36f2a8cd2bff3eb86193c42f7d18b9fa8b1f`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:52:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:53:18 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:53:18 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:53:18 GMT
ENV PYPY_VERSION=7.3.21
# Mon, 16 Mar 2026 22:53:18 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux64.tar.bz2'; 			sha256='43f27af8ee6673932493f2696ab407321cbf79dbed94c03d8b39e603f8f5f765'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-aarch64.tar.bz2'; 			sha256='6141f5c64dd96faf87e0a3f7f362521eadd26d5e3f851f90fc386a72208f8c18'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux32.tar.bz2'; 			sha256='0c449ff3f20589e331f163807a0200a9bf5dd375c95f513a0f60bf7524795f02'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 16 Mar 2026 22:53:18 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7df88149fc1005c96c0dd4c9aa7a60802d9b17a63361855b7dd452637b04b4e`  
		Last Modified: Mon, 16 Mar 2026 22:53:28 GMT  
		Size: 1.2 MB (1227997 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:08bd421834d1674247e34fc70285e0f1c3844d770a99bff981ec451c0020220b`  
		Last Modified: Mon, 16 Mar 2026 22:53:28 GMT  
		Size: 33.4 MB (33399421 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-7-slim-trixie` - unknown; unknown

```console
$ docker pull pypy@sha256:a19e79dcfe885e13c7637b24373312c0a617fdb9e0162f6f8c44a04fdd2fdf32
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2313294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b87ee448f01c080c77e6e5d19361acaf37a4d07561d5000667c0086d48f828c`

```dockerfile
```

-	Layers:
	-	`sha256:1a621f8846661ff1b95b156efb9a45bee3d822730c4dd8dbff182a37bf2888e1`  
		Last Modified: Mon, 16 Mar 2026 22:53:28 GMT  
		Size: 2.3 MB (2287761 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d38e07e24204feed676edc850aa758df79df7615eb40e5833a07d0a0c699e25d`  
		Last Modified: Mon, 16 Mar 2026 22:53:27 GMT  
		Size: 25.5 KB (25533 bytes)  
		MIME: application/vnd.in-toto+json
