## `hylang:1-pypy3.10-bullseye`

```console
$ docker pull hylang@sha256:75669635156d6e72f5a619fa5c5ddc5bef7490c76c68b1a9b7aaf928f74b8aa1
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 6
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown

### `hylang:1-pypy3.10-bullseye` - linux; amd64

```console
$ docker pull hylang@sha256:4e80da8587ebdd3bb904406cb06c8161c54678566a46192a9ab91bb897031ab2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.1 MB (72149043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:262afcb9ab0d16e6ee5f032e830507d5373e170842171fec35a855207fa28d23`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 18:15:04 GMT
RUN # debian.sh --arch 'amd64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:c8e1eb8ab3b017bd9e33ddec83ebdd8292c542bbd14a8d5a6cfa2edc3ad3b8eb`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 30.3 MB (30254604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d19028a4bead78a510dd68a2850e7f65f46142c918d01f3be3c763b621797f1`  
		Last Modified: Mon, 28 Apr 2025 22:02:20 GMT  
		Size: 1.1 MB (1066581 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ff5961a100bac2762e8953a17871c37791921824d0dfb3aa656b19cdb3eff1ce`  
		Last Modified: Mon, 28 Apr 2025 22:02:21 GMT  
		Size: 34.5 MB (34463475 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2c4c0cffea7f6a23a5100d69f666d87866c5e980ac75e80aa281ddb1e8ce3109`  
		Last Modified: Fri, 09 May 2025 17:36:20 GMT  
		Size: 6.4 MB (6364383 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:7d4603f0c09931e7cc53e169a2d378ab41a4c94bac7b90543519221e50209219
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a52f99aec348a896dcc5945205e2df323734d7284e040e24fa24382531d44694`

```dockerfile
```

-	Layers:
	-	`sha256:ae591bec46588008a0fbd8e22df58bfb3c7de8cb013d59cf2ef3326a2226b4b0`  
		Last Modified: Fri, 09 May 2025 17:36:20 GMT  
		Size: 2.7 MB (2700603 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5bc410759c4025ff716585744c18e89a3a7c4abf6b95c28c26f5c85243b2d251`  
		Last Modified: Fri, 09 May 2025 17:36:20 GMT  
		Size: 8.8 KB (8829 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.10-bullseye` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:4e4e092b6abc460c34af4bf18dd8e80d5ad062f2973dd98df9b178e4db7e2a47
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.9 MB (68900883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:710f4045e7651d82d7d8522fe3e8123cb9188dd48f441a0c4e82f91d3f073b7c`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 18:15:04 GMT
RUN # debian.sh --arch 'arm64' out/ 'bullseye' '@1745798400'
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
	-	`sha256:5d3a81360c5bb9281a4f735a1468429a1898f1a4fc24a2581dde4cf28ace4488`  
		Last Modified: Mon, 28 Apr 2025 21:21:09 GMT  
		Size: 28.7 MB (28744645 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c83e44360f009c07721c2385826825d166ecdc6b4371775fa993189073d8f788`  
		Last Modified: Tue, 29 Apr 2025 21:55:24 GMT  
		Size: 1.1 MB (1053875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3e18ae85cdc4b8f24c8e50d9c456341cd9490a2de76e95f27e4b5387a8a5eedc`  
		Last Modified: Tue, 29 Apr 2025 21:55:24 GMT  
		Size: 32.7 MB (32737918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e8064cf46384a73adcc1d0bb91e59e3893fca4e4c2a49bd39734679a4a8781d`  
		Last Modified: Fri, 09 May 2025 19:04:02 GMT  
		Size: 6.4 MB (6364445 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:8d66869bf9af47d28b8be386ff3c6defba609e4a6271fce1fb80de899fb15b2f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2709887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:21a0af725e57be8548fa9b122c53b8d5e70e50555146db9448a4bf7ba9c546bd`

```dockerfile
```

-	Layers:
	-	`sha256:4003a946d7961f4200082aaefafb78732c72a0f48f0e2c70f60024a5ba332530`  
		Last Modified: Fri, 09 May 2025 19:04:01 GMT  
		Size: 2.7 MB (2700904 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7f198577678b69815d24d920a2cd3431e7a2c33e47a97ecee66a59ea2034f6c6`  
		Last Modified: Fri, 09 May 2025 19:04:01 GMT  
		Size: 9.0 KB (8983 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-pypy3.10-bullseye` - linux; 386

```console
$ docker pull hylang@sha256:f9fbec5118e712cb2ba577157152ddb432625b8431c4831e46b63aa5b492a170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69513899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2e1488ccd102ecb72f387f914591d34f6097f724c1f20b5ef9c4abb1ee9fb19`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 09 Apr 2025 18:15:04 GMT
RUN # debian.sh --arch 'i386' out/ 'bullseye' '@1745798400'
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
	-	`sha256:73bb1b80ecf1f8784ad6f92a35120b6e2306657fc7e8cbaedca1f45900f3d746`  
		Last Modified: Mon, 28 Apr 2025 21:08:07 GMT  
		Size: 31.2 MB (31187893 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4de5f15f70fcb3e0fc324231009cabf09962ceac2d54ae7ca7ad10b721733c7`  
		Last Modified: Mon, 28 Apr 2025 21:56:42 GMT  
		Size: 1.1 MB (1079111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a1ff23cd9aa7bc77c02ff8c574cc54c56d5304ecd15390f05b4b8f06733cdae`  
		Last Modified: Mon, 28 Apr 2025 21:56:43 GMT  
		Size: 30.9 MB (30882312 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1eec197dacafaf647fec0ca57d56be8a59f32a2c68e1822a3d9950330ec2a45`  
		Last Modified: Fri, 09 May 2025 17:36:23 GMT  
		Size: 6.4 MB (6364583 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-pypy3.10-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:3d3c524df6812223feedd4f048d2f6d77e24b42fec4ce75b7619e4e27a3d6ba7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2706488 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1a006cd8b3ffc73d76493e65c2318f389182f83392ef73d20ccdfb9241c6a18a`

```dockerfile
```

-	Layers:
	-	`sha256:76f1f8fa4a3abacd75e3e7b9d52a265ab979dd9a06f03487112771ee85401663`  
		Last Modified: Fri, 09 May 2025 17:36:23 GMT  
		Size: 2.7 MB (2697709 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95210c7877ead1753d0ea7445b5640e3b3453a2a2af0221efdd7bf56f6179519`  
		Last Modified: Fri, 09 May 2025 17:36:23 GMT  
		Size: 8.8 KB (8779 bytes)  
		MIME: application/vnd.in-toto+json
