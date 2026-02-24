## `pypy:2-7-slim-bookworm`

```console
$ docker pull pypy@sha256:927e902ecc1577ad035b5c85398ffa3936648529a6f5645bf2269cebf55d05ae
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
$ docker pull pypy@sha256:628f9824cf5f31ce306a58be86089fe38c2031831e258d25803984798a9e4edb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.1 MB (66146639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c70ac680fda238c7ff0462fffb2961b1292d0a7e2818b31995ba1c4bdd2e48ba`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:38:40 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:38:51 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:38:51 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:38:51 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 24 Feb 2026 19:38:51 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux64.tar.bz2'; 			sha256='aa3bb92dbb529fa2d4920895b16d67a810b0c709207857d56cfe4a6e3b41e02a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-aarch64.tar.bz2'; 			sha256='f22a1be607deeaa4f9be6bc63aae09fe4fb5b990d6a23aa4e7c5960dc5d93c96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux32.tar.bz2'; 			sha256='9d554c5efcb6ef80146bb82965f5d8404d6848e6f04b25c378852a095768a69c'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 24 Feb 2026 19:38:51 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:84a2afebaf4de2e8eb885634a69abd0087b79c947c53fa4f0481235d6dfadc6c`  
		Last Modified: Tue, 24 Feb 2026 18:43:00 GMT  
		Size: 28.2 MB (28236279 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ddb5b02da5cb0f6d666f3a7d8607c906ee37b2d2c91310ee135770b5e170bccf`  
		Last Modified: Tue, 24 Feb 2026 19:39:02 GMT  
		Size: 3.5 MB (3510208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bab435becb6672271d0d43a025eb131cc1ec14ec8f336b6078f85a092b0ffbad`  
		Last Modified: Tue, 24 Feb 2026 19:39:03 GMT  
		Size: 34.4 MB (34400152 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:bda6b3a36f16a229ede1f31c700f49a260a19505c8e9d62f5cc1db319702971e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2537030 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f793f3c2b7b76ec859820d183fef67d2121c5d75ab9c70c548589e25661547c7`

```dockerfile
```

-	Layers:
	-	`sha256:1c36971569055aa7186db5a6f49206c40caddde42fdbcc5cd0be8838839b53ec`  
		Last Modified: Tue, 24 Feb 2026 19:39:02 GMT  
		Size: 2.5 MB (2518197 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:04421cf4d7ed31f83884e9920321e6b8aea142000bd6910b3e9286539aa06978`  
		Last Modified: Tue, 24 Feb 2026 19:39:01 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-slim-bookworm` - linux; arm64 variant v8

```console
$ docker pull pypy@sha256:d516af15d766a1f576f99fd95f196aca7e2c63b4ec4f3542d77dd29988c66411
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63768580 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd5228d8e159060d5a8d175a738cee0c571824b3b7f70687d7bd18923935be6`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:43:43 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:43:57 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:43:57 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:43:57 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 24 Feb 2026 19:43:57 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux64.tar.bz2'; 			sha256='aa3bb92dbb529fa2d4920895b16d67a810b0c709207857d56cfe4a6e3b41e02a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-aarch64.tar.bz2'; 			sha256='f22a1be607deeaa4f9be6bc63aae09fe4fb5b990d6a23aa4e7c5960dc5d93c96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux32.tar.bz2'; 			sha256='9d554c5efcb6ef80146bb82965f5d8404d6848e6f04b25c378852a095768a69c'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 24 Feb 2026 19:43:57 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:eb04ef52de3a23999fcda632f100324a4d1dbebd588b4df190c4a172bb88c603`  
		Last Modified: Tue, 24 Feb 2026 18:42:16 GMT  
		Size: 28.1 MB (28116081 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e88274e796fcb67d47febbd7453ff137a3128f5330ed487e55cafe9fd7a6ba0`  
		Last Modified: Tue, 24 Feb 2026 19:44:07 GMT  
		Size: 3.3 MB (3341515 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d7e53ef8cd44743fe9f8c2ade9a1761a50b3863b65661e0a00b20294807cae2`  
		Last Modified: Tue, 24 Feb 2026 19:44:08 GMT  
		Size: 32.3 MB (32310984 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:3e88a2da0a08742ac30b7a67c868571ac1cd66e611621f659cf5a1849a33317c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2537507 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f4805234b5d005a295a50f71d3224aeb7501d7dada23bebd8df9989efd61038`

```dockerfile
```

-	Layers:
	-	`sha256:f8d12623bac3d73d0a81ff090bcae2d2d70e028ceaad4038b00b3e2bda9bd7f6`  
		Last Modified: Tue, 24 Feb 2026 19:44:07 GMT  
		Size: 2.5 MB (2518507 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:63767bb50ffb165a948173ebdd59ca43015c5b73da013a6c7374561599170928`  
		Last Modified: Tue, 24 Feb 2026 19:44:07 GMT  
		Size: 19.0 KB (19000 bytes)  
		MIME: application/vnd.in-toto+json

### `pypy:2-7-slim-bookworm` - linux; 386

```console
$ docker pull pypy@sha256:844cd3f4c686d093dc7f49a1c353e998f0d8f215aec301b80d79a18d3f09e35b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.7 MB (62697509 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d32a457900897e82e70bd831cf64c38d5caff14d27972603f89d28e5d0a5476`
-	Default Command: `["pypy"]`

```dockerfile
# Mon, 23 Feb 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'bookworm' '@1771804800'
# Tue, 24 Feb 2026 19:34:51 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends ca-certificates; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 24 Feb 2026 19:35:05 GMT
ENV LANG=C.UTF-8
# Tue, 24 Feb 2026 19:35:05 GMT
ENV PATH=/opt/pypy/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 24 Feb 2026 19:35:05 GMT
ENV PYPY_VERSION=7.3.20
# Tue, 24 Feb 2026 19:35:05 GMT
RUN set -eux; 		dpkgArch="$(dpkg --print-architecture)"; 	case "${dpkgArch##*-}" in 		'amd64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux64.tar.bz2'; 			sha256='aa3bb92dbb529fa2d4920895b16d67a810b0c709207857d56cfe4a6e3b41e02a'; 			;; 		'arm64') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-aarch64.tar.bz2'; 			sha256='f22a1be607deeaa4f9be6bc63aae09fe4fb5b990d6a23aa4e7c5960dc5d93c96'; 			;; 		'i386') 			url='https://downloads.python.org/pypy/pypy2.7-v7.3.20-linux32.tar.bz2'; 			sha256='9d554c5efcb6ef80146bb82965f5d8404d6848e6f04b25c378852a095768a69c'; 			;; 		*) echo >&2 "error: current architecture ($dpkgArch) does not have a corresponding PyPy $PYPY_VERSION binary release"; exit 1 ;; 	esac; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		wget 		libfreetype6 	; 		wget -O pypy.tar.bz2 "$url" --progress=dot:giga; 	echo "$sha256 *pypy.tar.bz2" | sha256sum --check --strict -; 	mkdir /opt/pypy; 	tar -xjC /opt/pypy --strip-components=1 -f pypy.tar.bz2; 	find /opt/pypy/lib* -depth -type d -a \( -name test -o -name tests \) -exec rm -rf '{}' +; 	rm pypy.tar.bz2; 		ln -sv '/opt/pypy/bin/pypy' /usr/local/bin/; 		pypy --version; 		apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	export shellPid="$$"; 	find /opt/pypy -type f -executable -exec ldd '{}' ';' 		| grep -vE 'lib(tcl|tk|X[a-z]*)[0-9]*[.]' 		| awk '/not found/ { print >> "/dev/stderr"; system("kill -9 -$shellPid") } /=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1 || index(so, "/opt/pypy/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	pypy --version; 		pypy -m ensurepip --default-pip; 	pip --version; 	pip install --disable-pip-version-check --no-cache-dir --no-compile 'wheel<0.46'; 		find /opt/pypy -depth 		\( 			\( -type d -a \( -name test -o -name tests \) \) 			-o 			\( -type f -a \( -name '*.pyc' -o -name '*.pyo' \) \) 		\) -exec rm -rf '{}' + # buildkit
# Tue, 24 Feb 2026 19:35:05 GMT
CMD ["pypy"]
```

-	Layers:
	-	`sha256:bab6f574391274ab5dcfab8bda32d58ff3363c5f6d8b329979ceac5bd4afee6d`  
		Last Modified: Tue, 24 Feb 2026 18:42:08 GMT  
		Size: 29.2 MB (29221705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5af18b81eeb1e5efc4e0dfe1cf16bc9f5f753b995b3bf624ffa6a4a87a1b3d12`  
		Last Modified: Tue, 24 Feb 2026 19:35:15 GMT  
		Size: 3.5 MB (3512930 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f64cdb4d8185a89b1f350cb4e1cc4a4b149cb8568159377cc0ca851006cb7976`  
		Last Modified: Tue, 24 Feb 2026 19:35:16 GMT  
		Size: 30.0 MB (29962874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `pypy:2-7-slim-bookworm` - unknown; unknown

```console
$ docker pull pypy@sha256:26361550512df58b3e0a29350360462b66c8411df2a9fe850893255f2da42f8f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.5 MB (2534129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4f8c9f050de362a14212c74900d718b9a9bf9818d4eb6d0025685c931806c0c8`

```dockerfile
```

-	Layers:
	-	`sha256:21615746a93c6e957f0efeea48a61ada35aee24457f84f9a52c1ffff45859d24`  
		Last Modified: Tue, 24 Feb 2026 19:35:15 GMT  
		Size: 2.5 MB (2515350 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:95acf938af48748b2dd83349d79d9b3fe3d690e7e32adf95363bce3b7bda9ecb`  
		Last Modified: Tue, 24 Feb 2026 19:35:15 GMT  
		Size: 18.8 KB (18779 bytes)  
		MIME: application/vnd.in-toto+json
