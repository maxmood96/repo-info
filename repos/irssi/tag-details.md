<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `irssi`

-	[`irssi:1`](#irssi1)
-	[`irssi:1-alpine`](#irssi1-alpine)
-	[`irssi:1-alpine3.18`](#irssi1-alpine318)
-	[`irssi:1-bookworm`](#irssi1-bookworm)
-	[`irssi:1.4`](#irssi14)
-	[`irssi:1.4-alpine`](#irssi14-alpine)
-	[`irssi:1.4-alpine3.18`](#irssi14-alpine318)
-	[`irssi:1.4-bookworm`](#irssi14-bookworm)
-	[`irssi:1.4.5`](#irssi145)
-	[`irssi:1.4.5-alpine`](#irssi145-alpine)
-	[`irssi:1.4.5-alpine3.18`](#irssi145-alpine318)
-	[`irssi:1.4.5-bookworm`](#irssi145-bookworm)
-	[`irssi:alpine`](#irssialpine)
-	[`irssi:alpine3.18`](#irssialpine318)
-	[`irssi:bookworm`](#irssibookworm)
-	[`irssi:latest`](#irssilatest)

## `irssi:1`

```console
$ docker pull irssi@sha256:df2314e3c83d5dd353eafa769eee4302e869ca2782ba3906a63beb9c1e45d88b
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

### `irssi:1` - linux; amd64

```console
$ docker pull irssi@sha256:f348397f4e94c8233af74fdea9b0e212e59940476974ab34d100894496547bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75868792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ba45dda22d90fa5e9e29f44f3c9db5d8f7ef6ab9a565f15845b3fc25c70ca2`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
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
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c80471fc9f279ecbb940d938880d5d417992f34809cffcc35de55e5c5b7b50`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 18.3 MB (18267918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2fe054dac6c8448486f7f83fb8d9a935f49600d14786eb028d05f1aca7be4d`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0c8cbf7b0f50debae5d2c4db813db40ef72d3f463d35255151d01f443c8f3b`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 28.5 MB (28473427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:0b4f3f615631a2195ca922bb269cc41ce0094ca6b506c2a6f42972e0edb4bb85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6635471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5bdb10eee477ea82a96d9db1c1a6ba2b86d46b4a80e1a99fc3067f614e5ead`

```dockerfile
```

-	Layers:
	-	`sha256:ad8396ba1d7eb23f85a9f1aa776ff1736aa74a41840bdb1336c90e8b0502ebd8`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 6.6 MB (6616868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97019d8cfce10dc023be567084137669d8fb7772cec7218f1e711f4cfae562dc`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 18.6 KB (18603 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v5

```console
$ docker pull irssi@sha256:87ad7b222f94bd4ffeda78eb7cf201ac297f22792db2eb6c627342cd68e91c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69868386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df3cfc1c8fffefd348cacfe8d18c9367e7b15f4227b2b32750bba9a1dad4eba`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:557a5348da1e680593a9ba709ef059b96baf15e0c89d8f8343e97bf008d9dc05 in / 
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
	-	`sha256:b508f3272b9b70b8dd19c621a4da1be63880a1f6412063787647ceeb464d772a`  
		Last Modified: Wed, 31 Jan 2024 22:48:00 GMT  
		Size: 26.9 MB (26909323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5389309a8aec1769eaeaa29319de4bebf1627abb4b7c25ceaef27190cd064cfc`  
		Last Modified: Thu, 01 Feb 2024 12:00:33 GMT  
		Size: 16.8 MB (16840201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31b408b37e2ea86da1e5dbb066b4b3fb5d09551561012dec426720879e0ebee`  
		Last Modified: Thu, 01 Feb 2024 12:00:32 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3f755d015144784b5213f297ec37d52ddb303651246f90287675b59fdb928e`  
		Last Modified: Thu, 01 Feb 2024 12:00:34 GMT  
		Size: 26.1 MB (26115505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:10fa924814f0100863a02d43cde888366c56bb1999d35f4ec2cb5458ede1d8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6608604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005c1e6b2319f0434d5ccdc6f83cedaf5c4931041228a3b257bf9d9d5fb2e4c2`

```dockerfile
```

-	Layers:
	-	`sha256:f0eebab35555f3e7c0ebb7213ba7f2f39f5d2117387aec58252ad62f3578ad40`  
		Last Modified: Thu, 01 Feb 2024 12:00:33 GMT  
		Size: 6.6 MB (6590040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32bd71fd61ddf99b170b9b0785a26c0ee132d0d4f5715fac60a135b66c6200a2`  
		Last Modified: Thu, 01 Feb 2024 12:00:32 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm variant v7

```console
$ docker pull irssi@sha256:acbb7bca937bcbdadea02ea51bd199c2c3cb20c4710043cabbf16dcbc82ec971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66192097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9882134ca1726fbcba90c8ffa149ba970b02f9ca5f6f67952d386a590416acb3`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
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
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710b5644e8d7ce9b22f8100f04ed12089274d8e6ecaa7b281e784390d9a624b7`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 16.4 MB (16432998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c9b75f1d3fb010ce226691f08e04e0eca369822f016344e74c988e7ff9cbd8`  
		Last Modified: Sat, 03 Feb 2024 11:14:04 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4b63d99a8fee13ec791237ca413916d8e6c7533abae83274d4674c855395`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 25.0 MB (25014178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:5741bec69a3a0a56fa45545bb9325a960c1706d417f5c2d6739b28b865f70c2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6609678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e40dd73c96b2bc78fa4fc0bc3ebf1c7edb34aeb93676b09737429a7b8d753b0`

```dockerfile
```

-	Layers:
	-	`sha256:72cf1412c4556bb0f02816b52887305bbd5ebccd80827e0404367c869478d2ed`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 6.6 MB (6591114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64c76402e6b60447a3e1c01a7d118cb99869ea18b5b76ebe57796f09cf7cea62`  
		Last Modified: Sat, 03 Feb 2024 11:14:04 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:ab01c34a30c278373d07d580043e8a18e72fdaedef7dda4a42dc222f7b997295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74448713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6936425758539b2ebe94594f0f57669ce6f225b3fda544a7169b3a8c918fcf70`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
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
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3ca413b8af66fc07e47a491183e81f2d8418a36f4b96f3bdf10c96382787ee`  
		Last Modified: Thu, 01 Feb 2024 15:38:27 GMT  
		Size: 17.8 MB (17832825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f66dbcdfcc246d829efadc3627c1885169a547fd80fcef2f9f380ffb2cbc82a`  
		Last Modified: Thu, 01 Feb 2024 15:38:26 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0c68f2c78a25389c67e4236b05e25abf97345db7813892b2d0e8f00ef530db`  
		Last Modified: Thu, 01 Feb 2024 15:38:28 GMT  
		Size: 27.4 MB (27431697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:9b2ce4726f911cecf3cdc2ce92874aa0c7a1d9991a3be9a1fdb8488f3507b3d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6615993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d78c2cfaac7640d2fba3d28b916ab8c140371df8abe66975d35d9d5a224e724`

```dockerfile
```

-	Layers:
	-	`sha256:88a3436d2dc5f0b5a747fedf9b08fd46e9fa64aa7be78c7dc416e4ec9fc043fa`  
		Last Modified: Thu, 01 Feb 2024 15:38:31 GMT  
		Size: 6.6 MB (6597539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:174c63d7fedd1ff225033ff0e20a26b24492ce336185f5f0c5ca8a39e2e2b217`  
		Last Modified: Thu, 01 Feb 2024 15:38:27 GMT  
		Size: 18.5 KB (18454 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; 386

```console
$ docker pull irssi@sha256:766da4d0c23a6b5a02fcfe6a9c290de6c880f481723bd162ec357b72a4b47a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76119263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6e2b48aea52eb23e814469cc9fee45495df60d11dcfcf7136304f394069c00`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:540e2de73452bd162dd7f630bf29f60e7d2e4a7a5d32a495bedf8ad390b59d7f in / 
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
	-	`sha256:34ef135b45f33052e8e5bca668f9a45a938944a9cf3fb73a46f54a7bf11f091b`  
		Last Modified: Wed, 31 Jan 2024 22:43:46 GMT  
		Size: 30.2 MB (30165018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dbf5ba1aef114655d4178cb7b25fc40be6cbbc4e74271ef3c0d129f27f7948`  
		Last Modified: Wed, 31 Jan 2024 23:55:35 GMT  
		Size: 17.6 MB (17592714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5c8ab8d6a9d2481fb1e6c046eda1e5bebc72c7171390e7918bbf3230a3a722`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f0f14697a5f1c37fedc3b6d79441454aa012edc2c624b113dab83f6ae387fe`  
		Last Modified: Wed, 31 Jan 2024 23:55:35 GMT  
		Size: 28.4 MB (28358174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:209fdc2b901e8609cc13ee3d75d5ddc3ddc5a77eb48684669e38db4fecc4c502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5adccb9448d759136b20f5bdf9d17e7b24e77b7f9ab897d4f7e971f758f79bba`

```dockerfile
```

-	Layers:
	-	`sha256:d1c4277341c5a786dc08c35575a05e75f388d342d5a278a44d83c0c37d739506`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 6.6 MB (6609873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ee0cd483b9775bf82c5f73475a171139475368fc3052df090bfb26cafea30e`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; mips64le

```console
$ docker pull irssi@sha256:5b07d620f6e0a5a433dafa6289d75943fe3f50b878b31f3b50428e645a145462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73891556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec83415acb7aaf453c85c9fbf2dcb484813439e60106ce3678051032190e571b`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
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
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0542ca44f4608abe3eb8928a6679f1310a135de5d26dcaef75fdfc7158cb3ea`  
		Last Modified: Thu, 01 Feb 2024 20:14:13 GMT  
		Size: 16.7 MB (16739448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5445b96f290754cc47514654bf406c8cf27af72cafe3c07122d2319baeab5c6`  
		Last Modified: Thu, 01 Feb 2024 20:14:11 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c99cf776ed9d9e58bad7c58c6a56f0e52654611186998435beea42f692d00d`  
		Last Modified: Thu, 01 Feb 2024 20:14:14 GMT  
		Size: 28.0 MB (28006308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:2374bfe0c2ed5ac9aa6c56cbcd7c04c3173332bc39faa38c57a475b929a9b702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2339be92d5d786c3309d29bedbceefe69adad7b0444bd27b86f0b90776e9a30`

```dockerfile
```

-	Layers:
	-	`sha256:28e3d51004b87049273ec1ea39d8930a3cfdd6cc05b2194a9e96b65bca71c335`  
		Last Modified: Thu, 01 Feb 2024 20:14:11 GMT  
		Size: 18.3 KB (18320 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; ppc64le

```console
$ docker pull irssi@sha256:99fee1cd7190e2738316eca944f9cb4474388bdcdff44d4e7492808c79c1838a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81689464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a168acd494049e622c9716bfe5c16cc1c017bea4033b8fe102da9b3f41c70dc`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:fca8b919a8d1e36420dd1e3f3e427aaaae28a2f57e46c27207acd8e3df0d7a97 in / 
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
	-	`sha256:dfeacd5cd8171f4516ea86dadfb60a372eabf49428dc23d2efdda68cff5b05e7`  
		Last Modified: Wed, 31 Jan 2024 22:34:24 GMT  
		Size: 33.1 MB (33142917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a3bd8096c05f1674995eeb051e3cdf023bbca5505b3f75e624f37c5b13e1b3`  
		Last Modified: Thu, 01 Feb 2024 12:57:44 GMT  
		Size: 18.6 MB (18565973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c5b4610ff6d9b857d7b8bcbc7a90224f918f31c45540cb15c1625a86bf95bc`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcf5f7f76af69ab342a135aed7b0fe5dab9ec932f2bcaeeb58cf8e9491096cb`  
		Last Modified: Thu, 01 Feb 2024 12:57:44 GMT  
		Size: 30.0 MB (29977216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:e5e62f13b43055d9255623225d660999c6209f6cbc9413307aaea737b381644f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6627686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bceb9b0ed2cbb811589e573c40c51eef92a381ce1039e4c4a81f5bfef5f2d0db`

```dockerfile
```

-	Layers:
	-	`sha256:5faeac8a64644b64f37809aa623f431a2453aa3dc443ad2173158318e03ae6ec`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 6.6 MB (6609185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f23996cea2f94cdfa72579bfbb5a59af44283d6b74f21f3d83612614d8698f3`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1` - linux; s390x

```console
$ docker pull irssi@sha256:3be6d24893ec88d5484e2c6ff47dabe648e0c56d532619254ec2005f79b316f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72553121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eeb87370bfa6742ae5cdffe4e9e5fbcded5a376ea20cb9f0ff781310654cff`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
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
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4594bbef0c3ed6e5d274cc97e215f696416fa4ae17044dfd8fe130e789bbc1`  
		Last Modified: Tue, 06 Feb 2024 11:27:01 GMT  
		Size: 18.0 MB (18014343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb84559c99fdfcc14828d4d1d39640bc61b21c99711be784b356d5c32b0fc8a7`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f15c7c91a157b6cb1adb4e9eff1265e940d9ae9d78fa1d5396c6d03f14b7e6e`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 27.0 MB (27021938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1` - unknown; unknown

```console
$ docker pull irssi@sha256:2c98314fd3cf3cdcc7aca67a7f251b24cb5c0f597abe52b639fda52f8631094b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6624174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1856fea1ea1713d5b1fe2b0ff097f7d0a688d0bd16c23f7de87310eb9f37a7a8`

```dockerfile
```

-	Layers:
	-	`sha256:e65ba0bc6f82ed76a16bdbe6b6618f3835b881b23d55dbc63e573dc31c537b19`  
		Last Modified: Tue, 06 Feb 2024 11:27:01 GMT  
		Size: 6.6 MB (6605739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01339a4362670ca4baef375e49a866c7339d89de67789528e853a5a62dd0a787`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 18.4 KB (18435 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine`

```console
$ docker pull irssi@sha256:294a5ddd1a7991782f7df46f7f0b1ef870818a1cf3a9afc37399222c27fa95cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1-alpine` - linux; amd64

```console
$ docker pull irssi@sha256:ef6c7693f4591e49ec7ebb9d9e3ff118d31da2e6e989cc01d7c4ba68d6ab312e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18451473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33d0b6133f016daecdc32847e2719e1b8377593ca3a157e4e2182ec699b3619`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d5073c9dc162f6d73c33561ca62b1f3d4afe73e51dfe01bc3bdbe570603526`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 9.6 MB (9645490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaa94b168ed27385c169187548faa3944812324045e5b7d4f9fa0141d934de7`  
		Last Modified: Sat, 27 Jan 2024 00:53:19 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33ada92546b652616e31a208091cb77dc65019c90e5944f396554ea13e63472`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 5.4 MB (5402150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d7192c220068161f91626a3d88eb71585cea3908b88e32bc9d7a200ba73e04f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.5 KB (992458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e03dcb09479e1e99b8f120055916a32994d838a16cdeba603eb3779a35bdb3`

```dockerfile
```

-	Layers:
	-	`sha256:2d6761df79ddf9480ea4aa104a72a140a5347d5dea19b3eb975a78d2a144483b`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 975.0 KB (975030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f3ba2fd4c9e25b6b8c3ce87fda3494b8506f3cebb1bc0e371df70b3a1c44a87`  
		Last Modified: Sat, 27 Jan 2024 00:53:19 GMT  
		Size: 17.4 KB (17428 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:11cdd850f01f7020ea3dc559a1cacf1710ce7e1110b2b3be3d5088a753388e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980aff2e9d7fdabd52ca418744d9e75a16f305953ff369624a6f3e91ee563444`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1caa0b93da06dd2aa46cce7a3fd9bbc4b0b58ff19b6dee6450b493cb819f9cd`  
		Last Modified: Tue, 30 Jan 2024 18:54:03 GMT  
		Size: 8.9 MB (8880054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93390793c8d561bd6d0fed103d923be9845e322d71b5187396645909aee925df`  
		Last Modified: Tue, 30 Jan 2024 18:54:02 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db82a85a709f0d1d93b2c72989821c461582c5c99c841cb1d8529c32826084d`  
		Last Modified: Tue, 30 Jan 2024 18:54:03 GMT  
		Size: 5.2 MB (5242167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:bd1dc317b136af3a211fed01816891cbea3e545a66d52fec0a8cfe3c9ae9a9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 KB (17341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af05cb00d364bd5dc1c1184bb77489a40ba8096333fcb8ad4b6969822a45b3ac`

```dockerfile
```

-	Layers:
	-	`sha256:7a7a2bdaf6762372aa21871c515a18d90c4cfa782df359a7f10dcafb1a8acbcf`  
		Last Modified: Tue, 30 Jan 2024 18:54:02 GMT  
		Size: 17.3 KB (17341 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:89e22268640c72b2ae0efb98e009b34bd5534ad6c4aa596df74bfd27c1775e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16630432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9bff58300e84d8932cb47d4638ebdafbd9eb55888c2cfe35e7c89ce11cacec`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a728625b39c4526fc00d553e9ad76abf2d838e770db539a4503401b8151b7`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 8.7 MB (8721243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80dec7634cb6fd64dad041788335bf81e0374c155777e94d292608fadbc918e3`  
		Last Modified: Sat, 27 Jan 2024 16:10:09 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a274dbd32034295ddcbc1067913cee45ae78dfd48bcfa5a5a0227438b251e6c`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 5.0 MB (5006505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:81909a4824efd52f673139f1bfce8946affddffd9073b10d3429fc7e6a25b6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **995.1 KB (995130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f8bf5414c3b8dabe31b6645b897840a59666ed989623f0fa633e51cd171a51`

```dockerfile
```

-	Layers:
	-	`sha256:788b342a7afe442fa8cc36f28d56399fe0b0abcded67366d9cfc6f4414ec6b28`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 977.6 KB (977574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af9e565fad9e84cc85a9eb745382b7350da37e969b74d2723023407a1dc827b`  
		Last Modified: Sat, 27 Jan 2024 16:10:09 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f967a5aba07f362a1fc42968dc5c25d932ddf7c5afc29b87f3e103f41e11b3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b852dcd533ac6fef70eee55ddc2eb8cd1a1a2438f10c7fb9780fcc8f8c53ae7`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427b55bea52be9d140397d36bdf44940754b11f701ab1c8860bf265108864474`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 9.7 MB (9672879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3172290de02d764723938f6bbf53611e992dca7775d89910602a51d4fdc12c0c`  
		Last Modified: Sat, 27 Jan 2024 20:28:06 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4046f82759ffd91ca630dba178059b2985f3ec4fb9cb5a8d928a59215b0b5b2`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 5.3 MB (5308548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b68051a5d753ec8037cd2f9d14313c65e2bf5d4c67f564eec3f3f58eb4a131b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.5 KB (992495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edf1b50c168b27a6f3a5f6a4b2a2711df8f7bd7bbfdc93ea5eef3a8861c5e0c`

```dockerfile
```

-	Layers:
	-	`sha256:f636b4606a093b4d77ac5276a6d5402ca1ff4b0641b2656d45bb27ff2ed683af`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 975.0 KB (975049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0aae570a126a40b9525d270285ba0d643a33c387a1f9f79698263d38a935f73`  
		Last Modified: Sat, 27 Jan 2024 20:28:06 GMT  
		Size: 17.4 KB (17446 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; 386

```console
$ docker pull irssi@sha256:387d4dc6384ebea47ed5276a5865acb546bb67dfc227fe393dc75db5d45852dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17557817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e96759752775aacd2fda0f53e8cf266fc1c7b3e068566a8fc8c2add735f586`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8086f06106cd7bdd94cddf1c7363b144b801cd672997d9fe81ed6ab8ae03891`  
		Last Modified: Sat, 27 Jan 2024 01:54:00 GMT  
		Size: 8.9 MB (8904430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d1dba1f614043dea1e85138edb339caa7e16cca6c013e81384bd9f7f1afe02`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a341596e873d51872b196d8782ad7c32261c5a181b99f1f2d4c8c053a35a752a`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 5.4 MB (5413031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d7e896f39991af1e19a5fea9c4353550ddd15bbb4fa05afc17e02656c66c8104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.4 KB (992360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617babf31d74046af9500e49f9674cbad6f479da89ac7b7cb51ba62e91a8f83a`

```dockerfile
```

-	Layers:
	-	`sha256:b11bca7efa15aa00afe306253a110a6805f8d56ebdfb10ff646a51e2a4f69f81`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 975.0 KB (974985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4a8d0da397b1dded79f569fffc3082addee92a84c9f41f986ef310c44a72bf8`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 17.4 KB (17375 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:a0a400f2133847c9bbfa653f898fc72042aac4b03cb1371156d8726812131313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18717231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0def155df329eeefa5360cf54f1657dc7731e2f631182fce7e96924a4cabb8`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc74fa4ba26fc8c0460833da6460f59a2b7fdb551209793e9177aa8e4f59346c`  
		Last Modified: Sat, 27 Jan 2024 09:47:30 GMT  
		Size: 9.7 MB (9736547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596eae301f8ffae57ffc8c11b668ca24b994f12d9935de6216884db8f13188d3`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65ab57b806e5436452de1e909990c85bf46bb183048518a40b3e91cceaa914d`  
		Last Modified: Sat, 27 Jan 2024 09:47:30 GMT  
		Size: 5.6 MB (5630906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c822cd405d36a575a6a510133bbc7870de59eabfd7fc4a2bb9485e127fa82363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.9 KB (990946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00c5eb1975042e0f47315f4ba48ed6fe69fbb8e39eb0c845ac7edf8cea9bc47`

```dockerfile
```

-	Layers:
	-	`sha256:51daf79105767963a7bfa2160a6d94beb71eecf88329550e2f9150d944fc2a52`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 973.5 KB (973452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6afd3a59a575c01cda08047a63543de5e7a3b3293e87e18e1bb870d4a2df4e74`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 17.5 KB (17494 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:cb11647a91b30743f090d9c0e26aeb8ac9ad300c50b661af12505ae290befd40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18707370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891ea14f0ba63e76c3bf45e2ede5b212af9d872f0b77a89d369fed7f2d5bfd3a`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc77a74801be7299707a33e8a653a76c9c5b8d7289fad0e44f86f0eb950c0dfb`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 10.1 MB (10082896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f5141af0a2579801617b6ef53cc8da747d109de43e1b88c92ba151618c1c12`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7efe871fc37a59627f7fb75e2cd481a361e23ae4423cbd5c60ebfd9cfc40ce4`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 5.4 MB (5405651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:703020e7529818ace6da7d3f3424df173c4f428cf3fdaadb5bfb9d5a806ea431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.8 KB (990826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168cdfdbfc8e0c3b5a619ac19b836bbfce7a1baa6ab36ceaeb816e42d0073b3f`

```dockerfile
```

-	Layers:
	-	`sha256:a2f8050d7c3f109cc73636ae770c90e2cde71f2ed0dcd93078524351667493a8`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 973.4 KB (973394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304d7cd47112bf0ace221c02f2bdff3de634bfada70e48aad5065bc3c7424e87`  
		Last Modified: Sun, 28 Jan 2024 09:20:59 GMT  
		Size: 17.4 KB (17432 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-alpine3.18`

```console
$ docker pull irssi@sha256:294a5ddd1a7991782f7df46f7f0b1ef870818a1cf3a9afc37399222c27fa95cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1-alpine3.18` - linux; amd64

```console
$ docker pull irssi@sha256:ef6c7693f4591e49ec7ebb9d9e3ff118d31da2e6e989cc01d7c4ba68d6ab312e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18451473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33d0b6133f016daecdc32847e2719e1b8377593ca3a157e4e2182ec699b3619`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d5073c9dc162f6d73c33561ca62b1f3d4afe73e51dfe01bc3bdbe570603526`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 9.6 MB (9645490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaa94b168ed27385c169187548faa3944812324045e5b7d4f9fa0141d934de7`  
		Last Modified: Sat, 27 Jan 2024 00:53:19 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33ada92546b652616e31a208091cb77dc65019c90e5944f396554ea13e63472`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 5.4 MB (5402150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:d7192c220068161f91626a3d88eb71585cea3908b88e32bc9d7a200ba73e04f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.5 KB (992458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e03dcb09479e1e99b8f120055916a32994d838a16cdeba603eb3779a35bdb3`

```dockerfile
```

-	Layers:
	-	`sha256:2d6761df79ddf9480ea4aa104a72a140a5347d5dea19b3eb975a78d2a144483b`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 975.0 KB (975030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f3ba2fd4c9e25b6b8c3ce87fda3494b8506f3cebb1bc0e371df70b3a1c44a87`  
		Last Modified: Sat, 27 Jan 2024 00:53:19 GMT  
		Size: 17.4 KB (17428 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.18` - linux; arm variant v6

```console
$ docker pull irssi@sha256:11cdd850f01f7020ea3dc559a1cacf1710ce7e1110b2b3be3d5088a753388e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980aff2e9d7fdabd52ca418744d9e75a16f305953ff369624a6f3e91ee563444`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1caa0b93da06dd2aa46cce7a3fd9bbc4b0b58ff19b6dee6450b493cb819f9cd`  
		Last Modified: Tue, 30 Jan 2024 18:54:03 GMT  
		Size: 8.9 MB (8880054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93390793c8d561bd6d0fed103d923be9845e322d71b5187396645909aee925df`  
		Last Modified: Tue, 30 Jan 2024 18:54:02 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db82a85a709f0d1d93b2c72989821c461582c5c99c841cb1d8529c32826084d`  
		Last Modified: Tue, 30 Jan 2024 18:54:03 GMT  
		Size: 5.2 MB (5242167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:bd1dc317b136af3a211fed01816891cbea3e545a66d52fec0a8cfe3c9ae9a9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 KB (17341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af05cb00d364bd5dc1c1184bb77489a40ba8096333fcb8ad4b6969822a45b3ac`

```dockerfile
```

-	Layers:
	-	`sha256:7a7a2bdaf6762372aa21871c515a18d90c4cfa782df359a7f10dcafb1a8acbcf`  
		Last Modified: Tue, 30 Jan 2024 18:54:02 GMT  
		Size: 17.3 KB (17341 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.18` - linux; arm variant v7

```console
$ docker pull irssi@sha256:89e22268640c72b2ae0efb98e009b34bd5534ad6c4aa596df74bfd27c1775e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16630432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9bff58300e84d8932cb47d4638ebdafbd9eb55888c2cfe35e7c89ce11cacec`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a728625b39c4526fc00d553e9ad76abf2d838e770db539a4503401b8151b7`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 8.7 MB (8721243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80dec7634cb6fd64dad041788335bf81e0374c155777e94d292608fadbc918e3`  
		Last Modified: Sat, 27 Jan 2024 16:10:09 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a274dbd32034295ddcbc1067913cee45ae78dfd48bcfa5a5a0227438b251e6c`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 5.0 MB (5006505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:81909a4824efd52f673139f1bfce8946affddffd9073b10d3429fc7e6a25b6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **995.1 KB (995130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f8bf5414c3b8dabe31b6645b897840a59666ed989623f0fa633e51cd171a51`

```dockerfile
```

-	Layers:
	-	`sha256:788b342a7afe442fa8cc36f28d56399fe0b0abcded67366d9cfc6f4414ec6b28`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 977.6 KB (977574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af9e565fad9e84cc85a9eb745382b7350da37e969b74d2723023407a1dc827b`  
		Last Modified: Sat, 27 Jan 2024 16:10:09 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f967a5aba07f362a1fc42968dc5c25d932ddf7c5afc29b87f3e103f41e11b3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b852dcd533ac6fef70eee55ddc2eb8cd1a1a2438f10c7fb9780fcc8f8c53ae7`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427b55bea52be9d140397d36bdf44940754b11f701ab1c8860bf265108864474`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 9.7 MB (9672879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3172290de02d764723938f6bbf53611e992dca7775d89910602a51d4fdc12c0c`  
		Last Modified: Sat, 27 Jan 2024 20:28:06 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4046f82759ffd91ca630dba178059b2985f3ec4fb9cb5a8d928a59215b0b5b2`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 5.3 MB (5308548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:b68051a5d753ec8037cd2f9d14313c65e2bf5d4c67f564eec3f3f58eb4a131b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.5 KB (992495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edf1b50c168b27a6f3a5f6a4b2a2711df8f7bd7bbfdc93ea5eef3a8861c5e0c`

```dockerfile
```

-	Layers:
	-	`sha256:f636b4606a093b4d77ac5276a6d5402ca1ff4b0641b2656d45bb27ff2ed683af`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 975.0 KB (975049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0aae570a126a40b9525d270285ba0d643a33c387a1f9f79698263d38a935f73`  
		Last Modified: Sat, 27 Jan 2024 20:28:06 GMT  
		Size: 17.4 KB (17446 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.18` - linux; 386

```console
$ docker pull irssi@sha256:387d4dc6384ebea47ed5276a5865acb546bb67dfc227fe393dc75db5d45852dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17557817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e96759752775aacd2fda0f53e8cf266fc1c7b3e068566a8fc8c2add735f586`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8086f06106cd7bdd94cddf1c7363b144b801cd672997d9fe81ed6ab8ae03891`  
		Last Modified: Sat, 27 Jan 2024 01:54:00 GMT  
		Size: 8.9 MB (8904430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d1dba1f614043dea1e85138edb339caa7e16cca6c013e81384bd9f7f1afe02`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a341596e873d51872b196d8782ad7c32261c5a181b99f1f2d4c8c053a35a752a`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 5.4 MB (5413031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:d7e896f39991af1e19a5fea9c4353550ddd15bbb4fa05afc17e02656c66c8104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.4 KB (992360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617babf31d74046af9500e49f9674cbad6f479da89ac7b7cb51ba62e91a8f83a`

```dockerfile
```

-	Layers:
	-	`sha256:b11bca7efa15aa00afe306253a110a6805f8d56ebdfb10ff646a51e2a4f69f81`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 975.0 KB (974985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4a8d0da397b1dded79f569fffc3082addee92a84c9f41f986ef310c44a72bf8`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 17.4 KB (17375 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.18` - linux; ppc64le

```console
$ docker pull irssi@sha256:a0a400f2133847c9bbfa653f898fc72042aac4b03cb1371156d8726812131313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18717231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0def155df329eeefa5360cf54f1657dc7731e2f631182fce7e96924a4cabb8`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc74fa4ba26fc8c0460833da6460f59a2b7fdb551209793e9177aa8e4f59346c`  
		Last Modified: Sat, 27 Jan 2024 09:47:30 GMT  
		Size: 9.7 MB (9736547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596eae301f8ffae57ffc8c11b668ca24b994f12d9935de6216884db8f13188d3`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65ab57b806e5436452de1e909990c85bf46bb183048518a40b3e91cceaa914d`  
		Last Modified: Sat, 27 Jan 2024 09:47:30 GMT  
		Size: 5.6 MB (5630906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:c822cd405d36a575a6a510133bbc7870de59eabfd7fc4a2bb9485e127fa82363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.9 KB (990946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00c5eb1975042e0f47315f4ba48ed6fe69fbb8e39eb0c845ac7edf8cea9bc47`

```dockerfile
```

-	Layers:
	-	`sha256:51daf79105767963a7bfa2160a6d94beb71eecf88329550e2f9150d944fc2a52`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 973.5 KB (973452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6afd3a59a575c01cda08047a63543de5e7a3b3293e87e18e1bb870d4a2df4e74`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 17.5 KB (17494 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-alpine3.18` - linux; s390x

```console
$ docker pull irssi@sha256:cb11647a91b30743f090d9c0e26aeb8ac9ad300c50b661af12505ae290befd40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18707370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891ea14f0ba63e76c3bf45e2ede5b212af9d872f0b77a89d369fed7f2d5bfd3a`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc77a74801be7299707a33e8a653a76c9c5b8d7289fad0e44f86f0eb950c0dfb`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 10.1 MB (10082896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f5141af0a2579801617b6ef53cc8da747d109de43e1b88c92ba151618c1c12`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7efe871fc37a59627f7fb75e2cd481a361e23ae4423cbd5c60ebfd9cfc40ce4`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 5.4 MB (5405651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:703020e7529818ace6da7d3f3424df173c4f428cf3fdaadb5bfb9d5a806ea431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.8 KB (990826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168cdfdbfc8e0c3b5a619ac19b836bbfce7a1baa6ab36ceaeb816e42d0073b3f`

```dockerfile
```

-	Layers:
	-	`sha256:a2f8050d7c3f109cc73636ae770c90e2cde71f2ed0dcd93078524351667493a8`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 973.4 KB (973394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304d7cd47112bf0ace221c02f2bdff3de634bfada70e48aad5065bc3c7424e87`  
		Last Modified: Sun, 28 Jan 2024 09:20:59 GMT  
		Size: 17.4 KB (17432 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1-bookworm`

```console
$ docker pull irssi@sha256:df2314e3c83d5dd353eafa769eee4302e869ca2782ba3906a63beb9c1e45d88b
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
$ docker pull irssi@sha256:f348397f4e94c8233af74fdea9b0e212e59940476974ab34d100894496547bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75868792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ba45dda22d90fa5e9e29f44f3c9db5d8f7ef6ab9a565f15845b3fc25c70ca2`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
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
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c80471fc9f279ecbb940d938880d5d417992f34809cffcc35de55e5c5b7b50`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 18.3 MB (18267918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2fe054dac6c8448486f7f83fb8d9a935f49600d14786eb028d05f1aca7be4d`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0c8cbf7b0f50debae5d2c4db813db40ef72d3f463d35255151d01f443c8f3b`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 28.5 MB (28473427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:0b4f3f615631a2195ca922bb269cc41ce0094ca6b506c2a6f42972e0edb4bb85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6635471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5bdb10eee477ea82a96d9db1c1a6ba2b86d46b4a80e1a99fc3067f614e5ead`

```dockerfile
```

-	Layers:
	-	`sha256:ad8396ba1d7eb23f85a9f1aa776ff1736aa74a41840bdb1336c90e8b0502ebd8`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 6.6 MB (6616868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97019d8cfce10dc023be567084137669d8fb7772cec7218f1e711f4cfae562dc`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 18.6 KB (18603 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:87ad7b222f94bd4ffeda78eb7cf201ac297f22792db2eb6c627342cd68e91c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69868386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df3cfc1c8fffefd348cacfe8d18c9367e7b15f4227b2b32750bba9a1dad4eba`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:557a5348da1e680593a9ba709ef059b96baf15e0c89d8f8343e97bf008d9dc05 in / 
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
	-	`sha256:b508f3272b9b70b8dd19c621a4da1be63880a1f6412063787647ceeb464d772a`  
		Last Modified: Wed, 31 Jan 2024 22:48:00 GMT  
		Size: 26.9 MB (26909323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5389309a8aec1769eaeaa29319de4bebf1627abb4b7c25ceaef27190cd064cfc`  
		Last Modified: Thu, 01 Feb 2024 12:00:33 GMT  
		Size: 16.8 MB (16840201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31b408b37e2ea86da1e5dbb066b4b3fb5d09551561012dec426720879e0ebee`  
		Last Modified: Thu, 01 Feb 2024 12:00:32 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3f755d015144784b5213f297ec37d52ddb303651246f90287675b59fdb928e`  
		Last Modified: Thu, 01 Feb 2024 12:00:34 GMT  
		Size: 26.1 MB (26115505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:10fa924814f0100863a02d43cde888366c56bb1999d35f4ec2cb5458ede1d8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6608604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005c1e6b2319f0434d5ccdc6f83cedaf5c4931041228a3b257bf9d9d5fb2e4c2`

```dockerfile
```

-	Layers:
	-	`sha256:f0eebab35555f3e7c0ebb7213ba7f2f39f5d2117387aec58252ad62f3578ad40`  
		Last Modified: Thu, 01 Feb 2024 12:00:33 GMT  
		Size: 6.6 MB (6590040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32bd71fd61ddf99b170b9b0785a26c0ee132d0d4f5715fac60a135b66c6200a2`  
		Last Modified: Thu, 01 Feb 2024 12:00:32 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:acbb7bca937bcbdadea02ea51bd199c2c3cb20c4710043cabbf16dcbc82ec971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66192097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9882134ca1726fbcba90c8ffa149ba970b02f9ca5f6f67952d386a590416acb3`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
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
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710b5644e8d7ce9b22f8100f04ed12089274d8e6ecaa7b281e784390d9a624b7`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 16.4 MB (16432998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c9b75f1d3fb010ce226691f08e04e0eca369822f016344e74c988e7ff9cbd8`  
		Last Modified: Sat, 03 Feb 2024 11:14:04 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4b63d99a8fee13ec791237ca413916d8e6c7533abae83274d4674c855395`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 25.0 MB (25014178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:5741bec69a3a0a56fa45545bb9325a960c1706d417f5c2d6739b28b865f70c2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6609678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e40dd73c96b2bc78fa4fc0bc3ebf1c7edb34aeb93676b09737429a7b8d753b0`

```dockerfile
```

-	Layers:
	-	`sha256:72cf1412c4556bb0f02816b52887305bbd5ebccd80827e0404367c869478d2ed`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 6.6 MB (6591114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64c76402e6b60447a3e1c01a7d118cb99869ea18b5b76ebe57796f09cf7cea62`  
		Last Modified: Sat, 03 Feb 2024 11:14:04 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:ab01c34a30c278373d07d580043e8a18e72fdaedef7dda4a42dc222f7b997295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74448713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6936425758539b2ebe94594f0f57669ce6f225b3fda544a7169b3a8c918fcf70`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
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
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3ca413b8af66fc07e47a491183e81f2d8418a36f4b96f3bdf10c96382787ee`  
		Last Modified: Thu, 01 Feb 2024 15:38:27 GMT  
		Size: 17.8 MB (17832825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f66dbcdfcc246d829efadc3627c1885169a547fd80fcef2f9f380ffb2cbc82a`  
		Last Modified: Thu, 01 Feb 2024 15:38:26 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0c68f2c78a25389c67e4236b05e25abf97345db7813892b2d0e8f00ef530db`  
		Last Modified: Thu, 01 Feb 2024 15:38:28 GMT  
		Size: 27.4 MB (27431697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9b2ce4726f911cecf3cdc2ce92874aa0c7a1d9991a3be9a1fdb8488f3507b3d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6615993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d78c2cfaac7640d2fba3d28b916ab8c140371df8abe66975d35d9d5a224e724`

```dockerfile
```

-	Layers:
	-	`sha256:88a3436d2dc5f0b5a747fedf9b08fd46e9fa64aa7be78c7dc416e4ec9fc043fa`  
		Last Modified: Thu, 01 Feb 2024 15:38:31 GMT  
		Size: 6.6 MB (6597539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:174c63d7fedd1ff225033ff0e20a26b24492ce336185f5f0c5ca8a39e2e2b217`  
		Last Modified: Thu, 01 Feb 2024 15:38:27 GMT  
		Size: 18.5 KB (18454 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:766da4d0c23a6b5a02fcfe6a9c290de6c880f481723bd162ec357b72a4b47a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76119263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6e2b48aea52eb23e814469cc9fee45495df60d11dcfcf7136304f394069c00`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:540e2de73452bd162dd7f630bf29f60e7d2e4a7a5d32a495bedf8ad390b59d7f in / 
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
	-	`sha256:34ef135b45f33052e8e5bca668f9a45a938944a9cf3fb73a46f54a7bf11f091b`  
		Last Modified: Wed, 31 Jan 2024 22:43:46 GMT  
		Size: 30.2 MB (30165018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dbf5ba1aef114655d4178cb7b25fc40be6cbbc4e74271ef3c0d129f27f7948`  
		Last Modified: Wed, 31 Jan 2024 23:55:35 GMT  
		Size: 17.6 MB (17592714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5c8ab8d6a9d2481fb1e6c046eda1e5bebc72c7171390e7918bbf3230a3a722`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f0f14697a5f1c37fedc3b6d79441454aa012edc2c624b113dab83f6ae387fe`  
		Last Modified: Wed, 31 Jan 2024 23:55:35 GMT  
		Size: 28.4 MB (28358174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:209fdc2b901e8609cc13ee3d75d5ddc3ddc5a77eb48684669e38db4fecc4c502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5adccb9448d759136b20f5bdf9d17e7b24e77b7f9ab897d4f7e971f758f79bba`

```dockerfile
```

-	Layers:
	-	`sha256:d1c4277341c5a786dc08c35575a05e75f388d342d5a278a44d83c0c37d739506`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 6.6 MB (6609873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ee0cd483b9775bf82c5f73475a171139475368fc3052df090bfb26cafea30e`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:5b07d620f6e0a5a433dafa6289d75943fe3f50b878b31f3b50428e645a145462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73891556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec83415acb7aaf453c85c9fbf2dcb484813439e60106ce3678051032190e571b`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
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
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0542ca44f4608abe3eb8928a6679f1310a135de5d26dcaef75fdfc7158cb3ea`  
		Last Modified: Thu, 01 Feb 2024 20:14:13 GMT  
		Size: 16.7 MB (16739448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5445b96f290754cc47514654bf406c8cf27af72cafe3c07122d2319baeab5c6`  
		Last Modified: Thu, 01 Feb 2024 20:14:11 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c99cf776ed9d9e58bad7c58c6a56f0e52654611186998435beea42f692d00d`  
		Last Modified: Thu, 01 Feb 2024 20:14:14 GMT  
		Size: 28.0 MB (28006308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:2374bfe0c2ed5ac9aa6c56cbcd7c04c3173332bc39faa38c57a475b929a9b702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2339be92d5d786c3309d29bedbceefe69adad7b0444bd27b86f0b90776e9a30`

```dockerfile
```

-	Layers:
	-	`sha256:28e3d51004b87049273ec1ea39d8930a3cfdd6cc05b2194a9e96b65bca71c335`  
		Last Modified: Thu, 01 Feb 2024 20:14:11 GMT  
		Size: 18.3 KB (18320 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:99fee1cd7190e2738316eca944f9cb4474388bdcdff44d4e7492808c79c1838a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81689464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a168acd494049e622c9716bfe5c16cc1c017bea4033b8fe102da9b3f41c70dc`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:fca8b919a8d1e36420dd1e3f3e427aaaae28a2f57e46c27207acd8e3df0d7a97 in / 
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
	-	`sha256:dfeacd5cd8171f4516ea86dadfb60a372eabf49428dc23d2efdda68cff5b05e7`  
		Last Modified: Wed, 31 Jan 2024 22:34:24 GMT  
		Size: 33.1 MB (33142917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a3bd8096c05f1674995eeb051e3cdf023bbca5505b3f75e624f37c5b13e1b3`  
		Last Modified: Thu, 01 Feb 2024 12:57:44 GMT  
		Size: 18.6 MB (18565973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c5b4610ff6d9b857d7b8bcbc7a90224f918f31c45540cb15c1625a86bf95bc`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcf5f7f76af69ab342a135aed7b0fe5dab9ec932f2bcaeeb58cf8e9491096cb`  
		Last Modified: Thu, 01 Feb 2024 12:57:44 GMT  
		Size: 30.0 MB (29977216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:e5e62f13b43055d9255623225d660999c6209f6cbc9413307aaea737b381644f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6627686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bceb9b0ed2cbb811589e573c40c51eef92a381ce1039e4c4a81f5bfef5f2d0db`

```dockerfile
```

-	Layers:
	-	`sha256:5faeac8a64644b64f37809aa623f431a2453aa3dc443ad2173158318e03ae6ec`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 6.6 MB (6609185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f23996cea2f94cdfa72579bfbb5a59af44283d6b74f21f3d83612614d8698f3`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:3be6d24893ec88d5484e2c6ff47dabe648e0c56d532619254ec2005f79b316f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72553121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eeb87370bfa6742ae5cdffe4e9e5fbcded5a376ea20cb9f0ff781310654cff`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
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
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4594bbef0c3ed6e5d274cc97e215f696416fa4ae17044dfd8fe130e789bbc1`  
		Last Modified: Tue, 06 Feb 2024 11:27:01 GMT  
		Size: 18.0 MB (18014343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb84559c99fdfcc14828d4d1d39640bc61b21c99711be784b356d5c32b0fc8a7`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f15c7c91a157b6cb1adb4e9eff1265e940d9ae9d78fa1d5396c6d03f14b7e6e`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 27.0 MB (27021938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:2c98314fd3cf3cdcc7aca67a7f251b24cb5c0f597abe52b639fda52f8631094b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6624174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1856fea1ea1713d5b1fe2b0ff097f7d0a688d0bd16c23f7de87310eb9f37a7a8`

```dockerfile
```

-	Layers:
	-	`sha256:e65ba0bc6f82ed76a16bdbe6b6618f3835b881b23d55dbc63e573dc31c537b19`  
		Last Modified: Tue, 06 Feb 2024 11:27:01 GMT  
		Size: 6.6 MB (6605739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01339a4362670ca4baef375e49a866c7339d89de67789528e853a5a62dd0a787`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 18.4 KB (18435 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4`

```console
$ docker pull irssi@sha256:df2314e3c83d5dd353eafa769eee4302e869ca2782ba3906a63beb9c1e45d88b
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

### `irssi:1.4` - linux; amd64

```console
$ docker pull irssi@sha256:f348397f4e94c8233af74fdea9b0e212e59940476974ab34d100894496547bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75868792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ba45dda22d90fa5e9e29f44f3c9db5d8f7ef6ab9a565f15845b3fc25c70ca2`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
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
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c80471fc9f279ecbb940d938880d5d417992f34809cffcc35de55e5c5b7b50`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 18.3 MB (18267918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2fe054dac6c8448486f7f83fb8d9a935f49600d14786eb028d05f1aca7be4d`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0c8cbf7b0f50debae5d2c4db813db40ef72d3f463d35255151d01f443c8f3b`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 28.5 MB (28473427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:0b4f3f615631a2195ca922bb269cc41ce0094ca6b506c2a6f42972e0edb4bb85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6635471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5bdb10eee477ea82a96d9db1c1a6ba2b86d46b4a80e1a99fc3067f614e5ead`

```dockerfile
```

-	Layers:
	-	`sha256:ad8396ba1d7eb23f85a9f1aa776ff1736aa74a41840bdb1336c90e8b0502ebd8`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 6.6 MB (6616868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97019d8cfce10dc023be567084137669d8fb7772cec7218f1e711f4cfae562dc`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 18.6 KB (18603 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v5

```console
$ docker pull irssi@sha256:87ad7b222f94bd4ffeda78eb7cf201ac297f22792db2eb6c627342cd68e91c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69868386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df3cfc1c8fffefd348cacfe8d18c9367e7b15f4227b2b32750bba9a1dad4eba`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:557a5348da1e680593a9ba709ef059b96baf15e0c89d8f8343e97bf008d9dc05 in / 
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
	-	`sha256:b508f3272b9b70b8dd19c621a4da1be63880a1f6412063787647ceeb464d772a`  
		Last Modified: Wed, 31 Jan 2024 22:48:00 GMT  
		Size: 26.9 MB (26909323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5389309a8aec1769eaeaa29319de4bebf1627abb4b7c25ceaef27190cd064cfc`  
		Last Modified: Thu, 01 Feb 2024 12:00:33 GMT  
		Size: 16.8 MB (16840201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31b408b37e2ea86da1e5dbb066b4b3fb5d09551561012dec426720879e0ebee`  
		Last Modified: Thu, 01 Feb 2024 12:00:32 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3f755d015144784b5213f297ec37d52ddb303651246f90287675b59fdb928e`  
		Last Modified: Thu, 01 Feb 2024 12:00:34 GMT  
		Size: 26.1 MB (26115505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:10fa924814f0100863a02d43cde888366c56bb1999d35f4ec2cb5458ede1d8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6608604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005c1e6b2319f0434d5ccdc6f83cedaf5c4931041228a3b257bf9d9d5fb2e4c2`

```dockerfile
```

-	Layers:
	-	`sha256:f0eebab35555f3e7c0ebb7213ba7f2f39f5d2117387aec58252ad62f3578ad40`  
		Last Modified: Thu, 01 Feb 2024 12:00:33 GMT  
		Size: 6.6 MB (6590040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32bd71fd61ddf99b170b9b0785a26c0ee132d0d4f5715fac60a135b66c6200a2`  
		Last Modified: Thu, 01 Feb 2024 12:00:32 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm variant v7

```console
$ docker pull irssi@sha256:acbb7bca937bcbdadea02ea51bd199c2c3cb20c4710043cabbf16dcbc82ec971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66192097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9882134ca1726fbcba90c8ffa149ba970b02f9ca5f6f67952d386a590416acb3`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
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
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710b5644e8d7ce9b22f8100f04ed12089274d8e6ecaa7b281e784390d9a624b7`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 16.4 MB (16432998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c9b75f1d3fb010ce226691f08e04e0eca369822f016344e74c988e7ff9cbd8`  
		Last Modified: Sat, 03 Feb 2024 11:14:04 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4b63d99a8fee13ec791237ca413916d8e6c7533abae83274d4674c855395`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 25.0 MB (25014178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:5741bec69a3a0a56fa45545bb9325a960c1706d417f5c2d6739b28b865f70c2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6609678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e40dd73c96b2bc78fa4fc0bc3ebf1c7edb34aeb93676b09737429a7b8d753b0`

```dockerfile
```

-	Layers:
	-	`sha256:72cf1412c4556bb0f02816b52887305bbd5ebccd80827e0404367c869478d2ed`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 6.6 MB (6591114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64c76402e6b60447a3e1c01a7d118cb99869ea18b5b76ebe57796f09cf7cea62`  
		Last Modified: Sat, 03 Feb 2024 11:14:04 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:ab01c34a30c278373d07d580043e8a18e72fdaedef7dda4a42dc222f7b997295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74448713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6936425758539b2ebe94594f0f57669ce6f225b3fda544a7169b3a8c918fcf70`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
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
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3ca413b8af66fc07e47a491183e81f2d8418a36f4b96f3bdf10c96382787ee`  
		Last Modified: Thu, 01 Feb 2024 15:38:27 GMT  
		Size: 17.8 MB (17832825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f66dbcdfcc246d829efadc3627c1885169a547fd80fcef2f9f380ffb2cbc82a`  
		Last Modified: Thu, 01 Feb 2024 15:38:26 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0c68f2c78a25389c67e4236b05e25abf97345db7813892b2d0e8f00ef530db`  
		Last Modified: Thu, 01 Feb 2024 15:38:28 GMT  
		Size: 27.4 MB (27431697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:9b2ce4726f911cecf3cdc2ce92874aa0c7a1d9991a3be9a1fdb8488f3507b3d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6615993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d78c2cfaac7640d2fba3d28b916ab8c140371df8abe66975d35d9d5a224e724`

```dockerfile
```

-	Layers:
	-	`sha256:88a3436d2dc5f0b5a747fedf9b08fd46e9fa64aa7be78c7dc416e4ec9fc043fa`  
		Last Modified: Thu, 01 Feb 2024 15:38:31 GMT  
		Size: 6.6 MB (6597539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:174c63d7fedd1ff225033ff0e20a26b24492ce336185f5f0c5ca8a39e2e2b217`  
		Last Modified: Thu, 01 Feb 2024 15:38:27 GMT  
		Size: 18.5 KB (18454 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; 386

```console
$ docker pull irssi@sha256:766da4d0c23a6b5a02fcfe6a9c290de6c880f481723bd162ec357b72a4b47a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76119263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6e2b48aea52eb23e814469cc9fee45495df60d11dcfcf7136304f394069c00`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:540e2de73452bd162dd7f630bf29f60e7d2e4a7a5d32a495bedf8ad390b59d7f in / 
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
	-	`sha256:34ef135b45f33052e8e5bca668f9a45a938944a9cf3fb73a46f54a7bf11f091b`  
		Last Modified: Wed, 31 Jan 2024 22:43:46 GMT  
		Size: 30.2 MB (30165018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dbf5ba1aef114655d4178cb7b25fc40be6cbbc4e74271ef3c0d129f27f7948`  
		Last Modified: Wed, 31 Jan 2024 23:55:35 GMT  
		Size: 17.6 MB (17592714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5c8ab8d6a9d2481fb1e6c046eda1e5bebc72c7171390e7918bbf3230a3a722`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f0f14697a5f1c37fedc3b6d79441454aa012edc2c624b113dab83f6ae387fe`  
		Last Modified: Wed, 31 Jan 2024 23:55:35 GMT  
		Size: 28.4 MB (28358174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:209fdc2b901e8609cc13ee3d75d5ddc3ddc5a77eb48684669e38db4fecc4c502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5adccb9448d759136b20f5bdf9d17e7b24e77b7f9ab897d4f7e971f758f79bba`

```dockerfile
```

-	Layers:
	-	`sha256:d1c4277341c5a786dc08c35575a05e75f388d342d5a278a44d83c0c37d739506`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 6.6 MB (6609873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ee0cd483b9775bf82c5f73475a171139475368fc3052df090bfb26cafea30e`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; mips64le

```console
$ docker pull irssi@sha256:5b07d620f6e0a5a433dafa6289d75943fe3f50b878b31f3b50428e645a145462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73891556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec83415acb7aaf453c85c9fbf2dcb484813439e60106ce3678051032190e571b`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
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
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0542ca44f4608abe3eb8928a6679f1310a135de5d26dcaef75fdfc7158cb3ea`  
		Last Modified: Thu, 01 Feb 2024 20:14:13 GMT  
		Size: 16.7 MB (16739448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5445b96f290754cc47514654bf406c8cf27af72cafe3c07122d2319baeab5c6`  
		Last Modified: Thu, 01 Feb 2024 20:14:11 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c99cf776ed9d9e58bad7c58c6a56f0e52654611186998435beea42f692d00d`  
		Last Modified: Thu, 01 Feb 2024 20:14:14 GMT  
		Size: 28.0 MB (28006308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:2374bfe0c2ed5ac9aa6c56cbcd7c04c3173332bc39faa38c57a475b929a9b702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2339be92d5d786c3309d29bedbceefe69adad7b0444bd27b86f0b90776e9a30`

```dockerfile
```

-	Layers:
	-	`sha256:28e3d51004b87049273ec1ea39d8930a3cfdd6cc05b2194a9e96b65bca71c335`  
		Last Modified: Thu, 01 Feb 2024 20:14:11 GMT  
		Size: 18.3 KB (18320 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; ppc64le

```console
$ docker pull irssi@sha256:99fee1cd7190e2738316eca944f9cb4474388bdcdff44d4e7492808c79c1838a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81689464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a168acd494049e622c9716bfe5c16cc1c017bea4033b8fe102da9b3f41c70dc`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:fca8b919a8d1e36420dd1e3f3e427aaaae28a2f57e46c27207acd8e3df0d7a97 in / 
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
	-	`sha256:dfeacd5cd8171f4516ea86dadfb60a372eabf49428dc23d2efdda68cff5b05e7`  
		Last Modified: Wed, 31 Jan 2024 22:34:24 GMT  
		Size: 33.1 MB (33142917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a3bd8096c05f1674995eeb051e3cdf023bbca5505b3f75e624f37c5b13e1b3`  
		Last Modified: Thu, 01 Feb 2024 12:57:44 GMT  
		Size: 18.6 MB (18565973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c5b4610ff6d9b857d7b8bcbc7a90224f918f31c45540cb15c1625a86bf95bc`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcf5f7f76af69ab342a135aed7b0fe5dab9ec932f2bcaeeb58cf8e9491096cb`  
		Last Modified: Thu, 01 Feb 2024 12:57:44 GMT  
		Size: 30.0 MB (29977216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:e5e62f13b43055d9255623225d660999c6209f6cbc9413307aaea737b381644f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6627686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bceb9b0ed2cbb811589e573c40c51eef92a381ce1039e4c4a81f5bfef5f2d0db`

```dockerfile
```

-	Layers:
	-	`sha256:5faeac8a64644b64f37809aa623f431a2453aa3dc443ad2173158318e03ae6ec`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 6.6 MB (6609185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f23996cea2f94cdfa72579bfbb5a59af44283d6b74f21f3d83612614d8698f3`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4` - linux; s390x

```console
$ docker pull irssi@sha256:3be6d24893ec88d5484e2c6ff47dabe648e0c56d532619254ec2005f79b316f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72553121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eeb87370bfa6742ae5cdffe4e9e5fbcded5a376ea20cb9f0ff781310654cff`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
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
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4594bbef0c3ed6e5d274cc97e215f696416fa4ae17044dfd8fe130e789bbc1`  
		Last Modified: Tue, 06 Feb 2024 11:27:01 GMT  
		Size: 18.0 MB (18014343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb84559c99fdfcc14828d4d1d39640bc61b21c99711be784b356d5c32b0fc8a7`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f15c7c91a157b6cb1adb4e9eff1265e940d9ae9d78fa1d5396c6d03f14b7e6e`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 27.0 MB (27021938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4` - unknown; unknown

```console
$ docker pull irssi@sha256:2c98314fd3cf3cdcc7aca67a7f251b24cb5c0f597abe52b639fda52f8631094b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6624174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1856fea1ea1713d5b1fe2b0ff097f7d0a688d0bd16c23f7de87310eb9f37a7a8`

```dockerfile
```

-	Layers:
	-	`sha256:e65ba0bc6f82ed76a16bdbe6b6618f3835b881b23d55dbc63e573dc31c537b19`  
		Last Modified: Tue, 06 Feb 2024 11:27:01 GMT  
		Size: 6.6 MB (6605739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01339a4362670ca4baef375e49a866c7339d89de67789528e853a5a62dd0a787`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 18.4 KB (18435 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine`

```console
$ docker pull irssi@sha256:294a5ddd1a7991782f7df46f7f0b1ef870818a1cf3a9afc37399222c27fa95cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1.4-alpine` - linux; amd64

```console
$ docker pull irssi@sha256:ef6c7693f4591e49ec7ebb9d9e3ff118d31da2e6e989cc01d7c4ba68d6ab312e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18451473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33d0b6133f016daecdc32847e2719e1b8377593ca3a157e4e2182ec699b3619`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d5073c9dc162f6d73c33561ca62b1f3d4afe73e51dfe01bc3bdbe570603526`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 9.6 MB (9645490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaa94b168ed27385c169187548faa3944812324045e5b7d4f9fa0141d934de7`  
		Last Modified: Sat, 27 Jan 2024 00:53:19 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33ada92546b652616e31a208091cb77dc65019c90e5944f396554ea13e63472`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 5.4 MB (5402150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d7192c220068161f91626a3d88eb71585cea3908b88e32bc9d7a200ba73e04f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.5 KB (992458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e03dcb09479e1e99b8f120055916a32994d838a16cdeba603eb3779a35bdb3`

```dockerfile
```

-	Layers:
	-	`sha256:2d6761df79ddf9480ea4aa104a72a140a5347d5dea19b3eb975a78d2a144483b`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 975.0 KB (975030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f3ba2fd4c9e25b6b8c3ce87fda3494b8506f3cebb1bc0e371df70b3a1c44a87`  
		Last Modified: Sat, 27 Jan 2024 00:53:19 GMT  
		Size: 17.4 KB (17428 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:11cdd850f01f7020ea3dc559a1cacf1710ce7e1110b2b3be3d5088a753388e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980aff2e9d7fdabd52ca418744d9e75a16f305953ff369624a6f3e91ee563444`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1caa0b93da06dd2aa46cce7a3fd9bbc4b0b58ff19b6dee6450b493cb819f9cd`  
		Last Modified: Tue, 30 Jan 2024 18:54:03 GMT  
		Size: 8.9 MB (8880054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93390793c8d561bd6d0fed103d923be9845e322d71b5187396645909aee925df`  
		Last Modified: Tue, 30 Jan 2024 18:54:02 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db82a85a709f0d1d93b2c72989821c461582c5c99c841cb1d8529c32826084d`  
		Last Modified: Tue, 30 Jan 2024 18:54:03 GMT  
		Size: 5.2 MB (5242167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:bd1dc317b136af3a211fed01816891cbea3e545a66d52fec0a8cfe3c9ae9a9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 KB (17341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af05cb00d364bd5dc1c1184bb77489a40ba8096333fcb8ad4b6969822a45b3ac`

```dockerfile
```

-	Layers:
	-	`sha256:7a7a2bdaf6762372aa21871c515a18d90c4cfa782df359a7f10dcafb1a8acbcf`  
		Last Modified: Tue, 30 Jan 2024 18:54:02 GMT  
		Size: 17.3 KB (17341 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:89e22268640c72b2ae0efb98e009b34bd5534ad6c4aa596df74bfd27c1775e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16630432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9bff58300e84d8932cb47d4638ebdafbd9eb55888c2cfe35e7c89ce11cacec`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a728625b39c4526fc00d553e9ad76abf2d838e770db539a4503401b8151b7`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 8.7 MB (8721243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80dec7634cb6fd64dad041788335bf81e0374c155777e94d292608fadbc918e3`  
		Last Modified: Sat, 27 Jan 2024 16:10:09 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a274dbd32034295ddcbc1067913cee45ae78dfd48bcfa5a5a0227438b251e6c`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 5.0 MB (5006505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:81909a4824efd52f673139f1bfce8946affddffd9073b10d3429fc7e6a25b6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **995.1 KB (995130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f8bf5414c3b8dabe31b6645b897840a59666ed989623f0fa633e51cd171a51`

```dockerfile
```

-	Layers:
	-	`sha256:788b342a7afe442fa8cc36f28d56399fe0b0abcded67366d9cfc6f4414ec6b28`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 977.6 KB (977574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af9e565fad9e84cc85a9eb745382b7350da37e969b74d2723023407a1dc827b`  
		Last Modified: Sat, 27 Jan 2024 16:10:09 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f967a5aba07f362a1fc42968dc5c25d932ddf7c5afc29b87f3e103f41e11b3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b852dcd533ac6fef70eee55ddc2eb8cd1a1a2438f10c7fb9780fcc8f8c53ae7`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427b55bea52be9d140397d36bdf44940754b11f701ab1c8860bf265108864474`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 9.7 MB (9672879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3172290de02d764723938f6bbf53611e992dca7775d89910602a51d4fdc12c0c`  
		Last Modified: Sat, 27 Jan 2024 20:28:06 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4046f82759ffd91ca630dba178059b2985f3ec4fb9cb5a8d928a59215b0b5b2`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 5.3 MB (5308548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b68051a5d753ec8037cd2f9d14313c65e2bf5d4c67f564eec3f3f58eb4a131b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.5 KB (992495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edf1b50c168b27a6f3a5f6a4b2a2711df8f7bd7bbfdc93ea5eef3a8861c5e0c`

```dockerfile
```

-	Layers:
	-	`sha256:f636b4606a093b4d77ac5276a6d5402ca1ff4b0641b2656d45bb27ff2ed683af`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 975.0 KB (975049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0aae570a126a40b9525d270285ba0d643a33c387a1f9f79698263d38a935f73`  
		Last Modified: Sat, 27 Jan 2024 20:28:06 GMT  
		Size: 17.4 KB (17446 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; 386

```console
$ docker pull irssi@sha256:387d4dc6384ebea47ed5276a5865acb546bb67dfc227fe393dc75db5d45852dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17557817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e96759752775aacd2fda0f53e8cf266fc1c7b3e068566a8fc8c2add735f586`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8086f06106cd7bdd94cddf1c7363b144b801cd672997d9fe81ed6ab8ae03891`  
		Last Modified: Sat, 27 Jan 2024 01:54:00 GMT  
		Size: 8.9 MB (8904430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d1dba1f614043dea1e85138edb339caa7e16cca6c013e81384bd9f7f1afe02`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a341596e873d51872b196d8782ad7c32261c5a181b99f1f2d4c8c053a35a752a`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 5.4 MB (5413031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d7e896f39991af1e19a5fea9c4353550ddd15bbb4fa05afc17e02656c66c8104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.4 KB (992360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617babf31d74046af9500e49f9674cbad6f479da89ac7b7cb51ba62e91a8f83a`

```dockerfile
```

-	Layers:
	-	`sha256:b11bca7efa15aa00afe306253a110a6805f8d56ebdfb10ff646a51e2a4f69f81`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 975.0 KB (974985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4a8d0da397b1dded79f569fffc3082addee92a84c9f41f986ef310c44a72bf8`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 17.4 KB (17375 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:a0a400f2133847c9bbfa653f898fc72042aac4b03cb1371156d8726812131313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18717231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0def155df329eeefa5360cf54f1657dc7731e2f631182fce7e96924a4cabb8`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc74fa4ba26fc8c0460833da6460f59a2b7fdb551209793e9177aa8e4f59346c`  
		Last Modified: Sat, 27 Jan 2024 09:47:30 GMT  
		Size: 9.7 MB (9736547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596eae301f8ffae57ffc8c11b668ca24b994f12d9935de6216884db8f13188d3`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65ab57b806e5436452de1e909990c85bf46bb183048518a40b3e91cceaa914d`  
		Last Modified: Sat, 27 Jan 2024 09:47:30 GMT  
		Size: 5.6 MB (5630906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c822cd405d36a575a6a510133bbc7870de59eabfd7fc4a2bb9485e127fa82363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.9 KB (990946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00c5eb1975042e0f47315f4ba48ed6fe69fbb8e39eb0c845ac7edf8cea9bc47`

```dockerfile
```

-	Layers:
	-	`sha256:51daf79105767963a7bfa2160a6d94beb71eecf88329550e2f9150d944fc2a52`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 973.5 KB (973452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6afd3a59a575c01cda08047a63543de5e7a3b3293e87e18e1bb870d4a2df4e74`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 17.5 KB (17494 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:cb11647a91b30743f090d9c0e26aeb8ac9ad300c50b661af12505ae290befd40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18707370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891ea14f0ba63e76c3bf45e2ede5b212af9d872f0b77a89d369fed7f2d5bfd3a`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc77a74801be7299707a33e8a653a76c9c5b8d7289fad0e44f86f0eb950c0dfb`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 10.1 MB (10082896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f5141af0a2579801617b6ef53cc8da747d109de43e1b88c92ba151618c1c12`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7efe871fc37a59627f7fb75e2cd481a361e23ae4423cbd5c60ebfd9cfc40ce4`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 5.4 MB (5405651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:703020e7529818ace6da7d3f3424df173c4f428cf3fdaadb5bfb9d5a806ea431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.8 KB (990826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168cdfdbfc8e0c3b5a619ac19b836bbfce7a1baa6ab36ceaeb816e42d0073b3f`

```dockerfile
```

-	Layers:
	-	`sha256:a2f8050d7c3f109cc73636ae770c90e2cde71f2ed0dcd93078524351667493a8`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 973.4 KB (973394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304d7cd47112bf0ace221c02f2bdff3de634bfada70e48aad5065bc3c7424e87`  
		Last Modified: Sun, 28 Jan 2024 09:20:59 GMT  
		Size: 17.4 KB (17432 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-alpine3.18`

```console
$ docker pull irssi@sha256:294a5ddd1a7991782f7df46f7f0b1ef870818a1cf3a9afc37399222c27fa95cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1.4-alpine3.18` - linux; amd64

```console
$ docker pull irssi@sha256:ef6c7693f4591e49ec7ebb9d9e3ff118d31da2e6e989cc01d7c4ba68d6ab312e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18451473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33d0b6133f016daecdc32847e2719e1b8377593ca3a157e4e2182ec699b3619`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d5073c9dc162f6d73c33561ca62b1f3d4afe73e51dfe01bc3bdbe570603526`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 9.6 MB (9645490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaa94b168ed27385c169187548faa3944812324045e5b7d4f9fa0141d934de7`  
		Last Modified: Sat, 27 Jan 2024 00:53:19 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33ada92546b652616e31a208091cb77dc65019c90e5944f396554ea13e63472`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 5.4 MB (5402150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:d7192c220068161f91626a3d88eb71585cea3908b88e32bc9d7a200ba73e04f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.5 KB (992458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e03dcb09479e1e99b8f120055916a32994d838a16cdeba603eb3779a35bdb3`

```dockerfile
```

-	Layers:
	-	`sha256:2d6761df79ddf9480ea4aa104a72a140a5347d5dea19b3eb975a78d2a144483b`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 975.0 KB (975030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f3ba2fd4c9e25b6b8c3ce87fda3494b8506f3cebb1bc0e371df70b3a1c44a87`  
		Last Modified: Sat, 27 Jan 2024 00:53:19 GMT  
		Size: 17.4 KB (17428 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.18` - linux; arm variant v6

```console
$ docker pull irssi@sha256:11cdd850f01f7020ea3dc559a1cacf1710ce7e1110b2b3be3d5088a753388e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980aff2e9d7fdabd52ca418744d9e75a16f305953ff369624a6f3e91ee563444`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1caa0b93da06dd2aa46cce7a3fd9bbc4b0b58ff19b6dee6450b493cb819f9cd`  
		Last Modified: Tue, 30 Jan 2024 18:54:03 GMT  
		Size: 8.9 MB (8880054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93390793c8d561bd6d0fed103d923be9845e322d71b5187396645909aee925df`  
		Last Modified: Tue, 30 Jan 2024 18:54:02 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db82a85a709f0d1d93b2c72989821c461582c5c99c841cb1d8529c32826084d`  
		Last Modified: Tue, 30 Jan 2024 18:54:03 GMT  
		Size: 5.2 MB (5242167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:bd1dc317b136af3a211fed01816891cbea3e545a66d52fec0a8cfe3c9ae9a9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 KB (17341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af05cb00d364bd5dc1c1184bb77489a40ba8096333fcb8ad4b6969822a45b3ac`

```dockerfile
```

-	Layers:
	-	`sha256:7a7a2bdaf6762372aa21871c515a18d90c4cfa782df359a7f10dcafb1a8acbcf`  
		Last Modified: Tue, 30 Jan 2024 18:54:02 GMT  
		Size: 17.3 KB (17341 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.18` - linux; arm variant v7

```console
$ docker pull irssi@sha256:89e22268640c72b2ae0efb98e009b34bd5534ad6c4aa596df74bfd27c1775e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16630432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9bff58300e84d8932cb47d4638ebdafbd9eb55888c2cfe35e7c89ce11cacec`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a728625b39c4526fc00d553e9ad76abf2d838e770db539a4503401b8151b7`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 8.7 MB (8721243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80dec7634cb6fd64dad041788335bf81e0374c155777e94d292608fadbc918e3`  
		Last Modified: Sat, 27 Jan 2024 16:10:09 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a274dbd32034295ddcbc1067913cee45ae78dfd48bcfa5a5a0227438b251e6c`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 5.0 MB (5006505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:81909a4824efd52f673139f1bfce8946affddffd9073b10d3429fc7e6a25b6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **995.1 KB (995130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f8bf5414c3b8dabe31b6645b897840a59666ed989623f0fa633e51cd171a51`

```dockerfile
```

-	Layers:
	-	`sha256:788b342a7afe442fa8cc36f28d56399fe0b0abcded67366d9cfc6f4414ec6b28`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 977.6 KB (977574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af9e565fad9e84cc85a9eb745382b7350da37e969b74d2723023407a1dc827b`  
		Last Modified: Sat, 27 Jan 2024 16:10:09 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f967a5aba07f362a1fc42968dc5c25d932ddf7c5afc29b87f3e103f41e11b3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b852dcd533ac6fef70eee55ddc2eb8cd1a1a2438f10c7fb9780fcc8f8c53ae7`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427b55bea52be9d140397d36bdf44940754b11f701ab1c8860bf265108864474`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 9.7 MB (9672879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3172290de02d764723938f6bbf53611e992dca7775d89910602a51d4fdc12c0c`  
		Last Modified: Sat, 27 Jan 2024 20:28:06 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4046f82759ffd91ca630dba178059b2985f3ec4fb9cb5a8d928a59215b0b5b2`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 5.3 MB (5308548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:b68051a5d753ec8037cd2f9d14313c65e2bf5d4c67f564eec3f3f58eb4a131b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.5 KB (992495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edf1b50c168b27a6f3a5f6a4b2a2711df8f7bd7bbfdc93ea5eef3a8861c5e0c`

```dockerfile
```

-	Layers:
	-	`sha256:f636b4606a093b4d77ac5276a6d5402ca1ff4b0641b2656d45bb27ff2ed683af`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 975.0 KB (975049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0aae570a126a40b9525d270285ba0d643a33c387a1f9f79698263d38a935f73`  
		Last Modified: Sat, 27 Jan 2024 20:28:06 GMT  
		Size: 17.4 KB (17446 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.18` - linux; 386

```console
$ docker pull irssi@sha256:387d4dc6384ebea47ed5276a5865acb546bb67dfc227fe393dc75db5d45852dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17557817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e96759752775aacd2fda0f53e8cf266fc1c7b3e068566a8fc8c2add735f586`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8086f06106cd7bdd94cddf1c7363b144b801cd672997d9fe81ed6ab8ae03891`  
		Last Modified: Sat, 27 Jan 2024 01:54:00 GMT  
		Size: 8.9 MB (8904430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d1dba1f614043dea1e85138edb339caa7e16cca6c013e81384bd9f7f1afe02`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a341596e873d51872b196d8782ad7c32261c5a181b99f1f2d4c8c053a35a752a`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 5.4 MB (5413031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:d7e896f39991af1e19a5fea9c4353550ddd15bbb4fa05afc17e02656c66c8104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.4 KB (992360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617babf31d74046af9500e49f9674cbad6f479da89ac7b7cb51ba62e91a8f83a`

```dockerfile
```

-	Layers:
	-	`sha256:b11bca7efa15aa00afe306253a110a6805f8d56ebdfb10ff646a51e2a4f69f81`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 975.0 KB (974985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4a8d0da397b1dded79f569fffc3082addee92a84c9f41f986ef310c44a72bf8`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 17.4 KB (17375 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.18` - linux; ppc64le

```console
$ docker pull irssi@sha256:a0a400f2133847c9bbfa653f898fc72042aac4b03cb1371156d8726812131313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18717231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0def155df329eeefa5360cf54f1657dc7731e2f631182fce7e96924a4cabb8`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc74fa4ba26fc8c0460833da6460f59a2b7fdb551209793e9177aa8e4f59346c`  
		Last Modified: Sat, 27 Jan 2024 09:47:30 GMT  
		Size: 9.7 MB (9736547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596eae301f8ffae57ffc8c11b668ca24b994f12d9935de6216884db8f13188d3`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65ab57b806e5436452de1e909990c85bf46bb183048518a40b3e91cceaa914d`  
		Last Modified: Sat, 27 Jan 2024 09:47:30 GMT  
		Size: 5.6 MB (5630906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:c822cd405d36a575a6a510133bbc7870de59eabfd7fc4a2bb9485e127fa82363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.9 KB (990946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00c5eb1975042e0f47315f4ba48ed6fe69fbb8e39eb0c845ac7edf8cea9bc47`

```dockerfile
```

-	Layers:
	-	`sha256:51daf79105767963a7bfa2160a6d94beb71eecf88329550e2f9150d944fc2a52`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 973.5 KB (973452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6afd3a59a575c01cda08047a63543de5e7a3b3293e87e18e1bb870d4a2df4e74`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 17.5 KB (17494 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-alpine3.18` - linux; s390x

```console
$ docker pull irssi@sha256:cb11647a91b30743f090d9c0e26aeb8ac9ad300c50b661af12505ae290befd40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18707370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891ea14f0ba63e76c3bf45e2ede5b212af9d872f0b77a89d369fed7f2d5bfd3a`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc77a74801be7299707a33e8a653a76c9c5b8d7289fad0e44f86f0eb950c0dfb`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 10.1 MB (10082896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f5141af0a2579801617b6ef53cc8da747d109de43e1b88c92ba151618c1c12`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7efe871fc37a59627f7fb75e2cd481a361e23ae4423cbd5c60ebfd9cfc40ce4`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 5.4 MB (5405651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:703020e7529818ace6da7d3f3424df173c4f428cf3fdaadb5bfb9d5a806ea431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.8 KB (990826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168cdfdbfc8e0c3b5a619ac19b836bbfce7a1baa6ab36ceaeb816e42d0073b3f`

```dockerfile
```

-	Layers:
	-	`sha256:a2f8050d7c3f109cc73636ae770c90e2cde71f2ed0dcd93078524351667493a8`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 973.4 KB (973394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304d7cd47112bf0ace221c02f2bdff3de634bfada70e48aad5065bc3c7424e87`  
		Last Modified: Sun, 28 Jan 2024 09:20:59 GMT  
		Size: 17.4 KB (17432 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4-bookworm`

```console
$ docker pull irssi@sha256:df2314e3c83d5dd353eafa769eee4302e869ca2782ba3906a63beb9c1e45d88b
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

### `irssi:1.4-bookworm` - linux; amd64

```console
$ docker pull irssi@sha256:f348397f4e94c8233af74fdea9b0e212e59940476974ab34d100894496547bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75868792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ba45dda22d90fa5e9e29f44f3c9db5d8f7ef6ab9a565f15845b3fc25c70ca2`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
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
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c80471fc9f279ecbb940d938880d5d417992f34809cffcc35de55e5c5b7b50`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 18.3 MB (18267918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2fe054dac6c8448486f7f83fb8d9a935f49600d14786eb028d05f1aca7be4d`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0c8cbf7b0f50debae5d2c4db813db40ef72d3f463d35255151d01f443c8f3b`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 28.5 MB (28473427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:0b4f3f615631a2195ca922bb269cc41ce0094ca6b506c2a6f42972e0edb4bb85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6635471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5bdb10eee477ea82a96d9db1c1a6ba2b86d46b4a80e1a99fc3067f614e5ead`

```dockerfile
```

-	Layers:
	-	`sha256:ad8396ba1d7eb23f85a9f1aa776ff1736aa74a41840bdb1336c90e8b0502ebd8`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 6.6 MB (6616868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97019d8cfce10dc023be567084137669d8fb7772cec7218f1e711f4cfae562dc`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 18.6 KB (18603 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:87ad7b222f94bd4ffeda78eb7cf201ac297f22792db2eb6c627342cd68e91c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69868386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df3cfc1c8fffefd348cacfe8d18c9367e7b15f4227b2b32750bba9a1dad4eba`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:557a5348da1e680593a9ba709ef059b96baf15e0c89d8f8343e97bf008d9dc05 in / 
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
	-	`sha256:b508f3272b9b70b8dd19c621a4da1be63880a1f6412063787647ceeb464d772a`  
		Last Modified: Wed, 31 Jan 2024 22:48:00 GMT  
		Size: 26.9 MB (26909323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5389309a8aec1769eaeaa29319de4bebf1627abb4b7c25ceaef27190cd064cfc`  
		Last Modified: Thu, 01 Feb 2024 12:00:33 GMT  
		Size: 16.8 MB (16840201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31b408b37e2ea86da1e5dbb066b4b3fb5d09551561012dec426720879e0ebee`  
		Last Modified: Thu, 01 Feb 2024 12:00:32 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3f755d015144784b5213f297ec37d52ddb303651246f90287675b59fdb928e`  
		Last Modified: Thu, 01 Feb 2024 12:00:34 GMT  
		Size: 26.1 MB (26115505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:10fa924814f0100863a02d43cde888366c56bb1999d35f4ec2cb5458ede1d8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6608604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005c1e6b2319f0434d5ccdc6f83cedaf5c4931041228a3b257bf9d9d5fb2e4c2`

```dockerfile
```

-	Layers:
	-	`sha256:f0eebab35555f3e7c0ebb7213ba7f2f39f5d2117387aec58252ad62f3578ad40`  
		Last Modified: Thu, 01 Feb 2024 12:00:33 GMT  
		Size: 6.6 MB (6590040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32bd71fd61ddf99b170b9b0785a26c0ee132d0d4f5715fac60a135b66c6200a2`  
		Last Modified: Thu, 01 Feb 2024 12:00:32 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:acbb7bca937bcbdadea02ea51bd199c2c3cb20c4710043cabbf16dcbc82ec971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66192097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9882134ca1726fbcba90c8ffa149ba970b02f9ca5f6f67952d386a590416acb3`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
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
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710b5644e8d7ce9b22f8100f04ed12089274d8e6ecaa7b281e784390d9a624b7`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 16.4 MB (16432998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c9b75f1d3fb010ce226691f08e04e0eca369822f016344e74c988e7ff9cbd8`  
		Last Modified: Sat, 03 Feb 2024 11:14:04 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4b63d99a8fee13ec791237ca413916d8e6c7533abae83274d4674c855395`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 25.0 MB (25014178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:5741bec69a3a0a56fa45545bb9325a960c1706d417f5c2d6739b28b865f70c2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6609678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e40dd73c96b2bc78fa4fc0bc3ebf1c7edb34aeb93676b09737429a7b8d753b0`

```dockerfile
```

-	Layers:
	-	`sha256:72cf1412c4556bb0f02816b52887305bbd5ebccd80827e0404367c869478d2ed`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 6.6 MB (6591114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64c76402e6b60447a3e1c01a7d118cb99869ea18b5b76ebe57796f09cf7cea62`  
		Last Modified: Sat, 03 Feb 2024 11:14:04 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:ab01c34a30c278373d07d580043e8a18e72fdaedef7dda4a42dc222f7b997295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74448713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6936425758539b2ebe94594f0f57669ce6f225b3fda544a7169b3a8c918fcf70`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
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
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3ca413b8af66fc07e47a491183e81f2d8418a36f4b96f3bdf10c96382787ee`  
		Last Modified: Thu, 01 Feb 2024 15:38:27 GMT  
		Size: 17.8 MB (17832825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f66dbcdfcc246d829efadc3627c1885169a547fd80fcef2f9f380ffb2cbc82a`  
		Last Modified: Thu, 01 Feb 2024 15:38:26 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0c68f2c78a25389c67e4236b05e25abf97345db7813892b2d0e8f00ef530db`  
		Last Modified: Thu, 01 Feb 2024 15:38:28 GMT  
		Size: 27.4 MB (27431697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9b2ce4726f911cecf3cdc2ce92874aa0c7a1d9991a3be9a1fdb8488f3507b3d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6615993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d78c2cfaac7640d2fba3d28b916ab8c140371df8abe66975d35d9d5a224e724`

```dockerfile
```

-	Layers:
	-	`sha256:88a3436d2dc5f0b5a747fedf9b08fd46e9fa64aa7be78c7dc416e4ec9fc043fa`  
		Last Modified: Thu, 01 Feb 2024 15:38:31 GMT  
		Size: 6.6 MB (6597539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:174c63d7fedd1ff225033ff0e20a26b24492ce336185f5f0c5ca8a39e2e2b217`  
		Last Modified: Thu, 01 Feb 2024 15:38:27 GMT  
		Size: 18.5 KB (18454 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:766da4d0c23a6b5a02fcfe6a9c290de6c880f481723bd162ec357b72a4b47a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76119263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6e2b48aea52eb23e814469cc9fee45495df60d11dcfcf7136304f394069c00`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:540e2de73452bd162dd7f630bf29f60e7d2e4a7a5d32a495bedf8ad390b59d7f in / 
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
	-	`sha256:34ef135b45f33052e8e5bca668f9a45a938944a9cf3fb73a46f54a7bf11f091b`  
		Last Modified: Wed, 31 Jan 2024 22:43:46 GMT  
		Size: 30.2 MB (30165018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dbf5ba1aef114655d4178cb7b25fc40be6cbbc4e74271ef3c0d129f27f7948`  
		Last Modified: Wed, 31 Jan 2024 23:55:35 GMT  
		Size: 17.6 MB (17592714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5c8ab8d6a9d2481fb1e6c046eda1e5bebc72c7171390e7918bbf3230a3a722`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f0f14697a5f1c37fedc3b6d79441454aa012edc2c624b113dab83f6ae387fe`  
		Last Modified: Wed, 31 Jan 2024 23:55:35 GMT  
		Size: 28.4 MB (28358174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:209fdc2b901e8609cc13ee3d75d5ddc3ddc5a77eb48684669e38db4fecc4c502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5adccb9448d759136b20f5bdf9d17e7b24e77b7f9ab897d4f7e971f758f79bba`

```dockerfile
```

-	Layers:
	-	`sha256:d1c4277341c5a786dc08c35575a05e75f388d342d5a278a44d83c0c37d739506`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 6.6 MB (6609873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ee0cd483b9775bf82c5f73475a171139475368fc3052df090bfb26cafea30e`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:5b07d620f6e0a5a433dafa6289d75943fe3f50b878b31f3b50428e645a145462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73891556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec83415acb7aaf453c85c9fbf2dcb484813439e60106ce3678051032190e571b`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
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
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0542ca44f4608abe3eb8928a6679f1310a135de5d26dcaef75fdfc7158cb3ea`  
		Last Modified: Thu, 01 Feb 2024 20:14:13 GMT  
		Size: 16.7 MB (16739448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5445b96f290754cc47514654bf406c8cf27af72cafe3c07122d2319baeab5c6`  
		Last Modified: Thu, 01 Feb 2024 20:14:11 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c99cf776ed9d9e58bad7c58c6a56f0e52654611186998435beea42f692d00d`  
		Last Modified: Thu, 01 Feb 2024 20:14:14 GMT  
		Size: 28.0 MB (28006308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:2374bfe0c2ed5ac9aa6c56cbcd7c04c3173332bc39faa38c57a475b929a9b702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2339be92d5d786c3309d29bedbceefe69adad7b0444bd27b86f0b90776e9a30`

```dockerfile
```

-	Layers:
	-	`sha256:28e3d51004b87049273ec1ea39d8930a3cfdd6cc05b2194a9e96b65bca71c335`  
		Last Modified: Thu, 01 Feb 2024 20:14:11 GMT  
		Size: 18.3 KB (18320 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:99fee1cd7190e2738316eca944f9cb4474388bdcdff44d4e7492808c79c1838a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81689464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a168acd494049e622c9716bfe5c16cc1c017bea4033b8fe102da9b3f41c70dc`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:fca8b919a8d1e36420dd1e3f3e427aaaae28a2f57e46c27207acd8e3df0d7a97 in / 
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
	-	`sha256:dfeacd5cd8171f4516ea86dadfb60a372eabf49428dc23d2efdda68cff5b05e7`  
		Last Modified: Wed, 31 Jan 2024 22:34:24 GMT  
		Size: 33.1 MB (33142917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a3bd8096c05f1674995eeb051e3cdf023bbca5505b3f75e624f37c5b13e1b3`  
		Last Modified: Thu, 01 Feb 2024 12:57:44 GMT  
		Size: 18.6 MB (18565973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c5b4610ff6d9b857d7b8bcbc7a90224f918f31c45540cb15c1625a86bf95bc`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcf5f7f76af69ab342a135aed7b0fe5dab9ec932f2bcaeeb58cf8e9491096cb`  
		Last Modified: Thu, 01 Feb 2024 12:57:44 GMT  
		Size: 30.0 MB (29977216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:e5e62f13b43055d9255623225d660999c6209f6cbc9413307aaea737b381644f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6627686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bceb9b0ed2cbb811589e573c40c51eef92a381ce1039e4c4a81f5bfef5f2d0db`

```dockerfile
```

-	Layers:
	-	`sha256:5faeac8a64644b64f37809aa623f431a2453aa3dc443ad2173158318e03ae6ec`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 6.6 MB (6609185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f23996cea2f94cdfa72579bfbb5a59af44283d6b74f21f3d83612614d8698f3`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:3be6d24893ec88d5484e2c6ff47dabe648e0c56d532619254ec2005f79b316f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72553121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eeb87370bfa6742ae5cdffe4e9e5fbcded5a376ea20cb9f0ff781310654cff`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
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
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4594bbef0c3ed6e5d274cc97e215f696416fa4ae17044dfd8fe130e789bbc1`  
		Last Modified: Tue, 06 Feb 2024 11:27:01 GMT  
		Size: 18.0 MB (18014343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb84559c99fdfcc14828d4d1d39640bc61b21c99711be784b356d5c32b0fc8a7`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f15c7c91a157b6cb1adb4e9eff1265e940d9ae9d78fa1d5396c6d03f14b7e6e`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 27.0 MB (27021938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:2c98314fd3cf3cdcc7aca67a7f251b24cb5c0f597abe52b639fda52f8631094b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6624174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1856fea1ea1713d5b1fe2b0ff097f7d0a688d0bd16c23f7de87310eb9f37a7a8`

```dockerfile
```

-	Layers:
	-	`sha256:e65ba0bc6f82ed76a16bdbe6b6618f3835b881b23d55dbc63e573dc31c537b19`  
		Last Modified: Tue, 06 Feb 2024 11:27:01 GMT  
		Size: 6.6 MB (6605739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01339a4362670ca4baef375e49a866c7339d89de67789528e853a5a62dd0a787`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 18.4 KB (18435 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5`

```console
$ docker pull irssi@sha256:df2314e3c83d5dd353eafa769eee4302e869ca2782ba3906a63beb9c1e45d88b
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

### `irssi:1.4.5` - linux; amd64

```console
$ docker pull irssi@sha256:f348397f4e94c8233af74fdea9b0e212e59940476974ab34d100894496547bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75868792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ba45dda22d90fa5e9e29f44f3c9db5d8f7ef6ab9a565f15845b3fc25c70ca2`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
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
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c80471fc9f279ecbb940d938880d5d417992f34809cffcc35de55e5c5b7b50`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 18.3 MB (18267918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2fe054dac6c8448486f7f83fb8d9a935f49600d14786eb028d05f1aca7be4d`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0c8cbf7b0f50debae5d2c4db813db40ef72d3f463d35255151d01f443c8f3b`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 28.5 MB (28473427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:0b4f3f615631a2195ca922bb269cc41ce0094ca6b506c2a6f42972e0edb4bb85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6635471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5bdb10eee477ea82a96d9db1c1a6ba2b86d46b4a80e1a99fc3067f614e5ead`

```dockerfile
```

-	Layers:
	-	`sha256:ad8396ba1d7eb23f85a9f1aa776ff1736aa74a41840bdb1336c90e8b0502ebd8`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 6.6 MB (6616868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97019d8cfce10dc023be567084137669d8fb7772cec7218f1e711f4cfae562dc`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 18.6 KB (18603 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v5

```console
$ docker pull irssi@sha256:87ad7b222f94bd4ffeda78eb7cf201ac297f22792db2eb6c627342cd68e91c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69868386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df3cfc1c8fffefd348cacfe8d18c9367e7b15f4227b2b32750bba9a1dad4eba`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:557a5348da1e680593a9ba709ef059b96baf15e0c89d8f8343e97bf008d9dc05 in / 
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
	-	`sha256:b508f3272b9b70b8dd19c621a4da1be63880a1f6412063787647ceeb464d772a`  
		Last Modified: Wed, 31 Jan 2024 22:48:00 GMT  
		Size: 26.9 MB (26909323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5389309a8aec1769eaeaa29319de4bebf1627abb4b7c25ceaef27190cd064cfc`  
		Last Modified: Thu, 01 Feb 2024 12:00:33 GMT  
		Size: 16.8 MB (16840201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31b408b37e2ea86da1e5dbb066b4b3fb5d09551561012dec426720879e0ebee`  
		Last Modified: Thu, 01 Feb 2024 12:00:32 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3f755d015144784b5213f297ec37d52ddb303651246f90287675b59fdb928e`  
		Last Modified: Thu, 01 Feb 2024 12:00:34 GMT  
		Size: 26.1 MB (26115505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:10fa924814f0100863a02d43cde888366c56bb1999d35f4ec2cb5458ede1d8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6608604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005c1e6b2319f0434d5ccdc6f83cedaf5c4931041228a3b257bf9d9d5fb2e4c2`

```dockerfile
```

-	Layers:
	-	`sha256:f0eebab35555f3e7c0ebb7213ba7f2f39f5d2117387aec58252ad62f3578ad40`  
		Last Modified: Thu, 01 Feb 2024 12:00:33 GMT  
		Size: 6.6 MB (6590040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32bd71fd61ddf99b170b9b0785a26c0ee132d0d4f5715fac60a135b66c6200a2`  
		Last Modified: Thu, 01 Feb 2024 12:00:32 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm variant v7

```console
$ docker pull irssi@sha256:acbb7bca937bcbdadea02ea51bd199c2c3cb20c4710043cabbf16dcbc82ec971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66192097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9882134ca1726fbcba90c8ffa149ba970b02f9ca5f6f67952d386a590416acb3`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
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
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710b5644e8d7ce9b22f8100f04ed12089274d8e6ecaa7b281e784390d9a624b7`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 16.4 MB (16432998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c9b75f1d3fb010ce226691f08e04e0eca369822f016344e74c988e7ff9cbd8`  
		Last Modified: Sat, 03 Feb 2024 11:14:04 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4b63d99a8fee13ec791237ca413916d8e6c7533abae83274d4674c855395`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 25.0 MB (25014178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:5741bec69a3a0a56fa45545bb9325a960c1706d417f5c2d6739b28b865f70c2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6609678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e40dd73c96b2bc78fa4fc0bc3ebf1c7edb34aeb93676b09737429a7b8d753b0`

```dockerfile
```

-	Layers:
	-	`sha256:72cf1412c4556bb0f02816b52887305bbd5ebccd80827e0404367c869478d2ed`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 6.6 MB (6591114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64c76402e6b60447a3e1c01a7d118cb99869ea18b5b76ebe57796f09cf7cea62`  
		Last Modified: Sat, 03 Feb 2024 11:14:04 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:ab01c34a30c278373d07d580043e8a18e72fdaedef7dda4a42dc222f7b997295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74448713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6936425758539b2ebe94594f0f57669ce6f225b3fda544a7169b3a8c918fcf70`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
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
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3ca413b8af66fc07e47a491183e81f2d8418a36f4b96f3bdf10c96382787ee`  
		Last Modified: Thu, 01 Feb 2024 15:38:27 GMT  
		Size: 17.8 MB (17832825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f66dbcdfcc246d829efadc3627c1885169a547fd80fcef2f9f380ffb2cbc82a`  
		Last Modified: Thu, 01 Feb 2024 15:38:26 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0c68f2c78a25389c67e4236b05e25abf97345db7813892b2d0e8f00ef530db`  
		Last Modified: Thu, 01 Feb 2024 15:38:28 GMT  
		Size: 27.4 MB (27431697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:9b2ce4726f911cecf3cdc2ce92874aa0c7a1d9991a3be9a1fdb8488f3507b3d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6615993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d78c2cfaac7640d2fba3d28b916ab8c140371df8abe66975d35d9d5a224e724`

```dockerfile
```

-	Layers:
	-	`sha256:88a3436d2dc5f0b5a747fedf9b08fd46e9fa64aa7be78c7dc416e4ec9fc043fa`  
		Last Modified: Thu, 01 Feb 2024 15:38:31 GMT  
		Size: 6.6 MB (6597539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:174c63d7fedd1ff225033ff0e20a26b24492ce336185f5f0c5ca8a39e2e2b217`  
		Last Modified: Thu, 01 Feb 2024 15:38:27 GMT  
		Size: 18.5 KB (18454 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; 386

```console
$ docker pull irssi@sha256:766da4d0c23a6b5a02fcfe6a9c290de6c880f481723bd162ec357b72a4b47a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76119263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6e2b48aea52eb23e814469cc9fee45495df60d11dcfcf7136304f394069c00`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:540e2de73452bd162dd7f630bf29f60e7d2e4a7a5d32a495bedf8ad390b59d7f in / 
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
	-	`sha256:34ef135b45f33052e8e5bca668f9a45a938944a9cf3fb73a46f54a7bf11f091b`  
		Last Modified: Wed, 31 Jan 2024 22:43:46 GMT  
		Size: 30.2 MB (30165018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dbf5ba1aef114655d4178cb7b25fc40be6cbbc4e74271ef3c0d129f27f7948`  
		Last Modified: Wed, 31 Jan 2024 23:55:35 GMT  
		Size: 17.6 MB (17592714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5c8ab8d6a9d2481fb1e6c046eda1e5bebc72c7171390e7918bbf3230a3a722`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f0f14697a5f1c37fedc3b6d79441454aa012edc2c624b113dab83f6ae387fe`  
		Last Modified: Wed, 31 Jan 2024 23:55:35 GMT  
		Size: 28.4 MB (28358174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:209fdc2b901e8609cc13ee3d75d5ddc3ddc5a77eb48684669e38db4fecc4c502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5adccb9448d759136b20f5bdf9d17e7b24e77b7f9ab897d4f7e971f758f79bba`

```dockerfile
```

-	Layers:
	-	`sha256:d1c4277341c5a786dc08c35575a05e75f388d342d5a278a44d83c0c37d739506`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 6.6 MB (6609873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ee0cd483b9775bf82c5f73475a171139475368fc3052df090bfb26cafea30e`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; mips64le

```console
$ docker pull irssi@sha256:5b07d620f6e0a5a433dafa6289d75943fe3f50b878b31f3b50428e645a145462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73891556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec83415acb7aaf453c85c9fbf2dcb484813439e60106ce3678051032190e571b`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
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
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0542ca44f4608abe3eb8928a6679f1310a135de5d26dcaef75fdfc7158cb3ea`  
		Last Modified: Thu, 01 Feb 2024 20:14:13 GMT  
		Size: 16.7 MB (16739448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5445b96f290754cc47514654bf406c8cf27af72cafe3c07122d2319baeab5c6`  
		Last Modified: Thu, 01 Feb 2024 20:14:11 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c99cf776ed9d9e58bad7c58c6a56f0e52654611186998435beea42f692d00d`  
		Last Modified: Thu, 01 Feb 2024 20:14:14 GMT  
		Size: 28.0 MB (28006308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:2374bfe0c2ed5ac9aa6c56cbcd7c04c3173332bc39faa38c57a475b929a9b702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2339be92d5d786c3309d29bedbceefe69adad7b0444bd27b86f0b90776e9a30`

```dockerfile
```

-	Layers:
	-	`sha256:28e3d51004b87049273ec1ea39d8930a3cfdd6cc05b2194a9e96b65bca71c335`  
		Last Modified: Thu, 01 Feb 2024 20:14:11 GMT  
		Size: 18.3 KB (18320 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; ppc64le

```console
$ docker pull irssi@sha256:99fee1cd7190e2738316eca944f9cb4474388bdcdff44d4e7492808c79c1838a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81689464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a168acd494049e622c9716bfe5c16cc1c017bea4033b8fe102da9b3f41c70dc`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:fca8b919a8d1e36420dd1e3f3e427aaaae28a2f57e46c27207acd8e3df0d7a97 in / 
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
	-	`sha256:dfeacd5cd8171f4516ea86dadfb60a372eabf49428dc23d2efdda68cff5b05e7`  
		Last Modified: Wed, 31 Jan 2024 22:34:24 GMT  
		Size: 33.1 MB (33142917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a3bd8096c05f1674995eeb051e3cdf023bbca5505b3f75e624f37c5b13e1b3`  
		Last Modified: Thu, 01 Feb 2024 12:57:44 GMT  
		Size: 18.6 MB (18565973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c5b4610ff6d9b857d7b8bcbc7a90224f918f31c45540cb15c1625a86bf95bc`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcf5f7f76af69ab342a135aed7b0fe5dab9ec932f2bcaeeb58cf8e9491096cb`  
		Last Modified: Thu, 01 Feb 2024 12:57:44 GMT  
		Size: 30.0 MB (29977216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:e5e62f13b43055d9255623225d660999c6209f6cbc9413307aaea737b381644f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6627686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bceb9b0ed2cbb811589e573c40c51eef92a381ce1039e4c4a81f5bfef5f2d0db`

```dockerfile
```

-	Layers:
	-	`sha256:5faeac8a64644b64f37809aa623f431a2453aa3dc443ad2173158318e03ae6ec`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 6.6 MB (6609185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f23996cea2f94cdfa72579bfbb5a59af44283d6b74f21f3d83612614d8698f3`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5` - linux; s390x

```console
$ docker pull irssi@sha256:3be6d24893ec88d5484e2c6ff47dabe648e0c56d532619254ec2005f79b316f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72553121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eeb87370bfa6742ae5cdffe4e9e5fbcded5a376ea20cb9f0ff781310654cff`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
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
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4594bbef0c3ed6e5d274cc97e215f696416fa4ae17044dfd8fe130e789bbc1`  
		Last Modified: Tue, 06 Feb 2024 11:27:01 GMT  
		Size: 18.0 MB (18014343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb84559c99fdfcc14828d4d1d39640bc61b21c99711be784b356d5c32b0fc8a7`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f15c7c91a157b6cb1adb4e9eff1265e940d9ae9d78fa1d5396c6d03f14b7e6e`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 27.0 MB (27021938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5` - unknown; unknown

```console
$ docker pull irssi@sha256:2c98314fd3cf3cdcc7aca67a7f251b24cb5c0f597abe52b639fda52f8631094b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6624174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1856fea1ea1713d5b1fe2b0ff097f7d0a688d0bd16c23f7de87310eb9f37a7a8`

```dockerfile
```

-	Layers:
	-	`sha256:e65ba0bc6f82ed76a16bdbe6b6618f3835b881b23d55dbc63e573dc31c537b19`  
		Last Modified: Tue, 06 Feb 2024 11:27:01 GMT  
		Size: 6.6 MB (6605739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01339a4362670ca4baef375e49a866c7339d89de67789528e853a5a62dd0a787`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 18.4 KB (18435 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine`

```console
$ docker pull irssi@sha256:294a5ddd1a7991782f7df46f7f0b1ef870818a1cf3a9afc37399222c27fa95cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1.4.5-alpine` - linux; amd64

```console
$ docker pull irssi@sha256:ef6c7693f4591e49ec7ebb9d9e3ff118d31da2e6e989cc01d7c4ba68d6ab312e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18451473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33d0b6133f016daecdc32847e2719e1b8377593ca3a157e4e2182ec699b3619`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d5073c9dc162f6d73c33561ca62b1f3d4afe73e51dfe01bc3bdbe570603526`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 9.6 MB (9645490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaa94b168ed27385c169187548faa3944812324045e5b7d4f9fa0141d934de7`  
		Last Modified: Sat, 27 Jan 2024 00:53:19 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33ada92546b652616e31a208091cb77dc65019c90e5944f396554ea13e63472`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 5.4 MB (5402150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d7192c220068161f91626a3d88eb71585cea3908b88e32bc9d7a200ba73e04f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.5 KB (992458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e03dcb09479e1e99b8f120055916a32994d838a16cdeba603eb3779a35bdb3`

```dockerfile
```

-	Layers:
	-	`sha256:2d6761df79ddf9480ea4aa104a72a140a5347d5dea19b3eb975a78d2a144483b`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 975.0 KB (975030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f3ba2fd4c9e25b6b8c3ce87fda3494b8506f3cebb1bc0e371df70b3a1c44a87`  
		Last Modified: Sat, 27 Jan 2024 00:53:19 GMT  
		Size: 17.4 KB (17428 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:11cdd850f01f7020ea3dc559a1cacf1710ce7e1110b2b3be3d5088a753388e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980aff2e9d7fdabd52ca418744d9e75a16f305953ff369624a6f3e91ee563444`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1caa0b93da06dd2aa46cce7a3fd9bbc4b0b58ff19b6dee6450b493cb819f9cd`  
		Last Modified: Tue, 30 Jan 2024 18:54:03 GMT  
		Size: 8.9 MB (8880054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93390793c8d561bd6d0fed103d923be9845e322d71b5187396645909aee925df`  
		Last Modified: Tue, 30 Jan 2024 18:54:02 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db82a85a709f0d1d93b2c72989821c461582c5c99c841cb1d8529c32826084d`  
		Last Modified: Tue, 30 Jan 2024 18:54:03 GMT  
		Size: 5.2 MB (5242167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:bd1dc317b136af3a211fed01816891cbea3e545a66d52fec0a8cfe3c9ae9a9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 KB (17341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af05cb00d364bd5dc1c1184bb77489a40ba8096333fcb8ad4b6969822a45b3ac`

```dockerfile
```

-	Layers:
	-	`sha256:7a7a2bdaf6762372aa21871c515a18d90c4cfa782df359a7f10dcafb1a8acbcf`  
		Last Modified: Tue, 30 Jan 2024 18:54:02 GMT  
		Size: 17.3 KB (17341 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:89e22268640c72b2ae0efb98e009b34bd5534ad6c4aa596df74bfd27c1775e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16630432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9bff58300e84d8932cb47d4638ebdafbd9eb55888c2cfe35e7c89ce11cacec`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a728625b39c4526fc00d553e9ad76abf2d838e770db539a4503401b8151b7`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 8.7 MB (8721243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80dec7634cb6fd64dad041788335bf81e0374c155777e94d292608fadbc918e3`  
		Last Modified: Sat, 27 Jan 2024 16:10:09 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a274dbd32034295ddcbc1067913cee45ae78dfd48bcfa5a5a0227438b251e6c`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 5.0 MB (5006505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:81909a4824efd52f673139f1bfce8946affddffd9073b10d3429fc7e6a25b6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **995.1 KB (995130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f8bf5414c3b8dabe31b6645b897840a59666ed989623f0fa633e51cd171a51`

```dockerfile
```

-	Layers:
	-	`sha256:788b342a7afe442fa8cc36f28d56399fe0b0abcded67366d9cfc6f4414ec6b28`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 977.6 KB (977574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af9e565fad9e84cc85a9eb745382b7350da37e969b74d2723023407a1dc827b`  
		Last Modified: Sat, 27 Jan 2024 16:10:09 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f967a5aba07f362a1fc42968dc5c25d932ddf7c5afc29b87f3e103f41e11b3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b852dcd533ac6fef70eee55ddc2eb8cd1a1a2438f10c7fb9780fcc8f8c53ae7`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427b55bea52be9d140397d36bdf44940754b11f701ab1c8860bf265108864474`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 9.7 MB (9672879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3172290de02d764723938f6bbf53611e992dca7775d89910602a51d4fdc12c0c`  
		Last Modified: Sat, 27 Jan 2024 20:28:06 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4046f82759ffd91ca630dba178059b2985f3ec4fb9cb5a8d928a59215b0b5b2`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 5.3 MB (5308548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b68051a5d753ec8037cd2f9d14313c65e2bf5d4c67f564eec3f3f58eb4a131b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.5 KB (992495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edf1b50c168b27a6f3a5f6a4b2a2711df8f7bd7bbfdc93ea5eef3a8861c5e0c`

```dockerfile
```

-	Layers:
	-	`sha256:f636b4606a093b4d77ac5276a6d5402ca1ff4b0641b2656d45bb27ff2ed683af`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 975.0 KB (975049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0aae570a126a40b9525d270285ba0d643a33c387a1f9f79698263d38a935f73`  
		Last Modified: Sat, 27 Jan 2024 20:28:06 GMT  
		Size: 17.4 KB (17446 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; 386

```console
$ docker pull irssi@sha256:387d4dc6384ebea47ed5276a5865acb546bb67dfc227fe393dc75db5d45852dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17557817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e96759752775aacd2fda0f53e8cf266fc1c7b3e068566a8fc8c2add735f586`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8086f06106cd7bdd94cddf1c7363b144b801cd672997d9fe81ed6ab8ae03891`  
		Last Modified: Sat, 27 Jan 2024 01:54:00 GMT  
		Size: 8.9 MB (8904430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d1dba1f614043dea1e85138edb339caa7e16cca6c013e81384bd9f7f1afe02`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a341596e873d51872b196d8782ad7c32261c5a181b99f1f2d4c8c053a35a752a`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 5.4 MB (5413031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d7e896f39991af1e19a5fea9c4353550ddd15bbb4fa05afc17e02656c66c8104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.4 KB (992360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617babf31d74046af9500e49f9674cbad6f479da89ac7b7cb51ba62e91a8f83a`

```dockerfile
```

-	Layers:
	-	`sha256:b11bca7efa15aa00afe306253a110a6805f8d56ebdfb10ff646a51e2a4f69f81`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 975.0 KB (974985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4a8d0da397b1dded79f569fffc3082addee92a84c9f41f986ef310c44a72bf8`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 17.4 KB (17375 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:a0a400f2133847c9bbfa653f898fc72042aac4b03cb1371156d8726812131313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18717231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0def155df329eeefa5360cf54f1657dc7731e2f631182fce7e96924a4cabb8`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc74fa4ba26fc8c0460833da6460f59a2b7fdb551209793e9177aa8e4f59346c`  
		Last Modified: Sat, 27 Jan 2024 09:47:30 GMT  
		Size: 9.7 MB (9736547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596eae301f8ffae57ffc8c11b668ca24b994f12d9935de6216884db8f13188d3`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65ab57b806e5436452de1e909990c85bf46bb183048518a40b3e91cceaa914d`  
		Last Modified: Sat, 27 Jan 2024 09:47:30 GMT  
		Size: 5.6 MB (5630906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c822cd405d36a575a6a510133bbc7870de59eabfd7fc4a2bb9485e127fa82363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.9 KB (990946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00c5eb1975042e0f47315f4ba48ed6fe69fbb8e39eb0c845ac7edf8cea9bc47`

```dockerfile
```

-	Layers:
	-	`sha256:51daf79105767963a7bfa2160a6d94beb71eecf88329550e2f9150d944fc2a52`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 973.5 KB (973452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6afd3a59a575c01cda08047a63543de5e7a3b3293e87e18e1bb870d4a2df4e74`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 17.5 KB (17494 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine` - linux; s390x

```console
$ docker pull irssi@sha256:cb11647a91b30743f090d9c0e26aeb8ac9ad300c50b661af12505ae290befd40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18707370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891ea14f0ba63e76c3bf45e2ede5b212af9d872f0b77a89d369fed7f2d5bfd3a`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc77a74801be7299707a33e8a653a76c9c5b8d7289fad0e44f86f0eb950c0dfb`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 10.1 MB (10082896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f5141af0a2579801617b6ef53cc8da747d109de43e1b88c92ba151618c1c12`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7efe871fc37a59627f7fb75e2cd481a361e23ae4423cbd5c60ebfd9cfc40ce4`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 5.4 MB (5405651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:703020e7529818ace6da7d3f3424df173c4f428cf3fdaadb5bfb9d5a806ea431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.8 KB (990826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168cdfdbfc8e0c3b5a619ac19b836bbfce7a1baa6ab36ceaeb816e42d0073b3f`

```dockerfile
```

-	Layers:
	-	`sha256:a2f8050d7c3f109cc73636ae770c90e2cde71f2ed0dcd93078524351667493a8`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 973.4 KB (973394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304d7cd47112bf0ace221c02f2bdff3de634bfada70e48aad5065bc3c7424e87`  
		Last Modified: Sun, 28 Jan 2024 09:20:59 GMT  
		Size: 17.4 KB (17432 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-alpine3.18`

```console
$ docker pull irssi@sha256:294a5ddd1a7991782f7df46f7f0b1ef870818a1cf3a9afc37399222c27fa95cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:1.4.5-alpine3.18` - linux; amd64

```console
$ docker pull irssi@sha256:ef6c7693f4591e49ec7ebb9d9e3ff118d31da2e6e989cc01d7c4ba68d6ab312e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18451473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33d0b6133f016daecdc32847e2719e1b8377593ca3a157e4e2182ec699b3619`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d5073c9dc162f6d73c33561ca62b1f3d4afe73e51dfe01bc3bdbe570603526`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 9.6 MB (9645490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaa94b168ed27385c169187548faa3944812324045e5b7d4f9fa0141d934de7`  
		Last Modified: Sat, 27 Jan 2024 00:53:19 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33ada92546b652616e31a208091cb77dc65019c90e5944f396554ea13e63472`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 5.4 MB (5402150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:d7192c220068161f91626a3d88eb71585cea3908b88e32bc9d7a200ba73e04f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.5 KB (992458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e03dcb09479e1e99b8f120055916a32994d838a16cdeba603eb3779a35bdb3`

```dockerfile
```

-	Layers:
	-	`sha256:2d6761df79ddf9480ea4aa104a72a140a5347d5dea19b3eb975a78d2a144483b`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 975.0 KB (975030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f3ba2fd4c9e25b6b8c3ce87fda3494b8506f3cebb1bc0e371df70b3a1c44a87`  
		Last Modified: Sat, 27 Jan 2024 00:53:19 GMT  
		Size: 17.4 KB (17428 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.18` - linux; arm variant v6

```console
$ docker pull irssi@sha256:11cdd850f01f7020ea3dc559a1cacf1710ce7e1110b2b3be3d5088a753388e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980aff2e9d7fdabd52ca418744d9e75a16f305953ff369624a6f3e91ee563444`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1caa0b93da06dd2aa46cce7a3fd9bbc4b0b58ff19b6dee6450b493cb819f9cd`  
		Last Modified: Tue, 30 Jan 2024 18:54:03 GMT  
		Size: 8.9 MB (8880054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93390793c8d561bd6d0fed103d923be9845e322d71b5187396645909aee925df`  
		Last Modified: Tue, 30 Jan 2024 18:54:02 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db82a85a709f0d1d93b2c72989821c461582c5c99c841cb1d8529c32826084d`  
		Last Modified: Tue, 30 Jan 2024 18:54:03 GMT  
		Size: 5.2 MB (5242167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:bd1dc317b136af3a211fed01816891cbea3e545a66d52fec0a8cfe3c9ae9a9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 KB (17341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af05cb00d364bd5dc1c1184bb77489a40ba8096333fcb8ad4b6969822a45b3ac`

```dockerfile
```

-	Layers:
	-	`sha256:7a7a2bdaf6762372aa21871c515a18d90c4cfa782df359a7f10dcafb1a8acbcf`  
		Last Modified: Tue, 30 Jan 2024 18:54:02 GMT  
		Size: 17.3 KB (17341 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.18` - linux; arm variant v7

```console
$ docker pull irssi@sha256:89e22268640c72b2ae0efb98e009b34bd5534ad6c4aa596df74bfd27c1775e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16630432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9bff58300e84d8932cb47d4638ebdafbd9eb55888c2cfe35e7c89ce11cacec`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a728625b39c4526fc00d553e9ad76abf2d838e770db539a4503401b8151b7`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 8.7 MB (8721243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80dec7634cb6fd64dad041788335bf81e0374c155777e94d292608fadbc918e3`  
		Last Modified: Sat, 27 Jan 2024 16:10:09 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a274dbd32034295ddcbc1067913cee45ae78dfd48bcfa5a5a0227438b251e6c`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 5.0 MB (5006505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:81909a4824efd52f673139f1bfce8946affddffd9073b10d3429fc7e6a25b6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **995.1 KB (995130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f8bf5414c3b8dabe31b6645b897840a59666ed989623f0fa633e51cd171a51`

```dockerfile
```

-	Layers:
	-	`sha256:788b342a7afe442fa8cc36f28d56399fe0b0abcded67366d9cfc6f4414ec6b28`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 977.6 KB (977574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af9e565fad9e84cc85a9eb745382b7350da37e969b74d2723023407a1dc827b`  
		Last Modified: Sat, 27 Jan 2024 16:10:09 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.18` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f967a5aba07f362a1fc42968dc5c25d932ddf7c5afc29b87f3e103f41e11b3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b852dcd533ac6fef70eee55ddc2eb8cd1a1a2438f10c7fb9780fcc8f8c53ae7`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427b55bea52be9d140397d36bdf44940754b11f701ab1c8860bf265108864474`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 9.7 MB (9672879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3172290de02d764723938f6bbf53611e992dca7775d89910602a51d4fdc12c0c`  
		Last Modified: Sat, 27 Jan 2024 20:28:06 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4046f82759ffd91ca630dba178059b2985f3ec4fb9cb5a8d928a59215b0b5b2`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 5.3 MB (5308548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:b68051a5d753ec8037cd2f9d14313c65e2bf5d4c67f564eec3f3f58eb4a131b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.5 KB (992495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edf1b50c168b27a6f3a5f6a4b2a2711df8f7bd7bbfdc93ea5eef3a8861c5e0c`

```dockerfile
```

-	Layers:
	-	`sha256:f636b4606a093b4d77ac5276a6d5402ca1ff4b0641b2656d45bb27ff2ed683af`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 975.0 KB (975049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0aae570a126a40b9525d270285ba0d643a33c387a1f9f79698263d38a935f73`  
		Last Modified: Sat, 27 Jan 2024 20:28:06 GMT  
		Size: 17.4 KB (17446 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.18` - linux; 386

```console
$ docker pull irssi@sha256:387d4dc6384ebea47ed5276a5865acb546bb67dfc227fe393dc75db5d45852dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17557817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e96759752775aacd2fda0f53e8cf266fc1c7b3e068566a8fc8c2add735f586`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8086f06106cd7bdd94cddf1c7363b144b801cd672997d9fe81ed6ab8ae03891`  
		Last Modified: Sat, 27 Jan 2024 01:54:00 GMT  
		Size: 8.9 MB (8904430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d1dba1f614043dea1e85138edb339caa7e16cca6c013e81384bd9f7f1afe02`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a341596e873d51872b196d8782ad7c32261c5a181b99f1f2d4c8c053a35a752a`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 5.4 MB (5413031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:d7e896f39991af1e19a5fea9c4353550ddd15bbb4fa05afc17e02656c66c8104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.4 KB (992360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617babf31d74046af9500e49f9674cbad6f479da89ac7b7cb51ba62e91a8f83a`

```dockerfile
```

-	Layers:
	-	`sha256:b11bca7efa15aa00afe306253a110a6805f8d56ebdfb10ff646a51e2a4f69f81`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 975.0 KB (974985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4a8d0da397b1dded79f569fffc3082addee92a84c9f41f986ef310c44a72bf8`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 17.4 KB (17375 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.18` - linux; ppc64le

```console
$ docker pull irssi@sha256:a0a400f2133847c9bbfa653f898fc72042aac4b03cb1371156d8726812131313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18717231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0def155df329eeefa5360cf54f1657dc7731e2f631182fce7e96924a4cabb8`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc74fa4ba26fc8c0460833da6460f59a2b7fdb551209793e9177aa8e4f59346c`  
		Last Modified: Sat, 27 Jan 2024 09:47:30 GMT  
		Size: 9.7 MB (9736547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596eae301f8ffae57ffc8c11b668ca24b994f12d9935de6216884db8f13188d3`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65ab57b806e5436452de1e909990c85bf46bb183048518a40b3e91cceaa914d`  
		Last Modified: Sat, 27 Jan 2024 09:47:30 GMT  
		Size: 5.6 MB (5630906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:c822cd405d36a575a6a510133bbc7870de59eabfd7fc4a2bb9485e127fa82363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.9 KB (990946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00c5eb1975042e0f47315f4ba48ed6fe69fbb8e39eb0c845ac7edf8cea9bc47`

```dockerfile
```

-	Layers:
	-	`sha256:51daf79105767963a7bfa2160a6d94beb71eecf88329550e2f9150d944fc2a52`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 973.5 KB (973452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6afd3a59a575c01cda08047a63543de5e7a3b3293e87e18e1bb870d4a2df4e74`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 17.5 KB (17494 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-alpine3.18` - linux; s390x

```console
$ docker pull irssi@sha256:cb11647a91b30743f090d9c0e26aeb8ac9ad300c50b661af12505ae290befd40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18707370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891ea14f0ba63e76c3bf45e2ede5b212af9d872f0b77a89d369fed7f2d5bfd3a`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc77a74801be7299707a33e8a653a76c9c5b8d7289fad0e44f86f0eb950c0dfb`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 10.1 MB (10082896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f5141af0a2579801617b6ef53cc8da747d109de43e1b88c92ba151618c1c12`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7efe871fc37a59627f7fb75e2cd481a361e23ae4423cbd5c60ebfd9cfc40ce4`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 5.4 MB (5405651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:703020e7529818ace6da7d3f3424df173c4f428cf3fdaadb5bfb9d5a806ea431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.8 KB (990826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168cdfdbfc8e0c3b5a619ac19b836bbfce7a1baa6ab36ceaeb816e42d0073b3f`

```dockerfile
```

-	Layers:
	-	`sha256:a2f8050d7c3f109cc73636ae770c90e2cde71f2ed0dcd93078524351667493a8`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 973.4 KB (973394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304d7cd47112bf0ace221c02f2bdff3de634bfada70e48aad5065bc3c7424e87`  
		Last Modified: Sun, 28 Jan 2024 09:20:59 GMT  
		Size: 17.4 KB (17432 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:1.4.5-bookworm`

```console
$ docker pull irssi@sha256:df2314e3c83d5dd353eafa769eee4302e869ca2782ba3906a63beb9c1e45d88b
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

### `irssi:1.4.5-bookworm` - linux; amd64

```console
$ docker pull irssi@sha256:f348397f4e94c8233af74fdea9b0e212e59940476974ab34d100894496547bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75868792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ba45dda22d90fa5e9e29f44f3c9db5d8f7ef6ab9a565f15845b3fc25c70ca2`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
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
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c80471fc9f279ecbb940d938880d5d417992f34809cffcc35de55e5c5b7b50`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 18.3 MB (18267918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2fe054dac6c8448486f7f83fb8d9a935f49600d14786eb028d05f1aca7be4d`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0c8cbf7b0f50debae5d2c4db813db40ef72d3f463d35255151d01f443c8f3b`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 28.5 MB (28473427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:0b4f3f615631a2195ca922bb269cc41ce0094ca6b506c2a6f42972e0edb4bb85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6635471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5bdb10eee477ea82a96d9db1c1a6ba2b86d46b4a80e1a99fc3067f614e5ead`

```dockerfile
```

-	Layers:
	-	`sha256:ad8396ba1d7eb23f85a9f1aa776ff1736aa74a41840bdb1336c90e8b0502ebd8`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 6.6 MB (6616868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97019d8cfce10dc023be567084137669d8fb7772cec7218f1e711f4cfae562dc`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 18.6 KB (18603 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:87ad7b222f94bd4ffeda78eb7cf201ac297f22792db2eb6c627342cd68e91c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69868386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df3cfc1c8fffefd348cacfe8d18c9367e7b15f4227b2b32750bba9a1dad4eba`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:557a5348da1e680593a9ba709ef059b96baf15e0c89d8f8343e97bf008d9dc05 in / 
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
	-	`sha256:b508f3272b9b70b8dd19c621a4da1be63880a1f6412063787647ceeb464d772a`  
		Last Modified: Wed, 31 Jan 2024 22:48:00 GMT  
		Size: 26.9 MB (26909323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5389309a8aec1769eaeaa29319de4bebf1627abb4b7c25ceaef27190cd064cfc`  
		Last Modified: Thu, 01 Feb 2024 12:00:33 GMT  
		Size: 16.8 MB (16840201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31b408b37e2ea86da1e5dbb066b4b3fb5d09551561012dec426720879e0ebee`  
		Last Modified: Thu, 01 Feb 2024 12:00:32 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3f755d015144784b5213f297ec37d52ddb303651246f90287675b59fdb928e`  
		Last Modified: Thu, 01 Feb 2024 12:00:34 GMT  
		Size: 26.1 MB (26115505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:10fa924814f0100863a02d43cde888366c56bb1999d35f4ec2cb5458ede1d8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6608604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005c1e6b2319f0434d5ccdc6f83cedaf5c4931041228a3b257bf9d9d5fb2e4c2`

```dockerfile
```

-	Layers:
	-	`sha256:f0eebab35555f3e7c0ebb7213ba7f2f39f5d2117387aec58252ad62f3578ad40`  
		Last Modified: Thu, 01 Feb 2024 12:00:33 GMT  
		Size: 6.6 MB (6590040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32bd71fd61ddf99b170b9b0785a26c0ee132d0d4f5715fac60a135b66c6200a2`  
		Last Modified: Thu, 01 Feb 2024 12:00:32 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:acbb7bca937bcbdadea02ea51bd199c2c3cb20c4710043cabbf16dcbc82ec971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66192097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9882134ca1726fbcba90c8ffa149ba970b02f9ca5f6f67952d386a590416acb3`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
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
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710b5644e8d7ce9b22f8100f04ed12089274d8e6ecaa7b281e784390d9a624b7`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 16.4 MB (16432998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c9b75f1d3fb010ce226691f08e04e0eca369822f016344e74c988e7ff9cbd8`  
		Last Modified: Sat, 03 Feb 2024 11:14:04 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4b63d99a8fee13ec791237ca413916d8e6c7533abae83274d4674c855395`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 25.0 MB (25014178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:5741bec69a3a0a56fa45545bb9325a960c1706d417f5c2d6739b28b865f70c2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6609678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e40dd73c96b2bc78fa4fc0bc3ebf1c7edb34aeb93676b09737429a7b8d753b0`

```dockerfile
```

-	Layers:
	-	`sha256:72cf1412c4556bb0f02816b52887305bbd5ebccd80827e0404367c869478d2ed`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 6.6 MB (6591114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64c76402e6b60447a3e1c01a7d118cb99869ea18b5b76ebe57796f09cf7cea62`  
		Last Modified: Sat, 03 Feb 2024 11:14:04 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:ab01c34a30c278373d07d580043e8a18e72fdaedef7dda4a42dc222f7b997295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74448713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6936425758539b2ebe94594f0f57669ce6f225b3fda544a7169b3a8c918fcf70`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
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
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3ca413b8af66fc07e47a491183e81f2d8418a36f4b96f3bdf10c96382787ee`  
		Last Modified: Thu, 01 Feb 2024 15:38:27 GMT  
		Size: 17.8 MB (17832825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f66dbcdfcc246d829efadc3627c1885169a547fd80fcef2f9f380ffb2cbc82a`  
		Last Modified: Thu, 01 Feb 2024 15:38:26 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0c68f2c78a25389c67e4236b05e25abf97345db7813892b2d0e8f00ef530db`  
		Last Modified: Thu, 01 Feb 2024 15:38:28 GMT  
		Size: 27.4 MB (27431697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9b2ce4726f911cecf3cdc2ce92874aa0c7a1d9991a3be9a1fdb8488f3507b3d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6615993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d78c2cfaac7640d2fba3d28b916ab8c140371df8abe66975d35d9d5a224e724`

```dockerfile
```

-	Layers:
	-	`sha256:88a3436d2dc5f0b5a747fedf9b08fd46e9fa64aa7be78c7dc416e4ec9fc043fa`  
		Last Modified: Thu, 01 Feb 2024 15:38:31 GMT  
		Size: 6.6 MB (6597539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:174c63d7fedd1ff225033ff0e20a26b24492ce336185f5f0c5ca8a39e2e2b217`  
		Last Modified: Thu, 01 Feb 2024 15:38:27 GMT  
		Size: 18.5 KB (18454 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; 386

```console
$ docker pull irssi@sha256:766da4d0c23a6b5a02fcfe6a9c290de6c880f481723bd162ec357b72a4b47a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76119263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6e2b48aea52eb23e814469cc9fee45495df60d11dcfcf7136304f394069c00`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:540e2de73452bd162dd7f630bf29f60e7d2e4a7a5d32a495bedf8ad390b59d7f in / 
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
	-	`sha256:34ef135b45f33052e8e5bca668f9a45a938944a9cf3fb73a46f54a7bf11f091b`  
		Last Modified: Wed, 31 Jan 2024 22:43:46 GMT  
		Size: 30.2 MB (30165018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dbf5ba1aef114655d4178cb7b25fc40be6cbbc4e74271ef3c0d129f27f7948`  
		Last Modified: Wed, 31 Jan 2024 23:55:35 GMT  
		Size: 17.6 MB (17592714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5c8ab8d6a9d2481fb1e6c046eda1e5bebc72c7171390e7918bbf3230a3a722`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f0f14697a5f1c37fedc3b6d79441454aa012edc2c624b113dab83f6ae387fe`  
		Last Modified: Wed, 31 Jan 2024 23:55:35 GMT  
		Size: 28.4 MB (28358174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:209fdc2b901e8609cc13ee3d75d5ddc3ddc5a77eb48684669e38db4fecc4c502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5adccb9448d759136b20f5bdf9d17e7b24e77b7f9ab897d4f7e971f758f79bba`

```dockerfile
```

-	Layers:
	-	`sha256:d1c4277341c5a786dc08c35575a05e75f388d342d5a278a44d83c0c37d739506`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 6.6 MB (6609873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ee0cd483b9775bf82c5f73475a171139475368fc3052df090bfb26cafea30e`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:5b07d620f6e0a5a433dafa6289d75943fe3f50b878b31f3b50428e645a145462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73891556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec83415acb7aaf453c85c9fbf2dcb484813439e60106ce3678051032190e571b`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
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
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0542ca44f4608abe3eb8928a6679f1310a135de5d26dcaef75fdfc7158cb3ea`  
		Last Modified: Thu, 01 Feb 2024 20:14:13 GMT  
		Size: 16.7 MB (16739448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5445b96f290754cc47514654bf406c8cf27af72cafe3c07122d2319baeab5c6`  
		Last Modified: Thu, 01 Feb 2024 20:14:11 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c99cf776ed9d9e58bad7c58c6a56f0e52654611186998435beea42f692d00d`  
		Last Modified: Thu, 01 Feb 2024 20:14:14 GMT  
		Size: 28.0 MB (28006308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:2374bfe0c2ed5ac9aa6c56cbcd7c04c3173332bc39faa38c57a475b929a9b702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2339be92d5d786c3309d29bedbceefe69adad7b0444bd27b86f0b90776e9a30`

```dockerfile
```

-	Layers:
	-	`sha256:28e3d51004b87049273ec1ea39d8930a3cfdd6cc05b2194a9e96b65bca71c335`  
		Last Modified: Thu, 01 Feb 2024 20:14:11 GMT  
		Size: 18.3 KB (18320 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:99fee1cd7190e2738316eca944f9cb4474388bdcdff44d4e7492808c79c1838a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81689464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a168acd494049e622c9716bfe5c16cc1c017bea4033b8fe102da9b3f41c70dc`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:fca8b919a8d1e36420dd1e3f3e427aaaae28a2f57e46c27207acd8e3df0d7a97 in / 
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
	-	`sha256:dfeacd5cd8171f4516ea86dadfb60a372eabf49428dc23d2efdda68cff5b05e7`  
		Last Modified: Wed, 31 Jan 2024 22:34:24 GMT  
		Size: 33.1 MB (33142917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a3bd8096c05f1674995eeb051e3cdf023bbca5505b3f75e624f37c5b13e1b3`  
		Last Modified: Thu, 01 Feb 2024 12:57:44 GMT  
		Size: 18.6 MB (18565973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c5b4610ff6d9b857d7b8bcbc7a90224f918f31c45540cb15c1625a86bf95bc`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcf5f7f76af69ab342a135aed7b0fe5dab9ec932f2bcaeeb58cf8e9491096cb`  
		Last Modified: Thu, 01 Feb 2024 12:57:44 GMT  
		Size: 30.0 MB (29977216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:e5e62f13b43055d9255623225d660999c6209f6cbc9413307aaea737b381644f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6627686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bceb9b0ed2cbb811589e573c40c51eef92a381ce1039e4c4a81f5bfef5f2d0db`

```dockerfile
```

-	Layers:
	-	`sha256:5faeac8a64644b64f37809aa623f431a2453aa3dc443ad2173158318e03ae6ec`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 6.6 MB (6609185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f23996cea2f94cdfa72579bfbb5a59af44283d6b74f21f3d83612614d8698f3`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1.4.5-bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:3be6d24893ec88d5484e2c6ff47dabe648e0c56d532619254ec2005f79b316f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72553121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eeb87370bfa6742ae5cdffe4e9e5fbcded5a376ea20cb9f0ff781310654cff`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
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
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4594bbef0c3ed6e5d274cc97e215f696416fa4ae17044dfd8fe130e789bbc1`  
		Last Modified: Tue, 06 Feb 2024 11:27:01 GMT  
		Size: 18.0 MB (18014343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb84559c99fdfcc14828d4d1d39640bc61b21c99711be784b356d5c32b0fc8a7`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f15c7c91a157b6cb1adb4e9eff1265e940d9ae9d78fa1d5396c6d03f14b7e6e`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 27.0 MB (27021938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1.4.5-bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:2c98314fd3cf3cdcc7aca67a7f251b24cb5c0f597abe52b639fda52f8631094b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6624174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1856fea1ea1713d5b1fe2b0ff097f7d0a688d0bd16c23f7de87310eb9f37a7a8`

```dockerfile
```

-	Layers:
	-	`sha256:e65ba0bc6f82ed76a16bdbe6b6618f3835b881b23d55dbc63e573dc31c537b19`  
		Last Modified: Tue, 06 Feb 2024 11:27:01 GMT  
		Size: 6.6 MB (6605739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01339a4362670ca4baef375e49a866c7339d89de67789528e853a5a62dd0a787`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 18.4 KB (18435 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine`

```console
$ docker pull irssi@sha256:294a5ddd1a7991782f7df46f7f0b1ef870818a1cf3a9afc37399222c27fa95cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:alpine` - linux; amd64

```console
$ docker pull irssi@sha256:ef6c7693f4591e49ec7ebb9d9e3ff118d31da2e6e989cc01d7c4ba68d6ab312e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18451473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33d0b6133f016daecdc32847e2719e1b8377593ca3a157e4e2182ec699b3619`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d5073c9dc162f6d73c33561ca62b1f3d4afe73e51dfe01bc3bdbe570603526`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 9.6 MB (9645490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaa94b168ed27385c169187548faa3944812324045e5b7d4f9fa0141d934de7`  
		Last Modified: Sat, 27 Jan 2024 00:53:19 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33ada92546b652616e31a208091cb77dc65019c90e5944f396554ea13e63472`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 5.4 MB (5402150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d7192c220068161f91626a3d88eb71585cea3908b88e32bc9d7a200ba73e04f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.5 KB (992458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e03dcb09479e1e99b8f120055916a32994d838a16cdeba603eb3779a35bdb3`

```dockerfile
```

-	Layers:
	-	`sha256:2d6761df79ddf9480ea4aa104a72a140a5347d5dea19b3eb975a78d2a144483b`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 975.0 KB (975030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f3ba2fd4c9e25b6b8c3ce87fda3494b8506f3cebb1bc0e371df70b3a1c44a87`  
		Last Modified: Sat, 27 Jan 2024 00:53:19 GMT  
		Size: 17.4 KB (17428 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v6

```console
$ docker pull irssi@sha256:11cdd850f01f7020ea3dc559a1cacf1710ce7e1110b2b3be3d5088a753388e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980aff2e9d7fdabd52ca418744d9e75a16f305953ff369624a6f3e91ee563444`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1caa0b93da06dd2aa46cce7a3fd9bbc4b0b58ff19b6dee6450b493cb819f9cd`  
		Last Modified: Tue, 30 Jan 2024 18:54:03 GMT  
		Size: 8.9 MB (8880054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93390793c8d561bd6d0fed103d923be9845e322d71b5187396645909aee925df`  
		Last Modified: Tue, 30 Jan 2024 18:54:02 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db82a85a709f0d1d93b2c72989821c461582c5c99c841cb1d8529c32826084d`  
		Last Modified: Tue, 30 Jan 2024 18:54:03 GMT  
		Size: 5.2 MB (5242167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:bd1dc317b136af3a211fed01816891cbea3e545a66d52fec0a8cfe3c9ae9a9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 KB (17341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af05cb00d364bd5dc1c1184bb77489a40ba8096333fcb8ad4b6969822a45b3ac`

```dockerfile
```

-	Layers:
	-	`sha256:7a7a2bdaf6762372aa21871c515a18d90c4cfa782df359a7f10dcafb1a8acbcf`  
		Last Modified: Tue, 30 Jan 2024 18:54:02 GMT  
		Size: 17.3 KB (17341 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm variant v7

```console
$ docker pull irssi@sha256:89e22268640c72b2ae0efb98e009b34bd5534ad6c4aa596df74bfd27c1775e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16630432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9bff58300e84d8932cb47d4638ebdafbd9eb55888c2cfe35e7c89ce11cacec`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a728625b39c4526fc00d553e9ad76abf2d838e770db539a4503401b8151b7`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 8.7 MB (8721243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80dec7634cb6fd64dad041788335bf81e0374c155777e94d292608fadbc918e3`  
		Last Modified: Sat, 27 Jan 2024 16:10:09 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a274dbd32034295ddcbc1067913cee45ae78dfd48bcfa5a5a0227438b251e6c`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 5.0 MB (5006505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:81909a4824efd52f673139f1bfce8946affddffd9073b10d3429fc7e6a25b6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **995.1 KB (995130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f8bf5414c3b8dabe31b6645b897840a59666ed989623f0fa633e51cd171a51`

```dockerfile
```

-	Layers:
	-	`sha256:788b342a7afe442fa8cc36f28d56399fe0b0abcded67366d9cfc6f4414ec6b28`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 977.6 KB (977574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af9e565fad9e84cc85a9eb745382b7350da37e969b74d2723023407a1dc827b`  
		Last Modified: Sat, 27 Jan 2024 16:10:09 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f967a5aba07f362a1fc42968dc5c25d932ddf7c5afc29b87f3e103f41e11b3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b852dcd533ac6fef70eee55ddc2eb8cd1a1a2438f10c7fb9780fcc8f8c53ae7`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427b55bea52be9d140397d36bdf44940754b11f701ab1c8860bf265108864474`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 9.7 MB (9672879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3172290de02d764723938f6bbf53611e992dca7775d89910602a51d4fdc12c0c`  
		Last Modified: Sat, 27 Jan 2024 20:28:06 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4046f82759ffd91ca630dba178059b2985f3ec4fb9cb5a8d928a59215b0b5b2`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 5.3 MB (5308548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:b68051a5d753ec8037cd2f9d14313c65e2bf5d4c67f564eec3f3f58eb4a131b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.5 KB (992495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edf1b50c168b27a6f3a5f6a4b2a2711df8f7bd7bbfdc93ea5eef3a8861c5e0c`

```dockerfile
```

-	Layers:
	-	`sha256:f636b4606a093b4d77ac5276a6d5402ca1ff4b0641b2656d45bb27ff2ed683af`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 975.0 KB (975049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0aae570a126a40b9525d270285ba0d643a33c387a1f9f79698263d38a935f73`  
		Last Modified: Sat, 27 Jan 2024 20:28:06 GMT  
		Size: 17.4 KB (17446 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; 386

```console
$ docker pull irssi@sha256:387d4dc6384ebea47ed5276a5865acb546bb67dfc227fe393dc75db5d45852dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17557817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e96759752775aacd2fda0f53e8cf266fc1c7b3e068566a8fc8c2add735f586`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8086f06106cd7bdd94cddf1c7363b144b801cd672997d9fe81ed6ab8ae03891`  
		Last Modified: Sat, 27 Jan 2024 01:54:00 GMT  
		Size: 8.9 MB (8904430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d1dba1f614043dea1e85138edb339caa7e16cca6c013e81384bd9f7f1afe02`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a341596e873d51872b196d8782ad7c32261c5a181b99f1f2d4c8c053a35a752a`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 5.4 MB (5413031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:d7e896f39991af1e19a5fea9c4353550ddd15bbb4fa05afc17e02656c66c8104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.4 KB (992360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617babf31d74046af9500e49f9674cbad6f479da89ac7b7cb51ba62e91a8f83a`

```dockerfile
```

-	Layers:
	-	`sha256:b11bca7efa15aa00afe306253a110a6805f8d56ebdfb10ff646a51e2a4f69f81`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 975.0 KB (974985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4a8d0da397b1dded79f569fffc3082addee92a84c9f41f986ef310c44a72bf8`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 17.4 KB (17375 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; ppc64le

```console
$ docker pull irssi@sha256:a0a400f2133847c9bbfa653f898fc72042aac4b03cb1371156d8726812131313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18717231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0def155df329eeefa5360cf54f1657dc7731e2f631182fce7e96924a4cabb8`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc74fa4ba26fc8c0460833da6460f59a2b7fdb551209793e9177aa8e4f59346c`  
		Last Modified: Sat, 27 Jan 2024 09:47:30 GMT  
		Size: 9.7 MB (9736547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596eae301f8ffae57ffc8c11b668ca24b994f12d9935de6216884db8f13188d3`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65ab57b806e5436452de1e909990c85bf46bb183048518a40b3e91cceaa914d`  
		Last Modified: Sat, 27 Jan 2024 09:47:30 GMT  
		Size: 5.6 MB (5630906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:c822cd405d36a575a6a510133bbc7870de59eabfd7fc4a2bb9485e127fa82363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.9 KB (990946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00c5eb1975042e0f47315f4ba48ed6fe69fbb8e39eb0c845ac7edf8cea9bc47`

```dockerfile
```

-	Layers:
	-	`sha256:51daf79105767963a7bfa2160a6d94beb71eecf88329550e2f9150d944fc2a52`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 973.5 KB (973452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6afd3a59a575c01cda08047a63543de5e7a3b3293e87e18e1bb870d4a2df4e74`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 17.5 KB (17494 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine` - linux; s390x

```console
$ docker pull irssi@sha256:cb11647a91b30743f090d9c0e26aeb8ac9ad300c50b661af12505ae290befd40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18707370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891ea14f0ba63e76c3bf45e2ede5b212af9d872f0b77a89d369fed7f2d5bfd3a`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc77a74801be7299707a33e8a653a76c9c5b8d7289fad0e44f86f0eb950c0dfb`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 10.1 MB (10082896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f5141af0a2579801617b6ef53cc8da747d109de43e1b88c92ba151618c1c12`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7efe871fc37a59627f7fb75e2cd481a361e23ae4423cbd5c60ebfd9cfc40ce4`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 5.4 MB (5405651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine` - unknown; unknown

```console
$ docker pull irssi@sha256:703020e7529818ace6da7d3f3424df173c4f428cf3fdaadb5bfb9d5a806ea431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.8 KB (990826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168cdfdbfc8e0c3b5a619ac19b836bbfce7a1baa6ab36ceaeb816e42d0073b3f`

```dockerfile
```

-	Layers:
	-	`sha256:a2f8050d7c3f109cc73636ae770c90e2cde71f2ed0dcd93078524351667493a8`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 973.4 KB (973394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304d7cd47112bf0ace221c02f2bdff3de634bfada70e48aad5065bc3c7424e87`  
		Last Modified: Sun, 28 Jan 2024 09:20:59 GMT  
		Size: 17.4 KB (17432 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:alpine3.18`

```console
$ docker pull irssi@sha256:294a5ddd1a7991782f7df46f7f0b1ef870818a1cf3a9afc37399222c27fa95cc
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 14
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm variant v6
	-	unknown; unknown
	-	linux; arm variant v7
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown
	-	linux; 386
	-	unknown; unknown
	-	linux; ppc64le
	-	unknown; unknown
	-	linux; s390x
	-	unknown; unknown

### `irssi:alpine3.18` - linux; amd64

```console
$ docker pull irssi@sha256:ef6c7693f4591e49ec7ebb9d9e3ff118d31da2e6e989cc01d7c4ba68d6ab312e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.5 MB (18451473 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c33d0b6133f016daecdc32847e2719e1b8377593ca3a157e4e2182ec699b3619`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:60d5073c9dc162f6d73c33561ca62b1f3d4afe73e51dfe01bc3bdbe570603526`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 9.6 MB (9645490 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cfaa94b168ed27385c169187548faa3944812324045e5b7d4f9fa0141d934de7`  
		Last Modified: Sat, 27 Jan 2024 00:53:19 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b33ada92546b652616e31a208091cb77dc65019c90e5944f396554ea13e63472`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 5.4 MB (5402150 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:d7192c220068161f91626a3d88eb71585cea3908b88e32bc9d7a200ba73e04f1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.5 KB (992458 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a3e03dcb09479e1e99b8f120055916a32994d838a16cdeba603eb3779a35bdb3`

```dockerfile
```

-	Layers:
	-	`sha256:2d6761df79ddf9480ea4aa104a72a140a5347d5dea19b3eb975a78d2a144483b`  
		Last Modified: Sat, 27 Jan 2024 00:53:20 GMT  
		Size: 975.0 KB (975030 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:9f3ba2fd4c9e25b6b8c3ce87fda3494b8506f3cebb1bc0e371df70b3a1c44a87`  
		Last Modified: Sat, 27 Jan 2024 00:53:19 GMT  
		Size: 17.4 KB (17428 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.18` - linux; arm variant v6

```console
$ docker pull irssi@sha256:11cdd850f01f7020ea3dc559a1cacf1710ce7e1110b2b3be3d5088a753388e41
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 MB (17270571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:980aff2e9d7fdabd52ca418744d9e75a16f305953ff369624a6f3e91ee563444`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e1caa0b93da06dd2aa46cce7a3fd9bbc4b0b58ff19b6dee6450b493cb819f9cd`  
		Last Modified: Tue, 30 Jan 2024 18:54:03 GMT  
		Size: 8.9 MB (8880054 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:93390793c8d561bd6d0fed103d923be9845e322d71b5187396645909aee925df`  
		Last Modified: Tue, 30 Jan 2024 18:54:02 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0db82a85a709f0d1d93b2c72989821c461582c5c99c841cb1d8529c32826084d`  
		Last Modified: Tue, 30 Jan 2024 18:54:03 GMT  
		Size: 5.2 MB (5242167 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:bd1dc317b136af3a211fed01816891cbea3e545a66d52fec0a8cfe3c9ae9a9bf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.3 KB (17341 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af05cb00d364bd5dc1c1184bb77489a40ba8096333fcb8ad4b6969822a45b3ac`

```dockerfile
```

-	Layers:
	-	`sha256:7a7a2bdaf6762372aa21871c515a18d90c4cfa782df359a7f10dcafb1a8acbcf`  
		Last Modified: Tue, 30 Jan 2024 18:54:02 GMT  
		Size: 17.3 KB (17341 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.18` - linux; arm variant v7

```console
$ docker pull irssi@sha256:89e22268640c72b2ae0efb98e009b34bd5534ad6c4aa596df74bfd27c1775e21
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **16.6 MB (16630432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0b9bff58300e84d8932cb47d4638ebdafbd9eb55888c2cfe35e7c89ce11cacec`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:46464fd9557915ea434ccac5505de2df053c83ad36eb366d24d2ec8a8c74d466 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:19ffc66afc416e14f8733d680abfae4e1f6a3c90ae23c045857121fea320862b`  
		Last Modified: Sat, 27 Jan 2024 00:15:39 GMT  
		Size: 2.9 MB (2901392 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cf9a728625b39c4526fc00d553e9ad76abf2d838e770db539a4503401b8151b7`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 8.7 MB (8721243 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:80dec7634cb6fd64dad041788335bf81e0374c155777e94d292608fadbc918e3`  
		Last Modified: Sat, 27 Jan 2024 16:10:09 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5a274dbd32034295ddcbc1067913cee45ae78dfd48bcfa5a5a0227438b251e6c`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 5.0 MB (5006505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:81909a4824efd52f673139f1bfce8946affddffd9073b10d3429fc7e6a25b6a4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **995.1 KB (995130 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4f8bf5414c3b8dabe31b6645b897840a59666ed989623f0fa633e51cd171a51`

```dockerfile
```

-	Layers:
	-	`sha256:788b342a7afe442fa8cc36f28d56399fe0b0abcded67366d9cfc6f4414ec6b28`  
		Last Modified: Sat, 27 Jan 2024 16:10:10 GMT  
		Size: 977.6 KB (977574 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8af9e565fad9e84cc85a9eb745382b7350da37e969b74d2723023407a1dc827b`  
		Last Modified: Sat, 27 Jan 2024 16:10:09 GMT  
		Size: 17.6 KB (17556 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.18` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:f967a5aba07f362a1fc42968dc5c25d932ddf7c5afc29b87f3e103f41e11b3ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 MB (18316080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3b852dcd533ac6fef70eee55ddc2eb8cd1a1a2438f10c7fb9780fcc8f8c53ae7`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:427b55bea52be9d140397d36bdf44940754b11f701ab1c8860bf265108864474`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 9.7 MB (9672879 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3172290de02d764723938f6bbf53611e992dca7775d89910602a51d4fdc12c0c`  
		Last Modified: Sat, 27 Jan 2024 20:28:06 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c4046f82759ffd91ca630dba178059b2985f3ec4fb9cb5a8d928a59215b0b5b2`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 5.3 MB (5308548 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:b68051a5d753ec8037cd2f9d14313c65e2bf5d4c67f564eec3f3f58eb4a131b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.5 KB (992495 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7edf1b50c168b27a6f3a5f6a4b2a2711df8f7bd7bbfdc93ea5eef3a8861c5e0c`

```dockerfile
```

-	Layers:
	-	`sha256:f636b4606a093b4d77ac5276a6d5402ca1ff4b0641b2656d45bb27ff2ed683af`  
		Last Modified: Sat, 27 Jan 2024 20:28:07 GMT  
		Size: 975.0 KB (975049 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e0aae570a126a40b9525d270285ba0d643a33c387a1f9f79698263d38a935f73`  
		Last Modified: Sat, 27 Jan 2024 20:28:06 GMT  
		Size: 17.4 KB (17446 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.18` - linux; 386

```console
$ docker pull irssi@sha256:387d4dc6384ebea47ed5276a5865acb546bb67dfc227fe393dc75db5d45852dd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **17.6 MB (17557817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27e96759752775aacd2fda0f53e8cf266fc1c7b3e068566a8fc8c2add735f586`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c8086f06106cd7bdd94cddf1c7363b144b801cd672997d9fe81ed6ab8ae03891`  
		Last Modified: Sat, 27 Jan 2024 01:54:00 GMT  
		Size: 8.9 MB (8904430 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:85d1dba1f614043dea1e85138edb339caa7e16cca6c013e81384bd9f7f1afe02`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a341596e873d51872b196d8782ad7c32261c5a181b99f1f2d4c8c053a35a752a`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 5.4 MB (5413031 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:d7e896f39991af1e19a5fea9c4353550ddd15bbb4fa05afc17e02656c66c8104
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **992.4 KB (992360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:617babf31d74046af9500e49f9674cbad6f479da89ac7b7cb51ba62e91a8f83a`

```dockerfile
```

-	Layers:
	-	`sha256:b11bca7efa15aa00afe306253a110a6805f8d56ebdfb10ff646a51e2a4f69f81`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 975.0 KB (974985 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a4a8d0da397b1dded79f569fffc3082addee92a84c9f41f986ef310c44a72bf8`  
		Last Modified: Sat, 27 Jan 2024 01:53:59 GMT  
		Size: 17.4 KB (17375 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.18` - linux; ppc64le

```console
$ docker pull irssi@sha256:a0a400f2133847c9bbfa653f898fc72042aac4b03cb1371156d8726812131313
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18717231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac0def155df329eeefa5360cf54f1657dc7731e2f631182fce7e96924a4cabb8`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:9adfbd84cce437533ba2c9cac17cd508a477a1a94523005875b2f04ddac20112 in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:08384a48688a8dcab52a530af58b9cbe1f870dd11e2ef2d0d645d658bd2ac537`  
		Last Modified: Sat, 27 Jan 2024 00:28:24 GMT  
		Size: 3.3 MB (3348487 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fc74fa4ba26fc8c0460833da6460f59a2b7fdb551209793e9177aa8e4f59346c`  
		Last Modified: Sat, 27 Jan 2024 09:47:30 GMT  
		Size: 9.7 MB (9736547 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:596eae301f8ffae57ffc8c11b668ca24b994f12d9935de6216884db8f13188d3`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e65ab57b806e5436452de1e909990c85bf46bb183048518a40b3e91cceaa914d`  
		Last Modified: Sat, 27 Jan 2024 09:47:30 GMT  
		Size: 5.6 MB (5630906 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:c822cd405d36a575a6a510133bbc7870de59eabfd7fc4a2bb9485e127fa82363
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.9 KB (990946 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e00c5eb1975042e0f47315f4ba48ed6fe69fbb8e39eb0c845ac7edf8cea9bc47`

```dockerfile
```

-	Layers:
	-	`sha256:51daf79105767963a7bfa2160a6d94beb71eecf88329550e2f9150d944fc2a52`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 973.5 KB (973452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6afd3a59a575c01cda08047a63543de5e7a3b3293e87e18e1bb870d4a2df4e74`  
		Last Modified: Sat, 27 Jan 2024 09:47:29 GMT  
		Size: 17.5 KB (17494 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:alpine3.18` - linux; s390x

```console
$ docker pull irssi@sha256:cb11647a91b30743f090d9c0e26aeb8ac9ad300c50b661af12505ae290befd40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.7 MB (18707370 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:891ea14f0ba63e76c3bf45e2ede5b212af9d872f0b77a89d369fed7f2d5bfd3a`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:191985024ed5be9a747edd5501846e6799b10e6ec729cc95d33625e1f5fed04f in / 
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["/bin/sh"]
# Tue, 03 Oct 2023 09:06:10 GMT
RUN apk add --no-cache 		ca-certificates 		perl-libwww # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV HOME=/home/user
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 	adduser -u 1001 -D -h "$HOME" user; 	mkdir "$HOME/.irssi"; 	chown -R user:user "$HOME" # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
ENV LANG=C.UTF-8
# Tue, 03 Oct 2023 09:06:10 GMT
ENV IRSSI_VERSION=1.4.5
# Tue, 03 Oct 2023 09:06:10 GMT
RUN set -eux; 		apk add --no-cache --virtual .build-deps 		coreutils 		gcc 		glib-dev 		gnupg 		libc-dev 		libtool 		lynx 		meson 		ncurses-dev 		ninja 		openssl 		openssl-dev 		perl-dev 		pkgconf 		tar 		xz 	; 		wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz" -O /tmp/irssi.tar.xz; 	wget "https://github.com/irssi/irssi/releases/download/${IRSSI_VERSION}/irssi-${IRSSI_VERSION}.tar.xz.asc" -O /tmp/irssi.tar.xz.asc; 	export GNUPGHOME="$(mktemp -d)"; 	gpg --batch --keyserver keyserver.ubuntu.com --recv-keys 7EE65E3082A5FB06AC7C368D00CCB587DDBEF0E1; 	gpg --batch --verify /tmp/irssi.tar.xz.asc /tmp/irssi.tar.xz; 	gpgconf --kill all; 	rm -rf "$GNUPGHOME" /tmp/irssi.tar.xz.asc; 		mkdir -p /usr/src/irssi; 	tar -xf /tmp/irssi.tar.xz -C /usr/src/irssi --strip-components 1; 	rm /tmp/irssi.tar.xz; 		cd /usr/src/irssi; 	meson 		-Denable-true-color=yes 		-Dwith-bot=yes 		-Dwith-perl=yes 		-Dwith-proxy=yes 		Build 	; 	ninja -C Build -j "$(nproc)"; 	ninja -C Build install; 		cd /; 	rm -rf /usr/src/irssi; 		runDeps="$( 		scanelf --needed --nobanner --format '%n#p' --recursive /usr/local 			| tr ',' '\n' 			| sort -u 			| awk 'system("[ -e /usr/local/lib/" $1 " ]") == 0 { next } { print "so:" $1 }' 	)"; 	apk add --no-network --virtual .irssi-rundeps $runDeps; 	apk del --no-network .build-deps; 		irssi --version # buildkit
# Tue, 03 Oct 2023 09:06:10 GMT
WORKDIR /home/user
# Tue, 03 Oct 2023 09:06:10 GMT
USER user
# Tue, 03 Oct 2023 09:06:10 GMT
CMD ["irssi"]
```

-	Layers:
	-	`sha256:61301311dfdb7c2627b8937a9c34ae4a82f4e16bb4ab80df35458b56bbbaee8b`  
		Last Modified: Sat, 27 Jan 2024 00:43:29 GMT  
		Size: 3.2 MB (3217530 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:dc77a74801be7299707a33e8a653a76c9c5b8d7289fad0e44f86f0eb950c0dfb`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 10.1 MB (10082896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f4f5141af0a2579801617b6ef53cc8da747d109de43e1b88c92ba151618c1c12`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a7efe871fc37a59627f7fb75e2cd481a361e23ae4423cbd5c60ebfd9cfc40ce4`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 5.4 MB (5405651 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:alpine3.18` - unknown; unknown

```console
$ docker pull irssi@sha256:703020e7529818ace6da7d3f3424df173c4f428cf3fdaadb5bfb9d5a806ea431
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **990.8 KB (990826 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:168cdfdbfc8e0c3b5a619ac19b836bbfce7a1baa6ab36ceaeb816e42d0073b3f`

```dockerfile
```

-	Layers:
	-	`sha256:a2f8050d7c3f109cc73636ae770c90e2cde71f2ed0dcd93078524351667493a8`  
		Last Modified: Sun, 28 Jan 2024 09:21:00 GMT  
		Size: 973.4 KB (973394 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:304d7cd47112bf0ace221c02f2bdff3de634bfada70e48aad5065bc3c7424e87`  
		Last Modified: Sun, 28 Jan 2024 09:20:59 GMT  
		Size: 17.4 KB (17432 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:bookworm`

```console
$ docker pull irssi@sha256:df2314e3c83d5dd353eafa769eee4302e869ca2782ba3906a63beb9c1e45d88b
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

### `irssi:bookworm` - linux; amd64

```console
$ docker pull irssi@sha256:f348397f4e94c8233af74fdea9b0e212e59940476974ab34d100894496547bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75868792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ba45dda22d90fa5e9e29f44f3c9db5d8f7ef6ab9a565f15845b3fc25c70ca2`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
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
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c80471fc9f279ecbb940d938880d5d417992f34809cffcc35de55e5c5b7b50`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 18.3 MB (18267918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2fe054dac6c8448486f7f83fb8d9a935f49600d14786eb028d05f1aca7be4d`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0c8cbf7b0f50debae5d2c4db813db40ef72d3f463d35255151d01f443c8f3b`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 28.5 MB (28473427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:0b4f3f615631a2195ca922bb269cc41ce0094ca6b506c2a6f42972e0edb4bb85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6635471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5bdb10eee477ea82a96d9db1c1a6ba2b86d46b4a80e1a99fc3067f614e5ead`

```dockerfile
```

-	Layers:
	-	`sha256:ad8396ba1d7eb23f85a9f1aa776ff1736aa74a41840bdb1336c90e8b0502ebd8`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 6.6 MB (6616868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97019d8cfce10dc023be567084137669d8fb7772cec7218f1e711f4cfae562dc`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 18.6 KB (18603 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v5

```console
$ docker pull irssi@sha256:87ad7b222f94bd4ffeda78eb7cf201ac297f22792db2eb6c627342cd68e91c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69868386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df3cfc1c8fffefd348cacfe8d18c9367e7b15f4227b2b32750bba9a1dad4eba`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:557a5348da1e680593a9ba709ef059b96baf15e0c89d8f8343e97bf008d9dc05 in / 
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
	-	`sha256:b508f3272b9b70b8dd19c621a4da1be63880a1f6412063787647ceeb464d772a`  
		Last Modified: Wed, 31 Jan 2024 22:48:00 GMT  
		Size: 26.9 MB (26909323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5389309a8aec1769eaeaa29319de4bebf1627abb4b7c25ceaef27190cd064cfc`  
		Last Modified: Thu, 01 Feb 2024 12:00:33 GMT  
		Size: 16.8 MB (16840201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31b408b37e2ea86da1e5dbb066b4b3fb5d09551561012dec426720879e0ebee`  
		Last Modified: Thu, 01 Feb 2024 12:00:32 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3f755d015144784b5213f297ec37d52ddb303651246f90287675b59fdb928e`  
		Last Modified: Thu, 01 Feb 2024 12:00:34 GMT  
		Size: 26.1 MB (26115505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:10fa924814f0100863a02d43cde888366c56bb1999d35f4ec2cb5458ede1d8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6608604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005c1e6b2319f0434d5ccdc6f83cedaf5c4931041228a3b257bf9d9d5fb2e4c2`

```dockerfile
```

-	Layers:
	-	`sha256:f0eebab35555f3e7c0ebb7213ba7f2f39f5d2117387aec58252ad62f3578ad40`  
		Last Modified: Thu, 01 Feb 2024 12:00:33 GMT  
		Size: 6.6 MB (6590040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32bd71fd61ddf99b170b9b0785a26c0ee132d0d4f5715fac60a135b66c6200a2`  
		Last Modified: Thu, 01 Feb 2024 12:00:32 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm variant v7

```console
$ docker pull irssi@sha256:acbb7bca937bcbdadea02ea51bd199c2c3cb20c4710043cabbf16dcbc82ec971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66192097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9882134ca1726fbcba90c8ffa149ba970b02f9ca5f6f67952d386a590416acb3`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
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
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710b5644e8d7ce9b22f8100f04ed12089274d8e6ecaa7b281e784390d9a624b7`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 16.4 MB (16432998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c9b75f1d3fb010ce226691f08e04e0eca369822f016344e74c988e7ff9cbd8`  
		Last Modified: Sat, 03 Feb 2024 11:14:04 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4b63d99a8fee13ec791237ca413916d8e6c7533abae83274d4674c855395`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 25.0 MB (25014178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:5741bec69a3a0a56fa45545bb9325a960c1706d417f5c2d6739b28b865f70c2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6609678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e40dd73c96b2bc78fa4fc0bc3ebf1c7edb34aeb93676b09737429a7b8d753b0`

```dockerfile
```

-	Layers:
	-	`sha256:72cf1412c4556bb0f02816b52887305bbd5ebccd80827e0404367c869478d2ed`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 6.6 MB (6591114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64c76402e6b60447a3e1c01a7d118cb99869ea18b5b76ebe57796f09cf7cea62`  
		Last Modified: Sat, 03 Feb 2024 11:14:04 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:ab01c34a30c278373d07d580043e8a18e72fdaedef7dda4a42dc222f7b997295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74448713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6936425758539b2ebe94594f0f57669ce6f225b3fda544a7169b3a8c918fcf70`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
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
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3ca413b8af66fc07e47a491183e81f2d8418a36f4b96f3bdf10c96382787ee`  
		Last Modified: Thu, 01 Feb 2024 15:38:27 GMT  
		Size: 17.8 MB (17832825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f66dbcdfcc246d829efadc3627c1885169a547fd80fcef2f9f380ffb2cbc82a`  
		Last Modified: Thu, 01 Feb 2024 15:38:26 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0c68f2c78a25389c67e4236b05e25abf97345db7813892b2d0e8f00ef530db`  
		Last Modified: Thu, 01 Feb 2024 15:38:28 GMT  
		Size: 27.4 MB (27431697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:9b2ce4726f911cecf3cdc2ce92874aa0c7a1d9991a3be9a1fdb8488f3507b3d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6615993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d78c2cfaac7640d2fba3d28b916ab8c140371df8abe66975d35d9d5a224e724`

```dockerfile
```

-	Layers:
	-	`sha256:88a3436d2dc5f0b5a747fedf9b08fd46e9fa64aa7be78c7dc416e4ec9fc043fa`  
		Last Modified: Thu, 01 Feb 2024 15:38:31 GMT  
		Size: 6.6 MB (6597539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:174c63d7fedd1ff225033ff0e20a26b24492ce336185f5f0c5ca8a39e2e2b217`  
		Last Modified: Thu, 01 Feb 2024 15:38:27 GMT  
		Size: 18.5 KB (18454 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; 386

```console
$ docker pull irssi@sha256:766da4d0c23a6b5a02fcfe6a9c290de6c880f481723bd162ec357b72a4b47a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76119263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6e2b48aea52eb23e814469cc9fee45495df60d11dcfcf7136304f394069c00`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:540e2de73452bd162dd7f630bf29f60e7d2e4a7a5d32a495bedf8ad390b59d7f in / 
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
	-	`sha256:34ef135b45f33052e8e5bca668f9a45a938944a9cf3fb73a46f54a7bf11f091b`  
		Last Modified: Wed, 31 Jan 2024 22:43:46 GMT  
		Size: 30.2 MB (30165018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dbf5ba1aef114655d4178cb7b25fc40be6cbbc4e74271ef3c0d129f27f7948`  
		Last Modified: Wed, 31 Jan 2024 23:55:35 GMT  
		Size: 17.6 MB (17592714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5c8ab8d6a9d2481fb1e6c046eda1e5bebc72c7171390e7918bbf3230a3a722`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f0f14697a5f1c37fedc3b6d79441454aa012edc2c624b113dab83f6ae387fe`  
		Last Modified: Wed, 31 Jan 2024 23:55:35 GMT  
		Size: 28.4 MB (28358174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:209fdc2b901e8609cc13ee3d75d5ddc3ddc5a77eb48684669e38db4fecc4c502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5adccb9448d759136b20f5bdf9d17e7b24e77b7f9ab897d4f7e971f758f79bba`

```dockerfile
```

-	Layers:
	-	`sha256:d1c4277341c5a786dc08c35575a05e75f388d342d5a278a44d83c0c37d739506`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 6.6 MB (6609873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ee0cd483b9775bf82c5f73475a171139475368fc3052df090bfb26cafea30e`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; mips64le

```console
$ docker pull irssi@sha256:5b07d620f6e0a5a433dafa6289d75943fe3f50b878b31f3b50428e645a145462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73891556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec83415acb7aaf453c85c9fbf2dcb484813439e60106ce3678051032190e571b`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
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
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0542ca44f4608abe3eb8928a6679f1310a135de5d26dcaef75fdfc7158cb3ea`  
		Last Modified: Thu, 01 Feb 2024 20:14:13 GMT  
		Size: 16.7 MB (16739448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5445b96f290754cc47514654bf406c8cf27af72cafe3c07122d2319baeab5c6`  
		Last Modified: Thu, 01 Feb 2024 20:14:11 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c99cf776ed9d9e58bad7c58c6a56f0e52654611186998435beea42f692d00d`  
		Last Modified: Thu, 01 Feb 2024 20:14:14 GMT  
		Size: 28.0 MB (28006308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:2374bfe0c2ed5ac9aa6c56cbcd7c04c3173332bc39faa38c57a475b929a9b702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2339be92d5d786c3309d29bedbceefe69adad7b0444bd27b86f0b90776e9a30`

```dockerfile
```

-	Layers:
	-	`sha256:28e3d51004b87049273ec1ea39d8930a3cfdd6cc05b2194a9e96b65bca71c335`  
		Last Modified: Thu, 01 Feb 2024 20:14:11 GMT  
		Size: 18.3 KB (18320 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; ppc64le

```console
$ docker pull irssi@sha256:99fee1cd7190e2738316eca944f9cb4474388bdcdff44d4e7492808c79c1838a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81689464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a168acd494049e622c9716bfe5c16cc1c017bea4033b8fe102da9b3f41c70dc`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:fca8b919a8d1e36420dd1e3f3e427aaaae28a2f57e46c27207acd8e3df0d7a97 in / 
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
	-	`sha256:dfeacd5cd8171f4516ea86dadfb60a372eabf49428dc23d2efdda68cff5b05e7`  
		Last Modified: Wed, 31 Jan 2024 22:34:24 GMT  
		Size: 33.1 MB (33142917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a3bd8096c05f1674995eeb051e3cdf023bbca5505b3f75e624f37c5b13e1b3`  
		Last Modified: Thu, 01 Feb 2024 12:57:44 GMT  
		Size: 18.6 MB (18565973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c5b4610ff6d9b857d7b8bcbc7a90224f918f31c45540cb15c1625a86bf95bc`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcf5f7f76af69ab342a135aed7b0fe5dab9ec932f2bcaeeb58cf8e9491096cb`  
		Last Modified: Thu, 01 Feb 2024 12:57:44 GMT  
		Size: 30.0 MB (29977216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:e5e62f13b43055d9255623225d660999c6209f6cbc9413307aaea737b381644f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6627686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bceb9b0ed2cbb811589e573c40c51eef92a381ce1039e4c4a81f5bfef5f2d0db`

```dockerfile
```

-	Layers:
	-	`sha256:5faeac8a64644b64f37809aa623f431a2453aa3dc443ad2173158318e03ae6ec`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 6.6 MB (6609185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f23996cea2f94cdfa72579bfbb5a59af44283d6b74f21f3d83612614d8698f3`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:bookworm` - linux; s390x

```console
$ docker pull irssi@sha256:3be6d24893ec88d5484e2c6ff47dabe648e0c56d532619254ec2005f79b316f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72553121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eeb87370bfa6742ae5cdffe4e9e5fbcded5a376ea20cb9f0ff781310654cff`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
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
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4594bbef0c3ed6e5d274cc97e215f696416fa4ae17044dfd8fe130e789bbc1`  
		Last Modified: Tue, 06 Feb 2024 11:27:01 GMT  
		Size: 18.0 MB (18014343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb84559c99fdfcc14828d4d1d39640bc61b21c99711be784b356d5c32b0fc8a7`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f15c7c91a157b6cb1adb4e9eff1265e940d9ae9d78fa1d5396c6d03f14b7e6e`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 27.0 MB (27021938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:bookworm` - unknown; unknown

```console
$ docker pull irssi@sha256:2c98314fd3cf3cdcc7aca67a7f251b24cb5c0f597abe52b639fda52f8631094b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6624174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1856fea1ea1713d5b1fe2b0ff097f7d0a688d0bd16c23f7de87310eb9f37a7a8`

```dockerfile
```

-	Layers:
	-	`sha256:e65ba0bc6f82ed76a16bdbe6b6618f3835b881b23d55dbc63e573dc31c537b19`  
		Last Modified: Tue, 06 Feb 2024 11:27:01 GMT  
		Size: 6.6 MB (6605739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01339a4362670ca4baef375e49a866c7339d89de67789528e853a5a62dd0a787`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 18.4 KB (18435 bytes)  
		MIME: application/vnd.in-toto+json

## `irssi:latest`

```console
$ docker pull irssi@sha256:df2314e3c83d5dd353eafa769eee4302e869ca2782ba3906a63beb9c1e45d88b
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
$ docker pull irssi@sha256:f348397f4e94c8233af74fdea9b0e212e59940476974ab34d100894496547bbb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.9 MB (75868792 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d3ba45dda22d90fa5e9e29f44f3c9db5d8f7ef6ab9a565f15845b3fc25c70ca2`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:eb6a3def1f69e76655620640e610015f285bc23c97e89855feb1f0548309d518 in / 
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
	-	`sha256:e1caac4eb9d2ec24aa3618e5992208321a92492aef5fef5eb9e470895f771c56`  
		Last Modified: Tue, 13 Feb 2024 00:42:02 GMT  
		Size: 29.1 MB (29124091 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3c80471fc9f279ecbb940d938880d5d417992f34809cffcc35de55e5c5b7b50`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 18.3 MB (18267918 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:da2fe054dac6c8448486f7f83fb8d9a935f49600d14786eb028d05f1aca7be4d`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bc0c8cbf7b0f50debae5d2c4db813db40ef72d3f463d35255151d01f443c8f3b`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 28.5 MB (28473427 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:0b4f3f615631a2195ca922bb269cc41ce0094ca6b506c2a6f42972e0edb4bb85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6635471 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b5bdb10eee477ea82a96d9db1c1a6ba2b86d46b4a80e1a99fc3067f614e5ead`

```dockerfile
```

-	Layers:
	-	`sha256:ad8396ba1d7eb23f85a9f1aa776ff1736aa74a41840bdb1336c90e8b0502ebd8`  
		Last Modified: Tue, 13 Feb 2024 01:53:56 GMT  
		Size: 6.6 MB (6616868 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:97019d8cfce10dc023be567084137669d8fb7772cec7218f1e711f4cfae562dc`  
		Last Modified: Tue, 13 Feb 2024 01:53:55 GMT  
		Size: 18.6 KB (18603 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v5

```console
$ docker pull irssi@sha256:87ad7b222f94bd4ffeda78eb7cf201ac297f22792db2eb6c627342cd68e91c1c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.9 MB (69868386 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6df3cfc1c8fffefd348cacfe8d18c9367e7b15f4227b2b32750bba9a1dad4eba`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:557a5348da1e680593a9ba709ef059b96baf15e0c89d8f8343e97bf008d9dc05 in / 
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
	-	`sha256:b508f3272b9b70b8dd19c621a4da1be63880a1f6412063787647ceeb464d772a`  
		Last Modified: Wed, 31 Jan 2024 22:48:00 GMT  
		Size: 26.9 MB (26909323 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5389309a8aec1769eaeaa29319de4bebf1627abb4b7c25ceaef27190cd064cfc`  
		Last Modified: Thu, 01 Feb 2024 12:00:33 GMT  
		Size: 16.8 MB (16840201 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d31b408b37e2ea86da1e5dbb066b4b3fb5d09551561012dec426720879e0ebee`  
		Last Modified: Thu, 01 Feb 2024 12:00:32 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a3f755d015144784b5213f297ec37d52ddb303651246f90287675b59fdb928e`  
		Last Modified: Thu, 01 Feb 2024 12:00:34 GMT  
		Size: 26.1 MB (26115505 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:10fa924814f0100863a02d43cde888366c56bb1999d35f4ec2cb5458ede1d8bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6608604 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:005c1e6b2319f0434d5ccdc6f83cedaf5c4931041228a3b257bf9d9d5fb2e4c2`

```dockerfile
```

-	Layers:
	-	`sha256:f0eebab35555f3e7c0ebb7213ba7f2f39f5d2117387aec58252ad62f3578ad40`  
		Last Modified: Thu, 01 Feb 2024 12:00:33 GMT  
		Size: 6.6 MB (6590040 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:32bd71fd61ddf99b170b9b0785a26c0ee132d0d4f5715fac60a135b66c6200a2`  
		Last Modified: Thu, 01 Feb 2024 12:00:32 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm variant v7

```console
$ docker pull irssi@sha256:acbb7bca937bcbdadea02ea51bd199c2c3cb20c4710043cabbf16dcbc82ec971
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.2 MB (66192097 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9882134ca1726fbcba90c8ffa149ba970b02f9ca5f6f67952d386a590416acb3`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:d6072ced9736ca566086eea2514cf12faccec9859bbd93e83950ad51f6827e8c in / 
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
	-	`sha256:404006a0fd99beed6ef1a9502692bd5005ae8c3b9d36a9b48654f7dfaacfb2c5`  
		Last Modified: Wed, 31 Jan 2024 22:48:51 GMT  
		Size: 24.7 MB (24741565 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:710b5644e8d7ce9b22f8100f04ed12089274d8e6ecaa7b281e784390d9a624b7`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 16.4 MB (16432998 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:20c9b75f1d3fb010ce226691f08e04e0eca369822f016344e74c988e7ff9cbd8`  
		Last Modified: Sat, 03 Feb 2024 11:14:04 GMT  
		Size: 3.3 KB (3324 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ed5e4b63d99a8fee13ec791237ca413916d8e6c7533abae83274d4674c855395`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 25.0 MB (25014178 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:5741bec69a3a0a56fa45545bb9325a960c1706d417f5c2d6739b28b865f70c2a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6609678 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e40dd73c96b2bc78fa4fc0bc3ebf1c7edb34aeb93676b09737429a7b8d753b0`

```dockerfile
```

-	Layers:
	-	`sha256:72cf1412c4556bb0f02816b52887305bbd5ebccd80827e0404367c869478d2ed`  
		Last Modified: Sat, 03 Feb 2024 11:14:05 GMT  
		Size: 6.6 MB (6591114 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:64c76402e6b60447a3e1c01a7d118cb99869ea18b5b76ebe57796f09cf7cea62`  
		Last Modified: Sat, 03 Feb 2024 11:14:04 GMT  
		Size: 18.6 KB (18564 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:ab01c34a30c278373d07d580043e8a18e72fdaedef7dda4a42dc222f7b997295
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.4 MB (74448713 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6936425758539b2ebe94594f0f57669ce6f225b3fda544a7169b3a8c918fcf70`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:ef6f078c1e72fcfafb9bfeeff0c1c771219dc2efe34650963106f63d32183b49 in / 
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
	-	`sha256:25d3892798f8b99159e3c1136799bfed560027ce451b50d57d961f4f02577ff5`  
		Last Modified: Wed, 31 Jan 2024 22:48:07 GMT  
		Size: 29.2 MB (29180832 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ae3ca413b8af66fc07e47a491183e81f2d8418a36f4b96f3bdf10c96382787ee`  
		Last Modified: Thu, 01 Feb 2024 15:38:27 GMT  
		Size: 17.8 MB (17832825 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9f66dbcdfcc246d829efadc3627c1885169a547fd80fcef2f9f380ffb2cbc82a`  
		Last Modified: Thu, 01 Feb 2024 15:38:26 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8b0c68f2c78a25389c67e4236b05e25abf97345db7813892b2d0e8f00ef530db`  
		Last Modified: Thu, 01 Feb 2024 15:38:28 GMT  
		Size: 27.4 MB (27431697 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:9b2ce4726f911cecf3cdc2ce92874aa0c7a1d9991a3be9a1fdb8488f3507b3d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6615993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4d78c2cfaac7640d2fba3d28b916ab8c140371df8abe66975d35d9d5a224e724`

```dockerfile
```

-	Layers:
	-	`sha256:88a3436d2dc5f0b5a747fedf9b08fd46e9fa64aa7be78c7dc416e4ec9fc043fa`  
		Last Modified: Thu, 01 Feb 2024 15:38:31 GMT  
		Size: 6.6 MB (6597539 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:174c63d7fedd1ff225033ff0e20a26b24492ce336185f5f0c5ca8a39e2e2b217`  
		Last Modified: Thu, 01 Feb 2024 15:38:27 GMT  
		Size: 18.5 KB (18454 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; 386

```console
$ docker pull irssi@sha256:766da4d0c23a6b5a02fcfe6a9c290de6c880f481723bd162ec357b72a4b47a28
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.1 MB (76119263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd6e2b48aea52eb23e814469cc9fee45495df60d11dcfcf7136304f394069c00`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:540e2de73452bd162dd7f630bf29f60e7d2e4a7a5d32a495bedf8ad390b59d7f in / 
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
	-	`sha256:34ef135b45f33052e8e5bca668f9a45a938944a9cf3fb73a46f54a7bf11f091b`  
		Last Modified: Wed, 31 Jan 2024 22:43:46 GMT  
		Size: 30.2 MB (30165018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c2dbf5ba1aef114655d4178cb7b25fc40be6cbbc4e74271ef3c0d129f27f7948`  
		Last Modified: Wed, 31 Jan 2024 23:55:35 GMT  
		Size: 17.6 MB (17592714 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2e5c8ab8d6a9d2481fb1e6c046eda1e5bebc72c7171390e7918bbf3230a3a722`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94f0f14697a5f1c37fedc3b6d79441454aa012edc2c624b113dab83f6ae387fe`  
		Last Modified: Wed, 31 Jan 2024 23:55:35 GMT  
		Size: 28.4 MB (28358174 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:209fdc2b901e8609cc13ee3d75d5ddc3ddc5a77eb48684669e38db4fecc4c502
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6628423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5adccb9448d759136b20f5bdf9d17e7b24e77b7f9ab897d4f7e971f758f79bba`

```dockerfile
```

-	Layers:
	-	`sha256:d1c4277341c5a786dc08c35575a05e75f388d342d5a278a44d83c0c37d739506`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 6.6 MB (6609873 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b4ee0cd483b9775bf82c5f73475a171139475368fc3052df090bfb26cafea30e`  
		Last Modified: Wed, 31 Jan 2024 23:55:34 GMT  
		Size: 18.6 KB (18550 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; mips64le

```console
$ docker pull irssi@sha256:5b07d620f6e0a5a433dafa6289d75943fe3f50b878b31f3b50428e645a145462
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.9 MB (73891556 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ec83415acb7aaf453c85c9fbf2dcb484813439e60106ce3678051032190e571b`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:c38ae3175b2ea7bff74f0e28558af27158de7697be9142ed9d681c4d37b24e35 in / 
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
	-	`sha256:21bfa6f58b3ab30099793f844be56212a593fddbf3f030cd8c42b38a1dcefcff`  
		Last Modified: Wed, 31 Jan 2024 22:38:21 GMT  
		Size: 29.1 MB (29142437 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f0542ca44f4608abe3eb8928a6679f1310a135de5d26dcaef75fdfc7158cb3ea`  
		Last Modified: Thu, 01 Feb 2024 20:14:13 GMT  
		Size: 16.7 MB (16739448 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d5445b96f290754cc47514654bf406c8cf27af72cafe3c07122d2319baeab5c6`  
		Last Modified: Thu, 01 Feb 2024 20:14:11 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56c99cf776ed9d9e58bad7c58c6a56f0e52654611186998435beea42f692d00d`  
		Last Modified: Thu, 01 Feb 2024 20:14:14 GMT  
		Size: 28.0 MB (28006308 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:2374bfe0c2ed5ac9aa6c56cbcd7c04c3173332bc39faa38c57a475b929a9b702
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **18.3 KB (18320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2339be92d5d786c3309d29bedbceefe69adad7b0444bd27b86f0b90776e9a30`

```dockerfile
```

-	Layers:
	-	`sha256:28e3d51004b87049273ec1ea39d8930a3cfdd6cc05b2194a9e96b65bca71c335`  
		Last Modified: Thu, 01 Feb 2024 20:14:11 GMT  
		Size: 18.3 KB (18320 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; ppc64le

```console
$ docker pull irssi@sha256:99fee1cd7190e2738316eca944f9cb4474388bdcdff44d4e7492808c79c1838a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81689464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a168acd494049e622c9716bfe5c16cc1c017bea4033b8fe102da9b3f41c70dc`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:fca8b919a8d1e36420dd1e3f3e427aaaae28a2f57e46c27207acd8e3df0d7a97 in / 
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
	-	`sha256:dfeacd5cd8171f4516ea86dadfb60a372eabf49428dc23d2efdda68cff5b05e7`  
		Last Modified: Wed, 31 Jan 2024 22:34:24 GMT  
		Size: 33.1 MB (33142917 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:67a3bd8096c05f1674995eeb051e3cdf023bbca5505b3f75e624f37c5b13e1b3`  
		Last Modified: Thu, 01 Feb 2024 12:57:44 GMT  
		Size: 18.6 MB (18565973 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:11c5b4610ff6d9b857d7b8bcbc7a90224f918f31c45540cb15c1625a86bf95bc`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7fcf5f7f76af69ab342a135aed7b0fe5dab9ec932f2bcaeeb58cf8e9491096cb`  
		Last Modified: Thu, 01 Feb 2024 12:57:44 GMT  
		Size: 30.0 MB (29977216 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:e5e62f13b43055d9255623225d660999c6209f6cbc9413307aaea737b381644f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6627686 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bceb9b0ed2cbb811589e573c40c51eef92a381ce1039e4c4a81f5bfef5f2d0db`

```dockerfile
```

-	Layers:
	-	`sha256:5faeac8a64644b64f37809aa623f431a2453aa3dc443ad2173158318e03ae6ec`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 6.6 MB (6609185 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6f23996cea2f94cdfa72579bfbb5a59af44283d6b74f21f3d83612614d8698f3`  
		Last Modified: Thu, 01 Feb 2024 12:57:43 GMT  
		Size: 18.5 KB (18501 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:latest` - linux; s390x

```console
$ docker pull irssi@sha256:3be6d24893ec88d5484e2c6ff47dabe648e0c56d532619254ec2005f79b316f8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.6 MB (72553121 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b1eeb87370bfa6742ae5cdffe4e9e5fbcded5a376ea20cb9f0ff781310654cff`
-	Default Command: `["irssi"]`

```dockerfile
# Tue, 03 Oct 2023 09:06:10 GMT
ADD file:d543e4bc70d0d1d81c594a97289d7f2b4925d86461644cf881890997abfb6ead in / 
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
	-	`sha256:84abfb784f629f520e19ebd281090b7f1b3b78ff96b3be919578a053d2708ad5`  
		Last Modified: Wed, 31 Jan 2024 23:29:10 GMT  
		Size: 27.5 MB (27513479 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6e4594bbef0c3ed6e5d274cc97e215f696416fa4ae17044dfd8fe130e789bbc1`  
		Last Modified: Tue, 06 Feb 2024 11:27:01 GMT  
		Size: 18.0 MB (18014343 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:cb84559c99fdfcc14828d4d1d39640bc61b21c99711be784b356d5c32b0fc8a7`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0f15c7c91a157b6cb1adb4e9eff1265e940d9ae9d78fa1d5396c6d03f14b7e6e`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 27.0 MB (27021938 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Tue, 07 Mar 2017 15:01:14 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:latest` - unknown; unknown

```console
$ docker pull irssi@sha256:2c98314fd3cf3cdcc7aca67a7f251b24cb5c0f597abe52b639fda52f8631094b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **6.6 MB (6624174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1856fea1ea1713d5b1fe2b0ff097f7d0a688d0bd16c23f7de87310eb9f37a7a8`

```dockerfile
```

-	Layers:
	-	`sha256:e65ba0bc6f82ed76a16bdbe6b6618f3835b881b23d55dbc63e573dc31c537b19`  
		Last Modified: Tue, 06 Feb 2024 11:27:01 GMT  
		Size: 6.6 MB (6605739 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:01339a4362670ca4baef375e49a866c7339d89de67789528e853a5a62dd0a787`  
		Last Modified: Tue, 06 Feb 2024 11:27:00 GMT  
		Size: 18.4 KB (18435 bytes)  
		MIME: application/vnd.in-toto+json
