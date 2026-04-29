## `hylang:1-pypy3.11`

```console
$ docker pull hylang@sha256:f8abd7dbfd8dfbeb0e8fa1f917f5f885e8c398eec65775885c5ee0ad2069a4d8
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
$ docker pull hylang@sha256:ecbfccd156ada7cf5c4a2bc927c7bd883f27f8ccee8bee463038f1bc2d045245
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.0 MB (76014766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf4b8cace361a572e3dbba53668f1405ec3099ca0e25a435987d8779e2c1fac6`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Tue, 28 Apr 2026 23:34:31 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 23:35:18 GMT
ENV LANG=C.UTF-8
# Tue, 28 Apr 2026 23:35:18 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 23:35:18 GMT
ENV PYPY_VERSION=7.3.22
# Tue, 28 Apr 2026 23:35:18 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux64.tar.bz2'; 			sha256='c0c239a6b0d381338bcccf852d0690b9daca632e0216389a3796f8817fd66e0e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-aarch64.tar.bz2'; 			sha256='c29a8933e2084f52df74c829aa0d8f5652b9d5919f68e9fb89cab3afe35dd884'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux32.tar.bz2'; 			sha256='6fdad58d6d376810cf6291be1d396032f4da8109517357de0091adc3874f04c9'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 28 Apr 2026 23:35:18 GMT
CMD ["pypy3"]
# Wed, 29 Apr 2026 00:10:16 GMT
ENV HY_VERSION=1.2.0
# Wed, 29 Apr 2026 00:10:16 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 29 Apr 2026 00:10:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 29 Apr 2026 00:10:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:482b286e91e65575f9c050ac38745c8076a0e51fe8910134bccf76b28995cd1c`  
		Last Modified: Tue, 28 Apr 2026 23:35:29 GMT  
		Size: 1.2 MB (1220838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dca32d7599dc191e6046b135c6a63fcebb0fcfa305cb658056e123756db047a9`  
		Last Modified: Tue, 28 Apr 2026 23:35:30 GMT  
		Size: 37.8 MB (37772400 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:98265ad61b1b1667e74a2d51aef3a0da6277e94e0e051e2b4cd76f2424919a9a`  
		Last Modified: Wed, 29 Apr 2026 00:10:24 GMT  
		Size: 7.2 MB (7241354 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:61ae6431abb19485cfadffc4350b9e6df9f0e7b45fef1d5cdb13f49adf44a8a0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2308927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6628c5f65c905ff3f0c1cc672ec9c53320cab493aa4f5f92e66bbbe277f86baa`

```dockerfile
```

-	Layers:
	-	`sha256:bc2bf54254187eb1958b28a210c5ad0c55faac8e534cf1eb69c04779fe4787c9`  
		Last Modified: Wed, 29 Apr 2026 00:10:24 GMT  
		Size: 2.3 MB (2297637 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:28375ac03b861a8f76bce1c41e4c1ef4b2e958d0ccfdc362122200a8c7b43e1e`  
		Last Modified: Wed, 29 Apr 2026 00:10:24 GMT  
		Size: 11.3 KB (11290 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.11` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:b9713cdf22900c056696d3c5c54ff493b0dc9fa98bf0f932d51a5c1582618b0d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.5 MB (74545355 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:550337eb70dfcae69defba19e6a6fbbfcd7a18b7faf48597553ce642ea764ba8`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Tue, 28 Apr 2026 23:35:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 28 Apr 2026 23:36:29 GMT
ENV LANG=C.UTF-8
# Tue, 28 Apr 2026 23:36:29 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 28 Apr 2026 23:36:29 GMT
ENV PYPY_VERSION=7.3.22
# Tue, 28 Apr 2026 23:36:29 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux64.tar.bz2'; 			sha256='c0c239a6b0d381338bcccf852d0690b9daca632e0216389a3796f8817fd66e0e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-aarch64.tar.bz2'; 			sha256='c29a8933e2084f52df74c829aa0d8f5652b9d5919f68e9fb89cab3afe35dd884'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux32.tar.bz2'; 			sha256='6fdad58d6d376810cf6291be1d396032f4da8109517357de0091adc3874f04c9'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 28 Apr 2026 23:36:29 GMT
CMD ["pypy3"]
# Wed, 29 Apr 2026 00:10:13 GMT
ENV HY_VERSION=1.2.0
# Wed, 29 Apr 2026 00:10:13 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 29 Apr 2026 00:10:13 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 29 Apr 2026 00:10:13 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f7a93fb0b478b98c152c681a358deec99c7d525432ce9ed15b66701cc6ba9f64`  
		Last Modified: Tue, 28 Apr 2026 23:36:41 GMT  
		Size: 1.2 MB (1202297 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e711930c7be2fd3b05ce383d6629e5d0b9ad450c7c16f0f2ee06002a3d288f18`  
		Last Modified: Tue, 28 Apr 2026 23:36:42 GMT  
		Size: 36.0 MB (35957934 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f538f165eadf41c9032cc3816b8413e5e1f45731894f5b06a321a1dd25e02f0f`  
		Last Modified: Wed, 29 Apr 2026 00:10:21 GMT  
		Size: 7.2 MB (7241518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:f1e09199bd1f7489304d28ee670916ea71f1cbd38c6050bd110cc3432a60f26b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2309589 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88e174ea6df87de533f545f54d8ccd0b646f410d12bc528e57f9198b3b93cdcf`

```dockerfile
```

-	Layers:
	-	`sha256:52205348268af43f5b01ed99b54ebe807261568379e5c51b8d949960e12561b4`  
		Last Modified: Wed, 29 Apr 2026 00:10:21 GMT  
		Size: 2.3 MB (2298051 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a910cbcdcb2d06eb466c3572a9bb25b319ac97f4e3c8d53304e14d3297fc926c`  
		Last Modified: Wed, 29 Apr 2026 00:10:21 GMT  
		Size: 11.5 KB (11538 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.11` - linux; 386

```console
$ docker pull hylang@sha256:5f884c5182b093c8a957716c48ed658a563f0fe8d3e75b65bf9e129b3c470d79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73575391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:795d32b666af9d785f1927c574fd47f9446642411ca78b3097ce7cfef4d6c1de`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 29 Apr 2026 00:30:34 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 29 Apr 2026 00:31:26 GMT
ENV LANG=C.UTF-8
# Wed, 29 Apr 2026 00:31:26 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 29 Apr 2026 00:31:26 GMT
ENV PYPY_VERSION=7.3.22
# Wed, 29 Apr 2026 00:31:26 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux64.tar.bz2'; 			sha256='c0c239a6b0d381338bcccf852d0690b9daca632e0216389a3796f8817fd66e0e'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-aarch64.tar.bz2'; 			sha256='c29a8933e2084f52df74c829aa0d8f5652b9d5919f68e9fb89cab3afe35dd884'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy3.11-v7.3.22-linux32.tar.bz2'; 			sha256='6fdad58d6d376810cf6291be1d396032f4da8109517357de0091adc3874f04c9'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfontconfig1 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		rm -v /opt/pypy/lib/libtk*.so /opt/pypy/lib/libz.so*; 		ln -sv '/opt/pypy/bin/pypy3' /usr/local/bin/; 		pypy3 --version; 		cd /opt/pypy/lib/pypy3.11; 	if [ -f _gdbm_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libgdbm-dev; 		pypy3 _gdbm_build.py; 	fi; 	if [ -f _ssl_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libssl-dev; 		pypy3 _ssl_build.py; 	fi; 	if [ -f _lzma_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev liblzma-dev; 		pypy3 _lzma_build.py; 	fi; 	if [ -f _sqlite3_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev libsqlite3-dev; 		pypy3 _sqlite3_build.py; 	fi; 	if [ -f _tkinter/tklib_build.py ]; then 		apt-get install -y --no-install-recommends gcc libc6-dev tk-dev; 		pypy3 _tkinter/tklib_build.py; 	fi; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy3 --version; 		pypy3 -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Wed, 29 Apr 2026 00:31:26 GMT
CMD ["pypy3"]
# Wed, 29 Apr 2026 03:34:09 GMT
ENV HY_VERSION=1.2.0
# Wed, 29 Apr 2026 03:34:09 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 29 Apr 2026 03:34:09 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 29 Apr 2026 03:34:09 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec5e2026808942afeab418e84417cac8a989aee1893edc853192545eb4ffebf`  
		Last Modified: Wed, 29 Apr 2026 00:31:37 GMT  
		Size: 1.2 MB (1227969 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:972983c9669487bc3804c602068c61c89fd5b0defa6d39de6f52f489ab2c144c`  
		Last Modified: Wed, 29 Apr 2026 00:31:38 GMT  
		Size: 33.8 MB (33809661 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:33bb848d24853072120b037afa3415a0ac204a27f03ac69144d27499f0bfb3c1`  
		Last Modified: Wed, 29 Apr 2026 03:34:16 GMT  
		Size: 7.2 MB (7241434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:1f6d6e2f15f78f0bb316c15fc888174797eb22aeb7c83dd14df1321430f8049c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.3 MB (2305948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ac0f51bcd16c1c81f410d9727066faa4ab86ee5c74fa3b8e4d479242c73d26`

```dockerfile
```

-	Layers:
	-	`sha256:c56e07fbaba5558c7b5c46f45c7d6c6d297916f69a7190b4e8885ffe87638ba6`  
		Last Modified: Wed, 29 Apr 2026 03:34:16 GMT  
		Size: 2.3 MB (2294750 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:55c9929e38b735af78cc35d71772851c3db00d08a172db861f7b6596e2fc62c8`  
		Last Modified: Wed, 29 Apr 2026 03:34:16 GMT  
		Size: 11.2 KB (11198 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.11` - windows version 10.0.26100.32690; amd64

```console
$ docker pull hylang@sha256:0e89f327b29e31ba9bb726e48c41b48bacd2b5b0e2d388e8ea4566bc07e99a4e
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2184937011 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba0cbd822debc81ec2bc872bd7dbb4b22153332619310ce4981446ed0fd8aa3a`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 28 Apr 2026 23:43:27 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 28 Apr 2026 23:44:10 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 28 Apr 2026 23:44:41 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 28 Apr 2026 23:44:42 GMT
ENV PYPY_VERSION=7.3.22
# Tue, 28 Apr 2026 23:45:25 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.22-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '748f393e69726f32c908bfd8d778dda267482c0b15b2d4957c97f0842f37d33f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.22-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 28 Apr 2026 23:45:25 GMT
CMD ["pypy"]
# Wed, 29 Apr 2026 00:09:14 GMT
ENV HY_VERSION=1.2.0
# Wed, 29 Apr 2026 00:09:14 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 29 Apr 2026 00:10:01 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 29 Apr 2026 00:10:01 GMT
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
	-	`sha256:921d9d8a0d1cbcbd263a6b927a82d6935d5da5fb021c9a4fbfec721f4604a33d`  
		Last Modified: Tue, 28 Apr 2026 23:45:31 GMT  
		Size: 1.3 KB (1348 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fc1ff47ac99687b5605cc056ef288f23174c6f64bc8d869a652c305c647381c`  
		Last Modified: Tue, 28 Apr 2026 23:45:30 GMT  
		Size: 393.5 KB (393470 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14aa3b3b9d2b95df2c594d5cdd72f0c160f226760374d3216c10474274c1dee3`  
		Last Modified: Tue, 28 Apr 2026 23:45:34 GMT  
		Size: 15.6 MB (15572165 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12b747414ce435fc752348a3f85bf0ff1e1b67d79eee476991fa7e9daeccde6e`  
		Last Modified: Tue, 28 Apr 2026 23:45:30 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105ac0f4f46f30056c6539c8140b7ed6f5822972c0ed8b5d99a624e17853d24e`  
		Last Modified: Tue, 28 Apr 2026 23:45:34 GMT  
		Size: 30.9 MB (30934827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d68ee3b414a8d926138b6b15b6e8d15d547490220824a32f41caaaf6768378f`  
		Last Modified: Tue, 28 Apr 2026 23:45:30 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51aae8044d3ec4871484b77332c7041cbd42b9623c458d54190aca4ea421dde5`  
		Last Modified: Wed, 29 Apr 2026 00:10:06 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f36e2d4160ff0509da938cd9e2c904b34a151a336e3fd0ed05479ff69976e04e`  
		Last Modified: Wed, 29 Apr 2026 00:10:06 GMT  
		Size: 1.3 KB (1293 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988f0e81109c9fdfca44df17433ed985b0554519a21b72dc9ec9a7f352523e6b`  
		Last Modified: Wed, 29 Apr 2026 00:10:07 GMT  
		Size: 8.0 MB (8042670 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d08da71ef120fb6653dae039b340adb2cbe358803a0a8727dec22e45da3ed90`  
		Last Modified: Wed, 29 Apr 2026 00:10:05 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-pypy3.11` - windows version 10.0.20348.5020; amd64

```console
$ docker pull hylang@sha256:d59ccdc70233dc6e271529ed2123c8eb0b554fd1f067c733385f2a6e87edabbc
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2125187132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d9567d7049e565c4cb09470fcd0ac195b92ef74a1189ea2e05fe85ee57b0a7b`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 28 Apr 2026 23:38:40 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 28 Apr 2026 23:54:55 GMT
RUN $newPath = ('C:\pypy;C:\pypy\Scripts;{0}' -f $env:PATH); 	Write-Host ('Updating PATH: {0}' -f $newPath); 	[Environment]::SetEnvironmentVariable('PATH', $newPath, [EnvironmentVariableTarget]::Machine); 	Write-Host 'Complete.'
# Tue, 28 Apr 2026 23:55:05 GMT
RUN $url = 'https://download.microsoft.com/download/6/A/A/6AA4EDFF-645B-48C5-81CC-ED5963AEAD48/vc_redist.x64.exe'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'vc.exe'; 		$sha256 = 'da66717784c192f1004e856bbcf7b3e13b7bf3ea45932c48e4c9b9a50ca80965'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash vc.exe -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	Start-Process 		-NoNewWindow 		-Wait 		-FilePath .\vc.exe 		-ArgumentList @( 			'/install', 			'/quiet', 			'/norestart' 		); 		Write-Host 'Removing ...'; 	Remove-Item vc.exe -Force; 		Write-Host 'Complete.'
# Tue, 28 Apr 2026 23:55:05 GMT
ENV PYPY_VERSION=7.3.22
# Tue, 28 Apr 2026 23:55:41 GMT
RUN $url = 'https://downloads.python.org/pypy/pypy3.11-v7.3.22-win64.zip'; 	Write-Host ('Downloading {0} ...' -f $url); 	Invoke-WebRequest -Uri $url -OutFile 'pypy.zip'; 		$sha256 = '748f393e69726f32c908bfd8d778dda267482c0b15b2d4957c97f0842f37d33f'; 	Write-Host ('Verifying sha256 ({0}) ...' -f $sha256); 	if ((Get-FileHash pypy.zip -Algorithm sha256).Hash -ne $sha256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Expanding ...'; 	Expand-Archive pypy.zip -DestinationPath C:\; 		Write-Host 'Removing ...'; 	Remove-Item pypy.zip -Force; 		Write-Host 'Renaming ...'; 	Rename-Item -Path C:\pypy3.11-v7.3.22-win64 -NewName C:\pypy; 		Write-Host 'Verifying install ("pypy --version") ...'; 	pypy --version; 		Write-Host 'Installing pip ...'; 	pypy -m ensurepip --default-pip; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Installing "wheel" (backwards compat) ...'; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		Write-Host 'Cleanup install ...'; 	Get-ChildItem 		-Path C:\pypy 		-Include @( 'test', 'tests' ) 		-Directory 		-Recurse 		| Remove-Item -Force -Recurse; 	Get-ChildItem 		-Path C:\pypy 		-Include @( '*.pyc', '*.pyo' ) 		-File 		-Recurse 		| Remove-Item -Force; 		Write-Host 'Complete.'
# Tue, 28 Apr 2026 23:55:42 GMT
CMD ["pypy"]
# Wed, 29 Apr 2026 00:10:44 GMT
ENV HY_VERSION=1.2.0
# Wed, 29 Apr 2026 00:10:45 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 29 Apr 2026 00:11:31 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 29 Apr 2026 00:11:32 GMT
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
	-	`sha256:53ca5032646149381c2c20fb699279519e0fd4478538cc8b6a7db546c3309a3c`  
		Last Modified: Tue, 28 Apr 2026 23:40:35 GMT  
		Size: 1.3 KB (1296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f140fab81434cf3ce8bc50228ef9fd44fd7d47f195314d7acadd2b43894af5bc`  
		Last Modified: Tue, 28 Apr 2026 23:55:46 GMT  
		Size: 496.7 KB (496701 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2d9b2bf257fcbd014618b444c3442b0c251b46c729cffd7a98a1097906e359`  
		Last Modified: Tue, 28 Apr 2026 23:55:51 GMT  
		Size: 15.5 MB (15541455 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4853a6f29f1f0cd23dd4fe9fadcbeec8d729d12994ff836919093c6c0a754b`  
		Last Modified: Tue, 28 Apr 2026 23:55:46 GMT  
		Size: 1.3 KB (1333 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cab4c1315f8e91d5f3e5b1ebff648e33261bf31a23c2a663ddcb700d8658c0a`  
		Last Modified: Tue, 28 Apr 2026 23:55:50 GMT  
		Size: 30.9 MB (30911073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdd96caffc5da425ba4d285fcea86be014b0082cc518a54841b1895ed86c93d0`  
		Last Modified: Tue, 28 Apr 2026 23:55:46 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:581981b30904e6d43cc7e85b5057e1fa5642c9e296fd377a9e5bc0e384dc72c0`  
		Last Modified: Wed, 29 Apr 2026 00:11:36 GMT  
		Size: 1.3 KB (1323 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59717c2257ceb2229f060e55f612e36b1c969943f0202d5cd2d89f13f50afafb`  
		Last Modified: Wed, 29 Apr 2026 00:11:36 GMT  
		Size: 1.3 KB (1330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f760ee82bf7e6b856bdf7ae2564a3b67dcf03a6e1a2123d15b37bd3d57d75d60`  
		Last Modified: Wed, 29 Apr 2026 00:11:37 GMT  
		Size: 8.0 MB (8018732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f3beb9b168f98d7b4827dc75f199e4d8e59695c7cbd008bbb523dcd230c8803`  
		Last Modified: Wed, 29 Apr 2026 00:11:36 GMT  
		Size: 1.3 KB (1331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
