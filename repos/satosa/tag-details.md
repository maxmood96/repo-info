<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `satosa`

-	[`satosa:8`](#satosa8)
-	[`satosa:8-alpine`](#satosa8-alpine)
-	[`satosa:8-alpine3.22`](#satosa8-alpine322)
-	[`satosa:8-bookworm`](#satosa8-bookworm)
-	[`satosa:8.5`](#satosa85)
-	[`satosa:8.5-alpine`](#satosa85-alpine)
-	[`satosa:8.5-alpine3.22`](#satosa85-alpine322)
-	[`satosa:8.5-bookworm`](#satosa85-bookworm)
-	[`satosa:8.5.1`](#satosa851)
-	[`satosa:8.5.1-alpine`](#satosa851-alpine)
-	[`satosa:8.5.1-alpine3.22`](#satosa851-alpine322)
-	[`satosa:8.5.1-bookworm`](#satosa851-bookworm)
-	[`satosa:alpine`](#satosaalpine)
-	[`satosa:alpine3.22`](#satosaalpine322)
-	[`satosa:bookworm`](#satosabookworm)
-	[`satosa:latest`](#satosalatest)

## `satosa:8`

```console
$ docker pull satosa@sha256:7c907d50804dc6ecbe36c4faa8d54754f386ef005a1e82442a35dcd34b992995
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8` - linux; amd64

```console
$ docker pull satosa@sha256:5655dae76305b96869065034d848eb92090aaa0c388fb6ec10c523acfe64fc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92457715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26bb17950e679e22cf69f7c9e1538ffa56c520b298527c2a9eff0b77a4c6c47c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:59:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:59:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PYTHON_VERSION=3.13.14
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PYTHON_SHA256=639e43243c620a308f968213df9e00f2f8f62332f7adbaa7a7eeb9783057c690
# Wed, 24 Jun 2026 02:10:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 24 Jun 2026 02:10:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 24 Jun 2026 02:10:55 GMT
CMD ["python3"]
# Wed, 24 Jun 2026 02:43:04 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Wed, 24 Jun 2026 02:43:52 GMT
ENV SATOSA_VERSION=8.5.1
# Wed, 24 Jun 2026 02:43:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
WORKDIR /etc/satosa
# Wed, 24 Jun 2026 02:43:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:43:53 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 24 Jun 2026 02:43:53 GMT
USER satosa:satosa
# Wed, 24 Jun 2026 02:43:53 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e26001d5620dfc2698f3a683c497e1cabdcc4757f4ca4ff70e33cb36057df02`  
		Last Modified: Wed, 24 Jun 2026 02:11:04 GMT  
		Size: 3.5 MB (3520812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90b26812a028bfa582bede756e645cf91fe9d05f2991b0862d719a003cce5ed`  
		Last Modified: Wed, 24 Jun 2026 02:11:05 GMT  
		Size: 12.6 MB (12570253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d229a71b9e515d634cb7f17b8bfe71586ed1282edbcfb81faaca1aebd0ed028b`  
		Last Modified: Wed, 24 Jun 2026 02:11:04 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0d169f435410c8068b61f1f86441b66ba63e5b017eb2a7db41dcdb1f48d007`  
		Last Modified: Wed, 24 Jun 2026 02:44:05 GMT  
		Size: 21.6 MB (21598611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5723dc18369d76c11887e05369a995342ca50992ecf72a7d14b766a7164e896b`  
		Last Modified: Wed, 24 Jun 2026 02:44:05 GMT  
		Size: 26.5 MB (26517606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca12e5f4cad01e654ee761cf49288d7dd440d9ac1bdf2cab826b64a9090213c9`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 10.4 KB (10437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1594679d03fab51ca435b90ed827eb2b73e41cfea3f269fafee6cdafb6f6eac`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 2.1 KB (2074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8` - unknown; unknown

```console
$ docker pull satosa@sha256:5f98c4b2665f69dcf052d4ab597ff30427c3dc5edd3604a267e79edfca34634e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8b97b41f3b02471095632cc69e5647bbe7f5be1499d8512bd4e4254e0447d3`

```dockerfile
```

-	Layers:
	-	`sha256:9e9a9262540a6671d38ce01f5f543fd48f4096a8b3339ec72d7401b0ed450fc2`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 2.7 MB (2704660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0fe9e7f73f935ef31b3b3d1f07c9a4794a74a0447d0153ddc5dbfaa4e71a7ce`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 22.3 KB (22266 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e18cfffa9074424656f99d0444260f631f2a354659ba025c73a84abd42bb8226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91562388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab281fe3962b4af7fcd4f4cd9ef08844ba62e49b65cb1c4e070aad6a834c5a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:02:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:02:38 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PYTHON_VERSION=3.13.14
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PYTHON_SHA256=639e43243c620a308f968213df9e00f2f8f62332f7adbaa7a7eeb9783057c690
# Wed, 24 Jun 2026 02:16:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 24 Jun 2026 02:16:22 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 24 Jun 2026 02:16:22 GMT
CMD ["python3"]
# Wed, 24 Jun 2026 03:23:47 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Wed, 24 Jun 2026 03:24:34 GMT
ENV SATOSA_VERSION=8.5.1
# Wed, 24 Jun 2026 03:24:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
WORKDIR /etc/satosa
# Wed, 24 Jun 2026 03:24:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:24:35 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 24 Jun 2026 03:24:35 GMT
USER satosa:satosa
# Wed, 24 Jun 2026 03:24:35 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e03177a4ba5d2a105c80da4d791b999a2c0d8592218bf604937099767dce4`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 3.4 MB (3352640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8112ec847c4c51cc9e087e72458f63645ee819d8f7f5b00b18c78d8b45457b`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 12.5 MB (12472943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4140d7667663a40213044b01b7f98a453c79fa59784459232580dd4608afcdd`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d1353c5acbe10355ef9cfcf93a6db67a29c03e660d0ac1af30cf1e72cb8542`  
		Last Modified: Wed, 24 Jun 2026 03:24:46 GMT  
		Size: 21.5 MB (21451922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25368aad8a3d30bf1e9c31630225e8631f0de92e424d60e2c58e26eaecee3f51`  
		Last Modified: Wed, 24 Jun 2026 03:24:46 GMT  
		Size: 26.1 MB (26149666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9ca620b6bee0b901297e863ac4357db955c3bd67ff01aa0f4e618d6de2ccaf`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 10.4 KB (10442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cccdfcb5100f94f01bec9af80fe397d740ea6bcb32e131db97cbacce527834`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 2.1 KB (2075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8` - unknown; unknown

```console
$ docker pull satosa@sha256:cfd648ffe65a01b96b5584990dc074c7a1f1e961a386dcc8446c0372e1ecfac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2727434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76688f62ede38ed94bd9711fb0cfcbfd6e7ab709ab504ef46889c172ef57faf7`

```dockerfile
```

-	Layers:
	-	`sha256:8734d5cd42d0cfe8c59fc9680272074d7b1f4b5ed314e46bbe0b8656d6fed5d7`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 2.7 MB (2704986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f33959acb229dcf2327a93d12ecb800afb9fe3dafc7ab97bba3371cc15ab1a45`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 22.4 KB (22448 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8-alpine`

```console
$ docker pull satosa@sha256:635c3bd8a7b1e62eb8f505c7640cf1bdf930cfac6ab7926573baed9958354ba7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8-alpine` - linux; amd64

```console
$ docker pull satosa@sha256:e64adbaaaed0ecd676889a71476ffb657b6c96e99ea168202a836e9338daf5da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49591032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245adc8cf01a5f66ff2284be88e273d4841d80dc1a1c3e904abc104fd609db9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:30:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:30:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 00:36:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:36:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:36:29 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:14:35 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
ENV SATOSA_VERSION=8.5.1
# Fri, 17 Apr 2026 01:14:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
WORKDIR /etc/satosa
# Fri, 17 Apr 2026 01:14:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:14:56 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 17 Apr 2026 01:14:56 GMT
USER satosa:satosa
# Fri, 17 Apr 2026 01:14:56 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df730813d20b0cb8062fb76ce24dc8fc02961ddd625cd6be3c86a0bc4dde8e56`  
		Last Modified: Fri, 17 Apr 2026 00:36:36 GMT  
		Size: 455.0 KB (454972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe818d7ffa27044c9667e73b415f9ae4c37a5d5d78c0cc4462423ded6b373a5`  
		Last Modified: Fri, 17 Apr 2026 00:36:36 GMT  
		Size: 12.5 MB (12472237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf71161b7b0782d25e76411844b95d7c41c91a90891d50df620e89e99fe18b8`  
		Last Modified: Fri, 17 Apr 2026 00:36:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8d9dc3a6733c4a32030cfa81ae0f31e2968fd1b1097d14d360df5e799d9bc9`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 6.7 MB (6744550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77426ee3fb08a0c6baa34b9704abd4f7fd61339c643f0a43c04b0f4962c07a93`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 26.1 MB (26098299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92f5d482e5e64b0b81c6a55dbb5a3cda363eb3e4979e4288755506f6d617458`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 10.4 KB (10431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7c65b6d4cd12b071c97dca761ea5c539c9402480aa6da6b50e82cfcf0306cc`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 2.1 KB (2076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:f995f2aa2d9c5f4f425e5c76b9a84833ab0168d8777212eb0fd0a6454b896e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.5 KB (805473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2e4d3867615dc4bcf34d3615fffd2782c10a5980b2e89b2cfc5acf53027d74`

```dockerfile
```

-	Layers:
	-	`sha256:66040d43ba1ffe7cbed77eaa5a76d1f221c9253d108cf118fc8d85ddd831614c`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 782.5 KB (782513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b2a4e9a01427f7604acf929bf5d708369cff7bc24cfa7d0c012c8589bc32450`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 23.0 KB (22960 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8-alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:ad74b8922ba82d4cc6b9d562384bc8e5cc6d53864ea2bc66078696d7397cdafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49501857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34acd28bc2bbd82e5e73375c4a90f7169c780bc2d0e6c41ca9e0c5d4f74b7ade`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:32:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:32:45 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 00:39:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:39:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:39:34 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:38:03 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Fri, 17 Apr 2026 01:38:26 GMT
ENV SATOSA_VERSION=8.5.1
# Fri, 17 Apr 2026 01:38:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
WORKDIR /etc/satosa
# Fri, 17 Apr 2026 01:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:38:27 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 17 Apr 2026 01:38:27 GMT
USER satosa:satosa
# Fri, 17 Apr 2026 01:38:27 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcaff11adfb133e9e9320abbc299cc834c1403c253c3f7ea4ccaab6d6932fa60`  
		Last Modified: Fri, 17 Apr 2026 00:39:41 GMT  
		Size: 457.3 KB (457313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53736ed35b86baa4c031683ba780c3f739bb4f9961f7885b78af60392fbe5836`  
		Last Modified: Fri, 17 Apr 2026 00:39:41 GMT  
		Size: 12.5 MB (12486525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2c305c7606c8ddaf30bedaeaa4c18783036b29fbe2d07fc7eda11e7d1ddc34`  
		Last Modified: Fri, 17 Apr 2026 00:39:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b6dc3325f307fb75ee4f9d98da6f233aeecb5d14c89aed997bf4e4a7779b13`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 6.7 MB (6722767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff746c3bcb9c24e2fffa44e7893b11145a71ccdfe87092818c60c9623c85ed2`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 25.7 MB (25680563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd7e304e8119cfb61e7ee17a3fbbb3da922d4451e07f437b04b287b9f40dba7`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 10.4 KB (10437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971990212ec60ae1f33629f70147ae21a007cb7d5de9f51ca8d4e59285daae35`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 2.1 KB (2077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:efe89864481f12046d4262654db36e678973a38432e6dcadf461cd5fd7b879d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.8 KB (805756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87cf93dfa5044bb65b87291d2d5eebb13f163d81f9ae12b8be61e327fe686e02`

```dockerfile
```

-	Layers:
	-	`sha256:eae9966f053053199b40dcaff83fb353a628619b1d5a607c2eb2c63a81dd97b7`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 782.6 KB (782617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d78e2d97608d25661c448f1e9b7cc46f0db7db9ff9ca118581f492f49b6a11b8`  
		Last Modified: Fri, 17 Apr 2026 01:38:35 GMT  
		Size: 23.1 KB (23139 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8-alpine3.22`

```console
$ docker pull satosa@sha256:635c3bd8a7b1e62eb8f505c7640cf1bdf930cfac6ab7926573baed9958354ba7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8-alpine3.22` - linux; amd64

```console
$ docker pull satosa@sha256:e64adbaaaed0ecd676889a71476ffb657b6c96e99ea168202a836e9338daf5da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49591032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245adc8cf01a5f66ff2284be88e273d4841d80dc1a1c3e904abc104fd609db9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:30:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:30:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 00:36:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:36:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:36:29 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:14:35 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
ENV SATOSA_VERSION=8.5.1
# Fri, 17 Apr 2026 01:14:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
WORKDIR /etc/satosa
# Fri, 17 Apr 2026 01:14:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:14:56 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 17 Apr 2026 01:14:56 GMT
USER satosa:satosa
# Fri, 17 Apr 2026 01:14:56 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df730813d20b0cb8062fb76ce24dc8fc02961ddd625cd6be3c86a0bc4dde8e56`  
		Last Modified: Fri, 17 Apr 2026 00:36:36 GMT  
		Size: 455.0 KB (454972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe818d7ffa27044c9667e73b415f9ae4c37a5d5d78c0cc4462423ded6b373a5`  
		Last Modified: Fri, 17 Apr 2026 00:36:36 GMT  
		Size: 12.5 MB (12472237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf71161b7b0782d25e76411844b95d7c41c91a90891d50df620e89e99fe18b8`  
		Last Modified: Fri, 17 Apr 2026 00:36:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8d9dc3a6733c4a32030cfa81ae0f31e2968fd1b1097d14d360df5e799d9bc9`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 6.7 MB (6744550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77426ee3fb08a0c6baa34b9704abd4f7fd61339c643f0a43c04b0f4962c07a93`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 26.1 MB (26098299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92f5d482e5e64b0b81c6a55dbb5a3cda363eb3e4979e4288755506f6d617458`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 10.4 KB (10431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7c65b6d4cd12b071c97dca761ea5c539c9402480aa6da6b50e82cfcf0306cc`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 2.1 KB (2076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-alpine3.22` - unknown; unknown

```console
$ docker pull satosa@sha256:f995f2aa2d9c5f4f425e5c76b9a84833ab0168d8777212eb0fd0a6454b896e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.5 KB (805473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2e4d3867615dc4bcf34d3615fffd2782c10a5980b2e89b2cfc5acf53027d74`

```dockerfile
```

-	Layers:
	-	`sha256:66040d43ba1ffe7cbed77eaa5a76d1f221c9253d108cf118fc8d85ddd831614c`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 782.5 KB (782513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b2a4e9a01427f7604acf929bf5d708369cff7bc24cfa7d0c012c8589bc32450`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 23.0 KB (22960 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:ad74b8922ba82d4cc6b9d562384bc8e5cc6d53864ea2bc66078696d7397cdafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49501857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34acd28bc2bbd82e5e73375c4a90f7169c780bc2d0e6c41ca9e0c5d4f74b7ade`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:32:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:32:45 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 00:39:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:39:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:39:34 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:38:03 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Fri, 17 Apr 2026 01:38:26 GMT
ENV SATOSA_VERSION=8.5.1
# Fri, 17 Apr 2026 01:38:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
WORKDIR /etc/satosa
# Fri, 17 Apr 2026 01:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:38:27 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 17 Apr 2026 01:38:27 GMT
USER satosa:satosa
# Fri, 17 Apr 2026 01:38:27 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcaff11adfb133e9e9320abbc299cc834c1403c253c3f7ea4ccaab6d6932fa60`  
		Last Modified: Fri, 17 Apr 2026 00:39:41 GMT  
		Size: 457.3 KB (457313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53736ed35b86baa4c031683ba780c3f739bb4f9961f7885b78af60392fbe5836`  
		Last Modified: Fri, 17 Apr 2026 00:39:41 GMT  
		Size: 12.5 MB (12486525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2c305c7606c8ddaf30bedaeaa4c18783036b29fbe2d07fc7eda11e7d1ddc34`  
		Last Modified: Fri, 17 Apr 2026 00:39:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b6dc3325f307fb75ee4f9d98da6f233aeecb5d14c89aed997bf4e4a7779b13`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 6.7 MB (6722767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff746c3bcb9c24e2fffa44e7893b11145a71ccdfe87092818c60c9623c85ed2`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 25.7 MB (25680563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd7e304e8119cfb61e7ee17a3fbbb3da922d4451e07f437b04b287b9f40dba7`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 10.4 KB (10437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971990212ec60ae1f33629f70147ae21a007cb7d5de9f51ca8d4e59285daae35`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 2.1 KB (2077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-alpine3.22` - unknown; unknown

```console
$ docker pull satosa@sha256:efe89864481f12046d4262654db36e678973a38432e6dcadf461cd5fd7b879d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.8 KB (805756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87cf93dfa5044bb65b87291d2d5eebb13f163d81f9ae12b8be61e327fe686e02`

```dockerfile
```

-	Layers:
	-	`sha256:eae9966f053053199b40dcaff83fb353a628619b1d5a607c2eb2c63a81dd97b7`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 782.6 KB (782617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d78e2d97608d25661c448f1e9b7cc46f0db7db9ff9ca118581f492f49b6a11b8`  
		Last Modified: Fri, 17 Apr 2026 01:38:35 GMT  
		Size: 23.1 KB (23139 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8-bookworm`

```console
$ docker pull satosa@sha256:7c907d50804dc6ecbe36c4faa8d54754f386ef005a1e82442a35dcd34b992995
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8-bookworm` - linux; amd64

```console
$ docker pull satosa@sha256:5655dae76305b96869065034d848eb92090aaa0c388fb6ec10c523acfe64fc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92457715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26bb17950e679e22cf69f7c9e1538ffa56c520b298527c2a9eff0b77a4c6c47c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:59:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:59:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PYTHON_VERSION=3.13.14
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PYTHON_SHA256=639e43243c620a308f968213df9e00f2f8f62332f7adbaa7a7eeb9783057c690
# Wed, 24 Jun 2026 02:10:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 24 Jun 2026 02:10:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 24 Jun 2026 02:10:55 GMT
CMD ["python3"]
# Wed, 24 Jun 2026 02:43:04 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Wed, 24 Jun 2026 02:43:52 GMT
ENV SATOSA_VERSION=8.5.1
# Wed, 24 Jun 2026 02:43:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
WORKDIR /etc/satosa
# Wed, 24 Jun 2026 02:43:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:43:53 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 24 Jun 2026 02:43:53 GMT
USER satosa:satosa
# Wed, 24 Jun 2026 02:43:53 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e26001d5620dfc2698f3a683c497e1cabdcc4757f4ca4ff70e33cb36057df02`  
		Last Modified: Wed, 24 Jun 2026 02:11:04 GMT  
		Size: 3.5 MB (3520812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90b26812a028bfa582bede756e645cf91fe9d05f2991b0862d719a003cce5ed`  
		Last Modified: Wed, 24 Jun 2026 02:11:05 GMT  
		Size: 12.6 MB (12570253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d229a71b9e515d634cb7f17b8bfe71586ed1282edbcfb81faaca1aebd0ed028b`  
		Last Modified: Wed, 24 Jun 2026 02:11:04 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0d169f435410c8068b61f1f86441b66ba63e5b017eb2a7db41dcdb1f48d007`  
		Last Modified: Wed, 24 Jun 2026 02:44:05 GMT  
		Size: 21.6 MB (21598611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5723dc18369d76c11887e05369a995342ca50992ecf72a7d14b766a7164e896b`  
		Last Modified: Wed, 24 Jun 2026 02:44:05 GMT  
		Size: 26.5 MB (26517606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca12e5f4cad01e654ee761cf49288d7dd440d9ac1bdf2cab826b64a9090213c9`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 10.4 KB (10437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1594679d03fab51ca435b90ed827eb2b73e41cfea3f269fafee6cdafb6f6eac`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 2.1 KB (2074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:5f98c4b2665f69dcf052d4ab597ff30427c3dc5edd3604a267e79edfca34634e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8b97b41f3b02471095632cc69e5647bbe7f5be1499d8512bd4e4254e0447d3`

```dockerfile
```

-	Layers:
	-	`sha256:9e9a9262540a6671d38ce01f5f543fd48f4096a8b3339ec72d7401b0ed450fc2`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 2.7 MB (2704660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0fe9e7f73f935ef31b3b3d1f07c9a4794a74a0447d0153ddc5dbfaa4e71a7ce`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 22.3 KB (22266 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8-bookworm` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e18cfffa9074424656f99d0444260f631f2a354659ba025c73a84abd42bb8226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91562388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab281fe3962b4af7fcd4f4cd9ef08844ba62e49b65cb1c4e070aad6a834c5a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:02:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:02:38 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PYTHON_VERSION=3.13.14
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PYTHON_SHA256=639e43243c620a308f968213df9e00f2f8f62332f7adbaa7a7eeb9783057c690
# Wed, 24 Jun 2026 02:16:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 24 Jun 2026 02:16:22 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 24 Jun 2026 02:16:22 GMT
CMD ["python3"]
# Wed, 24 Jun 2026 03:23:47 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Wed, 24 Jun 2026 03:24:34 GMT
ENV SATOSA_VERSION=8.5.1
# Wed, 24 Jun 2026 03:24:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
WORKDIR /etc/satosa
# Wed, 24 Jun 2026 03:24:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:24:35 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 24 Jun 2026 03:24:35 GMT
USER satosa:satosa
# Wed, 24 Jun 2026 03:24:35 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e03177a4ba5d2a105c80da4d791b999a2c0d8592218bf604937099767dce4`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 3.4 MB (3352640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8112ec847c4c51cc9e087e72458f63645ee819d8f7f5b00b18c78d8b45457b`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 12.5 MB (12472943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4140d7667663a40213044b01b7f98a453c79fa59784459232580dd4608afcdd`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d1353c5acbe10355ef9cfcf93a6db67a29c03e660d0ac1af30cf1e72cb8542`  
		Last Modified: Wed, 24 Jun 2026 03:24:46 GMT  
		Size: 21.5 MB (21451922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25368aad8a3d30bf1e9c31630225e8631f0de92e424d60e2c58e26eaecee3f51`  
		Last Modified: Wed, 24 Jun 2026 03:24:46 GMT  
		Size: 26.1 MB (26149666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9ca620b6bee0b901297e863ac4357db955c3bd67ff01aa0f4e618d6de2ccaf`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 10.4 KB (10442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cccdfcb5100f94f01bec9af80fe397d740ea6bcb32e131db97cbacce527834`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 2.1 KB (2075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:cfd648ffe65a01b96b5584990dc074c7a1f1e961a386dcc8446c0372e1ecfac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2727434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76688f62ede38ed94bd9711fb0cfcbfd6e7ab709ab504ef46889c172ef57faf7`

```dockerfile
```

-	Layers:
	-	`sha256:8734d5cd42d0cfe8c59fc9680272074d7b1f4b5ed314e46bbe0b8656d6fed5d7`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 2.7 MB (2704986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f33959acb229dcf2327a93d12ecb800afb9fe3dafc7ab97bba3371cc15ab1a45`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 22.4 KB (22448 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.5`

```console
$ docker pull satosa@sha256:7c907d50804dc6ecbe36c4faa8d54754f386ef005a1e82442a35dcd34b992995
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8.5` - linux; amd64

```console
$ docker pull satosa@sha256:5655dae76305b96869065034d848eb92090aaa0c388fb6ec10c523acfe64fc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92457715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26bb17950e679e22cf69f7c9e1538ffa56c520b298527c2a9eff0b77a4c6c47c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:59:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:59:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PYTHON_VERSION=3.13.14
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PYTHON_SHA256=639e43243c620a308f968213df9e00f2f8f62332f7adbaa7a7eeb9783057c690
# Wed, 24 Jun 2026 02:10:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 24 Jun 2026 02:10:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 24 Jun 2026 02:10:55 GMT
CMD ["python3"]
# Wed, 24 Jun 2026 02:43:04 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Wed, 24 Jun 2026 02:43:52 GMT
ENV SATOSA_VERSION=8.5.1
# Wed, 24 Jun 2026 02:43:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
WORKDIR /etc/satosa
# Wed, 24 Jun 2026 02:43:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:43:53 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 24 Jun 2026 02:43:53 GMT
USER satosa:satosa
# Wed, 24 Jun 2026 02:43:53 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e26001d5620dfc2698f3a683c497e1cabdcc4757f4ca4ff70e33cb36057df02`  
		Last Modified: Wed, 24 Jun 2026 02:11:04 GMT  
		Size: 3.5 MB (3520812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90b26812a028bfa582bede756e645cf91fe9d05f2991b0862d719a003cce5ed`  
		Last Modified: Wed, 24 Jun 2026 02:11:05 GMT  
		Size: 12.6 MB (12570253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d229a71b9e515d634cb7f17b8bfe71586ed1282edbcfb81faaca1aebd0ed028b`  
		Last Modified: Wed, 24 Jun 2026 02:11:04 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0d169f435410c8068b61f1f86441b66ba63e5b017eb2a7db41dcdb1f48d007`  
		Last Modified: Wed, 24 Jun 2026 02:44:05 GMT  
		Size: 21.6 MB (21598611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5723dc18369d76c11887e05369a995342ca50992ecf72a7d14b766a7164e896b`  
		Last Modified: Wed, 24 Jun 2026 02:44:05 GMT  
		Size: 26.5 MB (26517606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca12e5f4cad01e654ee761cf49288d7dd440d9ac1bdf2cab826b64a9090213c9`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 10.4 KB (10437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1594679d03fab51ca435b90ed827eb2b73e41cfea3f269fafee6cdafb6f6eac`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 2.1 KB (2074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5` - unknown; unknown

```console
$ docker pull satosa@sha256:5f98c4b2665f69dcf052d4ab597ff30427c3dc5edd3604a267e79edfca34634e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8b97b41f3b02471095632cc69e5647bbe7f5be1499d8512bd4e4254e0447d3`

```dockerfile
```

-	Layers:
	-	`sha256:9e9a9262540a6671d38ce01f5f543fd48f4096a8b3339ec72d7401b0ed450fc2`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 2.7 MB (2704660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0fe9e7f73f935ef31b3b3d1f07c9a4794a74a0447d0153ddc5dbfaa4e71a7ce`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 22.3 KB (22266 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.5` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e18cfffa9074424656f99d0444260f631f2a354659ba025c73a84abd42bb8226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91562388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab281fe3962b4af7fcd4f4cd9ef08844ba62e49b65cb1c4e070aad6a834c5a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:02:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:02:38 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PYTHON_VERSION=3.13.14
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PYTHON_SHA256=639e43243c620a308f968213df9e00f2f8f62332f7adbaa7a7eeb9783057c690
# Wed, 24 Jun 2026 02:16:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 24 Jun 2026 02:16:22 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 24 Jun 2026 02:16:22 GMT
CMD ["python3"]
# Wed, 24 Jun 2026 03:23:47 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Wed, 24 Jun 2026 03:24:34 GMT
ENV SATOSA_VERSION=8.5.1
# Wed, 24 Jun 2026 03:24:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
WORKDIR /etc/satosa
# Wed, 24 Jun 2026 03:24:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:24:35 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 24 Jun 2026 03:24:35 GMT
USER satosa:satosa
# Wed, 24 Jun 2026 03:24:35 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e03177a4ba5d2a105c80da4d791b999a2c0d8592218bf604937099767dce4`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 3.4 MB (3352640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8112ec847c4c51cc9e087e72458f63645ee819d8f7f5b00b18c78d8b45457b`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 12.5 MB (12472943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4140d7667663a40213044b01b7f98a453c79fa59784459232580dd4608afcdd`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d1353c5acbe10355ef9cfcf93a6db67a29c03e660d0ac1af30cf1e72cb8542`  
		Last Modified: Wed, 24 Jun 2026 03:24:46 GMT  
		Size: 21.5 MB (21451922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25368aad8a3d30bf1e9c31630225e8631f0de92e424d60e2c58e26eaecee3f51`  
		Last Modified: Wed, 24 Jun 2026 03:24:46 GMT  
		Size: 26.1 MB (26149666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9ca620b6bee0b901297e863ac4357db955c3bd67ff01aa0f4e618d6de2ccaf`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 10.4 KB (10442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cccdfcb5100f94f01bec9af80fe397d740ea6bcb32e131db97cbacce527834`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 2.1 KB (2075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5` - unknown; unknown

```console
$ docker pull satosa@sha256:cfd648ffe65a01b96b5584990dc074c7a1f1e961a386dcc8446c0372e1ecfac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2727434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76688f62ede38ed94bd9711fb0cfcbfd6e7ab709ab504ef46889c172ef57faf7`

```dockerfile
```

-	Layers:
	-	`sha256:8734d5cd42d0cfe8c59fc9680272074d7b1f4b5ed314e46bbe0b8656d6fed5d7`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 2.7 MB (2704986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f33959acb229dcf2327a93d12ecb800afb9fe3dafc7ab97bba3371cc15ab1a45`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 22.4 KB (22448 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.5-alpine`

```console
$ docker pull satosa@sha256:635c3bd8a7b1e62eb8f505c7640cf1bdf930cfac6ab7926573baed9958354ba7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8.5-alpine` - linux; amd64

```console
$ docker pull satosa@sha256:e64adbaaaed0ecd676889a71476ffb657b6c96e99ea168202a836e9338daf5da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49591032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245adc8cf01a5f66ff2284be88e273d4841d80dc1a1c3e904abc104fd609db9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:30:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:30:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 00:36:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:36:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:36:29 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:14:35 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
ENV SATOSA_VERSION=8.5.1
# Fri, 17 Apr 2026 01:14:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
WORKDIR /etc/satosa
# Fri, 17 Apr 2026 01:14:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:14:56 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 17 Apr 2026 01:14:56 GMT
USER satosa:satosa
# Fri, 17 Apr 2026 01:14:56 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df730813d20b0cb8062fb76ce24dc8fc02961ddd625cd6be3c86a0bc4dde8e56`  
		Last Modified: Fri, 17 Apr 2026 00:36:36 GMT  
		Size: 455.0 KB (454972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe818d7ffa27044c9667e73b415f9ae4c37a5d5d78c0cc4462423ded6b373a5`  
		Last Modified: Fri, 17 Apr 2026 00:36:36 GMT  
		Size: 12.5 MB (12472237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf71161b7b0782d25e76411844b95d7c41c91a90891d50df620e89e99fe18b8`  
		Last Modified: Fri, 17 Apr 2026 00:36:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8d9dc3a6733c4a32030cfa81ae0f31e2968fd1b1097d14d360df5e799d9bc9`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 6.7 MB (6744550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77426ee3fb08a0c6baa34b9704abd4f7fd61339c643f0a43c04b0f4962c07a93`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 26.1 MB (26098299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92f5d482e5e64b0b81c6a55dbb5a3cda363eb3e4979e4288755506f6d617458`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 10.4 KB (10431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7c65b6d4cd12b071c97dca761ea5c539c9402480aa6da6b50e82cfcf0306cc`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 2.1 KB (2076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:f995f2aa2d9c5f4f425e5c76b9a84833ab0168d8777212eb0fd0a6454b896e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.5 KB (805473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2e4d3867615dc4bcf34d3615fffd2782c10a5980b2e89b2cfc5acf53027d74`

```dockerfile
```

-	Layers:
	-	`sha256:66040d43ba1ffe7cbed77eaa5a76d1f221c9253d108cf118fc8d85ddd831614c`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 782.5 KB (782513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b2a4e9a01427f7604acf929bf5d708369cff7bc24cfa7d0c012c8589bc32450`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 23.0 KB (22960 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.5-alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:ad74b8922ba82d4cc6b9d562384bc8e5cc6d53864ea2bc66078696d7397cdafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49501857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34acd28bc2bbd82e5e73375c4a90f7169c780bc2d0e6c41ca9e0c5d4f74b7ade`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:32:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:32:45 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 00:39:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:39:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:39:34 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:38:03 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Fri, 17 Apr 2026 01:38:26 GMT
ENV SATOSA_VERSION=8.5.1
# Fri, 17 Apr 2026 01:38:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
WORKDIR /etc/satosa
# Fri, 17 Apr 2026 01:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:38:27 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 17 Apr 2026 01:38:27 GMT
USER satosa:satosa
# Fri, 17 Apr 2026 01:38:27 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcaff11adfb133e9e9320abbc299cc834c1403c253c3f7ea4ccaab6d6932fa60`  
		Last Modified: Fri, 17 Apr 2026 00:39:41 GMT  
		Size: 457.3 KB (457313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53736ed35b86baa4c031683ba780c3f739bb4f9961f7885b78af60392fbe5836`  
		Last Modified: Fri, 17 Apr 2026 00:39:41 GMT  
		Size: 12.5 MB (12486525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2c305c7606c8ddaf30bedaeaa4c18783036b29fbe2d07fc7eda11e7d1ddc34`  
		Last Modified: Fri, 17 Apr 2026 00:39:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b6dc3325f307fb75ee4f9d98da6f233aeecb5d14c89aed997bf4e4a7779b13`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 6.7 MB (6722767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff746c3bcb9c24e2fffa44e7893b11145a71ccdfe87092818c60c9623c85ed2`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 25.7 MB (25680563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd7e304e8119cfb61e7ee17a3fbbb3da922d4451e07f437b04b287b9f40dba7`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 10.4 KB (10437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971990212ec60ae1f33629f70147ae21a007cb7d5de9f51ca8d4e59285daae35`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 2.1 KB (2077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:efe89864481f12046d4262654db36e678973a38432e6dcadf461cd5fd7b879d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.8 KB (805756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87cf93dfa5044bb65b87291d2d5eebb13f163d81f9ae12b8be61e327fe686e02`

```dockerfile
```

-	Layers:
	-	`sha256:eae9966f053053199b40dcaff83fb353a628619b1d5a607c2eb2c63a81dd97b7`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 782.6 KB (782617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d78e2d97608d25661c448f1e9b7cc46f0db7db9ff9ca118581f492f49b6a11b8`  
		Last Modified: Fri, 17 Apr 2026 01:38:35 GMT  
		Size: 23.1 KB (23139 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.5-alpine3.22`

```console
$ docker pull satosa@sha256:635c3bd8a7b1e62eb8f505c7640cf1bdf930cfac6ab7926573baed9958354ba7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8.5-alpine3.22` - linux; amd64

```console
$ docker pull satosa@sha256:e64adbaaaed0ecd676889a71476ffb657b6c96e99ea168202a836e9338daf5da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49591032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245adc8cf01a5f66ff2284be88e273d4841d80dc1a1c3e904abc104fd609db9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:30:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:30:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 00:36:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:36:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:36:29 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:14:35 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
ENV SATOSA_VERSION=8.5.1
# Fri, 17 Apr 2026 01:14:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
WORKDIR /etc/satosa
# Fri, 17 Apr 2026 01:14:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:14:56 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 17 Apr 2026 01:14:56 GMT
USER satosa:satosa
# Fri, 17 Apr 2026 01:14:56 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df730813d20b0cb8062fb76ce24dc8fc02961ddd625cd6be3c86a0bc4dde8e56`  
		Last Modified: Fri, 17 Apr 2026 00:36:36 GMT  
		Size: 455.0 KB (454972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe818d7ffa27044c9667e73b415f9ae4c37a5d5d78c0cc4462423ded6b373a5`  
		Last Modified: Fri, 17 Apr 2026 00:36:36 GMT  
		Size: 12.5 MB (12472237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf71161b7b0782d25e76411844b95d7c41c91a90891d50df620e89e99fe18b8`  
		Last Modified: Fri, 17 Apr 2026 00:36:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8d9dc3a6733c4a32030cfa81ae0f31e2968fd1b1097d14d360df5e799d9bc9`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 6.7 MB (6744550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77426ee3fb08a0c6baa34b9704abd4f7fd61339c643f0a43c04b0f4962c07a93`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 26.1 MB (26098299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92f5d482e5e64b0b81c6a55dbb5a3cda363eb3e4979e4288755506f6d617458`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 10.4 KB (10431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7c65b6d4cd12b071c97dca761ea5c539c9402480aa6da6b50e82cfcf0306cc`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 2.1 KB (2076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5-alpine3.22` - unknown; unknown

```console
$ docker pull satosa@sha256:f995f2aa2d9c5f4f425e5c76b9a84833ab0168d8777212eb0fd0a6454b896e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.5 KB (805473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2e4d3867615dc4bcf34d3615fffd2782c10a5980b2e89b2cfc5acf53027d74`

```dockerfile
```

-	Layers:
	-	`sha256:66040d43ba1ffe7cbed77eaa5a76d1f221c9253d108cf118fc8d85ddd831614c`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 782.5 KB (782513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b2a4e9a01427f7604acf929bf5d708369cff7bc24cfa7d0c012c8589bc32450`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 23.0 KB (22960 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.5-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:ad74b8922ba82d4cc6b9d562384bc8e5cc6d53864ea2bc66078696d7397cdafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49501857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34acd28bc2bbd82e5e73375c4a90f7169c780bc2d0e6c41ca9e0c5d4f74b7ade`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:32:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:32:45 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 00:39:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:39:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:39:34 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:38:03 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Fri, 17 Apr 2026 01:38:26 GMT
ENV SATOSA_VERSION=8.5.1
# Fri, 17 Apr 2026 01:38:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
WORKDIR /etc/satosa
# Fri, 17 Apr 2026 01:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:38:27 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 17 Apr 2026 01:38:27 GMT
USER satosa:satosa
# Fri, 17 Apr 2026 01:38:27 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcaff11adfb133e9e9320abbc299cc834c1403c253c3f7ea4ccaab6d6932fa60`  
		Last Modified: Fri, 17 Apr 2026 00:39:41 GMT  
		Size: 457.3 KB (457313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53736ed35b86baa4c031683ba780c3f739bb4f9961f7885b78af60392fbe5836`  
		Last Modified: Fri, 17 Apr 2026 00:39:41 GMT  
		Size: 12.5 MB (12486525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2c305c7606c8ddaf30bedaeaa4c18783036b29fbe2d07fc7eda11e7d1ddc34`  
		Last Modified: Fri, 17 Apr 2026 00:39:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b6dc3325f307fb75ee4f9d98da6f233aeecb5d14c89aed997bf4e4a7779b13`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 6.7 MB (6722767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff746c3bcb9c24e2fffa44e7893b11145a71ccdfe87092818c60c9623c85ed2`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 25.7 MB (25680563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd7e304e8119cfb61e7ee17a3fbbb3da922d4451e07f437b04b287b9f40dba7`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 10.4 KB (10437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971990212ec60ae1f33629f70147ae21a007cb7d5de9f51ca8d4e59285daae35`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 2.1 KB (2077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5-alpine3.22` - unknown; unknown

```console
$ docker pull satosa@sha256:efe89864481f12046d4262654db36e678973a38432e6dcadf461cd5fd7b879d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.8 KB (805756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87cf93dfa5044bb65b87291d2d5eebb13f163d81f9ae12b8be61e327fe686e02`

```dockerfile
```

-	Layers:
	-	`sha256:eae9966f053053199b40dcaff83fb353a628619b1d5a607c2eb2c63a81dd97b7`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 782.6 KB (782617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d78e2d97608d25661c448f1e9b7cc46f0db7db9ff9ca118581f492f49b6a11b8`  
		Last Modified: Fri, 17 Apr 2026 01:38:35 GMT  
		Size: 23.1 KB (23139 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.5-bookworm`

```console
$ docker pull satosa@sha256:7c907d50804dc6ecbe36c4faa8d54754f386ef005a1e82442a35dcd34b992995
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8.5-bookworm` - linux; amd64

```console
$ docker pull satosa@sha256:5655dae76305b96869065034d848eb92090aaa0c388fb6ec10c523acfe64fc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92457715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26bb17950e679e22cf69f7c9e1538ffa56c520b298527c2a9eff0b77a4c6c47c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:59:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:59:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PYTHON_VERSION=3.13.14
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PYTHON_SHA256=639e43243c620a308f968213df9e00f2f8f62332f7adbaa7a7eeb9783057c690
# Wed, 24 Jun 2026 02:10:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 24 Jun 2026 02:10:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 24 Jun 2026 02:10:55 GMT
CMD ["python3"]
# Wed, 24 Jun 2026 02:43:04 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Wed, 24 Jun 2026 02:43:52 GMT
ENV SATOSA_VERSION=8.5.1
# Wed, 24 Jun 2026 02:43:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
WORKDIR /etc/satosa
# Wed, 24 Jun 2026 02:43:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:43:53 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 24 Jun 2026 02:43:53 GMT
USER satosa:satosa
# Wed, 24 Jun 2026 02:43:53 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e26001d5620dfc2698f3a683c497e1cabdcc4757f4ca4ff70e33cb36057df02`  
		Last Modified: Wed, 24 Jun 2026 02:11:04 GMT  
		Size: 3.5 MB (3520812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90b26812a028bfa582bede756e645cf91fe9d05f2991b0862d719a003cce5ed`  
		Last Modified: Wed, 24 Jun 2026 02:11:05 GMT  
		Size: 12.6 MB (12570253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d229a71b9e515d634cb7f17b8bfe71586ed1282edbcfb81faaca1aebd0ed028b`  
		Last Modified: Wed, 24 Jun 2026 02:11:04 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0d169f435410c8068b61f1f86441b66ba63e5b017eb2a7db41dcdb1f48d007`  
		Last Modified: Wed, 24 Jun 2026 02:44:05 GMT  
		Size: 21.6 MB (21598611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5723dc18369d76c11887e05369a995342ca50992ecf72a7d14b766a7164e896b`  
		Last Modified: Wed, 24 Jun 2026 02:44:05 GMT  
		Size: 26.5 MB (26517606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca12e5f4cad01e654ee761cf49288d7dd440d9ac1bdf2cab826b64a9090213c9`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 10.4 KB (10437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1594679d03fab51ca435b90ed827eb2b73e41cfea3f269fafee6cdafb6f6eac`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 2.1 KB (2074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:5f98c4b2665f69dcf052d4ab597ff30427c3dc5edd3604a267e79edfca34634e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8b97b41f3b02471095632cc69e5647bbe7f5be1499d8512bd4e4254e0447d3`

```dockerfile
```

-	Layers:
	-	`sha256:9e9a9262540a6671d38ce01f5f543fd48f4096a8b3339ec72d7401b0ed450fc2`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 2.7 MB (2704660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0fe9e7f73f935ef31b3b3d1f07c9a4794a74a0447d0153ddc5dbfaa4e71a7ce`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 22.3 KB (22266 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.5-bookworm` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e18cfffa9074424656f99d0444260f631f2a354659ba025c73a84abd42bb8226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91562388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab281fe3962b4af7fcd4f4cd9ef08844ba62e49b65cb1c4e070aad6a834c5a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:02:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:02:38 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PYTHON_VERSION=3.13.14
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PYTHON_SHA256=639e43243c620a308f968213df9e00f2f8f62332f7adbaa7a7eeb9783057c690
# Wed, 24 Jun 2026 02:16:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 24 Jun 2026 02:16:22 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 24 Jun 2026 02:16:22 GMT
CMD ["python3"]
# Wed, 24 Jun 2026 03:23:47 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Wed, 24 Jun 2026 03:24:34 GMT
ENV SATOSA_VERSION=8.5.1
# Wed, 24 Jun 2026 03:24:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
WORKDIR /etc/satosa
# Wed, 24 Jun 2026 03:24:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:24:35 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 24 Jun 2026 03:24:35 GMT
USER satosa:satosa
# Wed, 24 Jun 2026 03:24:35 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e03177a4ba5d2a105c80da4d791b999a2c0d8592218bf604937099767dce4`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 3.4 MB (3352640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8112ec847c4c51cc9e087e72458f63645ee819d8f7f5b00b18c78d8b45457b`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 12.5 MB (12472943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4140d7667663a40213044b01b7f98a453c79fa59784459232580dd4608afcdd`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d1353c5acbe10355ef9cfcf93a6db67a29c03e660d0ac1af30cf1e72cb8542`  
		Last Modified: Wed, 24 Jun 2026 03:24:46 GMT  
		Size: 21.5 MB (21451922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25368aad8a3d30bf1e9c31630225e8631f0de92e424d60e2c58e26eaecee3f51`  
		Last Modified: Wed, 24 Jun 2026 03:24:46 GMT  
		Size: 26.1 MB (26149666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9ca620b6bee0b901297e863ac4357db955c3bd67ff01aa0f4e618d6de2ccaf`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 10.4 KB (10442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cccdfcb5100f94f01bec9af80fe397d740ea6bcb32e131db97cbacce527834`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 2.1 KB (2075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:cfd648ffe65a01b96b5584990dc074c7a1f1e961a386dcc8446c0372e1ecfac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2727434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76688f62ede38ed94bd9711fb0cfcbfd6e7ab709ab504ef46889c172ef57faf7`

```dockerfile
```

-	Layers:
	-	`sha256:8734d5cd42d0cfe8c59fc9680272074d7b1f4b5ed314e46bbe0b8656d6fed5d7`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 2.7 MB (2704986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f33959acb229dcf2327a93d12ecb800afb9fe3dafc7ab97bba3371cc15ab1a45`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 22.4 KB (22448 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.5.1`

```console
$ docker pull satosa@sha256:7c907d50804dc6ecbe36c4faa8d54754f386ef005a1e82442a35dcd34b992995
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8.5.1` - linux; amd64

```console
$ docker pull satosa@sha256:5655dae76305b96869065034d848eb92090aaa0c388fb6ec10c523acfe64fc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92457715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26bb17950e679e22cf69f7c9e1538ffa56c520b298527c2a9eff0b77a4c6c47c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:59:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:59:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PYTHON_VERSION=3.13.14
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PYTHON_SHA256=639e43243c620a308f968213df9e00f2f8f62332f7adbaa7a7eeb9783057c690
# Wed, 24 Jun 2026 02:10:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 24 Jun 2026 02:10:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 24 Jun 2026 02:10:55 GMT
CMD ["python3"]
# Wed, 24 Jun 2026 02:43:04 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Wed, 24 Jun 2026 02:43:52 GMT
ENV SATOSA_VERSION=8.5.1
# Wed, 24 Jun 2026 02:43:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
WORKDIR /etc/satosa
# Wed, 24 Jun 2026 02:43:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:43:53 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 24 Jun 2026 02:43:53 GMT
USER satosa:satosa
# Wed, 24 Jun 2026 02:43:53 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e26001d5620dfc2698f3a683c497e1cabdcc4757f4ca4ff70e33cb36057df02`  
		Last Modified: Wed, 24 Jun 2026 02:11:04 GMT  
		Size: 3.5 MB (3520812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90b26812a028bfa582bede756e645cf91fe9d05f2991b0862d719a003cce5ed`  
		Last Modified: Wed, 24 Jun 2026 02:11:05 GMT  
		Size: 12.6 MB (12570253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d229a71b9e515d634cb7f17b8bfe71586ed1282edbcfb81faaca1aebd0ed028b`  
		Last Modified: Wed, 24 Jun 2026 02:11:04 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0d169f435410c8068b61f1f86441b66ba63e5b017eb2a7db41dcdb1f48d007`  
		Last Modified: Wed, 24 Jun 2026 02:44:05 GMT  
		Size: 21.6 MB (21598611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5723dc18369d76c11887e05369a995342ca50992ecf72a7d14b766a7164e896b`  
		Last Modified: Wed, 24 Jun 2026 02:44:05 GMT  
		Size: 26.5 MB (26517606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca12e5f4cad01e654ee761cf49288d7dd440d9ac1bdf2cab826b64a9090213c9`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 10.4 KB (10437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1594679d03fab51ca435b90ed827eb2b73e41cfea3f269fafee6cdafb6f6eac`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 2.1 KB (2074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5.1` - unknown; unknown

```console
$ docker pull satosa@sha256:5f98c4b2665f69dcf052d4ab597ff30427c3dc5edd3604a267e79edfca34634e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8b97b41f3b02471095632cc69e5647bbe7f5be1499d8512bd4e4254e0447d3`

```dockerfile
```

-	Layers:
	-	`sha256:9e9a9262540a6671d38ce01f5f543fd48f4096a8b3339ec72d7401b0ed450fc2`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 2.7 MB (2704660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0fe9e7f73f935ef31b3b3d1f07c9a4794a74a0447d0153ddc5dbfaa4e71a7ce`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 22.3 KB (22266 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.5.1` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e18cfffa9074424656f99d0444260f631f2a354659ba025c73a84abd42bb8226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91562388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab281fe3962b4af7fcd4f4cd9ef08844ba62e49b65cb1c4e070aad6a834c5a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:02:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:02:38 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PYTHON_VERSION=3.13.14
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PYTHON_SHA256=639e43243c620a308f968213df9e00f2f8f62332f7adbaa7a7eeb9783057c690
# Wed, 24 Jun 2026 02:16:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 24 Jun 2026 02:16:22 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 24 Jun 2026 02:16:22 GMT
CMD ["python3"]
# Wed, 24 Jun 2026 03:23:47 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Wed, 24 Jun 2026 03:24:34 GMT
ENV SATOSA_VERSION=8.5.1
# Wed, 24 Jun 2026 03:24:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
WORKDIR /etc/satosa
# Wed, 24 Jun 2026 03:24:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:24:35 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 24 Jun 2026 03:24:35 GMT
USER satosa:satosa
# Wed, 24 Jun 2026 03:24:35 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e03177a4ba5d2a105c80da4d791b999a2c0d8592218bf604937099767dce4`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 3.4 MB (3352640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8112ec847c4c51cc9e087e72458f63645ee819d8f7f5b00b18c78d8b45457b`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 12.5 MB (12472943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4140d7667663a40213044b01b7f98a453c79fa59784459232580dd4608afcdd`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d1353c5acbe10355ef9cfcf93a6db67a29c03e660d0ac1af30cf1e72cb8542`  
		Last Modified: Wed, 24 Jun 2026 03:24:46 GMT  
		Size: 21.5 MB (21451922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25368aad8a3d30bf1e9c31630225e8631f0de92e424d60e2c58e26eaecee3f51`  
		Last Modified: Wed, 24 Jun 2026 03:24:46 GMT  
		Size: 26.1 MB (26149666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9ca620b6bee0b901297e863ac4357db955c3bd67ff01aa0f4e618d6de2ccaf`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 10.4 KB (10442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cccdfcb5100f94f01bec9af80fe397d740ea6bcb32e131db97cbacce527834`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 2.1 KB (2075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5.1` - unknown; unknown

```console
$ docker pull satosa@sha256:cfd648ffe65a01b96b5584990dc074c7a1f1e961a386dcc8446c0372e1ecfac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2727434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76688f62ede38ed94bd9711fb0cfcbfd6e7ab709ab504ef46889c172ef57faf7`

```dockerfile
```

-	Layers:
	-	`sha256:8734d5cd42d0cfe8c59fc9680272074d7b1f4b5ed314e46bbe0b8656d6fed5d7`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 2.7 MB (2704986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f33959acb229dcf2327a93d12ecb800afb9fe3dafc7ab97bba3371cc15ab1a45`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 22.4 KB (22448 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.5.1-alpine`

```console
$ docker pull satosa@sha256:635c3bd8a7b1e62eb8f505c7640cf1bdf930cfac6ab7926573baed9958354ba7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8.5.1-alpine` - linux; amd64

```console
$ docker pull satosa@sha256:e64adbaaaed0ecd676889a71476ffb657b6c96e99ea168202a836e9338daf5da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49591032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245adc8cf01a5f66ff2284be88e273d4841d80dc1a1c3e904abc104fd609db9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:30:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:30:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 00:36:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:36:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:36:29 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:14:35 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
ENV SATOSA_VERSION=8.5.1
# Fri, 17 Apr 2026 01:14:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
WORKDIR /etc/satosa
# Fri, 17 Apr 2026 01:14:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:14:56 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 17 Apr 2026 01:14:56 GMT
USER satosa:satosa
# Fri, 17 Apr 2026 01:14:56 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df730813d20b0cb8062fb76ce24dc8fc02961ddd625cd6be3c86a0bc4dde8e56`  
		Last Modified: Fri, 17 Apr 2026 00:36:36 GMT  
		Size: 455.0 KB (454972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe818d7ffa27044c9667e73b415f9ae4c37a5d5d78c0cc4462423ded6b373a5`  
		Last Modified: Fri, 17 Apr 2026 00:36:36 GMT  
		Size: 12.5 MB (12472237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf71161b7b0782d25e76411844b95d7c41c91a90891d50df620e89e99fe18b8`  
		Last Modified: Fri, 17 Apr 2026 00:36:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8d9dc3a6733c4a32030cfa81ae0f31e2968fd1b1097d14d360df5e799d9bc9`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 6.7 MB (6744550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77426ee3fb08a0c6baa34b9704abd4f7fd61339c643f0a43c04b0f4962c07a93`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 26.1 MB (26098299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92f5d482e5e64b0b81c6a55dbb5a3cda363eb3e4979e4288755506f6d617458`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 10.4 KB (10431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7c65b6d4cd12b071c97dca761ea5c539c9402480aa6da6b50e82cfcf0306cc`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 2.1 KB (2076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5.1-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:f995f2aa2d9c5f4f425e5c76b9a84833ab0168d8777212eb0fd0a6454b896e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.5 KB (805473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2e4d3867615dc4bcf34d3615fffd2782c10a5980b2e89b2cfc5acf53027d74`

```dockerfile
```

-	Layers:
	-	`sha256:66040d43ba1ffe7cbed77eaa5a76d1f221c9253d108cf118fc8d85ddd831614c`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 782.5 KB (782513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b2a4e9a01427f7604acf929bf5d708369cff7bc24cfa7d0c012c8589bc32450`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 23.0 KB (22960 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.5.1-alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:ad74b8922ba82d4cc6b9d562384bc8e5cc6d53864ea2bc66078696d7397cdafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49501857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34acd28bc2bbd82e5e73375c4a90f7169c780bc2d0e6c41ca9e0c5d4f74b7ade`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:32:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:32:45 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 00:39:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:39:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:39:34 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:38:03 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Fri, 17 Apr 2026 01:38:26 GMT
ENV SATOSA_VERSION=8.5.1
# Fri, 17 Apr 2026 01:38:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
WORKDIR /etc/satosa
# Fri, 17 Apr 2026 01:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:38:27 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 17 Apr 2026 01:38:27 GMT
USER satosa:satosa
# Fri, 17 Apr 2026 01:38:27 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcaff11adfb133e9e9320abbc299cc834c1403c253c3f7ea4ccaab6d6932fa60`  
		Last Modified: Fri, 17 Apr 2026 00:39:41 GMT  
		Size: 457.3 KB (457313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53736ed35b86baa4c031683ba780c3f739bb4f9961f7885b78af60392fbe5836`  
		Last Modified: Fri, 17 Apr 2026 00:39:41 GMT  
		Size: 12.5 MB (12486525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2c305c7606c8ddaf30bedaeaa4c18783036b29fbe2d07fc7eda11e7d1ddc34`  
		Last Modified: Fri, 17 Apr 2026 00:39:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b6dc3325f307fb75ee4f9d98da6f233aeecb5d14c89aed997bf4e4a7779b13`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 6.7 MB (6722767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff746c3bcb9c24e2fffa44e7893b11145a71ccdfe87092818c60c9623c85ed2`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 25.7 MB (25680563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd7e304e8119cfb61e7ee17a3fbbb3da922d4451e07f437b04b287b9f40dba7`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 10.4 KB (10437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971990212ec60ae1f33629f70147ae21a007cb7d5de9f51ca8d4e59285daae35`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 2.1 KB (2077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5.1-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:efe89864481f12046d4262654db36e678973a38432e6dcadf461cd5fd7b879d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.8 KB (805756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87cf93dfa5044bb65b87291d2d5eebb13f163d81f9ae12b8be61e327fe686e02`

```dockerfile
```

-	Layers:
	-	`sha256:eae9966f053053199b40dcaff83fb353a628619b1d5a607c2eb2c63a81dd97b7`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 782.6 KB (782617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d78e2d97608d25661c448f1e9b7cc46f0db7db9ff9ca118581f492f49b6a11b8`  
		Last Modified: Fri, 17 Apr 2026 01:38:35 GMT  
		Size: 23.1 KB (23139 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.5.1-alpine3.22`

```console
$ docker pull satosa@sha256:635c3bd8a7b1e62eb8f505c7640cf1bdf930cfac6ab7926573baed9958354ba7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8.5.1-alpine3.22` - linux; amd64

```console
$ docker pull satosa@sha256:e64adbaaaed0ecd676889a71476ffb657b6c96e99ea168202a836e9338daf5da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49591032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245adc8cf01a5f66ff2284be88e273d4841d80dc1a1c3e904abc104fd609db9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:30:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:30:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 00:36:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:36:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:36:29 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:14:35 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
ENV SATOSA_VERSION=8.5.1
# Fri, 17 Apr 2026 01:14:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
WORKDIR /etc/satosa
# Fri, 17 Apr 2026 01:14:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:14:56 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 17 Apr 2026 01:14:56 GMT
USER satosa:satosa
# Fri, 17 Apr 2026 01:14:56 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df730813d20b0cb8062fb76ce24dc8fc02961ddd625cd6be3c86a0bc4dde8e56`  
		Last Modified: Fri, 17 Apr 2026 00:36:36 GMT  
		Size: 455.0 KB (454972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe818d7ffa27044c9667e73b415f9ae4c37a5d5d78c0cc4462423ded6b373a5`  
		Last Modified: Fri, 17 Apr 2026 00:36:36 GMT  
		Size: 12.5 MB (12472237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf71161b7b0782d25e76411844b95d7c41c91a90891d50df620e89e99fe18b8`  
		Last Modified: Fri, 17 Apr 2026 00:36:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8d9dc3a6733c4a32030cfa81ae0f31e2968fd1b1097d14d360df5e799d9bc9`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 6.7 MB (6744550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77426ee3fb08a0c6baa34b9704abd4f7fd61339c643f0a43c04b0f4962c07a93`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 26.1 MB (26098299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92f5d482e5e64b0b81c6a55dbb5a3cda363eb3e4979e4288755506f6d617458`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 10.4 KB (10431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7c65b6d4cd12b071c97dca761ea5c539c9402480aa6da6b50e82cfcf0306cc`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 2.1 KB (2076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5.1-alpine3.22` - unknown; unknown

```console
$ docker pull satosa@sha256:f995f2aa2d9c5f4f425e5c76b9a84833ab0168d8777212eb0fd0a6454b896e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.5 KB (805473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2e4d3867615dc4bcf34d3615fffd2782c10a5980b2e89b2cfc5acf53027d74`

```dockerfile
```

-	Layers:
	-	`sha256:66040d43ba1ffe7cbed77eaa5a76d1f221c9253d108cf118fc8d85ddd831614c`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 782.5 KB (782513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b2a4e9a01427f7604acf929bf5d708369cff7bc24cfa7d0c012c8589bc32450`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 23.0 KB (22960 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.5.1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:ad74b8922ba82d4cc6b9d562384bc8e5cc6d53864ea2bc66078696d7397cdafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49501857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34acd28bc2bbd82e5e73375c4a90f7169c780bc2d0e6c41ca9e0c5d4f74b7ade`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:32:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:32:45 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 00:39:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:39:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:39:34 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:38:03 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Fri, 17 Apr 2026 01:38:26 GMT
ENV SATOSA_VERSION=8.5.1
# Fri, 17 Apr 2026 01:38:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
WORKDIR /etc/satosa
# Fri, 17 Apr 2026 01:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:38:27 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 17 Apr 2026 01:38:27 GMT
USER satosa:satosa
# Fri, 17 Apr 2026 01:38:27 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcaff11adfb133e9e9320abbc299cc834c1403c253c3f7ea4ccaab6d6932fa60`  
		Last Modified: Fri, 17 Apr 2026 00:39:41 GMT  
		Size: 457.3 KB (457313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53736ed35b86baa4c031683ba780c3f739bb4f9961f7885b78af60392fbe5836`  
		Last Modified: Fri, 17 Apr 2026 00:39:41 GMT  
		Size: 12.5 MB (12486525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2c305c7606c8ddaf30bedaeaa4c18783036b29fbe2d07fc7eda11e7d1ddc34`  
		Last Modified: Fri, 17 Apr 2026 00:39:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b6dc3325f307fb75ee4f9d98da6f233aeecb5d14c89aed997bf4e4a7779b13`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 6.7 MB (6722767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff746c3bcb9c24e2fffa44e7893b11145a71ccdfe87092818c60c9623c85ed2`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 25.7 MB (25680563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd7e304e8119cfb61e7ee17a3fbbb3da922d4451e07f437b04b287b9f40dba7`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 10.4 KB (10437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971990212ec60ae1f33629f70147ae21a007cb7d5de9f51ca8d4e59285daae35`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 2.1 KB (2077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5.1-alpine3.22` - unknown; unknown

```console
$ docker pull satosa@sha256:efe89864481f12046d4262654db36e678973a38432e6dcadf461cd5fd7b879d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.8 KB (805756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87cf93dfa5044bb65b87291d2d5eebb13f163d81f9ae12b8be61e327fe686e02`

```dockerfile
```

-	Layers:
	-	`sha256:eae9966f053053199b40dcaff83fb353a628619b1d5a607c2eb2c63a81dd97b7`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 782.6 KB (782617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d78e2d97608d25661c448f1e9b7cc46f0db7db9ff9ca118581f492f49b6a11b8`  
		Last Modified: Fri, 17 Apr 2026 01:38:35 GMT  
		Size: 23.1 KB (23139 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.5.1-bookworm`

```console
$ docker pull satosa@sha256:7c907d50804dc6ecbe36c4faa8d54754f386ef005a1e82442a35dcd34b992995
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8.5.1-bookworm` - linux; amd64

```console
$ docker pull satosa@sha256:5655dae76305b96869065034d848eb92090aaa0c388fb6ec10c523acfe64fc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92457715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26bb17950e679e22cf69f7c9e1538ffa56c520b298527c2a9eff0b77a4c6c47c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:59:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:59:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PYTHON_VERSION=3.13.14
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PYTHON_SHA256=639e43243c620a308f968213df9e00f2f8f62332f7adbaa7a7eeb9783057c690
# Wed, 24 Jun 2026 02:10:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 24 Jun 2026 02:10:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 24 Jun 2026 02:10:55 GMT
CMD ["python3"]
# Wed, 24 Jun 2026 02:43:04 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Wed, 24 Jun 2026 02:43:52 GMT
ENV SATOSA_VERSION=8.5.1
# Wed, 24 Jun 2026 02:43:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
WORKDIR /etc/satosa
# Wed, 24 Jun 2026 02:43:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:43:53 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 24 Jun 2026 02:43:53 GMT
USER satosa:satosa
# Wed, 24 Jun 2026 02:43:53 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e26001d5620dfc2698f3a683c497e1cabdcc4757f4ca4ff70e33cb36057df02`  
		Last Modified: Wed, 24 Jun 2026 02:11:04 GMT  
		Size: 3.5 MB (3520812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90b26812a028bfa582bede756e645cf91fe9d05f2991b0862d719a003cce5ed`  
		Last Modified: Wed, 24 Jun 2026 02:11:05 GMT  
		Size: 12.6 MB (12570253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d229a71b9e515d634cb7f17b8bfe71586ed1282edbcfb81faaca1aebd0ed028b`  
		Last Modified: Wed, 24 Jun 2026 02:11:04 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0d169f435410c8068b61f1f86441b66ba63e5b017eb2a7db41dcdb1f48d007`  
		Last Modified: Wed, 24 Jun 2026 02:44:05 GMT  
		Size: 21.6 MB (21598611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5723dc18369d76c11887e05369a995342ca50992ecf72a7d14b766a7164e896b`  
		Last Modified: Wed, 24 Jun 2026 02:44:05 GMT  
		Size: 26.5 MB (26517606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca12e5f4cad01e654ee761cf49288d7dd440d9ac1bdf2cab826b64a9090213c9`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 10.4 KB (10437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1594679d03fab51ca435b90ed827eb2b73e41cfea3f269fafee6cdafb6f6eac`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 2.1 KB (2074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5.1-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:5f98c4b2665f69dcf052d4ab597ff30427c3dc5edd3604a267e79edfca34634e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8b97b41f3b02471095632cc69e5647bbe7f5be1499d8512bd4e4254e0447d3`

```dockerfile
```

-	Layers:
	-	`sha256:9e9a9262540a6671d38ce01f5f543fd48f4096a8b3339ec72d7401b0ed450fc2`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 2.7 MB (2704660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0fe9e7f73f935ef31b3b3d1f07c9a4794a74a0447d0153ddc5dbfaa4e71a7ce`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 22.3 KB (22266 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.5.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e18cfffa9074424656f99d0444260f631f2a354659ba025c73a84abd42bb8226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91562388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab281fe3962b4af7fcd4f4cd9ef08844ba62e49b65cb1c4e070aad6a834c5a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:02:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:02:38 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PYTHON_VERSION=3.13.14
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PYTHON_SHA256=639e43243c620a308f968213df9e00f2f8f62332f7adbaa7a7eeb9783057c690
# Wed, 24 Jun 2026 02:16:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 24 Jun 2026 02:16:22 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 24 Jun 2026 02:16:22 GMT
CMD ["python3"]
# Wed, 24 Jun 2026 03:23:47 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Wed, 24 Jun 2026 03:24:34 GMT
ENV SATOSA_VERSION=8.5.1
# Wed, 24 Jun 2026 03:24:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
WORKDIR /etc/satosa
# Wed, 24 Jun 2026 03:24:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:24:35 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 24 Jun 2026 03:24:35 GMT
USER satosa:satosa
# Wed, 24 Jun 2026 03:24:35 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e03177a4ba5d2a105c80da4d791b999a2c0d8592218bf604937099767dce4`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 3.4 MB (3352640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8112ec847c4c51cc9e087e72458f63645ee819d8f7f5b00b18c78d8b45457b`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 12.5 MB (12472943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4140d7667663a40213044b01b7f98a453c79fa59784459232580dd4608afcdd`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d1353c5acbe10355ef9cfcf93a6db67a29c03e660d0ac1af30cf1e72cb8542`  
		Last Modified: Wed, 24 Jun 2026 03:24:46 GMT  
		Size: 21.5 MB (21451922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25368aad8a3d30bf1e9c31630225e8631f0de92e424d60e2c58e26eaecee3f51`  
		Last Modified: Wed, 24 Jun 2026 03:24:46 GMT  
		Size: 26.1 MB (26149666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9ca620b6bee0b901297e863ac4357db955c3bd67ff01aa0f4e618d6de2ccaf`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 10.4 KB (10442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cccdfcb5100f94f01bec9af80fe397d740ea6bcb32e131db97cbacce527834`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 2.1 KB (2075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5.1-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:cfd648ffe65a01b96b5584990dc074c7a1f1e961a386dcc8446c0372e1ecfac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2727434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76688f62ede38ed94bd9711fb0cfcbfd6e7ab709ab504ef46889c172ef57faf7`

```dockerfile
```

-	Layers:
	-	`sha256:8734d5cd42d0cfe8c59fc9680272074d7b1f4b5ed314e46bbe0b8656d6fed5d7`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 2.7 MB (2704986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f33959acb229dcf2327a93d12ecb800afb9fe3dafc7ab97bba3371cc15ab1a45`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 22.4 KB (22448 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:alpine`

```console
$ docker pull satosa@sha256:635c3bd8a7b1e62eb8f505c7640cf1bdf930cfac6ab7926573baed9958354ba7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:alpine` - linux; amd64

```console
$ docker pull satosa@sha256:e64adbaaaed0ecd676889a71476ffb657b6c96e99ea168202a836e9338daf5da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49591032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245adc8cf01a5f66ff2284be88e273d4841d80dc1a1c3e904abc104fd609db9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:30:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:30:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 00:36:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:36:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:36:29 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:14:35 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
ENV SATOSA_VERSION=8.5.1
# Fri, 17 Apr 2026 01:14:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
WORKDIR /etc/satosa
# Fri, 17 Apr 2026 01:14:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:14:56 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 17 Apr 2026 01:14:56 GMT
USER satosa:satosa
# Fri, 17 Apr 2026 01:14:56 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df730813d20b0cb8062fb76ce24dc8fc02961ddd625cd6be3c86a0bc4dde8e56`  
		Last Modified: Fri, 17 Apr 2026 00:36:36 GMT  
		Size: 455.0 KB (454972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe818d7ffa27044c9667e73b415f9ae4c37a5d5d78c0cc4462423ded6b373a5`  
		Last Modified: Fri, 17 Apr 2026 00:36:36 GMT  
		Size: 12.5 MB (12472237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf71161b7b0782d25e76411844b95d7c41c91a90891d50df620e89e99fe18b8`  
		Last Modified: Fri, 17 Apr 2026 00:36:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8d9dc3a6733c4a32030cfa81ae0f31e2968fd1b1097d14d360df5e799d9bc9`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 6.7 MB (6744550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77426ee3fb08a0c6baa34b9704abd4f7fd61339c643f0a43c04b0f4962c07a93`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 26.1 MB (26098299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92f5d482e5e64b0b81c6a55dbb5a3cda363eb3e4979e4288755506f6d617458`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 10.4 KB (10431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7c65b6d4cd12b071c97dca761ea5c539c9402480aa6da6b50e82cfcf0306cc`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 2.1 KB (2076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:f995f2aa2d9c5f4f425e5c76b9a84833ab0168d8777212eb0fd0a6454b896e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.5 KB (805473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2e4d3867615dc4bcf34d3615fffd2782c10a5980b2e89b2cfc5acf53027d74`

```dockerfile
```

-	Layers:
	-	`sha256:66040d43ba1ffe7cbed77eaa5a76d1f221c9253d108cf118fc8d85ddd831614c`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 782.5 KB (782513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b2a4e9a01427f7604acf929bf5d708369cff7bc24cfa7d0c012c8589bc32450`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 23.0 KB (22960 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:ad74b8922ba82d4cc6b9d562384bc8e5cc6d53864ea2bc66078696d7397cdafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49501857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34acd28bc2bbd82e5e73375c4a90f7169c780bc2d0e6c41ca9e0c5d4f74b7ade`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:32:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:32:45 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 00:39:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:39:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:39:34 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:38:03 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Fri, 17 Apr 2026 01:38:26 GMT
ENV SATOSA_VERSION=8.5.1
# Fri, 17 Apr 2026 01:38:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
WORKDIR /etc/satosa
# Fri, 17 Apr 2026 01:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:38:27 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 17 Apr 2026 01:38:27 GMT
USER satosa:satosa
# Fri, 17 Apr 2026 01:38:27 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcaff11adfb133e9e9320abbc299cc834c1403c253c3f7ea4ccaab6d6932fa60`  
		Last Modified: Fri, 17 Apr 2026 00:39:41 GMT  
		Size: 457.3 KB (457313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53736ed35b86baa4c031683ba780c3f739bb4f9961f7885b78af60392fbe5836`  
		Last Modified: Fri, 17 Apr 2026 00:39:41 GMT  
		Size: 12.5 MB (12486525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2c305c7606c8ddaf30bedaeaa4c18783036b29fbe2d07fc7eda11e7d1ddc34`  
		Last Modified: Fri, 17 Apr 2026 00:39:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b6dc3325f307fb75ee4f9d98da6f233aeecb5d14c89aed997bf4e4a7779b13`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 6.7 MB (6722767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff746c3bcb9c24e2fffa44e7893b11145a71ccdfe87092818c60c9623c85ed2`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 25.7 MB (25680563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd7e304e8119cfb61e7ee17a3fbbb3da922d4451e07f437b04b287b9f40dba7`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 10.4 KB (10437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971990212ec60ae1f33629f70147ae21a007cb7d5de9f51ca8d4e59285daae35`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 2.1 KB (2077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:efe89864481f12046d4262654db36e678973a38432e6dcadf461cd5fd7b879d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.8 KB (805756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87cf93dfa5044bb65b87291d2d5eebb13f163d81f9ae12b8be61e327fe686e02`

```dockerfile
```

-	Layers:
	-	`sha256:eae9966f053053199b40dcaff83fb353a628619b1d5a607c2eb2c63a81dd97b7`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 782.6 KB (782617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d78e2d97608d25661c448f1e9b7cc46f0db7db9ff9ca118581f492f49b6a11b8`  
		Last Modified: Fri, 17 Apr 2026 01:38:35 GMT  
		Size: 23.1 KB (23139 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:alpine3.22`

```console
$ docker pull satosa@sha256:635c3bd8a7b1e62eb8f505c7640cf1bdf930cfac6ab7926573baed9958354ba7
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:alpine3.22` - linux; amd64

```console
$ docker pull satosa@sha256:e64adbaaaed0ecd676889a71476ffb657b6c96e99ea168202a836e9338daf5da
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49591032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:245adc8cf01a5f66ff2284be88e273d4841d80dc1a1c3e904abc104fd609db9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:02 GMT
ADD alpine-minirootfs-3.22.4-x86_64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:02 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:30:52 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:30:52 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 00:30:52 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 00:36:29 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:36:29 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:36:29 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:14:35 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
ENV SATOSA_VERSION=8.5.1
# Fri, 17 Apr 2026 01:14:56 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
WORKDIR /etc/satosa
# Fri, 17 Apr 2026 01:14:56 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:14:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:14:56 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 17 Apr 2026 01:14:56 GMT
USER satosa:satosa
# Fri, 17 Apr 2026 01:14:56 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:84f5eff04246b56d48d1ed6cbd82d6bc7e53f7e790db6a467f92571c69f3289e`  
		Last Modified: Thu, 16 Apr 2026 23:53:07 GMT  
		Size: 3.8 MB (3808189 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:df730813d20b0cb8062fb76ce24dc8fc02961ddd625cd6be3c86a0bc4dde8e56`  
		Last Modified: Fri, 17 Apr 2026 00:36:36 GMT  
		Size: 455.0 KB (454972 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ffe818d7ffa27044c9667e73b415f9ae4c37a5d5d78c0cc4462423ded6b373a5`  
		Last Modified: Fri, 17 Apr 2026 00:36:36 GMT  
		Size: 12.5 MB (12472237 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4cf71161b7b0782d25e76411844b95d7c41c91a90891d50df620e89e99fe18b8`  
		Last Modified: Fri, 17 Apr 2026 00:36:35 GMT  
		Size: 246.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e8d9dc3a6733c4a32030cfa81ae0f31e2968fd1b1097d14d360df5e799d9bc9`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 6.7 MB (6744550 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77426ee3fb08a0c6baa34b9704abd4f7fd61339c643f0a43c04b0f4962c07a93`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 26.1 MB (26098299 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f92f5d482e5e64b0b81c6a55dbb5a3cda363eb3e4979e4288755506f6d617458`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 10.4 KB (10431 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3b7c65b6d4cd12b071c97dca761ea5c539c9402480aa6da6b50e82cfcf0306cc`  
		Last Modified: Fri, 17 Apr 2026 01:15:06 GMT  
		Size: 2.1 KB (2076 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:alpine3.22` - unknown; unknown

```console
$ docker pull satosa@sha256:f995f2aa2d9c5f4f425e5c76b9a84833ab0168d8777212eb0fd0a6454b896e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.5 KB (805473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7b2e4d3867615dc4bcf34d3615fffd2782c10a5980b2e89b2cfc5acf53027d74`

```dockerfile
```

-	Layers:
	-	`sha256:66040d43ba1ffe7cbed77eaa5a76d1f221c9253d108cf118fc8d85ddd831614c`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 782.5 KB (782513 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7b2a4e9a01427f7604acf929bf5d708369cff7bc24cfa7d0c012c8589bc32450`  
		Last Modified: Fri, 17 Apr 2026 01:15:05 GMT  
		Size: 23.0 KB (22960 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:ad74b8922ba82d4cc6b9d562384bc8e5cc6d53864ea2bc66078696d7397cdafb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49501857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:34acd28bc2bbd82e5e73375c4a90f7169c780bc2d0e6c41ca9e0c5d4f74b7ade`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Thu, 16 Apr 2026 23:53:00 GMT
ADD alpine-minirootfs-3.22.4-aarch64.tar.gz / # buildkit
# Thu, 16 Apr 2026 23:53:00 GMT
CMD ["/bin/sh"]
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Fri, 17 Apr 2026 00:32:45 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Fri, 17 Apr 2026 00:32:45 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PYTHON_VERSION=3.13.13
# Fri, 17 Apr 2026 00:32:45 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Fri, 17 Apr 2026 00:39:34 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(apk --print-arch)"; 	case "$arch" in 		x86_64|aarch64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		x86) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Fri, 17 Apr 2026 00:39:34 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Fri, 17 Apr 2026 00:39:34 GMT
CMD ["python3"]
# Fri, 17 Apr 2026 01:38:03 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Fri, 17 Apr 2026 01:38:26 GMT
ENV SATOSA_VERSION=8.5.1
# Fri, 17 Apr 2026 01:38:26 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
WORKDIR /etc/satosa
# Fri, 17 Apr 2026 01:38:27 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Fri, 17 Apr 2026 01:38:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 17 Apr 2026 01:38:27 GMT
EXPOSE map[8080/tcp:{}]
# Fri, 17 Apr 2026 01:38:27 GMT
USER satosa:satosa
# Fri, 17 Apr 2026 01:38:27 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:58e777220c395c319866c5d73ea32a5ea574bbd12f4eb289b392f584d0cd953e`  
		Last Modified: Thu, 16 Apr 2026 23:53:05 GMT  
		Size: 4.1 MB (4141894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dcaff11adfb133e9e9320abbc299cc834c1403c253c3f7ea4ccaab6d6932fa60`  
		Last Modified: Fri, 17 Apr 2026 00:39:41 GMT  
		Size: 457.3 KB (457313 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53736ed35b86baa4c031683ba780c3f739bb4f9961f7885b78af60392fbe5836`  
		Last Modified: Fri, 17 Apr 2026 00:39:41 GMT  
		Size: 12.5 MB (12486525 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f2c305c7606c8ddaf30bedaeaa4c18783036b29fbe2d07fc7eda11e7d1ddc34`  
		Last Modified: Fri, 17 Apr 2026 00:39:40 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c5b6dc3325f307fb75ee4f9d98da6f233aeecb5d14c89aed997bf4e4a7779b13`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 6.7 MB (6722767 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bff746c3bcb9c24e2fffa44e7893b11145a71ccdfe87092818c60c9623c85ed2`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 25.7 MB (25680563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dbd7e304e8119cfb61e7ee17a3fbbb3da922d4451e07f437b04b287b9f40dba7`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 10.4 KB (10437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:971990212ec60ae1f33629f70147ae21a007cb7d5de9f51ca8d4e59285daae35`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 2.1 KB (2077 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:alpine3.22` - unknown; unknown

```console
$ docker pull satosa@sha256:efe89864481f12046d4262654db36e678973a38432e6dcadf461cd5fd7b879d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **805.8 KB (805756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:87cf93dfa5044bb65b87291d2d5eebb13f163d81f9ae12b8be61e327fe686e02`

```dockerfile
```

-	Layers:
	-	`sha256:eae9966f053053199b40dcaff83fb353a628619b1d5a607c2eb2c63a81dd97b7`  
		Last Modified: Fri, 17 Apr 2026 01:38:36 GMT  
		Size: 782.6 KB (782617 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d78e2d97608d25661c448f1e9b7cc46f0db7db9ff9ca118581f492f49b6a11b8`  
		Last Modified: Fri, 17 Apr 2026 01:38:35 GMT  
		Size: 23.1 KB (23139 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:bookworm`

```console
$ docker pull satosa@sha256:7c907d50804dc6ecbe36c4faa8d54754f386ef005a1e82442a35dcd34b992995
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:bookworm` - linux; amd64

```console
$ docker pull satosa@sha256:5655dae76305b96869065034d848eb92090aaa0c388fb6ec10c523acfe64fc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92457715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26bb17950e679e22cf69f7c9e1538ffa56c520b298527c2a9eff0b77a4c6c47c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:59:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:59:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PYTHON_VERSION=3.13.14
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PYTHON_SHA256=639e43243c620a308f968213df9e00f2f8f62332f7adbaa7a7eeb9783057c690
# Wed, 24 Jun 2026 02:10:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 24 Jun 2026 02:10:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 24 Jun 2026 02:10:55 GMT
CMD ["python3"]
# Wed, 24 Jun 2026 02:43:04 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Wed, 24 Jun 2026 02:43:52 GMT
ENV SATOSA_VERSION=8.5.1
# Wed, 24 Jun 2026 02:43:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
WORKDIR /etc/satosa
# Wed, 24 Jun 2026 02:43:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:43:53 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 24 Jun 2026 02:43:53 GMT
USER satosa:satosa
# Wed, 24 Jun 2026 02:43:53 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e26001d5620dfc2698f3a683c497e1cabdcc4757f4ca4ff70e33cb36057df02`  
		Last Modified: Wed, 24 Jun 2026 02:11:04 GMT  
		Size: 3.5 MB (3520812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90b26812a028bfa582bede756e645cf91fe9d05f2991b0862d719a003cce5ed`  
		Last Modified: Wed, 24 Jun 2026 02:11:05 GMT  
		Size: 12.6 MB (12570253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d229a71b9e515d634cb7f17b8bfe71586ed1282edbcfb81faaca1aebd0ed028b`  
		Last Modified: Wed, 24 Jun 2026 02:11:04 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0d169f435410c8068b61f1f86441b66ba63e5b017eb2a7db41dcdb1f48d007`  
		Last Modified: Wed, 24 Jun 2026 02:44:05 GMT  
		Size: 21.6 MB (21598611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5723dc18369d76c11887e05369a995342ca50992ecf72a7d14b766a7164e896b`  
		Last Modified: Wed, 24 Jun 2026 02:44:05 GMT  
		Size: 26.5 MB (26517606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca12e5f4cad01e654ee761cf49288d7dd440d9ac1bdf2cab826b64a9090213c9`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 10.4 KB (10437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1594679d03fab51ca435b90ed827eb2b73e41cfea3f269fafee6cdafb6f6eac`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 2.1 KB (2074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:5f98c4b2665f69dcf052d4ab597ff30427c3dc5edd3604a267e79edfca34634e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8b97b41f3b02471095632cc69e5647bbe7f5be1499d8512bd4e4254e0447d3`

```dockerfile
```

-	Layers:
	-	`sha256:9e9a9262540a6671d38ce01f5f543fd48f4096a8b3339ec72d7401b0ed450fc2`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 2.7 MB (2704660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0fe9e7f73f935ef31b3b3d1f07c9a4794a74a0447d0153ddc5dbfaa4e71a7ce`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 22.3 KB (22266 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:bookworm` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e18cfffa9074424656f99d0444260f631f2a354659ba025c73a84abd42bb8226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91562388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab281fe3962b4af7fcd4f4cd9ef08844ba62e49b65cb1c4e070aad6a834c5a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:02:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:02:38 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PYTHON_VERSION=3.13.14
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PYTHON_SHA256=639e43243c620a308f968213df9e00f2f8f62332f7adbaa7a7eeb9783057c690
# Wed, 24 Jun 2026 02:16:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 24 Jun 2026 02:16:22 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 24 Jun 2026 02:16:22 GMT
CMD ["python3"]
# Wed, 24 Jun 2026 03:23:47 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Wed, 24 Jun 2026 03:24:34 GMT
ENV SATOSA_VERSION=8.5.1
# Wed, 24 Jun 2026 03:24:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
WORKDIR /etc/satosa
# Wed, 24 Jun 2026 03:24:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:24:35 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 24 Jun 2026 03:24:35 GMT
USER satosa:satosa
# Wed, 24 Jun 2026 03:24:35 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e03177a4ba5d2a105c80da4d791b999a2c0d8592218bf604937099767dce4`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 3.4 MB (3352640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8112ec847c4c51cc9e087e72458f63645ee819d8f7f5b00b18c78d8b45457b`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 12.5 MB (12472943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4140d7667663a40213044b01b7f98a453c79fa59784459232580dd4608afcdd`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d1353c5acbe10355ef9cfcf93a6db67a29c03e660d0ac1af30cf1e72cb8542`  
		Last Modified: Wed, 24 Jun 2026 03:24:46 GMT  
		Size: 21.5 MB (21451922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25368aad8a3d30bf1e9c31630225e8631f0de92e424d60e2c58e26eaecee3f51`  
		Last Modified: Wed, 24 Jun 2026 03:24:46 GMT  
		Size: 26.1 MB (26149666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9ca620b6bee0b901297e863ac4357db955c3bd67ff01aa0f4e618d6de2ccaf`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 10.4 KB (10442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cccdfcb5100f94f01bec9af80fe397d740ea6bcb32e131db97cbacce527834`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 2.1 KB (2075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:cfd648ffe65a01b96b5584990dc074c7a1f1e961a386dcc8446c0372e1ecfac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2727434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76688f62ede38ed94bd9711fb0cfcbfd6e7ab709ab504ef46889c172ef57faf7`

```dockerfile
```

-	Layers:
	-	`sha256:8734d5cd42d0cfe8c59fc9680272074d7b1f4b5ed314e46bbe0b8656d6fed5d7`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 2.7 MB (2704986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f33959acb229dcf2327a93d12ecb800afb9fe3dafc7ab97bba3371cc15ab1a45`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 22.4 KB (22448 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:latest`

```console
$ docker pull satosa@sha256:7c907d50804dc6ecbe36c4faa8d54754f386ef005a1e82442a35dcd34b992995
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:latest` - linux; amd64

```console
$ docker pull satosa@sha256:5655dae76305b96869065034d848eb92090aaa0c388fb6ec10c523acfe64fc62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.5 MB (92457715 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26bb17950e679e22cf69f7c9e1538ffa56c520b298527c2a9eff0b77a4c6c47c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 01:59:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 01:59:00 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PYTHON_VERSION=3.13.14
# Wed, 24 Jun 2026 01:59:00 GMT
ENV PYTHON_SHA256=639e43243c620a308f968213df9e00f2f8f62332f7adbaa7a7eeb9783057c690
# Wed, 24 Jun 2026 02:10:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 24 Jun 2026 02:10:55 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 24 Jun 2026 02:10:55 GMT
CMD ["python3"]
# Wed, 24 Jun 2026 02:43:04 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Wed, 24 Jun 2026 02:43:52 GMT
ENV SATOSA_VERSION=8.5.1
# Wed, 24 Jun 2026 02:43:52 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
WORKDIR /etc/satosa
# Wed, 24 Jun 2026 02:43:53 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 02:43:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 02:43:53 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 24 Jun 2026 02:43:53 GMT
USER satosa:satosa
# Wed, 24 Jun 2026 02:43:53 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:68629629b516c3cd6f5e71ffbe18e32afb1ae5b4926c92d058c0f11ef1fd58a3`  
		Last Modified: Wed, 24 Jun 2026 00:27:52 GMT  
		Size: 28.2 MB (28237639 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e26001d5620dfc2698f3a683c497e1cabdcc4757f4ca4ff70e33cb36057df02`  
		Last Modified: Wed, 24 Jun 2026 02:11:04 GMT  
		Size: 3.5 MB (3520812 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c90b26812a028bfa582bede756e645cf91fe9d05f2991b0862d719a003cce5ed`  
		Last Modified: Wed, 24 Jun 2026 02:11:05 GMT  
		Size: 12.6 MB (12570253 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d229a71b9e515d634cb7f17b8bfe71586ed1282edbcfb81faaca1aebd0ed028b`  
		Last Modified: Wed, 24 Jun 2026 02:11:04 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f0d169f435410c8068b61f1f86441b66ba63e5b017eb2a7db41dcdb1f48d007`  
		Last Modified: Wed, 24 Jun 2026 02:44:05 GMT  
		Size: 21.6 MB (21598611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5723dc18369d76c11887e05369a995342ca50992ecf72a7d14b766a7164e896b`  
		Last Modified: Wed, 24 Jun 2026 02:44:05 GMT  
		Size: 26.5 MB (26517606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ca12e5f4cad01e654ee761cf49288d7dd440d9ac1bdf2cab826b64a9090213c9`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 10.4 KB (10437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b1594679d03fab51ca435b90ed827eb2b73e41cfea3f269fafee6cdafb6f6eac`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 2.1 KB (2074 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:latest` - unknown; unknown

```console
$ docker pull satosa@sha256:5f98c4b2665f69dcf052d4ab597ff30427c3dc5edd3604a267e79edfca34634e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726926 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd8b97b41f3b02471095632cc69e5647bbe7f5be1499d8512bd4e4254e0447d3`

```dockerfile
```

-	Layers:
	-	`sha256:9e9a9262540a6671d38ce01f5f543fd48f4096a8b3339ec72d7401b0ed450fc2`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 2.7 MB (2704660 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0fe9e7f73f935ef31b3b3d1f07c9a4794a74a0447d0153ddc5dbfaa4e71a7ce`  
		Last Modified: Wed, 24 Jun 2026 02:44:04 GMT  
		Size: 22.3 KB (22266 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:latest` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e18cfffa9074424656f99d0444260f631f2a354659ba025c73a84abd42bb8226
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91562388 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dab281fe3962b4af7fcd4f4cd9ef08844ba62e49b65cb1c4e070aad6a834c5a7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Tue, 23 Jun 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1782172800'
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 24 Jun 2026 02:02:38 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Wed, 24 Jun 2026 02:02:38 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PYTHON_VERSION=3.13.14
# Wed, 24 Jun 2026 02:02:38 GMT
ENV PYTHON_SHA256=639e43243c620a308f968213df9e00f2f8f62332f7adbaa7a7eeb9783057c690
# Wed, 24 Jun 2026 02:16:22 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 24 Jun 2026 02:16:22 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 24 Jun 2026 02:16:22 GMT
CMD ["python3"]
# Wed, 24 Jun 2026 03:23:47 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Wed, 24 Jun 2026 03:24:34 GMT
ENV SATOSA_VERSION=8.5.1
# Wed, 24 Jun 2026 03:24:34 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
WORKDIR /etc/satosa
# Wed, 24 Jun 2026 03:24:35 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Wed, 24 Jun 2026 03:24:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Jun 2026 03:24:35 GMT
EXPOSE map[8080/tcp:{}]
# Wed, 24 Jun 2026 03:24:35 GMT
USER satosa:satosa
# Wed, 24 Jun 2026 03:24:35 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:74f1dcfcc9c80045f6f6394ffcfc261cb19d0c71b97e964aec3d4abf4e0f7009`  
		Last Modified: Wed, 24 Jun 2026 00:27:48 GMT  
		Size: 28.1 MB (28122418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb8e03177a4ba5d2a105c80da4d791b999a2c0d8592218bf604937099767dce4`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 3.4 MB (3352640 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dd8112ec847c4c51cc9e087e72458f63645ee819d8f7f5b00b18c78d8b45457b`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 12.5 MB (12472943 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d4140d7667663a40213044b01b7f98a453c79fa59784459232580dd4608afcdd`  
		Last Modified: Wed, 24 Jun 2026 02:16:31 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:66d1353c5acbe10355ef9cfcf93a6db67a29c03e660d0ac1af30cf1e72cb8542`  
		Last Modified: Wed, 24 Jun 2026 03:24:46 GMT  
		Size: 21.5 MB (21451922 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:25368aad8a3d30bf1e9c31630225e8631f0de92e424d60e2c58e26eaecee3f51`  
		Last Modified: Wed, 24 Jun 2026 03:24:46 GMT  
		Size: 26.1 MB (26149666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a9ca620b6bee0b901297e863ac4357db955c3bd67ff01aa0f4e618d6de2ccaf`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 10.4 KB (10442 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:70cccdfcb5100f94f01bec9af80fe397d740ea6bcb32e131db97cbacce527834`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 2.1 KB (2075 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:latest` - unknown; unknown

```console
$ docker pull satosa@sha256:cfd648ffe65a01b96b5584990dc074c7a1f1e961a386dcc8446c0372e1ecfac0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2727434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76688f62ede38ed94bd9711fb0cfcbfd6e7ab709ab504ef46889c172ef57faf7`

```dockerfile
```

-	Layers:
	-	`sha256:8734d5cd42d0cfe8c59fc9680272074d7b1f4b5ed314e46bbe0b8656d6fed5d7`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 2.7 MB (2704986 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f33959acb229dcf2327a93d12ecb800afb9fe3dafc7ab97bba3371cc15ab1a45`  
		Last Modified: Wed, 24 Jun 2026 03:24:45 GMT  
		Size: 22.4 KB (22448 bytes)  
		MIME: application/vnd.in-toto+json
