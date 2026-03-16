## `hylang:pypy`

```console
$ docker pull hylang@sha256:aa2e3e3acff6e5ea30b3330ed9017faf662389c8113c130cb66d80e5adea8462
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 8
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	windows version 10.0.26100.32522; amd64
	-	windows version 10.0.20348.4893; amd64

### `hylang:pypy` - linux; amd64

```console
$ docker pull hylang@sha256:df6ec11db150c40552b17445fc3fb4e0825d9da6d8053a99d4e850960a01d13a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.6 MB (85556895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:931a91bfd037c9ab3f6837550f1de4401ee37632f12bb1317496d2dd4218aa77`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1771804800'
# Mon, 16 Mar 2026 18:59:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 19:00:26 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 19:00:26 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 19:00:26 GMT
ENV PYPY_VERSION=7.3.21
# Mon, 16 Mar 2026 19:00:26 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux64.tar.bz2'; 			sha256='43f27af8ee6673932493f2696ab407321cbf79dbed94c03d8b39e603f8f5f765'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-aarch64.tar.bz2'; 			sha256='6141f5c64dd96faf87e0a3f7f362521eadd26d5e3f851f90fc386a72208f8c18'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux32.tar.bz2'; 			sha256='0c449ff3f20589e331f163807a0200a9bf5dd375c95f513a0f60bf7524795f02'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 16 Mar 2026 19:00:26 GMT
CMD ["pypy3"]
# Mon, 16 Mar 2026 19:10:03 GMT
ENV HY_VERSION=1.2.0
# Mon, 16 Mar 2026 19:10:03 GMT
ENV HYRULE_VERSION=1.0.1
# Mon, 16 Mar 2026 19:10:03 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 16 Mar 2026 19:10:03 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:206356c42440674ecbdf1070cf70ce8ef7885ac2e5c56f1ecf800b758f6b0419`  
		Last Modified: Tue, 24 Feb 2026 18:43:25 GMT  
		Size: 29.8 MB (29778632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e4f3a78dd030d8f118bb2e0534fb2f15901011af745a581702e711a19d3e852d`  
		Last Modified: Mon, 16 Mar 2026 19:00:40 GMT  
		Size: 4.2 MB (4182080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16c51c7287921420db10559ac4a83c52b3cb78756df7be04455436c3be6d89f1`  
		Last Modified: Mon, 16 Mar 2026 19:00:41 GMT  
		Size: 44.4 MB (44415493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:37c90a0331cbb01529f045c7239cddb77dc37f45fc2f678dd5c1c3d1bc231f9a`  
		Last Modified: Mon, 16 Mar 2026 19:10:11 GMT  
		Size: 7.2 MB (7180690 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy` - unknown; unknown

```console
$ docker pull hylang@sha256:e71c1f8d24b42d34c6b0d85f5865ee7046dbd204302222b976a1768430035031
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308891 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb5d06a65a0e0a50064838d371c69d78d0391cf42626a5882c651c46ec9b42a9`

```dockerfile
```

-	Layers:
	-	`sha256:ae7d8fcf42f4c148165c66d22fbce0d3cce6141d39d7a61f372609e0e7982663`  
		Last Modified: Mon, 16 Mar 2026 19:10:11 GMT  
		Size: 2.3 MB (2297601 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ab152e6b06ef55c36ac80b8392d52fbe5c047ecce13fbf44c8669f02936e34da`  
		Last Modified: Mon, 16 Mar 2026 19:10:11 GMT  
		Size: 11.3 KB (11290 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:93c1c55581ac9a171a087278db6b0858d69db5af598d0ce25bff6afde853d31b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **84.5 MB (84533727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f8c2b8cd37da79a75092b2976a67f6b930066f86c1ec9b3e78022dbec5daa882`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1771804800'
# Mon, 16 Mar 2026 18:59:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 19:00:15 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 19:00:15 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 19:00:15 GMT
ENV PYPY_VERSION=7.3.21
# Mon, 16 Mar 2026 19:00:15 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux64.tar.bz2'; 			sha256='43f27af8ee6673932493f2696ab407321cbf79dbed94c03d8b39e603f8f5f765'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-aarch64.tar.bz2'; 			sha256='6141f5c64dd96faf87e0a3f7f362521eadd26d5e3f851f90fc386a72208f8c18'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux32.tar.bz2'; 			sha256='0c449ff3f20589e331f163807a0200a9bf5dd375c95f513a0f60bf7524795f02'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 16 Mar 2026 19:00:15 GMT
CMD ["pypy3"]
# Mon, 16 Mar 2026 19:10:35 GMT
ENV HY_VERSION=1.2.0
# Mon, 16 Mar 2026 19:10:35 GMT
ENV HYRULE_VERSION=1.0.1
# Mon, 16 Mar 2026 19:10:35 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 16 Mar 2026 19:10:35 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3b66ab8c894cad95899b704e688938517870850391d1349c862c2b09214acb86`  
		Last Modified: Tue, 24 Feb 2026 18:42:52 GMT  
		Size: 30.1 MB (30140098 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9ce99683da05098ea89eb1d480fdab656a50604376726b5667ba9dbfd530541`  
		Last Modified: Mon, 16 Mar 2026 19:00:27 GMT  
		Size: 4.5 MB (4524989 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d4e3743be52a13966e5635171bdd7cfd8d6303d7424f3e4fb41ce3ffb1b0ac7`  
		Last Modified: Mon, 16 Mar 2026 19:00:28 GMT  
		Size: 42.7 MB (42688109 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c901c07ef24f9549185d8d7b648c6823bccf9bf24889a1fed5ede812823f8c6e`  
		Last Modified: Mon, 16 Mar 2026 19:10:43 GMT  
		Size: 7.2 MB (7180531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy` - unknown; unknown

```console
$ docker pull hylang@sha256:6890f9cf56e758e8e0796a1397b6e4dcc80f04ec89ba9ba9f87284bc9f32816b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309553 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c05d9f24e5247d18a5e279f8060261dfd90ae51659a3de78b748a152d0eb54f1`

```dockerfile
```

-	Layers:
	-	`sha256:dac792d5d23f3097de5e6f3632911d804e0eca9459e361c3bcfe0444cd7f1175`  
		Last Modified: Mon, 16 Mar 2026 19:10:43 GMT  
		Size: 2.3 MB (2298015 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c3e2b58f5bbbae4945f1e6c3f052a90ff7647361d8bb0ef71200c5a975af27c5`  
		Last Modified: Mon, 16 Mar 2026 19:10:42 GMT  
		Size: 11.5 KB (11538 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy` - linux; 386

```console
$ docker pull hylang@sha256:dfe1e8f1e29447b131104ea9d3d300e9e9db79bd945417730574a35190b4f531
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **83.1 MB (83093037 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:438238c7f10001c1a2090fb4b95884f8769bd8c8f353a794fc7cc3ba3febad3a`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1771804800'
# Mon, 16 Mar 2026 18:59:37 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 19:00:31 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 19:00:31 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 16 Mar 2026 19:00:31 GMT
ENV PYPY_VERSION=7.3.21
# Mon, 16 Mar 2026 19:00:31 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux64.tar.bz2'; 			sha256='43f27af8ee6673932493f2696ab407321cbf79dbed94c03d8b39e603f8f5f765'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-aarch64.tar.bz2'; 			sha256='6141f5c64dd96faf87e0a3f7f362521eadd26d5e3f851f90fc386a72208f8c18'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.21-linux32.tar.bz2'; 			sha256='0c449ff3f20589e331f163807a0200a9bf5dd375c95f513a0f60bf7524795f02'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Mon, 16 Mar 2026 19:00:31 GMT
CMD ["pypy3"]
# Mon, 16 Mar 2026 19:10:48 GMT
ENV HY_VERSION=1.2.0
# Mon, 16 Mar 2026 19:10:48 GMT
ENV HYRULE_VERSION=1.0.1
# Mon, 16 Mar 2026 19:10:48 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 16 Mar 2026 19:10:48 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:f4e0b944ee1e7e50bdfbfa77bda370b6eccee7d698a7adca78c38f5ca0767ca5`  
		Last Modified: Tue, 24 Feb 2026 18:43:18 GMT  
		Size: 31.3 MB (31293918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:be987a46462a9668b0cbdcabfc5c919236353810e4c793ffa12f50bb10cd90b4`  
		Last Modified: Mon, 16 Mar 2026 19:00:43 GMT  
		Size: 4.1 MB (4119520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:87699ffbb6336d81981f3b649db038273e817358d00a8a119ca185b4de9d209e`  
		Last Modified: Mon, 16 Mar 2026 19:00:47 GMT  
		Size: 40.5 MB (40499112 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e5d283a54c706a46369217ecd8b272fdbc458b2c8ff1653680d30e2b6274302`  
		Last Modified: Mon, 16 Mar 2026 19:10:57 GMT  
		Size: 7.2 MB (7180487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:pypy` - unknown; unknown

```console
$ docker pull hylang@sha256:4011cf5b751e0001e15c95865c4cd08d27f5c5775c5978feba73410b9ef05bc2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2b8c78a384fc04290460a2451586829fe585a414346be7ffa19956657b2627e`

```dockerfile
```

-	Layers:
	-	`sha256:4a771ac3020475a7c3ffca0ebbb8d01139dea91070e0eab69a6594913b10561f`  
		Last Modified: Mon, 16 Mar 2026 19:10:57 GMT  
		Size: 2.3 MB (2294714 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:94a6d0881c94199899a9eacf9bce0a5b0a7f38cb941a88901249699c3268d2e5`  
		Last Modified: Mon, 16 Mar 2026 19:10:57 GMT  
		Size: 11.2 KB (11198 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:pypy` - windows version 10.0.26100.32522; amd64

```console
$ docker pull hylang@sha256:fa23773aad257062e4081f610d094be8b3ab7f18f410cf8f321c2cda75ca752a
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2135591361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:faac391dd2277421bec287c8bc71fe446a74e348b0b47ed1af7c4bda502f81ea`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Fri, 06 Mar 2026 02:07:33 GMT
RUN Install update 10.0.26100.32522
# Mon, 16 Mar 2026 18:57:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Mar 2026 18:58:16 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Mon, 16 Mar 2026 18:58:33 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Mon, 16 Mar 2026 18:58:34 GMT
ENV PYPY_VERSION=7.3.21
# Mon, 16 Mar 2026 18:59:39 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.21-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a1a2b069533b838f465157025e58933199f311f5f3f58549ccaf9872ee90fa53'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.21-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Mon, 16 Mar 2026 18:59:40 GMT
CMD ["pypy"]
# Mon, 16 Mar 2026 19:11:25 GMT
ENV HY_VERSION=1.2.0
# Mon, 16 Mar 2026 19:11:25 GMT
ENV HYRULE_VERSION=1.0.1
# Mon, 16 Mar 2026 19:12:16 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Mon, 16 Mar 2026 19:12:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0938cf51b672b81c9804d1d5f0c57031c931f41b279270e84820c63642d6a3bd`  
		Last Modified: Tue, 10 Feb 2026 18:56:17 GMT  
		Size: 1.5 GB (1523059351 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b887ef086b6ed6d2abdb72b842528552ef42d0e668e96556db2d01a9b71bfd77`  
		Last Modified: Tue, 10 Mar 2026 17:52:26 GMT  
		Size: 558.1 MB (558136625 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d94ce603a9b18879fb25ac7cdb4c606fd45b84e2af8c29d3231798cf141b1cc`  
		Last Modified: Mon, 16 Mar 2026 18:59:52 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5837e92aa2de45f44f3d2b3060ffd3490ec0983c202a9bc1f807ad3da1f5e712`  
		Last Modified: Mon, 16 Mar 2026 18:59:51 GMT  
		Size: 380.2 KB (380232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8502be92ec15f0d47b7c6c05b086027d2d313888e0fb5aef31224259146b1c9b`  
		Last Modified: Mon, 16 Mar 2026 18:59:55 GMT  
		Size: 15.6 MB (15556706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2740253ebf914ffc57ea83c438d724c87bb9906ce48db31b3c93300de1bd84`  
		Last Modified: Mon, 16 Mar 2026 18:59:51 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2fdbcde8331dc0b77e20809348669030c6d8e2cbd414c5b950bf0abcd0e45d3c`  
		Last Modified: Mon, 16 Mar 2026 18:59:55 GMT  
		Size: 30.5 MB (30475091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80f14009f6f960f10b79ba36ab1aacef2176617036365bb656c967c4ebfd730c`  
		Last Modified: Mon, 16 Mar 2026 18:59:51 GMT  
		Size: 1.3 KB (1340 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ec5943fa167460142c1d9acee72b8efc1e9a7a736c5d51780f1d5bd1db3c8db`  
		Last Modified: Mon, 16 Mar 2026 19:12:21 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb1692b766be31fabf95778c67c7aa8e6ab1e43fa3168efc25c59082ef333b69`  
		Last Modified: Mon, 16 Mar 2026 19:12:21 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34a1a45d7fa2e8991c11edc5c2357a042183a4585a7e4346c0da7ec4f24e62aa`  
		Last Modified: Mon, 16 Mar 2026 19:12:22 GMT  
		Size: 8.0 MB (7975418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2161145a50cdb267fc61f59cc368e92a66eead0e45a27841c5ee723f34d4ee6`  
		Last Modified: Mon, 16 Mar 2026 19:12:21 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:pypy` - windows version 10.0.20348.4893; amd64

```console
$ docker pull hylang@sha256:0e88062085dabd73dc435585e97a4c33393c745223756b6bd97a773c39203e6f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.0 GB (2036755303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b2977025fed60aed301c3a89be3a6b6faaa38e425e31f928375efe62a24daae0`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Tue, 03 Mar 2026 22:48:22 GMT
RUN Install update 10.0.20348.4893
# Mon, 16 Mar 2026 19:04:30 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Mon, 16 Mar 2026 19:04:53 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Mon, 16 Mar 2026 19:05:09 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Mon, 16 Mar 2026 19:05:10 GMT
ENV PYPY_VERSION=7.3.21
# Mon, 16 Mar 2026 19:05:51 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.21-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = 'a1a2b069533b838f465157025e58933199f311f5f3f58549ccaf9872ee90fa53'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.21-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Mon, 16 Mar 2026 19:05:52 GMT
CMD ["pypy"]
# Mon, 16 Mar 2026 20:11:34 GMT
ENV HY_VERSION=1.2.0
# Mon, 16 Mar 2026 20:11:35 GMT
ENV HYRULE_VERSION=1.0.1
# Mon, 16 Mar 2026 20:12:32 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Mon, 16 Mar 2026 20:12:33 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 18:58:34 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e55fb54b35ee36c2d316d377de271bb39bd7e71b8d127ad0d2a686bc485ab280`  
		Last Modified: Tue, 10 Mar 2026 18:03:51 GMT  
		Size: 493.3 MB (493262254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:382c211fcd999305c4f8a97b951257f3d692b04bec7ed4271da15f6476df81c2`  
		Last Modified: Mon, 16 Mar 2026 19:05:59 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973b8980fc320096181b3ba375e3732b07cc6cc9d28b246c086f917be93acc1a`  
		Last Modified: Mon, 16 Mar 2026 19:05:58 GMT  
		Size: 502.2 KB (502199 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35178cd89d97626ea7dd8e156aa93e5d1a3cf33ba17a4fc9f25ffc6e1108e9b3`  
		Last Modified: Mon, 16 Mar 2026 19:06:01 GMT  
		Size: 15.5 MB (15542789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b716dc9c30275013b0d59f080fa7c328c1fdb1e62626bb721d8f13d30701e43b`  
		Last Modified: Mon, 16 Mar 2026 19:05:58 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03487f5371c4c2070c72e870c88b29a6f55912c21095458d6abe8c2fb41f29c1`  
		Last Modified: Mon, 16 Mar 2026 19:06:02 GMT  
		Size: 30.5 MB (30461339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da5b2bb6148d2fa9adabc824647dbf60486d7b53ad24da9ff0a00652dcf8c2f6`  
		Last Modified: Mon, 16 Mar 2026 19:05:58 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ec05b5f5e9359f05105a691d346bd479573e04e48d6155539619c04587ce13b`  
		Last Modified: Mon, 16 Mar 2026 20:12:37 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1bdfb7fd0810d7d4d7061f1eeff583f9ef3556f3a7bb12d9761595cc5f3f69c`  
		Last Modified: Mon, 16 Mar 2026 20:12:37 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d0bb56161a33711bad86201ca1d4cf5d6b6607064c42a33cfcb6d0f0af26e29`  
		Last Modified: Mon, 16 Mar 2026 20:12:38 GMT  
		Size: 8.0 MB (7959803 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcc0170ceafeae64cc3d3789f3f84232b5c0a2762beac609f8291ff8c6e39c0b`  
		Last Modified: Mon, 16 Mar 2026 20:12:37 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
