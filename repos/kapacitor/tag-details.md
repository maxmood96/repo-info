<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `kapacitor`

-	[`kapacitor:1.6`](#kapacitor16)
-	[`kapacitor:1.6-alpine`](#kapacitor16-alpine)
-	[`kapacitor:1.6.6`](#kapacitor166)
-	[`kapacitor:1.6.6-alpine`](#kapacitor166-alpine)
-	[`kapacitor:1.7`](#kapacitor17)
-	[`kapacitor:1.7-alpine`](#kapacitor17-alpine)
-	[`kapacitor:1.7.5`](#kapacitor175)
-	[`kapacitor:1.7.5-alpine`](#kapacitor175-alpine)
-	[`kapacitor:alpine`](#kapacitoralpine)
-	[`kapacitor:latest`](#kapacitorlatest)

## `kapacitor:1.6`

```console
$ docker pull kapacitor@sha256:0653b6e42eeabd2b3518e1a1d38f5200f8418cb42d47a31ade14d04410cb17eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:9caf2d32acaef44190cdc1eb65b1d20739770ee8938c67c6d484a854c2527f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140252888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f120bd711d39ba84edf1a01843cc2a703dbc608716249286c191e146e65d9725`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4128354ff964965db59ca596509ba61c1ed2cc5f0413b174dff9b216f5118688`  
		Last Modified: Tue, 02 Jul 2024 02:04:20 GMT  
		Size: 7.1 MB (7091450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af41040fa9a3d9ebe778481b836595d7577099df641e25a4e7db7336f97297a`  
		Last Modified: Tue, 02 Jul 2024 03:03:47 GMT  
		Size: 37.0 MB (37048509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d613c9ca58462aef786c1ac056e4a65f4cd5ec63fbc207a29dfcd2568e21e2ed`  
		Last Modified: Tue, 02 Jul 2024 03:03:47 GMT  
		Size: 65.7 MB (65672604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec857f4b1e86910dff572410e9aaac26c658fdf983d554ae69e59dc53d0ebb2`  
		Last Modified: Tue, 02 Jul 2024 03:03:47 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842cef93aa6e4958b1cc1b9db0c0f40c1f042954ffed9a07015819b80d5db487`  
		Last Modified: Tue, 02 Jul 2024 03:03:48 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7713a746d4e9325f856d7ae72508059a9dfd59d2f0a5262b0b469b10a999b671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3484223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01645d77c03317195e2e653924a790c5933c0343a21ac2bcac789a1842089db`

```dockerfile
```

-	Layers:
	-	`sha256:357c60675253b4ba0c4d82ff7968d3f26fc9c53d4d131354e4a4ee23d1f49a74`  
		Last Modified: Tue, 02 Jul 2024 03:03:47 GMT  
		Size: 3.5 MB (3469619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c85c1a89a75d7ac8b8dd6b081c257bac86a2d76017da976d0f7a5b57c9799d8c`  
		Last Modified: Tue, 02 Jul 2024 03:03:46 GMT  
		Size: 14.6 KB (14604 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:36de21fe7114bf182333a849175df4fcb66daced7cfa6724a6b190a947caf43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131334973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7d96b3ce549b242abbd2a62cb958f3647157ebc86a962e3c0174f3c8101cb9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3706be4328054e3209c8500f7b95bbc5c067e576fd3affd3080f2a6b5d407608`  
		Last Modified: Tue, 02 Jul 2024 04:05:14 GMT  
		Size: 7.0 MB (7033274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eac7d312ec6db59f1eb49ffcaca52f4a778b57744c7f07a3091430d418f02ba`  
		Last Modified: Tue, 02 Jul 2024 15:40:15 GMT  
		Size: 34.2 MB (34230175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d73c92d04468d46ef8fa6c91f831c0e7010dd9a19aaf877817a8c15498b9844`  
		Last Modified: Tue, 02 Jul 2024 15:40:15 GMT  
		Size: 61.7 MB (61669936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d837895d20bc97465a91fbce2604e2bfa18ec4f36320b882f3cfb13d97309fbc`  
		Last Modified: Tue, 02 Jul 2024 15:40:14 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7548d71e3fa20842d6eb131809072b0cee0326a453cad5994b7e8dfb6392f4a2`  
		Last Modified: Tue, 02 Jul 2024 15:40:15 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:1b6a73918c8d1a32ef727b79f418467710fe062bd9b11318a66dddb233de531a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3484779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293cd46e1769dab389879219210de861f465fb6c1ebb01fd1a019635e5f624c6`

```dockerfile
```

-	Layers:
	-	`sha256:deed5dc2db1a23a07824d24a530c8a023d16ce4f37606b039bfc1f6db0a7eefa`  
		Last Modified: Tue, 02 Jul 2024 15:40:14 GMT  
		Size: 3.5 MB (3469885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c24f867251b00c24caa61752373b53e25fbca20001b71a6bee45efa6acebc5`  
		Last Modified: Tue, 02 Jul 2024 15:40:14 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6-alpine`

```console
$ docker pull kapacitor@sha256:33edac88e9cda33409753721ad9c9c52c0b0ee57480fb9a009fbd9acede9bdbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:e41efb14aefdea98acfa1edb7f5aedfa3e5ba3f66761f3921022522bb9414a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69494617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce35adfb2532dc7e6ff7ac343d9908eaf8e291f6e90d68ad726a68efcc5705e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc4e516b2badd0270b176bf642f4c8b9112ab64ed8eabd993974c6f59e67c2d`  
		Last Modified: Mon, 22 Jul 2024 23:05:46 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a080aed35f3d178bcb7567a5d322cf2caea4e5ca2ae39ba43c9c5beeb68d6ab7`  
		Last Modified: Mon, 22 Jul 2024 23:05:47 GMT  
		Size: 290.9 KB (290880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a526be1d1117507e11cad9d3217b79061148a3b0e313b4f342a16f58cc0804`  
		Last Modified: Mon, 22 Jul 2024 23:05:49 GMT  
		Size: 65.6 MB (65580111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79424ae07b311d94b2fa53a9179960df4e6ae6580e9a1795e884590e8483d791`  
		Last Modified: Mon, 22 Jul 2024 23:05:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca8901ae6c1b0a57140b91902aff4daab6b9795bf7fe088fd961211561dbc40`  
		Last Modified: Mon, 22 Jul 2024 23:05:47 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:cc731d053f22be542c22b2c7b7b088d84b7c92b7f6ff4832fedad44f08e76874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.7 KB (369677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ec9d8832b74ec2a37c449efbe190662ad69433c6530247a2b8a470f141ae8d`

```dockerfile
```

-	Layers:
	-	`sha256:104737d15d53769b390b5a962afe4f0c195e81e9e8ae6a6506379178a6cf78e7`  
		Last Modified: Mon, 22 Jul 2024 23:05:47 GMT  
		Size: 355.1 KB (355135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1fa2792007f906179786cca529add83e11f6c41c46df0a529746ef8140c3281`  
		Last Modified: Mon, 22 Jul 2024 23:05:47 GMT  
		Size: 14.5 KB (14542 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6.6`

```console
$ docker pull kapacitor@sha256:0653b6e42eeabd2b3518e1a1d38f5200f8418cb42d47a31ade14d04410cb17eb
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.6.6` - linux; amd64

```console
$ docker pull kapacitor@sha256:9caf2d32acaef44190cdc1eb65b1d20739770ee8938c67c6d484a854c2527f8b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **140.3 MB (140252888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f120bd711d39ba84edf1a01843cc2a703dbc608716249286c191e146e65d9725`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4128354ff964965db59ca596509ba61c1ed2cc5f0413b174dff9b216f5118688`  
		Last Modified: Tue, 02 Jul 2024 02:04:20 GMT  
		Size: 7.1 MB (7091450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:0af41040fa9a3d9ebe778481b836595d7577099df641e25a4e7db7336f97297a`  
		Last Modified: Tue, 02 Jul 2024 03:03:47 GMT  
		Size: 37.0 MB (37048509 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d613c9ca58462aef786c1ac056e4a65f4cd5ec63fbc207a29dfcd2568e21e2ed`  
		Last Modified: Tue, 02 Jul 2024 03:03:47 GMT  
		Size: 65.7 MB (65672604 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:eec857f4b1e86910dff572410e9aaac26c658fdf983d554ae69e59dc53d0ebb2`  
		Last Modified: Tue, 02 Jul 2024 03:03:47 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:842cef93aa6e4958b1cc1b9db0c0f40c1f042954ffed9a07015819b80d5db487`  
		Last Modified: Tue, 02 Jul 2024 03:03:48 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7713a746d4e9325f856d7ae72508059a9dfd59d2f0a5262b0b469b10a999b671
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3484223 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b01645d77c03317195e2e653924a790c5933c0343a21ac2bcac789a1842089db`

```dockerfile
```

-	Layers:
	-	`sha256:357c60675253b4ba0c4d82ff7968d3f26fc9c53d4d131354e4a4ee23d1f49a74`  
		Last Modified: Tue, 02 Jul 2024 03:03:47 GMT  
		Size: 3.5 MB (3469619 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:c85c1a89a75d7ac8b8dd6b081c257bac86a2d76017da976d0f7a5b57c9799d8c`  
		Last Modified: Tue, 02 Jul 2024 03:03:46 GMT  
		Size: 14.6 KB (14604 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.6.6` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:36de21fe7114bf182333a849175df4fcb66daced7cfa6724a6b190a947caf43e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **131.3 MB (131334973 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:be7d96b3ce549b242abbd2a62cb958f3647157ebc86a962e3c0174f3c8101cb9`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3706be4328054e3209c8500f7b95bbc5c067e576fd3affd3080f2a6b5d407608`  
		Last Modified: Tue, 02 Jul 2024 04:05:14 GMT  
		Size: 7.0 MB (7033274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eac7d312ec6db59f1eb49ffcaca52f4a778b57744c7f07a3091430d418f02ba`  
		Last Modified: Tue, 02 Jul 2024 15:40:15 GMT  
		Size: 34.2 MB (34230175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1d73c92d04468d46ef8fa6c91f831c0e7010dd9a19aaf877817a8c15498b9844`  
		Last Modified: Tue, 02 Jul 2024 15:40:15 GMT  
		Size: 61.7 MB (61669936 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d837895d20bc97465a91fbce2604e2bfa18ec4f36320b882f3cfb13d97309fbc`  
		Last Modified: Tue, 02 Jul 2024 15:40:14 GMT  
		Size: 227.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:7548d71e3fa20842d6eb131809072b0cee0326a453cad5994b7e8dfb6392f4a2`  
		Last Modified: Tue, 02 Jul 2024 15:40:15 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6` - unknown; unknown

```console
$ docker pull kapacitor@sha256:1b6a73918c8d1a32ef727b79f418467710fe062bd9b11318a66dddb233de531a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3484779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:293cd46e1769dab389879219210de861f465fb6c1ebb01fd1a019635e5f624c6`

```dockerfile
```

-	Layers:
	-	`sha256:deed5dc2db1a23a07824d24a530c8a023d16ce4f37606b039bfc1f6db0a7eefa`  
		Last Modified: Tue, 02 Jul 2024 15:40:14 GMT  
		Size: 3.5 MB (3469885 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:d7c24f867251b00c24caa61752373b53e25fbca20001b71a6bee45efa6acebc5`  
		Last Modified: Tue, 02 Jul 2024 15:40:14 GMT  
		Size: 14.9 KB (14894 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.6.6-alpine`

```console
$ docker pull kapacitor@sha256:33edac88e9cda33409753721ad9c9c52c0b0ee57480fb9a009fbd9acede9bdbd
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.6.6-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:e41efb14aefdea98acfa1edb7f5aedfa3e5ba3f66761f3921022522bb9414a40
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.5 MB (69494617 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fce35adfb2532dc7e6ff7ac343d9908eaf8e291f6e90d68ad726a68efcc5705e`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
RUN apk add --no-cache ca-certificates &&     update-ca-certificates # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.6.6
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc4e516b2badd0270b176bf642f4c8b9112ab64ed8eabd993974c6f59e67c2d`  
		Last Modified: Mon, 22 Jul 2024 23:05:46 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a080aed35f3d178bcb7567a5d322cf2caea4e5ca2ae39ba43c9c5beeb68d6ab7`  
		Last Modified: Mon, 22 Jul 2024 23:05:47 GMT  
		Size: 290.9 KB (290880 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:a2a526be1d1117507e11cad9d3217b79061148a3b0e313b4f342a16f58cc0804`  
		Last Modified: Mon, 22 Jul 2024 23:05:49 GMT  
		Size: 65.6 MB (65580111 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:79424ae07b311d94b2fa53a9179960df4e6ae6580e9a1795e884590e8483d791`  
		Last Modified: Mon, 22 Jul 2024 23:05:47 GMT  
		Size: 223.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8ca8901ae6c1b0a57140b91902aff4daab6b9795bf7fe088fd961211561dbc40`  
		Last Modified: Mon, 22 Jul 2024 23:05:47 GMT  
		Size: 231.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.6.6-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:cc731d053f22be542c22b2c7b7b088d84b7c92b7f6ff4832fedad44f08e76874
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **369.7 KB (369677 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6ec9d8832b74ec2a37c449efbe190662ad69433c6530247a2b8a470f141ae8d`

```dockerfile
```

-	Layers:
	-	`sha256:104737d15d53769b390b5a962afe4f0c195e81e9e8ae6a6506379178a6cf78e7`  
		Last Modified: Mon, 22 Jul 2024 23:05:47 GMT  
		Size: 355.1 KB (355135 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:b1fa2792007f906179786cca529add83e11f6c41c46df0a529746ef8140c3281`  
		Last Modified: Mon, 22 Jul 2024 23:05:47 GMT  
		Size: 14.5 KB (14542 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7`

```console
$ docker pull kapacitor@sha256:073392166ea8864178a66f6be6daf5d5eb74bb87a31e73fcb16f8fd9885db66e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7` - linux; amd64

```console
$ docker pull kapacitor@sha256:ab0dd73564996f7bcc8b0c3eed4d43dc59e00325dbb5aa11e5da288c010b8404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.0 MB (145969720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74d0898b5f4fbb6b4bbb5ccd6d7a290891940d13a7d02b39bf0b3e0a2dc4da6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4128354ff964965db59ca596509ba61c1ed2cc5f0413b174dff9b216f5118688`  
		Last Modified: Tue, 02 Jul 2024 02:04:20 GMT  
		Size: 7.1 MB (7091450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f095eea47a73940c638cfba9b826f5faccd0cf4ed6f5c7089b00edb7d8ec0c0`  
		Last Modified: Tue, 02 Jul 2024 03:03:53 GMT  
		Size: 37.0 MB (37048489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa720b92cf1d97fa32608d4d7027c0eba642f795426e6784f9baaa6f64a7c944`  
		Last Modified: Tue, 02 Jul 2024 03:03:53 GMT  
		Size: 71.4 MB (71389393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a6e8df5db4cd35baa573876f499c7222fb0d92967ea5a94584462f7385e792`  
		Last Modified: Tue, 02 Jul 2024 03:03:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb5de742855bf604e70663030915f13a12c299789d00352e863533895d929f1`  
		Last Modified: Tue, 02 Jul 2024 03:03:52 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:cae6b9692b8f5b563e29fb908f08d4fa3417f0ca32303acdd8605e89524f08de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609f81b847e2e25ee10fed75bfd3b1aacc4986b3e5fedae4f2de976fb6e95ed9`

```dockerfile
```

-	Layers:
	-	`sha256:8232fc8d3a0c8d07826a620024c52bdc428061b5100e85b1ea45d13b0e136f1d`  
		Last Modified: Tue, 02 Jul 2024 03:03:52 GMT  
		Size: 3.5 MB (3476155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d07f98069e79b289e54a3744a8408c014320129a638f7dc4eed2a6b78de92be`  
		Last Modified: Tue, 02 Jul 2024 03:03:52 GMT  
		Size: 14.9 KB (14908 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:218d96a9cc830fce73ee247bdc38c6f162172dbe41ad62eea48c546a682fe199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 MB (136780221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a44c142f039870ab89373fb64c5e1f41c60875ecdffae765e02ca83d6aa6ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3706be4328054e3209c8500f7b95bbc5c067e576fd3affd3080f2a6b5d407608`  
		Last Modified: Tue, 02 Jul 2024 04:05:14 GMT  
		Size: 7.0 MB (7033274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eac7d312ec6db59f1eb49ffcaca52f4a778b57744c7f07a3091430d418f02ba`  
		Last Modified: Tue, 02 Jul 2024 15:40:15 GMT  
		Size: 34.2 MB (34230175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad9e7409d184b07f1f9b7fdd9ff700629371d5526df706506571d309c691e45`  
		Last Modified: Tue, 02 Jul 2024 15:40:47 GMT  
		Size: 67.1 MB (67115121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe38e937968cc36da555f5c8919577900c0d30273cbd5d7f604ec909c6e3d03`  
		Last Modified: Tue, 02 Jul 2024 15:40:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717e5322a305963cd7e31964336fae9e5360c43fa6c8862c1bcad3c13f0df1fa`  
		Last Modified: Tue, 02 Jul 2024 15:40:44 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7` - unknown; unknown

```console
$ docker pull kapacitor@sha256:05bb5323fce53beb283c56135693b4ae9de46acae13b9b8cba9895b660c7af56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3490991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a7e4b50fd0726b08d97b5b906bf1070e1518f604113abfe154660341408784`

```dockerfile
```

-	Layers:
	-	`sha256:501ef2f86b23b0818a6c3cdfe779bb2036d18f84f652b3bbb3dcce168a4d181d`  
		Last Modified: Tue, 02 Jul 2024 15:40:45 GMT  
		Size: 3.5 MB (3475781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be6a666749fb0ca8c4e3cc750398f7c52b7c0b26c2891ff9accfad3f0a5c16db`  
		Last Modified: Tue, 02 Jul 2024 15:40:44 GMT  
		Size: 15.2 KB (15210 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7-alpine`

```console
$ docker pull kapacitor@sha256:9cd9bfa5b92536486d8d266f401418bb3131ae900ad7bd24af89adb2f6d37e0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:0eead438c8ee551d625b70d3db2a10f968cfb2dbdf493fb33365eb07b51f8bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75235654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90353e9aec2989f510f5da6f0f61a6b761516d5458c01f5037c83adbf5062c68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc4e516b2badd0270b176bf642f4c8b9112ab64ed8eabd993974c6f59e67c2d`  
		Last Modified: Mon, 22 Jul 2024 23:05:46 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bcdc3e1ad224b92ba7ece19fe4d901e51c880fc8f6fd6caf839a146df659c7`  
		Last Modified: Mon, 22 Jul 2024 23:05:46 GMT  
		Size: 292.6 KB (292603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f5f0cfc3ac9e0faafca08acf6ae2e2a3647188d63816923b0e356daa924ac2`  
		Last Modified: Mon, 22 Jul 2024 23:05:49 GMT  
		Size: 71.3 MB (71319378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60e5b31ae3483a9e303f6fd208762721434726d969f78d7b68cee72f4406960`  
		Last Modified: Mon, 22 Jul 2024 23:05:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c24e582295ce7c469cef0ba36f1743aa34f6b35f1435db390c3df5a29f069f`  
		Last Modified: Mon, 22 Jul 2024 23:05:47 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7fffc213fe268116e389e0e44d489f3bf67ad1203c024c249345065d6297891c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 KB (380165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6f7de787c92d9129e84e91532becd8367bb4e42c8599404e59549781c46bf9`

```dockerfile
```

-	Layers:
	-	`sha256:61de9d0c7f5c77ffc2e896d992b1a17cccc4225b73481b35b2b57e5025234aef`  
		Last Modified: Mon, 22 Jul 2024 23:05:47 GMT  
		Size: 364.7 KB (364702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:863b0742b4d96ea200a45105467676ec9a86d88aa768ce26ce7ab5313c5a680d`  
		Last Modified: Mon, 22 Jul 2024 23:05:46 GMT  
		Size: 15.5 KB (15463 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.5`

```console
$ docker pull kapacitor@sha256:073392166ea8864178a66f6be6daf5d5eb74bb87a31e73fcb16f8fd9885db66e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:1.7.5` - linux; amd64

```console
$ docker pull kapacitor@sha256:ab0dd73564996f7bcc8b0c3eed4d43dc59e00325dbb5aa11e5da288c010b8404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.0 MB (145969720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74d0898b5f4fbb6b4bbb5ccd6d7a290891940d13a7d02b39bf0b3e0a2dc4da6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4128354ff964965db59ca596509ba61c1ed2cc5f0413b174dff9b216f5118688`  
		Last Modified: Tue, 02 Jul 2024 02:04:20 GMT  
		Size: 7.1 MB (7091450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f095eea47a73940c638cfba9b826f5faccd0cf4ed6f5c7089b00edb7d8ec0c0`  
		Last Modified: Tue, 02 Jul 2024 03:03:53 GMT  
		Size: 37.0 MB (37048489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa720b92cf1d97fa32608d4d7027c0eba642f795426e6784f9baaa6f64a7c944`  
		Last Modified: Tue, 02 Jul 2024 03:03:53 GMT  
		Size: 71.4 MB (71389393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a6e8df5db4cd35baa573876f499c7222fb0d92967ea5a94584462f7385e792`  
		Last Modified: Tue, 02 Jul 2024 03:03:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb5de742855bf604e70663030915f13a12c299789d00352e863533895d929f1`  
		Last Modified: Tue, 02 Jul 2024 03:03:52 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.5` - unknown; unknown

```console
$ docker pull kapacitor@sha256:cae6b9692b8f5b563e29fb908f08d4fa3417f0ca32303acdd8605e89524f08de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609f81b847e2e25ee10fed75bfd3b1aacc4986b3e5fedae4f2de976fb6e95ed9`

```dockerfile
```

-	Layers:
	-	`sha256:8232fc8d3a0c8d07826a620024c52bdc428061b5100e85b1ea45d13b0e136f1d`  
		Last Modified: Tue, 02 Jul 2024 03:03:52 GMT  
		Size: 3.5 MB (3476155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d07f98069e79b289e54a3744a8408c014320129a638f7dc4eed2a6b78de92be`  
		Last Modified: Tue, 02 Jul 2024 03:03:52 GMT  
		Size: 14.9 KB (14908 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:1.7.5` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:218d96a9cc830fce73ee247bdc38c6f162172dbe41ad62eea48c546a682fe199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 MB (136780221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a44c142f039870ab89373fb64c5e1f41c60875ecdffae765e02ca83d6aa6ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3706be4328054e3209c8500f7b95bbc5c067e576fd3affd3080f2a6b5d407608`  
		Last Modified: Tue, 02 Jul 2024 04:05:14 GMT  
		Size: 7.0 MB (7033274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eac7d312ec6db59f1eb49ffcaca52f4a778b57744c7f07a3091430d418f02ba`  
		Last Modified: Tue, 02 Jul 2024 15:40:15 GMT  
		Size: 34.2 MB (34230175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad9e7409d184b07f1f9b7fdd9ff700629371d5526df706506571d309c691e45`  
		Last Modified: Tue, 02 Jul 2024 15:40:47 GMT  
		Size: 67.1 MB (67115121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe38e937968cc36da555f5c8919577900c0d30273cbd5d7f604ec909c6e3d03`  
		Last Modified: Tue, 02 Jul 2024 15:40:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717e5322a305963cd7e31964336fae9e5360c43fa6c8862c1bcad3c13f0df1fa`  
		Last Modified: Tue, 02 Jul 2024 15:40:44 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.5` - unknown; unknown

```console
$ docker pull kapacitor@sha256:05bb5323fce53beb283c56135693b4ae9de46acae13b9b8cba9895b660c7af56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3490991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a7e4b50fd0726b08d97b5b906bf1070e1518f604113abfe154660341408784`

```dockerfile
```

-	Layers:
	-	`sha256:501ef2f86b23b0818a6c3cdfe779bb2036d18f84f652b3bbb3dcce168a4d181d`  
		Last Modified: Tue, 02 Jul 2024 15:40:45 GMT  
		Size: 3.5 MB (3475781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be6a666749fb0ca8c4e3cc750398f7c52b7c0b26c2891ff9accfad3f0a5c16db`  
		Last Modified: Tue, 02 Jul 2024 15:40:44 GMT  
		Size: 15.2 KB (15210 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:1.7.5-alpine`

```console
$ docker pull kapacitor@sha256:9cd9bfa5b92536486d8d266f401418bb3131ae900ad7bd24af89adb2f6d37e0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:1.7.5-alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:0eead438c8ee551d625b70d3db2a10f968cfb2dbdf493fb33365eb07b51f8bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75235654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90353e9aec2989f510f5da6f0f61a6b761516d5458c01f5037c83adbf5062c68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc4e516b2badd0270b176bf642f4c8b9112ab64ed8eabd993974c6f59e67c2d`  
		Last Modified: Mon, 22 Jul 2024 23:05:46 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bcdc3e1ad224b92ba7ece19fe4d901e51c880fc8f6fd6caf839a146df659c7`  
		Last Modified: Mon, 22 Jul 2024 23:05:46 GMT  
		Size: 292.6 KB (292603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f5f0cfc3ac9e0faafca08acf6ae2e2a3647188d63816923b0e356daa924ac2`  
		Last Modified: Mon, 22 Jul 2024 23:05:49 GMT  
		Size: 71.3 MB (71319378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60e5b31ae3483a9e303f6fd208762721434726d969f78d7b68cee72f4406960`  
		Last Modified: Mon, 22 Jul 2024 23:05:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c24e582295ce7c469cef0ba36f1743aa34f6b35f1435db390c3df5a29f069f`  
		Last Modified: Mon, 22 Jul 2024 23:05:47 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:1.7.5-alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7fffc213fe268116e389e0e44d489f3bf67ad1203c024c249345065d6297891c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 KB (380165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6f7de787c92d9129e84e91532becd8367bb4e42c8599404e59549781c46bf9`

```dockerfile
```

-	Layers:
	-	`sha256:61de9d0c7f5c77ffc2e896d992b1a17cccc4225b73481b35b2b57e5025234aef`  
		Last Modified: Mon, 22 Jul 2024 23:05:47 GMT  
		Size: 364.7 KB (364702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:863b0742b4d96ea200a45105467676ec9a86d88aa768ce26ce7ab5313c5a680d`  
		Last Modified: Mon, 22 Jul 2024 23:05:46 GMT  
		Size: 15.5 KB (15463 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:alpine`

```console
$ docker pull kapacitor@sha256:9cd9bfa5b92536486d8d266f401418bb3131ae900ad7bd24af89adb2f6d37e0f
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 2
	-	linux; amd64
	-	unknown; unknown

### `kapacitor:alpine` - linux; amd64

```console
$ docker pull kapacitor@sha256:0eead438c8ee551d625b70d3db2a10f968cfb2dbdf493fb33365eb07b51f8bcb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **75.2 MB (75235654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90353e9aec2989f510f5da6f0f61a6b761516d5458c01f5037c83adbf5062c68`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:99093095d62d0421541d882f9ceeddb2981fe701ec0aa9d2c08480712d5fed21 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN echo 'hosts: files dns' >> /etc/nsswitch.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
RUN apk add --no-cache ca-certificates su-exec &&     update-ca-certificates # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -ex &&     mkdir ~/.gnupg;     echo "disable-ipv6" >> ~/.gnupg/dirmngr.conf;     apk add --no-cache --virtual .build-deps wget gnupg tar &&     for key in         9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E ;     do         gpg --keyserver hkp://keyserver.ubuntu.com --recv-keys "$key" ;     done &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     gpg --batch --verify kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz.asc kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     mkdir -p /usr/src &&     tar -C /usr/src -xzf kapacitor-${KAPACITOR_VERSION}_linux_amd64.tar.gz &&     cp -ar /usr/src/kapacitor-*/* / &&     gpgconf --kill all &&     rm -rf *.tar.gz* /usr/src /root/.gnupg &&     apk del .build-deps &&     addgroup -S kapacitor &&     adduser -S kapacitor -G kapacitor &&     mkdir -m 0750 -p /var/lib/kapacitor &&     chown kapacitor:kapacitor /var/lib/kapacitor # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:c6a83fedfae6ed8a4f5f7cbb6a7b6f1c1ec3d86fea8cb9e5ba2e5e6673fde9f6`  
		Last Modified: Mon, 22 Jul 2024 22:27:14 GMT  
		Size: 3.6 MB (3622892 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3dc4e516b2badd0270b176bf642f4c8b9112ab64ed8eabd993974c6f59e67c2d`  
		Last Modified: Mon, 22 Jul 2024 23:05:46 GMT  
		Size: 280.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:72bcdc3e1ad224b92ba7ece19fe4d901e51c880fc8f6fd6caf839a146df659c7`  
		Last Modified: Mon, 22 Jul 2024 23:05:46 GMT  
		Size: 292.6 KB (292603 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d8f5f0cfc3ac9e0faafca08acf6ae2e2a3647188d63816923b0e356daa924ac2`  
		Last Modified: Mon, 22 Jul 2024 23:05:49 GMT  
		Size: 71.3 MB (71319378 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c60e5b31ae3483a9e303f6fd208762721434726d969f78d7b68cee72f4406960`  
		Last Modified: Mon, 22 Jul 2024 23:05:46 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:f5c24e582295ce7c469cef0ba36f1743aa34f6b35f1435db390c3df5a29f069f`  
		Last Modified: Mon, 22 Jul 2024 23:05:47 GMT  
		Size: 277.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:alpine` - unknown; unknown

```console
$ docker pull kapacitor@sha256:7fffc213fe268116e389e0e44d489f3bf67ad1203c024c249345065d6297891c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **380.2 KB (380165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4c6f7de787c92d9129e84e91532becd8367bb4e42c8599404e59549781c46bf9`

```dockerfile
```

-	Layers:
	-	`sha256:61de9d0c7f5c77ffc2e896d992b1a17cccc4225b73481b35b2b57e5025234aef`  
		Last Modified: Mon, 22 Jul 2024 23:05:47 GMT  
		Size: 364.7 KB (364702 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:863b0742b4d96ea200a45105467676ec9a86d88aa768ce26ce7ab5313c5a680d`  
		Last Modified: Mon, 22 Jul 2024 23:05:46 GMT  
		Size: 15.5 KB (15463 bytes)  
		MIME: application/vnd.in-toto+json

## `kapacitor:latest`

```console
$ docker pull kapacitor@sha256:073392166ea8864178a66f6be6daf5d5eb74bb87a31e73fcb16f8fd9885db66e
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `kapacitor:latest` - linux; amd64

```console
$ docker pull kapacitor@sha256:ab0dd73564996f7bcc8b0c3eed4d43dc59e00325dbb5aa11e5da288c010b8404
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **146.0 MB (145969720 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d74d0898b5f4fbb6b4bbb5ccd6d7a290891940d13a7d02b39bf0b3e0a2dc4da6`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:d5da92199726e42da09a6f75a778befb607fe3f79e4afaf7ef5188329b26b386 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:9b857f539cb142c9aa2201a17bb8e1cd5cf12edd4a65adf5732fe9f4343964cf`  
		Last Modified: Fri, 28 Jun 2024 01:17:21 GMT  
		Size: 30.4 MB (30439866 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4128354ff964965db59ca596509ba61c1ed2cc5f0413b174dff9b216f5118688`  
		Last Modified: Tue, 02 Jul 2024 02:04:20 GMT  
		Size: 7.1 MB (7091450 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:6f095eea47a73940c638cfba9b826f5faccd0cf4ed6f5c7089b00edb7d8ec0c0`  
		Last Modified: Tue, 02 Jul 2024 03:03:53 GMT  
		Size: 37.0 MB (37048489 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fa720b92cf1d97fa32608d4d7027c0eba642f795426e6784f9baaa6f64a7c944`  
		Last Modified: Tue, 02 Jul 2024 03:03:53 GMT  
		Size: 71.4 MB (71389393 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:88a6e8df5db4cd35baa573876f499c7222fb0d92967ea5a94584462f7385e792`  
		Last Modified: Tue, 02 Jul 2024 03:03:52 GMT  
		Size: 225.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:fbb5de742855bf604e70663030915f13a12c299789d00352e863533895d929f1`  
		Last Modified: Tue, 02 Jul 2024 03:03:52 GMT  
		Size: 297.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:cae6b9692b8f5b563e29fb908f08d4fa3417f0ca32303acdd8605e89524f08de
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3491063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:609f81b847e2e25ee10fed75bfd3b1aacc4986b3e5fedae4f2de976fb6e95ed9`

```dockerfile
```

-	Layers:
	-	`sha256:8232fc8d3a0c8d07826a620024c52bdc428061b5100e85b1ea45d13b0e136f1d`  
		Last Modified: Tue, 02 Jul 2024 03:03:52 GMT  
		Size: 3.5 MB (3476155 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:8d07f98069e79b289e54a3744a8408c014320129a638f7dc4eed2a6b78de92be`  
		Last Modified: Tue, 02 Jul 2024 03:03:52 GMT  
		Size: 14.9 KB (14908 bytes)  
		MIME: application/vnd.in-toto+json

### `kapacitor:latest` - linux; arm64 variant v8

```console
$ docker pull kapacitor@sha256:218d96a9cc830fce73ee247bdc38c6f162172dbe41ad62eea48c546a682fe199
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **136.8 MB (136780221 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35a44c142f039870ab89373fb64c5e1f41c60875ecdffae765e02ca83d6aa6ac`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["kapacitord"]`

```dockerfile
# Tue, 18 Jun 2024 15:52:41 GMT
ARG RELEASE
# Tue, 18 Jun 2024 15:52:41 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Tue, 18 Jun 2024 15:52:41 GMT
LABEL org.opencontainers.image.version=22.04
# Tue, 18 Jun 2024 15:52:41 GMT
ADD file:2bed1fbf8253926f27dc275983c274712d836e9b6acdb1059d29c072d8f63a03 in / 
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["/bin/bash"]
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux; 	apt-get update; 	apt-get install -y --no-install-recommends 		ca-certificates 		curl 		gnupg 		netbase 		wget 		tzdata 	; 	rm -rf /var/lib/apt/lists/*
# Tue, 18 Jun 2024 15:52:41 GMT
RUN DEBIAN_FRONTEND=noninteractive apt-get update &&     DEBIAN_FRONTEND=noninteractive apt-get install -y bash-completion &&     awk 'f{if(sub(/^#/,"",$0)==0){f=0}};/^# enable bash completion/{f=1};{print;}' /etc/bash.bashrc > /etc/bash.bashrc.new &&     mv /etc/bash.bashrc.new /etc/bash.bashrc # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENV KAPACITOR_VERSION=1.7.5
# Tue, 18 Jun 2024 15:52:41 GMT
RUN set -eux &&     ARCH= && dpkgArch="$(dpkg --print-architecture)" &&     case "${dpkgArch##*-}" in         amd64) ARCH='amd64';;         arm64) ARCH='arm64';;         *)     echo "Unsupported architecture: ${dpkgArch}"; exit 1;;     esac &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc &&     wget --no-verbose https://dl.influxdata.com/kapacitor/releases/kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     export GNUPGHOME="$(mktemp -d)" &&     echo "disable-ipv6" >> $GNUPGHOME/dirmngr.conf &&     gpg --batch --keyserver hkp://keyserver.ubuntu.com --recv-keys 9D539D90D3328DC7D6C8D3B9D8FF8E1F7DF8B07E &&     gpg --batch --verify kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb.asc kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     rm -rf "$GNUPGHOME" &&     dpkg -i kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb &&     gpgconf --kill all &&     rm -f kapacitor_${KAPACITOR_VERSION}-1_${ARCH}.deb* # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
COPY kapacitor.conf /etc/kapacitor/kapacitor.conf # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
EXPOSE map[9092/tcp:{}]
# Tue, 18 Jun 2024 15:52:41 GMT
VOLUME [/var/lib/kapacitor]
# Tue, 18 Jun 2024 15:52:41 GMT
COPY entrypoint.sh /entrypoint.sh # buildkit
# Tue, 18 Jun 2024 15:52:41 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Tue, 18 Jun 2024 15:52:41 GMT
CMD ["kapacitord"]
```

-	Layers:
	-	`sha256:24cfbc0d689f4d514c091713d28dff40b2e697cb854a24b2fae97f94b10bc383`  
		Last Modified: Fri, 28 Jun 2024 02:10:56 GMT  
		Size: 28.4 MB (28401129 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:3706be4328054e3209c8500f7b95bbc5c067e576fd3affd3080f2a6b5d407608`  
		Last Modified: Tue, 02 Jul 2024 04:05:14 GMT  
		Size: 7.0 MB (7033274 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:8eac7d312ec6db59f1eb49ffcaca52f4a778b57744c7f07a3091430d418f02ba`  
		Last Modified: Tue, 02 Jul 2024 15:40:15 GMT  
		Size: 34.2 MB (34230175 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bad9e7409d184b07f1f9b7fdd9ff700629371d5526df706506571d309c691e45`  
		Last Modified: Tue, 02 Jul 2024 15:40:47 GMT  
		Size: 67.1 MB (67115121 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5fe38e937968cc36da555f5c8919577900c0d30273cbd5d7f604ec909c6e3d03`  
		Last Modified: Tue, 02 Jul 2024 15:40:45 GMT  
		Size: 224.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:717e5322a305963cd7e31964336fae9e5360c43fa6c8862c1bcad3c13f0df1fa`  
		Last Modified: Tue, 02 Jul 2024 15:40:44 GMT  
		Size: 298.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `kapacitor:latest` - unknown; unknown

```console
$ docker pull kapacitor@sha256:05bb5323fce53beb283c56135693b4ae9de46acae13b9b8cba9895b660c7af56
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **3.5 MB (3490991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08a7e4b50fd0726b08d97b5b906bf1070e1518f604113abfe154660341408784`

```dockerfile
```

-	Layers:
	-	`sha256:501ef2f86b23b0818a6c3cdfe779bb2036d18f84f652b3bbb3dcce168a4d181d`  
		Last Modified: Tue, 02 Jul 2024 15:40:45 GMT  
		Size: 3.5 MB (3475781 bytes)  
		MIME: application/vnd.in-toto+json
	-	`sha256:be6a666749fb0ca8c4e3cc750398f7c52b7c0b26c2891ff9accfad3f0a5c16db`  
		Last Modified: Tue, 02 Jul 2024 15:40:44 GMT  
		Size: 15.2 KB (15210 bytes)  
		MIME: application/vnd.in-toto+json
