## `hylang:1-python3.9-bullseye`

```console
$ docker pull hylang@sha256:1b463c1976408b17f7fc3e9d338b379be8a272b83870a37a2affa4047027628c
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; arm variant v5
	-	unknown; unknown

### `hylang:1-python3.9-bullseye` - linux; arm variant v5

```console
$ docker pull hylang@sha256:c5d356f44dfd71578f78e5f9794e26ee3d1995b440a93aaf948a52e137da1bb6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.3 MB (47290479 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d4efa41a045da7bd36ae69443965c7c979f3d50427d2f636b0562cdcb0172ae`
-	Default Command: `["hy"]`

```dockerfile
# Wed, 04 Sep 2024 21:48:48 GMT
ADD file:b6f3f19f4bd2bf78068380b3cd10d72519ced99a2b5abe830b4729df341dcfdf in / 
# Wed, 04 Sep 2024 21:48:48 GMT
CMD ["bash"]
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Mon, 09 Sep 2024 17:16:05 GMT
ENV LANG=C.UTF-8
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
ENV GPG_KEY=E3FF2839C048B25C084DEBE9B26995E310250568
# Mon, 09 Sep 2024 17:16:05 GMT
ENV PYTHON_VERSION=3.9.20
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libexpat1-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		--with-system-expat 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:--Wl},--strip-all"; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 		"PROFILE_TASK=${PROFILE_TASK:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:--Wl},-rpath='\$\$ORIGIN/../lib'" 		"PROFILE_TASK=${PROFILE_TASK:-}" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	rm -rf /var/lib/apt/lists/*; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 		pip3 install 		--disable-pip-version-check 		--no-cache-dir 		--no-compile 		'setuptools==58.1.0' 		wheel 	; 	pip3 --version # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Mon, 09 Sep 2024 17:16:05 GMT
CMD ["python3"]
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HY_VERSION=1.0.0
# Mon, 23 Sep 2024 18:27:06 GMT
ENV HYRULE_VERSION=0.7.0
# Mon, 23 Sep 2024 18:27:06 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Mon, 23 Sep 2024 18:27:06 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:c8ed7888c72e20491bc1a05ae8b473757ca4d400de33029eab69bacfb9dd933b`  
		Last Modified: Wed, 04 Sep 2024 21:52:15 GMT  
		Size: 28.9 MB (28924911 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:97807cce5cf83b1c41b0da06d4fa6f187874b42c006053352ec652b3c623a32f`  
		Last Modified: Thu, 05 Sep 2024 09:39:41 GMT  
		Size: 1.1 MB (1059669 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9818bb27a111f525858e5776921a09a79ce6d9f45eff4fcd6d64dfbaf33a08ce`  
		Last Modified: Fri, 13 Sep 2024 01:10:14 GMT  
		Size: 13.6 MB (13636043 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5f05ece179727996f58faf9b977f106b1dcd48b50ee091a4123f439f5e207b89`  
		Last Modified: Fri, 13 Sep 2024 01:10:13 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e21c59530c9197f7c568c3adb620d972729d8b895d54c424f57efd8152817e1b`  
		Last Modified: Tue, 24 Sep 2024 01:05:11 GMT  
		Size: 3.7 MB (3669606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:1-python3.9-bullseye` - unknown; unknown

```console
$ docker pull hylang@sha256:39a711f2154f79d2594aeddb02bb3e6b067eeff8c5578ef83323648b8b2b859d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.7 MB (2717917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ae1bb5a941841f4b90de99784c814865ef6a83fea003acbeee16e72bda5a25a`

```dockerfile
```

-	Layers:
	-	`sha256:5dce0a31228df23b6f72255e3174128041b32337a56c942a853458f261ac8129`  
		Last Modified: Tue, 24 Sep 2024 01:05:11 GMT  
		Size: 2.7 MB (2709927 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7131b8643a91ce1a30f34a24221711c0aa70bec5d7f72ad45319f435da91f7c3`  
		Last Modified: Tue, 24 Sep 2024 01:05:11 GMT  
		Size: 8.0 KB (7990 bytes)  
		MIME: application/vnd.in-toto+json
