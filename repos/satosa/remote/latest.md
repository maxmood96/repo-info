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
