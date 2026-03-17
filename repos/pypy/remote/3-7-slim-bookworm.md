## `pypy:3-7-slim-bookworm`

```console
$ docker pull pypy@sha256:3c23ce94f2bd27daae7f398a9f5efacb57a2cf9b86c5f6b95808127650474ad4
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `pypy:3-7-slim-bookworm` - linux; amd64

```console
$ docker pull pypy@sha256:8bfadd34743cb64e77e34d2f57253706d3ad3f3363c45a3f9364542e9c405c5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.2 MB (69226375 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a3100c4825033ce1540dcabc99333188a50f910abd6fc834c7c99582f78095e`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:56:49 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:57:33 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:57:33 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:57:33 GMT
ENV PYPY_VERSION=7.3.21
# Mon, 16 Mar 2026 22:57:33 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux64.tar.bz2'; 			sha256='43f27af8ee6673932493f2696ab407321cbf79dbed94c03d8b39e603f8f5f765'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-aarch64.tar.bz2'; 			sha256='6141f5c64dd96faf87e0a3f7f362521eadd26d5e3f851f90fc386a72208f8c18'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux32.tar.bz2'; 			sha256='0c449ff3f20589e331f163807a0200a9bf5dd375c95f513a0f60bf7524795f02'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 16 Mar 2026 22:57:33 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:6db0909c4473287ed4d1f950d26b8bc5b7b4206d365a0e7740cb89e46979153e`  
		Last Modified: Mon, 16 Mar 2026 21:52:32 GMT  
		Size: 28.2 MB (28236225 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3465c3744b4dbbfc3b0c894a51271afd0a3c1aafa7bf81f70d51c4e10493912e`  
		Last Modified: Mon, 16 Mar 2026 22:57:45 GMT  
		Size: 3.5 MB (3510220 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4de0d20bc227cfee0b49febf70127e17c1503029e22bc0d730c0672a12e4087c`  
		Last Modified: Mon, 16 Mar 2026 22:57:46 GMT  
		Size: 37.5 MB (37479930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:2be2a26d3cddcf199f8a5a3c4bdf3804c49a12ddcc684d1419dedf7529b65db6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699271 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2778cc4c410ccf08e7dff4684866a2e5a7d71efbad10891eacd144835bfd6aaa`

```dockerfile
```

-	Layers:
	-	`sha256:e45ad9ee08d25b89898c000a5626d3cf31f0fe3b65e300928013feca2a34f6c1`  
		Last Modified: Mon, 16 Mar 2026 22:57:45 GMT  
		Size: 2.7 MB (2676306 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:25e18cf3059c2fd74e1c697338cb48fbd3ef637b18f7e29f6acd62cc340f38cf`  
		Last Modified: Mon, 16 Mar 2026 22:57:45 GMT  
		Size: 23.0 KB (22965 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:3-7-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:fea9a191ba3beaa5cde02d7a0a6edfa9a24b158fc33f5f54123dfcc99fc0dcd3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67168863 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:031998d568772e2bc8177693e20c889e4694481bae33b6289b11cddf6362a3d3`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:59:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:00:23 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:00:23 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 23:00:23 GMT
ENV PYPY_VERSION=7.3.21
# Mon, 16 Mar 2026 23:00:23 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux64.tar.bz2'; 			sha256='43f27af8ee6673932493f2696ab407321cbf79dbed94c03d8b39e603f8f5f765'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-aarch64.tar.bz2'; 			sha256='6141f5c64dd96faf87e0a3f7f362521eadd26d5e3f851f90fc386a72208f8c18'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux32.tar.bz2'; 			sha256='0c449ff3f20589e331f163807a0200a9bf5dd375c95f513a0f60bf7524795f02'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 16 Mar 2026 23:00:23 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:d997cc310c981ac52155d0d9fe28888b261a7746a3877bb0ca848fd1a83d319a`  
		Last Modified: Mon, 16 Mar 2026 21:53:12 GMT  
		Size: 28.1 MB (28116065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a82b80e735c483af82682d31d4496ff9efe61466c78994efd4431a8af2ac244`  
		Last Modified: Mon, 16 Mar 2026 23:00:35 GMT  
		Size: 3.3 MB (3341481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94e697ccf052b03b6377883791fcb9f2ca4c5f3265acab4e68b77449ab3167b4`  
		Last Modified: Mon, 16 Mar 2026 23:00:37 GMT  
		Size: 35.7 MB (35711317 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:d757df62b80bb84d76a5fbbb0e396a0c58a728af823812fe3a2d0a4c87dbf7d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2699781 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc479890101a0e98556822b399c5a2a0ec97c7624bc009cf0f2db64494705f4`

```dockerfile
```

-	Layers:
	-	`sha256:b7de2d36f3bce60014bdfcf42ce1bd85fa468423fcae59cc666d519df9b0e2d2`  
		Last Modified: Mon, 16 Mar 2026 23:00:37 GMT  
		Size: 2.7 MB (2676637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3d8be3a5fdd74b39d26029a0883a5e384fe5d649993c8bce086ada3cdb75c481`  
		Last Modified: Mon, 16 Mar 2026 23:00:34 GMT  
		Size: 23.1 KB (23144 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:3-7-slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:5d673b992c401955719b1c3326be1edabb0dad4df8e2bb14c2b24c2553319f89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.6 MB (66644585 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:243847c6e0e024c797678cb9d000fe5e052b34d452e3d0cd2d15fd486024be42`
-	Default Command: `["pypy3"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1773619200'
# Mon, 16 Mar 2026 22:52:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:53:16 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:53:16 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 22:53:16 GMT
ENV PYPY_VERSION=7.3.21
# Mon, 16 Mar 2026 22:53:16 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux64.tar.bz2'; 			sha256='43f27af8ee6673932493f2696ab407321cbf79dbed94c03d8b39e603f8f5f765'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-aarch64.tar.bz2'; 			sha256='6141f5c64dd96faf87e0a3f7f362521eadd26d5e3f851f90fc386a72208f8c18'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux32.tar.bz2'; 			sha256='0c449ff3f20589e331f163807a0200a9bf5dd375c95f513a0f60bf7524795f02'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 16 Mar 2026 22:53:16 GMT
CMD ["pypy3"]
```

-	Layers:
	-	`sha256:f649af5ed0883ac0b5027f768cbd9576b7bc8c76adac1eddeb4035e88b9258fe`  
		Last Modified: Mon, 16 Mar 2026 21:53:10 GMT  
		Size: 29.2 MB (29221681 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8942c664f351cd7858ca2aaf9828091c517215b37d4d1d4690c5ea4b4c81f300`  
		Last Modified: Mon, 16 Mar 2026 22:53:26 GMT  
		Size: 3.5 MB (3512896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec5fd3d8179aff5472c43d982224d7936a7e8e08ad411a833f36bd978b168396`  
		Last Modified: Mon, 16 Mar 2026 22:53:26 GMT  
		Size: 33.9 MB (33910008 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:3-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:630e10c09fc0f40db93cab4ba2a38ceebcf0e667d3fc16882400ec570fd97f82
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2696342 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6f1524e958f90dd26fef3149a94da6561ac81bf17ddd0fa8bf5245b49ca15562`

```dockerfile
```

-	Layers:
	-	`sha256:44fb8f0d0473b65fee4ef4b7a9cfdfae266fc68a456ae54a58b9a55c68732151`  
		Last Modified: Mon, 16 Mar 2026 22:53:25 GMT  
		Size: 2.7 MB (2673436 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:adc846f85c9c9d9c621990fc1acb579deec1d7f233055514e6df8e6f2e0108c2`  
		Last Modified: Mon, 16 Mar 2026 22:53:25 GMT  
		Size: 22.9 KB (22906 bytes)  
		MIME: application/vnd.in-toto+json
