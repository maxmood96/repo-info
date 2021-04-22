<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `vault`

-	[`vault:1.4.7`](#vault147)
-	[`vault:1.5.7`](#vault157)
-	[`vault:1.6.3`](#vault163)
-	[`vault:1.7.0`](#vault170)
-	[`vault:1.7.0-rc1`](#vault170-rc1)
-	[`vault:1.7.0-rc2`](#vault170-rc2)
-	[`vault:latest`](#vaultlatest)

## `vault:1.4.7`

```console
$ docker pull vault@sha256:3929780d624754b7127293649a2c4af1fbc0e22742ea5414b647db3f5de71960
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.4.7` - linux; amd64

```console
$ docker pull vault@sha256:a78fd3a6f639f7e878ffe3f97b84bad492427fce2b1fd871839ab14ee9994342
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52083137 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50ed498508fb26fcd5ffdb9f6605176495c9012f77ca1f7c364a0312d649a04d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 19:20:04 GMT
ADD file:c5377eaa926bf412dd8d4a08b0a1f2399cfd708743533b0aa03b53d14cb4bb4e in / 
# Wed, 14 Apr 2021 19:20:05 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:33:40 GMT
ARG VAULT_VERSION=1.4.7
# Wed, 14 Apr 2021 23:33:41 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 14 Apr 2021 23:33:46 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 14 Apr 2021 23:33:47 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 14 Apr 2021 23:33:47 GMT
VOLUME [/vault/logs]
# Wed, 14 Apr 2021 23:33:48 GMT
VOLUME [/vault/file]
# Wed, 14 Apr 2021 23:33:48 GMT
EXPOSE 8200
# Wed, 14 Apr 2021 23:33:48 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:33:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:33:48 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:396c31837116ac290458afcb928f68b6cc1c7bdd6963fc72f52f365a2a89c1b5`  
		Last Modified: Wed, 14 Apr 2021 19:21:14 GMT  
		Size: 2.8 MB (2798338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e41f21c7fe2e9594ded42500cf671b2ed9a18c66eb86fea26c06acb0ffbd231`  
		Last Modified: Wed, 14 Apr 2021 23:35:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb829b3a48c480021a642347d25c24ff9f0cf4aa549b435d00d59fcd17fc2d36`  
		Last Modified: Wed, 14 Apr 2021 23:35:46 GMT  
		Size: 49.3 MB (49281503 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0343770964a6b5a63786e5e48d8ed95df86c1654f3d4ae65459502ab40fba8`  
		Last Modified: Wed, 14 Apr 2021 23:35:39 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fa7904766036ddaa3c4e3dbf4974d45a1d490f09f23df828844ef1c1870d2e`  
		Last Modified: Wed, 14 Apr 2021 23:35:39 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.4.7` - linux; arm variant v6

```console
$ docker pull vault@sha256:dc8b9937315bfdd099ae34aa110ed82211dd1ebf6e1a1fd2b98b660c7b2593cd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48720911 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5d681ffd16434fdd991b3e0c97592f59f0940e788e99cfffb8077e525ac30e82`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:50:06 GMT
ADD file:eac3dead6ff32a5f6ff9d979fab38a22b12f32db204d32d07bc716ba404332d8 in / 
# Wed, 14 Apr 2021 18:50:07 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 06:19:37 GMT
ARG VAULT_VERSION=1.4.7
# Thu, 15 Apr 2021 06:19:40 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 15 Apr 2021 06:19:50 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 15 Apr 2021 06:19:54 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 15 Apr 2021 06:19:55 GMT
VOLUME [/vault/logs]
# Thu, 15 Apr 2021 06:19:57 GMT
VOLUME [/vault/file]
# Thu, 15 Apr 2021 06:19:58 GMT
EXPOSE 8200
# Thu, 15 Apr 2021 06:19:58 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Apr 2021 06:19:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 06:20:00 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f81e2ad47903c231a972c23a24be618247a23a768b7b5dc7a04a7fe73e9f9b1b`  
		Last Modified: Wed, 14 Apr 2021 18:50:51 GMT  
		Size: 2.6 MB (2575724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f7d898841b0fffd0e26f29f3edc87c805d6722c54de85c677170134d70ec814`  
		Last Modified: Thu, 15 Apr 2021 06:22:26 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11385c46733b24671ddc427a44500a667008fdfb0304347d4ee8632bd45083c4`  
		Last Modified: Thu, 15 Apr 2021 06:22:39 GMT  
		Size: 46.1 MB (46141890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dda24ccfb534e7105a44bcd85593bf38780bb39a4f28b55091e30decf9a66008`  
		Last Modified: Thu, 15 Apr 2021 06:22:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20f0ee9c627babe4745e697c6e6b941205d98f2541c5969e9bfa08579c5b620f`  
		Last Modified: Thu, 15 Apr 2021 06:22:27 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.4.7` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:03924ddd9b600984723275603ffe2243cd661cd841ce211e804a710d4f746838
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48965514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ba458c7ecf1229e67947410a9eca5f1849770bf9c9b6735aa0d8077f9b540632`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:16 GMT
ADD file:85a5071af4733240679a3799298092cb671cae007156a367219b6edf6cfc6377 in / 
# Wed, 14 Apr 2021 18:43:17 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 08:04:11 GMT
ARG VAULT_VERSION=1.4.7
# Thu, 15 Apr 2021 08:04:13 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 15 Apr 2021 08:04:21 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 15 Apr 2021 08:04:24 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 15 Apr 2021 08:04:25 GMT
VOLUME [/vault/logs]
# Thu, 15 Apr 2021 08:04:27 GMT
VOLUME [/vault/file]
# Thu, 15 Apr 2021 08:04:28 GMT
EXPOSE 8200
# Thu, 15 Apr 2021 08:04:29 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Apr 2021 08:04:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 08:04:31 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:26d14edc4f17638cda363ea80b29c55e83058fc0dff1129b38ea3e8231217f7d`  
		Last Modified: Wed, 14 Apr 2021 18:44:10 GMT  
		Size: 2.7 MB (2721209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a13f29247f226257b7f48caf4fedb678dd46bde336d90df89ec0e4ac4b3a734`  
		Last Modified: Thu, 15 Apr 2021 08:06:39 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b10dbbe125f0010f908d3899877b2b0407414c122464f9904890db295215b82`  
		Last Modified: Thu, 15 Apr 2021 08:06:50 GMT  
		Size: 46.2 MB (46241009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd9da28246c59c8866adce494e212d8fcd81c8b1b1a3040c9089939bc4536157`  
		Last Modified: Thu, 15 Apr 2021 08:06:38 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b6b66ea5e0ad5ce76302bda7b6d30bdff4b9816d59b92e694458e3182557603`  
		Last Modified: Thu, 15 Apr 2021 08:06:38 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.4.7` - linux; 386

```console
$ docker pull vault@sha256:345f80ab9b9909051f148fd2f7d548f34a2e1ee37d18aaee83975cb73e0988d3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50215852 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:59c0ef5791ed016878ff6bc144553986fc1a6c2a25098028cf080fdee54015cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:47 GMT
ADD file:efe0af5733a00f82ae4fc3c5ccb3b69f4905c32fc85eefbdd02050c7d5801bca in / 
# Wed, 14 Apr 2021 18:38:48 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 07:30:53 GMT
ARG VAULT_VERSION=1.4.7
# Thu, 15 Apr 2021 07:30:54 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 15 Apr 2021 07:30:59 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 15 Apr 2021 07:31:00 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 15 Apr 2021 07:31:00 GMT
VOLUME [/vault/logs]
# Thu, 15 Apr 2021 07:31:01 GMT
VOLUME [/vault/file]
# Thu, 15 Apr 2021 07:31:01 GMT
EXPOSE 8200
# Thu, 15 Apr 2021 07:31:01 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Apr 2021 07:31:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 07:31:01 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:dee031f24faca3217cadd467d2cee7be95baa0c9dd9b51188fec034bf586bce7`  
		Last Modified: Wed, 14 Apr 2021 18:40:13 GMT  
		Size: 2.8 MB (2790063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03a1cd634e18906fff02479307a5e43d2420233b698e66700fe3de0a9afcdfff`  
		Last Modified: Thu, 15 Apr 2021 07:33:04 GMT  
		Size: 1.3 KB (1284 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88c5adc4c758d9d73918f13235f6b4b700c9c9eff1b1b17c7acf31fea76c3f29`  
		Last Modified: Thu, 15 Apr 2021 07:33:08 GMT  
		Size: 47.4 MB (47422501 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f80b9c4210596cfa2185634e07a0f33c9f7177b7a0d1f022cfede53a965dbb53`  
		Last Modified: Thu, 15 Apr 2021 07:33:01 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f6ffcc627bc58f0167992fc9d71bf425bab5f4e9cb0f5f339c57263cb7a9cf9`  
		Last Modified: Thu, 15 Apr 2021 07:33:04 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.5.7`

```console
$ docker pull vault@sha256:e1452f12d1f2671a7a0262be8cfb1a3a97cef747b1035262da4760873ba86447
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.5.7` - linux; amd64

```console
$ docker pull vault@sha256:b9bc496121878fbcb763304ee48e684258ff8e86831065cf403d726aceba8797
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55011192 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:64a3e3035197d19f6402e5422e35cb69863f50650deab8fd454ae9fe67d96a55`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 19:20:04 GMT
ADD file:c5377eaa926bf412dd8d4a08b0a1f2399cfd708743533b0aa03b53d14cb4bb4e in / 
# Wed, 14 Apr 2021 19:20:05 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:33:27 GMT
ARG VAULT_VERSION=1.5.7
# Wed, 14 Apr 2021 23:33:28 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 14 Apr 2021 23:33:33 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 14 Apr 2021 23:33:34 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 14 Apr 2021 23:33:35 GMT
VOLUME [/vault/logs]
# Wed, 14 Apr 2021 23:33:35 GMT
VOLUME [/vault/file]
# Wed, 14 Apr 2021 23:33:35 GMT
EXPOSE 8200
# Wed, 14 Apr 2021 23:33:35 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:33:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:33:35 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:396c31837116ac290458afcb928f68b6cc1c7bdd6963fc72f52f365a2a89c1b5`  
		Last Modified: Wed, 14 Apr 2021 19:21:14 GMT  
		Size: 2.8 MB (2798338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:977ece12193ef23d7bd1a4baa03e56e0ce1cf17be04ec959312abe0880793b0f`  
		Last Modified: Wed, 14 Apr 2021 23:35:21 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80eb5995d8c829801400fd2d3e2f3b08a24c91be1e08ff534e88f4aa7c8f4382`  
		Last Modified: Wed, 14 Apr 2021 23:35:31 GMT  
		Size: 52.2 MB (52209559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d5e8735dfae00ff39b10e23aee288bd2dc75fbcc4e824e59816acd9c1379fe0`  
		Last Modified: Wed, 14 Apr 2021 23:35:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92b20ed418560b129a4459f8f112d620a1fe050727c31e2facbf9255beb0ab5`  
		Last Modified: Wed, 14 Apr 2021 23:35:21 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.5.7` - linux; arm variant v6

```console
$ docker pull vault@sha256:563b1c4784ab153049a49f4e29b830572ae878ce669f6a8de56ceba9c041b1d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51564639 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c294fcc541992723658b275d280ea2c5df2c3b66469b598342f54f2a9308441a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:50:06 GMT
ADD file:eac3dead6ff32a5f6ff9d979fab38a22b12f32db204d32d07bc716ba404332d8 in / 
# Wed, 14 Apr 2021 18:50:07 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 06:19:06 GMT
ARG VAULT_VERSION=1.5.7
# Thu, 15 Apr 2021 06:19:08 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 15 Apr 2021 06:19:21 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 15 Apr 2021 06:19:23 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 15 Apr 2021 06:19:24 GMT
VOLUME [/vault/logs]
# Thu, 15 Apr 2021 06:19:25 GMT
VOLUME [/vault/file]
# Thu, 15 Apr 2021 06:19:26 GMT
EXPOSE 8200
# Thu, 15 Apr 2021 06:19:27 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Apr 2021 06:19:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 06:19:29 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f81e2ad47903c231a972c23a24be618247a23a768b7b5dc7a04a7fe73e9f9b1b`  
		Last Modified: Wed, 14 Apr 2021 18:50:51 GMT  
		Size: 2.6 MB (2575724 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92213c23ce8a502f87703d7ef639fb43f978e2158067c8ec5ecfece1efb7ebe`  
		Last Modified: Thu, 15 Apr 2021 06:22:04 GMT  
		Size: 1.3 KB (1291 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74a069ca03e9458ccea811466153c7ba9698a006051c273dae6b85fc29619dd5`  
		Last Modified: Thu, 15 Apr 2021 06:22:20 GMT  
		Size: 49.0 MB (48985617 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5dbce06b2aac800fe3323ee51c50b444819c81e9074988ea9779c3405e0430`  
		Last Modified: Thu, 15 Apr 2021 06:22:05 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a076c9396c928e8670cda2529e3241ac86db94fff86323472595b0ba00b971a`  
		Last Modified: Thu, 15 Apr 2021 06:22:05 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.5.7` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:fe0ac5f501e58276b7e2073878426992b3b0860b535103254e383c66466c7f62
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51918849 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f56bb5b097f3e00b399adc614f8e6817f95f1efe5a1a245f7083f924e509d390`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:43:16 GMT
ADD file:85a5071af4733240679a3799298092cb671cae007156a367219b6edf6cfc6377 in / 
# Wed, 14 Apr 2021 18:43:17 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 08:03:39 GMT
ARG VAULT_VERSION=1.5.7
# Thu, 15 Apr 2021 08:03:42 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 15 Apr 2021 08:03:51 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 15 Apr 2021 08:03:54 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 15 Apr 2021 08:03:55 GMT
VOLUME [/vault/logs]
# Thu, 15 Apr 2021 08:03:57 GMT
VOLUME [/vault/file]
# Thu, 15 Apr 2021 08:03:58 GMT
EXPOSE 8200
# Thu, 15 Apr 2021 08:03:59 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Apr 2021 08:04:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 08:04:01 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:26d14edc4f17638cda363ea80b29c55e83058fc0dff1129b38ea3e8231217f7d`  
		Last Modified: Wed, 14 Apr 2021 18:44:10 GMT  
		Size: 2.7 MB (2721209 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce811f96853fcf9e99ed4d4da185b4c96e7ab8b8add56ca3f38c9aa4008b832c`  
		Last Modified: Thu, 15 Apr 2021 08:06:18 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25f943933053155806a3de725ae6841d715bc90a674739ff6c270d4aec4ccba5`  
		Last Modified: Thu, 15 Apr 2021 08:06:31 GMT  
		Size: 49.2 MB (49194346 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:709a41a0e465b65f4d95a35b5d23277ea97b462423bf861c35be8680ea666ffb`  
		Last Modified: Thu, 15 Apr 2021 08:06:18 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65fe791f49d8d9f567de549b24b0172cf4d0063012cca7dd6263d8253008c1e2`  
		Last Modified: Thu, 15 Apr 2021 08:06:18 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.5.7` - linux; 386

```console
$ docker pull vault@sha256:1384c1cd1bf9b9b3c4e4d789013dba6402414de907d4cf95553c382922c9d623
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53088571 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ade4b8135ebce60c7839ea050268d948ad69b8e9ae04254476adcf9dcfad9979`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:47 GMT
ADD file:efe0af5733a00f82ae4fc3c5ccb3b69f4905c32fc85eefbdd02050c7d5801bca in / 
# Wed, 14 Apr 2021 18:38:48 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 07:30:39 GMT
ARG VAULT_VERSION=1.5.7
# Thu, 15 Apr 2021 07:30:39 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 15 Apr 2021 07:30:45 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 15 Apr 2021 07:30:46 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 15 Apr 2021 07:30:47 GMT
VOLUME [/vault/logs]
# Thu, 15 Apr 2021 07:30:47 GMT
VOLUME [/vault/file]
# Thu, 15 Apr 2021 07:30:47 GMT
EXPOSE 8200
# Thu, 15 Apr 2021 07:30:47 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Apr 2021 07:30:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 07:30:48 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:dee031f24faca3217cadd467d2cee7be95baa0c9dd9b51188fec034bf586bce7`  
		Last Modified: Wed, 14 Apr 2021 18:40:13 GMT  
		Size: 2.8 MB (2790063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c886555c2e0916b43902bda1833d57f77aba272fc14e5fbf81ca26ea1a52eb3f`  
		Last Modified: Thu, 15 Apr 2021 07:32:46 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afc68c3af7296e54f541c064c10bcc9c04aa19c1fe31ab32609ef2cf172a7475`  
		Last Modified: Thu, 15 Apr 2021 07:32:53 GMT  
		Size: 50.3 MB (50295218 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b967d5527a9ecf9e76e00eb880aa70439e4567922d46b036043016797071992c`  
		Last Modified: Thu, 15 Apr 2021 07:32:45 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d35d9806078f8acbb29bb21014b9f89f861e31e9838e685874ca2a24f61c9cb8`  
		Last Modified: Thu, 15 Apr 2021 07:32:45 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.6.3`

```console
$ docker pull vault@sha256:dac5f4f14d92dd59b0d3923cc5aeb7c70207590563b664295ca3f4f7ffec8c76
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.6.3` - linux; amd64

```console
$ docker pull vault@sha256:55183a92e2f97188d4f4372c765213977c1d80137fe8775f641cddf540860a40
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68983150 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40e169bb684a93be500876a1a82f90e862784d8dfd2d39512a09ffacbd2e26cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:33:01 GMT
ARG VAULT_VERSION=1.6.3
# Wed, 14 Apr 2021 23:33:02 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 14 Apr 2021 23:33:19 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 14 Apr 2021 23:33:20 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 14 Apr 2021 23:33:20 GMT
VOLUME [/vault/logs]
# Wed, 14 Apr 2021 23:33:20 GMT
VOLUME [/vault/file]
# Wed, 14 Apr 2021 23:33:21 GMT
EXPOSE 8200
# Wed, 14 Apr 2021 23:33:21 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:33:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:33:21 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c48208a9d912b6f55e551cf7f38862c155fa34ce2a9ed4871bc9d3241eb6c7`  
		Last Modified: Wed, 14 Apr 2021 23:35:01 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:33e02fad8a52224cae5995f086cb1ad40e12975f11e7b407f7be793d1cd188b1`  
		Last Modified: Wed, 14 Apr 2021 23:35:12 GMT  
		Size: 66.2 MB (66167915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8964ac276d4a9b628ded19ae18f6c60e3562f48b2c3b515d92ca84064e099251`  
		Last Modified: Wed, 14 Apr 2021 23:35:01 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1162d013f2c24c8124cd256c9572be008832c86bdf7d9126d6fb00a6810c6127`  
		Last Modified: Wed, 14 Apr 2021 23:35:01 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.6.3` - linux; arm variant v6

```console
$ docker pull vault@sha256:a4b03d4495e3dcb7d91610b75a546983277e6236ea651ca450b78483ca41144b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63718994 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb2ef16fa61cc8ecdecd77170b36315ace9214c839515b2805ca95f2a5e1882b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 06:18:23 GMT
ARG VAULT_VERSION=1.6.3
# Thu, 15 Apr 2021 06:18:26 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 15 Apr 2021 06:18:40 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 15 Apr 2021 06:18:46 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 15 Apr 2021 06:18:49 GMT
VOLUME [/vault/logs]
# Thu, 15 Apr 2021 06:18:52 GMT
VOLUME [/vault/file]
# Thu, 15 Apr 2021 06:18:53 GMT
EXPOSE 8200
# Thu, 15 Apr 2021 06:18:53 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Apr 2021 06:18:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 06:18:55 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13ac1f74812be45e85ae3dc284a37418d71978d6a46a6d4eb8a1d6279e624b8e`  
		Last Modified: Thu, 15 Apr 2021 06:21:40 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d001c5e3340edd296de9d4bf8a0aff2920edb63de10630462fb0e3216d1ca43`  
		Last Modified: Thu, 15 Apr 2021 06:21:58 GMT  
		Size: 61.1 MB (61093598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea567b0da812b9bff49c65775fa975d51b6f7a1cf01be418e054fe55a39c31c0`  
		Last Modified: Thu, 15 Apr 2021 06:21:41 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:461baaea6b54c71b837310837204992b1b8113fd44a8e96fd6ddac726b7bf639`  
		Last Modified: Thu, 15 Apr 2021 06:21:41 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.6.3` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:b8b06d92a5d58891d83f3ff9540a6054a9400ab10e35c1a530038a20c1f2d42a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (65016423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:69800f06fb63d8f404f91817744c66c4d5938dfff552cdd4df5c056e6b45ab58`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 08:03:08 GMT
ARG VAULT_VERSION=1.6.3
# Thu, 15 Apr 2021 08:03:10 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 15 Apr 2021 08:03:20 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 15 Apr 2021 08:03:23 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 15 Apr 2021 08:03:24 GMT
VOLUME [/vault/logs]
# Thu, 15 Apr 2021 08:03:25 GMT
VOLUME [/vault/file]
# Thu, 15 Apr 2021 08:03:26 GMT
EXPOSE 8200
# Thu, 15 Apr 2021 08:03:27 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Apr 2021 08:03:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 08:03:29 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e234bde63d3e954cd1e4ade1915dd2ce8b8ea3583099e65559bdf0c9708fcd1`  
		Last Modified: Thu, 15 Apr 2021 08:05:55 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9e3c93d6b3e992483a7c29d62305eda58a673c9c2c8cabcf65c6b625b83a1bd`  
		Last Modified: Thu, 15 Apr 2021 08:06:07 GMT  
		Size: 62.3 MB (62301131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05fa6d34ea79a41298fa3857ef2d7414e8735ea5bb0bbdb0977ece125a4a18c2`  
		Last Modified: Thu, 15 Apr 2021 08:05:55 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f61c70ed0ffd59a85848e1ecc973308df1b84fd4d76f0a14558eb1877e85ba8e`  
		Last Modified: Thu, 15 Apr 2021 08:05:55 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.6.3` - linux; 386

```console
$ docker pull vault@sha256:2d4b381c4cb3960caea1fe60e7745e7595bc115f86ccaeb7dcee57e92fd42e8e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67033887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c1d07530f438c0dbb2f3360de96f018aaafc771f21a09427888d4a1d5be606fb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 07:30:23 GMT
ARG VAULT_VERSION=1.6.3
# Thu, 15 Apr 2021 07:30:24 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 15 Apr 2021 07:30:31 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 15 Apr 2021 07:30:32 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 15 Apr 2021 07:30:33 GMT
VOLUME [/vault/logs]
# Thu, 15 Apr 2021 07:30:33 GMT
VOLUME [/vault/file]
# Thu, 15 Apr 2021 07:30:33 GMT
EXPOSE 8200
# Thu, 15 Apr 2021 07:30:33 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Apr 2021 07:30:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 07:30:34 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1764dca5737cc1569878753a5062646fa31bd42d180bed48c13415ae889994a`  
		Last Modified: Thu, 15 Apr 2021 07:32:26 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae0a04805b117d13fc339935a293ce8533693118a105fbb55d8719bf38782a4a`  
		Last Modified: Thu, 15 Apr 2021 07:32:36 GMT  
		Size: 64.2 MB (64211723 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59c313655f3a50f55b917d663fc9dd9b53ab98202e86b8d23aa4a0eea352de39`  
		Last Modified: Thu, 15 Apr 2021 07:32:27 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b998d34a61939e5a41f2d816a9e8aa96d2898cd1e0caa48f6c46aa45601f3e36`  
		Last Modified: Thu, 15 Apr 2021 07:32:26 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.7.0`

```console
$ docker pull vault@sha256:61a386a6fcb6cb9fa0aa32c8df5c4a913819a6297733ce3a228fa7aaca489f5f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.7.0` - linux; amd64

```console
$ docker pull vault@sha256:e218aa2a8d80fc25c1ddae492c561e74d08e2c928a88d4f96e1ccc25a37e4b22
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72707013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432c4edbf4b8a0554bb904d97136912887198dcdc84153ec15d2f6fa50f6a3b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:32:09 GMT
ARG VAULT_VERSION=1.7.0
# Wed, 14 Apr 2021 23:32:10 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 14 Apr 2021 23:32:27 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 14 Apr 2021 23:32:28 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 14 Apr 2021 23:32:28 GMT
VOLUME [/vault/logs]
# Wed, 14 Apr 2021 23:32:29 GMT
VOLUME [/vault/file]
# Wed, 14 Apr 2021 23:32:29 GMT
EXPOSE 8200
# Wed, 14 Apr 2021 23:32:29 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:32:29 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e47ca89f619c6efbe8c9381e96824ba56511ffc8b2935f403c5de2bd6b8a322`  
		Last Modified: Wed, 14 Apr 2021 23:34:05 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db20698d79d24cfa4df7808d221f918609d0cb38d829a6f4aa8e912265e50cdb`  
		Last Modified: Wed, 14 Apr 2021 23:34:14 GMT  
		Size: 69.9 MB (69891779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e539904218df495c5136d799fc260f12e2072c6a21d2984a44bf2d28a83e3da`  
		Last Modified: Wed, 14 Apr 2021 23:34:05 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9e9a69a7f1d325abdfdde6de6b6aefd36ff2408fb62470d49602ae50aeb1b2`  
		Last Modified: Wed, 14 Apr 2021 23:34:05 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0` - linux; arm variant v6

```console
$ docker pull vault@sha256:d594fb96e6019d607484d57f3780ddc5f7e546049211a84542068a15f845d8be
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66726634 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26660e9bd3567cdd08032195f269d53b9d7f53730fb02d9a8a53c536b93f2dca`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 06:16:35 GMT
ARG VAULT_VERSION=1.7.0
# Thu, 15 Apr 2021 06:16:37 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 15 Apr 2021 06:16:54 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 15 Apr 2021 06:16:58 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 15 Apr 2021 06:16:58 GMT
VOLUME [/vault/logs]
# Thu, 15 Apr 2021 06:16:59 GMT
VOLUME [/vault/file]
# Thu, 15 Apr 2021 06:17:01 GMT
EXPOSE 8200
# Thu, 15 Apr 2021 06:17:01 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Apr 2021 06:17:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 06:17:03 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08d9c6c909210b42db6e550a001e44067922224dd1bbdd3aac3ea148792fe671`  
		Last Modified: Thu, 15 Apr 2021 06:20:21 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04cad5360050db4fe535b69095f0bfbbc9611b33296cd0dee3ea8df0a1ab06ae`  
		Last Modified: Thu, 15 Apr 2021 06:20:44 GMT  
		Size: 64.1 MB (64101241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:329c6ff7cba2492258b7ca02205b499f0fc071a18571e171158462bcfe4f3126`  
		Last Modified: Thu, 15 Apr 2021 06:20:22 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6870aae5b33b0a9670a09c2d4ce647a000118088ce29294d3279baf7d04f3e1e`  
		Last Modified: Thu, 15 Apr 2021 06:20:21 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:7f55715a780f7283749747b5ed569bce4cf1c9bd63dde0ea532bbf54c00eec9d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68535951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:411609b8bbe4654e155ee9a09efe521b629251bd67bff92cd7c3523a8b21f66b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 08:01:31 GMT
ARG VAULT_VERSION=1.7.0
# Thu, 15 Apr 2021 08:01:34 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 15 Apr 2021 08:01:43 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 15 Apr 2021 08:01:46 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 15 Apr 2021 08:01:47 GMT
VOLUME [/vault/logs]
# Thu, 15 Apr 2021 08:01:48 GMT
VOLUME [/vault/file]
# Thu, 15 Apr 2021 08:01:49 GMT
EXPOSE 8200
# Thu, 15 Apr 2021 08:01:50 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Apr 2021 08:01:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 08:01:52 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:14e3d04ec30b7c39f94ae4fd83298728d3eae91be1852e179c632084ce841e7a`  
		Last Modified: Thu, 15 Apr 2021 08:04:49 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22309ca14ea027ac0421fd5a78fca6fe6226acb07ef3e1b12fd4fe2de818e8d9`  
		Last Modified: Thu, 15 Apr 2021 08:05:04 GMT  
		Size: 65.8 MB (65820658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7655689df09438ed4656e740a1c9d058e429227ce9987f6f8d5b79d057aa4e7f`  
		Last Modified: Thu, 15 Apr 2021 08:04:50 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecf0844481d0e0a9ef42d03b226a4ca74f64ccd005dd587680e9c5382e495cf9`  
		Last Modified: Thu, 15 Apr 2021 08:04:49 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0` - linux; 386

```console
$ docker pull vault@sha256:274dbae42b3e591c7a5ff5e40aed6776b4cdcd71c5348a4998a7ef45277d0a4f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70570799 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6ae889a842747d2296863f1a816f37b15d788e7a51b0fd1db71ea9ad9ee16c4a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 07:29:27 GMT
ARG VAULT_VERSION=1.7.0
# Thu, 15 Apr 2021 07:29:28 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 15 Apr 2021 07:29:45 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 15 Apr 2021 07:29:46 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 15 Apr 2021 07:29:46 GMT
VOLUME [/vault/logs]
# Thu, 15 Apr 2021 07:29:46 GMT
VOLUME [/vault/file]
# Thu, 15 Apr 2021 07:29:46 GMT
EXPOSE 8200
# Thu, 15 Apr 2021 07:29:46 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Apr 2021 07:29:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 07:29:47 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f944069b5afc37b5ca0933428cc61a14555417a76391c707fc35d603d305794`  
		Last Modified: Thu, 15 Apr 2021 07:31:27 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9108913be301d75a08af69b99b00a96acd7e24b20653df6162727631dad404d`  
		Last Modified: Thu, 15 Apr 2021 07:31:36 GMT  
		Size: 67.7 MB (67748638 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e5d1e9467cc2f50525f71c6030157919bc1b20d0700284e97ac84608585b0b3`  
		Last Modified: Thu, 15 Apr 2021 07:31:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d993df13347eeaad3fb163d3905e8a13347b9bf02323e9b8a5481a1e90786a3`  
		Last Modified: Thu, 15 Apr 2021 07:31:26 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.7.0-rc1`

```console
$ docker pull vault@sha256:0476796ed02a6f6399c8899f631b50bf8ae578b3c6499e8f7b233411eea3a6db
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.7.0-rc1` - linux; amd64

```console
$ docker pull vault@sha256:de502a810737693895a760248d25d7deba78de44e399975cc9df54da48e3a01b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72670903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ee4a73808b949db3fe41c2929c74d0ac521518bae51813fed89c4990b467270`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:32:48 GMT
ARG VAULT_VERSION=1.7.0-rc1
# Wed, 14 Apr 2021 23:32:49 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 14 Apr 2021 23:32:56 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 14 Apr 2021 23:32:57 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 14 Apr 2021 23:32:57 GMT
VOLUME [/vault/logs]
# Wed, 14 Apr 2021 23:32:58 GMT
VOLUME [/vault/file]
# Wed, 14 Apr 2021 23:32:58 GMT
EXPOSE 8200
# Wed, 14 Apr 2021 23:32:58 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:32:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:32:58 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740606ea9be68fc7e1dcc52b55586bd7b35959d7cbee761a77c348b76ae70769`  
		Last Modified: Wed, 14 Apr 2021 23:34:43 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fc6f0c9f23b754f027eaabe4596673608dda81bb86c4e959abc7d08bb3a9f8e`  
		Last Modified: Wed, 14 Apr 2021 23:34:52 GMT  
		Size: 69.9 MB (69855669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4e0daa1ae536d1cd69a797663189f446b67be14a72b4fb59b282b9c0055173`  
		Last Modified: Wed, 14 Apr 2021 23:34:43 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:287fdf9cbabdc270a13849541dc9c95c01b230c9d154dbcc88ea0348009dd06d`  
		Last Modified: Wed, 14 Apr 2021 23:34:43 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0-rc1` - linux; arm variant v6

```console
$ docker pull vault@sha256:ca64f5ae6da53bf4705f5c75681ee31d3ec1958f9a5c7cc40c8b25466d521e66
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66701286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ebed69cd5fdaa19bef12cbc4523a338543fca2789a66578ea3a43392f4b4a38`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 06:17:53 GMT
ARG VAULT_VERSION=1.7.0-rc1
# Thu, 15 Apr 2021 06:17:56 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 15 Apr 2021 06:18:09 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 15 Apr 2021 06:18:12 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 15 Apr 2021 06:18:13 GMT
VOLUME [/vault/logs]
# Thu, 15 Apr 2021 06:18:14 GMT
VOLUME [/vault/file]
# Thu, 15 Apr 2021 06:18:15 GMT
EXPOSE 8200
# Thu, 15 Apr 2021 06:18:16 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Apr 2021 06:18:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 06:18:18 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4fcfada7c373b9ec158409e868ff09c5a8102316c54368fa1f965d0e8cc7a83`  
		Last Modified: Thu, 15 Apr 2021 06:21:17 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a498e9806be7e049f5637891cfa8c7e2ef4bfb9a22269ac927f035b14c5d9f2`  
		Last Modified: Thu, 15 Apr 2021 06:21:35 GMT  
		Size: 64.1 MB (64075890 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f3a7a6058b5503b2b407e17ca9d3b9f9bf41ed986c41617a24aab81c91b824e`  
		Last Modified: Thu, 15 Apr 2021 06:21:17 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d01580f09d730da494aa53a1f82c1c627521024fd57975fdb48392e6b0590a46`  
		Last Modified: Thu, 15 Apr 2021 06:21:17 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0-rc1` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:50f89f8f72adc87c6b7e1801e8bb73cc32f9a878f9ed539851c76b5256ff2c43
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68500426 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ea511d2fd959da0746c8357d6cd6e2b5198c49dc0c168a52538ce8b399da18f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 08:02:36 GMT
ARG VAULT_VERSION=1.7.0-rc1
# Thu, 15 Apr 2021 08:02:38 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 15 Apr 2021 08:02:48 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 15 Apr 2021 08:02:52 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 15 Apr 2021 08:02:53 GMT
VOLUME [/vault/logs]
# Thu, 15 Apr 2021 08:02:54 GMT
VOLUME [/vault/file]
# Thu, 15 Apr 2021 08:02:55 GMT
EXPOSE 8200
# Thu, 15 Apr 2021 08:02:56 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Apr 2021 08:02:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 08:02:57 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:321c23508dfeab5d93f811a26322808d351060a46ce94c693696eeef2e442cd8`  
		Last Modified: Thu, 15 Apr 2021 08:05:34 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1059bef1f0f69ab171ffa0c944ac6a34fa9e2b71bd1a834a077fcf4e283faf9d`  
		Last Modified: Thu, 15 Apr 2021 08:05:49 GMT  
		Size: 65.8 MB (65785134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58e96db1177a17c5410f93aace714bd73b6f66fc50756207f01e524f3e565fd8`  
		Last Modified: Thu, 15 Apr 2021 08:05:34 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ace980cac8c0ac5340c117fad94a6098795da019a6041929a6127d2faaf0e216`  
		Last Modified: Thu, 15 Apr 2021 08:05:33 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0-rc1` - linux; 386

```console
$ docker pull vault@sha256:4a99f32fed840a88ceba1a5b37f9485ed30f0f37fce8bcf286d0ed6b7ce8bd3e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70535947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23445b43c8557f36a5fcb8c39adf2878f7970ac629ad59702f38df0f5400b4b5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 07:30:09 GMT
ARG VAULT_VERSION=1.7.0-rc1
# Thu, 15 Apr 2021 07:30:09 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 15 Apr 2021 07:30:17 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 15 Apr 2021 07:30:18 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 15 Apr 2021 07:30:18 GMT
VOLUME [/vault/logs]
# Thu, 15 Apr 2021 07:30:18 GMT
VOLUME [/vault/file]
# Thu, 15 Apr 2021 07:30:18 GMT
EXPOSE 8200
# Thu, 15 Apr 2021 07:30:18 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Apr 2021 07:30:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 07:30:19 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e55dfdcdf2d668e05af527e574465dad858aca62ef1f157491f53647418477d`  
		Last Modified: Thu, 15 Apr 2021 07:32:08 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6649931728fd1211760789c5f9c2a3a59bb7e71390a75d317a21fe2d2853099c`  
		Last Modified: Thu, 15 Apr 2021 07:32:18 GMT  
		Size: 67.7 MB (67713786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f169dd6a94d5d89d922b166fe19a9c084de18c83b774ff7fdd9a2a2ddf5cf07`  
		Last Modified: Thu, 15 Apr 2021 07:32:09 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040f24ae85eae629393d2de798ee1cd09d29c0bff2c209b03b5dce4537a3005e`  
		Last Modified: Thu, 15 Apr 2021 07:32:10 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.7.0-rc2`

```console
$ docker pull vault@sha256:5fcd45747cc5dc01fa54353447c973114f7142b38a3b66539dcb0a6e08afd3f2
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.7.0-rc2` - linux; amd64

```console
$ docker pull vault@sha256:dc1e8fb0de08e01b6c8d1e397583a27696aafc0c07dd3882bb0e889c936218fe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72667676 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76cb9453ef123ee868f48ba0a9126d34b0f98de60ef65d5130834188d64874c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:32:35 GMT
ARG VAULT_VERSION=1.7.0-rc2
# Wed, 14 Apr 2021 23:32:36 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 14 Apr 2021 23:32:42 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 14 Apr 2021 23:32:43 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 14 Apr 2021 23:32:44 GMT
VOLUME [/vault/logs]
# Wed, 14 Apr 2021 23:32:44 GMT
VOLUME [/vault/file]
# Wed, 14 Apr 2021 23:32:44 GMT
EXPOSE 8200
# Wed, 14 Apr 2021 23:32:44 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:32:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:32:45 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1060185671752ed8d29a0d606672aa62c281046561a08084f949bd4487d6cdb`  
		Last Modified: Wed, 14 Apr 2021 23:34:28 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9343043677925bc13ee73bae70715a7c45998945905d9c65a253dd80a7e47a3`  
		Last Modified: Wed, 14 Apr 2021 23:34:34 GMT  
		Size: 69.9 MB (69852442 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f211fd460329e123f6ff304608dc6c6fd6d2989df73cd6a65b0d8843cd2fa9a`  
		Last Modified: Wed, 14 Apr 2021 23:34:25 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a80b7e8e9947936cbe7e8e1abde854f7307818764bdd81ac4b50f5026923ce74`  
		Last Modified: Wed, 14 Apr 2021 23:34:25 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0-rc2` - linux; arm variant v6

```console
$ docker pull vault@sha256:c1a2c8d5ca758676e374f88fe1700bbc07402325a6d12ab6a7c79ff7e5217fda
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66702819 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b809d887ed74732e8b8820f1440cd7e4e16bf9c3b399544f1ec04bf70e32d83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 06:17:12 GMT
ARG VAULT_VERSION=1.7.0-rc2
# Thu, 15 Apr 2021 06:17:16 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 15 Apr 2021 06:17:30 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 15 Apr 2021 06:17:34 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 15 Apr 2021 06:17:35 GMT
VOLUME [/vault/logs]
# Thu, 15 Apr 2021 06:17:37 GMT
VOLUME [/vault/file]
# Thu, 15 Apr 2021 06:17:38 GMT
EXPOSE 8200
# Thu, 15 Apr 2021 06:17:39 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Apr 2021 06:17:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 06:17:42 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83438b519662b8df9a327cbed7e4193a7124efe63b2a381db6a324ae8130873d`  
		Last Modified: Thu, 15 Apr 2021 06:20:53 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae1a8b393d0d3f24687aeb0603a39886804e7375b4b464f688d67ad4af3692f`  
		Last Modified: Thu, 15 Apr 2021 06:21:10 GMT  
		Size: 64.1 MB (64077422 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0461027527c1339817ca61ba0105659fad7e933a86a6a1a821f1d7e7b370d4c`  
		Last Modified: Thu, 15 Apr 2021 06:20:53 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:212a36941bd3b29270eeeef0988f1bd997747a21f7ff34da49f4fc21d6da4dfe`  
		Last Modified: Thu, 15 Apr 2021 06:20:53 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0-rc2` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:1be19b0315cb039d8b655cdada9e1801854aff05bd6826044696c34705655b68
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68525750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:346f1d23f83c2dd4be5c1b7a09f3928ca58251033c3bb1fdee39f419e5d62066`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 08:01:59 GMT
ARG VAULT_VERSION=1.7.0-rc2
# Thu, 15 Apr 2021 08:02:03 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 15 Apr 2021 08:02:16 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 15 Apr 2021 08:02:20 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 15 Apr 2021 08:02:21 GMT
VOLUME [/vault/logs]
# Thu, 15 Apr 2021 08:02:23 GMT
VOLUME [/vault/file]
# Thu, 15 Apr 2021 08:02:24 GMT
EXPOSE 8200
# Thu, 15 Apr 2021 08:02:26 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Apr 2021 08:02:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 08:02:28 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98242f9e38853fc9aeaeec2409b705ce88aff6c879ffa80570925a34370eb9a5`  
		Last Modified: Thu, 15 Apr 2021 08:05:15 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3b1d029e68fdabf490ee905e9b5f0c2555a021bb97e39113666dd36afe8d880e`  
		Last Modified: Thu, 15 Apr 2021 08:05:27 GMT  
		Size: 65.8 MB (65810460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77fcaadbd22b681f2b4bedf6c7b73f9c62e1dbd1b272484def8adb39641a91f9`  
		Last Modified: Thu, 15 Apr 2021 08:05:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59376d62d3dfcdc75df21adc91587a58e53a0b822495ed7105c0532ef3d89a75`  
		Last Modified: Thu, 15 Apr 2021 08:05:13 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0-rc2` - linux; 386

```console
$ docker pull vault@sha256:177412860887401c5375c88ed32b7780149ba79671604f09db9d52ba19bd4a75
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70540365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf08540bbfeda1c67a57ed0f24ff98dd415a365fefdf53ba11627ede11858d4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 15 Apr 2021 07:29:54 GMT
ARG VAULT_VERSION=1.7.0-rc2
# Thu, 15 Apr 2021 07:29:55 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 15 Apr 2021 07:30:02 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 15 Apr 2021 07:30:03 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 15 Apr 2021 07:30:03 GMT
VOLUME [/vault/logs]
# Thu, 15 Apr 2021 07:30:03 GMT
VOLUME [/vault/file]
# Thu, 15 Apr 2021 07:30:03 GMT
EXPOSE 8200
# Thu, 15 Apr 2021 07:30:03 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 15 Apr 2021 07:30:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 15 Apr 2021 07:30:04 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4c76426b45e98b33c315003ada5bdc0356c01a8b331b05e74534c5d3a275fcb`  
		Last Modified: Thu, 15 Apr 2021 07:31:48 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ace9f444dafd3445fd40d04dafefd5c90b5dd96e9af6dc74f9663a71ed07a3`  
		Last Modified: Thu, 15 Apr 2021 07:31:58 GMT  
		Size: 67.7 MB (67718197 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2563edc847008972e38a141b0c3767dc62899aba30717123490ea3069bffd2b5`  
		Last Modified: Thu, 15 Apr 2021 07:31:48 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d1a1c3c8bda9e004d8c385e8c8b4cf6846115af4ffbdb3110a4ede5063fc09e`  
		Last Modified: Thu, 15 Apr 2021 07:31:48 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:latest`

```console
$ docker pull vault@sha256:e6a9f932a56bdc3e716f81ce3956a1fc968645f08a1087f933279537c3712f45
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:e218aa2a8d80fc25c1ddae492c561e74d08e2c928a88d4f96e1ccc25a37e4b22
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72707013 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:432c4edbf4b8a0554bb904d97136912887198dcdc84153ec15d2f6fa50f6a3b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 23:32:09 GMT
ARG VAULT_VERSION=1.7.0
# Wed, 14 Apr 2021 23:32:10 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 14 Apr 2021 23:32:27 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 14 Apr 2021 23:32:28 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 14 Apr 2021 23:32:28 GMT
VOLUME [/vault/logs]
# Wed, 14 Apr 2021 23:32:29 GMT
VOLUME [/vault/file]
# Wed, 14 Apr 2021 23:32:29 GMT
EXPOSE 8200
# Wed, 14 Apr 2021 23:32:29 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Apr 2021 23:32:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Apr 2021 23:32:29 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e47ca89f619c6efbe8c9381e96824ba56511ffc8b2935f403c5de2bd6b8a322`  
		Last Modified: Wed, 14 Apr 2021 23:34:05 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db20698d79d24cfa4df7808d221f918609d0cb38d829a6f4aa8e912265e50cdb`  
		Last Modified: Wed, 14 Apr 2021 23:34:14 GMT  
		Size: 69.9 MB (69891779 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e539904218df495c5136d799fc260f12e2072c6a21d2984a44bf2d28a83e3da`  
		Last Modified: Wed, 14 Apr 2021 23:34:05 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9e9a69a7f1d325abdfdde6de6b6aefd36ff2408fb62470d49602ae50aeb1b2`  
		Last Modified: Wed, 14 Apr 2021 23:34:05 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:75739463a8000a8bc3709b952e4dbc1e4577cd7d8f0a0ed2933f8a98f9104fb3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66746361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaeff817a9d594bfc213819fee619bdaeb2bc3dd8f71433ac0524d9aaa95bcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 00:03:22 GMT
ARG VAULT_VERSION=1.7.1
# Thu, 22 Apr 2021 00:03:25 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 22 Apr 2021 00:03:39 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 22 Apr 2021 00:03:42 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 22 Apr 2021 00:03:42 GMT
VOLUME [/vault/logs]
# Thu, 22 Apr 2021 00:03:43 GMT
VOLUME [/vault/file]
# Thu, 22 Apr 2021 00:03:44 GMT
EXPOSE 8200
# Thu, 22 Apr 2021 00:03:45 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Apr 2021 00:03:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 00:03:47 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3255facdf2728fe182f052e94f0479bbaf6cadfbe8cd4aa978c8803f8738f9e5`  
		Last Modified: Thu, 22 Apr 2021 00:05:06 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c547d8de9ec409e430255410de106de39ff878a36758d71f6818dc799566d252`  
		Last Modified: Thu, 22 Apr 2021 00:05:22 GMT  
		Size: 64.1 MB (64120962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b228f949e5779456017dd39918f3ae59a5d466e498b0cf054f7cc89bc27c515b`  
		Last Modified: Thu, 22 Apr 2021 00:05:06 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee2ad32bff6754a64decc8b1a5113e295eda8606423b3261cc2595d904cb556`  
		Last Modified: Thu, 22 Apr 2021 00:05:06 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:22bd3bd288973afbe2fe51004c64ad04f5803f51250c18def7b96b462e97b38d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68609349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f8c5f66a6428d7e372609f75666ad04b4ec688292e8d9b6f89ac0682b435ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 21 Apr 2021 23:42:02 GMT
ARG VAULT_VERSION=1.7.1
# Wed, 21 Apr 2021 23:42:04 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 21 Apr 2021 23:42:13 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 21 Apr 2021 23:42:16 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 21 Apr 2021 23:42:17 GMT
VOLUME [/vault/logs]
# Wed, 21 Apr 2021 23:42:18 GMT
VOLUME [/vault/file]
# Wed, 21 Apr 2021 23:42:18 GMT
EXPOSE 8200
# Wed, 21 Apr 2021 23:42:19 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Apr 2021 23:42:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Apr 2021 23:42:21 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afbab083caa522eaa170c65751dfbd70588d3d1339718ef76783388716ffafe`  
		Last Modified: Wed, 21 Apr 2021 23:43:25 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1878b93e8bf7428c9f64cc136aec8f260a6c45de1cc74dc1ba782370b8df6aec`  
		Last Modified: Wed, 21 Apr 2021 23:43:39 GMT  
		Size: 65.9 MB (65894058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f32296b0b49ad7b325c4acdae677d63b61cd73bd49a2cbf1bf078f30c7aa7f`  
		Last Modified: Wed, 21 Apr 2021 23:43:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabfc9e3c880ad5c72b17f06c96faa62a33b1214d14511abda81d059301e76c6`  
		Last Modified: Wed, 21 Apr 2021 23:43:25 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:661c3c426525f8a7b246dcde3de08a1a06f1c80daddf963aaadcc60a8432dab1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70582514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab923df6f9daf4521d48e608fd79f5dc62e3e185f771f1a262335cab7b6e70d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Wed, 21 Apr 2021 23:41:23 GMT
ARG VAULT_VERSION=1.7.1
# Wed, 21 Apr 2021 23:41:24 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 21 Apr 2021 23:41:33 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 21 Apr 2021 23:41:34 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 21 Apr 2021 23:41:34 GMT
VOLUME [/vault/logs]
# Wed, 21 Apr 2021 23:41:34 GMT
VOLUME [/vault/file]
# Wed, 21 Apr 2021 23:41:35 GMT
EXPOSE 8200
# Wed, 21 Apr 2021 23:41:35 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Apr 2021 23:41:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Apr 2021 23:41:35 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1dd406aad66bc47a2a17b2d6a848d762f4787471afd3fabcb8318a4be343e3`  
		Last Modified: Wed, 21 Apr 2021 23:42:27 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d2281cd90daca415c01bd1088232356df75260fa2e29ae66817bfff7e0af45`  
		Last Modified: Wed, 21 Apr 2021 23:42:44 GMT  
		Size: 67.8 MB (67760352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bd8116cdd83cf85d77a626989b4f854834394a3900cdc4c87ac05d61795f9e`  
		Last Modified: Wed, 21 Apr 2021 23:42:27 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b240059e0c23ad083ef13f3846a09a02a372006486590acd1fff81c8aaff45`  
		Last Modified: Wed, 21 Apr 2021 23:42:27 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
