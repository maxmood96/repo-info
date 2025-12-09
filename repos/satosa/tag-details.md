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
$ docker pull satosa@sha256:47cab947e2477f7a89747951af0cca8f8d911c9807dc8aa2d0a0eb66d2b0b5d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8` - linux; amd64

```console
$ docker pull satosa@sha256:02d11444e8397d8cf844cfe4966790e8acd11bb96df692b0d2246fdc4b84e724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91546319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fdbbd78fb77c1c45bf4c6de659e0b646927937253d1ea05101ef20673dc9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:33:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:33:46 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:43:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:43:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:43:53 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:11:52 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:12:46 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:12:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:12:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:12:47 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:12:47 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:12:47 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009f5cc336e3b76a99df531b878e328e7a550219c8956a8a194aa3b0d195db91`  
		Last Modified: Mon, 08 Dec 2025 20:44:07 GMT  
		Size: 3.5 MB (3515868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661abbc8fe10b243e7e573653867ccaa905ddb32a37a534e407d8d13edf850b`  
		Last Modified: Mon, 08 Dec 2025 20:44:12 GMT  
		Size: 12.5 MB (12470573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed91f2f794eb4b70d66bbfdcc185d49c206fe04adc5a2342583287af687d5a1`  
		Last Modified: Mon, 08 Dec 2025 20:44:07 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79acb76c9c0b4b230bfe39a96674638997c6e3e604a3ac06679eff10f301a3ed`  
		Last Modified: Mon, 08 Dec 2025 21:13:17 GMT  
		Size: 21.5 MB (21456825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2375cde2b745416d789de4916d59cca9acbe71b560fab10770ef2334ab8b7c0`  
		Last Modified: Mon, 08 Dec 2025 21:13:24 GMT  
		Size: 25.9 MB (25861803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb2815d937de7372beed80131c8ea74f531bfef1e5e42327f78e5845b8d3a94`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 10.4 KB (10441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddafdd0c89bdf32c613738b8bf29e31ecf1b9378a6090d858a7161e166ad0ea`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8` - unknown; unknown

```console
$ docker pull satosa@sha256:ba2a77056920b0b8c29c5c1cd5b4ad488cd5d77b6b98a2c1d8fb0b8166659112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139237f34ca29fe7e6eca10a086e04e1388e05fb722c6a11c6898ee2afc51c90`

```dockerfile
```

-	Layers:
	-	`sha256:74f9eb40f65c4cc8706a37a324099d2b084fa1e4996275f01a193b1dedc06bc4`  
		Last Modified: Mon, 08 Dec 2025 23:13:58 GMT  
		Size: 2.7 MB (2704633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59c7c8a0e3d3d3e331479afb101f477f0105ef999c2fec379b98c7e55d61f69b`  
		Last Modified: Mon, 08 Dec 2025 23:13:59 GMT  
		Size: 22.3 KB (22266 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e6034f8923cc420bf624c03933ca51d3fa3fa53369e574d01519048130a6ea08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90626193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a048ae55480d2f33d8cfc4e898989706e7365329e4c1dd6033c938644b7e9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:10:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:10:26 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:23:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:23:02 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:23:02 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:10:47 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:11:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:11:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:11:36 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:11:36 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:11:36 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067a176e286689d9a5616e9a9ccb474753231475a3b74b8c4eb6897476010420`  
		Last Modified: Mon, 08 Dec 2025 20:37:28 GMT  
		Size: 3.3 MB (3349161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fc0b8bf8e30d988c0f398a3673770af657a9ad94ba5605b3c5ff9927aa69d4`  
		Last Modified: Mon, 08 Dec 2025 21:10:40 GMT  
		Size: 12.4 MB (12372485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfc60c769de0a434549492e317c8c2ff2cae1e4a35d3c369d631538c2588087`  
		Last Modified: Mon, 08 Dec 2025 20:37:37 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572f90ee4f08e9e7e4545f1fec7a2502d142eddf118a4fd7bf2645c7be56ef69`  
		Last Modified: Mon, 08 Dec 2025 21:12:08 GMT  
		Size: 21.3 MB (21306657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8001b73c61fa8c9d9ac229832e7a11cf353654a05001f5774eddb626e0a8e`  
		Last Modified: Mon, 08 Dec 2025 21:12:13 GMT  
		Size: 25.5 MB (25482878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8968998041481e37921326fcbf07ff2ed641dcba0c5c05dca511426bf6870817`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 10.4 KB (10439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebca083d50d345d85ac73c6847800d6f5240548843ad64f9930b46be656536d`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8` - unknown; unknown

```console
$ docker pull satosa@sha256:1b7e4ec015d578ac03adee68f7e1eef5a0a20228c6bdb3e3e7a0aa69ba363f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2727406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef91488e298c4cf89b88685f361b8c0e0b25207e9096cc5309b29b59e8087d0`

```dockerfile
```

-	Layers:
	-	`sha256:c2688d87a56f8ed7f757ae7f9a2eca3beece73a77533054ff78d0b527bd9a223`  
		Last Modified: Mon, 08 Dec 2025 23:14:03 GMT  
		Size: 2.7 MB (2704959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a6c70eeb25bdce5e4963b184cbb29ab0ecd0c886fe9ce1ac44cfda2be17eebf`  
		Last Modified: Mon, 08 Dec 2025 23:14:04 GMT  
		Size: 22.4 KB (22447 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8-alpine`

```console
$ docker pull satosa@sha256:adedc568ec1d96b84febaeaeccdf3b6741cee3c12af9843c693bbc7ae51d2c8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8-alpine` - linux; amd64

```console
$ docker pull satosa@sha256:e121448d38b02e6ee0e78f99e088425663bfd6747886f0efce468291c3f62f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49149075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ccd9369292b929b0366109da11f96c50afebbfadcedc880613ce2ce475cb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:30:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:30:58 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:36:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:36:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:36:20 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:12:34 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:12:54 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:12:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:12:55 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:12:55 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:12:55 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26daf640290a5c96818eeceda9d0ca2e9fc41fc3a6b57a9042ed93a479c15161`  
		Last Modified: Mon, 08 Dec 2025 20:36:32 GMT  
		Size: 456.9 KB (456928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b1972ad510f9ac01c1a925be2d191877631aa1ac5fb973b6e7bd8bcb4133e2`  
		Last Modified: Mon, 08 Dec 2025 20:36:33 GMT  
		Size: 12.4 MB (12438092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25dc0fb9705edc6661711090bbb88c90560b516b861680a35178aaf986296a8`  
		Last Modified: Mon, 08 Dec 2025 20:36:32 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df3e3c3fcc2bba3d34c49be0a42c155b93ce4bf7434accf72beafb185d61011`  
		Last Modified: Mon, 08 Dec 2025 21:13:14 GMT  
		Size: 6.7 MB (6717688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249b2e05caedcdb9b33eae3134a31c6903ef0ebe4bd1fb7524fb6372d1336bf8`  
		Last Modified: Mon, 08 Dec 2025 21:13:18 GMT  
		Size: 25.7 MB (25721114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5521ff6cf19924b06d81d65132085a2884c9d16ef8d12f8b33a7ab10892a2c1d`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 10.4 KB (10438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fbb063fad282ec1ecd0eda6d419d1179e9ba7908dd0a38496b03a8976084e4`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 2.1 KB (2080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:053b3548aded493f8b8d389ffdfa856d72a53956ec08f9d6cb9d1a0562071613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **806.2 KB (806179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fdc00dcb12fdc98bc985aa473ee27ce5e931601d5e426d2ed8c559491bc45b7`

```dockerfile
```

-	Layers:
	-	`sha256:de6df0a0041eccd13155e23b861f0a62034e6a8535664f050f8341328c38b9d4`  
		Last Modified: Mon, 08 Dec 2025 23:14:06 GMT  
		Size: 783.2 KB (783219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa32fe9c93af693fbacaf0283ddfeb2882849bc3b6e1066ee29e4dd85060f1fa`  
		Last Modified: Mon, 08 Dec 2025 23:14:07 GMT  
		Size: 23.0 KB (22960 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8-alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:092eadb6a3d49e7ac1803172ff64eed6c55596b94ae18393e4e83e917bf1abc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49093844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643ccb5cb566e62f38c946f4ed47ccf98a3dea79baf075ae1d9f2b8bf1b151e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:13:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:13:36 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:20:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:20:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:20:06 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:11:21 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:11:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:11:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:11:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:11:44 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:11:44 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:11:44 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04eda5d87448437994b338947f03a72065bf589d08071ba33ba5dc3ea1ddcf9`  
		Last Modified: Mon, 08 Dec 2025 20:20:23 GMT  
		Size: 459.0 KB (459020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19756ed87e004e14deeb5d042df980b7204f44649d4cce479201223a8589ab`  
		Last Modified: Mon, 08 Dec 2025 20:20:23 GMT  
		Size: 12.5 MB (12453549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be90ee3c5e8855f927e9dabc42fd16e3baec85cb245b81e43412665495c6b4a`  
		Last Modified: Mon, 08 Dec 2025 20:20:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a131be40642a2cf885cdcb75474faaf4e6651804fc3f8cd6201c9960ca7d3f`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 6.7 MB (6694259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a8917a69ecc315188c393d384a8726146e9a2226632ec028e7e54a5546c701`  
		Last Modified: Mon, 08 Dec 2025 21:12:08 GMT  
		Size: 25.3 MB (25336149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b79bc7d0a94fb0a4eaa2b1cace6bf0e4b799d4e76449fa4b17cf2d02f9ed1a4`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 10.4 KB (10440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd5054ceea4ea2377c4734c970adf4f763deaeaaa9e72dca0fbc2beda863685`  
		Last Modified: Mon, 08 Dec 2025 21:12:05 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:fbfef43bbeaf94239cde0843248f928b598c0b683f6e8a8209428bceede91894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **806.5 KB (806465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f04a24d13f86b5d751637955c00828100756cb72f170fb3422f7cd5bc8c6773`

```dockerfile
```

-	Layers:
	-	`sha256:fbe4e8fa0a2a61b3f561fcd5420ad68fb6cc07c61a2592e567ab105acdab481d`  
		Last Modified: Mon, 08 Dec 2025 23:14:10 GMT  
		Size: 783.3 KB (783323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24efd495e1ac9fb1735f89706533f4d82e1c5bc1d3747b3cb4d0a599225a46fb`  
		Last Modified: Mon, 08 Dec 2025 23:14:11 GMT  
		Size: 23.1 KB (23142 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8-alpine3.22`

```console
$ docker pull satosa@sha256:adedc568ec1d96b84febaeaeccdf3b6741cee3c12af9843c693bbc7ae51d2c8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8-alpine3.22` - linux; amd64

```console
$ docker pull satosa@sha256:e121448d38b02e6ee0e78f99e088425663bfd6747886f0efce468291c3f62f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49149075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ccd9369292b929b0366109da11f96c50afebbfadcedc880613ce2ce475cb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:30:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:30:58 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:36:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:36:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:36:20 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:12:34 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:12:54 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:12:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:12:55 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:12:55 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:12:55 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26daf640290a5c96818eeceda9d0ca2e9fc41fc3a6b57a9042ed93a479c15161`  
		Last Modified: Mon, 08 Dec 2025 20:36:32 GMT  
		Size: 456.9 KB (456928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b1972ad510f9ac01c1a925be2d191877631aa1ac5fb973b6e7bd8bcb4133e2`  
		Last Modified: Mon, 08 Dec 2025 20:36:33 GMT  
		Size: 12.4 MB (12438092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25dc0fb9705edc6661711090bbb88c90560b516b861680a35178aaf986296a8`  
		Last Modified: Mon, 08 Dec 2025 20:36:32 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df3e3c3fcc2bba3d34c49be0a42c155b93ce4bf7434accf72beafb185d61011`  
		Last Modified: Mon, 08 Dec 2025 21:13:14 GMT  
		Size: 6.7 MB (6717688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249b2e05caedcdb9b33eae3134a31c6903ef0ebe4bd1fb7524fb6372d1336bf8`  
		Last Modified: Mon, 08 Dec 2025 21:13:18 GMT  
		Size: 25.7 MB (25721114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5521ff6cf19924b06d81d65132085a2884c9d16ef8d12f8b33a7ab10892a2c1d`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 10.4 KB (10438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fbb063fad282ec1ecd0eda6d419d1179e9ba7908dd0a38496b03a8976084e4`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 2.1 KB (2080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-alpine3.22` - unknown; unknown

```console
$ docker pull satosa@sha256:053b3548aded493f8b8d389ffdfa856d72a53956ec08f9d6cb9d1a0562071613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **806.2 KB (806179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fdc00dcb12fdc98bc985aa473ee27ce5e931601d5e426d2ed8c559491bc45b7`

```dockerfile
```

-	Layers:
	-	`sha256:de6df0a0041eccd13155e23b861f0a62034e6a8535664f050f8341328c38b9d4`  
		Last Modified: Mon, 08 Dec 2025 23:14:06 GMT  
		Size: 783.2 KB (783219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa32fe9c93af693fbacaf0283ddfeb2882849bc3b6e1066ee29e4dd85060f1fa`  
		Last Modified: Mon, 08 Dec 2025 23:14:07 GMT  
		Size: 23.0 KB (22960 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:092eadb6a3d49e7ac1803172ff64eed6c55596b94ae18393e4e83e917bf1abc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49093844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643ccb5cb566e62f38c946f4ed47ccf98a3dea79baf075ae1d9f2b8bf1b151e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:13:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:13:36 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:20:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:20:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:20:06 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:11:21 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:11:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:11:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:11:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:11:44 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:11:44 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:11:44 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04eda5d87448437994b338947f03a72065bf589d08071ba33ba5dc3ea1ddcf9`  
		Last Modified: Mon, 08 Dec 2025 20:20:23 GMT  
		Size: 459.0 KB (459020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19756ed87e004e14deeb5d042df980b7204f44649d4cce479201223a8589ab`  
		Last Modified: Mon, 08 Dec 2025 20:20:23 GMT  
		Size: 12.5 MB (12453549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be90ee3c5e8855f927e9dabc42fd16e3baec85cb245b81e43412665495c6b4a`  
		Last Modified: Mon, 08 Dec 2025 20:20:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a131be40642a2cf885cdcb75474faaf4e6651804fc3f8cd6201c9960ca7d3f`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 6.7 MB (6694259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a8917a69ecc315188c393d384a8726146e9a2226632ec028e7e54a5546c701`  
		Last Modified: Mon, 08 Dec 2025 21:12:08 GMT  
		Size: 25.3 MB (25336149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b79bc7d0a94fb0a4eaa2b1cace6bf0e4b799d4e76449fa4b17cf2d02f9ed1a4`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 10.4 KB (10440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd5054ceea4ea2377c4734c970adf4f763deaeaaa9e72dca0fbc2beda863685`  
		Last Modified: Mon, 08 Dec 2025 21:12:05 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-alpine3.22` - unknown; unknown

```console
$ docker pull satosa@sha256:fbfef43bbeaf94239cde0843248f928b598c0b683f6e8a8209428bceede91894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **806.5 KB (806465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f04a24d13f86b5d751637955c00828100756cb72f170fb3422f7cd5bc8c6773`

```dockerfile
```

-	Layers:
	-	`sha256:fbe4e8fa0a2a61b3f561fcd5420ad68fb6cc07c61a2592e567ab105acdab481d`  
		Last Modified: Mon, 08 Dec 2025 23:14:10 GMT  
		Size: 783.3 KB (783323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24efd495e1ac9fb1735f89706533f4d82e1c5bc1d3747b3cb4d0a599225a46fb`  
		Last Modified: Mon, 08 Dec 2025 23:14:11 GMT  
		Size: 23.1 KB (23142 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8-bookworm`

```console
$ docker pull satosa@sha256:47cab947e2477f7a89747951af0cca8f8d911c9807dc8aa2d0a0eb66d2b0b5d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8-bookworm` - linux; amd64

```console
$ docker pull satosa@sha256:02d11444e8397d8cf844cfe4966790e8acd11bb96df692b0d2246fdc4b84e724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91546319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fdbbd78fb77c1c45bf4c6de659e0b646927937253d1ea05101ef20673dc9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:33:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:33:46 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:43:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:43:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:43:53 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:11:52 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:12:46 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:12:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:12:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:12:47 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:12:47 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:12:47 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009f5cc336e3b76a99df531b878e328e7a550219c8956a8a194aa3b0d195db91`  
		Last Modified: Mon, 08 Dec 2025 20:44:07 GMT  
		Size: 3.5 MB (3515868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661abbc8fe10b243e7e573653867ccaa905ddb32a37a534e407d8d13edf850b`  
		Last Modified: Mon, 08 Dec 2025 20:44:12 GMT  
		Size: 12.5 MB (12470573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed91f2f794eb4b70d66bbfdcc185d49c206fe04adc5a2342583287af687d5a1`  
		Last Modified: Mon, 08 Dec 2025 20:44:07 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79acb76c9c0b4b230bfe39a96674638997c6e3e604a3ac06679eff10f301a3ed`  
		Last Modified: Mon, 08 Dec 2025 21:13:17 GMT  
		Size: 21.5 MB (21456825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2375cde2b745416d789de4916d59cca9acbe71b560fab10770ef2334ab8b7c0`  
		Last Modified: Mon, 08 Dec 2025 21:13:24 GMT  
		Size: 25.9 MB (25861803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb2815d937de7372beed80131c8ea74f531bfef1e5e42327f78e5845b8d3a94`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 10.4 KB (10441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddafdd0c89bdf32c613738b8bf29e31ecf1b9378a6090d858a7161e166ad0ea`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:ba2a77056920b0b8c29c5c1cd5b4ad488cd5d77b6b98a2c1d8fb0b8166659112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139237f34ca29fe7e6eca10a086e04e1388e05fb722c6a11c6898ee2afc51c90`

```dockerfile
```

-	Layers:
	-	`sha256:74f9eb40f65c4cc8706a37a324099d2b084fa1e4996275f01a193b1dedc06bc4`  
		Last Modified: Mon, 08 Dec 2025 23:13:58 GMT  
		Size: 2.7 MB (2704633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59c7c8a0e3d3d3e331479afb101f477f0105ef999c2fec379b98c7e55d61f69b`  
		Last Modified: Mon, 08 Dec 2025 23:13:59 GMT  
		Size: 22.3 KB (22266 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8-bookworm` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e6034f8923cc420bf624c03933ca51d3fa3fa53369e574d01519048130a6ea08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90626193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a048ae55480d2f33d8cfc4e898989706e7365329e4c1dd6033c938644b7e9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:10:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:10:26 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:23:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:23:02 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:23:02 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:10:47 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:11:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:11:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:11:36 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:11:36 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:11:36 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067a176e286689d9a5616e9a9ccb474753231475a3b74b8c4eb6897476010420`  
		Last Modified: Mon, 08 Dec 2025 20:37:28 GMT  
		Size: 3.3 MB (3349161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fc0b8bf8e30d988c0f398a3673770af657a9ad94ba5605b3c5ff9927aa69d4`  
		Last Modified: Mon, 08 Dec 2025 21:10:40 GMT  
		Size: 12.4 MB (12372485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfc60c769de0a434549492e317c8c2ff2cae1e4a35d3c369d631538c2588087`  
		Last Modified: Mon, 08 Dec 2025 20:37:37 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572f90ee4f08e9e7e4545f1fec7a2502d142eddf118a4fd7bf2645c7be56ef69`  
		Last Modified: Mon, 08 Dec 2025 21:12:08 GMT  
		Size: 21.3 MB (21306657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8001b73c61fa8c9d9ac229832e7a11cf353654a05001f5774eddb626e0a8e`  
		Last Modified: Mon, 08 Dec 2025 21:12:13 GMT  
		Size: 25.5 MB (25482878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8968998041481e37921326fcbf07ff2ed641dcba0c5c05dca511426bf6870817`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 10.4 KB (10439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebca083d50d345d85ac73c6847800d6f5240548843ad64f9930b46be656536d`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:1b7e4ec015d578ac03adee68f7e1eef5a0a20228c6bdb3e3e7a0aa69ba363f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2727406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef91488e298c4cf89b88685f361b8c0e0b25207e9096cc5309b29b59e8087d0`

```dockerfile
```

-	Layers:
	-	`sha256:c2688d87a56f8ed7f757ae7f9a2eca3beece73a77533054ff78d0b527bd9a223`  
		Last Modified: Mon, 08 Dec 2025 23:14:03 GMT  
		Size: 2.7 MB (2704959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a6c70eeb25bdce5e4963b184cbb29ab0ecd0c886fe9ce1ac44cfda2be17eebf`  
		Last Modified: Mon, 08 Dec 2025 23:14:04 GMT  
		Size: 22.4 KB (22447 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.5`

```console
$ docker pull satosa@sha256:47cab947e2477f7a89747951af0cca8f8d911c9807dc8aa2d0a0eb66d2b0b5d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8.5` - linux; amd64

```console
$ docker pull satosa@sha256:02d11444e8397d8cf844cfe4966790e8acd11bb96df692b0d2246fdc4b84e724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91546319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fdbbd78fb77c1c45bf4c6de659e0b646927937253d1ea05101ef20673dc9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:33:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:33:46 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:43:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:43:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:43:53 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:11:52 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:12:46 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:12:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:12:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:12:47 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:12:47 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:12:47 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009f5cc336e3b76a99df531b878e328e7a550219c8956a8a194aa3b0d195db91`  
		Last Modified: Mon, 08 Dec 2025 20:44:07 GMT  
		Size: 3.5 MB (3515868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661abbc8fe10b243e7e573653867ccaa905ddb32a37a534e407d8d13edf850b`  
		Last Modified: Mon, 08 Dec 2025 20:44:12 GMT  
		Size: 12.5 MB (12470573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed91f2f794eb4b70d66bbfdcc185d49c206fe04adc5a2342583287af687d5a1`  
		Last Modified: Mon, 08 Dec 2025 20:44:07 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79acb76c9c0b4b230bfe39a96674638997c6e3e604a3ac06679eff10f301a3ed`  
		Last Modified: Mon, 08 Dec 2025 21:13:17 GMT  
		Size: 21.5 MB (21456825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2375cde2b745416d789de4916d59cca9acbe71b560fab10770ef2334ab8b7c0`  
		Last Modified: Mon, 08 Dec 2025 21:13:24 GMT  
		Size: 25.9 MB (25861803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb2815d937de7372beed80131c8ea74f531bfef1e5e42327f78e5845b8d3a94`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 10.4 KB (10441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddafdd0c89bdf32c613738b8bf29e31ecf1b9378a6090d858a7161e166ad0ea`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5` - unknown; unknown

```console
$ docker pull satosa@sha256:ba2a77056920b0b8c29c5c1cd5b4ad488cd5d77b6b98a2c1d8fb0b8166659112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139237f34ca29fe7e6eca10a086e04e1388e05fb722c6a11c6898ee2afc51c90`

```dockerfile
```

-	Layers:
	-	`sha256:74f9eb40f65c4cc8706a37a324099d2b084fa1e4996275f01a193b1dedc06bc4`  
		Last Modified: Mon, 08 Dec 2025 23:13:58 GMT  
		Size: 2.7 MB (2704633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59c7c8a0e3d3d3e331479afb101f477f0105ef999c2fec379b98c7e55d61f69b`  
		Last Modified: Mon, 08 Dec 2025 23:13:59 GMT  
		Size: 22.3 KB (22266 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.5` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e6034f8923cc420bf624c03933ca51d3fa3fa53369e574d01519048130a6ea08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90626193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a048ae55480d2f33d8cfc4e898989706e7365329e4c1dd6033c938644b7e9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:10:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:10:26 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:23:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:23:02 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:23:02 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:10:47 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:11:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:11:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:11:36 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:11:36 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:11:36 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067a176e286689d9a5616e9a9ccb474753231475a3b74b8c4eb6897476010420`  
		Last Modified: Mon, 08 Dec 2025 20:37:28 GMT  
		Size: 3.3 MB (3349161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fc0b8bf8e30d988c0f398a3673770af657a9ad94ba5605b3c5ff9927aa69d4`  
		Last Modified: Mon, 08 Dec 2025 21:10:40 GMT  
		Size: 12.4 MB (12372485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfc60c769de0a434549492e317c8c2ff2cae1e4a35d3c369d631538c2588087`  
		Last Modified: Mon, 08 Dec 2025 20:37:37 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572f90ee4f08e9e7e4545f1fec7a2502d142eddf118a4fd7bf2645c7be56ef69`  
		Last Modified: Mon, 08 Dec 2025 21:12:08 GMT  
		Size: 21.3 MB (21306657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8001b73c61fa8c9d9ac229832e7a11cf353654a05001f5774eddb626e0a8e`  
		Last Modified: Mon, 08 Dec 2025 21:12:13 GMT  
		Size: 25.5 MB (25482878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8968998041481e37921326fcbf07ff2ed641dcba0c5c05dca511426bf6870817`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 10.4 KB (10439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebca083d50d345d85ac73c6847800d6f5240548843ad64f9930b46be656536d`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5` - unknown; unknown

```console
$ docker pull satosa@sha256:1b7e4ec015d578ac03adee68f7e1eef5a0a20228c6bdb3e3e7a0aa69ba363f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2727406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef91488e298c4cf89b88685f361b8c0e0b25207e9096cc5309b29b59e8087d0`

```dockerfile
```

-	Layers:
	-	`sha256:c2688d87a56f8ed7f757ae7f9a2eca3beece73a77533054ff78d0b527bd9a223`  
		Last Modified: Mon, 08 Dec 2025 23:14:03 GMT  
		Size: 2.7 MB (2704959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a6c70eeb25bdce5e4963b184cbb29ab0ecd0c886fe9ce1ac44cfda2be17eebf`  
		Last Modified: Mon, 08 Dec 2025 23:14:04 GMT  
		Size: 22.4 KB (22447 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.5-alpine`

```console
$ docker pull satosa@sha256:adedc568ec1d96b84febaeaeccdf3b6741cee3c12af9843c693bbc7ae51d2c8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8.5-alpine` - linux; amd64

```console
$ docker pull satosa@sha256:e121448d38b02e6ee0e78f99e088425663bfd6747886f0efce468291c3f62f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49149075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ccd9369292b929b0366109da11f96c50afebbfadcedc880613ce2ce475cb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:30:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:30:58 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:36:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:36:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:36:20 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:12:34 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:12:54 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:12:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:12:55 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:12:55 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:12:55 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26daf640290a5c96818eeceda9d0ca2e9fc41fc3a6b57a9042ed93a479c15161`  
		Last Modified: Mon, 08 Dec 2025 20:36:32 GMT  
		Size: 456.9 KB (456928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b1972ad510f9ac01c1a925be2d191877631aa1ac5fb973b6e7bd8bcb4133e2`  
		Last Modified: Mon, 08 Dec 2025 20:36:33 GMT  
		Size: 12.4 MB (12438092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25dc0fb9705edc6661711090bbb88c90560b516b861680a35178aaf986296a8`  
		Last Modified: Mon, 08 Dec 2025 20:36:32 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df3e3c3fcc2bba3d34c49be0a42c155b93ce4bf7434accf72beafb185d61011`  
		Last Modified: Mon, 08 Dec 2025 21:13:14 GMT  
		Size: 6.7 MB (6717688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249b2e05caedcdb9b33eae3134a31c6903ef0ebe4bd1fb7524fb6372d1336bf8`  
		Last Modified: Mon, 08 Dec 2025 21:13:18 GMT  
		Size: 25.7 MB (25721114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5521ff6cf19924b06d81d65132085a2884c9d16ef8d12f8b33a7ab10892a2c1d`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 10.4 KB (10438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fbb063fad282ec1ecd0eda6d419d1179e9ba7908dd0a38496b03a8976084e4`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 2.1 KB (2080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:053b3548aded493f8b8d389ffdfa856d72a53956ec08f9d6cb9d1a0562071613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **806.2 KB (806179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fdc00dcb12fdc98bc985aa473ee27ce5e931601d5e426d2ed8c559491bc45b7`

```dockerfile
```

-	Layers:
	-	`sha256:de6df0a0041eccd13155e23b861f0a62034e6a8535664f050f8341328c38b9d4`  
		Last Modified: Mon, 08 Dec 2025 23:14:06 GMT  
		Size: 783.2 KB (783219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa32fe9c93af693fbacaf0283ddfeb2882849bc3b6e1066ee29e4dd85060f1fa`  
		Last Modified: Mon, 08 Dec 2025 23:14:07 GMT  
		Size: 23.0 KB (22960 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.5-alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:092eadb6a3d49e7ac1803172ff64eed6c55596b94ae18393e4e83e917bf1abc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49093844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643ccb5cb566e62f38c946f4ed47ccf98a3dea79baf075ae1d9f2b8bf1b151e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:13:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:13:36 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:20:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:20:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:20:06 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:11:21 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:11:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:11:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:11:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:11:44 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:11:44 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:11:44 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04eda5d87448437994b338947f03a72065bf589d08071ba33ba5dc3ea1ddcf9`  
		Last Modified: Mon, 08 Dec 2025 20:20:23 GMT  
		Size: 459.0 KB (459020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19756ed87e004e14deeb5d042df980b7204f44649d4cce479201223a8589ab`  
		Last Modified: Mon, 08 Dec 2025 20:20:23 GMT  
		Size: 12.5 MB (12453549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be90ee3c5e8855f927e9dabc42fd16e3baec85cb245b81e43412665495c6b4a`  
		Last Modified: Mon, 08 Dec 2025 20:20:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a131be40642a2cf885cdcb75474faaf4e6651804fc3f8cd6201c9960ca7d3f`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 6.7 MB (6694259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a8917a69ecc315188c393d384a8726146e9a2226632ec028e7e54a5546c701`  
		Last Modified: Mon, 08 Dec 2025 21:12:08 GMT  
		Size: 25.3 MB (25336149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b79bc7d0a94fb0a4eaa2b1cace6bf0e4b799d4e76449fa4b17cf2d02f9ed1a4`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 10.4 KB (10440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd5054ceea4ea2377c4734c970adf4f763deaeaaa9e72dca0fbc2beda863685`  
		Last Modified: Mon, 08 Dec 2025 21:12:05 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:fbfef43bbeaf94239cde0843248f928b598c0b683f6e8a8209428bceede91894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **806.5 KB (806465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f04a24d13f86b5d751637955c00828100756cb72f170fb3422f7cd5bc8c6773`

```dockerfile
```

-	Layers:
	-	`sha256:fbe4e8fa0a2a61b3f561fcd5420ad68fb6cc07c61a2592e567ab105acdab481d`  
		Last Modified: Mon, 08 Dec 2025 23:14:10 GMT  
		Size: 783.3 KB (783323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24efd495e1ac9fb1735f89706533f4d82e1c5bc1d3747b3cb4d0a599225a46fb`  
		Last Modified: Mon, 08 Dec 2025 23:14:11 GMT  
		Size: 23.1 KB (23142 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.5-alpine3.22`

```console
$ docker pull satosa@sha256:adedc568ec1d96b84febaeaeccdf3b6741cee3c12af9843c693bbc7ae51d2c8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8.5-alpine3.22` - linux; amd64

```console
$ docker pull satosa@sha256:e121448d38b02e6ee0e78f99e088425663bfd6747886f0efce468291c3f62f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49149075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ccd9369292b929b0366109da11f96c50afebbfadcedc880613ce2ce475cb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:30:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:30:58 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:36:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:36:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:36:20 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:12:34 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:12:54 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:12:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:12:55 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:12:55 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:12:55 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26daf640290a5c96818eeceda9d0ca2e9fc41fc3a6b57a9042ed93a479c15161`  
		Last Modified: Mon, 08 Dec 2025 20:36:32 GMT  
		Size: 456.9 KB (456928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b1972ad510f9ac01c1a925be2d191877631aa1ac5fb973b6e7bd8bcb4133e2`  
		Last Modified: Mon, 08 Dec 2025 20:36:33 GMT  
		Size: 12.4 MB (12438092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25dc0fb9705edc6661711090bbb88c90560b516b861680a35178aaf986296a8`  
		Last Modified: Mon, 08 Dec 2025 20:36:32 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df3e3c3fcc2bba3d34c49be0a42c155b93ce4bf7434accf72beafb185d61011`  
		Last Modified: Mon, 08 Dec 2025 21:13:14 GMT  
		Size: 6.7 MB (6717688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249b2e05caedcdb9b33eae3134a31c6903ef0ebe4bd1fb7524fb6372d1336bf8`  
		Last Modified: Mon, 08 Dec 2025 21:13:18 GMT  
		Size: 25.7 MB (25721114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5521ff6cf19924b06d81d65132085a2884c9d16ef8d12f8b33a7ab10892a2c1d`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 10.4 KB (10438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fbb063fad282ec1ecd0eda6d419d1179e9ba7908dd0a38496b03a8976084e4`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 2.1 KB (2080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5-alpine3.22` - unknown; unknown

```console
$ docker pull satosa@sha256:053b3548aded493f8b8d389ffdfa856d72a53956ec08f9d6cb9d1a0562071613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **806.2 KB (806179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fdc00dcb12fdc98bc985aa473ee27ce5e931601d5e426d2ed8c559491bc45b7`

```dockerfile
```

-	Layers:
	-	`sha256:de6df0a0041eccd13155e23b861f0a62034e6a8535664f050f8341328c38b9d4`  
		Last Modified: Mon, 08 Dec 2025 23:14:06 GMT  
		Size: 783.2 KB (783219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa32fe9c93af693fbacaf0283ddfeb2882849bc3b6e1066ee29e4dd85060f1fa`  
		Last Modified: Mon, 08 Dec 2025 23:14:07 GMT  
		Size: 23.0 KB (22960 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.5-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:092eadb6a3d49e7ac1803172ff64eed6c55596b94ae18393e4e83e917bf1abc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49093844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643ccb5cb566e62f38c946f4ed47ccf98a3dea79baf075ae1d9f2b8bf1b151e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:13:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:13:36 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:20:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:20:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:20:06 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:11:21 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:11:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:11:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:11:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:11:44 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:11:44 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:11:44 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04eda5d87448437994b338947f03a72065bf589d08071ba33ba5dc3ea1ddcf9`  
		Last Modified: Mon, 08 Dec 2025 20:20:23 GMT  
		Size: 459.0 KB (459020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19756ed87e004e14deeb5d042df980b7204f44649d4cce479201223a8589ab`  
		Last Modified: Mon, 08 Dec 2025 20:20:23 GMT  
		Size: 12.5 MB (12453549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be90ee3c5e8855f927e9dabc42fd16e3baec85cb245b81e43412665495c6b4a`  
		Last Modified: Mon, 08 Dec 2025 20:20:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a131be40642a2cf885cdcb75474faaf4e6651804fc3f8cd6201c9960ca7d3f`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 6.7 MB (6694259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a8917a69ecc315188c393d384a8726146e9a2226632ec028e7e54a5546c701`  
		Last Modified: Mon, 08 Dec 2025 21:12:08 GMT  
		Size: 25.3 MB (25336149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b79bc7d0a94fb0a4eaa2b1cace6bf0e4b799d4e76449fa4b17cf2d02f9ed1a4`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 10.4 KB (10440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd5054ceea4ea2377c4734c970adf4f763deaeaaa9e72dca0fbc2beda863685`  
		Last Modified: Mon, 08 Dec 2025 21:12:05 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5-alpine3.22` - unknown; unknown

```console
$ docker pull satosa@sha256:fbfef43bbeaf94239cde0843248f928b598c0b683f6e8a8209428bceede91894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **806.5 KB (806465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f04a24d13f86b5d751637955c00828100756cb72f170fb3422f7cd5bc8c6773`

```dockerfile
```

-	Layers:
	-	`sha256:fbe4e8fa0a2a61b3f561fcd5420ad68fb6cc07c61a2592e567ab105acdab481d`  
		Last Modified: Mon, 08 Dec 2025 23:14:10 GMT  
		Size: 783.3 KB (783323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24efd495e1ac9fb1735f89706533f4d82e1c5bc1d3747b3cb4d0a599225a46fb`  
		Last Modified: Mon, 08 Dec 2025 23:14:11 GMT  
		Size: 23.1 KB (23142 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.5-bookworm`

```console
$ docker pull satosa@sha256:47cab947e2477f7a89747951af0cca8f8d911c9807dc8aa2d0a0eb66d2b0b5d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8.5-bookworm` - linux; amd64

```console
$ docker pull satosa@sha256:02d11444e8397d8cf844cfe4966790e8acd11bb96df692b0d2246fdc4b84e724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91546319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fdbbd78fb77c1c45bf4c6de659e0b646927937253d1ea05101ef20673dc9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:33:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:33:46 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:43:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:43:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:43:53 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:11:52 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:12:46 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:12:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:12:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:12:47 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:12:47 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:12:47 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009f5cc336e3b76a99df531b878e328e7a550219c8956a8a194aa3b0d195db91`  
		Last Modified: Mon, 08 Dec 2025 20:44:07 GMT  
		Size: 3.5 MB (3515868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661abbc8fe10b243e7e573653867ccaa905ddb32a37a534e407d8d13edf850b`  
		Last Modified: Mon, 08 Dec 2025 20:44:12 GMT  
		Size: 12.5 MB (12470573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed91f2f794eb4b70d66bbfdcc185d49c206fe04adc5a2342583287af687d5a1`  
		Last Modified: Mon, 08 Dec 2025 20:44:07 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79acb76c9c0b4b230bfe39a96674638997c6e3e604a3ac06679eff10f301a3ed`  
		Last Modified: Mon, 08 Dec 2025 21:13:17 GMT  
		Size: 21.5 MB (21456825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2375cde2b745416d789de4916d59cca9acbe71b560fab10770ef2334ab8b7c0`  
		Last Modified: Mon, 08 Dec 2025 21:13:24 GMT  
		Size: 25.9 MB (25861803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb2815d937de7372beed80131c8ea74f531bfef1e5e42327f78e5845b8d3a94`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 10.4 KB (10441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddafdd0c89bdf32c613738b8bf29e31ecf1b9378a6090d858a7161e166ad0ea`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:ba2a77056920b0b8c29c5c1cd5b4ad488cd5d77b6b98a2c1d8fb0b8166659112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139237f34ca29fe7e6eca10a086e04e1388e05fb722c6a11c6898ee2afc51c90`

```dockerfile
```

-	Layers:
	-	`sha256:74f9eb40f65c4cc8706a37a324099d2b084fa1e4996275f01a193b1dedc06bc4`  
		Last Modified: Mon, 08 Dec 2025 23:13:58 GMT  
		Size: 2.7 MB (2704633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59c7c8a0e3d3d3e331479afb101f477f0105ef999c2fec379b98c7e55d61f69b`  
		Last Modified: Mon, 08 Dec 2025 23:13:59 GMT  
		Size: 22.3 KB (22266 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.5-bookworm` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e6034f8923cc420bf624c03933ca51d3fa3fa53369e574d01519048130a6ea08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90626193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a048ae55480d2f33d8cfc4e898989706e7365329e4c1dd6033c938644b7e9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:10:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:10:26 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:23:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:23:02 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:23:02 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:10:47 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:11:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:11:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:11:36 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:11:36 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:11:36 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067a176e286689d9a5616e9a9ccb474753231475a3b74b8c4eb6897476010420`  
		Last Modified: Mon, 08 Dec 2025 20:37:28 GMT  
		Size: 3.3 MB (3349161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fc0b8bf8e30d988c0f398a3673770af657a9ad94ba5605b3c5ff9927aa69d4`  
		Last Modified: Mon, 08 Dec 2025 21:10:40 GMT  
		Size: 12.4 MB (12372485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfc60c769de0a434549492e317c8c2ff2cae1e4a35d3c369d631538c2588087`  
		Last Modified: Mon, 08 Dec 2025 20:37:37 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572f90ee4f08e9e7e4545f1fec7a2502d142eddf118a4fd7bf2645c7be56ef69`  
		Last Modified: Mon, 08 Dec 2025 21:12:08 GMT  
		Size: 21.3 MB (21306657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8001b73c61fa8c9d9ac229832e7a11cf353654a05001f5774eddb626e0a8e`  
		Last Modified: Mon, 08 Dec 2025 21:12:13 GMT  
		Size: 25.5 MB (25482878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8968998041481e37921326fcbf07ff2ed641dcba0c5c05dca511426bf6870817`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 10.4 KB (10439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebca083d50d345d85ac73c6847800d6f5240548843ad64f9930b46be656536d`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:1b7e4ec015d578ac03adee68f7e1eef5a0a20228c6bdb3e3e7a0aa69ba363f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2727406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef91488e298c4cf89b88685f361b8c0e0b25207e9096cc5309b29b59e8087d0`

```dockerfile
```

-	Layers:
	-	`sha256:c2688d87a56f8ed7f757ae7f9a2eca3beece73a77533054ff78d0b527bd9a223`  
		Last Modified: Mon, 08 Dec 2025 23:14:03 GMT  
		Size: 2.7 MB (2704959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a6c70eeb25bdce5e4963b184cbb29ab0ecd0c886fe9ce1ac44cfda2be17eebf`  
		Last Modified: Mon, 08 Dec 2025 23:14:04 GMT  
		Size: 22.4 KB (22447 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.5.1`

```console
$ docker pull satosa@sha256:47cab947e2477f7a89747951af0cca8f8d911c9807dc8aa2d0a0eb66d2b0b5d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8.5.1` - linux; amd64

```console
$ docker pull satosa@sha256:02d11444e8397d8cf844cfe4966790e8acd11bb96df692b0d2246fdc4b84e724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91546319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fdbbd78fb77c1c45bf4c6de659e0b646927937253d1ea05101ef20673dc9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:33:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:33:46 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:43:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:43:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:43:53 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:11:52 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:12:46 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:12:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:12:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:12:47 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:12:47 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:12:47 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009f5cc336e3b76a99df531b878e328e7a550219c8956a8a194aa3b0d195db91`  
		Last Modified: Mon, 08 Dec 2025 20:44:07 GMT  
		Size: 3.5 MB (3515868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661abbc8fe10b243e7e573653867ccaa905ddb32a37a534e407d8d13edf850b`  
		Last Modified: Mon, 08 Dec 2025 20:44:12 GMT  
		Size: 12.5 MB (12470573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed91f2f794eb4b70d66bbfdcc185d49c206fe04adc5a2342583287af687d5a1`  
		Last Modified: Mon, 08 Dec 2025 20:44:07 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79acb76c9c0b4b230bfe39a96674638997c6e3e604a3ac06679eff10f301a3ed`  
		Last Modified: Mon, 08 Dec 2025 21:13:17 GMT  
		Size: 21.5 MB (21456825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2375cde2b745416d789de4916d59cca9acbe71b560fab10770ef2334ab8b7c0`  
		Last Modified: Mon, 08 Dec 2025 21:13:24 GMT  
		Size: 25.9 MB (25861803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb2815d937de7372beed80131c8ea74f531bfef1e5e42327f78e5845b8d3a94`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 10.4 KB (10441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddafdd0c89bdf32c613738b8bf29e31ecf1b9378a6090d858a7161e166ad0ea`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5.1` - unknown; unknown

```console
$ docker pull satosa@sha256:ba2a77056920b0b8c29c5c1cd5b4ad488cd5d77b6b98a2c1d8fb0b8166659112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139237f34ca29fe7e6eca10a086e04e1388e05fb722c6a11c6898ee2afc51c90`

```dockerfile
```

-	Layers:
	-	`sha256:74f9eb40f65c4cc8706a37a324099d2b084fa1e4996275f01a193b1dedc06bc4`  
		Last Modified: Mon, 08 Dec 2025 23:13:58 GMT  
		Size: 2.7 MB (2704633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59c7c8a0e3d3d3e331479afb101f477f0105ef999c2fec379b98c7e55d61f69b`  
		Last Modified: Mon, 08 Dec 2025 23:13:59 GMT  
		Size: 22.3 KB (22266 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.5.1` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e6034f8923cc420bf624c03933ca51d3fa3fa53369e574d01519048130a6ea08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90626193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a048ae55480d2f33d8cfc4e898989706e7365329e4c1dd6033c938644b7e9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:10:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:10:26 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:23:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:23:02 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:23:02 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:10:47 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:11:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:11:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:11:36 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:11:36 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:11:36 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067a176e286689d9a5616e9a9ccb474753231475a3b74b8c4eb6897476010420`  
		Last Modified: Mon, 08 Dec 2025 20:37:28 GMT  
		Size: 3.3 MB (3349161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fc0b8bf8e30d988c0f398a3673770af657a9ad94ba5605b3c5ff9927aa69d4`  
		Last Modified: Mon, 08 Dec 2025 21:10:40 GMT  
		Size: 12.4 MB (12372485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfc60c769de0a434549492e317c8c2ff2cae1e4a35d3c369d631538c2588087`  
		Last Modified: Mon, 08 Dec 2025 20:37:37 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572f90ee4f08e9e7e4545f1fec7a2502d142eddf118a4fd7bf2645c7be56ef69`  
		Last Modified: Mon, 08 Dec 2025 21:12:08 GMT  
		Size: 21.3 MB (21306657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8001b73c61fa8c9d9ac229832e7a11cf353654a05001f5774eddb626e0a8e`  
		Last Modified: Mon, 08 Dec 2025 21:12:13 GMT  
		Size: 25.5 MB (25482878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8968998041481e37921326fcbf07ff2ed641dcba0c5c05dca511426bf6870817`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 10.4 KB (10439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebca083d50d345d85ac73c6847800d6f5240548843ad64f9930b46be656536d`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5.1` - unknown; unknown

```console
$ docker pull satosa@sha256:1b7e4ec015d578ac03adee68f7e1eef5a0a20228c6bdb3e3e7a0aa69ba363f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2727406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef91488e298c4cf89b88685f361b8c0e0b25207e9096cc5309b29b59e8087d0`

```dockerfile
```

-	Layers:
	-	`sha256:c2688d87a56f8ed7f757ae7f9a2eca3beece73a77533054ff78d0b527bd9a223`  
		Last Modified: Mon, 08 Dec 2025 23:14:03 GMT  
		Size: 2.7 MB (2704959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a6c70eeb25bdce5e4963b184cbb29ab0ecd0c886fe9ce1ac44cfda2be17eebf`  
		Last Modified: Mon, 08 Dec 2025 23:14:04 GMT  
		Size: 22.4 KB (22447 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.5.1-alpine`

```console
$ docker pull satosa@sha256:adedc568ec1d96b84febaeaeccdf3b6741cee3c12af9843c693bbc7ae51d2c8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8.5.1-alpine` - linux; amd64

```console
$ docker pull satosa@sha256:e121448d38b02e6ee0e78f99e088425663bfd6747886f0efce468291c3f62f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49149075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ccd9369292b929b0366109da11f96c50afebbfadcedc880613ce2ce475cb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:30:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:30:58 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:36:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:36:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:36:20 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:12:34 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:12:54 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:12:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:12:55 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:12:55 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:12:55 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26daf640290a5c96818eeceda9d0ca2e9fc41fc3a6b57a9042ed93a479c15161`  
		Last Modified: Mon, 08 Dec 2025 20:36:32 GMT  
		Size: 456.9 KB (456928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b1972ad510f9ac01c1a925be2d191877631aa1ac5fb973b6e7bd8bcb4133e2`  
		Last Modified: Mon, 08 Dec 2025 20:36:33 GMT  
		Size: 12.4 MB (12438092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25dc0fb9705edc6661711090bbb88c90560b516b861680a35178aaf986296a8`  
		Last Modified: Mon, 08 Dec 2025 20:36:32 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df3e3c3fcc2bba3d34c49be0a42c155b93ce4bf7434accf72beafb185d61011`  
		Last Modified: Mon, 08 Dec 2025 21:13:14 GMT  
		Size: 6.7 MB (6717688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249b2e05caedcdb9b33eae3134a31c6903ef0ebe4bd1fb7524fb6372d1336bf8`  
		Last Modified: Mon, 08 Dec 2025 21:13:18 GMT  
		Size: 25.7 MB (25721114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5521ff6cf19924b06d81d65132085a2884c9d16ef8d12f8b33a7ab10892a2c1d`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 10.4 KB (10438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fbb063fad282ec1ecd0eda6d419d1179e9ba7908dd0a38496b03a8976084e4`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 2.1 KB (2080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5.1-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:053b3548aded493f8b8d389ffdfa856d72a53956ec08f9d6cb9d1a0562071613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **806.2 KB (806179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fdc00dcb12fdc98bc985aa473ee27ce5e931601d5e426d2ed8c559491bc45b7`

```dockerfile
```

-	Layers:
	-	`sha256:de6df0a0041eccd13155e23b861f0a62034e6a8535664f050f8341328c38b9d4`  
		Last Modified: Mon, 08 Dec 2025 23:14:06 GMT  
		Size: 783.2 KB (783219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa32fe9c93af693fbacaf0283ddfeb2882849bc3b6e1066ee29e4dd85060f1fa`  
		Last Modified: Mon, 08 Dec 2025 23:14:07 GMT  
		Size: 23.0 KB (22960 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.5.1-alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:092eadb6a3d49e7ac1803172ff64eed6c55596b94ae18393e4e83e917bf1abc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49093844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643ccb5cb566e62f38c946f4ed47ccf98a3dea79baf075ae1d9f2b8bf1b151e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:13:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:13:36 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:20:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:20:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:20:06 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:11:21 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:11:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:11:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:11:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:11:44 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:11:44 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:11:44 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04eda5d87448437994b338947f03a72065bf589d08071ba33ba5dc3ea1ddcf9`  
		Last Modified: Mon, 08 Dec 2025 20:20:23 GMT  
		Size: 459.0 KB (459020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19756ed87e004e14deeb5d042df980b7204f44649d4cce479201223a8589ab`  
		Last Modified: Mon, 08 Dec 2025 20:20:23 GMT  
		Size: 12.5 MB (12453549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be90ee3c5e8855f927e9dabc42fd16e3baec85cb245b81e43412665495c6b4a`  
		Last Modified: Mon, 08 Dec 2025 20:20:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a131be40642a2cf885cdcb75474faaf4e6651804fc3f8cd6201c9960ca7d3f`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 6.7 MB (6694259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a8917a69ecc315188c393d384a8726146e9a2226632ec028e7e54a5546c701`  
		Last Modified: Mon, 08 Dec 2025 21:12:08 GMT  
		Size: 25.3 MB (25336149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b79bc7d0a94fb0a4eaa2b1cace6bf0e4b799d4e76449fa4b17cf2d02f9ed1a4`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 10.4 KB (10440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd5054ceea4ea2377c4734c970adf4f763deaeaaa9e72dca0fbc2beda863685`  
		Last Modified: Mon, 08 Dec 2025 21:12:05 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5.1-alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:fbfef43bbeaf94239cde0843248f928b598c0b683f6e8a8209428bceede91894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **806.5 KB (806465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f04a24d13f86b5d751637955c00828100756cb72f170fb3422f7cd5bc8c6773`

```dockerfile
```

-	Layers:
	-	`sha256:fbe4e8fa0a2a61b3f561fcd5420ad68fb6cc07c61a2592e567ab105acdab481d`  
		Last Modified: Mon, 08 Dec 2025 23:14:10 GMT  
		Size: 783.3 KB (783323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24efd495e1ac9fb1735f89706533f4d82e1c5bc1d3747b3cb4d0a599225a46fb`  
		Last Modified: Mon, 08 Dec 2025 23:14:11 GMT  
		Size: 23.1 KB (23142 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.5.1-alpine3.22`

```console
$ docker pull satosa@sha256:adedc568ec1d96b84febaeaeccdf3b6741cee3c12af9843c693bbc7ae51d2c8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8.5.1-alpine3.22` - linux; amd64

```console
$ docker pull satosa@sha256:e121448d38b02e6ee0e78f99e088425663bfd6747886f0efce468291c3f62f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49149075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ccd9369292b929b0366109da11f96c50afebbfadcedc880613ce2ce475cb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:30:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:30:58 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:36:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:36:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:36:20 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:12:34 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:12:54 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:12:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:12:55 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:12:55 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:12:55 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26daf640290a5c96818eeceda9d0ca2e9fc41fc3a6b57a9042ed93a479c15161`  
		Last Modified: Mon, 08 Dec 2025 20:36:32 GMT  
		Size: 456.9 KB (456928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b1972ad510f9ac01c1a925be2d191877631aa1ac5fb973b6e7bd8bcb4133e2`  
		Last Modified: Mon, 08 Dec 2025 20:36:33 GMT  
		Size: 12.4 MB (12438092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25dc0fb9705edc6661711090bbb88c90560b516b861680a35178aaf986296a8`  
		Last Modified: Mon, 08 Dec 2025 20:36:32 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df3e3c3fcc2bba3d34c49be0a42c155b93ce4bf7434accf72beafb185d61011`  
		Last Modified: Mon, 08 Dec 2025 21:13:14 GMT  
		Size: 6.7 MB (6717688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249b2e05caedcdb9b33eae3134a31c6903ef0ebe4bd1fb7524fb6372d1336bf8`  
		Last Modified: Mon, 08 Dec 2025 21:13:18 GMT  
		Size: 25.7 MB (25721114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5521ff6cf19924b06d81d65132085a2884c9d16ef8d12f8b33a7ab10892a2c1d`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 10.4 KB (10438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fbb063fad282ec1ecd0eda6d419d1179e9ba7908dd0a38496b03a8976084e4`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 2.1 KB (2080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5.1-alpine3.22` - unknown; unknown

```console
$ docker pull satosa@sha256:053b3548aded493f8b8d389ffdfa856d72a53956ec08f9d6cb9d1a0562071613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **806.2 KB (806179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fdc00dcb12fdc98bc985aa473ee27ce5e931601d5e426d2ed8c559491bc45b7`

```dockerfile
```

-	Layers:
	-	`sha256:de6df0a0041eccd13155e23b861f0a62034e6a8535664f050f8341328c38b9d4`  
		Last Modified: Mon, 08 Dec 2025 23:14:06 GMT  
		Size: 783.2 KB (783219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa32fe9c93af693fbacaf0283ddfeb2882849bc3b6e1066ee29e4dd85060f1fa`  
		Last Modified: Mon, 08 Dec 2025 23:14:07 GMT  
		Size: 23.0 KB (22960 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.5.1-alpine3.22` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:092eadb6a3d49e7ac1803172ff64eed6c55596b94ae18393e4e83e917bf1abc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49093844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643ccb5cb566e62f38c946f4ed47ccf98a3dea79baf075ae1d9f2b8bf1b151e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:13:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:13:36 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:20:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:20:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:20:06 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:11:21 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:11:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:11:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:11:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:11:44 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:11:44 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:11:44 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04eda5d87448437994b338947f03a72065bf589d08071ba33ba5dc3ea1ddcf9`  
		Last Modified: Mon, 08 Dec 2025 20:20:23 GMT  
		Size: 459.0 KB (459020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19756ed87e004e14deeb5d042df980b7204f44649d4cce479201223a8589ab`  
		Last Modified: Mon, 08 Dec 2025 20:20:23 GMT  
		Size: 12.5 MB (12453549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be90ee3c5e8855f927e9dabc42fd16e3baec85cb245b81e43412665495c6b4a`  
		Last Modified: Mon, 08 Dec 2025 20:20:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a131be40642a2cf885cdcb75474faaf4e6651804fc3f8cd6201c9960ca7d3f`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 6.7 MB (6694259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a8917a69ecc315188c393d384a8726146e9a2226632ec028e7e54a5546c701`  
		Last Modified: Mon, 08 Dec 2025 21:12:08 GMT  
		Size: 25.3 MB (25336149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b79bc7d0a94fb0a4eaa2b1cace6bf0e4b799d4e76449fa4b17cf2d02f9ed1a4`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 10.4 KB (10440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd5054ceea4ea2377c4734c970adf4f763deaeaaa9e72dca0fbc2beda863685`  
		Last Modified: Mon, 08 Dec 2025 21:12:05 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5.1-alpine3.22` - unknown; unknown

```console
$ docker pull satosa@sha256:fbfef43bbeaf94239cde0843248f928b598c0b683f6e8a8209428bceede91894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **806.5 KB (806465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f04a24d13f86b5d751637955c00828100756cb72f170fb3422f7cd5bc8c6773`

```dockerfile
```

-	Layers:
	-	`sha256:fbe4e8fa0a2a61b3f561fcd5420ad68fb6cc07c61a2592e567ab105acdab481d`  
		Last Modified: Mon, 08 Dec 2025 23:14:10 GMT  
		Size: 783.3 KB (783323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24efd495e1ac9fb1735f89706533f4d82e1c5bc1d3747b3cb4d0a599225a46fb`  
		Last Modified: Mon, 08 Dec 2025 23:14:11 GMT  
		Size: 23.1 KB (23142 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:8.5.1-bookworm`

```console
$ docker pull satosa@sha256:47cab947e2477f7a89747951af0cca8f8d911c9807dc8aa2d0a0eb66d2b0b5d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:8.5.1-bookworm` - linux; amd64

```console
$ docker pull satosa@sha256:02d11444e8397d8cf844cfe4966790e8acd11bb96df692b0d2246fdc4b84e724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91546319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fdbbd78fb77c1c45bf4c6de659e0b646927937253d1ea05101ef20673dc9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:33:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:33:46 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:43:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:43:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:43:53 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:11:52 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:12:46 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:12:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:12:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:12:47 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:12:47 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:12:47 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009f5cc336e3b76a99df531b878e328e7a550219c8956a8a194aa3b0d195db91`  
		Last Modified: Mon, 08 Dec 2025 20:44:07 GMT  
		Size: 3.5 MB (3515868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661abbc8fe10b243e7e573653867ccaa905ddb32a37a534e407d8d13edf850b`  
		Last Modified: Mon, 08 Dec 2025 20:44:12 GMT  
		Size: 12.5 MB (12470573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed91f2f794eb4b70d66bbfdcc185d49c206fe04adc5a2342583287af687d5a1`  
		Last Modified: Mon, 08 Dec 2025 20:44:07 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79acb76c9c0b4b230bfe39a96674638997c6e3e604a3ac06679eff10f301a3ed`  
		Last Modified: Mon, 08 Dec 2025 21:13:17 GMT  
		Size: 21.5 MB (21456825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2375cde2b745416d789de4916d59cca9acbe71b560fab10770ef2334ab8b7c0`  
		Last Modified: Mon, 08 Dec 2025 21:13:24 GMT  
		Size: 25.9 MB (25861803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb2815d937de7372beed80131c8ea74f531bfef1e5e42327f78e5845b8d3a94`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 10.4 KB (10441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddafdd0c89bdf32c613738b8bf29e31ecf1b9378a6090d858a7161e166ad0ea`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5.1-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:ba2a77056920b0b8c29c5c1cd5b4ad488cd5d77b6b98a2c1d8fb0b8166659112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139237f34ca29fe7e6eca10a086e04e1388e05fb722c6a11c6898ee2afc51c90`

```dockerfile
```

-	Layers:
	-	`sha256:74f9eb40f65c4cc8706a37a324099d2b084fa1e4996275f01a193b1dedc06bc4`  
		Last Modified: Mon, 08 Dec 2025 23:13:58 GMT  
		Size: 2.7 MB (2704633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59c7c8a0e3d3d3e331479afb101f477f0105ef999c2fec379b98c7e55d61f69b`  
		Last Modified: Mon, 08 Dec 2025 23:13:59 GMT  
		Size: 22.3 KB (22266 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:8.5.1-bookworm` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e6034f8923cc420bf624c03933ca51d3fa3fa53369e574d01519048130a6ea08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90626193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a048ae55480d2f33d8cfc4e898989706e7365329e4c1dd6033c938644b7e9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:10:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:10:26 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:23:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:23:02 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:23:02 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:10:47 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:11:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:11:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:11:36 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:11:36 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:11:36 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067a176e286689d9a5616e9a9ccb474753231475a3b74b8c4eb6897476010420`  
		Last Modified: Mon, 08 Dec 2025 20:37:28 GMT  
		Size: 3.3 MB (3349161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fc0b8bf8e30d988c0f398a3673770af657a9ad94ba5605b3c5ff9927aa69d4`  
		Last Modified: Mon, 08 Dec 2025 21:10:40 GMT  
		Size: 12.4 MB (12372485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfc60c769de0a434549492e317c8c2ff2cae1e4a35d3c369d631538c2588087`  
		Last Modified: Mon, 08 Dec 2025 20:37:37 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572f90ee4f08e9e7e4545f1fec7a2502d142eddf118a4fd7bf2645c7be56ef69`  
		Last Modified: Mon, 08 Dec 2025 21:12:08 GMT  
		Size: 21.3 MB (21306657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8001b73c61fa8c9d9ac229832e7a11cf353654a05001f5774eddb626e0a8e`  
		Last Modified: Mon, 08 Dec 2025 21:12:13 GMT  
		Size: 25.5 MB (25482878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8968998041481e37921326fcbf07ff2ed641dcba0c5c05dca511426bf6870817`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 10.4 KB (10439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebca083d50d345d85ac73c6847800d6f5240548843ad64f9930b46be656536d`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:8.5.1-bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:1b7e4ec015d578ac03adee68f7e1eef5a0a20228c6bdb3e3e7a0aa69ba363f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2727406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef91488e298c4cf89b88685f361b8c0e0b25207e9096cc5309b29b59e8087d0`

```dockerfile
```

-	Layers:
	-	`sha256:c2688d87a56f8ed7f757ae7f9a2eca3beece73a77533054ff78d0b527bd9a223`  
		Last Modified: Mon, 08 Dec 2025 23:14:03 GMT  
		Size: 2.7 MB (2704959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a6c70eeb25bdce5e4963b184cbb29ab0ecd0c886fe9ce1ac44cfda2be17eebf`  
		Last Modified: Mon, 08 Dec 2025 23:14:04 GMT  
		Size: 22.4 KB (22447 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:alpine`

```console
$ docker pull satosa@sha256:adedc568ec1d96b84febaeaeccdf3b6741cee3c12af9843c693bbc7ae51d2c8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:alpine` - linux; amd64

```console
$ docker pull satosa@sha256:e121448d38b02e6ee0e78f99e088425663bfd6747886f0efce468291c3f62f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49149075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ccd9369292b929b0366109da11f96c50afebbfadcedc880613ce2ce475cb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:30:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:30:58 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:36:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:36:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:36:20 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:12:34 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:12:54 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:12:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:12:55 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:12:55 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:12:55 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26daf640290a5c96818eeceda9d0ca2e9fc41fc3a6b57a9042ed93a479c15161`  
		Last Modified: Mon, 08 Dec 2025 20:36:32 GMT  
		Size: 456.9 KB (456928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b1972ad510f9ac01c1a925be2d191877631aa1ac5fb973b6e7bd8bcb4133e2`  
		Last Modified: Mon, 08 Dec 2025 20:36:33 GMT  
		Size: 12.4 MB (12438092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25dc0fb9705edc6661711090bbb88c90560b516b861680a35178aaf986296a8`  
		Last Modified: Mon, 08 Dec 2025 20:36:32 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df3e3c3fcc2bba3d34c49be0a42c155b93ce4bf7434accf72beafb185d61011`  
		Last Modified: Mon, 08 Dec 2025 21:13:14 GMT  
		Size: 6.7 MB (6717688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249b2e05caedcdb9b33eae3134a31c6903ef0ebe4bd1fb7524fb6372d1336bf8`  
		Last Modified: Mon, 08 Dec 2025 21:13:18 GMT  
		Size: 25.7 MB (25721114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5521ff6cf19924b06d81d65132085a2884c9d16ef8d12f8b33a7ab10892a2c1d`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 10.4 KB (10438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fbb063fad282ec1ecd0eda6d419d1179e9ba7908dd0a38496b03a8976084e4`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 2.1 KB (2080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:053b3548aded493f8b8d389ffdfa856d72a53956ec08f9d6cb9d1a0562071613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **806.2 KB (806179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fdc00dcb12fdc98bc985aa473ee27ce5e931601d5e426d2ed8c559491bc45b7`

```dockerfile
```

-	Layers:
	-	`sha256:de6df0a0041eccd13155e23b861f0a62034e6a8535664f050f8341328c38b9d4`  
		Last Modified: Mon, 08 Dec 2025 23:14:06 GMT  
		Size: 783.2 KB (783219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa32fe9c93af693fbacaf0283ddfeb2882849bc3b6e1066ee29e4dd85060f1fa`  
		Last Modified: Mon, 08 Dec 2025 23:14:07 GMT  
		Size: 23.0 KB (22960 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:alpine` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:092eadb6a3d49e7ac1803172ff64eed6c55596b94ae18393e4e83e917bf1abc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49093844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643ccb5cb566e62f38c946f4ed47ccf98a3dea79baf075ae1d9f2b8bf1b151e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:13:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:13:36 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:20:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:20:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:20:06 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:11:21 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:11:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:11:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:11:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:11:44 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:11:44 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:11:44 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04eda5d87448437994b338947f03a72065bf589d08071ba33ba5dc3ea1ddcf9`  
		Last Modified: Mon, 08 Dec 2025 20:20:23 GMT  
		Size: 459.0 KB (459020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19756ed87e004e14deeb5d042df980b7204f44649d4cce479201223a8589ab`  
		Last Modified: Mon, 08 Dec 2025 20:20:23 GMT  
		Size: 12.5 MB (12453549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be90ee3c5e8855f927e9dabc42fd16e3baec85cb245b81e43412665495c6b4a`  
		Last Modified: Mon, 08 Dec 2025 20:20:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a131be40642a2cf885cdcb75474faaf4e6651804fc3f8cd6201c9960ca7d3f`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 6.7 MB (6694259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a8917a69ecc315188c393d384a8726146e9a2226632ec028e7e54a5546c701`  
		Last Modified: Mon, 08 Dec 2025 21:12:08 GMT  
		Size: 25.3 MB (25336149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b79bc7d0a94fb0a4eaa2b1cace6bf0e4b799d4e76449fa4b17cf2d02f9ed1a4`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 10.4 KB (10440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd5054ceea4ea2377c4734c970adf4f763deaeaaa9e72dca0fbc2beda863685`  
		Last Modified: Mon, 08 Dec 2025 21:12:05 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:alpine` - unknown; unknown

```console
$ docker pull satosa@sha256:fbfef43bbeaf94239cde0843248f928b598c0b683f6e8a8209428bceede91894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **806.5 KB (806465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f04a24d13f86b5d751637955c00828100756cb72f170fb3422f7cd5bc8c6773`

```dockerfile
```

-	Layers:
	-	`sha256:fbe4e8fa0a2a61b3f561fcd5420ad68fb6cc07c61a2592e567ab105acdab481d`  
		Last Modified: Mon, 08 Dec 2025 23:14:10 GMT  
		Size: 783.3 KB (783323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24efd495e1ac9fb1735f89706533f4d82e1c5bc1d3747b3cb4d0a599225a46fb`  
		Last Modified: Mon, 08 Dec 2025 23:14:11 GMT  
		Size: 23.1 KB (23142 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:alpine3.22`

```console
$ docker pull satosa@sha256:adedc568ec1d96b84febaeaeccdf3b6741cee3c12af9843c693bbc7ae51d2c8a
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:alpine3.22` - linux; amd64

```console
$ docker pull satosa@sha256:e121448d38b02e6ee0e78f99e088425663bfd6747886f0efce468291c3f62f5e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49149075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38ccd9369292b929b0366109da11f96c50afebbfadcedc880613ce2ce475cb28`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-x86_64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:30:58 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:30:58 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:30:58 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:36:20 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:36:20 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:36:20 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:12:34 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:12:54 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:12:54 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:12:55 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:12:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:12:55 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:12:55 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:12:55 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:2d35ebdb57d9971fea0cac1582aa78935adf8058b2cc32db163c98822e5dfa1b`  
		Last Modified: Sun, 07 Dec 2025 13:53:31 GMT  
		Size: 3.8 MB (3802452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26daf640290a5c96818eeceda9d0ca2e9fc41fc3a6b57a9042ed93a479c15161`  
		Last Modified: Mon, 08 Dec 2025 20:36:32 GMT  
		Size: 456.9 KB (456928 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80b1972ad510f9ac01c1a925be2d191877631aa1ac5fb973b6e7bd8bcb4133e2`  
		Last Modified: Mon, 08 Dec 2025 20:36:33 GMT  
		Size: 12.4 MB (12438092 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b25dc0fb9705edc6661711090bbb88c90560b516b861680a35178aaf986296a8`  
		Last Modified: Mon, 08 Dec 2025 20:36:32 GMT  
		Size: 251.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9df3e3c3fcc2bba3d34c49be0a42c155b93ce4bf7434accf72beafb185d61011`  
		Last Modified: Mon, 08 Dec 2025 21:13:14 GMT  
		Size: 6.7 MB (6717688 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:249b2e05caedcdb9b33eae3134a31c6903ef0ebe4bd1fb7524fb6372d1336bf8`  
		Last Modified: Mon, 08 Dec 2025 21:13:18 GMT  
		Size: 25.7 MB (25721114 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5521ff6cf19924b06d81d65132085a2884c9d16ef8d12f8b33a7ab10892a2c1d`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 10.4 KB (10438 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8fbb063fad282ec1ecd0eda6d419d1179e9ba7908dd0a38496b03a8976084e4`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 2.1 KB (2080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:alpine3.22` - unknown; unknown

```console
$ docker pull satosa@sha256:053b3548aded493f8b8d389ffdfa856d72a53956ec08f9d6cb9d1a0562071613
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **806.2 KB (806179 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6fdc00dcb12fdc98bc985aa473ee27ce5e931601d5e426d2ed8c559491bc45b7`

```dockerfile
```

-	Layers:
	-	`sha256:de6df0a0041eccd13155e23b861f0a62034e6a8535664f050f8341328c38b9d4`  
		Last Modified: Mon, 08 Dec 2025 23:14:06 GMT  
		Size: 783.2 KB (783219 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:aa32fe9c93af693fbacaf0283ddfeb2882849bc3b6e1066ee29e4dd85060f1fa`  
		Last Modified: Mon, 08 Dec 2025 23:14:07 GMT  
		Size: 23.0 KB (22960 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:alpine3.22` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:092eadb6a3d49e7ac1803172ff64eed6c55596b94ae18393e4e83e917bf1abc5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.1 MB (49093844 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:643ccb5cb566e62f38c946f4ed47ccf98a3dea79baf075ae1d9f2b8bf1b151e2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Wed, 08 Oct 2025 11:04:56 GMT
ADD alpine-minirootfs-3.22.2-aarch64.tar.gz / # buildkit
# Wed, 08 Oct 2025 11:04:56 GMT
CMD ["/bin/sh"]
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:13:36 GMT
RUN set -eux; 	apk add --no-cache 		ca-certificates 		tzdata 	; # buildkit
# Mon, 08 Dec 2025 20:13:36 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:13:36 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:20:06 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		dpkg-dev dpkg 		findutils 		gcc 		gdbm-dev 		gnupg 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		ncurses-dev 		openssl-dev 		pax-utils 		readline-dev 		sqlite-dev 		tar 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz 		xz-dev 		zlib-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="-DTHREAD_STACK_SIZE=0x100000"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(apk --print-arch)"; 		case "$arch" in 			x86_64|aarch64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			x86) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| xargs -rt apk add --no-network --virtual .python-rundeps 	; 	apk del --no-network .build-deps; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:20:06 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:20:06 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:11:21 GMT
RUN set -eux; 	addgroup --gid 1000 satosa; 	adduser -D -G satosa --uid 1000 satosa; 	apk add --no-cache 		bash 		jq 		libxml2-utils 		openssl 		xmlsec 	; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:11:43 GMT
RUN set -eux; 	apk add --no-cache --virtual .build-deps 		bluez-dev 		bzip2-dev 		cargo 		coreutils 		dpkg 		dpkg-dev 		expat-dev 		findutils 		gcc 		gdbm-dev 		libc-dev 		libffi-dev 		libnsl-dev 		libtirpc-dev 		linux-headers 		make 		musl-dev 		ncurses-dev 		openssl-dev 		pax-utils 		pkgconfig 		python3-dev 		readline-dev 		sqlite-dev 		tcl-dev 		tk 		tk-dev 		util-linux-dev 		xz-dev 		zlib-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec scanelf --needed --nobanner --format '%n#p' '{}' ';' 		| tr ',' '\n' 		| sort -u 		| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 		| fgrep -v libgcc_s- 		| fgrep -v libc.so 		| xargs -rt apk add --no-network --virtual .satosa-rundeps 	; 	apk del --no-network .build-deps; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:11:43 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:11:44 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:11:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:11:44 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:11:44 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:11:44 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:6b59a28fa20117e6048ad0616b8d8c901877ef15ff4c7f18db04e4f01f43bc39`  
		Last Modified: Sun, 07 Dec 2025 13:54:03 GMT  
		Size: 4.1 MB (4138069 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e04eda5d87448437994b338947f03a72065bf589d08071ba33ba5dc3ea1ddcf9`  
		Last Modified: Mon, 08 Dec 2025 20:20:23 GMT  
		Size: 459.0 KB (459020 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0e19756ed87e004e14deeb5d042df980b7204f44649d4cce479201223a8589ab`  
		Last Modified: Mon, 08 Dec 2025 20:20:23 GMT  
		Size: 12.5 MB (12453549 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1be90ee3c5e8855f927e9dabc42fd16e3baec85cb245b81e43412665495c6b4a`  
		Last Modified: Mon, 08 Dec 2025 20:20:22 GMT  
		Size: 247.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:34a131be40642a2cf885cdcb75474faaf4e6651804fc3f8cd6201c9960ca7d3f`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 6.7 MB (6694259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:50a8917a69ecc315188c393d384a8726146e9a2226632ec028e7e54a5546c701`  
		Last Modified: Mon, 08 Dec 2025 21:12:08 GMT  
		Size: 25.3 MB (25336149 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1b79bc7d0a94fb0a4eaa2b1cace6bf0e4b799d4e76449fa4b17cf2d02f9ed1a4`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 10.4 KB (10440 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dfd5054ceea4ea2377c4734c970adf4f763deaeaaa9e72dca0fbc2beda863685`  
		Last Modified: Mon, 08 Dec 2025 21:12:05 GMT  
		Size: 2.1 KB (2079 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:alpine3.22` - unknown; unknown

```console
$ docker pull satosa@sha256:fbfef43bbeaf94239cde0843248f928b598c0b683f6e8a8209428bceede91894
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **806.5 KB (806465 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2f04a24d13f86b5d751637955c00828100756cb72f170fb3422f7cd5bc8c6773`

```dockerfile
```

-	Layers:
	-	`sha256:fbe4e8fa0a2a61b3f561fcd5420ad68fb6cc07c61a2592e567ab105acdab481d`  
		Last Modified: Mon, 08 Dec 2025 23:14:10 GMT  
		Size: 783.3 KB (783323 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:24efd495e1ac9fb1735f89706533f4d82e1c5bc1d3747b3cb4d0a599225a46fb`  
		Last Modified: Mon, 08 Dec 2025 23:14:11 GMT  
		Size: 23.1 KB (23142 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:bookworm`

```console
$ docker pull satosa@sha256:47cab947e2477f7a89747951af0cca8f8d911c9807dc8aa2d0a0eb66d2b0b5d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:bookworm` - linux; amd64

```console
$ docker pull satosa@sha256:02d11444e8397d8cf844cfe4966790e8acd11bb96df692b0d2246fdc4b84e724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91546319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fdbbd78fb77c1c45bf4c6de659e0b646927937253d1ea05101ef20673dc9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:33:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:33:46 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:43:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:43:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:43:53 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:11:52 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:12:46 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:12:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:12:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:12:47 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:12:47 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:12:47 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009f5cc336e3b76a99df531b878e328e7a550219c8956a8a194aa3b0d195db91`  
		Last Modified: Mon, 08 Dec 2025 20:44:07 GMT  
		Size: 3.5 MB (3515868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661abbc8fe10b243e7e573653867ccaa905ddb32a37a534e407d8d13edf850b`  
		Last Modified: Mon, 08 Dec 2025 20:44:12 GMT  
		Size: 12.5 MB (12470573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed91f2f794eb4b70d66bbfdcc185d49c206fe04adc5a2342583287af687d5a1`  
		Last Modified: Mon, 08 Dec 2025 20:44:07 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79acb76c9c0b4b230bfe39a96674638997c6e3e604a3ac06679eff10f301a3ed`  
		Last Modified: Mon, 08 Dec 2025 21:13:17 GMT  
		Size: 21.5 MB (21456825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2375cde2b745416d789de4916d59cca9acbe71b560fab10770ef2334ab8b7c0`  
		Last Modified: Mon, 08 Dec 2025 21:13:24 GMT  
		Size: 25.9 MB (25861803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb2815d937de7372beed80131c8ea74f531bfef1e5e42327f78e5845b8d3a94`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 10.4 KB (10441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddafdd0c89bdf32c613738b8bf29e31ecf1b9378a6090d858a7161e166ad0ea`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:ba2a77056920b0b8c29c5c1cd5b4ad488cd5d77b6b98a2c1d8fb0b8166659112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139237f34ca29fe7e6eca10a086e04e1388e05fb722c6a11c6898ee2afc51c90`

```dockerfile
```

-	Layers:
	-	`sha256:74f9eb40f65c4cc8706a37a324099d2b084fa1e4996275f01a193b1dedc06bc4`  
		Last Modified: Mon, 08 Dec 2025 23:13:58 GMT  
		Size: 2.7 MB (2704633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59c7c8a0e3d3d3e331479afb101f477f0105ef999c2fec379b98c7e55d61f69b`  
		Last Modified: Mon, 08 Dec 2025 23:13:59 GMT  
		Size: 22.3 KB (22266 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:bookworm` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e6034f8923cc420bf624c03933ca51d3fa3fa53369e574d01519048130a6ea08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90626193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a048ae55480d2f33d8cfc4e898989706e7365329e4c1dd6033c938644b7e9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:10:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:10:26 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:23:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:23:02 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:23:02 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:10:47 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:11:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:11:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:11:36 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:11:36 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:11:36 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067a176e286689d9a5616e9a9ccb474753231475a3b74b8c4eb6897476010420`  
		Last Modified: Mon, 08 Dec 2025 20:37:28 GMT  
		Size: 3.3 MB (3349161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fc0b8bf8e30d988c0f398a3673770af657a9ad94ba5605b3c5ff9927aa69d4`  
		Last Modified: Mon, 08 Dec 2025 21:10:40 GMT  
		Size: 12.4 MB (12372485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfc60c769de0a434549492e317c8c2ff2cae1e4a35d3c369d631538c2588087`  
		Last Modified: Mon, 08 Dec 2025 20:37:37 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572f90ee4f08e9e7e4545f1fec7a2502d142eddf118a4fd7bf2645c7be56ef69`  
		Last Modified: Mon, 08 Dec 2025 21:12:08 GMT  
		Size: 21.3 MB (21306657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8001b73c61fa8c9d9ac229832e7a11cf353654a05001f5774eddb626e0a8e`  
		Last Modified: Mon, 08 Dec 2025 21:12:13 GMT  
		Size: 25.5 MB (25482878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8968998041481e37921326fcbf07ff2ed641dcba0c5c05dca511426bf6870817`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 10.4 KB (10439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebca083d50d345d85ac73c6847800d6f5240548843ad64f9930b46be656536d`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:bookworm` - unknown; unknown

```console
$ docker pull satosa@sha256:1b7e4ec015d578ac03adee68f7e1eef5a0a20228c6bdb3e3e7a0aa69ba363f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2727406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef91488e298c4cf89b88685f361b8c0e0b25207e9096cc5309b29b59e8087d0`

```dockerfile
```

-	Layers:
	-	`sha256:c2688d87a56f8ed7f757ae7f9a2eca3beece73a77533054ff78d0b527bd9a223`  
		Last Modified: Mon, 08 Dec 2025 23:14:03 GMT  
		Size: 2.7 MB (2704959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a6c70eeb25bdce5e4963b184cbb29ab0ecd0c886fe9ce1ac44cfda2be17eebf`  
		Last Modified: Mon, 08 Dec 2025 23:14:04 GMT  
		Size: 22.4 KB (22447 bytes)  
		MIME: application/vnd.in-toto+json

## `satosa:latest`

```console
$ docker pull satosa@sha256:47cab947e2477f7a89747951af0cca8f8d911c9807dc8aa2d0a0eb66d2b0b5d8
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `satosa:latest` - linux; amd64

```console
$ docker pull satosa@sha256:02d11444e8397d8cf844cfe4966790e8acd11bb96df692b0d2246fdc4b84e724
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.5 MB (91546319 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fdbbd78fb77c1c45bf4c6de659e0b646927937253d1ea05101ef20673dc9a0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'bookworm' '@1763337600'
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:33:46 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:33:46 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:33:46 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:43:53 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:43:53 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:43:53 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:11:52 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:12:46 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:12:46 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:12:47 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:12:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:12:47 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:12:47 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:12:47 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:8e44f01296e3a6fdc31a671bee1c2259c5d5ee8b49f29aec42b5d2af15600296`  
		Last Modified: Tue, 18 Nov 2025 02:27:00 GMT  
		Size: 28.2 MB (28228449 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:009f5cc336e3b76a99df531b878e328e7a550219c8956a8a194aa3b0d195db91`  
		Last Modified: Mon, 08 Dec 2025 20:44:07 GMT  
		Size: 3.5 MB (3515868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b661abbc8fe10b243e7e573653867ccaa905ddb32a37a534e407d8d13edf850b`  
		Last Modified: Mon, 08 Dec 2025 20:44:12 GMT  
		Size: 12.5 MB (12470573 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ed91f2f794eb4b70d66bbfdcc185d49c206fe04adc5a2342583287af687d5a1`  
		Last Modified: Mon, 08 Dec 2025 20:44:07 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79acb76c9c0b4b230bfe39a96674638997c6e3e604a3ac06679eff10f301a3ed`  
		Last Modified: Mon, 08 Dec 2025 21:13:17 GMT  
		Size: 21.5 MB (21456825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2375cde2b745416d789de4916d59cca9acbe71b560fab10770ef2334ab8b7c0`  
		Last Modified: Mon, 08 Dec 2025 21:13:24 GMT  
		Size: 25.9 MB (25861803 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fb2815d937de7372beed80131c8ea74f531bfef1e5e42327f78e5845b8d3a94`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 10.4 KB (10441 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3ddafdd0c89bdf32c613738b8bf29e31ecf1b9378a6090d858a7161e166ad0ea`  
		Last Modified: Mon, 08 Dec 2025 21:13:13 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:latest` - unknown; unknown

```console
$ docker pull satosa@sha256:ba2a77056920b0b8c29c5c1cd5b4ad488cd5d77b6b98a2c1d8fb0b8166659112
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2726899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:139237f34ca29fe7e6eca10a086e04e1388e05fb722c6a11c6898ee2afc51c90`

```dockerfile
```

-	Layers:
	-	`sha256:74f9eb40f65c4cc8706a37a324099d2b084fa1e4996275f01a193b1dedc06bc4`  
		Last Modified: Mon, 08 Dec 2025 23:13:58 GMT  
		Size: 2.7 MB (2704633 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:59c7c8a0e3d3d3e331479afb101f477f0105ef999c2fec379b98c7e55d61f69b`  
		Last Modified: Mon, 08 Dec 2025 23:13:59 GMT  
		Size: 22.3 KB (22266 bytes)  
		MIME: application/vnd.in-toto+json

### `satosa:latest` - linux; arm64 variant v8

```console
$ docker pull satosa@sha256:e6034f8923cc420bf624c03933ca51d3fa3fa53369e574d01519048130a6ea08
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **90.6 MB (90626193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:88a048ae55480d2f33d8cfc4e898989706e7365329e4c1dd6033c938644b7e9f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["gunicorn","-b0.0.0.0:8080","satosa.wsgi:app"]`

```dockerfile
# Mon, 17 Nov 2025 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'bookworm' '@1763337600'
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 08 Dec 2025 20:10:26 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 08 Dec 2025 20:10:26 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PYTHON_VERSION=3.13.11
# Mon, 08 Dec 2025 20:10:26 GMT
ENV PYTHON_SHA256=16ede7bb7cdbfa895d11b0642fa0e523f291e6487194d53cf6d3b338c3a17ea2
# Mon, 08 Dec 2025 20:23:01 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 		arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 		case "$arch" in 			amd64|arm64) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 				;; 			i386) 				;; 			*) 				EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 				;; 		esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Mon, 08 Dec 2025 20:23:02 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 08 Dec 2025 20:23:02 GMT
CMD ["python3"]
# Mon, 08 Dec 2025 21:10:47 GMT
RUN set -eux; 	groupadd -g 1000 satosa; 	useradd -m -g 1000 -u 1000 satosa; 	apt-get update; 	apt-get install -y --no-install-recommends 		jq 		libxml2-utils 		xmlsec1 	; 	rm -rf /var/lib/apt/lists/*; 	pip install --no-cache-dir 		yq 	; # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
ENV SATOSA_VERSION=8.5.1
# Mon, 08 Dec 2025 21:11:36 GMT
RUN set -eux; 	savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		cargo 		dirmngr 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		pkg-config 		python3-dev 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 	pip install --no-cache-dir 		satosa[idpy_oidc_backend,ldap,pyop_mongo,pyop_redis]==${SATOSA_VERSION} 	; 	apt-mark auto '.*' > /dev/null; 	[ -z "$savedAptMark" ] || apt-mark manual $savedAptMark > /dev/null; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 	mkdir /etc/satosa; 	chown -R satosa:satosa /etc/satosa # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
RUN set -eux; 	python -c 'import urllib.request; urllib.request.urlretrieve("https://github.com/IdentityPython/SATOSA/archive/refs/tags/v'${SATOSA_VERSION%%[a-z]*}'.tar.gz","/tmp/satosa.tgz")'; 	mkdir /usr/share/satosa; 	tar --extract --directory /usr/share/satosa --strip-components=1 --file /tmp/satosa.tgz SATOSA-${SATOSA_VERSION%%[a-z]*}/example/; 	rm /tmp/satosa.tgz # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
WORKDIR /etc/satosa
# Mon, 08 Dec 2025 21:11:36 GMT
COPY docker-entrypoint.sh /usr/local/bin/ # buildkit
# Mon, 08 Dec 2025 21:11:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 08 Dec 2025 21:11:36 GMT
EXPOSE map[8080/tcp:{}]
# Mon, 08 Dec 2025 21:11:36 GMT
USER satosa:satosa
# Mon, 08 Dec 2025 21:11:36 GMT
CMD ["gunicorn" "-b0.0.0.0:8080" "satosa.wsgi:app"]
```

-	Layers:
	-	`sha256:1aee4545ebb8911538c1c2ebce2416c85af34096ca1a65bbe42a4ca157ca3fa2`  
		Last Modified: Tue, 18 Nov 2025 01:13:19 GMT  
		Size: 28.1 MB (28102207 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:067a176e286689d9a5616e9a9ccb474753231475a3b74b8c4eb6897476010420`  
		Last Modified: Mon, 08 Dec 2025 20:37:28 GMT  
		Size: 3.3 MB (3349161 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78fc0b8bf8e30d988c0f398a3673770af657a9ad94ba5605b3c5ff9927aa69d4`  
		Last Modified: Mon, 08 Dec 2025 21:10:40 GMT  
		Size: 12.4 MB (12372485 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8bfc60c769de0a434549492e317c8c2ff2cae1e4a35d3c369d631538c2588087`  
		Last Modified: Mon, 08 Dec 2025 20:37:37 GMT  
		Size: 256.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:572f90ee4f08e9e7e4545f1fec7a2502d142eddf118a4fd7bf2645c7be56ef69`  
		Last Modified: Mon, 08 Dec 2025 21:12:08 GMT  
		Size: 21.3 MB (21306657 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7bb8001b73c61fa8c9d9ac229832e7a11cf353654a05001f5774eddb626e0a8e`  
		Last Modified: Mon, 08 Dec 2025 21:12:13 GMT  
		Size: 25.5 MB (25482878 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8968998041481e37921326fcbf07ff2ed641dcba0c5c05dca511426bf6870817`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 10.4 KB (10439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7ebca083d50d345d85ac73c6847800d6f5240548843ad64f9930b46be656536d`  
		Last Modified: Mon, 08 Dec 2025 21:12:06 GMT  
		Size: 2.1 KB (2078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `satosa:latest` - unknown; unknown

```console
$ docker pull satosa@sha256:1b7e4ec015d578ac03adee68f7e1eef5a0a20228c6bdb3e3e7a0aa69ba363f42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2727406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ef91488e298c4cf89b88685f361b8c0e0b25207e9096cc5309b29b59e8087d0`

```dockerfile
```

-	Layers:
	-	`sha256:c2688d87a56f8ed7f757ae7f9a2eca3beece73a77533054ff78d0b527bd9a223`  
		Last Modified: Mon, 08 Dec 2025 23:14:03 GMT  
		Size: 2.7 MB (2704959 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7a6c70eeb25bdce5e4963b184cbb29ab0ecd0c886fe9ce1ac44cfda2be17eebf`  
		Last Modified: Mon, 08 Dec 2025 23:14:04 GMT  
		Size: 22.4 KB (22447 bytes)  
		MIME: application/vnd.in-toto+json
