## `hylang:1-python3.13`

```console
$ docker pull hylang@sha256:cf21cf5b709ec37c5c24a2b6c7838ae28d9f93d29042aaa88d10bfbcd80aea2b
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 18
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
	-	windows version 10.0.26100.7171; amd64
	-	windows version 10.0.20348.4405; amd64

### `hylang:1-python3.13` - linux; amd64

```console
$ docker pull hylang@sha256:05668486a84d3425d2fd97467a13a6f5fcbd935084f00246003f2ca98da3712e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.3 MB (48332558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee71224734c071ec1b338e19a9d48210c8c063e1752409ce7bab43aa2ea33df1`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1763337600'
# Wed, 03 Dec 2025 01:09:07 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Dec 2025 01:09:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 03 Dec 2025 01:09:07 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 03 Dec 2025 01:09:07 GMT
ENV PYTHON_VERSION=3.13.10
# Wed, 03 Dec 2025 01:09:07 GMT
ENV PYTHON_SHA256=bc673c04375a1a3f0808c27ba8f0411ab811ad390a8740318ccb9c60fad8fd77
# Wed, 03 Dec 2025 01:19:04 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Dec 2025 01:19:04 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Dec 2025 01:19:04 GMT
CMD ["python3"]
# Wed, 03 Dec 2025 02:13:37 GMT
ENV HY_VERSION=1.1.0
# Wed, 03 Dec 2025 02:13:37 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 03 Dec 2025 02:13:37 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 03 Dec 2025 02:13:37 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:0e4bc2bd6656e6e004e3c749af70e5650bac2258243eb0949dea51cb8b7863db`  
		Last Modified: Tue, 18 Nov 2025 02:35:01 GMT  
		Size: 29.8 MB (29776484 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c9e669a16e74d8022e55e0c6239a6b0898b1e7edea584946ed700da9ec3ca479`  
		Last Modified: Wed, 03 Dec 2025 01:19:20 GMT  
		Size: 1.3 MB (1292705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f2ec8236a2e7d9404af3e612305d3206a01b5f4062e924100374ef93dfa602f4`  
		Last Modified: Wed, 03 Dec 2025 01:19:21 GMT  
		Size: 11.8 MB (11786999 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:13a347a59782d57000d9d8f542cae148af6b9027fdce630d1412401301eeca5f`  
		Last Modified: Wed, 03 Dec 2025 01:19:20 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2331ba14d20f8cab6a60fd68b75e0c45093536ceaecec2dd1bdc94a172c0bcf`  
		Last Modified: Wed, 03 Dec 2025 02:13:51 GMT  
		Size: 5.5 MB (5476120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:7b8038b8da6cdd29f6a529f19da00668502826a274526a7e4b13e836991e4bd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffd246ccf881795738df67ab8189336d1960e653fe9e9084abe379e0b9762004`

```dockerfile
```

-	Layers:
	-	`sha256:b7deb9837543b1fb0b58760bd67d74ed2c48f5137f2f39181504752a790ae56e`  
		Last Modified: Wed, 03 Dec 2025 03:19:33 GMT  
		Size: 2.2 MB (2154155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:3a626d56242b7f15107c38d3285861e1cab703de71dfedb9a3c13722902f9cca`  
		Last Modified: Wed, 03 Dec 2025 03:19:34 GMT  
		Size: 9.3 KB (9305 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13` - linux; arm variant v5

```console
$ docker pull hylang@sha256:75d489201a231d391e1ef54965e5df28bac055a656c3613301985101a55c94b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46173204 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b6de64515f6b8f9c06cd38e00b79a8900a654dcd79859168ece9e5ecc849b0a9`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1763337600'
# Wed, 03 Dec 2025 01:26:09 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Dec 2025 01:26:09 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 03 Dec 2025 01:26:09 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 03 Dec 2025 01:26:09 GMT
ENV PYTHON_VERSION=3.13.10
# Wed, 03 Dec 2025 01:26:09 GMT
ENV PYTHON_SHA256=bc673c04375a1a3f0808c27ba8f0411ab811ad390a8740318ccb9c60fad8fd77
# Wed, 03 Dec 2025 01:45:48 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Dec 2025 01:45:48 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Dec 2025 01:45:48 GMT
CMD ["python3"]
# Wed, 03 Dec 2025 02:12:24 GMT
ENV HY_VERSION=1.1.0
# Wed, 03 Dec 2025 02:12:24 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 03 Dec 2025 02:12:24 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 03 Dec 2025 02:12:24 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:a1c0783a82710a65871102568a0ace23c3dd0f89dba1af72c3290089eac458f2`  
		Last Modified: Tue, 18 Nov 2025 01:14:09 GMT  
		Size: 27.9 MB (27944147 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b45723e5e084d85ff1adc01efd782427737478c5363573c1977983ca90932a1b`  
		Last Modified: Wed, 03 Dec 2025 01:46:03 GMT  
		Size: 1.3 MB (1275862 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3fbdf373c882a0940e7f5c70180031d461378667a2e7fffad9f06c85b2cdae75`  
		Last Modified: Wed, 03 Dec 2025 01:46:03 GMT  
		Size: 11.5 MB (11476463 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d18d6e6ef605fdbb9d2b8a202171801cc8d2955746a245ba275903fc3940d00`  
		Last Modified: Wed, 03 Dec 2025 01:46:03 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0edeef65c29201bc494f995cdb15fb7192b513c665fa9941a84d466759395f4`  
		Last Modified: Wed, 03 Dec 2025 02:12:38 GMT  
		Size: 5.5 MB (5476481 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:0e061c4d87d1e513e532d510d54f08e26844460d559403701b92c1cf28ed52b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2166573 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d53c83baef17cc3b0536962cf4c2772d661e2ffc66293a89429c39ad63f2274`

```dockerfile
```

-	Layers:
	-	`sha256:b0981a72e46866a9d4a70de5f69f5035c9a2aa3d5354f6e3df6a0076738518da`  
		Last Modified: Wed, 03 Dec 2025 03:19:38 GMT  
		Size: 2.2 MB (2157156 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8bea29c5198040a22477260244aceb36ac810108faa6d25ebc77c77131929bf6`  
		Last Modified: Wed, 03 Dec 2025 03:19:39 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13` - linux; arm variant v7

```console
$ docker pull hylang@sha256:5db9909c7a84f9d1b8488290ee49eabe9b6fde799bf6a285fafb11af044a89b4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44134303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a0390a4ea110a21269731728a2cd4947a1ff373b358ff83b4993ef7c537b74dc`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1763337600'
# Wed, 03 Dec 2025 01:07:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Dec 2025 01:07:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 03 Dec 2025 01:07:36 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 03 Dec 2025 01:07:36 GMT
ENV PYTHON_VERSION=3.13.10
# Wed, 03 Dec 2025 01:07:36 GMT
ENV PYTHON_SHA256=bc673c04375a1a3f0808c27ba8f0411ab811ad390a8740318ccb9c60fad8fd77
# Wed, 03 Dec 2025 01:25:56 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Dec 2025 01:25:56 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Dec 2025 01:25:56 GMT
CMD ["python3"]
# Wed, 03 Dec 2025 02:12:51 GMT
ENV HY_VERSION=1.1.0
# Wed, 03 Dec 2025 02:12:51 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 03 Dec 2025 02:12:51 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 03 Dec 2025 02:12:51 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8202667160e65087c34b2510837039e29b29936f1b75fc737a33219ae9c06ec0`  
		Last Modified: Tue, 18 Nov 2025 01:14:24 GMT  
		Size: 26.2 MB (26209960 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8c35d541953cfb3278d245bd21902f49f9031b5b89f1e64b8b2b7c9c8049939c`  
		Last Modified: Wed, 03 Dec 2025 01:26:11 GMT  
		Size: 1.2 MB (1248469 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e10394031a9c8fb5a446f49f986836e0df44ae6edf6d7b5a2a696945fade8ac8`  
		Last Modified: Wed, 03 Dec 2025 01:26:12 GMT  
		Size: 11.2 MB (11199244 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:63885240ebf6eafb58caf0a5130b0f5845260c5652f3cad411a9ea24c44e670d`  
		Last Modified: Wed, 03 Dec 2025 01:26:11 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2d334b572c784607ac4e9afcc42799382c11730d66c8a6181752db0f2228efc9`  
		Last Modified: Wed, 03 Dec 2025 02:13:13 GMT  
		Size: 5.5 MB (5476380 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:e5eb822d287b198fc4297e84501bd662d04d869828963dbbc5e76f1d831520ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165026 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3f47acf04ad755afd97c47efc9444f519dbc3423348b9ba60f3747b7619bdfe0`

```dockerfile
```

-	Layers:
	-	`sha256:a7e4f46350fd058584f5a1eb37758837401c37f8b1b7f4dc6142e8ef3aaf8033`  
		Last Modified: Wed, 03 Dec 2025 03:19:42 GMT  
		Size: 2.2 MB (2155609 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f41219d2bb44d307b660b13ced0b37065145f7678fb5b7037b39d0dc5ef43e9d`  
		Last Modified: Wed, 03 Dec 2025 03:19:43 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:8d0471af9818c607a9b7cc6a9656298ffcbcd16827d7764da408452553d7d192
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48604218 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a81cc9aa78d7c8569b09f1b0dcd42d5620e0f27885813c1d64909328d3e730`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1763337600'
# Wed, 03 Dec 2025 01:07:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Dec 2025 01:07:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 03 Dec 2025 01:07:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 03 Dec 2025 01:07:05 GMT
ENV PYTHON_VERSION=3.13.10
# Wed, 03 Dec 2025 01:07:05 GMT
ENV PYTHON_SHA256=bc673c04375a1a3f0808c27ba8f0411ab811ad390a8740318ccb9c60fad8fd77
# Wed, 03 Dec 2025 01:19:32 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Dec 2025 01:19:32 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Dec 2025 01:19:32 GMT
CMD ["python3"]
# Wed, 03 Dec 2025 02:11:17 GMT
ENV HY_VERSION=1.1.0
# Wed, 03 Dec 2025 02:11:17 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 03 Dec 2025 02:11:17 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 03 Dec 2025 02:11:17 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b89cf3ec7a3ed3a58015edd6724125187f0d284147e09b5739b511c74222b2a4`  
		Last Modified: Tue, 18 Nov 2025 01:13:26 GMT  
		Size: 30.1 MB (30138610 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7d4028a08380bc1acf83f7fe0d41346477c5e5980c165b62a9e99c5bba009756`  
		Last Modified: Wed, 03 Dec 2025 01:19:46 GMT  
		Size: 1.3 MB (1273721 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e3b614126b6af7499a0dca982baee8813f0c344b69204c587ac76eed7770b82`  
		Last Modified: Wed, 03 Dec 2025 01:19:47 GMT  
		Size: 11.7 MB (11715530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77e53a94adc6d36c5ae601c1ec53447f20ab3e139fb9b65a908ff9ea9cb98c5c`  
		Last Modified: Wed, 03 Dec 2025 01:19:46 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3edf3d667738dbdc007078336e9d12a30d386a6156e5bab4d19f782261b3bb30`  
		Last Modified: Wed, 03 Dec 2025 02:11:32 GMT  
		Size: 5.5 MB (5476106 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:531b7c0b07d2973f12ba582cf4ffd0e0e99d50a86e4b2101c34963f9758a9d6d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee45c6041cfa61b2498fda065df855cf4b7357f4c8122e7b59785c377bd64a9`

```dockerfile
```

-	Layers:
	-	`sha256:cb2f5bf27182c68ab2cef9c020071a2c3fc264a1415d32fa04f949d12ed1020b`  
		Last Modified: Wed, 03 Dec 2025 03:19:47 GMT  
		Size: 2.2 MB (2154469 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:434e7b112bb11a0e4cc4a359b0f2aeb4658b2b1bb74d9f1f1e0ef3ab786adaca`  
		Last Modified: Wed, 03 Dec 2025 03:19:48 GMT  
		Size: 9.5 KB (9457 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13` - linux; 386

```console
$ docker pull hylang@sha256:9e8097fcb614967da5d81009181eb27d9595cbf72fe956e6ebf5384780a42e1d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49963603 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3549222c016e3c6694080e0e44244878f7a9a59c7a8d8cbf972db465b8d90969`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1763337600'
# Wed, 03 Dec 2025 01:04:47 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Dec 2025 01:04:47 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 03 Dec 2025 01:04:47 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 03 Dec 2025 01:04:47 GMT
ENV PYTHON_VERSION=3.13.10
# Wed, 03 Dec 2025 01:04:47 GMT
ENV PYTHON_SHA256=bc673c04375a1a3f0808c27ba8f0411ab811ad390a8740318ccb9c60fad8fd77
# Wed, 03 Dec 2025 01:15:12 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Dec 2025 01:15:12 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Dec 2025 01:15:12 GMT
CMD ["python3"]
# Wed, 03 Dec 2025 02:12:14 GMT
ENV HY_VERSION=1.1.0
# Wed, 03 Dec 2025 02:12:14 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 03 Dec 2025 02:12:14 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 03 Dec 2025 02:12:14 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:8fdd29f45eb19adab28e642f5b411c2aac45db9e7dfc1ab412acdcf1365af598`  
		Last Modified: Tue, 18 Nov 2025 01:13:49 GMT  
		Size: 31.3 MB (31293068 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a94add4ca6bc569b05bb013a8f660d605254177c7530c382266054f240c3defc`  
		Last Modified: Wed, 03 Dec 2025 01:15:25 GMT  
		Size: 1.3 MB (1296739 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fd89e296bb97775c535239210204499f1e14671fe14748f63ec8ba2a368113f6`  
		Last Modified: Wed, 03 Dec 2025 01:15:26 GMT  
		Size: 11.9 MB (11897337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4edaf78108015deeaec88a9e0f374a9891c2b5f52977ed39fec34a2096dc3687`  
		Last Modified: Wed, 03 Dec 2025 01:15:25 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:af66955cd73ea774bff768d9e215c64cad641d08dd8b3ae96fef0760017b9f23`  
		Last Modified: Wed, 03 Dec 2025 02:12:28 GMT  
		Size: 5.5 MB (5476210 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:f8a5d7dcc08c6d5bb46ea62f3b9f9da25926430db68af41e3afef662be30cf2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2160569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:afe3a7dce579deebf34ffd12223a8320bb75b577b4550551a37f40f337596df7`

```dockerfile
```

-	Layers:
	-	`sha256:137571145dbc5a93b65d0a24b1853bf95f5091b4894706d5a0af50324df839c7`  
		Last Modified: Wed, 03 Dec 2025 03:19:52 GMT  
		Size: 2.2 MB (2151316 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b56a614928425efdad426c97effbae4cb1cc30946a21d77d491a494544eee537`  
		Last Modified: Wed, 03 Dec 2025 03:19:53 GMT  
		Size: 9.3 KB (9253 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13` - linux; ppc64le

```console
$ docker pull hylang@sha256:2a8eaa9cdcb5d227d32ce6df5d043e0a1dc4b835e449ea1cc4005fc5bee16770
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52587462 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ada4c0999374c01d1d189426ee4521930b5e19a6619a12c4e94bf7e59899ee0`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1763337600'
# Tue, 18 Nov 2025 18:24:03 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 18 Nov 2025 18:24:03 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 18 Nov 2025 18:24:03 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 18 Nov 2025 18:24:03 GMT
ENV PYTHON_VERSION=3.13.10
# Tue, 18 Nov 2025 18:24:03 GMT
ENV PYTHON_SHA256=bc673c04375a1a3f0808c27ba8f0411ab811ad390a8740318ccb9c60fad8fd77
# Wed, 03 Dec 2025 02:21:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Dec 2025 02:21:11 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Dec 2025 02:21:11 GMT
CMD ["python3"]
# Wed, 03 Dec 2025 04:16:59 GMT
ENV HY_VERSION=1.1.0
# Wed, 03 Dec 2025 04:16:59 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 03 Dec 2025 04:16:59 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 03 Dec 2025 04:16:59 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:38a4f720a0e1dc899707e3aaab397e56da721bf9b35e36e797b59d51b46ec989`  
		Last Modified: Tue, 18 Nov 2025 12:56:45 GMT  
		Size: 33.6 MB (33596858 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbcef8c770c0643674380f6787c6d13d11479fccd2e5a398f9584e6028aacd51`  
		Last Modified: Tue, 18 Nov 2025 18:32:41 GMT  
		Size: 1.3 MB (1320551 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e5ba73842844a2093604b2c1c7c13286ab6e591bf64d75dc659009dc6db49b3f`  
		Last Modified: Wed, 03 Dec 2025 02:21:40 GMT  
		Size: 12.2 MB (12193705 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dad451058cfca4deaac729573719d4d32fbdd4970c00fdd96a40fa059fc47248`  
		Last Modified: Wed, 03 Dec 2025 02:21:38 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d0e6c43e0daf81c1e16f7c1ce116932d4e6168ff1b9f346b0a7b80d4688cccba`  
		Last Modified: Wed, 03 Dec 2025 04:17:35 GMT  
		Size: 5.5 MB (5476097 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:5a2b96e4b21e15d3cd3d11811fda672ea30c1ab276c0d3c542318f6b1afa41e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2167119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a93e5adb8d854ce639d310b85bbfeed499a4e316265f9b536aeed51be50510f9`

```dockerfile
```

-	Layers:
	-	`sha256:eb2c7755efb53db8cb4ce5e3bdce7e60c23ec7203a43b9adfd93673403dac8c4`  
		Last Modified: Wed, 03 Dec 2025 06:18:27 GMT  
		Size: 2.2 MB (2157746 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90c84f37c700bd38bcb44867519f83b459e710fd8befab6dad91535e9bfcd88e`  
		Last Modified: Wed, 03 Dec 2025 06:18:28 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13` - linux; riscv64

```console
$ docker pull hylang@sha256:febd0e9819ddae7935b121682855d22687ce5317921183179fecc61cf04d0ecc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.8 MB (46793885 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ae9387525736e92168a0683ee6b57b50e3f1ebed788d3d56a47fb6e857a8255f`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1763337600'
# Thu, 20 Nov 2025 05:15:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Thu, 20 Nov 2025 05:15:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Thu, 20 Nov 2025 05:15:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Thu, 20 Nov 2025 05:15:00 GMT
ENV PYTHON_VERSION=3.13.10
# Thu, 20 Nov 2025 05:15:00 GMT
ENV PYTHON_SHA256=bc673c04375a1a3f0808c27ba8f0411ab811ad390a8740318ccb9c60fad8fd77
# Wed, 03 Dec 2025 09:28:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Dec 2025 09:28:36 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Dec 2025 09:28:36 GMT
CMD ["python3"]
# Wed, 03 Dec 2025 10:58:21 GMT
ENV HY_VERSION=1.1.0
# Wed, 03 Dec 2025 10:58:21 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 03 Dec 2025 10:58:21 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 03 Dec 2025 10:58:21 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:4522bc4acaa9a6a70c3e44b2e1942464457bbf2cb6f2df1cd45c06cf9b8b92c3`  
		Last Modified: Tue, 18 Nov 2025 01:46:31 GMT  
		Size: 28.3 MB (28273126 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca3c6622d839fd6b48607097e5c05e3cd8aa90969f85bdcac54be852f3e3e2d`  
		Last Modified: Thu, 20 Nov 2025 07:04:33 GMT  
		Size: 1.3 MB (1259913 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:01a7ada8fb20f2381829136d7a2ec631daa3c5c3bd0233d3edb3886d88096a80`  
		Last Modified: Wed, 03 Dec 2025 09:29:51 GMT  
		Size: 11.8 MB (11783300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d9eb10d8dcd50968212fed0f193cdbae9e1e73fed1b064904cf36f98afe0be83`  
		Last Modified: Wed, 03 Dec 2025 09:29:50 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ea07c73c55d99a513fed88a69537b3c4e694d53aa570bf74ae7dda78a45624ae`  
		Last Modified: Wed, 03 Dec 2025 10:59:27 GMT  
		Size: 5.5 MB (5477296 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:c0a8a450da0f663f12ecfda4866a197f020c5fd053691f3d3de0126129cad725
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157490 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f112799f3885e38255e65170d73caca65ee08d34eb098814e94c3723806999a6`

```dockerfile
```

-	Layers:
	-	`sha256:8b785fbd06f805ef7b07aaae213d82237800bef091bb1bc5636b526d2a05d358`  
		Last Modified: Wed, 03 Dec 2025 12:18:26 GMT  
		Size: 2.1 MB (2148117 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e2ff45759f663cfb775b85cb12e51afbee334264ef9e9439ffe624efd30756d9`  
		Last Modified: Wed, 03 Dec 2025 12:18:27 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13` - linux; s390x

```console
$ docker pull hylang@sha256:9da7f20a2a9d5b45479df346b804dfbc51a50fb5242222b8d5c32b6246311f00
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48453755 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a7fdedf35cbc31b0e5dae4c65ca9b8ef755c03cd4070e88e9a8807ce0e9d321`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1763337600'
# Wed, 03 Dec 2025 01:04:16 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 03 Dec 2025 01:04:16 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 03 Dec 2025 01:04:16 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 03 Dec 2025 01:04:16 GMT
ENV PYTHON_VERSION=3.13.10
# Wed, 03 Dec 2025 01:04:16 GMT
ENV PYTHON_SHA256=bc673c04375a1a3f0808c27ba8f0411ab811ad390a8740318ccb9c60fad8fd77
# Wed, 03 Dec 2025 01:46:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 03 Dec 2025 01:46:10 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 03 Dec 2025 01:46:10 GMT
CMD ["python3"]
# Wed, 03 Dec 2025 02:11:16 GMT
ENV HY_VERSION=1.1.0
# Wed, 03 Dec 2025 02:11:16 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 03 Dec 2025 02:11:16 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 03 Dec 2025 02:11:16 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3063905a9d3db554a6c1d839c1212baff57798d644d5b0d198eef84afd107192`  
		Last Modified: Tue, 18 Nov 2025 01:13:05 GMT  
		Size: 29.8 MB (29834372 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fca2651edd04eb46075baeedade45b6950ca3a205479849b4d9e1e5d179f5086`  
		Last Modified: Wed, 03 Dec 2025 01:19:30 GMT  
		Size: 1.3 MB (1305176 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4eebfc091b271b18e0a36aa860081d090bcc95bf54734371414a09fd57c60477`  
		Last Modified: Wed, 03 Dec 2025 01:46:31 GMT  
		Size: 11.8 MB (11837243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0be34d6b05821a62fe25814e02a3fb2d481328c157b57bcc6e4c0b0df82799ab`  
		Last Modified: Wed, 03 Dec 2025 01:46:30 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:16e15eb8d9b86dca9b86aa78d96f3a81e96556e0d3b091324633fdcdd9a9e916`  
		Last Modified: Wed, 03 Dec 2025 02:11:46 GMT  
		Size: 5.5 MB (5476713 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:eee4d9c03c189c896493577147edb99c213db757b9923171839e230b149f8054
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2164899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bded6821ca1b7d21784adb247e214db3826b4d4e4c4b73b9e1e01a25c022cff9`

```dockerfile
```

-	Layers:
	-	`sha256:165ea62b3438dea8c9c5110b11ed24e6f87418eac13c3bb5fa51888599f61625`  
		Last Modified: Wed, 03 Dec 2025 03:20:04 GMT  
		Size: 2.2 MB (2155594 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e4c868229be723bb13cb45f414c21774b6e4a99a1592210f941462b97b6b66a8`  
		Last Modified: Wed, 03 Dec 2025 03:20:04 GMT  
		Size: 9.3 KB (9305 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:1-python3.13` - windows version 10.0.26100.7171; amd64

```console
$ docker pull hylang@sha256:3c87fb3c0047529e45ac99f506eadbdc4581a8320560ff75a2eb249fbcb0546f
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.3 GB (3302719131 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2937ca095266cd706f7ad8caaffbbb81fc39ce0b31fc449e9ce694423925741f`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 08 Dec 2024 22:41:37 GMT
RUN Apply image 10.0.26100.2605
# Sun, 09 Nov 2025 10:25:55 GMT
RUN Install update 10.0.26100.7171
# Wed, 03 Dec 2025 01:08:50 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 01:08:52 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 03 Dec 2025 01:08:52 GMT
ENV PYTHON_VERSION=3.13.10
# Wed, 03 Dec 2025 01:08:53 GMT
ENV PYTHON_SHA256=ab30cd76655c6c91243b4f4d5a8499020f6503aa58e92b3e2e94ae4af7353257
# Wed, 03 Dec 2025 01:10:47 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 03 Dec 2025 01:10:47 GMT
CMD ["python"]
# Wed, 03 Dec 2025 02:13:34 GMT
ENV HY_VERSION=1.1.0
# Wed, 03 Dec 2025 02:13:35 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 03 Dec 2025 02:14:06 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 03 Dec 2025 02:14:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:1317fe15185685e9cd27f7542cd96f4847343401288a8b6798273a4ac60844eb`  
		Last Modified: Mon, 08 Dec 2025 10:02:12 GMT  
		Size: 2.2 GB (2215307110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a84ef3b04f81727036fe8b401efc70b6979844e2b78bdf09aa1b68b7ef4edf63`  
		Last Modified: Tue, 11 Nov 2025 21:02:47 GMT  
		Size: 1.0 GB (1020148600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc79475b321f3f485f171323886acb82a816c3ca538395f80d4f20cc7d23978e`  
		Last Modified: Wed, 03 Dec 2025 01:25:20 GMT  
		Size: 1.3 KB (1349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56c820b1100bd9cd0766e6c92e5ce9d58649e89891538731b04492f07df33cba`  
		Last Modified: Wed, 03 Dec 2025 01:25:18 GMT  
		Size: 1.3 KB (1314 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791801f468282f6fdee8125777a9cde8a86850e23b6d9da874f0e7ca19283600`  
		Last Modified: Wed, 03 Dec 2025 01:25:19 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83b374fa80ecbd3d52db3cf2c01e239bf07e2b64c9f5ef485795031b0b3181e1`  
		Last Modified: Wed, 03 Dec 2025 01:25:19 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a348876e947f4a980da4f96cb2d23ee574fdeab878abf635616422689c9421`  
		Last Modified: Wed, 03 Dec 2025 01:25:36 GMT  
		Size: 58.8 MB (58789330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:009e6fdde1baeec39614d9adec7183acc94c93666c4ca6b4361eba9bc4208296`  
		Last Modified: Wed, 03 Dec 2025 01:25:20 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af48061016506245c2b05d9e012d18b10a69d252078912355e570c5ea6ce769a`  
		Last Modified: Wed, 03 Dec 2025 02:14:21 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb71ce64fcf283646731aee3b0cc94bf9923ae9a3f7868f7f3a320fc00c35891`  
		Last Modified: Wed, 03 Dec 2025 02:14:20 GMT  
		Size: 1.3 KB (1342 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:539432d8a2d9bd24823cbfdba5b1a8ca92008c95060c3a3b30a6aa2c087cfa66`  
		Last Modified: Wed, 03 Dec 2025 02:14:21 GMT  
		Size: 8.5 MB (8463506 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e20e383cc2db01baf3ab9d6a4ee15c5928755944d61231757f2830a4cc656b`  
		Last Modified: Wed, 03 Dec 2025 02:14:20 GMT  
		Size: 1.3 KB (1312 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:1-python3.13` - windows version 10.0.20348.4405; amd64

```console
$ docker pull hylang@sha256:98029158f11bc9284efc939ee74ba4e1bc39a7ba61233efae5bb44b688467260
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **1.8 GB (1837269961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2f1e92814b96efc842114226b2647cdefdeba41b056ab45ef362c5ff5a6c060`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Wed, 05 Nov 2025 05:39:13 GMT
RUN Install update 10.0.20348.4405
# Wed, 03 Dec 2025 01:05:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Wed, 03 Dec 2025 01:05:27 GMT
ENV PYTHONIOENCODING=UTF-8
# Wed, 03 Dec 2025 01:12:33 GMT
ENV PYTHON_VERSION=3.13.10
# Wed, 03 Dec 2025 01:12:33 GMT
ENV PYTHON_SHA256=ab30cd76655c6c91243b4f4d5a8499020f6503aa58e92b3e2e94ae4af7353257
# Wed, 03 Dec 2025 01:13:21 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Wed, 03 Dec 2025 01:13:21 GMT
CMD ["python"]
# Wed, 03 Dec 2025 02:11:54 GMT
ENV HY_VERSION=1.1.0
# Wed, 03 Dec 2025 02:11:54 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 03 Dec 2025 02:12:22 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Wed, 03 Dec 2025 02:12:23 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3cc21a1b754848d23f00aa65cb94ec34c9a5dc6028b3aada42039c824738d02f`  
		Last Modified: Tue, 14 Oct 2025 19:03:59 GMT  
		Size: 1.5 GB (1489019076 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a26269efcb0f33c920b21f98d305592e7310bbe548291a16043e48a0c1feba5`  
		Last Modified: Tue, 11 Nov 2025 20:47:36 GMT  
		Size: 280.9 MB (280942415 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c27be210d6833cdc827bfc15972f5d728f0d871b50e3aa17e152f86594cb31ba`  
		Last Modified: Wed, 03 Dec 2025 01:12:24 GMT  
		Size: 1.3 KB (1329 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14fddf0b287656bd22c11db1941d0dac9b8298027d4deeb2f20f0c2fc07c4bd`  
		Last Modified: Wed, 03 Dec 2025 01:12:24 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d2eacf44e4e54f3d9ec14d16d76ef0c0d752f89b4ca04cc0ec42cc8cd84cb00`  
		Last Modified: Wed, 03 Dec 2025 01:13:39 GMT  
		Size: 1.3 KB (1318 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8b8730b5eef57309a6afaeca8053b6b0cdc8074a2cbf4ff749b7cc85fe9ab31`  
		Last Modified: Wed, 03 Dec 2025 01:13:39 GMT  
		Size: 1.3 KB (1308 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c387d952b55adcd6e5d64f015324d631594cc53f9ffee69b9d5c26a1e24fb59`  
		Last Modified: Wed, 03 Dec 2025 02:11:45 GMT  
		Size: 58.8 MB (58847831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce4e2c4fd07487e9a5bf794f25dda999ac9e7f9fa6e8544a47216e752eff51b4`  
		Last Modified: Wed, 03 Dec 2025 01:13:39 GMT  
		Size: 1.3 KB (1334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae28686b6584eaa85be4b90e811a11c2bc33bb8135bd37c48765ab09d34b4395`  
		Last Modified: Wed, 03 Dec 2025 02:12:36 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cad73e22d6c2f173bf5191b4b7a8643bb637b956ce812006403663291f3a20`  
		Last Modified: Wed, 03 Dec 2025 02:12:36 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2993e999f5e9a921857694059bc0f7d005659df2feeea92b6fac9bb989e15482`  
		Last Modified: Wed, 03 Dec 2025 02:12:37 GMT  
		Size: 8.5 MB (8450161 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6ce7d8dfac89eff549fc4a912d186b58212a073fc058e72a6452398887c62456`  
		Last Modified: Wed, 03 Dec 2025 02:12:36 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
