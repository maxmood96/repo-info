## `hylang:python3.13`

```console
$ docker pull hylang@sha256:a7cdf5905e9b3961c807f5afe42f48194a5718225b97fff07a9015ba30c8b1cd
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
	-	windows version 10.0.26100.32690; amd64
	-	windows version 10.0.20348.5020; amd64

### `hylang:python3.13` - linux; amd64

```console
$ docker pull hylang@sha256:6c39ac30b379aac61f95cb0ef07c8fc9afd1ab87fc16d018ebb77ab85c245b12
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.2 MB (48238768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e9b2ac9e14df14db912b4cfaf26fc8a3ef7df94537158944c441a8558c98f581`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:00:06 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:00:06 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:00:06 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 22 Apr 2026 02:00:06 GMT
ENV PYTHON_VERSION=3.13.13
# Wed, 22 Apr 2026 02:00:06 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Wed, 22 Apr 2026 02:09:26 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 02:09:27 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 02:09:27 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 04:59:58 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 04:59:58 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 04:59:58 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 04:59:58 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3531af2bc2a9c8883754652783cf96207d53189db279c9637b7157d034de7ecd`  
		Last Modified: Wed, 22 Apr 2026 00:17:32 GMT  
		Size: 29.8 MB (29780174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3f977313cbf20d1fcbf9d25f28735d97b7bc691319bc43f8c539c8d05c9cf886`  
		Last Modified: Wed, 22 Apr 2026 02:09:35 GMT  
		Size: 1.3 MB (1293080 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a51d847b5d4902dac7726e34078eeb8e64ee8047b67ea02877acabcef191b07f`  
		Last Modified: Wed, 22 Apr 2026 02:09:35 GMT  
		Size: 11.8 MB (11823653 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb7aeb6e31180144e93bad8e32441038f4c4520ec825039827c05fadcc01305f`  
		Last Modified: Wed, 22 Apr 2026 02:09:35 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4686f0a95575ec63e5d62ea6b7203be5866a3fb7a24283b676c495e9fbe00643`  
		Last Modified: Wed, 22 Apr 2026 05:00:10 GMT  
		Size: 5.3 MB (5341612 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:815cd9bb9771015c683739a16e308d41c5fda1bb7e1d84c07360575b75bc7980
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2163566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:82ff85e90e1f6942d4ee9efb44efb538c5830539d8571d0dc18266352d545bd3`

```dockerfile
```

-	Layers:
	-	`sha256:c8e48c20597ccc3264ce3e405c8816677d4b6c580ad8acbfa7aeca0a5830d956`  
		Last Modified: Wed, 22 Apr 2026 05:00:10 GMT  
		Size: 2.2 MB (2154261 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:0d1014f1c2da8f0e5e9dc6102f2897bee561a8d0bb3a073bb702af4af5db75d3`  
		Last Modified: Wed, 22 Apr 2026 05:00:08 GMT  
		Size: 9.3 KB (9305 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; arm variant v5

```console
$ docker pull hylang@sha256:7653897d56e3be6b27109a8a90407b7e4233046f8735a0ed3cb8d2c1178d8669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.1 MB (46082558 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d000499ad11697e76c34e5941d9e5cb4b9aa31b85c19c8b0955d3dd01ffc9f40`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:33:07 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:33:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:33:07 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 22 Apr 2026 02:33:07 GMT
ENV PYTHON_VERSION=3.13.13
# Wed, 22 Apr 2026 02:33:07 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Wed, 22 Apr 2026 02:54:05 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 02:54:05 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 02:54:05 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 04:08:44 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 04:08:44 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 04:08:44 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 04:08:44 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:6496d93bca0663211b9252da346044ecb734ee5b3ecaae5b1fbd230753faee2f`  
		Last Modified: Wed, 22 Apr 2026 00:15:59 GMT  
		Size: 27.9 MB (27948180 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6db1abc7b40de04143ed3b617c061695e90efff7d37b25cc1810125cd7563167`  
		Last Modified: Wed, 22 Apr 2026 02:54:13 GMT  
		Size: 1.3 MB (1276222 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fe18f89d90e138458c6e652e7d6cdd94a7a1c9e4d2cc8d8f633017ebbf9a974e`  
		Last Modified: Wed, 22 Apr 2026 02:54:13 GMT  
		Size: 11.5 MB (11515992 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb3d97705486ee1bbc44eb81d5cbcc48ee1f6540d6dfc28115f9f3b09fc9c6dc`  
		Last Modified: Wed, 22 Apr 2026 02:54:13 GMT  
		Size: 248.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f18c6e859739dd5b7b6de102621fec476dc794f909c1e67fbf4f01ddf6035751`  
		Last Modified: Wed, 22 Apr 2026 04:08:51 GMT  
		Size: 5.3 MB (5341916 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:57c7fce39de601cb5f04ac9c38fa4d31f9987f3cfdc8a844ee6cf0b45de7e073
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2166679 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7921dfd4e90109590165ef003029ada9692e0ead57c75372217035167c112a53`

```dockerfile
```

-	Layers:
	-	`sha256:c30aa6dfcfb884f5f2fac70a3501b1a23e225d857ecad676370abfac4c3549ff`  
		Last Modified: Wed, 22 Apr 2026 04:08:51 GMT  
		Size: 2.2 MB (2157262 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f08169c858442ef888e0645aae37c8d7ad7a464a6c568b32c015a6fb63f308a9`  
		Last Modified: Wed, 22 Apr 2026 04:08:51 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; arm variant v7

```console
$ docker pull hylang@sha256:2f3f466f5c4ed81dd31292b14d275c9bfdde2926d4dbfc519cb06ac745d03e9a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.0 MB (44041303 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e015e7a2b2ca597a4ca1fee10a9cc6a759bddef7d08a03af0d615075df0b4ce`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:09:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 03:09:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:09:19 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 22 Apr 2026 03:09:19 GMT
ENV PYTHON_VERSION=3.13.13
# Wed, 22 Apr 2026 03:09:19 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Wed, 22 Apr 2026 03:31:16 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 03:31:16 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 03:31:16 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 04:17:52 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 04:17:52 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 04:17:52 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 04:17:52 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:9e541e5bfbbe69b7bbe01cd2f1abf8560e2e43bf76eb96b2e88a3df29020834b`  
		Last Modified: Wed, 22 Apr 2026 00:17:02 GMT  
		Size: 26.2 MB (26214838 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:917ba6eeb28609b3008e58367f36b0439467a158d34a9aad30b1a8b8285c3491`  
		Last Modified: Wed, 22 Apr 2026 03:31:24 GMT  
		Size: 1.2 MB (1249094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a5bdda6a0aeaf992e47e8540869f10c1b245ef518e84a9355e26b5d91595e853`  
		Last Modified: Wed, 22 Apr 2026 03:31:24 GMT  
		Size: 11.2 MB (11235520 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2ef9f97544c1e5cf5d686b9cbdf05fbdb0726120d96497a4976174cd46726324`  
		Last Modified: Wed, 22 Apr 2026 03:31:24 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0796fcb529dea729f47f4b503bfa6e0fe6c15fd53a0d6b49c8d21c2cb21045e`  
		Last Modified: Wed, 22 Apr 2026 04:17:59 GMT  
		Size: 5.3 MB (5341602 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:e4822a0a11c2ba24e8d9db967cded4b71ab0b8b0c33756f4b9c92ece4a171050
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:770b43b03b0fbfa7420fc4455774dbb1db3a0f471360c3bcd762c3418b2c9aea`

```dockerfile
```

-	Layers:
	-	`sha256:4a95fdaf17d2198ad6afdee32f7df1584206d8a81f85c02b8d651d5c5b0cd127`  
		Last Modified: Wed, 22 Apr 2026 04:17:58 GMT  
		Size: 2.2 MB (2155715 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:20126474ce1892063ae742dae747177ff854609e76b8b8100e779e7e31dbdf7e`  
		Last Modified: Wed, 22 Apr 2026 04:17:58 GMT  
		Size: 9.4 KB (9417 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; arm64 variant v8

```console
$ docker pull hylang@sha256:6cf2fe4dedf08da0e7ee8c7cefe9c65f642db9798710707b93b6ef2c8b654ebd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.5 MB (48510482 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e9e5bc1ec37633a47935ea8a723f7dace03a856f101aa05f0c38a2888d91c34`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 02:00:35 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 02:00:35 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 02:00:35 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 22 Apr 2026 02:00:35 GMT
ENV PYTHON_VERSION=3.13.13
# Wed, 22 Apr 2026 02:00:35 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Wed, 22 Apr 2026 02:14:11 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 02:14:12 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 02:14:12 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 02:48:04 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 02:48:04 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 02:48:04 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 02:48:04 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:e4fb5f1cd4d4ee56da574ef5ed88a5c74f100ba98caacf6c5ef26cee66525179`  
		Last Modified: Wed, 22 Apr 2026 00:16:43 GMT  
		Size: 30.1 MB (30143606 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77147f59c0641698b2116ad59ac51b9f80aa3606c3440e2a02833b3df966383f`  
		Last Modified: Wed, 22 Apr 2026 02:14:20 GMT  
		Size: 1.3 MB (1273871 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85ca06eb999e8052f7ab3c5287687e23c305af5ad0853bb3077bc150bc6aebd5`  
		Last Modified: Wed, 22 Apr 2026 02:14:20 GMT  
		Size: 11.8 MB (11751234 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d066deb7ef19cbd348c908bb61bcf4a99a51cb31944437929250556989ad1ae4`  
		Last Modified: Wed, 22 Apr 2026 02:14:19 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:164c78584727d609868173cbe85b2def262faa4436f3283ae10f843c50d3944e`  
		Last Modified: Wed, 22 Apr 2026 02:48:11 GMT  
		Size: 5.3 MB (5341522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:f31d22ea65e596b2e3b60e51bef17881966161bf4b9811c36a9a1144bf7cfb9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2164032 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f045745145cc35df7a630087d3a1681f93aff983de8af72a478289d3841cb499`

```dockerfile
```

-	Layers:
	-	`sha256:ab48ed6fbe4e4d5a21f3dbb8ad5cff88c3442b0834ac2e56a70f4093b6bf4a24`  
		Last Modified: Wed, 22 Apr 2026 02:48:11 GMT  
		Size: 2.2 MB (2154575 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f27c583b95abb99dcb8faf3c102e81bafdba561c5629fd5c70473828a64cb56f`  
		Last Modified: Wed, 22 Apr 2026 02:48:11 GMT  
		Size: 9.5 KB (9457 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; 386

```console
$ docker pull hylang@sha256:8e75914d27f2433f0b65a375235df83553c97ba78d6b9c7c1d19d6d519a5997f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49792525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3e4baea7d1e5ce6558ca05d4b3e3cde4c246b8267387babed0235ef37201c9e`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1775433600'
# Tue, 07 Apr 2026 01:59:19 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Tue, 07 Apr 2026 01:59:19 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Tue, 07 Apr 2026 01:59:19 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Tue, 07 Apr 2026 01:59:19 GMT
ENV PYTHON_VERSION=3.13.12
# Tue, 07 Apr 2026 01:59:19 GMT
ENV PYTHON_SHA256=2a84cd31dd8d8ea8aaff75de66fc1b4b0127dd5799aa50a64ae9a313885b4593
# Tue, 07 Apr 2026 02:20:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Tue, 07 Apr 2026 02:20:30 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Tue, 07 Apr 2026 02:20:30 GMT
CMD ["python3"]
# Tue, 07 Apr 2026 03:20:35 GMT
ENV HY_VERSION=1.2.0
# Tue, 07 Apr 2026 03:20:35 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 07 Apr 2026 03:20:35 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Tue, 07 Apr 2026 03:20:35 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:3c3d391a832256e6eca1fcef63254ce2b8cf2d25bc53ac0b56d9de64a11a7f30`  
		Last Modified: Tue, 07 Apr 2026 00:11:35 GMT  
		Size: 31.3 MB (31291252 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4a61dbf07cb27b99e12ab9c00a5828bccc53975fb9ad9f6d2611d813569dcaf5`  
		Last Modified: Tue, 07 Apr 2026 02:20:37 GMT  
		Size: 1.3 MB (1297233 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfc16e30dac1cc7fb1011e604e6f521d36a1357d8e17026e37df9993ecc57616`  
		Last Modified: Tue, 07 Apr 2026 02:20:37 GMT  
		Size: 11.9 MB (11907461 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bccad2c2f683b79fee2ed3ae1f48c360192af367b2921d57905c4b3ace59470e`  
		Last Modified: Tue, 07 Apr 2026 02:20:37 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79536a29da319e9c55595683c8cb50ef68e77eefcdbb77a55752bd77721b398d`  
		Last Modified: Tue, 07 Apr 2026 03:20:42 GMT  
		Size: 5.3 MB (5296329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:a934f431cb612691227c8682255dbdc22c1f4a7d00a5d017f84957da41114a44
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2160667 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59bd9bc21c0abcd4e93f58e669ab9e8992e38bebb9f36fcd2edd0209f7b1841c`

```dockerfile
```

-	Layers:
	-	`sha256:2c323ff87d7b607ec6bd8f88a35165a5943cd901afe1eb4b33088db90867b10f`  
		Last Modified: Tue, 07 Apr 2026 03:20:42 GMT  
		Size: 2.2 MB (2151414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d0de6e364272d5a60e83a42ee0ee5604c792e36cd5b2f5f961891ca8d421f8e2`  
		Last Modified: Tue, 07 Apr 2026 03:20:42 GMT  
		Size: 9.3 KB (9253 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; ppc64le

```console
$ docker pull hylang@sha256:9a2f46a862cf765d22be5aec966ed869abdb2e1281e12e8241070f38edb659b2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.5 MB (52475529 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6ddd28147ffb3c5a86752069d89e24771950c65d574bb8895c7d57af7f86036`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 05:15:24 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 05:15:24 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 05:15:24 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 22 Apr 2026 05:15:24 GMT
ENV PYTHON_VERSION=3.13.13
# Wed, 22 Apr 2026 05:15:24 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Wed, 22 Apr 2026 06:37:36 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 06:37:36 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 06:37:36 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 11:55:54 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 11:55:54 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 11:55:54 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 11:55:54 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:b5fd051d0fcd0789e7358cba300f83befdba943416041497be86050e282a6d02`  
		Last Modified: Wed, 22 Apr 2026 00:18:18 GMT  
		Size: 33.6 MB (33598032 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f111c0180379849c2242c25410e5cfba1da759760c6fd915b382423a79dfeb09`  
		Last Modified: Wed, 22 Apr 2026 05:38:44 GMT  
		Size: 1.3 MB (1320835 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e668cfc5fed02e733e3b9e2d7c8ce660cc0af63a3d1aa96c85fe8399a10e457e`  
		Last Modified: Wed, 22 Apr 2026 06:38:00 GMT  
		Size: 12.2 MB (12214384 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f66caad9e36b2f4e1348205ebac183c021e422c035a9aa5e13aadc6c936fcacf`  
		Last Modified: Wed, 22 Apr 2026 06:37:59 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8964ae3aca18c2698a46aba1b8531eaee93223febad32af0c6b9ad37fac55f8`  
		Last Modified: Wed, 22 Apr 2026 11:56:14 GMT  
		Size: 5.3 MB (5342029 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:8be0844c5320c3832579d32018ef7aaf29eb7878edc356ab66d46677af09098c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2167225 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:376f71861986f5bb79a8736b995da32cba1db242d03555cd5f6a12278b11249a`

```dockerfile
```

-	Layers:
	-	`sha256:65e3344850769042ce95df06a67c17603fa3fee137e11f80cfd33b740c9a66f2`  
		Last Modified: Wed, 22 Apr 2026 11:56:14 GMT  
		Size: 2.2 MB (2157852 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:13594feda861e29d3e4413f20e6b98ddb0a4c55aab855b98de8f8ae211873ba8`  
		Last Modified: Wed, 22 Apr 2026 11:56:14 GMT  
		Size: 9.4 KB (9373 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; riscv64

```console
$ docker pull hylang@sha256:01cadec88fdfc7505c579b68e6bba2858fe15188b4f464b7fd8b370ea792f5db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.3 MB (49282209 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cb82ce5d2c12a0033f53031d0e05cafa9e80ec55d98e228ebecff1be00d0725c`
-	Default Command: `["hy"]`

```dockerfile
# Mon, 06 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1775433600'
# Sat, 11 Apr 2026 11:06:39 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Sat, 11 Apr 2026 11:06:39 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Sat, 11 Apr 2026 11:06:39 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Sat, 11 Apr 2026 11:06:39 GMT
ENV PYTHON_VERSION=3.13.13
# Sat, 11 Apr 2026 11:06:39 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Sat, 11 Apr 2026 18:31:17 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Sat, 11 Apr 2026 18:31:17 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Sat, 11 Apr 2026 18:31:17 GMT
CMD ["python3"]
# Sun, 12 Apr 2026 19:37:27 GMT
ENV HY_VERSION=1.2.0
# Sun, 12 Apr 2026 19:37:27 GMT
ENV HYRULE_VERSION=1.0.1
# Sun, 12 Apr 2026 19:37:27 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Sun, 12 Apr 2026 19:37:27 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:51128e253868f85aa5e3b9e86448414d946e8a6b685e02db1030aaa2b11e81d4`  
		Last Modified: Tue, 07 Apr 2026 01:55:37 GMT  
		Size: 28.3 MB (28275778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:14380c29384b5ed760b6898c4ce267c4a4b26800f0f895ed3c6f7c1456191663`  
		Last Modified: Sat, 11 Apr 2026 12:44:35 GMT  
		Size: 3.9 MB (3873978 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b07d7912715b47be9f8c8907d48d943b6ac927a83e3263655a4b4387f689f6f6`  
		Last Modified: Sat, 11 Apr 2026 18:32:24 GMT  
		Size: 11.8 MB (11810785 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7f9d10c85e0c5881d68a51b32adef84e04bb83c6ae1fa22a1573dc4371f0c8b7`  
		Last Modified: Sat, 11 Apr 2026 18:32:23 GMT  
		Size: 250.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:35436d0565395ab29fd03beece1ee299ac435c52bbd61a67431b27afd278c647`  
		Last Modified: Sun, 12 Apr 2026 19:38:27 GMT  
		Size: 5.3 MB (5321418 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:0b7d97a3bd3b2c8a4937e83f4eabc0005ffad80d9a2131d557d1220f8dde3114
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2157595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:528b880046f841d40d42951570a26dbb51871c20f20716e5e67a573f701af9d4`

```dockerfile
```

-	Layers:
	-	`sha256:84f32b53c7e4a07f7e52be4bc64b72585f5b594cbc2ae5f1cf007e03d28816a2`  
		Last Modified: Sun, 12 Apr 2026 19:38:27 GMT  
		Size: 2.1 MB (2148223 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:71816f41644e23f35334907634acf14d933c45dc839b14370bf370accb436c6c`  
		Last Modified: Sun, 12 Apr 2026 19:38:26 GMT  
		Size: 9.4 KB (9372 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - linux; s390x

```console
$ docker pull hylang@sha256:f67b7eabbc77acd910c9c8786cf9680c7d6ccf62de0c19f5223909fad5850bff
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48359958 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6990b48c3e97933aa9d0f9ad6d87137484515c913f6c202bf0e2927443cbba0`
-	Default Command: `["hy"]`

```dockerfile
# Tue, 21 Apr 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1776729600'
# Wed, 22 Apr 2026 03:15:05 GMT
ENV PATH=/usr/local/bin:/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin
# Wed, 22 Apr 2026 03:15:05 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		netbase 		tzdata 	; 	apt-get dist-clean # buildkit
# Wed, 22 Apr 2026 03:15:05 GMT
ENV GPG_KEY=7169605F62C751356D054A26A821E680E5FA6305
# Wed, 22 Apr 2026 03:15:05 GMT
ENV PYTHON_VERSION=3.13.13
# Wed, 22 Apr 2026 03:15:05 GMT
ENV PYTHON_SHA256=2ab91ff401783ccca64f75d10c882e957bdfd60e2bf5a72f8421793729b78a71
# Wed, 22 Apr 2026 03:34:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		dpkg-dev 		gcc 		gnupg 		libbluetooth-dev 		libbz2-dev 		libc6-dev 		libdb-dev 		libffi-dev 		libgdbm-dev 		liblzma-dev 		libncursesw5-dev 		libreadline-dev 		libsqlite3-dev 		libssl-dev 		make 		tk-dev 		uuid-dev 		wget 		xz-utils 		zlib1g-dev 	; 		wget -O python.tar.xz "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz"; 	echo "$PYTHON_SHA256 *python.tar.xz" | sha256sum -c -; 	wget -O python.tar.xz.asc "https://www.python.org/ftp/python/${PYTHON_VERSION%%[a-z]*}/Python-$PYTHON_VERSION.tar.xz.asc"; 	GNUPGHOME="$(mktemp -d)"; export GNUPGHOME; 	gpg --batch --keyserver hkps://keys.openpgp.org --recv-keys "$GPG_KEY"; 	gpg --batch --verify python.tar.xz.asc python.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" python.tar.xz.asc; 	mkdir -p /usr/src/python; 	tar --extract --directory /usr/src/python --strip-components=1 --file python.tar.xz; 	rm python.tar.xz; 		cd /usr/src/python; 	gnuArch="$(dpkg-architecture --query DEB_BUILD_GNU_TYPE)"; 	./configure 		--build="$gnuArch" 		--enable-loadable-sqlite-extensions 		--enable-optimizations 		--enable-option-checking=fatal 		--enable-shared 		$(test "${gnuArch%%-*}" != 'riscv64' && echo '--with-lto') 		--with-ensurepip 	; 	nproc="$(nproc)"; 	EXTRA_CFLAGS="$(dpkg-buildflags --get CFLAGS)"; 	LDFLAGS="$(dpkg-buildflags --get LDFLAGS)"; 	LDFLAGS="${LDFLAGS:-} -Wl,--strip-all"; 	arch="$(dpkg --print-architecture)"; arch="${arch##*-}"; 	case "$arch" in 		amd64|arm64) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer -mno-omit-leaf-frame-pointer"; 			;; 		i386) 			;; 		*) 			EXTRA_CFLAGS="${EXTRA_CFLAGS:-} -fno-omit-frame-pointer"; 			;; 	esac; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-}" 	; 	rm python; 	make -j "$nproc" 		"EXTRA_CFLAGS=${EXTRA_CFLAGS:-}" 		"LDFLAGS=${LDFLAGS:-} -Wl,-rpath='\$\$ORIGIN/../lib'" 		python 	; 	make install; 		cd /; 	rm -rf /usr/src/python; 		find /usr/local -depth 		\( 			\( -type d -a \( -name test -o -name tests -o -name idle_test \) \) 			-o \( -type f -a \( -name '*.pyc' -o -name '*.pyo' -o -name 'libpython*.a' \) \) 		\) -exec rm -rf '{}' + 	; 		ldconfig; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -not \( -name '*tkinter*' \) -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -rt dpkg-query --search 		| awk 'sub(":$", "", $1) { print $1 }' 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 	apt-get dist-clean; 		export PYTHONDONTWRITEBYTECODE=1; 	python3 --version; 	pip3 --version # buildkit
# Wed, 22 Apr 2026 03:34:21 GMT
RUN set -eux; 	for src in idle3 pip3 pydoc3 python3 python3-config; do 		dst="$(echo "$src" | tr -d 3)"; 		[ -s "/usr/local/bin/$src" ]; 		[ ! -e "/usr/local/bin/$dst" ]; 		ln -svT "$src" "/usr/local/bin/$dst"; 	done # buildkit
# Wed, 22 Apr 2026 03:34:21 GMT
CMD ["python3"]
# Wed, 22 Apr 2026 04:59:42 GMT
ENV HY_VERSION=1.2.0
# Wed, 22 Apr 2026 04:59:42 GMT
ENV HYRULE_VERSION=1.0.1
# Wed, 22 Apr 2026 04:59:42 GMT
RUN pip install --no-cache-dir "hy == $HY_VERSION" "hyrule == $HYRULE_VERSION" # buildkit
# Wed, 22 Apr 2026 04:59:42 GMT
CMD ["hy"]
```

-	Layers:
	-	`sha256:71574deb335f1e823f938f4a215de00a90d63866898f1f354a0b15e8b9c30577`  
		Last Modified: Wed, 22 Apr 2026 00:17:08 GMT  
		Size: 29.8 MB (29840300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5d6bc7e62628f7335a45c95f070ee5a190c7df1b596fb688f203a3b7338b5ef1`  
		Last Modified: Wed, 22 Apr 2026 03:23:55 GMT  
		Size: 1.3 MB (1305522 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3ce2238c3e11acf84d736e3def78d554c7cae7dd7fc224d8c472146c364caa2`  
		Last Modified: Wed, 22 Apr 2026 03:34:34 GMT  
		Size: 11.9 MB (11872185 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04ca72a746bba5af8e7a222be8e0d8eb5a7022a4eb8fc498475684bb582a847f`  
		Last Modified: Wed, 22 Apr 2026 03:34:34 GMT  
		Size: 249.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:633e23a0dc4890e8a5031c71f951ee8789c71430f93b08449116453a26d7ec05`  
		Last Modified: Wed, 22 Apr 2026 04:59:54 GMT  
		Size: 5.3 MB (5341702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `hylang:python3.13` - unknown; unknown

```console
$ docker pull hylang@sha256:9e6344b9d888cc4119c34bf9ceab79599ef661e386fcdc78efd074ccd49fb9ac
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 MB (2165005 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:937165e11b7771b63cb2c469d9d763ea76a47a374d33784d7b1cb6fb35dae461`

```dockerfile
```

-	Layers:
	-	`sha256:a25d48f9c1fbbbc59e7c5f35d5aa1320497e8f8f3bf6e2a2a030ee20c3a8c0a0`  
		Last Modified: Wed, 22 Apr 2026 04:59:54 GMT  
		Size: 2.2 MB (2155700 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cc94e6b6360344936feee73e49f9a2e0602fa185925e6cc77910fed6f7adb839`  
		Last Modified: Wed, 22 Apr 2026 04:59:54 GMT  
		Size: 9.3 KB (9305 bytes)  
		MIME: application/vnd.in-toto+json

### `hylang:python3.13` - windows version 10.0.26100.32690; amd64

```console
$ docker pull hylang@sha256:4c8f1fcb7ebf49fd307a9e1eff90b5cd1d96deae2e334912c860db793789dab2
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.2 GB (2197576070 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2aba466b369074fecf405a552718dcfdf47a54b37a3e0707fd5a60ef45b7fc77`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Sun, 11 Jan 2026 09:57:36 GMT
RUN Apply image 10.0.26100.32230
# Mon, 13 Apr 2026 07:00:46 GMT
RUN Install update 10.0.26100.32690
# Tue, 14 Apr 2026 21:02:09 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:16:15 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 14 Apr 2026 21:16:16 GMT
ENV PYTHON_VERSION=3.13.13
# Tue, 14 Apr 2026 21:16:17 GMT
ENV PYTHON_SHA256=3c9c81d80f91c002ced86d645422d81432c68c7d9b6b0e974768ca2e449a4d00
# Tue, 14 Apr 2026 21:17:00 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:17:00 GMT
CMD ["python"]
# Tue, 14 Apr 2026 22:15:07 GMT
ENV HY_VERSION=1.2.0
# Tue, 14 Apr 2026 22:15:07 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 14 Apr 2026 22:15:46 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 14 Apr 2026 22:15:47 GMT
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
	-	`sha256:8132c872e75f25bfa323300a3940e534262afa9775f557483dcc1c0951ee5277`  
		Last Modified: Tue, 14 Apr 2026 21:03:51 GMT  
		Size: 1.3 KB (1347 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd96d123a94c2e96da10a3bd0747ea0e160e9b2cdee1d607f8ba49e13b2ecbb`  
		Last Modified: Tue, 14 Apr 2026 21:17:05 GMT  
		Size: 1.3 KB (1336 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:513fed98c0242987a59790f45dda4da448e18cb5d3c98d5823a13cbf2655dc41`  
		Last Modified: Tue, 14 Apr 2026 21:17:05 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c9427b7e7928132139b82ace25661d40c8c9afddfaf727cf775643ea1dfb18`  
		Last Modified: Tue, 14 Apr 2026 21:17:05 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5908d8849ea04d9ba6848b83d07f812c6ab937025c5dfb0c7bf0d3e95762866`  
		Last Modified: Tue, 14 Apr 2026 21:17:10 GMT  
		Size: 59.2 MB (59156829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad9b333ef449d79783bcad63d085d9dd3945ecd7a10e47e83fe44d51519b9ade`  
		Last Modified: Tue, 14 Apr 2026 21:17:05 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75fecf7321eb98482440a5648fcd287b9fc3bf69e6c41d53722f081a9cac04ee`  
		Last Modified: Tue, 14 Apr 2026 22:15:51 GMT  
		Size: 1.3 KB (1313 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58bb81ba25c846028fc1d2292b9715efc6f059c8e14f349086feba3a49e116be`  
		Last Modified: Tue, 14 Apr 2026 22:15:51 GMT  
		Size: 1.3 KB (1321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe2462bf0fa7b8b1bce4e8b4405459693fcced2aa6717d4e554a80acedb034e3`  
		Last Modified: Tue, 14 Apr 2026 22:15:52 GMT  
		Size: 8.4 MB (8422724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a99695e0f3f5255cf838a6e06bb5dc9442e16f225e9ce5b91b54ad11e35a1109`  
		Last Modified: Tue, 14 Apr 2026 22:15:51 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `hylang:python3.13` - windows version 10.0.20348.5020; amd64

```console
$ docker pull hylang@sha256:efbd43ce3f47f7bf3f60fb84786b589f667691c712d7307aafd70e177bd490ca
```

-	Docker Version: 23.0.6
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **2.1 GB (2137466311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92f9a4e6c25c3d6f9c38485c6c801c40ad28d3edb45b0c1203bb5455b7e45d3f`
-	Default Command: `["hy"]`
-	`SHELL`: `["powershell","-Command","$ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';"]`

```dockerfile
# Thu, 09 Oct 2025 07:51:18 GMT
RUN Apply image 10.0.20348.4294
# Mon, 13 Apr 2026 03:24:09 GMT
RUN Install update 10.0.20348.5020
# Tue, 14 Apr 2026 21:03:26 GMT
SHELL [powershell -Command $ErrorActionPreference = 'Stop'; $ProgressPreference = 'SilentlyContinue';]
# Tue, 14 Apr 2026 21:26:56 GMT
ENV PYTHONIOENCODING=UTF-8
# Tue, 14 Apr 2026 21:26:56 GMT
ENV PYTHON_VERSION=3.13.13
# Tue, 14 Apr 2026 21:26:57 GMT
ENV PYTHON_SHA256=3c9c81d80f91c002ced86d645422d81432c68c7d9b6b0e974768ca2e449a4d00
# Tue, 14 Apr 2026 21:27:58 GMT
RUN $url = ('https://www.python.org/ftp/python/{0}/python-{1}-amd64.exe' -f ($env:PYTHON_VERSION -replace '[a-z]+[0-9]*$', ''), $env:PYTHON_VERSION); 	Write-Host ('Downloading {0} ...' -f $url); 	[Net.ServicePointManager]::SecurityProtocol = [Net.SecurityProtocolType]::Tls12; 	Invoke-WebRequest -Uri $url -OutFile 'python.exe'; 		Write-Host ('Verifying sha256 ({0}) ...' -f $env:PYTHON_SHA256); 	if ((Get-FileHash python.exe -Algorithm sha256).Hash -ne $env:PYTHON_SHA256) { 		Write-Host 'FAILED!'; 		exit 1; 	}; 		Write-Host 'Installing ...'; 	$exitCode = (Start-Process python.exe -Wait -NoNewWindow -PassThru 		-ArgumentList @( 			'/quiet', 			'InstallAllUsers=1', 			'TargetDir=C:\Python', 			'PrependPath=1', 			'Shortcuts=0', 			'Include_doc=0', 			'Include_pip=1', 			'Include_test=0' 		) 	).ExitCode; 	if ($exitCode -ne 0) { 		Write-Host ('Running python installer failed with exit code: {0}' -f $exitCode); 		Get-ChildItem $env:TEMP | Sort-Object -Descending -Property LastWriteTime | Select-Object -First 1 | Get-Content; 		exit $exitCode; 	} 		$env:PATH = [Environment]::GetEnvironmentVariable('PATH', [EnvironmentVariableTarget]::Machine); 		Write-Host 'Verifying install ...'; 	Write-Host '  python --version'; python --version; 		Write-Host 'Removing ...'; 	Remove-Item python.exe -Force; 	Remove-Item $env:TEMP/Python*.log -Force; 		$env:PYTHONDONTWRITEBYTECODE = '1'; 		Write-Host 'Verifying pip install ...'; 	pip --version; 		Write-Host 'Complete.'
# Tue, 14 Apr 2026 21:27:59 GMT
CMD ["python"]
# Tue, 14 Apr 2026 22:17:42 GMT
ENV HY_VERSION=1.2.0
# Tue, 14 Apr 2026 22:17:43 GMT
ENV HYRULE_VERSION=1.0.1
# Tue, 14 Apr 2026 22:18:11 GMT
RUN pip install --no-cache-dir ('hy == {0}' -f $env:HY_VERSION) ('hyrule == {0}' -f $env:HYRULE_VERSION)
# Tue, 14 Apr 2026 22:18:12 GMT
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
	-	`sha256:7859559f7e482ab69f3dddf83b05a23fb97e6c47cc09bb11f9f91ea0b96dbf26`  
		Last Modified: Tue, 14 Apr 2026 21:05:58 GMT  
		Size: 1.3 KB (1339 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89437b07bc34e480f349a26343836e3ed5139e1b10f8972f2d3ddec312d2d611`  
		Last Modified: Tue, 14 Apr 2026 21:28:06 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae1bd2253f26c1508194e0bf77f67b13da7b081cd79cdb41daaddbfc46ed5de4`  
		Last Modified: Tue, 14 Apr 2026 21:28:06 GMT  
		Size: 1.3 KB (1316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4485c9fd3753ce85b6f7c329af21719b49ba3ad7b1bb3e2ccd5ac879f55daca5`  
		Last Modified: Tue, 14 Apr 2026 21:28:06 GMT  
		Size: 1.3 KB (1315 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9d5ac3e78b81afb6d0b156609c966bde6fc28256ea05418a9e541891b4b5067`  
		Last Modified: Tue, 14 Apr 2026 21:28:14 GMT  
		Size: 59.0 MB (58997850 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d29c621a69ff97f7f9f0fe2c1151b86524f70582f734ef006f13879ca2f6cdd2`  
		Last Modified: Tue, 14 Apr 2026 21:28:06 GMT  
		Size: 1.3 KB (1320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb51a32a879ec4b89428b3fbd071746eb200ddcdb9132b96f4bed496f6b87924`  
		Last Modified: Tue, 14 Apr 2026 22:18:16 GMT  
		Size: 1.3 KB (1319 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484215f9090e90733b649596cb5ad44b482360eb62d76e6a90ce4c5c8e17e994`  
		Last Modified: Tue, 14 Apr 2026 22:18:16 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03272de8b736b3305f8bca26a23a99b3bb53a9b99ab2cbe3219fe243b4efb3c1`  
		Last Modified: Tue, 14 Apr 2026 22:18:17 GMT  
		Size: 8.2 MB (8246708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df353006c2305f69b550866c37ddb4e3e7dab0151b65269d295dbde638f6246a`  
		Last Modified: Tue, 14 Apr 2026 22:18:16 GMT  
		Size: 1.3 KB (1322 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
