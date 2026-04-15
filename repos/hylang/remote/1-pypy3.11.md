## `hylang:1-pypy3.11`

```console
$ docker pull hylang@sha256:976f4651b3ae173b9e7c042c47761477341b2a8deb283c2a2659dfc5cb79ab5c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `hylang:1-pypy3.11` - linux; amd64

```console
$ docker pull hylang@sha256:b7bb3d75b0714c041a1126b25ee0347e8c0b13473781629779075c1223b6e84f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75249541 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8646e83dcbbd4152d7ff6919ab49f9a967380bb579d407caf4e7205c1e4f5c65`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:13:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:14:34 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:14:34 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:14:34 GMT
ENV PYPY_VERSION=7.3.21
# Tue, 07 Apr 2026 02:14:34 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux64.tar.bz2'; 			sha256='43f27af8ee6673932493f2696ab407321cbf79dbed94c03d8b39e603f8f5f765'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-aarch64.tar.bz2'; 			sha256='6141f5c64dd96faf87e0a3f7f362521eadd26d5e3f851f90fc386a72208f8c18'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux32.tar.bz2'; 			sha256='0c449ff3f20589e331f163807a0200a9bf5dd375c95f513a0f60bf7524795f02'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 07 Apr 2026 02:14:34 GMT
CMD ["pypy3"]
# Tue, 07 Apr 2026 03:19:21 GMT
ENV HY_VERSION=1.2.0
# Tue, 07 Apr 2026 03:19:21 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 07 Apr 2026 03:19:21 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 07 Apr 2026 03:19:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:5435b2dcdf5cb7faa0d5b1d4d54be2c72a776fab9a605336f5067d6e9ecb5976`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 29.8 MB (29775640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e0d41af932a528d67595b27b0db777148b5ddc8a2413700c37ca53e99147475`  
		Last Modified: Tue, 07 Apr 2026 02:14:45 GMT  
		Size: 1.2 MB (1220868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f139c80505b3882d94649625645b87b98e677dc832b55876ed741ae297f72ba2`  
		Last Modified: Tue, 07 Apr 2026 02:14:46 GMT  
		Size: 37.1 MB (37072383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b87433be39ea54734355a4ae2b799f68f98e5489ad94dc0dd94f02c06afde936`  
		Last Modified: Tue, 07 Apr 2026 03:19:28 GMT  
		Size: 7.2 MB (7180650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:c92c763a671d734b53500693fa15938433998e5eee90cddd2f98e64d8beaee92
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4fb475c006ff6201cf6fccd4cc56795178e928b60aa1f39e48342a797f9b8bb6`

```dockerfile
```

-	Layers:
	-	`sha256:a208da252de2271b3ddcb336bc36e77413cc53285a3123ea3e77104b9b2e110d`  
		Last Modified: Tue, 07 Apr 2026 03:19:28 GMT  
		Size: 2.3 MB (2297637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1a54daaeac29c95259797bc8eab61f4b0860c9ae3e91568b947e53d5230fb34e`  
		Last Modified: Tue, 07 Apr 2026 03:19:28 GMT  
		Size: 11.3 KB (11290 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.11` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:30abff9ac87158f13e8b590273facf09c0e0c4e8839d9266ac8690a2d93e3987
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.8 MB (73827847 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c4a868573937b7bfb2930bdc3058181b6743c94c1f66a3a016c4a3cc5d5231`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 02:16:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 02:18:03 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 02:18:03 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 02:18:03 GMT
ENV PYPY_VERSION=7.3.21
# Tue, 07 Apr 2026 02:18:03 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux64.tar.bz2'; 			sha256='43f27af8ee6673932493f2696ab407321cbf79dbed94c03d8b39e603f8f5f765'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-aarch64.tar.bz2'; 			sha256='6141f5c64dd96faf87e0a3f7f362521eadd26d5e3f851f90fc386a72208f8c18'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux32.tar.bz2'; 			sha256='0c449ff3f20589e331f163807a0200a9bf5dd375c95f513a0f60bf7524795f02'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 07 Apr 2026 02:18:03 GMT
CMD ["pypy3"]
# Tue, 07 Apr 2026 03:44:04 GMT
ENV HY_VERSION=1.2.0
# Tue, 07 Apr 2026 03:44:04 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 07 Apr 2026 03:44:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 07 Apr 2026 03:44:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:53196b1f47bdd6997874156c61491c9a36e115d9b7bd5d74e0cb5c2fc4ee69ce`  
		Last Modified: Tue, 07 Apr 2026 00:11:28 GMT  
		Size: 30.1 MB (30138551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a593926a442e1c54e2f8802386826fd7523166d57eb280e990c8d073bca1254b`  
		Last Modified: Tue, 07 Apr 2026 02:18:15 GMT  
		Size: 1.2 MB (1202278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a20a8e97b39f6de0f377601f133bed8ee51ef07105a88b9048194cb22835579`  
		Last Modified: Tue, 07 Apr 2026 02:18:16 GMT  
		Size: 35.3 MB (35306384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:205414c02f155a42ebccdc04e136b3ebdb223af0230a87dc73c6a7fb289f6ed3`  
		Last Modified: Tue, 07 Apr 2026 03:44:13 GMT  
		Size: 7.2 MB (7180634 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:e9024e8f5b6627c4a6cc4be96c5df65a44d6aeda6c156e05b863804f1b0b5a89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40d0dab14163bb13252a11a3eb076348e54414a8489e59a90a2f160b018192f5`

```dockerfile
```

-	Layers:
	-	`sha256:b6315b5350c66a826b2892497bf20917f3cddf30b51b5d1b4e5cda13024d6a26`  
		Last Modified: Tue, 07 Apr 2026 03:44:13 GMT  
		Size: 2.3 MB (2298051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6a188f5440018d12064913ade57bb764683fdc5e2e732d342c293b312be2e344`  
		Last Modified: Tue, 07 Apr 2026 03:44:13 GMT  
		Size: 11.5 KB (11538 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.11` - linux; 386

```console
$ docker pull hylang@sha256:c8a0e5a8ff4c562a26d9ab8640a3c94798190215af4b934e7ad05ee4e0c798fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.1 MB (73099009 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:650001642532a287d68dca08e16b924a9076ed40125334d3ca395e5a24bdcca5`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:55:56 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 07 Apr 2026 01:56:42 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 01:56:42 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:56:42 GMT
ENV PYPY_VERSION=7.3.21
# Tue, 07 Apr 2026 01:56:42 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux64.tar.bz2'; 			sha256='43f27af8ee6673932493f2696ab407321cbf79dbed94c03d8b39e603f8f5f765'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-aarch64.tar.bz2'; 			sha256='6141f5c64dd96faf87e0a3f7f362521eadd26d5e3f851f90fc386a72208f8c18'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux32.tar.bz2'; 			sha256='0c449ff3f20589e331f163807a0200a9bf5dd375c95f513a0f60bf7524795f02'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 07 Apr 2026 01:56:42 GMT
CMD ["pypy3"]
# Tue, 07 Apr 2026 02:57:03 GMT
ENV HY_VERSION=1.2.0
# Tue, 07 Apr 2026 02:57:03 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 07 Apr 2026 02:57:03 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 07 Apr 2026 02:57:03 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:773848e4898ff86ca7af2caf3e12237e99606245159d1ce08b797666e18584d8`  
		Last Modified: Tue, 07 Apr 2026 01:56:51 GMT  
		Size: 1.2 MB (1227986 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d44dff1ce4c19c5be7fe05a7f11f3bdd73a2e70d85e4062c7da72747dbcd4c0e`  
		Last Modified: Tue, 07 Apr 2026 01:56:52 GMT  
		Size: 33.4 MB (33399234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2fb4a463d201ddb50acf71f30019b6aa12d0f0d58755f6fbcd37b449c8b7c6ed`  
		Last Modified: Tue, 07 Apr 2026 02:57:11 GMT  
		Size: 7.2 MB (7180537 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:f693ff7e18cee9a93377e9438089d2cc501adec3aefdd55fe48e9a9f0dfaba4b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2ad62eb7757f7b072d5e2b976ae3b5e7b1b955663afd14fd4061ec82dac9b52`

```dockerfile
```

-	Layers:
	-	`sha256:44bf973a3df09f3cd549a4ea416308d1ef9701fd38db6fadd9e0140c808629a1`  
		Last Modified: Tue, 07 Apr 2026 02:57:11 GMT  
		Size: 2.3 MB (2294750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:bb3b5370583a956ded7477db140ec7b24a2328a6155ef203680e1feaffaacb91`  
		Last Modified: Tue, 07 Apr 2026 02:57:10 GMT  
		Size: 11.2 KB (11197 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.11` - windows version 10.0.26100.32690; amd64

```console
$ docker pull hylang@sha256:c3ccfa2adc106317817578db4c11994aa17185c41632a178569c93a7fcb6778d
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2184394490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13fab629cc97a3bc8704dfebb6163f3537ab1664f16305fc0d56e4c5f69bb4a0`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:02:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:14:59 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:15:10 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:15:10 GMT
ENV PYPY_VERSION=7.3.21
# Tue, 14 Apr 2026 21:15:52 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.21-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a1a2b069533b838f465157025e58933199f311f5f3f58549ccaf9872ee90fa53'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.21-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:15:52 GMT
CMD ["pypy"]
# Tue, 14 Apr 2026 22:15:18 GMT
ENV HY_VERSION=1.2.0
# Tue, 14 Apr 2026 22:15:19 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 14 Apr 2026 22:16:06 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 14 Apr 2026 22:16:07 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3642e4b8bb65ad3768f9f74a0dc48bb2e3294779b5d51573a234bfbe4f65324e`  
		Last Modified: Tue, 14 Apr 2026 18:48:19 GMT  
		Size: 606.9 MB (606926634 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8132c872e75f25bfa323300a3940e534262afa9775f557483dcc1c0951ee5277`  
		Last Modified: Tue, 14 Apr 2026 21:03:51 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29d0d8e16ef065a8b6db2cfebe362724aa5ef4c91493f0b378ff5a7cb80c75df`  
		Last Modified: Tue, 14 Apr 2026 21:15:57 GMT  
		Size: 379.4 KB (379443 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e6b03329b5b6e4dceeb205949524561824440ee96a20b658814e26ee4827a6`  
		Last Modified: Tue, 14 Apr 2026 21:16:00 GMT  
		Size: 15.6 MB (15556934 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17116294dbeca37e56513b91b2c94124558b8eb3e3f1b31386b811e068ca263e`  
		Last Modified: Tue, 14 Apr 2026 21:15:57 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6b346fe1d14888510b97436ca03d36e18682148e5e1c0492515ec011c2df3a07`  
		Last Modified: Tue, 14 Apr 2026 21:16:01 GMT  
		Size: 30.5 MB (30467456 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65f9a96dbaf1b946029079fdb110991a9badca15a702b94b72c0c8bf23be322b`  
		Last Modified: Tue, 14 Apr 2026 21:15:57 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01731a8a179d4306f2adf79b3ba2b84efb2bdbc4c9418add27a52019e79fcb8e`  
		Last Modified: Tue, 14 Apr 2026 22:16:12 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:54e111807ed629cd04554fe74d68e46a990354acd12195f386cbb76b00a6dd6b`  
		Last Modified: Tue, 14 Apr 2026 22:16:12 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7aebef13d2bc5f181585b8e31c44a372f3d77af326a79da8a1dc6fd93f86bdb8`  
		Last Modified: Tue, 14 Apr 2026 22:16:13 GMT  
		Size: 8.0 MB (7996748 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9208cc121e8af5f2b50b9de52529b1fb69b927ed9bc5080bc6a1bcba8643a0ca`  
		Last Modified: Tue, 14 Apr 2026 22:16:12 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-pypy3.11` - windows version 10.0.20348.5020; amd64

```console
$ docker pull hylang@sha256:ab5f250d9229b788573688e9a3b51df65d6c347bc471169cbf93a42e1230135c
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2124653849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:78952ca18cad2d4e660e81f8da005154acec893e8e6fcc7d759bc9fa76c8debd`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:27:54 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:28:21 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:28:41 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:28:42 GMT
ENV PYPY_VERSION=7.3.21
# Tue, 14 Apr 2026 21:29:31 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.21-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a1a2b069533b838f465157025e58933199f311f5f3f58549ccaf9872ee90fa53'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.21-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:29:31 GMT
CMD ["pypy"]
# Tue, 14 Apr 2026 22:17:47 GMT
ENV HY_VERSION=1.2.0
# Tue, 14 Apr 2026 22:17:47 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 14 Apr 2026 22:18:32 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 14 Apr 2026 22:18:32 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7111ae68f8961455d230dc12d44c2193d29b7c981e35417323613a0c1aa06384`  
		Last Modified: Tue, 14 Apr 2026 17:31:38 GMT  
		Size: 581.2 MB (581192160 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2899a26551103e6e5cc055b841bd2a50fc17a3e30be5322487e248b9039cd737`  
		Last Modified: Tue, 14 Apr 2026 21:29:37 GMT  
		Size: 1.4 KB (1378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fb001c0cfb6f5546ef74c8d384bf18a620f7c5747d3aeeb6c48f88d990d5f54`  
		Last Modified: Tue, 14 Apr 2026 21:29:36 GMT  
		Size: 488.3 KB (488312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb25cf2e8a0da3b454e83deb483c4bdb54474fa97308b7f6410b868f60b99fef`  
		Last Modified: Tue, 14 Apr 2026 21:29:41 GMT  
		Size: 15.5 MB (15530485 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:383e5f921d8ba2e19e428fa34fbd4ca98c01ca5f9a6f3ddf632caca71c2f5f90`  
		Last Modified: Tue, 14 Apr 2026 21:29:36 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e94cca21004aa7ab875574a818a9528636ce8d2f61575c40b420fa4cfd79d17`  
		Last Modified: Tue, 14 Apr 2026 21:29:40 GMT  
		Size: 30.4 MB (30448293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f46e7edbb54d87a75029458a4bda70a879a2fdb2eed33bb140bdc9d9bc14a4e9`  
		Last Modified: Tue, 14 Apr 2026 21:29:36 GMT  
		Size: 1.3 KB (1324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6931c0b0810d444ab461bcbe904eec2ec9a3d5713e900c6aae9d9c51a3d8974`  
		Last Modified: Tue, 14 Apr 2026 22:18:36 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e19b833f7fcb203b58cdfef97305aa0d7ab3f7c695b24658a4e32d4dc8d12c`  
		Last Modified: Tue, 14 Apr 2026 22:18:36 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08ad628097bded01b870d7ade2f0612c5fa3ef463ebc93de4c9c4d8b4305ed44`  
		Last Modified: Tue, 14 Apr 2026 22:18:38 GMT  
		Size: 8.0 MB (7967573 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57e98417edd8fe56f4a172b7428143622b5476eb0288b607f58708dc6f213e82`  
		Last Modified: Tue, 14 Apr 2026 22:18:36 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
