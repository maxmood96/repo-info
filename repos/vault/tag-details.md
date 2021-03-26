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
$ docker pull vault@sha256:71eb107124f5843756e84532820275744e1a8a1b4e7e7e4c061f45afdad56ba1
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.4.7` - linux; amd64

```console
$ docker pull vault@sha256:efce1d7a6d51f0f4a3ca11cdf71af5d4a26167540cec763aa26cda073f91b143
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52081953 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:399211ba7e802a8bc2671369bd03b209694dc6f5c1c5e6933078726005d782a4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:48 GMT
ADD file:41685950b607fe90e0886c857e4efdafab1e43a09def174a4ea97f8ec624370b in / 
# Thu, 25 Mar 2021 22:19:48 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 05:04:30 GMT
ARG VAULT_VERSION=1.4.7
# Fri, 26 Mar 2021 05:04:31 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 05:04:36 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 05:04:37 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 05:04:37 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 05:04:38 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 05:04:38 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 05:04:38 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 05:04:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 05:04:38 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:c8bc66e2636f8133df434e1bce741b6b7fb21515e7c8a554a805b73f5fdae2de`  
		Last Modified: Thu, 25 Mar 2021 22:20:57 GMT  
		Size: 2.8 MB (2797179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ac20e13ef02f7cef8d8a0a19bc6001ba5ebfc945fe2f40f7bfb1c19010b218`  
		Last Modified: Fri, 26 Mar 2021 05:06:39 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:792a5e5d70ba9827ebb2518cab64bbcf5690de2777367e61a78cda687964692c`  
		Last Modified: Fri, 26 Mar 2021 05:06:48 GMT  
		Size: 49.3 MB (49281483 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e6a499157b7cd8993a265416b1c026c2094e634e8340d2f8a43978ebef3ffd`  
		Last Modified: Fri, 26 Mar 2021 05:06:39 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5a8342e9c9160b83f34a3520b9fc9e30ab48db104d1ae284b9cf6b41c8c1cdb`  
		Last Modified: Fri, 26 Mar 2021 05:06:39 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.4.7` - linux; arm variant v6

```console
$ docker pull vault@sha256:1d7cdd3157c0730e403268c42b1664c7a12a357fed370a76dc83162e1fb7cd69
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48719706 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0cf464349a93aca1192e4aa9a035dec84f5b917d73df3f0b972c8586b40a73a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 24 Feb 2021 20:50:55 GMT
ADD file:9e81f449863b2d114afc239efa445f3bed6ff45b123ea3aad271a5631ac4fa13 in / 
# Wed, 24 Feb 2021 20:50:56 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:37:59 GMT
ARG VAULT_VERSION=1.4.7
# Wed, 24 Feb 2021 23:38:01 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 24 Feb 2021 23:38:12 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 24 Feb 2021 23:38:14 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 24 Feb 2021 23:38:14 GMT
VOLUME [/vault/logs]
# Wed, 24 Feb 2021 23:38:15 GMT
VOLUME [/vault/file]
# Wed, 24 Feb 2021 23:38:16 GMT
EXPOSE 8200
# Wed, 24 Feb 2021 23:38:16 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:38:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:38:18 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:615b6501bf7ed56706d638bf075665f504b2fee0bdebf905dcb8610bc9271fa4`  
		Last Modified: Wed, 24 Feb 2021 20:51:33 GMT  
		Size: 2.6 MB (2574559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c493d5d6dd04e6c618a2a05545ed54f80425ee3ed724bd08f61f6a9a23760fed`  
		Last Modified: Wed, 24 Feb 2021 23:39:21 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:847e00f8e155413726c1399b24fd39855b85c0e5c680cd9899bd4ac4e57b8f6e`  
		Last Modified: Wed, 24 Feb 2021 23:39:33 GMT  
		Size: 46.1 MB (46141854 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a89c1e265b041edc4d3e36f1b93cfb8e3670c1453d620ee57fb087b52d9d72ed`  
		Last Modified: Wed, 24 Feb 2021 23:39:21 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:faeaa20bf0f90081dc23437718d36e14f3932144e6327241205c897074f3e0a3`  
		Last Modified: Wed, 24 Feb 2021 23:39:21 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.4.7` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:8cc9b11c41d3d548f20c9372abe9c2fa61cb76d88d001fd4dd7c53c37eb5bb21
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48964606 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cfcc717da55b17d38d94ab422a30a7fddbfe1ad425f21a04958c987615f49eb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:42:23 GMT
ADD file:a65de3d22c60aa364e967325d628757aa1f842fbefa48420403da87f91e9b7fd in / 
# Thu, 25 Mar 2021 22:42:41 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:15:41 GMT
ARG VAULT_VERSION=1.4.7
# Fri, 26 Mar 2021 08:15:44 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 08:15:52 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 08:15:55 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 08:15:56 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 08:15:57 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 08:15:58 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 08:15:59 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 08:15:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 08:16:00 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:c7baec6fc76f48bce7341e4ed36b01d548ba0189f534e42f20fa08c907fe9961`  
		Last Modified: Thu, 25 Mar 2021 22:46:29 GMT  
		Size: 2.7 MB (2720368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95a43479f256af47516077cd77761ad6cd5700477be79ea80adc876bfc4755b1`  
		Last Modified: Fri, 26 Mar 2021 08:18:15 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ae474a0d021cea326bee7d13a234f92067fde4ab5bb303964aeac19d3a97f47`  
		Last Modified: Fri, 26 Mar 2021 08:18:25 GMT  
		Size: 46.2 MB (46240944 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f8e9c39d5db46d135a7ef39e9d02fc580a16b124dc132571eda0f1266a4b567`  
		Last Modified: Fri, 26 Mar 2021 08:18:15 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:895e239fcedd3726c9988f1acae38413fcc730cc6c6871340984dc7dc7a5c6c4`  
		Last Modified: Fri, 26 Mar 2021 08:18:15 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.4.7` - linux; 386

```console
$ docker pull vault@sha256:b9734b15de7e34fdfbf36d4ae74737bc6a646c0482a3b7c45e0f0012d948cf86
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50214569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:af3bb1714b76162aae8557cae08feffc09d24d9de656cd8f148f74f43ae78f66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 24 Feb 2021 20:38:57 GMT
ADD file:b5ef4a4abd9ccb894bdda7a5750878d13fbac4746c7b173c5dc88cf4846fc976 in / 
# Wed, 24 Feb 2021 20:38:57 GMT
CMD ["/bin/sh"]
# Sat, 13 Mar 2021 04:21:13 GMT
ARG VAULT_VERSION=1.4.7
# Sat, 13 Mar 2021 04:21:14 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN addgroup vault &&     adduser -S -G vault vault
# Sat, 13 Mar 2021 04:21:19 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Sat, 13 Mar 2021 04:21:20 GMT
# ARGS: VAULT_VERSION=1.4.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Sat, 13 Mar 2021 04:21:21 GMT
VOLUME [/vault/logs]
# Sat, 13 Mar 2021 04:21:21 GMT
VOLUME [/vault/file]
# Sat, 13 Mar 2021 04:21:21 GMT
EXPOSE 8200
# Sat, 13 Mar 2021 04:21:21 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Mar 2021 04:21:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Mar 2021 04:21:22 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:9c18aa22aceabbea5b9c3d26c1e449591c02413fb34b574d9f73520f3fea602b`  
		Last Modified: Wed, 24 Feb 2021 20:39:36 GMT  
		Size: 2.8 MB (2788780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:337893333af33b7612c5297b9225634941437572144978bd22f18d2cb3725b66`  
		Last Modified: Sat, 13 Mar 2021 04:22:42 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4faabe768828e04b61961b8c59ef0ad38c7278efea3d06e24ff88b284e31e9a1`  
		Last Modified: Sat, 13 Mar 2021 04:22:50 GMT  
		Size: 47.4 MB (47422488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a0f265f3ac02602c89f81e9a183afdd5b082e05a7ab47a6e5f0b11834b7146b`  
		Last Modified: Sat, 13 Mar 2021 04:22:42 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb123cff4479d664b63b79d0b6b5f522991288d081474ec8cef3313a77127df4`  
		Last Modified: Sat, 13 Mar 2021 04:22:42 GMT  
		Size: 1.8 KB (1824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.5.7`

```console
$ docker pull vault@sha256:e5952ad3d6dcacb00899b66a88ee927d56cf74f6e90da6057b5d9ef521ba4e85
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.5.7` - linux; amd64

```console
$ docker pull vault@sha256:90f81843d6449824ebc3f69a6337145c62d2d25066856d4fa3d20a819f8aabe2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55009991 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8968f6dc172f97547ec98d8a82de53bbb25c71362e5e3b4e088328ba7065805d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:48 GMT
ADD file:41685950b607fe90e0886c857e4efdafab1e43a09def174a4ea97f8ec624370b in / 
# Thu, 25 Mar 2021 22:19:48 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 05:04:17 GMT
ARG VAULT_VERSION=1.5.7
# Fri, 26 Mar 2021 05:04:18 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 05:04:24 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 05:04:25 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 05:04:25 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 05:04:26 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 05:04:26 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 05:04:26 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 05:04:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 05:04:26 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:c8bc66e2636f8133df434e1bce741b6b7fb21515e7c8a554a805b73f5fdae2de`  
		Last Modified: Thu, 25 Mar 2021 22:20:57 GMT  
		Size: 2.8 MB (2797179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33fd36bf290dbeb2f64ce41780423d3530d00e5aa3337b545e5be3d52a3bf7f`  
		Last Modified: Fri, 26 Mar 2021 05:06:21 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:604044eae043c2d599c3f06d97fdc7cf15e332bddb95a175f922716cb652a186`  
		Last Modified: Fri, 26 Mar 2021 05:06:30 GMT  
		Size: 52.2 MB (52209515 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2bfa123b5cb9b8cd356acd7fee7a8d082beae1567ab06505be83708d6ee1c444`  
		Last Modified: Fri, 26 Mar 2021 05:06:21 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1089c5632db335189e5a662717d29f38293ac08eab3a4df6057de2c9b82c05e9`  
		Last Modified: Fri, 26 Mar 2021 05:06:21 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.5.7` - linux; arm variant v6

```console
$ docker pull vault@sha256:29e18e929a36011901973283bd4fb7c0723fa8605f3ce60c99f6089134821831
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51563428 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ebecacf8c1f7878517a0bdfc9b313dd3efcd661daaedcf07817766e44f70b20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 24 Feb 2021 20:50:55 GMT
ADD file:9e81f449863b2d114afc239efa445f3bed6ff45b123ea3aad271a5631ac4fa13 in / 
# Wed, 24 Feb 2021 20:50:56 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 23:37:28 GMT
ARG VAULT_VERSION=1.5.7
# Wed, 24 Feb 2021 23:37:29 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 24 Feb 2021 23:37:39 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 24 Feb 2021 23:37:42 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 24 Feb 2021 23:37:43 GMT
VOLUME [/vault/logs]
# Wed, 24 Feb 2021 23:37:45 GMT
VOLUME [/vault/file]
# Wed, 24 Feb 2021 23:37:47 GMT
EXPOSE 8200
# Wed, 24 Feb 2021 23:37:48 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 23:37:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 23:37:50 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:615b6501bf7ed56706d638bf075665f504b2fee0bdebf905dcb8610bc9271fa4`  
		Last Modified: Wed, 24 Feb 2021 20:51:33 GMT  
		Size: 2.6 MB (2574559 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:427a2d6e45231426c91f9a0a1944ac81ffce942376ba018cf400b75504c49268`  
		Last Modified: Wed, 24 Feb 2021 23:39:00 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:045524ab01e984686b84e13032ffbe082a603d939306b8d85c959d0f51952e27`  
		Last Modified: Wed, 24 Feb 2021 23:39:14 GMT  
		Size: 49.0 MB (48985575 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6aa1c5eae8a4aebc90bd1d179561f8b161f59f5c282b09c484816f4484fa381`  
		Last Modified: Wed, 24 Feb 2021 23:39:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b78833d0facb3234c90ed9bfe36fd6249bfe5f6f4523b017380487df1a390c0b`  
		Last Modified: Wed, 24 Feb 2021 23:39:00 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.5.7` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:a95ddb80eb8d0c528b68974f538dc308daf195868b57ecaba9975d636de4949a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51917984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb5afa9dc4e2053dbc36a399c95c55408b70ee67c61e9d8d2a2a8fc135ab810d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:42:23 GMT
ADD file:a65de3d22c60aa364e967325d628757aa1f842fbefa48420403da87f91e9b7fd in / 
# Thu, 25 Mar 2021 22:42:41 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:15:13 GMT
ARG VAULT_VERSION=1.5.7
# Fri, 26 Mar 2021 08:15:16 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 08:15:25 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 08:15:28 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 08:15:29 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 08:15:30 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 08:15:31 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 08:15:32 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 08:15:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 08:15:34 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:c7baec6fc76f48bce7341e4ed36b01d548ba0189f534e42f20fa08c907fe9961`  
		Last Modified: Thu, 25 Mar 2021 22:46:29 GMT  
		Size: 2.7 MB (2720368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9e0a85d4ff4095a26e8bc5aecdcf86033817a2419927df41e869eb3cee1e384`  
		Last Modified: Fri, 26 Mar 2021 08:17:57 GMT  
		Size: 1.3 KB (1286 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc46f6ebf437349f70be56b14aade2473e49e4ff664b83ed9d21d25549fbd569`  
		Last Modified: Fri, 26 Mar 2021 08:18:08 GMT  
		Size: 49.2 MB (49194320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24e1ea1af4f2afe8c0e2ff20a247ae1c2da0eae1904afe755185b87a5c6c4298`  
		Last Modified: Fri, 26 Mar 2021 08:17:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d247919a344e41e07c2ec2ef609bb3331181db07e7ce9dedaf0583c0516f9b43`  
		Last Modified: Fri, 26 Mar 2021 08:17:58 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.5.7` - linux; 386

```console
$ docker pull vault@sha256:46ec7cff4a3647c7ed489046f426ebb024642a65b2b488dd6bb135af2406311a
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53087311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8bad025aee0d1bd6e8b224dc8e9bbd13d122bc9d524335dac1b2fca064f5677c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 24 Feb 2021 20:38:57 GMT
ADD file:b5ef4a4abd9ccb894bdda7a5750878d13fbac4746c7b173c5dc88cf4846fc976 in / 
# Wed, 24 Feb 2021 20:38:57 GMT
CMD ["/bin/sh"]
# Sat, 13 Mar 2021 04:20:56 GMT
ARG VAULT_VERSION=1.5.7
# Sat, 13 Mar 2021 04:20:57 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN addgroup vault &&     adduser -S -G vault vault
# Sat, 13 Mar 2021 04:21:05 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Sat, 13 Mar 2021 04:21:06 GMT
# ARGS: VAULT_VERSION=1.5.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Sat, 13 Mar 2021 04:21:06 GMT
VOLUME [/vault/logs]
# Sat, 13 Mar 2021 04:21:06 GMT
VOLUME [/vault/file]
# Sat, 13 Mar 2021 04:21:07 GMT
EXPOSE 8200
# Sat, 13 Mar 2021 04:21:07 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Mar 2021 04:21:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Mar 2021 04:21:07 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:9c18aa22aceabbea5b9c3d26c1e449591c02413fb34b574d9f73520f3fea602b`  
		Last Modified: Wed, 24 Feb 2021 20:39:36 GMT  
		Size: 2.8 MB (2788780 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:559f9e16e7b8a03f75f8d44cea6686c77a35f318e8500965d38b07e88147859c`  
		Last Modified: Sat, 13 Mar 2021 04:22:25 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10f80a6539f1ecb5411831cd6d6c8e76943562b479d9bec0c0b0cbeab429b370`  
		Last Modified: Sat, 13 Mar 2021 04:22:33 GMT  
		Size: 50.3 MB (50295231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d435c9d37a5cf8cbd51d97d0ef73326f25172f8e04116c7cb74fb449ada6f728`  
		Last Modified: Sat, 13 Mar 2021 04:22:25 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5e2db9573d3e2d3a763721a2b69e3eeac4c1954fab91290b331175bbf1a4ae3`  
		Last Modified: Sat, 13 Mar 2021 04:22:25 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.6.3`

```console
$ docker pull vault@sha256:6cc190a30b54c278cf475f711e6db566fbaa81194e0fe74dddbb855cc4d8677b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.6.3` - linux; amd64

```console
$ docker pull vault@sha256:c3b98bbd8e571bd76e97f692d90143d949251fbb95a6160a1c2344f5e0560cc9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (68982834 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7363ef5cdf1e5d2c2ce8c20a274dcfb37c91bce0ba6f6370e30b1b097ab8b224`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:32 GMT
ADD file:6b081cabb4b256ee07587d249c4989b5b679375529542b81550a65b6f19f274e in / 
# Thu, 25 Mar 2021 22:19:32 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 05:04:01 GMT
ARG VAULT_VERSION=1.6.3
# Fri, 26 Mar 2021 05:04:03 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 05:04:11 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 05:04:12 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 05:04:12 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 05:04:13 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 05:04:13 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 05:04:13 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 05:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 05:04:14 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:9aae54b2144e5b2b00c610f8805128f4f86822e1e52d3714c463744a431f0f4a`  
		Last Modified: Thu, 25 Mar 2021 22:20:18 GMT  
		Size: 2.8 MB (2811681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a434ea0ba104f607ea9e907135e6d9864d4607d7fccdacb450799d2c28926918`  
		Last Modified: Fri, 26 Mar 2021 05:05:57 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:680018afd3e10264426e015a9df3efb577e55a7f34471e3e5eb600497d844c88`  
		Last Modified: Fri, 26 Mar 2021 05:06:09 GMT  
		Size: 66.2 MB (66167888 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba35ea1e81e0aa2b819506fba7d623924a50f9017c2bd6842c6be4f03f61825`  
		Last Modified: Fri, 26 Mar 2021 05:05:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:780a58f777556d5839094a1fcdb8a6c187b632455943fc301acbdab08e177c28`  
		Last Modified: Fri, 26 Mar 2021 05:05:57 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.6.3` - linux; arm variant v6

```console
$ docker pull vault@sha256:c259ca51167c63aa9607d919b2c55db9eb7b7a78f71e451da595a562e7481760
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.7 MB (63718893 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b12efd0b4318752f6ee120b58288113977130db7a2d1859621b3130c6c5e1c96`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Tue, 02 Mar 2021 23:14:53 GMT
ARG VAULT_VERSION=1.6.3
# Tue, 02 Mar 2021 23:14:54 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 02 Mar 2021 23:15:06 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 02 Mar 2021 23:15:09 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 02 Mar 2021 23:15:10 GMT
VOLUME [/vault/logs]
# Tue, 02 Mar 2021 23:15:11 GMT
VOLUME [/vault/file]
# Tue, 02 Mar 2021 23:15:12 GMT
EXPOSE 8200
# Tue, 02 Mar 2021 23:15:12 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 02 Mar 2021 23:15:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Mar 2021 23:15:14 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:565cbb62e6435fa12e134fa98dd06c89e72cb48235f763bc4d730d144cc7a1f8`  
		Last Modified: Tue, 02 Mar 2021 23:15:36 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:284162887dd90cdadae098858307a49f9d62bdd19a07dd1c13918486d4713703`  
		Last Modified: Tue, 02 Mar 2021 23:15:52 GMT  
		Size: 61.1 MB (61093587 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b4c9ad70bb6e855693e16c1a7108c23673a58ff4897b17b3b19282ec14ed02`  
		Last Modified: Tue, 02 Mar 2021 23:15:36 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51322c75e1e50cf02683375fbc23aa2288d8dd6af7d4a84029a7c142f4749ad5`  
		Last Modified: Tue, 02 Mar 2021 23:15:36 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.6.3` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:2a3fcd4e44aa5291ed10b2535e9d13e04875f025154d6f086a8c8eef940a2f03
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (65016293 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8209178a8a480af25fec96281f3f0b640654a477048db02d9b78aebda10fb20e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:40:10 GMT
ADD file:8d7431f7e3e42b162a1626e7abf4ef7605146671dccc753d490de6b7fe429261 in / 
# Thu, 25 Mar 2021 22:40:23 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:14:46 GMT
ARG VAULT_VERSION=1.6.3
# Fri, 26 Mar 2021 08:14:48 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 08:14:57 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 08:15:01 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 08:15:02 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 08:15:02 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 08:15:03 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 08:15:04 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 08:15:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 08:15:06 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:5ceb5101e3b0d54efb5f18318982508a04b181b4d5ae52b096dd35dea3a006cc`  
		Last Modified: Thu, 25 Mar 2021 22:44:41 GMT  
		Size: 2.7 MB (2711898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00b2f8b128aa711c1ad9c2d3b773b7b6f8d48d41ef140e2eeedea8c88b47b3ca`  
		Last Modified: Fri, 26 Mar 2021 08:17:37 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6492bdc2fc593fa06a5274d2109adadc62453a6585e29b876ff28786e7238f9`  
		Last Modified: Fri, 26 Mar 2021 08:17:51 GMT  
		Size: 62.3 MB (62301127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d803c1830a0df4de0f473e700c19f5ad71456dcc4561a33f10e97f47448a7466`  
		Last Modified: Fri, 26 Mar 2021 08:17:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2652120b47a31370fe540e0b4795336e64d41651f48ed34a6747f40c9d43bbd5`  
		Last Modified: Fri, 26 Mar 2021 08:17:37 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.6.3` - linux; 386

```console
$ docker pull vault@sha256:c88f2267f674e946cda289fe4ca74e08b020df367d5794079ddb5697993507ef
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.0 MB (67033174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eb4690e8d201f8da8e9156bc6aaddd0fd70be06fbc0e104f51f449199ec53f7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Sat, 13 Mar 2021 04:20:39 GMT
ARG VAULT_VERSION=1.6.3
# Sat, 13 Mar 2021 04:20:39 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN addgroup vault &&     adduser -S -G vault vault
# Sat, 13 Mar 2021 04:20:47 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Sat, 13 Mar 2021 04:20:48 GMT
# ARGS: VAULT_VERSION=1.6.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Sat, 13 Mar 2021 04:20:48 GMT
VOLUME [/vault/logs]
# Sat, 13 Mar 2021 04:20:49 GMT
VOLUME [/vault/file]
# Sat, 13 Mar 2021 04:20:49 GMT
EXPOSE 8200
# Sat, 13 Mar 2021 04:20:49 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Mar 2021 04:20:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Mar 2021 04:20:49 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e4e2efb828c20a20c7e10f0e0d5ad91c51d9d287e583c699ea0f71c618ad24c`  
		Last Modified: Sat, 13 Mar 2021 04:22:02 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ede3b452c48602c7f834022bf8eb76e66acb650c25659a3a2502346ffa46af6`  
		Last Modified: Sat, 13 Mar 2021 04:22:12 GMT  
		Size: 64.2 MB (64211731 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb4bcc937a3d8ed95c0cfac11c12b349557d4d0b78e6bb5f26c116549971c58`  
		Last Modified: Sat, 13 Mar 2021 04:22:02 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23fcb17f032c6add01d605cca0b8b53a075bafff6cd254c40eca88402865fc4`  
		Last Modified: Sat, 13 Mar 2021 04:22:02 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.7.0`

```console
$ docker pull vault@sha256:636539e5ab2dd0942061faeb232452774103a25e82bca969cb37945616aeae53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.7.0` - linux; amd64

```console
$ docker pull vault@sha256:d51a9c82d0d45857acabea988c7b2ec673855438a7718138569d199e80db2ad3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72706694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b359df68a663cd5d2528caab398298a176375aeaa13ae199d8b5f615c2a38bce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:32 GMT
ADD file:6b081cabb4b256ee07587d249c4989b5b679375529542b81550a65b6f19f274e in / 
# Thu, 25 Mar 2021 22:19:32 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 05:02:55 GMT
ARG VAULT_VERSION=1.7.0
# Fri, 26 Mar 2021 05:02:56 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 05:03:07 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 05:03:09 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 05:03:09 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 05:03:09 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 05:03:10 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 05:03:10 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 05:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 05:03:11 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:9aae54b2144e5b2b00c610f8805128f4f86822e1e52d3714c463744a431f0f4a`  
		Last Modified: Thu, 25 Mar 2021 22:20:18 GMT  
		Size: 2.8 MB (2811681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1d6dd05beb921063752a0e4b43d2dc08582069eaaeb4e32ffa7a370ede3515`  
		Last Modified: Fri, 26 Mar 2021 05:04:52 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4de46febc3613de2118ec655d1fffbe87968c11570858a476e7dc4fd74c6ff4`  
		Last Modified: Fri, 26 Mar 2021 05:05:03 GMT  
		Size: 69.9 MB (69891751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc279c1e752b4ac2f1af5f2c54603b7bbf0e712414a1383d79b2c684b895ff4`  
		Last Modified: Fri, 26 Mar 2021 05:04:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e437bfd1f45e31c4442a7038debd89139a36421ac53cf2e579c1f773a45432ea`  
		Last Modified: Fri, 26 Mar 2021 05:04:52 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0` - linux; arm variant v6

```console
$ docker pull vault@sha256:dfe5c6742e2c313a574f34a2e4fd5ea5e60ca2633498e74cb6cf9577dd4d7e6c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66726546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc64e5a7e7875e54681c1a1766c6d5672947c5023851f4866771bd752b0f94a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 01:03:46 GMT
ARG VAULT_VERSION=1.7.0
# Thu, 25 Mar 2021 01:03:51 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 25 Mar 2021 01:04:06 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 25 Mar 2021 01:04:10 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 25 Mar 2021 01:04:11 GMT
VOLUME [/vault/logs]
# Thu, 25 Mar 2021 01:04:13 GMT
VOLUME [/vault/file]
# Thu, 25 Mar 2021 01:04:13 GMT
EXPOSE 8200
# Thu, 25 Mar 2021 01:04:14 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 25 Mar 2021 01:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Mar 2021 01:04:16 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7303dbc8fff63055f01b5e582ca32737dc8a80653e1f42e05799670f9aed479`  
		Last Modified: Thu, 25 Mar 2021 01:05:27 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624bbd3dfaaf5a4bfd1713635f9c6337c972967fc53cd2da82046cccfa6db258`  
		Last Modified: Thu, 25 Mar 2021 01:05:44 GMT  
		Size: 64.1 MB (64101238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2f5fb2239acd5f8ee0da5bded2d3f842e8f8d51dc7ed835a469f1adb16cd3a`  
		Last Modified: Thu, 25 Mar 2021 01:05:27 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d198e7656fbdcaf409b9974f399ff8ab9abc75372b406403a538645b884240`  
		Last Modified: Thu, 25 Mar 2021 01:05:28 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:7bb03087f1872bba59add852953ac3e35a54d63798a5a42d53cc147d335150d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68535695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7c6e9941803130f0b68e0749e872a59bd13cd4c57b0aae51a46a532a37a3d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:40:10 GMT
ADD file:8d7431f7e3e42b162a1626e7abf4ef7605146671dccc753d490de6b7fe429261 in / 
# Thu, 25 Mar 2021 22:40:23 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:13:10 GMT
ARG VAULT_VERSION=1.7.0
# Fri, 26 Mar 2021 08:13:13 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 08:13:22 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 08:13:25 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 08:13:27 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 08:13:28 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 08:13:30 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 08:13:31 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 08:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 08:13:33 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:5ceb5101e3b0d54efb5f18318982508a04b181b4d5ae52b096dd35dea3a006cc`  
		Last Modified: Thu, 25 Mar 2021 22:44:41 GMT  
		Size: 2.7 MB (2711898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532760a713fdcc47b0750cf149032179ac109897d27a4a7387254e873782ef5a`  
		Last Modified: Fri, 26 Mar 2021 08:16:21 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da9e5d008656a72a376d31d7c1cf4c750c1d20fdc9725470e92748f3d902aeb`  
		Last Modified: Fri, 26 Mar 2021 08:16:38 GMT  
		Size: 65.8 MB (65820533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6121bcad7cba7d37518917de5d2e4bb729cc62708b2c847ea1df48ccb757483f`  
		Last Modified: Fri, 26 Mar 2021 08:16:21 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8253019ed837881d065d263f197f95708f7073be3629b60a1e367d07f44a853c`  
		Last Modified: Fri, 26 Mar 2021 08:16:21 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0` - linux; 386

```console
$ docker pull vault@sha256:9ca9c858c4c5fc19f6527c3a238cbdea0fa9c40201aa6dacb74ac8ecb44178c4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70570068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6444ddc13b71ba29ad4262acb8347705e3186bce68856b0002722465f8fe8502`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 00:53:26 GMT
ARG VAULT_VERSION=1.7.0
# Thu, 25 Mar 2021 00:53:27 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 25 Mar 2021 00:53:35 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 25 Mar 2021 00:53:36 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 25 Mar 2021 00:53:37 GMT
VOLUME [/vault/logs]
# Thu, 25 Mar 2021 00:53:37 GMT
VOLUME [/vault/file]
# Thu, 25 Mar 2021 00:53:37 GMT
EXPOSE 8200
# Thu, 25 Mar 2021 00:53:37 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 25 Mar 2021 00:53:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Mar 2021 00:53:38 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca768045b18d821bd7431ec5078619ab1ef0c99fb0ff614bfdaaa9665278029`  
		Last Modified: Thu, 25 Mar 2021 00:54:32 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499c2c4856c3e0862f29ef4729b42c6eb0a5afde44966cd810da36db6716fc6e`  
		Last Modified: Thu, 25 Mar 2021 00:54:42 GMT  
		Size: 67.7 MB (67748633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a0103fd85fb669bfde787d1f69ca52754be530ed43599423687363e29e1948`  
		Last Modified: Thu, 25 Mar 2021 00:54:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17cea17112d0c6e8d055ddd4d3c66dca71c604283ca12327457059b643ef5d60`  
		Last Modified: Thu, 25 Mar 2021 00:54:32 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.7.0-rc1`

```console
$ docker pull vault@sha256:aad6539afa0787fe58a268b4fb678cfb26e77eec326da6a5c19b81baebf9d4fa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.7.0-rc1` - linux; amd64

```console
$ docker pull vault@sha256:279bedc3775cd2d4709344d09844d0a3b69cc6e75da0998b3e6d6f270d9af04f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72670615 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9f48d30eaee4d3e3433a177470c5b2a76bb57ea1d631902ed4eec8b148726ecf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:32 GMT
ADD file:6b081cabb4b256ee07587d249c4989b5b679375529542b81550a65b6f19f274e in / 
# Thu, 25 Mar 2021 22:19:32 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 05:03:39 GMT
ARG VAULT_VERSION=1.7.0-rc1
# Fri, 26 Mar 2021 05:03:41 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 05:03:52 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 05:03:54 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 05:03:54 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 05:03:54 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 05:03:55 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 05:03:55 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 05:03:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 05:03:56 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:9aae54b2144e5b2b00c610f8805128f4f86822e1e52d3714c463744a431f0f4a`  
		Last Modified: Thu, 25 Mar 2021 22:20:18 GMT  
		Size: 2.8 MB (2811681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd5e3fad7b25f9966da1ed73b673927d38f8639b801dd42c45cd14122dc8faaf`  
		Last Modified: Fri, 26 Mar 2021 05:05:38 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca21ae151d70a79ac49ede65588f342677fd343ab77bf83d659e0d30a59d4af`  
		Last Modified: Fri, 26 Mar 2021 05:05:48 GMT  
		Size: 69.9 MB (69855668 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bea0c58469c7ca8e3f98ee85522201f1786a5b09352fd41027b88329c95506e`  
		Last Modified: Fri, 26 Mar 2021 05:05:38 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7bedbd52da6757129511a9fc2fcc52c881cfb3e39e13616c02869f48f2821052`  
		Last Modified: Fri, 26 Mar 2021 05:05:38 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0-rc1` - linux; arm variant v6

```console
$ docker pull vault@sha256:3774e40967516f02b0e1e95c0d6d5b2a0f5d2c1fc1b1444d925b9324ef08c5d1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66701202 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a076fb7281763a43289d7998affb280220ace610d2111bd206b4cffd71dddf0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Fri, 12 Mar 2021 21:06:53 GMT
ARG VAULT_VERSION=1.7.0-rc1
# Fri, 12 Mar 2021 21:06:55 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 12 Mar 2021 21:07:07 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 12 Mar 2021 21:07:10 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 12 Mar 2021 21:07:11 GMT
VOLUME [/vault/logs]
# Fri, 12 Mar 2021 21:07:11 GMT
VOLUME [/vault/file]
# Fri, 12 Mar 2021 21:07:12 GMT
EXPOSE 8200
# Fri, 12 Mar 2021 21:07:13 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Mar 2021 21:07:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Mar 2021 21:07:14 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da71943561a84c5a71b50584dce69c1fa92edeb892379413a3ca6aee79713b9f`  
		Last Modified: Fri, 12 Mar 2021 21:07:42 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fd520100b4e569f3cc80cfa37639845a4acc36da813548a31e3d7e49b1f4a5d`  
		Last Modified: Fri, 12 Mar 2021 21:08:00 GMT  
		Size: 64.1 MB (64075893 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7976f00f5bc42016b9f92eb0d013b94a23414c0d0c735630b236efe68d961e`  
		Last Modified: Fri, 12 Mar 2021 21:07:42 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4fd12f56f70b0f61bc421d11e7f15e4ae533e2783e397cca3dd0c1d60a1371e`  
		Last Modified: Fri, 12 Mar 2021 21:07:42 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0-rc1` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:3ecb0f69c8be43b1e09bc5121bbf470c180089ef5935d09e1112a2ced5713dd5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68500286 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a67ba1b71e53fe2f51a5998d18f9fdab955afc5c221c9f32df56a03d7b9e325`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:40:10 GMT
ADD file:8d7431f7e3e42b162a1626e7abf4ef7605146671dccc753d490de6b7fe429261 in / 
# Thu, 25 Mar 2021 22:40:23 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:14:14 GMT
ARG VAULT_VERSION=1.7.0-rc1
# Fri, 26 Mar 2021 08:14:17 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 08:14:26 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 08:14:29 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 08:14:30 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 08:14:31 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 08:14:32 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 08:14:33 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 08:14:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 08:14:35 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:5ceb5101e3b0d54efb5f18318982508a04b181b4d5ae52b096dd35dea3a006cc`  
		Last Modified: Thu, 25 Mar 2021 22:44:41 GMT  
		Size: 2.7 MB (2711898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8187b8e1d03228a2752f63c7e39eba5d389ec3dd2c52cc7824506210e0dc4ad4`  
		Last Modified: Fri, 26 Mar 2021 08:17:09 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:913d028ecb1aefdeb268ebcdc3a78e7e53a3a71461d068c75fcaf1b1f869426d`  
		Last Modified: Fri, 26 Mar 2021 08:17:25 GMT  
		Size: 65.8 MB (65785125 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb2dbe9b4063b6e8925a0a3d387f5c4bbf9a0c2c6942c2efd766c02358e876b5`  
		Last Modified: Fri, 26 Mar 2021 08:17:09 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb9c0c8956878f4eeee1251253694692a6430b23c001e471423e9b19096ce925`  
		Last Modified: Fri, 26 Mar 2021 08:17:09 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0-rc1` - linux; 386

```console
$ docker pull vault@sha256:33d8485e41ee4bc1644a2594a96629156686db055178a5a8cf725f557e3b20fe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70535213 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:97b9d341d2c791e479ceae1b24a791fe4f60a658fd97d8df9b70abad4bd8b2f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Sat, 13 Mar 2021 04:20:22 GMT
ARG VAULT_VERSION=1.7.0-rc1
# Sat, 13 Mar 2021 04:20:23 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN addgroup vault &&     adduser -S -G vault vault
# Sat, 13 Mar 2021 04:20:31 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Sat, 13 Mar 2021 04:20:32 GMT
# ARGS: VAULT_VERSION=1.7.0-rc1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Sat, 13 Mar 2021 04:20:33 GMT
VOLUME [/vault/logs]
# Sat, 13 Mar 2021 04:20:33 GMT
VOLUME [/vault/file]
# Sat, 13 Mar 2021 04:20:33 GMT
EXPOSE 8200
# Sat, 13 Mar 2021 04:20:33 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Mar 2021 04:20:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Mar 2021 04:20:34 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ec077617e334124628bc315a2fac18f3a58ea03e5b9a27f0c5b4b47d12ff901`  
		Last Modified: Sat, 13 Mar 2021 04:21:41 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a971e165b52bc71c746279bbbb38b15b3d7719f28c73fc1e73085ff029adf55`  
		Last Modified: Sat, 13 Mar 2021 04:21:53 GMT  
		Size: 67.7 MB (67713774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a9d35fbfd3611ce6411fa0ddcf21074c6cb74465db84181af0251e7ce3d9f21`  
		Last Modified: Sat, 13 Mar 2021 04:21:41 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5adcd7a014010274a71e984d64d721e11fb533558cde40d9daa5c0eb38d98f85`  
		Last Modified: Sat, 13 Mar 2021 04:21:41 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.7.0-rc2`

```console
$ docker pull vault@sha256:c99af81ddac094146e847678da3e195a07b1f86d56a6dea03f6cfb3106c8b139
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.7.0-rc2` - linux; amd64

```console
$ docker pull vault@sha256:b9006897b7a05a94a21424934c0702a8901cae52e0af754d34d1984fba0a6eaf
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72667408 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30252bbbc5eb3dd58af3b61067ac619c6820fece03d58d504be2d730f15bf35e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:32 GMT
ADD file:6b081cabb4b256ee07587d249c4989b5b679375529542b81550a65b6f19f274e in / 
# Thu, 25 Mar 2021 22:19:32 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 05:03:17 GMT
ARG VAULT_VERSION=1.7.0-rc2
# Fri, 26 Mar 2021 05:03:18 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 05:03:29 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 05:03:31 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 05:03:31 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 05:03:32 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 05:03:32 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 05:03:33 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 05:03:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 05:03:33 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:9aae54b2144e5b2b00c610f8805128f4f86822e1e52d3714c463744a431f0f4a`  
		Last Modified: Thu, 25 Mar 2021 22:20:18 GMT  
		Size: 2.8 MB (2811681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe5e3f6abe5a49305d2ca8342d4f34c71ffccbeb1f742401d25eb87182074b65`  
		Last Modified: Fri, 26 Mar 2021 05:05:17 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a824ecbb1efa7047912500b38d4d7b1db6f8efadd38723d1cef3033b6aed75`  
		Last Modified: Fri, 26 Mar 2021 05:05:26 GMT  
		Size: 69.9 MB (69852460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a1358f7df2c9c0eabf8f36b00315469ccf0025d8b2f6e635bf81dc8699b2721`  
		Last Modified: Fri, 26 Mar 2021 05:05:16 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7c683d5c63b7dfb69908ada4e5f7ac73c5c2b785aec61a75155a96383f348e4`  
		Last Modified: Fri, 26 Mar 2021 05:05:16 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0-rc2` - linux; arm variant v6

```console
$ docker pull vault@sha256:65909fe86ba946055904874fe4967fc7ad32c5ceb72e45d98ec8d1963ceb99bc
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66702732 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd98d68386fc5cd7a1dc18a79ac6d21b9d53e625fc82afdca06b2002a4dcf029`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 01:04:27 GMT
ARG VAULT_VERSION=1.7.0-rc2
# Thu, 25 Mar 2021 01:04:30 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 25 Mar 2021 01:04:43 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 25 Mar 2021 01:04:47 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 25 Mar 2021 01:04:48 GMT
VOLUME [/vault/logs]
# Thu, 25 Mar 2021 01:04:48 GMT
VOLUME [/vault/file]
# Thu, 25 Mar 2021 01:04:49 GMT
EXPOSE 8200
# Thu, 25 Mar 2021 01:04:50 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 25 Mar 2021 01:04:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Mar 2021 01:04:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:492de643f384b13d0d27e4c36fd34aaa53ae61f764df758975db2c53d7dcff02`  
		Last Modified: Thu, 25 Mar 2021 01:05:51 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:872ca995f4e82e5b83e9ad8f2b1a147ff9c2cfe1ec1aa0ebfce5b6f940eb5d03`  
		Last Modified: Thu, 25 Mar 2021 01:06:08 GMT  
		Size: 64.1 MB (64077425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5bf52c3959a3b0bf591b2f43c6e88cd693379f8dcc36e6537b3bbaf205f366c1`  
		Last Modified: Thu, 25 Mar 2021 01:05:51 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022a4592a597726a7eed358f790ed8ce4f46411265567bbe18958c296487679c`  
		Last Modified: Thu, 25 Mar 2021 01:05:51 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0-rc2` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:2dd9c1fe2c8d4c61e60fdfc8f99662ff80ed0f463fa7e9585f5db5989f6feaaa
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68525636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7bf9bf2c8461fa4ce891e6c0d771fa43e57d1b18882a7ce6130fc2eef41cab5c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:40:10 GMT
ADD file:8d7431f7e3e42b162a1626e7abf4ef7605146671dccc753d490de6b7fe429261 in / 
# Thu, 25 Mar 2021 22:40:23 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:13:44 GMT
ARG VAULT_VERSION=1.7.0-rc2
# Fri, 26 Mar 2021 08:13:46 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 08:13:56 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 08:13:59 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 08:14:00 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 08:14:01 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 08:14:02 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 08:14:03 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 08:14:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 08:14:05 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:5ceb5101e3b0d54efb5f18318982508a04b181b4d5ae52b096dd35dea3a006cc`  
		Last Modified: Thu, 25 Mar 2021 22:44:41 GMT  
		Size: 2.7 MB (2711898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47962abfdb64002920dc8fcf30ff78d74e29162dbd11fa9003eb42ac60c01461`  
		Last Modified: Fri, 26 Mar 2021 08:16:49 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ae5c56a9776e27efd2361547ee2322fd9c05596ca0845adab426969178dbad`  
		Last Modified: Fri, 26 Mar 2021 08:17:03 GMT  
		Size: 65.8 MB (65810476 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a3d054dda0f8af57d9f3330c5d563744ace79e88eb2e0ad2a8cb3a7da88d283`  
		Last Modified: Fri, 26 Mar 2021 08:16:48 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:767177bd639431f5c83efdfb16fdddf5ec1ec42260a8bd807d2f61a4983d8083`  
		Last Modified: Fri, 26 Mar 2021 08:16:48 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.0-rc2` - linux; 386

```console
$ docker pull vault@sha256:33ec9e94f6d0ddb6552e379934ca19b367b71b098fc281ecb70b5f33892a81ce
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70539647 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0451f5c6cc6397c5d19de1b78df1eae8cf143d4b31c3598728d46da51ef762b3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 00:53:43 GMT
ARG VAULT_VERSION=1.7.0-rc2
# Thu, 25 Mar 2021 00:53:44 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 25 Mar 2021 00:53:51 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 25 Mar 2021 00:53:52 GMT
# ARGS: VAULT_VERSION=1.7.0-rc2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 25 Mar 2021 00:53:52 GMT
VOLUME [/vault/logs]
# Thu, 25 Mar 2021 00:53:53 GMT
VOLUME [/vault/file]
# Thu, 25 Mar 2021 00:53:53 GMT
EXPOSE 8200
# Thu, 25 Mar 2021 00:53:53 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 25 Mar 2021 00:53:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Mar 2021 00:53:54 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:022eee5ce6d9086fdc32a097061ec34360ea2738acf90e78140b0ac58595bb1a`  
		Last Modified: Thu, 25 Mar 2021 00:54:54 GMT  
		Size: 1.3 KB (1254 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a201d0819858faaaabb6e02b2f17d7e014e2369938e0c7b5b695b7db22b8865`  
		Last Modified: Thu, 25 Mar 2021 00:55:04 GMT  
		Size: 67.7 MB (67718206 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f469fa9313f1206913d043e96d3774d2527a418fbc44fe789ae0445e62da508`  
		Last Modified: Thu, 25 Mar 2021 00:54:54 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ad3341af8f9a4b7c61660aa5fa84c98074b368187b6cfe887dfc3489a042939e`  
		Last Modified: Thu, 25 Mar 2021 00:54:54 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:latest`

```console
$ docker pull vault@sha256:636539e5ab2dd0942061faeb232452774103a25e82bca969cb37945616aeae53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:d51a9c82d0d45857acabea988c7b2ec673855438a7718138569d199e80db2ad3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72706694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b359df68a663cd5d2528caab398298a176375aeaa13ae199d8b5f615c2a38bce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:32 GMT
ADD file:6b081cabb4b256ee07587d249c4989b5b679375529542b81550a65b6f19f274e in / 
# Thu, 25 Mar 2021 22:19:32 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 05:02:55 GMT
ARG VAULT_VERSION=1.7.0
# Fri, 26 Mar 2021 05:02:56 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 05:03:07 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 05:03:09 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 05:03:09 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 05:03:09 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 05:03:10 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 05:03:10 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 05:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 05:03:11 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:9aae54b2144e5b2b00c610f8805128f4f86822e1e52d3714c463744a431f0f4a`  
		Last Modified: Thu, 25 Mar 2021 22:20:18 GMT  
		Size: 2.8 MB (2811681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1d6dd05beb921063752a0e4b43d2dc08582069eaaeb4e32ffa7a370ede3515`  
		Last Modified: Fri, 26 Mar 2021 05:04:52 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4de46febc3613de2118ec655d1fffbe87968c11570858a476e7dc4fd74c6ff4`  
		Last Modified: Fri, 26 Mar 2021 05:05:03 GMT  
		Size: 69.9 MB (69891751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc279c1e752b4ac2f1af5f2c54603b7bbf0e712414a1383d79b2c684b895ff4`  
		Last Modified: Fri, 26 Mar 2021 05:04:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e437bfd1f45e31c4442a7038debd89139a36421ac53cf2e579c1f773a45432ea`  
		Last Modified: Fri, 26 Mar 2021 05:04:52 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:dfe5c6742e2c313a574f34a2e4fd5ea5e60ca2633498e74cb6cf9577dd4d7e6c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66726546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc64e5a7e7875e54681c1a1766c6d5672947c5023851f4866771bd752b0f94a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 01:03:46 GMT
ARG VAULT_VERSION=1.7.0
# Thu, 25 Mar 2021 01:03:51 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 25 Mar 2021 01:04:06 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 25 Mar 2021 01:04:10 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 25 Mar 2021 01:04:11 GMT
VOLUME [/vault/logs]
# Thu, 25 Mar 2021 01:04:13 GMT
VOLUME [/vault/file]
# Thu, 25 Mar 2021 01:04:13 GMT
EXPOSE 8200
# Thu, 25 Mar 2021 01:04:14 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 25 Mar 2021 01:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Mar 2021 01:04:16 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7303dbc8fff63055f01b5e582ca32737dc8a80653e1f42e05799670f9aed479`  
		Last Modified: Thu, 25 Mar 2021 01:05:27 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624bbd3dfaaf5a4bfd1713635f9c6337c972967fc53cd2da82046cccfa6db258`  
		Last Modified: Thu, 25 Mar 2021 01:05:44 GMT  
		Size: 64.1 MB (64101238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2f5fb2239acd5f8ee0da5bded2d3f842e8f8d51dc7ed835a469f1adb16cd3a`  
		Last Modified: Thu, 25 Mar 2021 01:05:27 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d198e7656fbdcaf409b9974f399ff8ab9abc75372b406403a538645b884240`  
		Last Modified: Thu, 25 Mar 2021 01:05:28 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:7bb03087f1872bba59add852953ac3e35a54d63798a5a42d53cc147d335150d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68535695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7c6e9941803130f0b68e0749e872a59bd13cd4c57b0aae51a46a532a37a3d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:40:10 GMT
ADD file:8d7431f7e3e42b162a1626e7abf4ef7605146671dccc753d490de6b7fe429261 in / 
# Thu, 25 Mar 2021 22:40:23 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:13:10 GMT
ARG VAULT_VERSION=1.7.0
# Fri, 26 Mar 2021 08:13:13 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 08:13:22 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 08:13:25 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 08:13:27 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 08:13:28 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 08:13:30 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 08:13:31 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 08:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 08:13:33 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:5ceb5101e3b0d54efb5f18318982508a04b181b4d5ae52b096dd35dea3a006cc`  
		Last Modified: Thu, 25 Mar 2021 22:44:41 GMT  
		Size: 2.7 MB (2711898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532760a713fdcc47b0750cf149032179ac109897d27a4a7387254e873782ef5a`  
		Last Modified: Fri, 26 Mar 2021 08:16:21 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da9e5d008656a72a376d31d7c1cf4c750c1d20fdc9725470e92748f3d902aeb`  
		Last Modified: Fri, 26 Mar 2021 08:16:38 GMT  
		Size: 65.8 MB (65820533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6121bcad7cba7d37518917de5d2e4bb729cc62708b2c847ea1df48ccb757483f`  
		Last Modified: Fri, 26 Mar 2021 08:16:21 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8253019ed837881d065d263f197f95708f7073be3629b60a1e367d07f44a853c`  
		Last Modified: Fri, 26 Mar 2021 08:16:21 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:9ca9c858c4c5fc19f6527c3a238cbdea0fa9c40201aa6dacb74ac8ecb44178c4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70570068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6444ddc13b71ba29ad4262acb8347705e3186bce68856b0002722465f8fe8502`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 00:53:26 GMT
ARG VAULT_VERSION=1.7.0
# Thu, 25 Mar 2021 00:53:27 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 25 Mar 2021 00:53:35 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 25 Mar 2021 00:53:36 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 25 Mar 2021 00:53:37 GMT
VOLUME [/vault/logs]
# Thu, 25 Mar 2021 00:53:37 GMT
VOLUME [/vault/file]
# Thu, 25 Mar 2021 00:53:37 GMT
EXPOSE 8200
# Thu, 25 Mar 2021 00:53:37 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 25 Mar 2021 00:53:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Mar 2021 00:53:38 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca768045b18d821bd7431ec5078619ab1ef0c99fb0ff614bfdaaa9665278029`  
		Last Modified: Thu, 25 Mar 2021 00:54:32 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499c2c4856c3e0862f29ef4729b42c6eb0a5afde44966cd810da36db6716fc6e`  
		Last Modified: Thu, 25 Mar 2021 00:54:42 GMT  
		Size: 67.7 MB (67748633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a0103fd85fb669bfde787d1f69ca52754be530ed43599423687363e29e1948`  
		Last Modified: Thu, 25 Mar 2021 00:54:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17cea17112d0c6e8d055ddd4d3c66dca71c604283ca12327457059b643ef5d60`  
		Last Modified: Thu, 25 Mar 2021 00:54:32 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
