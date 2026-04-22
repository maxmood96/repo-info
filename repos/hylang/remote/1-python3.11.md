## `hylang:1-python3.11`

```console
$ docker pull hylang@sha256:c1f3d3bcf2ecc68cdf275c0546f42c36858b43bec766461245a08ef69338632d
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 16
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v5
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; riscv64
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `hylang:1-python3.11` - linux; amd64

```console
$ docker pull hylang@sha256:cd95b05a4bfc4f7f0d143e9913141c6c40d0bc27cb2eed2fc23dbf47e84b19d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52369274 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc344301ec4600746582c7b12c305b94753d3bf63a4e71ca341dda7a9558c34`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:01:45 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:01:45 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 02:01:45 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:01:45 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 22 Apr 2026 02:01:45 GMT
ENV PYTHON_VERSION=3.11.15
# Wed, 22 Apr 2026 02:01:45 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Wed, 22 Apr 2026 02:09:07 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 02:09:07 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 02:09:07 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 05:00:16 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 05:00:16 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 05:00:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 05:00:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:91ff8760033c3b9bc9c3a3bcc6ff66c113ec9e13f94fa2f12ae4b221aae996b9`  
		Last Modified: Wed, 22 Apr 2026 02:09:15 GMT  
		Size: 1.3 MB (1293086 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f3ba2250c52436e41e9f2f3830af92de466fcacc2d848264e1f9fdc76975d803`  
		Last Modified: Wed, 22 Apr 2026 02:09:16 GMT  
		Size: 14.4 MB (14366050 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ccd73948dde4b7f1623ac6bf9b58706fb83d0a363d765d7c799d46035ceb563`  
		Last Modified: Wed, 22 Apr 2026 02:09:15 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a45e71ecc83675e986e09f9dfcb39d99dd6872808aaa6e0e671e7c07a29ea9b3`  
		Last Modified: Wed, 22 Apr 2026 05:00:23 GMT  
		Size: 6.9 MB (6929715 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:8e21e037ee23e761ae0fc09473d840f9afb7a96cf7cc90703f94d6ca3cb0543b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209327 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:43c4eb64ec62c0019118536a40f4e10d10c465196501a455a4914fc5a2607ec4`

```dockerfile
```

-	Layers:
	-	`sha256:a27639a1c12bbf148e1a7f926d75856ada3678b1189cdf8a6031cbd171c06b26`  
		Last Modified: Wed, 22 Apr 2026 05:00:23 GMT  
		Size: 2.2 MB (2200007 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a419bd717ddb03c7be4dd0e0398d5c7c26479ec8fe939d8eb50bbaa5cc6a8fdf`  
		Last Modified: Wed, 22 Apr 2026 05:00:23 GMT  
		Size: 9.3 KB (9320 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11` - linux; arm variant v5

```console
$ docker pull hylang@sha256:29a9dbe0e6657ec375742b9c557eadb825acdf1db825abe70581daffd13cb544
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50152254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eead6536e9014e7ad7f5f6a23c2226194beb0d0e3387c8225cf1b89e879da484`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:41:02 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:41:02 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 02:41:02 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:41:02 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 22 Apr 2026 02:41:02 GMT
ENV PYTHON_VERSION=3.11.15
# Wed, 22 Apr 2026 02:41:02 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Wed, 22 Apr 2026 02:58:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 02:58:49 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 02:58:49 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 04:09:08 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 04:09:08 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 04:09:08 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 04:09:08 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f1a82d47b400a0558ac3a09d3cf64972143d5d24691e0cded53562bfb3fc1eab`  
		Last Modified: Wed, 22 Apr 2026 02:58:56 GMT  
		Size: 1.3 MB (1276210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:41cdb5269f240f2447739d1b38c1248911cb8736abfe9758c8149a4484d7eca3`  
		Last Modified: Wed, 22 Apr 2026 02:58:57 GMT  
		Size: 14.0 MB (13997769 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f954865472eaaaadee9c6bed35c848aa38e67f95bb2ad5736352c6e3228be13`  
		Last Modified: Wed, 22 Apr 2026 02:58:56 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3d94b03197178e684dda0fcf53c4efe692e5fa35f08203f195efd1dba2fdd34`  
		Last Modified: Wed, 22 Apr 2026 04:09:15 GMT  
		Size: 6.9 MB (6929846 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:d5874b3007d12b2c903b95971f3a040cc59e4a782953b65e93ca738a13bcf0aa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5bdb1d1bae5d3a1ac872c420bbfd6a2248545ec497a5ae8162aebefabf7ae924`

```dockerfile
```

-	Layers:
	-	`sha256:eb2b1b703dca00965105e773ccaf46a5bbb5f486c07e18945f8d8989e1f70ae5`  
		Last Modified: Wed, 22 Apr 2026 04:09:15 GMT  
		Size: 2.2 MB (2203008 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:18577acc4a6ebaae66d27b4779f58290922cd34e1d2abb86ade2ec4f5ba97c47`  
		Last Modified: Wed, 22 Apr 2026 04:09:15 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11` - linux; arm variant v7

```console
$ docker pull hylang@sha256:c74c58dab19c65ceda4c45e675f757b2a4e8102fffaf115069e0e612eb40d0b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.1 MB (48125615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8caa0f2775b3b5c0657a82a1bcbffc96866606f2a45bdcf705c1cd69bc44a8b`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:10:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 03:10:38 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 03:10:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:10:38 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 22 Apr 2026 03:10:38 GMT
ENV PYTHON_VERSION=3.11.15
# Wed, 22 Apr 2026 03:10:38 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Wed, 22 Apr 2026 03:27:34 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 03:27:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 03:27:34 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 04:19:36 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 04:19:36 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 04:19:36 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 04:19:36 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3405c7fd3b94edda7eae8a1091a07a7ae224f48ef94cc59d76b31d7ef2f676fa`  
		Last Modified: Wed, 22 Apr 2026 03:27:42 GMT  
		Size: 1.2 MB (1249085 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4aaeaab6b47de7775aa2bf579eae28525ecd4ff8e02af23576e49b1a971a849f`  
		Last Modified: Wed, 22 Apr 2026 03:27:42 GMT  
		Size: 13.7 MB (13731497 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009e86cbfc697ae6f648cb74b4adf1868bd19136126a86b3a57e042ed178e988`  
		Last Modified: Wed, 22 Apr 2026 03:27:42 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d51ad99b2dc8ef5b340787573e5010a4b87c93b903e96db8b023e39caec8e05`  
		Last Modified: Wed, 22 Apr 2026 04:19:44 GMT  
		Size: 6.9 MB (6929946 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:8e8040b962b45e2feac3088d9bc87e413624d10b94e766736ae0017afb8bf95d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1a8de7997e1ee38b016f213cb48707ed3150737a5b2422081d26c596d4fee97`

```dockerfile
```

-	Layers:
	-	`sha256:60164fbc90848bbb42249266e69e09afebfc15c2ac785276d8bc98f5278c50b4`  
		Last Modified: Wed, 22 Apr 2026 04:19:44 GMT  
		Size: 2.2 MB (2201461 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0129ba27e984e4a5d8039d97221feeee4311e5b625f2fb56df1c38160d19da27`  
		Last Modified: Wed, 22 Apr 2026 04:19:44 GMT  
		Size: 9.4 KB (9432 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:df3c4115ea6cf1098621e6e71d8dfb25220b0363f1f40ae73e365368f5f9c171
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.7 MB (52662703 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5449638f723ae8a0c1d2774317c553033f32acf14442342413a90b97ea8aa393`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:04:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:04:05 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 02:04:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:04:05 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 22 Apr 2026 02:04:05 GMT
ENV PYTHON_VERSION=3.11.15
# Wed, 22 Apr 2026 02:04:05 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Wed, 22 Apr 2026 02:15:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 02:15:31 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 02:15:31 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 03:23:47 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 03:23:47 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 03:23:47 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 03:23:47 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ecad6f632e356308bf250c61fa3ba255caf0b36e3efb607608b55152ece6b0a`  
		Last Modified: Wed, 22 Apr 2026 02:15:38 GMT  
		Size: 1.3 MB (1273878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c9a60876db124ced70648383f11a917724cb96c0efa0e3e385f2f77a9991dab`  
		Last Modified: Wed, 22 Apr 2026 02:15:39 GMT  
		Size: 14.3 MB (14315242 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:61e75fb678e2ee0bfa0b47ea287a2cf604198f951f04cf0cbbb7884058685a0c`  
		Last Modified: Wed, 22 Apr 2026 02:15:38 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fe3256ecb21c8414ac675073fc215aed240205fe22fe3fe09a83c775ff9c6c`  
		Last Modified: Wed, 22 Apr 2026 03:23:54 GMT  
		Size: 6.9 MB (6929729 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:64b619bc6f9de38377a541fda6e7d5f0353fbe51fc441f75e157c47225af755a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2209793 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8b29ea7d695361678393dab52dc38fc01e5017806a2782eed2ab20251189c000`

```dockerfile
```

-	Layers:
	-	`sha256:9d0520043f722ba5c63a796b645c03b58ec0b5eea85b4a47f6f38cb3ac99d018`  
		Last Modified: Wed, 22 Apr 2026 03:23:54 GMT  
		Size: 2.2 MB (2200321 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e90c6027950a2228fe3f9a8bfb9263c3eaa2d83c155d21943ca43bd93f283e1e`  
		Last Modified: Wed, 22 Apr 2026 03:23:54 GMT  
		Size: 9.5 KB (9472 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11` - linux; 386

```console
$ docker pull hylang@sha256:e68c6f5aabc1f93016c3b78752aac99b1b57b37eccf3985b11864000933744b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53928436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c12deca3262dd8a3cf7f8201366e5009ca3adc18dec1b52cbfc7738bab7e764a`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 01:56:32 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 01:56:32 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 01:56:32 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 01:56:32 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 22 Apr 2026 01:56:32 GMT
ENV PYTHON_VERSION=3.11.15
# Wed, 22 Apr 2026 01:56:32 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Wed, 22 Apr 2026 02:17:28 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 02:17:28 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 02:17:28 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 05:16:43 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 05:16:43 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 05:16:43 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 05:16:43 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:dacd7cda306bf5bd7a2030f9b0c2e9d71fda44ea58493a33450d210b74a8ec75`  
		Last Modified: Wed, 22 Apr 2026 00:17:04 GMT  
		Size: 31.3 MB (31296327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd1ad3e08d7625a6a4252697a769f50290f87591f7c2d4307f1c4da03481ea00`  
		Last Modified: Wed, 22 Apr 2026 02:17:36 GMT  
		Size: 1.3 MB (1297160 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:39c2a7efb7a97f949eeff8961671a91d5a2a8e1c95812473e1fbbeab77741271`  
		Last Modified: Wed, 22 Apr 2026 02:17:36 GMT  
		Size: 14.4 MB (14404838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff3993f95c21fbe2ed6d25d2740261afa6243d92c9bc7f752820a0db28c824b`  
		Last Modified: Wed, 22 Apr 2026 02:17:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2835acf017adeb04edb272f7aaa0d03256834632b8f6224ffc967a36599acdf9`  
		Last Modified: Wed, 22 Apr 2026 05:16:50 GMT  
		Size: 6.9 MB (6929862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:e8fc1e9b3915bd8fd4b218d0a32a74fbcd53c460110bff01dd1e4c2a1e08c2fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2206436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3800d3769fb2819592c01c21a688176c9653367d6539a715936983b83c28e2f5`

```dockerfile
```

-	Layers:
	-	`sha256:2ad7dade3a8d1706668af31eb289b51864f70a750cda1b3c2ed62fa00da9462c`  
		Last Modified: Wed, 22 Apr 2026 05:16:50 GMT  
		Size: 2.2 MB (2197168 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:09979e39e1971eca394a0f9fd0c8a9a34c77a60ff61e58bb972b37e970487653`  
		Last Modified: Wed, 22 Apr 2026 05:16:50 GMT  
		Size: 9.3 KB (9268 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11` - linux; ppc64le

```console
$ docker pull hylang@sha256:04950da18fa8fbacbdd3b611d973b9926c7496bb8b88119afc3058da8e53f8cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.5 MB (56523163 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3b6a3ae407dce376831c8c3dfc2c90661bfc5fed5a99a0ae049f16a61f9ad69`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 07:24:21 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 07:24:21 GMT
ENV LANG=C.UTF-8
# Tue, 07 Apr 2026 07:24:21 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 07:24:21 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Tue, 07 Apr 2026 07:24:21 GMT
ENV PYTHON_VERSION=3.11.15
# Tue, 07 Apr 2026 07:24:21 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Tue, 07 Apr 2026 08:03:58 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Tue, 07 Apr 2026 08:03:58 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 07 Apr 2026 08:03:58 GMT
CMD ["python3"]
# Tue, 07 Apr 2026 15:48:45 GMT
ENV HY_VERSION=1.2.0
# Tue, 07 Apr 2026 15:48:45 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 07 Apr 2026 15:48:45 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 07 Apr 2026 15:48:45 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6e3428d4efac15fe7728b465c9c3bc5d71a07ad502becbd70250a2c560e32b53`  
		Last Modified: Tue, 07 Apr 2026 00:12:50 GMT  
		Size: 33.6 MB (33593016 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bcfcd2054b2b60f7daf495bbbb757ed232b0425af9d1b2631defdc5f8442fa02`  
		Last Modified: Tue, 07 Apr 2026 07:44:26 GMT  
		Size: 1.3 MB (1320868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11df6c0041f160e60ef8676216172ba3494d2cdbb8c1d602d06c8074b01f14cc`  
		Last Modified: Tue, 07 Apr 2026 08:04:13 GMT  
		Size: 14.7 MB (14698790 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:628d4ac9d8c71a7367f05df09d120de928a0014bfb3062d9902205eaa80229d4`  
		Last Modified: Tue, 07 Apr 2026 08:04:12 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce7e8c7eece322b6ed87f4b3fb9b1c0ddc6ee24541ffcee0cac10528c88bab46`  
		Last Modified: Tue, 07 Apr 2026 15:49:00 GMT  
		Size: 6.9 MB (6910239 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:ac7598d2aad9f905811acf6aacbe74e5bacedd5580c1c35891e6b4f06758b8c4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2212986 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fd935f7146a3b20d4eb08bac0e9206ca9db0c1dd73cee829d90db1e32621003`

```dockerfile
```

-	Layers:
	-	`sha256:d8d332c1e7c45bae2bd45393ed72f9bb1c8be954d86bf6ffb8bde059e69d3b32`  
		Last Modified: Tue, 07 Apr 2026 15:49:00 GMT  
		Size: 2.2 MB (2203598 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dd8607ea9e5aafcb6228931267cb2225f95523a25643949f6b5ab07b71110922`  
		Last Modified: Tue, 07 Apr 2026 15:49:00 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11` - linux; riscv64

```console
$ docker pull hylang@sha256:9b47f4ac96a86d724c67fdd24c4a2fde0250148f3d7044dc35b49eca908fccad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.3 MB (53257909 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c4e6ca66099ce0bd7d86e3a4446f79489da357b437fe4f0a95c380bca0a5276`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Thu, 09 Apr 2026 12:22:54 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 09 Apr 2026 12:22:54 GMT
ENV LANG=C.UTF-8
# Thu, 09 Apr 2026 12:22:54 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 09 Apr 2026 12:22:54 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Thu, 09 Apr 2026 12:22:54 GMT
ENV PYTHON_VERSION=3.11.15
# Thu, 09 Apr 2026 12:22:54 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Thu, 09 Apr 2026 15:26:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Thu, 09 Apr 2026 15:26:17 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Thu, 09 Apr 2026 15:26:17 GMT
CMD ["python3"]
# Sat, 11 Apr 2026 23:12:42 GMT
ENV HY_VERSION=1.2.0
# Sat, 11 Apr 2026 23:12:42 GMT
ENV HYRULE_VERSION=1.0.1
# Sat, 11 Apr 2026 23:12:42 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sat, 11 Apr 2026 23:12:42 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba3c2fed2ba5fab1d54e686e47aefb417de8e5240c2a472890d543d9f1ae98b2`  
		Last Modified: Thu, 09 Apr 2026 14:05:33 GMT  
		Size: 3.9 MB (3873942 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ca12af81f6793cdec7675d6545b3f07f081340230c381426abee4585f434ee5`  
		Last Modified: Thu, 09 Apr 2026 15:27:30 GMT  
		Size: 14.2 MB (14197190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93a78f5fb527fc2b2d30957515a11dfff54b05c49e16289af3c9d0fabe542221`  
		Last Modified: Thu, 09 Apr 2026 15:27:28 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:579414679fea768df68280fe4bb6ef834a959ac839462e40e6e18e7d9e1eafc5`  
		Last Modified: Sat, 11 Apr 2026 23:13:49 GMT  
		Size: 6.9 MB (6910749 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:ef02fe5cb5a70cccb6d7d781bc99a48109f3774a6d9d8ad880cd44f0d25f7313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2203357 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:986010a0cbf2a8411c699cbfe94ff4916e4ef7c8f3c3be3985802955449e4ba5`

```dockerfile
```

-	Layers:
	-	`sha256:ecb8835e9e72f0478a9e06d8dbf50b6230b9b77e15259070bfe003d2f68eea8f`  
		Last Modified: Sat, 11 Apr 2026 23:13:48 GMT  
		Size: 2.2 MB (2193969 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:576ec9033414a50e360aeac008c26a7ff8f1952e52cae627f4448dc489fd18c5`  
		Last Modified: Sat, 11 Apr 2026 23:13:47 GMT  
		Size: 9.4 KB (9388 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.11` - linux; s390x

```console
$ docker pull hylang@sha256:7a573611ee6cbc7e0479dcf91eaee9891bad4c57d23df0c8601acc458ba871ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.4 MB (52443012 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:13c0f3b2dc351786c5065dbf1677faf230fbb9edd7202e77e543ab0006848ada`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:34:58 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 03:34:58 GMT
ENV LANG=C.UTF-8
# Wed, 22 Apr 2026 03:34:58 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:34:58 GMT
ENV GPG_KEY=A035C8C19219BA821ECEA86B64E628F8D684696D
# Wed, 22 Apr 2026 03:34:58 GMT
ENV PYTHON_VERSION=3.11.15
# Wed, 22 Apr 2026 03:34:58 GMT
ENV PYTHON_SHA256=272179ddd9a2e41a0fc8e42e33dfbdca0b3711aa5abf372d3f2d51543d09b625
# Wed, 22 Apr 2026 03:47:24 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==79.0.1' 		'wheel<0.46' 	; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 03:47:24 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 03:47:24 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 05:01:06 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 05:01:06 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 05:01:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 05:01:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1310e8f745a37e3601da1376e31f1363082251dd895435a51050dc6f1060fa70`  
		Last Modified: Wed, 22 Apr 2026 03:47:37 GMT  
		Size: 1.3 MB (1305544 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8def0d3fb46f63ba58db8115713d548d82920a346a601486fd21c64d856c3c5a`  
		Last Modified: Wed, 22 Apr 2026 03:47:37 GMT  
		Size: 14.4 MB (14367049 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2714d6d78b2a47d861a6da79e3acdead9fd74a4029ed2b7efa894931c21ac8d2`  
		Last Modified: Wed, 22 Apr 2026 03:47:37 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85e739367ce3eb44aeeeeb6b077efd147aee1032febf07f3c7b0e48738844f69`  
		Last Modified: Wed, 22 Apr 2026 05:01:19 GMT  
		Size: 6.9 MB (6929870 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.11` - unknown; unknown

```console
$ docker pull hylang@sha256:b90e4f93065f401d5a0b57d98c2db7ac097ad2344c082dcbbb142ddc3787bfb0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2210766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d29ef9ffc0faabdea4ef82f83230bf887c04692da1a699ca0e60f79871ccb783`

```dockerfile
```

-	Layers:
	-	`sha256:afef197f7d34f301b9aeb753bef0eee9e1f25975140fad2fffb02825d39fe2cd`  
		Last Modified: Wed, 22 Apr 2026 05:01:21 GMT  
		Size: 2.2 MB (2201446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1d102fce9f943452523c358897949d1ecff45db8541c7f7040480efe747dd501`  
		Last Modified: Wed, 22 Apr 2026 05:01:19 GMT  
		Size: 9.3 KB (9320 bytes)  
		MIME: application/vnd.in-toto+json
