<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `vault`

-	[`vault:1.3.4`](#vault134)
-	[`vault:1.4.0-rc1`](#vault140-rc1)
-	[`vault:latest`](#vaultlatest)

## `vault:1.3.4`

```console
$ docker pull vault@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `vault:1.4.0-rc1`

```console
$ docker pull vault@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `vault:latest`

```console
$ docker pull vault@sha256:5b753351ad1d9fd67505590b6b09496b295e0ae2e2ef4362d9b4beeaff574018
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:1b203c1d370e495d4379b3e755c2324410b6676b53c759aae22ca567af13db35
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51661318 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62afcace31e0772e99040ce20b031d771acecb0c6ca8e653444745a5fa4eaadd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:06 GMT
ADD file:d48cac34fac385cbc1de6adfdd88300f76f9bbe346cd17e64fd834d042a98326 in / 
# Thu, 23 Jan 2020 16:53:06 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2020 02:57:29 GMT
ARG VAULT_VERSION=1.3.3
# Fri, 06 Mar 2020 02:57:30 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 06 Mar 2020 02:57:38 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 06 Mar 2020 02:57:39 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 06 Mar 2020 02:57:40 GMT
VOLUME [/vault/logs]
# Fri, 06 Mar 2020 02:57:40 GMT
VOLUME [/vault/file]
# Fri, 06 Mar 2020 02:57:40 GMT
EXPOSE 8200
# Fri, 06 Mar 2020 02:57:41 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 06 Mar 2020 02:57:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Mar 2020 02:57:41 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:4167d3e149762ea326c26fc2fd4e36fdeb7d4e639408ad30f37b8f25ac285a98`  
		Last Modified: Thu, 23 Jan 2020 16:53:38 GMT  
		Size: 2.8 MB (2786962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:914a97be7f78b18056a221c1d0023fbb661f9541b82ddccc9370196e778f8fe6`  
		Last Modified: Fri, 06 Mar 2020 02:57:56 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6b0f45b5b08ad853e3605785296cfeeda0aea4ac447db9aa84dfe229f2c4bed`  
		Last Modified: Fri, 06 Mar 2020 02:58:09 GMT  
		Size: 48.9 MB (48871118 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87de0ca272088222aa4a962aff9e2f8208194873f9f9a91ddc75fe88d5e9a861`  
		Last Modified: Fri, 06 Mar 2020 02:57:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9bd5a355d95a63ef3fc609b4e2aa8d3a3353ae887c2e93c02aa501ca85eb8d3`  
		Last Modified: Fri, 06 Mar 2020 02:57:56 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:1b9997d4c553acbe418a13a4b73c762d7b49015d8b4c5b0e86f0f048596875f8
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48654912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b84ffdc311923e5d54fa3a59a1df6abf786f5ccd342895029ddb150dc5ff605b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Jan 2020 16:53:27 GMT
ADD file:2aa80d52585a6b34b2cc5811d46965a084e50cfb8cd183f1a88b2b1bc6556e1f in / 
# Thu, 23 Jan 2020 16:53:28 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2020 00:55:29 GMT
ARG VAULT_VERSION=1.3.3
# Fri, 06 Mar 2020 00:55:33 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 06 Mar 2020 00:55:45 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 06 Mar 2020 00:55:48 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 06 Mar 2020 00:55:49 GMT
VOLUME [/vault/logs]
# Fri, 06 Mar 2020 00:55:51 GMT
VOLUME [/vault/file]
# Fri, 06 Mar 2020 00:55:52 GMT
EXPOSE 8200
# Fri, 06 Mar 2020 00:55:53 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 06 Mar 2020 00:55:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Mar 2020 00:55:56 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:896868b7b9168cabb308702db96dc9769d10c23e20fc66f5f4abedf4c75d7642`  
		Last Modified: Thu, 23 Jan 2020 16:54:07 GMT  
		Size: 2.6 MB (2571407 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a567ddc30d56011de831c407b2129f5bcc2442b46cc8c15fbc1aacfabd3e0b9`  
		Last Modified: Fri, 06 Mar 2020 00:56:11 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edef0bda03882a1e50ca392e314c92878306caf2c2f58bebf6704b063c12627b`  
		Last Modified: Fri, 06 Mar 2020 00:56:27 GMT  
		Size: 46.1 MB (46080203 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdbaaf71699968312efe22141bfd4dde74d64cc07f33fe3b282a61f501dbeff2`  
		Last Modified: Fri, 06 Mar 2020 00:56:11 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7b7574cc3a74ae3094aa9e06c60e43bae43d2fac658175c79d6d4f07cbff8f7`  
		Last Modified: Fri, 06 Mar 2020 00:56:11 GMT  
		Size: 1.8 KB (1825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:08da0299cf2660db43448fb5ee35c0756cbcdfa1fcf150864acefc5f76484d3e
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48709684 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:63ef60ed7fe0af081d599c6b9f80fa226c9b35b8022cc7984bc41edb7a138adf`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Jan 2020 16:54:39 GMT
ADD file:bdfbd4b0dfb53eecc80bac65894d1e2fcfafb27dcf24ab019176e2c9f60b9a39 in / 
# Thu, 23 Jan 2020 16:54:40 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2020 01:47:23 GMT
ARG VAULT_VERSION=1.3.3
# Fri, 06 Mar 2020 01:47:25 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 06 Mar 2020 01:47:36 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 06 Mar 2020 01:47:44 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 06 Mar 2020 01:47:45 GMT
VOLUME [/vault/logs]
# Fri, 06 Mar 2020 01:47:46 GMT
VOLUME [/vault/file]
# Fri, 06 Mar 2020 01:47:48 GMT
EXPOSE 8200
# Fri, 06 Mar 2020 01:47:49 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 06 Mar 2020 01:47:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Mar 2020 01:47:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f07e4bcf42b862c240f4c00f2f7ed362d7d93ca15151de547beda593f3b669e5`  
		Last Modified: Thu, 23 Jan 2020 16:55:24 GMT  
		Size: 2.7 MB (2717732 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07ba3d7a0a1b09f2f2ba0550eeb29e8b8825c273d3a7bc682581606f0322023b`  
		Last Modified: Fri, 06 Mar 2020 01:48:09 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f186b25fe941fee17f647a95d3e025d5f937707bcaf8a282ca23ed947725edc`  
		Last Modified: Fri, 06 Mar 2020 01:48:22 GMT  
		Size: 46.0 MB (45988656 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b68c51c0befa64223d4d09e12b0a5f7a733aead3357fab45e490326e048d036`  
		Last Modified: Fri, 06 Mar 2020 01:48:09 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a752cc871ffdbf651cfa2e24fc6a82936583e1f4b2e1e8304d789361f9cc3047`  
		Last Modified: Fri, 06 Mar 2020 01:48:09 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:3cd22b722daff9917f9a08bde757562a2371dd05572cedf5aea35c59b951462d
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50115588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22be18d5c2e0ddec9e1715f2c4bf24393cc5c43cce976152e11e57a961fed73c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Jan 2020 16:52:57 GMT
ADD file:8c429ecc11f3cadcecc39922ce15df6b51a649929959b331fed8d1f42d722474 in / 
# Thu, 23 Jan 2020 16:52:57 GMT
CMD ["/bin/sh"]
# Fri, 06 Mar 2020 03:15:38 GMT
ARG VAULT_VERSION=1.3.3
# Fri, 06 Mar 2020 03:15:40 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 06 Mar 2020 03:15:47 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 06 Mar 2020 03:15:48 GMT
# ARGS: VAULT_VERSION=1.3.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 06 Mar 2020 03:15:48 GMT
VOLUME [/vault/logs]
# Fri, 06 Mar 2020 03:15:49 GMT
VOLUME [/vault/file]
# Fri, 06 Mar 2020 03:15:49 GMT
EXPOSE 8200
# Fri, 06 Mar 2020 03:15:49 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 06 Mar 2020 03:15:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 06 Mar 2020 03:15:49 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:8ad089020f8a1fd366fb13feb183e2f4c7410e2232c54b40f6a54fd56029fdf3`  
		Last Modified: Thu, 23 Jan 2020 16:53:22 GMT  
		Size: 2.8 MB (2785861 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2983c25fde9b3a5aac2130561da76af1294ddc9b74bf9009eb2938b24fc5f2d`  
		Last Modified: Fri, 06 Mar 2020 03:16:00 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c475463be64b31e8be1fd9086c0b94fe2c0232287a87de9a6041c92605356ec`  
		Last Modified: Fri, 06 Mar 2020 03:16:12 GMT  
		Size: 47.3 MB (47326492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eab3e6cabb9495f0b5417576d9a01675fffd8cc7af1cfca75d838b0ab15053e4`  
		Last Modified: Fri, 06 Mar 2020 03:16:00 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e799b1d2c4f4b1f74ac84f65f440b52ed376f5887c1d692e1391fe7c6d77a56`  
		Last Modified: Fri, 06 Mar 2020 03:16:00 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
