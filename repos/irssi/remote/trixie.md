## `irssi:trixie`

```console
$ docker pull irssi@sha256:3eef8420102722e83c01436cf5ecde77095a937ad0a9d1535480b7a426567219
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

### `irssi:trixie` - linux; amd64

```console
$ docker pull irssi@sha256:f62560d766eab4534167883aef43fa8fad47d829ff5c18467b86628e024bd9c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53870137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:769552443b8c0b77660078238cebe5d212969cc1cef60189b3e988284170f129`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1760918400'
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV HOME=/home/user
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 11 Aug 2025 16:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
WORKDIR /home/user
# Mon, 11 Aug 2025 16:45:42 GMT
USER user
# Mon, 11 Aug 2025 16:45:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:38513bd7256313495cdd83b3b0915a633cfa475dc2a07072ab2c8d191020ca5d`  
		Last Modified: Tue, 21 Oct 2025 00:20:31 GMT  
		Size: 29.8 MB (29777924 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a50e33926f10233e1cefedd2afc470ffdca1d03aae27f61804a5308859157ecd`  
		Last Modified: Tue, 21 Oct 2025 01:18:57 GMT  
		Size: 19.2 MB (19222452 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5172862d08ce0c808ae6bd8643e68f924682e5145be1e8111d0b52f49a6fe9bc`  
		Last Modified: Tue, 21 Oct 2025 01:18:55 GMT  
		Size: 3.3 KB (3335 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:160b0c22ddb061ea4cd17f1ed3ca11aec9c1535fa615b47a6577d131dafc4ba3`  
		Last Modified: Tue, 21 Oct 2025 01:18:56 GMT  
		Size: 4.9 MB (4866394 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:6eff9cda53aa1fce62b753cb7e75d79fbe1450f9fec0a77f0972a0a5c20df8d1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b4a3535c6261e33feac4e249dfb231f9d22a1d643b2b4a9b3d8f0a1ed8ff4dc`

```dockerfile
```

-	Layers:
	-	`sha256:984b3275ff964e7bbd701d8b5ca39a1b1abcd3f1bcf095ff7fea54585adab0a5`  
		Last Modified: Tue, 21 Oct 2025 10:59:26 GMT  
		Size: 5.6 MB (5588383 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:80576291496298d1465daebae79c9c7e21c694e8d2ab8ac5425ebf50e8de2192`  
		Last Modified: Tue, 21 Oct 2025 10:59:27 GMT  
		Size: 18.7 KB (18694 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:743f62dfb2723e5cf5b5580c13d984036e291c139dd9c147398041e13730f947
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944523 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:53264b9ae4718eaff15b08e6425684905e4eae0a430cef05af4fb500573637a5`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1760918400'
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV HOME=/home/user
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 11 Aug 2025 16:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
WORKDIR /home/user
# Mon, 11 Aug 2025 16:45:42 GMT
USER user
# Mon, 11 Aug 2025 16:45:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:389bac9f76fa529ccf801fd7c9cb260ecee27d208221c25004185ab22936c4d4`  
		Last Modified: Tue, 21 Oct 2025 00:20:45 GMT  
		Size: 27.9 MB (27946283 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3de732671811b90f398574980cdba725342aec2c44810dfbcd93340293498e25`  
		Last Modified: Tue, 21 Oct 2025 01:21:17 GMT  
		Size: 18.3 MB (18285300 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:78d491c0d806d5e00e2193d78068bd4f31c2988d932462603214e16dad90c4b0`  
		Last Modified: Tue, 21 Oct 2025 01:21:15 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f889921e2f952643433506973574b01f5cc90b4da8b4cd9d425392c111e54114`  
		Last Modified: Tue, 21 Oct 2025 01:21:15 GMT  
		Size: 4.7 MB (4709577 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:8d973519fe67af22b7280baf2dc807332873bdce1095226f3ac088e4249d4f98
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604764 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:57ca4080c3ddefe0ca125f76e0169a4c17c246bbbd05d7d5976dabfa85cee88b`

```dockerfile
```

-	Layers:
	-	`sha256:0e9998afc3dd0267cbf210040e460e02dd7e031b792d538f21fec1d525fb94ff`  
		Last Modified: Tue, 21 Oct 2025 07:59:25 GMT  
		Size: 5.6 MB (5585932 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c392b33eb145e5fe5e62eac2373db4ccaeedec88f8d638b2acf7838883903cff`  
		Last Modified: Tue, 21 Oct 2025 07:59:25 GMT  
		Size: 18.8 KB (18832 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:ec7216e01ceba6748f58241dd44ef50c704fd9d0cbf6131634fd49a15f702256
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48683586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:deb33d7b4c257421d912466ff540a8eab48db1957b1513f08e045342c3e09f7e`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1760918400'
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV HOME=/home/user
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 11 Aug 2025 16:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
WORKDIR /home/user
# Mon, 11 Aug 2025 16:45:42 GMT
USER user
# Mon, 11 Aug 2025 16:45:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f157a4589edc88a89367c83c97b73205a4a80cffc6af7a71b789000a1bc8763e`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 26.2 MB (26212894 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec21711d4a258965a72caed76918b337c0aa5de6b91e590c06fc5e4745646f55`  
		Last Modified: Tue, 21 Oct 2025 01:21:40 GMT  
		Size: 17.9 MB (17908849 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b844f9ec9159fe5dc1bceb0c829cf8fed6b324e19975cd9a3e797da3b9e7f32`  
		Last Modified: Tue, 21 Oct 2025 01:21:39 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e8319989dae0a45f302eefb7eacf795675adb09faf457ef920f5f154d9e8fd6a`  
		Last Modified: Tue, 21 Oct 2025 01:21:40 GMT  
		Size: 4.6 MB (4558483 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:1caf5b32a9cc375fdb8989c5e37fd5701d48a4ee13f33a1efb1c643b6656b614
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1644fbc65e3d69b2d3bdd0d9e16c452b7d1c7156e981d44b810e54fb21f72726`

```dockerfile
```

-	Layers:
	-	`sha256:ef4ef36a4fd0ce15ccfe9d8c5c18fc16fafd0038ee0a805f0e2fbd3884993613`  
		Last Modified: Tue, 21 Oct 2025 07:59:30 GMT  
		Size: 5.6 MB (5588954 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a879647ba458c48533bd9bc58dc4e49735e56b2b2509ed8842988ba5b86312e0`  
		Last Modified: Tue, 21 Oct 2025 07:59:31 GMT  
		Size: 18.8 KB (18832 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:77dfd1a59d7b77b123cca1beadf2971d1ba2ab34fdeeefeadce1a24e0f13126c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53976450 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03efcec3d095c3aea650cc38e8beac272725967f1d9705561a88cc2cfabd06c7`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1760918400'
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV HOME=/home/user
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 11 Aug 2025 16:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
WORKDIR /home/user
# Mon, 11 Aug 2025 16:45:42 GMT
USER user
# Mon, 11 Aug 2025 16:45:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a16e551192670581ec8359c70ab9eebf8f2af5468ffc79b3d4f9ce21b0366f47`  
		Last Modified: Tue, 21 Oct 2025 00:23:17 GMT  
		Size: 30.1 MB (30142127 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:38b408dc86163fc3064303c3d87a6f050d94d7e50026af6fec8d474bde261f9b`  
		Last Modified: Tue, 21 Oct 2025 01:19:20 GMT  
		Size: 19.0 MB (19049325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec261c2c31268433efbe285382be2e8e472bc1069f6f4703a8c3225b10ce0192`  
		Last Modified: Tue, 21 Oct 2025 01:19:18 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1acd4e881dacb1490ed68208dd4440fca46f3dc100f2a812bf12c1f676495e5`  
		Last Modified: Tue, 21 Oct 2025 01:19:19 GMT  
		Size: 4.8 MB (4781638 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:2835026ba33a88cc6dd9fad1db6db1ec4ac24c190ed8d34348d3c797171fcabb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613743 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6636c1128d2fa3dcbaaa075ffd279fcdb2e092e8cd8f4acd4b4056e29c38c764`

```dockerfile
```

-	Layers:
	-	`sha256:71b8d4b308985e51f1304ef1f8d2a4365932f656bec2d21685a2b0333d5e3ccb`  
		Last Modified: Tue, 21 Oct 2025 07:59:54 GMT  
		Size: 5.6 MB (5594867 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:cda273518a593b1fdc06763d67c1ec3babffc7218cf0dfde047a1d3545ed65a0`  
		Last Modified: Tue, 21 Oct 2025 07:59:55 GMT  
		Size: 18.9 KB (18876 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; 386

```console
$ docker pull irssi@sha256:906a0c6f51c0b1f3b4ecb3f2e1c968d3704a25c07977646ef27d94b4b52f843b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54906871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0f15a626e6515729d1e92c4029f7fd5ad811e6b1fa57491b31c1375bfd151edd`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1760918400'
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV HOME=/home/user
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 11 Aug 2025 16:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
WORKDIR /home/user
# Mon, 11 Aug 2025 16:45:42 GMT
USER user
# Mon, 11 Aug 2025 16:45:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c39cee8c4780ac17d9c2caff77324495220e917ba3f61826c72fe134724c1e4a`  
		Last Modified: Tue, 21 Oct 2025 00:20:54 GMT  
		Size: 31.3 MB (31294628 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a10221caffdcbfa0e53f49b1c8340c488768b10a5ea331304fe42934a151e92`  
		Last Modified: Tue, 21 Oct 2025 01:19:19 GMT  
		Size: 18.7 MB (18740674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d99453861535e7430a13e074b1001d31ea1b6113f5f26cbd98c4898b8f5248b1`  
		Last Modified: Tue, 21 Oct 2025 01:19:17 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2532aeb1762cf3e40be739eca77e4a75e1fe38161883765d09f93de9e8e2da0e`  
		Last Modified: Tue, 21 Oct 2025 01:19:17 GMT  
		Size: 4.9 MB (4868206 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:7da87f53975d8a9812601bfebe2d8b85bb1ddace02345349599eb31d26603b89
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603144 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38b166c953777c8cc44a6f84ea8cf0efae3b040be490d0e4cf0af5fc12b2fffe`

```dockerfile
```

-	Layers:
	-	`sha256:0d1c17737f2969710a690596ea60539faa8669ce29c2cdb5aea0ab822518a718`  
		Last Modified: Tue, 21 Oct 2025 10:59:42 GMT  
		Size: 5.6 MB (5584506 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:4cf1c8a6fed6cbd711442dee178708058badce283771d0b8d81faae2d7964c89`  
		Last Modified: Tue, 21 Oct 2025 10:59:43 GMT  
		Size: 18.6 KB (18638 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:4c3af27a12790c0cfa48c4f1d2019faa9d05c1220cd122ff5fb2bed6d23a583b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58240798 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44f030cef13fb3fda7086c6e51cea0efa5002adc6edbc1ef26e4e33215033c6`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1760918400'
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV HOME=/home/user
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 11 Aug 2025 16:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
WORKDIR /home/user
# Mon, 11 Aug 2025 16:45:42 GMT
USER user
# Mon, 11 Aug 2025 16:45:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a9b4dd19a96be85b367998327f4288ed2fa8f174d1b3e8bea8ac7c2c626ec865`  
		Last Modified: Tue, 21 Oct 2025 00:26:55 GMT  
		Size: 33.6 MB (33598518 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5e841ebc0539e7a4e368171ccc16ecb7ba162ac576a7ed27ec223e471bbe621e`  
		Last Modified: Tue, 21 Oct 2025 01:41:45 GMT  
		Size: 19.5 MB (19541826 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4d17036e1b961a7ed458bbe72784ed34010cf138364b4c74dd743ea2e99b8cb6`  
		Last Modified: Tue, 21 Oct 2025 01:41:44 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b877628b4fb7aa6e57300b7541321fd3b45f3ff13703e89c233bbab0335ff50e`  
		Last Modified: Tue, 21 Oct 2025 01:41:44 GMT  
		Size: 5.1 MB (5097094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:15dc3a6b9763ac4a7b8d768b40696f82670076aec2641a34982e3d302d8ed13f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614180 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d708390baaced630af008a8475443ec42ad8a76aa30ce617721f6895b793448`

```dockerfile
```

-	Layers:
	-	`sha256:9e9376eef7e487f645137dcc729905458a2e1622750918c2f587ec46859726ef`  
		Last Modified: Tue, 21 Oct 2025 04:59:53 GMT  
		Size: 5.6 MB (5595414 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:1cdadf52d6279f778515c7f5c74ded387e79c8ca8708b5770fb75623f3dbf19a`  
		Last Modified: Tue, 21 Oct 2025 04:59:54 GMT  
		Size: 18.8 KB (18766 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:b82298c317e6a439c3f099afd72b7fa6b5201568a6d3153b7497dc49dc6507b9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51688089 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:403e3b6a66a85cb085f199cffa308e5023bf3fe729824e41c002416b247d956d`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1760918400'
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV HOME=/home/user
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 11 Aug 2025 16:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
WORKDIR /home/user
# Mon, 11 Aug 2025 16:45:42 GMT
USER user
# Mon, 11 Aug 2025 16:45:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6d1567708d42906165204f9177d357cb6a2fd51f758da447f1743b00813f892f`  
		Last Modified: Tue, 21 Oct 2025 00:37:37 GMT  
		Size: 28.3 MB (28275650 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4b7f3891906df4cd2403737375e54dde2c73b881597839e92a5b6dd344424615`  
		Last Modified: Tue, 21 Oct 2025 03:29:47 GMT  
		Size: 18.5 MB (18548564 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8a8029bd371998b89c8a8d64828d38f7eb4bb4399482ac3dc5e71efd730657d2`  
		Last Modified: Tue, 21 Oct 2025 03:29:46 GMT  
		Size: 3.3 KB (3334 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8ee3c3fcfa1af49e05f1182ce4c1afa2a0194bd74879ad097cffa2ac8103f4b`  
		Last Modified: Tue, 21 Oct 2025 03:29:47 GMT  
		Size: 4.9 MB (4860509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:d1526a7a0acb4e17c7d0de75a8520b71f48bdb12e866edd8ba1cbd14837d69a5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598452 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03e18a04baf8b90318746b631be324866c2a5ad0e97c19ef045a02f165a76e2b`

```dockerfile
```

-	Layers:
	-	`sha256:37562df56ffc930fadaeedc49a3a26963856b734a535427bba784d283715a3a1`  
		Last Modified: Tue, 21 Oct 2025 04:59:59 GMT  
		Size: 5.6 MB (5579686 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9272ab45c64a4e06e1fbd5d599a72a87516cee4a10db99acc8447cb1d60aeb51`  
		Last Modified: Tue, 21 Oct 2025 04:59:59 GMT  
		Size: 18.8 KB (18766 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:trixie` - linux; s390x

```console
$ docker pull irssi@sha256:6ad2a6133d7a3f7dc5ff92c0aa1deb7d7b165ac204dc0f26e5584c76abc2c3f5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54506670 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64e14d35f2f384bf17f65321f9e1840602b079eb7494376e6648990576df8456`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1760918400'
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV HOME=/home/user
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 11 Aug 2025 16:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 11 Aug 2025 16:45:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 11 Aug 2025 16:45:42 GMT
WORKDIR /home/user
# Mon, 11 Aug 2025 16:45:42 GMT
USER user
# Mon, 11 Aug 2025 16:45:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:71dc03f1fd788f9fc2bbb931d3df17cbfaf0b486bdfb19f4e3b8792a206689a1`  
		Last Modified: Tue, 21 Oct 2025 00:28:26 GMT  
		Size: 29.8 MB (29837255 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:19f88a88d131abc80f528ad72f4aebe45615151d669b662b12d6a467768c8eeb`  
		Last Modified: Tue, 21 Oct 2025 01:40:22 GMT  
		Size: 19.8 MB (19759936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e050dd837c6b952cdb383cc1fc92c916f81f7cc145631c34cc1548f4cb142919`  
		Last Modified: Tue, 21 Oct 2025 01:40:18 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6fc39bd796918472fccc0972b0d27910c908de94de7fb5ac18899a1fae3616b0`  
		Last Modified: Tue, 21 Oct 2025 01:40:20 GMT  
		Size: 4.9 MB (4906120 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 10 Oct 2025 22:54:50 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:113a78b783a042adc94225452492fadf26486df752caf2c87e12da311865a887
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607982 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ff05f3eba2b78ec5528d1fe45d0a88ca223e23f7efe099b37fba59fec487827`

```dockerfile
```

-	Layers:
	-	`sha256:ed1f775e1289c1475d1f711b4de020aaede1b17e3b59c184d46e912de22093bd`  
		Last Modified: Tue, 21 Oct 2025 10:59:56 GMT  
		Size: 5.6 MB (5589288 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c0ee33fd0409cc1f108ffba698d8917ef1521af0335f355c98fd26cfc1830770`  
		Last Modified: Tue, 21 Oct 2025 10:59:57 GMT  
		Size: 18.7 KB (18694 bytes)  
		MIME: application/vnd.in-toto+json
