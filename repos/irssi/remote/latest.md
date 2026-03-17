## `irssi:latest`

```console
$ docker pull irssi@sha256:1e2b88072e70a14e12cbeb266a8584fe3fc1d4ea408fb648464cc15dc06b6375
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

### `irssi:latest` - linux; amd64

```console
$ docker pull irssi@sha256:370465c195d0eb6095f108834b4739dbc5114a13b1538da76a0f6c9351ab72fb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53868443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9026a14b72f91df1d9cc096fa3b36c7663961092996bbea9a4b6e52a37209d43`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:21:17 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:21:17 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:21:17 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:21:17 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:21:17 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:21:57 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:21:57 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:21:57 GMT
USER user
# Mon, 16 Mar 2026 22:21:57 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:ec781dee3f4719c2ca0dd9e73cb1d4ed834ed1a406495eb6e44b6dfaad5d1f8f`  
		Last Modified: Mon, 16 Mar 2026 21:53:19 GMT  
		Size: 29.8 MB (29775500 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a0f82ae590b7de5a98b09b4978b5716c76caed369caececee30fbd4b31b7757e`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 19.2 MB (19222709 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec7f6e6258f6df00d14d758e622cacffec7a8857d6aeda16e3076689c49fdcd1`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80e04fd68fe0175cf1f176d75b117dfc56b2b9f41ddc3cc94b0cc0ba2d07a979`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 4.9 MB (4866874 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:4543ee4df6efb094189788c003d73af7712257670a883449019bf61aa2bd08be
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ee62cab81b18ef741cf2727599cbf6c58af30e05806a6b4734e6a4fe0b48025`

```dockerfile
```

-	Layers:
	-	`sha256:419a1199659298b3f408847cbd42fd1a432db5d31a7a3596aca2b37996f2f9a0`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 5.6 MB (5588511 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:7cfaf35ddb7bb0e6635a0b6a952317bf4df3e7388110e6ac1aad998e036d9a47`  
		Last Modified: Mon, 16 Mar 2026 22:22:07 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:e6dee81be9d9b9fe4a16fadb73b91b063a97e9500bc13a2eb0114755a094fbdd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.0 MB (50950464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fcdf12e1625c423052e5de613474545d2207737f6693afb668df8e87b90de41c`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:07 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:19:07 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:19:07 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:19:07 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:19:07 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:19:55 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:19:55 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:19:55 GMT
USER user
# Mon, 16 Mar 2026 22:19:55 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:eb1defba38d0de4655b895d4763345b3ab078983d3385db43c308a7caca13f2a`  
		Last Modified: Mon, 16 Mar 2026 21:52:26 GMT  
		Size: 27.9 MB (27943649 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1e42f39bb96430487edfd6614d46f74ae2baf45a591488570d79e036c13787d4`  
		Last Modified: Mon, 16 Mar 2026 22:20:06 GMT  
		Size: 18.3 MB (18293761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:255bce58c19debca5b48c43b356e6247ca0eedf383d077ddf4cea1e1cd4bb605`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bb2a4e1a3ca4e2ee85196bb6a49fb29374507445e687b1dc5b4caefef167210a`  
		Last Modified: Mon, 16 Mar 2026 22:20:06 GMT  
		Size: 4.7 MB (4709697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:aa80cb6ce1bd3c70906b4fb68ad52215e587f7b7df791925d9c4be14ef2af351
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604848 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:47f8506b8107fdead6e4250a855c0274e03acd5addfc53a0577cd207782e8dc7`

```dockerfile
```

-	Layers:
	-	`sha256:2a0db0802a261059fd81aca578c300ebacfaba5ca0abe8ad820ece3b488e0000`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 5.6 MB (5586060 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:90630b0251ccd7cabefc580fc4815a1c574f945fb5ba15bf1e0b707cafe5e631`  
		Last Modified: Mon, 16 Mar 2026 22:20:05 GMT  
		Size: 18.8 KB (18788 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:d191036c54d1f77bb37f8c1b281e68c8017eb7bacedf52cf0ec33211379e0a79
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48684247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:105bd2788706cbdfb23a715874799c9f3b52d35da3c03a92431c2edf48c09620`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:20:00 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:20:01 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:20:01 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:20:01 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:20:01 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:20:42 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:20:42 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:20:42 GMT
USER user
# Mon, 16 Mar 2026 22:20:42 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:7d73604d2a042e7beeb809f68c76f5be3576747809bfaa49747f334227d8d250`  
		Last Modified: Mon, 16 Mar 2026 21:53:24 GMT  
		Size: 26.2 MB (26209505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21cad6b02b14c6883831521acb77aaa191fb76b913d4fa9fde2f564aa0cad8ff`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 17.9 MB (17912988 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c352dfeb034880d1249ea30b2fa49689f7b337a288e7eba30cf95e6f5ba17b96`  
		Last Modified: Mon, 16 Mar 2026 22:20:51 GMT  
		Size: 3.3 KB (3323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5556e2e8cc1af62f312f90d989a5e7d51a2615166f8d8ed4a4171efe9ba4f2e0`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 4.6 MB (4558399 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:660745334a5530ae00d3583fe9fad6ca4e2f5520059f895b9dfa479d47694593
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cecba8fb29f1c2ae36950769bee857fcdfa73ab1bcf63ec1dc83c540fa8ff67`

```dockerfile
```

-	Layers:
	-	`sha256:d4df04203ca6306e2d125d020f109cbca6a115c48376314d5fdd6dfb1b8057e7`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 5.6 MB (5589082 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:62920e758bc89bfea24877545c1d23a1f03432d946af10f52b20d6c329f05c19`  
		Last Modified: Mon, 16 Mar 2026 22:20:52 GMT  
		Size: 18.8 KB (18789 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:47fbd3fd9c29579b7e69b1c4313ebb445323d4ed719be468b7c68d14b2abd2e6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53973077 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9d4d7330c359e06aa03a0f9a8907be5ac9f33e4b3bebd3085cfd57595f11d83`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:20:57 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:20:57 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:20:57 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:20:57 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:20:57 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:21:33 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:21:33 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:21:33 GMT
USER user
# Mon, 16 Mar 2026 22:21:33 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f4badedbec24858ef2dc51256f6418328e305e9c3c5a5e093581f83425618bd5`  
		Last Modified: Mon, 16 Mar 2026 21:53:04 GMT  
		Size: 30.1 MB (30138416 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0fb31e50afba1e9f4e5d30a1f69b37200fe6d048e08a9154dc5d428a19311f98`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 19.0 MB (19049827 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5308417c534a9f8d624333157b354360e1e890b26a97d485e140701a6698b1ac`  
		Last Modified: Mon, 16 Mar 2026 22:21:43 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a3d12bce18db22eb687ec2963ecca32b2699ef68d4db59402170e52595d3d537`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 4.8 MB (4781477 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:f8cba54d17ab50b78bdf67028862a20fc722f100089b7152cb095860352e3b75
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613828 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c4a3d8bc1a4bf22b05db46afe559ca895e17c7b6ac0576d65dca765b088b52b8`

```dockerfile
```

-	Layers:
	-	`sha256:255c11193236e4d964a0b5ddb4e3b7ed894f7dcf87fc63939a75996d558211f9`  
		Last Modified: Mon, 16 Mar 2026 22:21:44 GMT  
		Size: 5.6 MB (5594995 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:5e64e453c9471334d393c6f1df01984893fcafb5449950bf211bc09b8e230f60`  
		Last Modified: Mon, 16 Mar 2026 22:21:43 GMT  
		Size: 18.8 KB (18833 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:63680def1d326ae407e1ae02493688a9c4acea3f611981d55814491d8c3c44f0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54905927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0460a4309f5c833d0c770ece3df4c07d37f2c2f7c11124c6b06b113746462df`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:17:36 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:17:36 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:17:36 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:17:36 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:17:36 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:18:21 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:18:21 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:18:21 GMT
USER user
# Mon, 16 Mar 2026 22:18:21 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2c0c3f3238f3d4cecd93e4dee6eda788943ef955de61c3ad4ff659da1f43ba60`  
		Last Modified: Mon, 16 Mar 2026 21:53:39 GMT  
		Size: 31.3 MB (31291132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed823e90612c06e134aff9e0461a04c2cba8549f32b26df297333dcb04604fa5`  
		Last Modified: Mon, 16 Mar 2026 22:18:32 GMT  
		Size: 18.7 MB (18743003 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ec4670464fbc254cf47ea7aaf2cc7d4ffa31190eb9612de0f1d3c8201b6fac36`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 3.3 KB (3321 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:52ecc256f7ada526642547b0872e9a750e6242d389dc15be1e33c7fe8ca4ed5b`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 4.9 MB (4868439 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:5787acbd16de76de532c0e7068fb302dc7b936c77ce17228d944031fcbe7f566
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603229 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7023210dc541dbe0a69f102e25f2268dd3dcaf19e838746c04521f5384a0b3e1`

```dockerfile
```

-	Layers:
	-	`sha256:02f2c76604c2e5ae5bae385b2c78f3185cfb2953551697cff6eb748e27ad97bd`  
		Last Modified: Mon, 16 Mar 2026 22:18:32 GMT  
		Size: 5.6 MB (5584634 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d3db2d63d844d734bbe27c242f94d6d695cc5bfa53883bf15213dc0ebbc37374`  
		Last Modified: Mon, 16 Mar 2026 22:18:31 GMT  
		Size: 18.6 KB (18595 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:fccbc6079cb2cbe7dbd0f5afd147fab0f06914545c827fa785ed8f5242f62e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58232560 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3592d3df435ba91f4ff3c6c8cfab2d87ea3960759e9a15eafb0d41fc3bc7eac`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 23:45:42 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 23:45:42 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 23:45:42 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 23:45:42 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 23:45:42 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 23:47:18 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 23:47:18 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 23:47:18 GMT
USER user
# Mon, 16 Mar 2026 23:47:18 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:f078139432e0b368e27241df524f6ef0ed0148b217d7495670dc297af77699fb`  
		Last Modified: Mon, 16 Mar 2026 21:55:56 GMT  
		Size: 33.6 MB (33592834 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4c12f09b9e4177d94f41c37871cd1b82422133c219b73dc2dbc0e408dbd9d5d5`  
		Last Modified: Mon, 16 Mar 2026 23:47:42 GMT  
		Size: 19.5 MB (19538609 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67cb02d7dcbb114624765424b5426ac3d6dd3b42eb9d47f6f2e8f3cffd9cd8a7`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f9dd8f57d3ac980371e1912275463f4771ddaeda847d673f55d906e3bbf1fa3`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 5.1 MB (5097761 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:3a5eed81680d787d4e6f811b2713043e3a782d0275bbc307f2fef7c7c5698add
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c840181270a82fbcb90febd720ab270605174e51dc00541f1a8a800d3a53952c`

```dockerfile
```

-	Layers:
	-	`sha256:64f1d6d3b35278672cb57bc9e5cd846ed7798d989eda85629837eba4350c4436`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 5.6 MB (5595542 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d1c63475cc46864a67a3dee3d3a4d337b8783abdcdc86d884fac5030b839e4c1`  
		Last Modified: Mon, 16 Mar 2026 23:47:41 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; riscv64

```console
$ docker pull irssi@sha256:2cbadffdcd1d9e6ed0a1a41bdf4458aa7edbfa64db8a6e6bdbfe89bff4e1cd74
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51694478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c7da0eaef880d7ee87d04875d9a091d11c77728a27a7b74c6759480a2e0b19fc`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1773619200'
# Tue, 17 Mar 2026 01:07:01 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 17 Mar 2026 01:07:02 GMT
ENV HOME=/home/user
# Tue, 17 Mar 2026 01:07:02 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 17 Mar 2026 01:07:02 GMT
ENV LANG=C.UTF-8
# Tue, 17 Mar 2026 01:07:02 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 17 Mar 2026 01:13:52 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 17 Mar 2026 01:13:52 GMT
WORKDIR /home/user
# Tue, 17 Mar 2026 01:13:52 GMT
USER user
# Tue, 17 Mar 2026 01:13:52 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:0b5164900a4737bd8c71921f9d6095f2a9499d5081755c56a4aa46d8f37e9865`  
		Last Modified: Mon, 16 Mar 2026 22:10:41 GMT  
		Size: 28.3 MB (28275636 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9858543b6cdb95faa5a271d8d6e144f9bebdcbe3a9c5b6ef8f5fb4bb06b94415`  
		Last Modified: Tue, 17 Mar 2026 01:15:46 GMT  
		Size: 18.6 MB (18554804 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb4563f0caa4e9e53a466cb918133ac9e4a6405287e7995dd0f88bac22193e72`  
		Last Modified: Tue, 17 Mar 2026 01:15:42 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8f37ead72ac6f64000b3808b93f9d7aa91c91feab9f1cb9dacee4479704c13e5`  
		Last Modified: Tue, 17 Mar 2026 01:15:43 GMT  
		Size: 4.9 MB (4860679 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:89d031e6fd4a44af129ffc83fb02a40d7d37e3a491871dbad7ab718dea95b570
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5598537 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ffa087de9353474ba006a98dcadcf0a73e53faa63799c5ece469f3bbc7aad2ac`

```dockerfile
```

-	Layers:
	-	`sha256:d3a65bc22acd92912ceac134ebb9a042fed6644c02599f5de92da2554623caab`  
		Last Modified: Tue, 17 Mar 2026 01:15:44 GMT  
		Size: 5.6 MB (5579814 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:2536062f6e034e6ef3adc4b1566293f22e5ea30df6bae1d1325244190d6cc0ea`  
		Last Modified: Tue, 17 Mar 2026 01:15:42 GMT  
		Size: 18.7 KB (18723 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:16c45edbb53f73d35416492ab7fefab595ed708101a34a8ab298e7e875f6ef13
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54513134 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:add98d16ba468c5f0141ec9bc72f3ec4e70a34f8dba4bc40d4789a5e9499b6c2`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 16 Mar 2026 00:00:00 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1773619200'
# Mon, 16 Mar 2026 22:19:52 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Mon, 16 Mar 2026 22:19:53 GMT
ENV HOME=/home/user
# Mon, 16 Mar 2026 22:19:53 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Mon, 16 Mar 2026 22:19:53 GMT
ENV LANG=C.UTF-8
# Mon, 16 Mar 2026 22:19:53 GMT
ENV IRSSI_VERSION=1.4.5
# Mon, 16 Mar 2026 22:20:30 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); printf "*%s\n", so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Mon, 16 Mar 2026 22:20:30 GMT
WORKDIR /home/user
# Mon, 16 Mar 2026 22:20:30 GMT
USER user
# Mon, 16 Mar 2026 22:20:30 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:2c02a3d3f135c4bbe56488921bd86d969a76dcd5278abca1e81884d3bff0bd88`  
		Last Modified: Mon, 16 Mar 2026 21:52:55 GMT  
		Size: 29.8 MB (29835265 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eb10e7d0116bc67deaad33352b5dd8dbf874615e4b7a8da9ce6352825587393a`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 19.8 MB (19768702 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da4efe93509da5130f31ec16fe6392dc1209ca1ba007bf2c384f1144d2dc0327`  
		Last Modified: Mon, 16 Mar 2026 22:20:48 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7a78c2e6061da1698c646011666b27584ee7e0995352863a2b5007d361bc7a6c`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 4.9 MB (4905810 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:d8859d4c623030a138b8a3a2c91c74c214ab9b30704054451bc7332eeb9633d5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5608066 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2547317a5b935ab6ab9e9d2398a4bbc9622c0ac96fd76625c4b1be9fe4e6df77`

```dockerfile
```

-	Layers:
	-	`sha256:a5c41ac4cced1161224fdb9bf27afd7821bdb0e5437a728cefbd25b6b9cfa107`  
		Last Modified: Mon, 16 Mar 2026 22:20:49 GMT  
		Size: 5.6 MB (5589416 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9e3e507638aece2e1272791643753c89eaf5b5dd3120dec3612fade2187f2db2`  
		Last Modified: Mon, 16 Mar 2026 22:20:48 GMT  
		Size: 18.6 KB (18650 bytes)  
		MIME: application/vnd.in-toto+json
