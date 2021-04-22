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
