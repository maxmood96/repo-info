<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `vault`

-	[`vault:1.3.2`](#vault132)
-	[`vault:latest`](#vaultlatest)

## `vault:1.3.2`

```console
$ docker pull vault@sha256:2c174b5405de7ce9f2c1953416715dd6b6aeec4c5f3d68485bb2ebcf1372f15f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.3.2` - linux; amd64

```console
$ docker pull vault@sha256:f5d59e4661c476456436053c3fc095d44cfc3a1a567c946b480c9084519b31e0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51638456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed4dfee4b28684a3ce4dc88e661fd7766c1f474f11de592584d4f9235e4c7e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 01:42:37 GMT
ARG VAULT_VERSION=1.3.2
# Thu, 23 Jan 2020 01:42:39 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 23 Jan 2020 01:42:48 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 23 Jan 2020 01:42:49 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 23 Jan 2020 01:42:50 GMT
VOLUME [/vault/logs]
# Thu, 23 Jan 2020 01:42:50 GMT
VOLUME [/vault/file]
# Thu, 23 Jan 2020 01:42:50 GMT
EXPOSE 8200
# Thu, 23 Jan 2020 01:42:51 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 01:42:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 01:42:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28dde1fe3c3a096c6913f6ac86539b832c59b03752e505a79598bbb651cdd31`  
		Last Modified: Thu, 23 Jan 2020 01:43:02 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5c8a53e93f6eb56cb61c0058c51b92748ad67df223fe5455d4793e108ad0d3`  
		Last Modified: Thu, 23 Jan 2020 01:43:28 GMT  
		Size: 48.8 MB (48848090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd37952b5471a8e7853bd82ccadb28eb577024017cc137ebcb88a0fd938cc13`  
		Last Modified: Thu, 23 Jan 2020 01:43:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f49952ad5ba9abcb19b33d48ff892dca7268ed04c8f883cec3b453ad4a8684c`  
		Last Modified: Thu, 23 Jan 2020 01:43:02 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.3.2` - linux; arm variant v6

```console
$ docker pull vault@sha256:c1ac1d0368915ea132a37c45aa13f75c7cefa9c39325efb868786cd28fa967a1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48648883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df56abd187c6a4cc9f3e65c682f477380a0c8e00ae27ceb9e3ee5a3a011bbd30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 21 Oct 2019 16:56:02 GMT
ADD file:d3c7d938a78143f106a6a467ce23b599198e041220e661e5326ba91054c353ef in / 
# Mon, 21 Oct 2019 16:56:04 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 01:01:29 GMT
ARG VAULT_VERSION=1.3.2
# Thu, 23 Jan 2020 01:01:32 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 23 Jan 2020 01:01:47 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 23 Jan 2020 01:01:50 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 23 Jan 2020 01:01:52 GMT
VOLUME [/vault/logs]
# Thu, 23 Jan 2020 01:01:53 GMT
VOLUME [/vault/file]
# Thu, 23 Jan 2020 01:01:54 GMT
EXPOSE 8200
# Thu, 23 Jan 2020 01:01:55 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 01:01:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 01:01:57 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ecf664be551d26dcd221b7387283cdcc54f46c6789700d037fa3cd0c297f8645`  
		Last Modified: Mon, 21 Oct 2019 16:56:34 GMT  
		Size: 2.6 MB (2571309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f236cf72b651649acd302f6c9aa5b5cce89f399157e01df84670cd33b1b433`  
		Last Modified: Thu, 23 Jan 2020 01:02:06 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c5ec0d9992ffe79ddaa0317f506446fadb5d202d30800fc9b7838deca810bb`  
		Last Modified: Thu, 23 Jan 2020 01:02:21 GMT  
		Size: 46.1 MB (46074267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1be5f5708bd4eb33e839ae3aea27cd1164dc88077b80b172945673bc0fdfea`  
		Last Modified: Thu, 23 Jan 2020 01:02:06 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d38d7b809cadb1b5891d1d95194ecb0e5c7f8e88b9d7f8f37524da4d8027a80`  
		Last Modified: Thu, 23 Jan 2020 01:02:06 GMT  
		Size: 1.8 KB (1826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.3.2` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:5b33ffc999c630e56c3546d32178a0c60e717a8742bad5ec543ed9d277507060
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48702927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cd00da8104eab4240b89d524326f0303a4f67ab341e0e75684bbb14c2c114f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 21 Oct 2019 18:07:03 GMT
ADD file:02f4d68afd9e9e303ff893f198d535d0d78c4b2554f299ab2d0955b2bef0e06a in / 
# Mon, 21 Oct 2019 18:07:09 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 00:51:12 GMT
ARG VAULT_VERSION=1.3.2
# Thu, 23 Jan 2020 00:51:17 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 23 Jan 2020 00:51:29 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 23 Jan 2020 00:51:35 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 23 Jan 2020 00:51:36 GMT
VOLUME [/vault/logs]
# Thu, 23 Jan 2020 00:51:37 GMT
VOLUME [/vault/file]
# Thu, 23 Jan 2020 00:51:38 GMT
EXPOSE 8200
# Thu, 23 Jan 2020 00:51:39 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 00:51:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 00:51:42 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:8bfa913040406727f36faa9b69d0b96e071b13792a83ad69c19389031a9f3797`  
		Last Modified: Mon, 21 Oct 2019 18:08:36 GMT  
		Size: 2.7 MB (2717778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cd64812492ee9f3b02daa786466fbf62288308eeb7ee14638234839bd89cfc`  
		Last Modified: Thu, 23 Jan 2020 00:51:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339e585090f8b57b724bc3f7f948c1ce605d38161fe0529a66b9252aa2d6fb42`  
		Last Modified: Thu, 23 Jan 2020 00:52:12 GMT  
		Size: 46.0 MB (45981853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f6ec1e08412208fcb3ec2fbe92f0ab87ef8e7f69d7c6f458c5aa43d94005e5`  
		Last Modified: Thu, 23 Jan 2020 00:51:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e5657a899463cb81fd7e196333884c8ed8f37f5b13cc2f54f9f3d565194230`  
		Last Modified: Thu, 23 Jan 2020 00:51:57 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.3.2` - linux; 386

```console
$ docker pull vault@sha256:a08805ef34293243ed0b42b2992cddada942af061928472b4179e43a8b0aa303
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50110969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a35287d792e022200aaba53c6a482be3e78713f916e6e9793a2d18c9ba33f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 21 Oct 2019 16:46:04 GMT
ADD file:dd3b3676fd9c1e0983ade68242b9b9ac5c477f3e4bfc97c2e78fd5db93a441c9 in / 
# Mon, 21 Oct 2019 16:46:04 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 00:37:26 GMT
ARG VAULT_VERSION=1.3.2
# Thu, 23 Jan 2020 00:37:27 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 23 Jan 2020 00:37:33 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 23 Jan 2020 00:37:34 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 23 Jan 2020 00:37:34 GMT
VOLUME [/vault/logs]
# Thu, 23 Jan 2020 00:37:34 GMT
VOLUME [/vault/file]
# Thu, 23 Jan 2020 00:37:34 GMT
EXPOSE 8200
# Thu, 23 Jan 2020 00:37:34 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 00:37:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 00:37:35 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f913bd05bf684aaa4bc173d73cfbb58abb45587962d74f0aa71df36b6b489def`  
		Last Modified: Mon, 21 Oct 2019 16:46:25 GMT  
		Size: 2.8 MB (2785939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff789d789e4d18dd368b4863e187d271f0dd7a14e13bef3dbbed045aa88a109`  
		Last Modified: Thu, 23 Jan 2020 00:37:42 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031da651da359ea0381bae5680d7bca73dc7690e81fbb5cf1258ce0884c606d8`  
		Last Modified: Thu, 23 Jan 2020 00:37:54 GMT  
		Size: 47.3 MB (47321799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92ca2c9ac411ddcaa517ab7f9e4581b1485b098538a964c689e3eb04df783c0`  
		Last Modified: Thu, 23 Jan 2020 00:37:42 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6ca638a990477e39c71747e693985f5a200fbe4ad4a9114f900e9794250ed1`  
		Last Modified: Thu, 23 Jan 2020 00:37:42 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:latest`

```console
$ docker pull vault@sha256:2c174b5405de7ce9f2c1953416715dd6b6aeec4c5f3d68485bb2ebcf1372f15f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:f5d59e4661c476456436053c3fc095d44cfc3a1a567c946b480c9084519b31e0
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.6 MB (51638456 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ed4dfee4b28684a3ce4dc88e661fd7766c1f474f11de592584d4f9235e4c7e6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 21 Oct 2019 17:21:42 GMT
ADD file:fe1f09249227e2da2089afb4d07e16cbf832eeb804120074acd2b8192876cd28 in / 
# Mon, 21 Oct 2019 17:21:42 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 01:42:37 GMT
ARG VAULT_VERSION=1.3.2
# Thu, 23 Jan 2020 01:42:39 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 23 Jan 2020 01:42:48 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 23 Jan 2020 01:42:49 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 23 Jan 2020 01:42:50 GMT
VOLUME [/vault/logs]
# Thu, 23 Jan 2020 01:42:50 GMT
VOLUME [/vault/file]
# Thu, 23 Jan 2020 01:42:50 GMT
EXPOSE 8200
# Thu, 23 Jan 2020 01:42:51 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 01:42:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 01:42:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:89d9c30c1d48bac627e5c6cb0d1ed1eec28e7dbdfbcc04712e4c79c0f83faf17`  
		Last Modified: Mon, 21 Oct 2019 17:22:48 GMT  
		Size: 2.8 MB (2787134 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a28dde1fe3c3a096c6913f6ac86539b832c59b03752e505a79598bbb651cdd31`  
		Last Modified: Thu, 23 Jan 2020 01:43:02 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf5c8a53e93f6eb56cb61c0058c51b92748ad67df223fe5455d4793e108ad0d3`  
		Last Modified: Thu, 23 Jan 2020 01:43:28 GMT  
		Size: 48.8 MB (48848090 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fcd37952b5471a8e7853bd82ccadb28eb577024017cc137ebcb88a0fd938cc13`  
		Last Modified: Thu, 23 Jan 2020 01:43:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f49952ad5ba9abcb19b33d48ff892dca7268ed04c8f883cec3b453ad4a8684c`  
		Last Modified: Thu, 23 Jan 2020 01:43:02 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:c1ac1d0368915ea132a37c45aa13f75c7cefa9c39325efb868786cd28fa967a1
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.6 MB (48648883 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:df56abd187c6a4cc9f3e65c682f477380a0c8e00ae27ceb9e3ee5a3a011bbd30`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 21 Oct 2019 16:56:02 GMT
ADD file:d3c7d938a78143f106a6a467ce23b599198e041220e661e5326ba91054c353ef in / 
# Mon, 21 Oct 2019 16:56:04 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 01:01:29 GMT
ARG VAULT_VERSION=1.3.2
# Thu, 23 Jan 2020 01:01:32 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 23 Jan 2020 01:01:47 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 23 Jan 2020 01:01:50 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 23 Jan 2020 01:01:52 GMT
VOLUME [/vault/logs]
# Thu, 23 Jan 2020 01:01:53 GMT
VOLUME [/vault/file]
# Thu, 23 Jan 2020 01:01:54 GMT
EXPOSE 8200
# Thu, 23 Jan 2020 01:01:55 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 01:01:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 01:01:57 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ecf664be551d26dcd221b7387283cdcc54f46c6789700d037fa3cd0c297f8645`  
		Last Modified: Mon, 21 Oct 2019 16:56:34 GMT  
		Size: 2.6 MB (2571309 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96f236cf72b651649acd302f6c9aa5b5cce89f399157e01df84670cd33b1b433`  
		Last Modified: Thu, 23 Jan 2020 01:02:06 GMT  
		Size: 1.3 KB (1295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c5ec0d9992ffe79ddaa0317f506446fadb5d202d30800fc9b7838deca810bb`  
		Last Modified: Thu, 23 Jan 2020 01:02:21 GMT  
		Size: 46.1 MB (46074267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1be5f5708bd4eb33e839ae3aea27cd1164dc88077b80b172945673bc0fdfea`  
		Last Modified: Thu, 23 Jan 2020 01:02:06 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d38d7b809cadb1b5891d1d95194ecb0e5c7f8e88b9d7f8f37524da4d8027a80`  
		Last Modified: Thu, 23 Jan 2020 01:02:06 GMT  
		Size: 1.8 KB (1826 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:5b33ffc999c630e56c3546d32178a0c60e717a8742bad5ec543ed9d277507060
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48702927 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b0cd00da8104eab4240b89d524326f0303a4f67ab341e0e75684bbb14c2c114f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 21 Oct 2019 18:07:03 GMT
ADD file:02f4d68afd9e9e303ff893f198d535d0d78c4b2554f299ab2d0955b2bef0e06a in / 
# Mon, 21 Oct 2019 18:07:09 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 00:51:12 GMT
ARG VAULT_VERSION=1.3.2
# Thu, 23 Jan 2020 00:51:17 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 23 Jan 2020 00:51:29 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 23 Jan 2020 00:51:35 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 23 Jan 2020 00:51:36 GMT
VOLUME [/vault/logs]
# Thu, 23 Jan 2020 00:51:37 GMT
VOLUME [/vault/file]
# Thu, 23 Jan 2020 00:51:38 GMT
EXPOSE 8200
# Thu, 23 Jan 2020 00:51:39 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 00:51:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 00:51:42 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:8bfa913040406727f36faa9b69d0b96e071b13792a83ad69c19389031a9f3797`  
		Last Modified: Mon, 21 Oct 2019 18:08:36 GMT  
		Size: 2.7 MB (2717778 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6cd64812492ee9f3b02daa786466fbf62288308eeb7ee14638234839bd89cfc`  
		Last Modified: Thu, 23 Jan 2020 00:51:58 GMT  
		Size: 1.3 KB (1285 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:339e585090f8b57b724bc3f7f948c1ce605d38161fe0529a66b9252aa2d6fb42`  
		Last Modified: Thu, 23 Jan 2020 00:52:12 GMT  
		Size: 46.0 MB (45981853 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56f6ec1e08412208fcb3ec2fbe92f0ab87ef8e7f69d7c6f458c5aa43d94005e5`  
		Last Modified: Thu, 23 Jan 2020 00:51:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e5657a899463cb81fd7e196333884c8ed8f37f5b13cc2f54f9f3d565194230`  
		Last Modified: Thu, 23 Jan 2020 00:51:57 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:a08805ef34293243ed0b42b2992cddada942af061928472b4179e43a8b0aa303
```

-	Docker Version: 18.06.1-ce
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50110969 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:75a35287d792e022200aaba53c6a482be3e78713f916e6e9793a2d18c9ba33f4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 21 Oct 2019 16:46:04 GMT
ADD file:dd3b3676fd9c1e0983ade68242b9b9ac5c477f3e4bfc97c2e78fd5db93a441c9 in / 
# Mon, 21 Oct 2019 16:46:04 GMT
CMD ["/bin/sh"]
# Thu, 23 Jan 2020 00:37:26 GMT
ARG VAULT_VERSION=1.3.2
# Thu, 23 Jan 2020 00:37:27 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 23 Jan 2020 00:37:33 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 23 Jan 2020 00:37:34 GMT
# ARGS: VAULT_VERSION=1.3.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 23 Jan 2020 00:37:34 GMT
VOLUME [/vault/logs]
# Thu, 23 Jan 2020 00:37:34 GMT
VOLUME [/vault/file]
# Thu, 23 Jan 2020 00:37:34 GMT
EXPOSE 8200
# Thu, 23 Jan 2020 00:37:34 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 23 Jan 2020 00:37:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 23 Jan 2020 00:37:35 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f913bd05bf684aaa4bc173d73cfbb58abb45587962d74f0aa71df36b6b489def`  
		Last Modified: Mon, 21 Oct 2019 16:46:25 GMT  
		Size: 2.8 MB (2785939 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dff789d789e4d18dd368b4863e187d271f0dd7a14e13bef3dbbed045aa88a109`  
		Last Modified: Thu, 23 Jan 2020 00:37:42 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:031da651da359ea0381bae5680d7bca73dc7690e81fbb5cf1258ce0884c606d8`  
		Last Modified: Thu, 23 Jan 2020 00:37:54 GMT  
		Size: 47.3 MB (47321799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b92ca2c9ac411ddcaa517ab7f9e4581b1485b098538a964c689e3eb04df783c0`  
		Last Modified: Thu, 23 Jan 2020 00:37:42 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb6ca638a990477e39c71747e693985f5a200fbe4ad4a9114f900e9794250ed1`  
		Last Modified: Thu, 23 Jan 2020 00:37:42 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
