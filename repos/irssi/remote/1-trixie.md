## `irssi:1-trixie`

```console
$ docker pull irssi@sha256:6efb57bea041c303bac62c5003143e3d1b736cdf6260975b0003f2d540bb62df
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

### `irssi:1-trixie` - linux; amd64

```console
$ docker pull irssi@sha256:97fe355e885196e7f6c03e8818e90b3408897a4242563efdd22c983a993c0a8c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.9 MB (53865436 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9e78b103b8dade34342904922d5072865992f695907f608a3006692d77077685`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'amd64' out/ 'trixie' '@1757289600'
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
	-	`sha256:ce1261c6d567efa8e3b457673eeeb474a0a8066df6bb95ca9a6a94a31e219dd3`  
		Last Modified: Mon, 08 Sep 2025 21:12:35 GMT  
		Size: 29.8 MB (29773495 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d53d900ec985caa6f950d4bece290e5d420e178382a84b15b032d1a6ce584a38`  
		Last Modified: Mon, 08 Sep 2025 21:57:52 GMT  
		Size: 19.2 MB (19222208 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6aa9be1176d5e0438c9cdeccefc2fe3c37b13bafd30c129f9dd282a21391eaa5`  
		Last Modified: Mon, 08 Sep 2025 21:35:06 GMT  
		Size: 3.3 KB (3325 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b430fe59c9cfd670a1444d5fa49a639c822d49896273966f1ad05d5e1cad1b16`  
		Last Modified: Mon, 08 Sep 2025 21:57:43 GMT  
		Size: 4.9 MB (4866376 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:a22963eb5b48dc3c81a50248506a1900b34c3e88c51ae33ab15075818e536eae
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607023 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89732f33bb8ba2ba4943b714f3418f9f973e462c23c255a857a306a954e5226a`

```dockerfile
```

-	Layers:
	-	`sha256:5311f0f0138879e60d8a6725396b665c75b5232061394cd42abfb3f4c797202f`  
		Last Modified: Mon, 08 Sep 2025 22:59:36 GMT  
		Size: 5.6 MB (5588329 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:40e0e9a6266575ea9f1cc5ce32120989faa9ffc0746e214ce0155df21ea26211`  
		Last Modified: Mon, 08 Sep 2025 22:59:37 GMT  
		Size: 18.7 KB (18694 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v5

```console
$ docker pull irssi@sha256:be4078db13c627f3e5697290a4f47b6ba52f6f9b6e31d062b9b66aea4c9f4ec5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50941741 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:729ae936a04dfc6ae97b9aed68c5147f321ef0ae398d72e8adb8ff53661303b0`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'armel' out/ 'trixie' '@1757289600'
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
	-	`sha256:5d61fc20e756831552727f89a087e2b45b07dace604ad2cda0a2afa80ace388d`  
		Last Modified: Mon, 08 Sep 2025 21:13:29 GMT  
		Size: 27.9 MB (27941760 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4975f116bd8ce8cbb5521a8a84e2ea292726ef1a0d3eb7524930ea44e01e6d65`  
		Last Modified: Mon, 08 Sep 2025 21:53:52 GMT  
		Size: 18.3 MB (18286947 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:04167ced4ec5bf3465cd8d648485d8d6c7411d90af9ba6193c3c1008fb47688d`  
		Last Modified: Mon, 08 Sep 2025 21:35:05 GMT  
		Size: 3.3 KB (3328 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:efd88d5833741eb0be4a0b17f5d90ab2b111a76fbb24de739be5345771bb5d15`  
		Last Modified: Mon, 08 Sep 2025 21:53:48 GMT  
		Size: 4.7 MB (4709674 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:04a63e03029e7a492ceb327829ef35f4ea626710cd49635adc67604d333e76a2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5604710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ab0fba7306e03301234c43fd7a7efadc19e49ac70b897687e78a52b3f2f97dfb`

```dockerfile
```

-	Layers:
	-	`sha256:4e572c22f196fa2358b93e1d5d7f0c38cf86a8600800dca67c285d2ac68f45bf`  
		Last Modified: Mon, 08 Sep 2025 22:59:42 GMT  
		Size: 5.6 MB (5585878 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:6ef10af60bef500cc05abaeaba2a29bbec1665a3b82a733897fe9d691196aa6d`  
		Last Modified: Mon, 08 Sep 2025 22:59:43 GMT  
		Size: 18.8 KB (18832 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm variant v7

```console
$ docker pull irssi@sha256:bb64cf6df2f5d05c74d1e8d2268f6661882ea77b4a1148103cf530f4d4ba77ba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48679233 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:02ccbb6f040193cb52e320ea59bc509b278451cbe33b821e13d6381d00d85e38`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'armhf' out/ 'trixie' '@1757289600'
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
	-	`sha256:c01338083e94735040ac705e73d3207fecb1a829de94334396239199538796bd`  
		Last Modified: Mon, 08 Sep 2025 21:13:56 GMT  
		Size: 26.2 MB (26207847 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4015d185ae3073400ffd614267535910eaa25d33bef0d0384fb07644fa672b6c`  
		Last Modified: Mon, 08 Sep 2025 21:54:08 GMT  
		Size: 17.9 MB (17909595 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0cc12d1b98fc4fb10eb78b652f6d93c57adde759ca50be2963e9339d8c04bd3c`  
		Last Modified: Mon, 08 Sep 2025 21:54:11 GMT  
		Size: 3.3 KB (3326 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:49d54fe1eb2c301197ae8866e01552e78857e7ba910a041fe1b503aef69c138b`  
		Last Modified: Mon, 08 Sep 2025 21:54:05 GMT  
		Size: 4.6 MB (4558433 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:625e60aa679a366635fa1b7e07abdfc12493903895f8e4690e637931daee49cd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f7d60b6957564b0f6b0a7e0bc9387cbfe1e713ad09abd78710619fdbe9af1d2c`

```dockerfile
```

-	Layers:
	-	`sha256:7a8f6c13288f5cf97ca9a3643eedff3a1f0a2500e96c79f72490dbebc308baad`  
		Last Modified: Mon, 08 Sep 2025 22:59:49 GMT  
		Size: 5.6 MB (5588900 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:e3c8ca5afedf2b09ab78fa1c1914738e8c6756f56314699c96e6e912ad6bc3c2`  
		Last Modified: Mon, 08 Sep 2025 22:59:50 GMT  
		Size: 18.8 KB (18832 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; arm64 variant v8

```console
$ docker pull irssi@sha256:52988d34803047e12055b9b450f451bf3b26c7fa0e2da7b9b629a3d4ac27c060
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53970852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:80fe411431ff6a2b2eade20bf653ef9662249d06b9b8c0d74900c4f6235994be`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'arm64' out/ 'trixie' '@1757289600'
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
	-	`sha256:b2feff975e6dd2ebaf182772fb9ee26274648387b061e821e0bb5026735dd094`  
		Last Modified: Mon, 08 Sep 2025 21:13:54 GMT  
		Size: 30.1 MB (30136631 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:71a0518d48d02cf53222a8ff36da8c2cf801b0cff47cc700ea8948e610d224e8`  
		Last Modified: Mon, 08 Sep 2025 21:56:21 GMT  
		Size: 19.0 MB (19049204 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3438495e1dca5df35724d10163c25e75181223cd181719d004c30929c9e4d27`  
		Last Modified: Mon, 08 Sep 2025 21:56:19 GMT  
		Size: 3.3 KB (3329 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ce1bd56028a7b2ba4355a1bfed7760f1d35e930d153825ec98a2aa01e07af5e8`  
		Last Modified: Mon, 08 Sep 2025 21:56:18 GMT  
		Size: 4.8 MB (4781656 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:19269c7b1c5f3a3283cb4e5cff0bbe9dc12797cc62bcf5e4ce1d2d5c0d256c07
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5613689 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83bb0b13eadc962b072abaa07338599949f36765ef0d5e3b646a3653dd14963f`

```dockerfile
```

-	Layers:
	-	`sha256:51c083102aa5a0ffa7ec32a52165cf4f444756d601c7ea7a6575b7a5966756e1`  
		Last Modified: Mon, 08 Sep 2025 22:59:56 GMT  
		Size: 5.6 MB (5594813 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:ebf877a495033ca06451037b7f44e83a164f4f8ddf72e4a96543f7287ceeae62`  
		Last Modified: Mon, 08 Sep 2025 22:59:57 GMT  
		Size: 18.9 KB (18876 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; 386

```console
$ docker pull irssi@sha256:3d3d99adde0bf578be156783bf6955ff29c522a5f11374c25547ea9168c0d045
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.9 MB (54902502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df04313058ecb223fcf2b97dc11a2823917eac45108b4604c5b4a498e6a408cf`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'i386' out/ 'trixie' '@1757289600'
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
	-	`sha256:d6e01c57fc6d674eef68e6bfe57a080b0a70c1c25810b7d6e769151bad3645bf`  
		Last Modified: Mon, 08 Sep 2025 21:12:32 GMT  
		Size: 31.3 MB (31289784 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d582fc0ca2e00e31fee72b9740f6b332316a995c8442be84a38e4ecba1109281`  
		Last Modified: Mon, 08 Sep 2025 21:57:06 GMT  
		Size: 18.7 MB (18741295 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:51673f5175091b1e883bd15f06de0b75a25569beaf3adf920b30f94e1a0da052`  
		Last Modified: Mon, 08 Sep 2025 21:35:09 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0ad4550937d735d09c483268d7cff8e1d9df87ba59bc747600d5841b8e2bf469`  
		Last Modified: Mon, 08 Sep 2025 21:57:09 GMT  
		Size: 4.9 MB (4868060 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:7dd093f9d10c564ab3ed4256fbf78cf3f0cb7569cdd32590e90c072c7a604859
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5603090 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3cefa6e6b54d4f3fd5232305bd16cf609e78526c2ffeec54694ad81d59625418`

```dockerfile
```

-	Layers:
	-	`sha256:91fdd559718a010ac4aa432125e0029eac613f7caf6a4e0f476fe5a7d77b7235`  
		Last Modified: Mon, 08 Sep 2025 23:00:03 GMT  
		Size: 5.6 MB (5584452 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:421c530e57382c8129edd0a656f4dcb98ff2c173f1e59bee40462e7182989170`  
		Last Modified: Mon, 08 Sep 2025 23:00:05 GMT  
		Size: 18.6 KB (18638 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; ppc64le

```console
$ docker pull irssi@sha256:7a621140dff5c933a16580e4e682c0d4cd63cd93f97b69f9d56e0be52a262562
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.2 MB (58237397 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ce85beccdd6b81be2b51f9fd1fad22c3b384331cd0c1266523e7091881f03b54`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 'ppc64el' out/ 'trixie' '@1757289600'
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
	-	`sha256:d11c44105444ef722eccd8c92c6b2fce9986e3274ba9b346e044a458c0425852`  
		Last Modified: Mon, 08 Sep 2025 22:03:02 GMT  
		Size: 33.6 MB (33594351 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8fa49b4abf95ab84d89bcb4ce107e30810565d01119db6e2af45945049f66f8c`  
		Last Modified: Mon, 08 Sep 2025 22:27:48 GMT  
		Size: 19.5 MB (19542493 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6ed86a10819063491921242873bfaae5652aca26b97b02155289b75b0b3413e0`  
		Last Modified: Mon, 08 Sep 2025 21:59:38 GMT  
		Size: 3.3 KB (3331 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:94a0a5767c719285e3ab801c06aee046ca7b6954914d38568e765046dc11b429`  
		Last Modified: Mon, 08 Sep 2025 22:27:50 GMT  
		Size: 5.1 MB (5097190 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:bddd38aaacc24173cefa954bae3c8661dcc666547807b7526a1254d8f5e9d6e2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5614125 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bac3054cf9370ca706b9634227df6a3ce19af0ad65d631c0d8c05ece865fd077`

```dockerfile
```

-	Layers:
	-	`sha256:96a21c7fe75ca573c585d5f98658825d7de80b73f77fe194e6bf031ae208a827`  
		Last Modified: Mon, 08 Sep 2025 23:00:11 GMT  
		Size: 5.6 MB (5595360 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:befcf449335f71a5084894e89812faad4ca34e7326fafedb88c4548b364be779`  
		Last Modified: Mon, 08 Sep 2025 23:00:12 GMT  
		Size: 18.8 KB (18765 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; riscv64

```console
$ docker pull irssi@sha256:8f8637fe913064cfbc2fa2bb1cb4d66ad28ee1a935d1238125764c4a4e763240
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51683694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66ca37ec8afd9d241d622fe15c2a65ebe38aa0a39d2fec0b43066f6fcec0a90e`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 00:00:00 GMT
RUN # debian.sh --arch 'riscv64' out/ 'trixie' '@1754870400'
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
	-	`sha256:a37386b9234ad75f65b5aa72f3d919ff0eb3bb18978566fa959d6e357480594c`  
		Last Modified: Wed, 13 Aug 2025 04:01:43 GMT  
		Size: 28.3 MB (28271623 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b3c06a3222e88ed840b1ac200e6df35a4a10c8f3a01b74a7367f2e7c64acedc8`  
		Last Modified: Wed, 13 Aug 2025 11:02:32 GMT  
		Size: 18.5 MB (18548816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8491db56a2d24536096f4792720b8538dceecbd4652a0a13b8b41d11f5a94811`  
		Last Modified: Wed, 13 Aug 2025 10:18:42 GMT  
		Size: 3.3 KB (3327 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1dec5c0bd1a94b2c01b2b10b2240f03e88b0e3366bce402601a13c24b233ff8d`  
		Last Modified: Wed, 13 Aug 2025 10:18:49 GMT  
		Size: 4.9 MB (4859896 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:29c57a7dd85bc4c527b4fda41ff482bba414e48cd3894dde90806188a669a88b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5597518 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:587eae02f903180e82164e4ffd9c42e981e35d70d66cdb4e1989c41f649f69f0`

```dockerfile
```

-	Layers:
	-	`sha256:4128ec00f64a84c3499b73eb7bbc428b797429fb8e0f9c6f9fbbb474f27f1b39`  
		Last Modified: Wed, 13 Aug 2025 10:59:44 GMT  
		Size: 5.6 MB (5578752 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:a2a9dc47f7df355b3fcca7036b52393f544e0dc74d7bafd2cb13271318213f49`  
		Last Modified: Wed, 13 Aug 2025 10:59:45 GMT  
		Size: 18.8 KB (18766 bytes)  
		MIME: application/vnd.in-toto+json

### `irssi:1-trixie` - linux; s390x

```console
$ docker pull irssi@sha256:69602baa19f13dbd80dc1fa90497ab6df52345e0257ab72c7f43f41f18ddc443
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.5 MB (54501969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3be375f84a070f6061271448ca0af7e32b17cf6692bc2bec9e68e545c453b702`
-	Default Command: `["irssi"]`

```dockerfile
# Mon, 11 Aug 2025 16:45:42 GMT
RUN # debian.sh --arch 's390x' out/ 'trixie' '@1757289600'
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
	-	`sha256:8af003c0cb712f415b555d33f1c4a9cc3fad82782766d388f3426c4d807a5ab2`  
		Last Modified: Mon, 08 Sep 2025 21:53:51 GMT  
		Size: 29.8 MB (29832904 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a8d7af71d3a3931ca909de58c09aa30b3decdccf1dc2e5dd6fc4fe09d26ad423`  
		Last Modified: Mon, 08 Sep 2025 22:09:53 GMT  
		Size: 19.8 MB (19759933 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2fc08faf9f65a5e8658d2380489898c9f59516fec0555e408f8af708723bbec`  
		Last Modified: Mon, 08 Sep 2025 21:47:10 GMT  
		Size: 3.3 KB (3322 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9a14b18f0b239284229a58b014836672e6fe3ce7de13f6fff494e75a29aef760`  
		Last Modified: Mon, 08 Sep 2025 22:09:56 GMT  
		Size: 4.9 MB (4905778 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `irssi:1-trixie` - unknown; unknown

```console
$ docker pull irssi@sha256:73f989e3e9eb79a3d18c32cb7e75cff1d7112321e0426c82f97b3c02f8b9f965
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **5.6 MB (5607928 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c685efa9dff783fd03ec35cee465e9594703da54e33ae3be729a2ec87f452179`

```dockerfile
```

-	Layers:
	-	`sha256:56e5b41b8dc9ca33399b53b081f544e9533da92111b27fda89405526615c594a`  
		Last Modified: Mon, 08 Sep 2025 23:00:23 GMT  
		Size: 5.6 MB (5589234 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:77e98446e21b354415d21ff10a7e3cc6a42ee110fb426ecf4e48476a0a271d90`  
		Last Modified: Mon, 08 Sep 2025 23:00:25 GMT  
		Size: 18.7 KB (18694 bytes)  
		MIME: application/vnd.in-toto+json
