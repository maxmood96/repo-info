## `irssi:1-bookworm`

```console
$ docker pull irssi@sha256:055913d85126e5fa68e5550ed4c9681198548068dbe60f9b05076f274c51a2e9
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

### `irssi:1-bookworm` - linux; amd64

```console
$ docker pull irssi@sha256:ad2d92a2b6923759f0bfa3bc865efac3e5fe2b2d11e0e9fa4930ddf9ee0da344
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75869071 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9482bce16535d397822db7f41bbb171b46f12a3cb191978fed9c713a9fff5755`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:b86ae1c7ca3586d8feedcd9ff1b2b1e8ab872caf6587618f1da689045a5d7ae4 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:8a1e25ce7c4f75e372e9884f8f7b1bedcfe4a7a7d452eb4b0a1c7477c9a90345`  
		Last Modified: Tue, 12 Mar 2024 01:25:41 GMT  
		Size: 29.1 MB (29124181 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:582d1e1e2493b9307c11b074ce370a24f812884365e1ecc88bb4fdf3b259609d`  
		Last Modified: Tue, 12 Mar 2024 01:55:47 GMT  
		Size: 18.3 MB (18267915 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80db29b097f3b112fc1ff243d00079ba54461223baa0b050a75bf99f9cce2ca1`  
		Last Modified: Tue, 12 Mar 2024 01:55:46 GMT  
		Size: 3.3 KB (3332 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:204c39e13724b78cc8d75cbbf3e0997ae1354d5b435678d3fa17badc2500930c`  
		Last Modified: Tue, 12 Mar 2024 01:55:47 GMT  
		Size: 28.5 MB (28473611 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:dcaaa93d646ca3d60351c50ae57406136b89d41f2b1c337f417dd6139afd19b3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7665049 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4e11af5f29b8e696cedb9197a4ca315fbdb72c66f20a571478fe2d3084aca08d`

```dockerfile
```

-	Layers:
	-	`sha256:5b64f771d60768ba7a9d9f21cb144f64d3fc7e5e1d89f32f6daeee0295701245`  
		Last Modified: Tue, 12 Mar 2024 01:55:47 GMT  
		Size: 7.6 MB (7646446 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b6ddf48e28f883d56fffbba37157de8475387cdaad57a9e8dbb29d35dda362ab`  
		Last Modified: Tue, 12 Mar 2024 01:55:46 GMT  
		Size: 18.6 KB (18603 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:de60f3b1ca48c2f8a3f55bf3c7ce93d5e51d13f8ca53a5e75e8fe4d38b4b3c48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.0 MB (70045244 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f16962b86de84f1bc7cab33580eb4cd4a3ed925bd1b232d835fd7f8f228b4f0e`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:b1bd2ec7dd2a8894ea7b5837afba4e15ba798f4809586f0ac1b8855bd0032651 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:64806d9455193063a6bd4aebf47380e94fad8313f6ad1b5d831882c453f43261`  
		Last Modified: Tue, 12 Mar 2024 00:51:39 GMT  
		Size: 26.9 MB (26884021 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9bcc7deca2e5639a8faa6f42193ab221a143391ebf3a0eab4fa68d1a7eeb4d7c`  
		Last Modified: Tue, 12 Mar 2024 14:57:24 GMT  
		Size: 17.0 MB (17042078 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:777acae739a4824ae2c46f92724f59103d34fcb96c0729f738a2e2d87616cfd0`  
		Last Modified: Tue, 12 Mar 2024 14:57:23 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:26378f570f40924fd40313bd1bd350f56cbae3c7b8a0714d7a34302cb3853bdd`  
		Last Modified: Tue, 12 Mar 2024 14:57:24 GMT  
		Size: 26.1 MB (26115784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:5bb6ceaad6e38827d9f4bba59a486b25137974aa12e36a324879214779a3c137
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7633460 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb3e3b03d3193fa9ac5f0c24481aeaf37dc393f650ce4398d3abdf1081a0a934`

```dockerfile
```

-	Layers:
	-	`sha256:8df51a2ed41a99f99d90f2ce572d3ea4ebac12f981d3f3731afecb33539a7b0a`  
		Last Modified: Tue, 12 Mar 2024 14:57:23 GMT  
		Size: 7.6 MB (7614896 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:f5e2386e6153d33c9ecb25356e8e7530d0a389cf70afe866db1d463defb19082`  
		Last Modified: Tue, 12 Mar 2024 14:57:23 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:fc0d653d61d3945bf0570318dbe2f6c9900983aafcf73e52487708591c9011c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.4 MB (66369132 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fb2d7facc1c2bf2956ff1c012f670eeff961a195f0fe5f574b5a0a07cb3b29e1`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:6c18cdac8d96366de6fc24521b972b80d34639ac5484f27a5d4e355fca934e5d in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c5c3540d9b4f416003fa1e21822e15ea4bbe0749e6d1104e7af5c8a1a30b26fd`  
		Last Modified: Tue, 12 Mar 2024 01:03:36 GMT  
		Size: 24.7 MB (24716725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8420bbdfd2faf36185715f9a54d19b09f9cb01b572f876d020475a8745bc9048`  
		Last Modified: Wed, 13 Mar 2024 00:42:00 GMT  
		Size: 16.6 MB (16635173 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:664285349a936b2551d811d8d81e0efb2d7fa586e11054d3e7bb35359bb27a23`  
		Last Modified: Wed, 13 Mar 2024 00:41:59 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:510eaf8a72d7beaeb98fdbe16ea5917f59027c9367d9a11af73d813bf6203f0b`  
		Last Modified: Wed, 13 Mar 2024 00:42:01 GMT  
		Size: 25.0 MB (25013875 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:b0b62d2aaebb504784c2cb3b0724e75a078afec67624b195d257204a398321c6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7634428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1c02406bf500bc7189c5c0dd9f87d7330b621a6ac3062137f309dd7135da6421`

```dockerfile
```

-	Layers:
	-	`sha256:6b6d3ca761f77f01470d06b4ea0a2e915a5f8537f27e75b427733e17c6a653d4`  
		Last Modified: Wed, 13 Mar 2024 00:42:00 GMT  
		Size: 7.6 MB (7615864 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:03f3bb1899c7734da476aae1b96f0e16b556d201b9ef999fb9d06cb77c11e083`  
		Last Modified: Wed, 13 Mar 2024 00:41:59 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:c1311d38ee6e2be9aaafdf522e97332382bb4e03f5ed4e8407f3c84ff330bbcf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.6 MB (74627380 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6106de5c4ef153bcd85e95659af5558d64f48735d93d154fa9f73a6db1f6818e`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:85e3f04235f949795629380f3a50ca566471f0258cd4322937c8b1e0648a69ae in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:59f5764b1f6d170ea07ca424965974024a14970ff826e9ffa3489c90dc040c24`  
		Last Modified: Tue, 12 Mar 2024 00:48:56 GMT  
		Size: 29.2 MB (29156434 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b2dfa30960065bddabb8009b2cc083aa4ca9a9041807e2479e89702514c2643f`  
		Last Modified: Tue, 12 Mar 2024 21:55:46 GMT  
		Size: 18.0 MB (18035387 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:53e7ed76783e5afb7e0f1751a7715b6468db749599fb35599acfef979cad9634`  
		Last Modified: Tue, 12 Mar 2024 21:55:45 GMT  
		Size: 3.3 KB (3330 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ba4243f8d542a0b235f75dba411ba612b6ed3952a4c01a2f605426cdc4b56173`  
		Last Modified: Tue, 12 Mar 2024 21:55:47 GMT  
		Size: 27.4 MB (27432197 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:c8955fcc526175dc80bf83fc72d3253326b35f47f77a1e022d1f9debc140aa4d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.6 MB (7642333 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef09c241c3416744693f519a7d7b6c361162b9f5a59ee5c99cd3faedfd5ba1fb`

```dockerfile
```

-	Layers:
	-	`sha256:b5994dcbbd5ab56f816cd78d8415867dfb792f4e89d29e068c5666116a5a2661`  
		Last Modified: Tue, 12 Mar 2024 21:55:46 GMT  
		Size: 7.6 MB (7623879 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a560de11e063ce41b045e88b5eb9ba0dadcda421e8bde1c2f0ad000114aeea7d`  
		Last Modified: Tue, 12 Mar 2024 21:55:45 GMT  
		Size: 18.5 KB (18454 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:bde96bee91c54b9eb5667d98b240d49012a84b09879e802a88fe32d6d0b58546
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76298466 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5329e346461cf9ce8c83137b7e0e6420ff3c84210e5d0ba5a3474ca63e29ed07`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:88f04d79dc9f1691544c636ff52d6744a2ff68d504793ea8034b797d0bfc6fd3 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:576af7ffb10b3f3b8d5523e6b91da8667eb39393cdfd50fb26dfc178e504ba70`  
		Last Modified: Tue, 12 Mar 2024 01:02:43 GMT  
		Size: 30.1 MB (30141873 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0d0395da1d241c86eda2fa2c49f390657278234d92ce2d73c973b8ece26e0cfa`  
		Last Modified: Tue, 12 Mar 2024 01:55:43 GMT  
		Size: 17.8 MB (17795132 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bfc7dbcef2877f83dc1120a5b60eb70d4bab1318fc6cd30c76dd2477c33bf4a1`  
		Last Modified: Tue, 12 Mar 2024 01:55:42 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d152b698aad7a71bd233b06cb37642500f6d248b6dedf88135278c28ea118da8`  
		Last Modified: Tue, 12 Mar 2024 01:55:43 GMT  
		Size: 28.4 MB (28358104 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:ba3c3abdd343011d4f359c1868eddf4f9821e0f2e5686279ece0932db92ffe86
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7657625 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a8973ef69240cde5d25a228732d076b7b65ec75a3f0e945aad121c6893f45e55`

```dockerfile
```

-	Layers:
	-	`sha256:2c463a7caeb1c491167499b57163d879f58deb51b76045c1f183dfb63facdda2`  
		Last Modified: Tue, 12 Mar 2024 01:55:43 GMT  
		Size: 7.6 MB (7639075 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e15be1baec7755353f898278b0c90db0978a5340f5de3595f8600b2901e062d4`  
		Last Modified: Tue, 12 Mar 2024 01:55:42 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:dce3ac50d17a08cc406358f69231a82e1631ed99e36324afb93a9f68663ab9ed
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74071406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f90d0eab6cf48a12adfb59de5b7b2c3c249ff7efbdd83c551933e8633baa7dd8`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:c03c59e261bb08f39e6a97df2fd4b82f1e11b49a62d1859a8f8efac680b80a88 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:aad79459a0f767fcded51c9547150a1cfd96638972389ab8621b5f3eb4a9c280`  
		Last Modified: Tue, 12 Mar 2024 01:17:09 GMT  
		Size: 29.1 MB (29119205 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:05a1b9063df6782dc40b01a454d557546fd423005894d985f2e89e7a0e722e2f`  
		Last Modified: Wed, 13 Mar 2024 02:33:17 GMT  
		Size: 16.9 MB (16941970 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:12f56104cf19e64dc2b75d419e5a3cd7174084318239eda02776013089aed836`  
		Last Modified: Wed, 13 Mar 2024 02:33:15 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3c532e3542df9d96d233d4ea656513eb8276fe88965b58b0db6837279d24adf8`  
		Last Modified: Wed, 13 Mar 2024 02:33:18 GMT  
		Size: 28.0 MB (28006868 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:2a3e0b513a618c32e634257c22c885c25730e6e95df7d168dfb11c4015c05807
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:748bf3d8a82630177b9b67425b9bff90e107d8d285dfec18dcdac142ebafac1c`

```dockerfile
```

-	Layers:
	-	`sha256:138b494034ce96b91827c9d3540d1d656ac4b33016cd1f0c60b27cff37080e6e`  
		Last Modified: Wed, 13 Mar 2024 02:33:15 GMT  
		Size: 18.3 KB (18320 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:40977063293f74d3f6e116014e8def1fc34a4778319c6d32e3e662a8b49e3b26
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.9 MB (81865315 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:16376e2e7f5dbf6d6aac1d23e70035033fcac79907e03ca6ee4613b93c8c0f8a`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:9273ef56d086dbc93b46b7e8ae424eb04096fb00c693dd6cda1f48346290d4d5 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c28cd0e276dcdeb4d44f5cc5bb958610750ff902a081b668e3863c2f38eef054`  
		Last Modified: Tue, 12 Mar 2024 00:38:06 GMT  
		Size: 33.1 MB (33119023 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4ffef820b3af3e9b52b7e9b34e00c0a28ecee9a950078bdc934decff7fad2442`  
		Last Modified: Wed, 13 Mar 2024 02:05:04 GMT  
		Size: 18.8 MB (18765658 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e2ff8ed08063693275bc7ef8b3942ec4044135b87bf3f4e83a5b5522858c6a43`  
		Last Modified: Wed, 13 Mar 2024 02:05:02 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:496152e0e053477b1c5610cc35eb180d23fbfa97f844fd34174eeac4cc93e7fd`  
		Last Modified: Wed, 13 Mar 2024 02:05:04 GMT  
		Size: 30.0 MB (29977277 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:be5125210a3e78f62d99645c19b84d5cfa3410bad5cadbb567edcd6804c8aa3a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **7.7 MB (7654557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:678de622d464e8b7e988a9795fe1ffc8665c15f3754e264c31e480dadd2b810a`

```dockerfile
```

-	Layers:
	-	`sha256:529eda450bc5080f006ad7062de5988bfaacc325cfc3a235b40e18ab253136e4`  
		Last Modified: Wed, 13 Mar 2024 02:05:03 GMT  
		Size: 7.6 MB (7636055 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e233e6faffa2f9c9e3ec7ce497705e0d7aa6168a1cc24e447ef015ed20a2d688`  
		Last Modified: Wed, 13 Mar 2024 02:05:03 GMT  
		Size: 18.5 KB (18502 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:f9a771bdecd02b65e97e7e7baa83460d3db3a32f69b7da86b2800944a171b664
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72729436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0a2be125cafffe145515c0036e1c6561bebc318b4b182598fb5fbbfe9081615`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:2dc5fd465b3cc728990229e12489d68faf8a93e6f574cacdca11cc9bf31f511d in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["bash"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		libdatetime-perl 		libwww-perl 		perl 		wget 	; 	rm -rf /var/lib/apt/lists/* # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	useradd --create-home --home-dir "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		savedAptMark="$(apt-mark showmanual)"; 	apt-get update; 	apt-get install -y --no-install-recommends 		bzip2 		gnupg 		libglib2.0-dev 		libncurses-dev 		libperl-dev 		libssl-dev 		libtool 		lynx 		meson 		ninja-build 		pkg-config 		xz-utils 	; 	rm -rf /var/lib/apt/lists/*; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		apt-mark auto '.*' > /dev/null; 	apt-mark manual $savedAptMark; 	find /usr/local -type f -executable -exec ldd '{}' ';' 		| awk '/=>/ { so = $(NF-1); if (index(so, "/usr/local/") == 1) { next }; gsub("^/(usr/)?", "", so); print so }' 		| sort -u 		| xargs -r dpkg-query --search 		| cut -d: -f1 		| sort -u 		| xargs -r apt-mark manual 	; 	apt-get purge -y --auto-remove -o APT::AutoRemove::RecommendsImportant=false; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:e55f0b78e9a121a048a72242f0aec2a221466b10bedb873c07b73e4b99f873cb`  
		Last Modified: Tue, 13 Feb 2024 01:30:22 GMT  
		Size: 27.5 MB (27488587 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:725b5eed9447ac4e99e0776a094f9551b09fcedb42e63b5544f2dd43f4bed3de`  
		Last Modified: Thu, 15 Feb 2024 05:11:04 GMT  
		Size: 18.2 MB (18215134 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b6b1170c81f6c3fa2de886603999f13e5f4e0893e630a3b4bed694bf669a78c4`  
		Last Modified: Thu, 15 Feb 2024 05:11:04 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d2562af3b5c3ee533f41cf49a8d8147fce57b97c2153e953fed9ff0184dc444b`  
		Last Modified: Thu, 15 Feb 2024 05:11:04 GMT  
		Size: 27.0 MB (27022358 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:78696dcf9293e7de604611b85896e1b16fe055a5e85a926575158052af51f4fe
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6624223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4b5349254aabfc07202ae8ca9e08039c6c6d63d2fa377da7d51d7a26f1513db1`

```dockerfile
```

-	Layers:
	-	`sha256:a954d232f3ed6c99df586eb52c317d81bed3e0dfc9009011cb89724e6e26b708`  
		Last Modified: Thu, 15 Feb 2024 05:11:04 GMT  
		Size: 6.6 MB (6605787 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:dc9ce212bfd7fbb6c714f4cecce09176182b8c9b5f0221f1d4f8eb557d52d11f`  
		Last Modified: Thu, 15 Feb 2024 05:11:04 GMT  
		Size: 18.4 KB (18436 bytes)  
		MIME: application/vnd.in-toto+json
