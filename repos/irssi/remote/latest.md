## `irssi:latest`

```console
$ docker pull irssi@sha256:32865da433913da20c89af97afbd8560b089f4e2948a0514b15a13ca9317b2b5
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
	-	linux; mips64le
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:latest` - linux; amd64

```console
$ docker pull irssi@sha256:f0e925e08ab5da6d0d6691a6d442f4b8e8cdb1ff735a06d1aef55f059af4d44c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51990258 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf35f7b67228a5ad73cdc26d15a4c213ae4cbd6e618b3a0967f359da89e5778d`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:b24689567a7c604de93e4ef1dc87c372514f692556744da43925c575b4f80df6 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f11c1adaa26e078479ccdd45312ea3b88476441b91be0ec898a7e07bfd05badc`  
		Last Modified: Tue, 02 Jul 2024 01:28:49 GMT  
		Size: 29.1 MB (29126278 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4bdf2047a469d806be70210ac4acc095ec529bb936d6b97f9bd9a38b0424aa6e`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 18.3 MB (18267754 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2b6271d2094a9766727773ccbf0d91deb4d2855345d8d86955c7dda1d02e168`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b686344d1cdcc27faa26d348a6fea64c0e6896854a8e810e061b11257fa60388`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 4.6 MB (4592869 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:f7b337379e2e992ec179978eb24bbe6eaa00c13882272df4c0f78a160ed7d4b5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5355354 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8718877338684ebbabdff0ea8eb65ce94251ed9318e37f034f7360a69f1eca78`

```dockerfile
```

-	Layers:
	-	`sha256:9414cfd75a4291492b80a0885becbdaa903a312f4c5e785638ba344b494ad113`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 5.3 MB (5336838 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5aeb684ff498eeef7adbd01f7a7061a1c6fcc8a4ee5cec94fbadbd2c0f00f6f5`  
		Last Modified: Tue, 02 Jul 2024 03:03:55 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:123e2dd04518de990f5bde84d6e7f33f845008b51fbe7be2aef7c499da2228dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.4 MB (48375090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7488a2df1b9c04e6418fbf1c6dac202b40373b047e85569760966d7cdef6f7ff`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:acd64fd8017b050fbd1031cf3a9abb59fd15c600649b9467c16029cc6bfd11d5 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:a8f08669f346f00b060b912e835bd6c163fca9818f070c730d6ffcc249497315`  
		Last Modified: Tue, 02 Jul 2024 00:51:30 GMT  
		Size: 26.9 MB (26887286 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9ec18306fc60314a9a2166ccbaca936ca2dccf5ca30f8c9db809264fca1ea4c4`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 17.0 MB (17039888 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8cf73419b7e8b9c7e77061b596ce031d5668d17fc61a70fc42aa256d77eabc65`  
		Last Modified: Tue, 02 Jul 2024 12:16:15 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cd6a363daccb316033ea4320d7d8f4223d1f7be59c1c82ea5a0cc7694dcb6bde`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 4.4 MB (4444560 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:c3309a9cf085e1de032e1ea1c3c2dbe7f949a1abf66259b0874305d2e9574626
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5356837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1f014f57180666232dc5a501ddf6c9dc5c60675b84802d991fb3ab6158db4d5`

```dockerfile
```

-	Layers:
	-	`sha256:ed4f6760e5adfa1dcabfbc8ff998a1a5c74998699267836ed6e6bcb1e09ac621`  
		Last Modified: Tue, 02 Jul 2024 12:16:16 GMT  
		Size: 5.3 MB (5338194 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:14467139da358956c5aa6c5b459d8752f332b0e5d9928c071c82977723630c59`  
		Last Modified: Tue, 02 Jul 2024 12:16:15 GMT  
		Size: 18.6 KB (18643 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:eb05735cc27b176fe900f04880bdbab52576e21031ba4b73933c603916bf2b3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45488734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f380c34478aa84c98280c47cea02579b6d3f9ac07d6c92c2714d22924287f4db`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:4c737c0a5e5b59fcbe2bc42dca815263159a1e1d16789ebeee086933aac4649a in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:12af5edb53b85c10582c3e3d437561cc626437f48928a30456a99941d87706e3`  
		Last Modified: Thu, 13 Jun 2024 01:01:38 GMT  
		Size: 24.7 MB (24740215 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:07a5d832dbe595bc1e2a75e36b60b0fd48c9ec396ff96396353a03da987fbaaf`  
		Last Modified: Thu, 13 Jun 2024 19:49:06 GMT  
		Size: 16.4 MB (16446067 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6996b6709de6e01597eaf745a5f33f45aa0f9a7700c4505aaa0717ccb994d24b`  
		Last Modified: Thu, 13 Jun 2024 19:49:05 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3a3019584a88ebe40b175669dee1c12fad5eb50879fb175079f1572c123eb333`  
		Last Modified: Thu, 13 Jun 2024 19:49:06 GMT  
		Size: 4.3 MB (4299094 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:811d45ddf836aa57ede7931f0d4bff2ac9cd788a478ad4d80d9504646a193669
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18425 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9088cf348955490adc570162ef2b66a1561e512a44c835753fbbdfb708ae4ac2`

```dockerfile
```

-	Layers:
	-	`sha256:bc29a7d2f657a96ec7adbf9cf757a90e31a17e6c4a22b92cfb8ff0e5b1784f2a`  
		Last Modified: Thu, 13 Jun 2024 19:49:05 GMT  
		Size: 18.4 KB (18425 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:92f3934599c3b62d79f344daac402ac11533567c6f999ca4dcc0bbcc38cbe2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51538299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b95e81ec63c0d234be1e626c2782053ca23509d250cc92049dd67c3ae8bc9c58`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:5f17f77072bcd27aa8c4d09ef5117423b789c42445b6e6c13af711dfb2abd544 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:559a764445207341cf1207d83ceb89f1e59e2b57e860b7a80a6df6447641832b`  
		Last Modified: Thu, 13 Jun 2024 00:43:13 GMT  
		Size: 29.2 MB (29179666 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d5676af87d0acd0d04331053481918ab1a7ee347225711caabf4adcb81fe05`  
		Last Modified: Thu, 13 Jun 2024 19:18:41 GMT  
		Size: 17.8 MB (17842531 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:40140c1bb67c880bc20d037235f8f3dec09d3ca08c09de7234b8bbc111eef391`  
		Last Modified: Thu, 13 Jun 2024 19:18:40 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cadc0f7310666a5eebff79eb1eb82ee1db0328e7dfb223a184c9dbbe7f6b2d45`  
		Last Modified: Thu, 13 Jun 2024 19:18:41 GMT  
		Size: 4.5 MB (4512743 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:702d51601ea4c2d8cca8ed95defb4b08831481825a9a29de4113e79a7fa0fb25
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 KB (18653 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3496fd93ce65d70973eb7b9ad824b57746f33b7bc19737295fa9ce45940f8d8a`

```dockerfile
```

-	Layers:
	-	`sha256:add4a5deb8137d5fd1a087cff0d3df34f27d7112df7357428727120719d6c681`  
		Last Modified: Thu, 13 Jun 2024 19:18:40 GMT  
		Size: 18.7 KB (18653 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:1be9cbd2699972e2610562b07162f125898b1dbaecc6b8cced5865e2fa9bcab7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.6 MB (52557222 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff1d000a75c6e288e13f3ccb093fb7e9b79b29b0e80ec81b6d0e6de7bd6b2e8a`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:833af11e99172b5d823c96481bc09ac63041d36ae1212658673bdc5b134499d7 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:b9519b4198cfa047c0958f7cde32a32d32c6ae3486aea1aefc60e08ecf59449b`  
		Last Modified: Tue, 02 Jul 2024 00:42:41 GMT  
		Size: 30.1 MB (30144275 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a4fa4d5e2af9d30a0f8d254b8d77870a13142eda7142c7f8173c57369c23e7a`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 17.8 MB (17803027 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b724112c5748097fe12620d076ff3f50946464a9059e9b207ae2957ba8bcf5a8`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4954b48f847fb871dc04f7c370473574d0554f29ac6ddcb6cc91f2252c3aea0b`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 4.6 MB (4606563 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:ab0387c5504277b4d5ff79ba05b852004bbc86f0a42a3fcdc0633965000dd625
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5351378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d939dc614d7a37c55e7e4b27d8f8483173271ad06461f97f141125ad88a1ce6`

```dockerfile
```

-	Layers:
	-	`sha256:d620b8a81f539b799e0a8caa48f1a10cc06e5858ca82b761cd9a0bd573ac052b`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 5.3 MB (5332916 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ffc88078db59bd861714bd3b37d4257d3123706c9297a80bc75a21436e24ff2c`  
		Last Modified: Tue, 02 Jul 2024 03:04:03 GMT  
		Size: 18.5 KB (18462 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; mips64le

```console
$ docker pull irssi@sha256:fc4794b88247953161aa19d4cb3a2376d96ed8d30fa1976f3a0c1927d9026003
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.5 MB (50454016 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cab538060a856550cfce4c6b123051f1d72d4f03cf98fc41f9b9999287fd2d39`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:7843ce82552ae9139a9fa1f09b2a1d74f36c493548aa1a5c10b828cb7e02cbe7 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:9c779e4f033b6f7eb9f6b2e62bbf866659c6eedcf2db024108a6e1d4b9cd8742`  
		Last Modified: Thu, 13 Jun 2024 01:21:54 GMT  
		Size: 29.1 MB (29143819 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3d71fdfa695909e06c96ffd3753a7dfaba8157f808a80086c047cad870672433`  
		Last Modified: Fri, 14 Jun 2024 00:11:36 GMT  
		Size: 16.8 MB (16751746 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f30b0813246acb99b3122b11b395b164397530fdbc510d517c725ba7143d2481`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5ef1f01d5ba2df11dff3f158b9af1d5606ae5fb84bfefe0240b3ce1b64ea7d80`  
		Last Modified: Fri, 14 Jun 2024 00:11:35 GMT  
		Size: 4.6 MB (4555089 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:a89d4c9ba3e7478b764956a5701d18d61a9e0b16e27acb822966d3bd1dfd8c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.4 KB (18396 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:775c199952503d263f44345350142a977b4732d683f30dab90dae92f4a2757bf`

```dockerfile
```

-	Layers:
	-	`sha256:ffb05e2d045607795da684dfba5d47908550830bdc7f7298d12dc24f20e4c8d1`  
		Last Modified: Fri, 14 Jun 2024 00:11:34 GMT  
		Size: 18.4 KB (18396 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:c3139f30600bb9d76cf4edd4485840f8e55799be64b1f3f77d1a1c70cc240140
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56722288 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9c563bba3c41bcf166df0a909803586511775e5dba8572b3ae5594210d20467`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:1f056377e490976ef05b1f93f7003e637bc4464b1db7265cfe611b97c8fa8116 in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:6082a6ec8f0d4a9558cf2d3df5a429c7ae3e1cbf78bb5f0f3291dd68df0934d2`  
		Last Modified: Tue, 02 Jul 2024 01:21:57 GMT  
		Size: 33.1 MB (33122277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bd89c779e22bda7b987da370784971663604e823320ac15b0c0ece3ef21f6509`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 18.8 MB (18768021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:767c88248fee9c8c273a74f8063c197bdc7dfe6a994e4422f85c0b1c55747192`  
		Last Modified: Tue, 02 Jul 2024 10:45:25 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7c017d27ae7c791857fb6f81fe4df92287cef55c7f0037c477e6b8d08d868eb1`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 4.8 MB (4828633 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:906f7ff2c62c9ea89113e2661cc423351cde77126ac24086bf562548456a638b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5363114 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:99ee94946d84f365c75a3fdc306930c045e96830b4c0f31f900b52b4d02c05b8`

```dockerfile
```

-	Layers:
	-	`sha256:20755a303526158bb1a90f65ad9813798bd505dc14bdf17b8126fb0630ad7d3e`  
		Last Modified: Tue, 02 Jul 2024 10:45:26 GMT  
		Size: 5.3 MB (5344532 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f31fa107c321979db8e55f3342adba2cd2a85e5489e722b52bfa6dcade713b0`  
		Last Modified: Tue, 02 Jul 2024 10:45:25 GMT  
		Size: 18.6 KB (18582 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:0cfeb3679873f280862e293f19d752877312c05076bb9bdc9268869f91a7994d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50301730 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7a753a8ca4ad44979bb7446d787ce98a11c987054aeb4fb27d0dc4e5547ae4eb`
-	Default Command: `["irssi"]`

```dockerfile
# Fri, 05 Apr 2024 21:50:10 GMT
ADD file:e13e277230efdcc9e4a44bd7a459bf0e65b04440b6bbf292da87f61b4c9ae2fc in / 
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["bash"]
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV HOME=/home/user
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
ENV LANG=C.UTF-8
# Fri, 05 Apr 2024 21:50:10 GMT
ENV IRSSI_VERSION=1.4.5
# Fri, 05 Apr 2024 21:50:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Fri, 05 Apr 2024 21:50:10 GMT
WORKDIR /home/user
# Fri, 05 Apr 2024 21:50:10 GMT
USER user
# Fri, 05 Apr 2024 21:50:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:407bad4d6e39c8adb6cf98fb11c1bd255ae53204b7059378e0c0f6f76fa3c585`  
		Last Modified: Tue, 02 Jul 2024 00:48:33 GMT  
		Size: 27.5 MB (27490090 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f74b04024eb97eca20d4e3a66ab78385eff282fa8d24f1d8944dc5be9f442fdd`  
		Last Modified: Tue, 02 Jul 2024 06:11:01 GMT  
		Size: 18.2 MB (18221651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8d5e8322ca615a2aaf00b8ff8d7f693e0361c4a4cddfea177104edfbc4c0063e`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:181ab8e95d39b2ba1e86a2e59e9f75c175cfd5e944faaed8087c950c8da94f1e`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 4.6 MB (4586632 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:c8ad84703a2262d8ee2ea15210983a5f815fb64ab18dcf01f5cdaa888f011a9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.4 MB (5354655 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e89c866a2992d36db0b7edce7de8d72f25b493ec2c92645fdfc032a5c504e3c3`

```dockerfile
```

-	Layers:
	-	`sha256:50ce79ca968833ecda1e48cd45194314af892f47a38adbfe63b57c4c2f8fcb19`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 5.3 MB (5336139 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ed1b494e1b4d866c9650e2cb81657474222847073b701a88c148769314e2a8e7`  
		Last Modified: Tue, 02 Jul 2024 06:11:00 GMT  
		Size: 18.5 KB (18516 bytes)  
		MIME: application/vnd.in-toto+json
