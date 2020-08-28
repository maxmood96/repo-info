<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `vault`

-	[`vault:1.2.7`](#vault127)
-	[`vault:1.3.10`](#vault1310)
-	[`vault:1.4.6`](#vault146)
-	[`vault:1.5.3`](#vault153)
-	[`vault:latest`](#vaultlatest)

## `vault:1.2.7`

```console
$ docker pull vault@sha256:aee462dc8a23239ecce95807ab934f229a356656cc8ff15ac31a04fbcce20bd8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.2.7` - linux; amd64

```console
$ docker pull vault@sha256:e29ea9ccb329275d4dcfa369d367bd9dd7a71359162b6e1e9063c01ccdc0cbfa
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.4 MB (49440366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dfb4737e954bb0872117b35ba39ccfb70c20e7f14acbf111a47cd531f8a4136`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 28 Aug 2020 17:27:36 GMT
ARG VAULT_VERSION=1.2.7
# Fri, 28 Aug 2020 17:27:36 GMT
# ARGS: VAULT_VERSION=1.2.7
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 28 Aug 2020 17:27:41 GMT
# ARGS: VAULT_VERSION=1.2.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 28 Aug 2020 17:27:42 GMT
# ARGS: VAULT_VERSION=1.2.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 28 Aug 2020 17:27:42 GMT
VOLUME [/vault/logs]
# Fri, 28 Aug 2020 17:27:42 GMT
VOLUME [/vault/file]
# Fri, 28 Aug 2020 17:27:42 GMT
EXPOSE 8200
# Fri, 28 Aug 2020 17:27:43 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 28 Aug 2020 17:27:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Aug 2020 17:27:43 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:740b18f94145e074ad48fc25bf0ebd7248bf7ddc6f6d878155a17b2e54e7795a`  
		Last Modified: Fri, 28 Aug 2020 17:28:32 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:266eb890c0e41d7fa0b16b7cf1f3f9effe062d9bca1b76ebe669b7d731623a26`  
		Last Modified: Fri, 28 Aug 2020 17:28:40 GMT  
		Size: 46.6 MB (46641550 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a00807a58482655bbe17e2defd05868daba7ccec91f0ad85a509c931a40dc981`  
		Last Modified: Fri, 28 Aug 2020 17:28:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2886bac70f514e11c9fe0434b99beb39d00e5232b1fbc9418adeb501be669f`  
		Last Modified: Fri, 28 Aug 2020 17:28:32 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.2.7` - linux; arm variant v6

```console
$ docker pull vault@sha256:15206204d0c56fe550d044f662c25392250b1de3d336eda4c36bd2ca0241854d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46536890 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4303cff742b86b4811fc68e512cf527f5db9da5034d4b4d7e3dab2f92dd3fd8f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:35 GMT
ADD file:ef75120295e25a8e67c5ef378df2cf4ce9f7b83b44709452fcaf247b54fabd16 in / 
# Thu, 23 Apr 2020 15:51:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Aug 2020 18:20:21 GMT
ARG VAULT_VERSION=1.2.7
# Fri, 28 Aug 2020 18:20:27 GMT
# ARGS: VAULT_VERSION=1.2.7
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 28 Aug 2020 18:20:38 GMT
# ARGS: VAULT_VERSION=1.2.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 28 Aug 2020 18:20:42 GMT
# ARGS: VAULT_VERSION=1.2.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 28 Aug 2020 18:20:42 GMT
VOLUME [/vault/logs]
# Fri, 28 Aug 2020 18:20:43 GMT
VOLUME [/vault/file]
# Fri, 28 Aug 2020 18:20:44 GMT
EXPOSE 8200
# Fri, 28 Aug 2020 18:20:44 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 28 Aug 2020 18:20:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Aug 2020 18:20:46 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:e745d1dc1c9e0be26166278da7632765ca98fa1be8179a7cc440b3bdc5671860`  
		Last Modified: Thu, 23 Apr 2020 15:52:15 GMT  
		Size: 2.6 MB (2572512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a54ec1fa1029fc97984ea63634a4b1fb3e8528b370fea257e68ebbc6b849495f`  
		Last Modified: Fri, 28 Aug 2020 18:21:55 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7439080c4c21265353b53de8895718cfbbaf16baad454c61ccd293bdcf8d3fc`  
		Last Modified: Fri, 28 Aug 2020 18:22:07 GMT  
		Size: 44.0 MB (43961079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:416cd98d841bfa527479438c5024816b8939d2ce589ef0cf29ea681fd6ae7f0a`  
		Last Modified: Fri, 28 Aug 2020 18:21:55 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:110cbf89758190f6a67effa36ad5f64942d9fb2ed2408c247d96451634863849`  
		Last Modified: Fri, 28 Aug 2020 18:21:55 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.2.7` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:3bf2af64d4a696228a77473f038f4a7b5c07b7173ccccd00d88b85c2e0e538ba
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46601389 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f21dd896d21130f74969b695e829b913148a0be08ab9905d538cf79c7f1fb0a9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:52 GMT
ADD file:75529f7e83edb6d0457a3b8bbfe33d4e3a12f339c5ace517d0f52dbedd9a146b in / 
# Fri, 24 Apr 2020 00:14:53 GMT
CMD ["/bin/sh"]
# Fri, 28 Aug 2020 19:13:11 GMT
ARG VAULT_VERSION=1.2.7
# Fri, 28 Aug 2020 19:13:13 GMT
# ARGS: VAULT_VERSION=1.2.7
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 28 Aug 2020 19:13:20 GMT
# ARGS: VAULT_VERSION=1.2.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 28 Aug 2020 19:13:23 GMT
# ARGS: VAULT_VERSION=1.2.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 28 Aug 2020 19:13:24 GMT
VOLUME [/vault/logs]
# Fri, 28 Aug 2020 19:13:24 GMT
VOLUME [/vault/file]
# Fri, 28 Aug 2020 19:13:25 GMT
EXPOSE 8200
# Fri, 28 Aug 2020 19:13:26 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 28 Aug 2020 19:13:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Aug 2020 19:13:27 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:b038bcb63e9c8905cc879c957302f686a9b43f24a18dcfc4186ab236ddf04cad`  
		Last Modified: Fri, 24 Apr 2020 00:15:54 GMT  
		Size: 2.7 MB (2718734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2cfc897594fe8cc183a46faeda09ce1d7de0b3726a491ede58c2e0eecb38cda8`  
		Last Modified: Fri, 28 Aug 2020 19:14:32 GMT  
		Size: 1.3 KB (1292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7cf77a6432db7b3f748ad3543eda682005f3eece438f8a8aace25d3d323928`  
		Last Modified: Fri, 28 Aug 2020 19:14:44 GMT  
		Size: 43.9 MB (43879352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b523ed4ebb04f4b6a831f63360a70c4495a39a7ba6e5f775ad6369fab3ad22a5`  
		Last Modified: Fri, 28 Aug 2020 19:14:32 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83caf85cb0f3094392cd748e88196834d5ac5996bb636b22493107c406900920`  
		Last Modified: Fri, 28 Aug 2020 19:14:32 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.2.7` - linux; 386

```console
$ docker pull vault@sha256:6c4449ec08fafacec68c70560fb9e937bf66e079736af60915cad6e6ebbe4375
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.9 MB (47930888 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23f441550f1ceb173ce152125c3b492850c35f01c1566902cebb50eb847a1e83`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:11 GMT
ADD file:2e9fb162fdd20e7ac6e9edcb9e1ce9ece750f125c93824c5709a2800ae397f89 in / 
# Thu, 23 Apr 2020 21:16:11 GMT
CMD ["/bin/sh"]
# Fri, 28 Aug 2020 19:53:24 GMT
ARG VAULT_VERSION=1.2.7
# Fri, 28 Aug 2020 19:53:25 GMT
# ARGS: VAULT_VERSION=1.2.7
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 28 Aug 2020 19:53:31 GMT
# ARGS: VAULT_VERSION=1.2.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 28 Aug 2020 19:53:32 GMT
# ARGS: VAULT_VERSION=1.2.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 28 Aug 2020 19:53:32 GMT
VOLUME [/vault/logs]
# Fri, 28 Aug 2020 19:53:33 GMT
VOLUME [/vault/file]
# Fri, 28 Aug 2020 19:53:33 GMT
EXPOSE 8200
# Fri, 28 Aug 2020 19:53:33 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 28 Aug 2020 19:53:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Aug 2020 19:53:34 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:294658c31053f36b08a64158e37d4fb84478e6fe8f4d5127c51a6334c8a3c36d`  
		Last Modified: Thu, 23 Apr 2020 21:16:37 GMT  
		Size: 2.8 MB (2787128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38a28f7aa84f9b80fd14e802a15b7f544f170f43606d0fe1037dbe9bde9c0cb4`  
		Last Modified: Fri, 28 Aug 2020 19:54:34 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd17384d999dd979495fccd4839026185fb357ea3859385ab238f5d401fdcdf`  
		Last Modified: Fri, 28 Aug 2020 19:54:44 GMT  
		Size: 45.1 MB (45140523 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e7a2a7877ab5f8922b8ae2a25d04f53b0296fc6ca7e947f81c75e5ac2c4d1711`  
		Last Modified: Fri, 28 Aug 2020 19:54:34 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f782f2f2e9c1fa4650bad994c9a074c277c1edf8820b8c4e02737627797d00e`  
		Last Modified: Fri, 28 Aug 2020 19:54:34 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.3.10`

```console
$ docker pull vault@sha256:8199c0f2edb1436d7fccf4c53c6f117026d9280534cb6e50d3671506ae5dd553
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.3.10` - linux; amd64

```console
$ docker pull vault@sha256:9d0ded16939c280c64178490cdadbdfaa55f267ccf2560338732b9d688eb8637
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51663648 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:26d28da1236b6d5c77abe62599aa617ae781aab5446c0f6c6f784d95dc5ad79d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 28 Aug 2020 17:27:23 GMT
ARG VAULT_VERSION=1.3.10
# Fri, 28 Aug 2020 17:27:24 GMT
# ARGS: VAULT_VERSION=1.3.10
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 28 Aug 2020 17:27:29 GMT
# ARGS: VAULT_VERSION=1.3.10
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 28 Aug 2020 17:27:29 GMT
# ARGS: VAULT_VERSION=1.3.10
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 28 Aug 2020 17:27:30 GMT
VOLUME [/vault/logs]
# Fri, 28 Aug 2020 17:27:30 GMT
VOLUME [/vault/file]
# Fri, 28 Aug 2020 17:27:30 GMT
EXPOSE 8200
# Fri, 28 Aug 2020 17:27:30 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 28 Aug 2020 17:27:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Aug 2020 17:27:31 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2864427cd927834196a4af585b1da25a844a00695e9c75b680cc3e3ea7ca455f`  
		Last Modified: Fri, 28 Aug 2020 17:28:21 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0665b6a455a88fa56ba8d09d6afdc2c31be7c4d792b10dda844fb99648742a67`  
		Last Modified: Fri, 28 Aug 2020 17:28:29 GMT  
		Size: 48.9 MB (48864829 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ae56a42199a877bee8d42cfc4faaa851e030a2d006621b481c687c98e0e1b8`  
		Last Modified: Fri, 28 Aug 2020 17:28:21 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04641152c2a14b8c7dc01d5e2a5782abb60d5424b86ef499fef11932726a20d4`  
		Last Modified: Fri, 28 Aug 2020 17:28:21 GMT  
		Size: 1.8 KB (1824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.3.10` - linux; arm variant v6

```console
$ docker pull vault@sha256:14ffcaff915361a898847034df18e5186e382445cb861d2fceb6188170bd1e9d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48656145 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:acf56572633fe1ff52dee9a2cbaf1a30250feea99d4afb63dc7af8ead6ef38d5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:35 GMT
ADD file:ef75120295e25a8e67c5ef378df2cf4ce9f7b83b44709452fcaf247b54fabd16 in / 
# Thu, 23 Apr 2020 15:51:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Aug 2020 18:19:50 GMT
ARG VAULT_VERSION=1.3.10
# Fri, 28 Aug 2020 18:19:53 GMT
# ARGS: VAULT_VERSION=1.3.10
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 28 Aug 2020 18:20:03 GMT
# ARGS: VAULT_VERSION=1.3.10
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 28 Aug 2020 18:20:07 GMT
# ARGS: VAULT_VERSION=1.3.10
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 28 Aug 2020 18:20:08 GMT
VOLUME [/vault/logs]
# Fri, 28 Aug 2020 18:20:09 GMT
VOLUME [/vault/file]
# Fri, 28 Aug 2020 18:20:10 GMT
EXPOSE 8200
# Fri, 28 Aug 2020 18:20:10 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 28 Aug 2020 18:20:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Aug 2020 18:20:13 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:e745d1dc1c9e0be26166278da7632765ca98fa1be8179a7cc440b3bdc5671860`  
		Last Modified: Thu, 23 Apr 2020 15:52:15 GMT  
		Size: 2.6 MB (2572512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ae40600e8fe17ccc0a515a5746519966b797357c8f70cce8312909de838021`  
		Last Modified: Fri, 28 Aug 2020 18:21:35 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0772f6b771be817b9ed2bc2caf2d00d091d557d3ab8f0a627b92cfca96946e71`  
		Last Modified: Fri, 28 Aug 2020 18:21:49 GMT  
		Size: 46.1 MB (46080334 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:febe7e7234b460a4e6c2c438f83a4f142c6caf6ab4678c01b9e637dcbc1a83fd`  
		Last Modified: Fri, 28 Aug 2020 18:21:35 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a7166fdaa3f2aeda0a90b2b4770ce9600e32363733724e4119c66d2b369864ff`  
		Last Modified: Fri, 28 Aug 2020 18:21:35 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.3.10` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:5bdfcd9077bbf2f29e1bbf050c09fb48f18de63e247ae7f1fafb00fb8e4dc9be
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48688701 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca31dfe8d035fbf179600878013a2cc88d8ffa5ac3e3f7ec3b69a7d585f18a49`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:52 GMT
ADD file:75529f7e83edb6d0457a3b8bbfe33d4e3a12f339c5ace517d0f52dbedd9a146b in / 
# Fri, 24 Apr 2020 00:14:53 GMT
CMD ["/bin/sh"]
# Fri, 28 Aug 2020 19:12:41 GMT
ARG VAULT_VERSION=1.3.10
# Fri, 28 Aug 2020 19:12:45 GMT
# ARGS: VAULT_VERSION=1.3.10
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 28 Aug 2020 19:12:55 GMT
# ARGS: VAULT_VERSION=1.3.10
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 28 Aug 2020 19:12:59 GMT
# ARGS: VAULT_VERSION=1.3.10
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 28 Aug 2020 19:13:00 GMT
VOLUME [/vault/logs]
# Fri, 28 Aug 2020 19:13:01 GMT
VOLUME [/vault/file]
# Fri, 28 Aug 2020 19:13:02 GMT
EXPOSE 8200
# Fri, 28 Aug 2020 19:13:03 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 28 Aug 2020 19:13:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Aug 2020 19:13:04 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:b038bcb63e9c8905cc879c957302f686a9b43f24a18dcfc4186ab236ddf04cad`  
		Last Modified: Fri, 24 Apr 2020 00:15:54 GMT  
		Size: 2.7 MB (2718734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ab7eeaab3ba49192f2e544672e20921e63bc218102c1cf5fba05aa407a2672f`  
		Last Modified: Fri, 28 Aug 2020 19:14:14 GMT  
		Size: 1.3 KB (1287 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:22135197380ddbe542ff1a83e98d6a7d1d3dd9a038a2bef9fa31a0441aa84727`  
		Last Modified: Fri, 28 Aug 2020 19:14:26 GMT  
		Size: 46.0 MB (45966669 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:484ee2d9eee3a9e319ac090bcad1f5999aac4247e8d6494d961be18c817a67d0`  
		Last Modified: Fri, 28 Aug 2020 19:14:15 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d6c625c23648647e578a6519b2829b43e1293e125a8d59928bb107ac996bbb3`  
		Last Modified: Fri, 28 Aug 2020 19:14:14 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.3.10` - linux; 386

```console
$ docker pull vault@sha256:82e5312ed4247b021e771a9d41cfd0baa1e2b64671bec0339cc2ff2324b6cc05
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.1 MB (50109671 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cd62b27693a617dfc74514abd871aa060a0cf9b09fa9a6873552eb3119c79057`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:11 GMT
ADD file:2e9fb162fdd20e7ac6e9edcb9e1ce9ece750f125c93824c5709a2800ae397f89 in / 
# Thu, 23 Apr 2020 21:16:11 GMT
CMD ["/bin/sh"]
# Fri, 28 Aug 2020 19:53:10 GMT
ARG VAULT_VERSION=1.3.10
# Fri, 28 Aug 2020 19:53:11 GMT
# ARGS: VAULT_VERSION=1.3.10
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 28 Aug 2020 19:53:17 GMT
# ARGS: VAULT_VERSION=1.3.10
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 28 Aug 2020 19:53:18 GMT
# ARGS: VAULT_VERSION=1.3.10
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 28 Aug 2020 19:53:19 GMT
VOLUME [/vault/logs]
# Fri, 28 Aug 2020 19:53:19 GMT
VOLUME [/vault/file]
# Fri, 28 Aug 2020 19:53:19 GMT
EXPOSE 8200
# Fri, 28 Aug 2020 19:53:19 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 28 Aug 2020 19:53:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Aug 2020 19:53:20 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:294658c31053f36b08a64158e37d4fb84478e6fe8f4d5127c51a6334c8a3c36d`  
		Last Modified: Thu, 23 Apr 2020 21:16:37 GMT  
		Size: 2.8 MB (2787128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:958bfe319e91092152e873d8240c7686781c583513b0602a7baf6228008a8b43`  
		Last Modified: Fri, 28 Aug 2020 19:54:18 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cd62208c6b59adc4690de62f3f1c43af0aa2d6b52c361fa6485d7bda22c4b39`  
		Last Modified: Fri, 28 Aug 2020 19:54:30 GMT  
		Size: 47.3 MB (47319305 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cbd9105313afcb66346b70d0f2f0e6c0bb2566544b0293be0cb8efe6de6f48c`  
		Last Modified: Fri, 28 Aug 2020 19:54:18 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e79a1c4c49926a374e6264d22a6859fb626eff912bb6045c9ff1f9de3e49b2d`  
		Last Modified: Fri, 28 Aug 2020 19:54:18 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.4.6`

```console
$ docker pull vault@sha256:89c3c1bfdb3adf8c9e44035564ff314c2df78b4e7e58b285eafe684fa66b0e87
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.4.6` - linux; amd64

```console
$ docker pull vault@sha256:8f2e9e25aa4e3047ea72df174cb30c75dba0a1c124ff09349f2bb29028c921a4
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52067665 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f857baf96a31e74e926307779077dad56ada5f8fd5eeb8f7960b2b7c3b1b4e3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 28 Aug 2020 17:27:11 GMT
ARG VAULT_VERSION=1.4.6
# Fri, 28 Aug 2020 17:27:11 GMT
# ARGS: VAULT_VERSION=1.4.6
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 28 Aug 2020 17:27:16 GMT
# ARGS: VAULT_VERSION=1.4.6
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 28 Aug 2020 17:27:17 GMT
# ARGS: VAULT_VERSION=1.4.6
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 28 Aug 2020 17:27:17 GMT
VOLUME [/vault/logs]
# Fri, 28 Aug 2020 17:27:17 GMT
VOLUME [/vault/file]
# Fri, 28 Aug 2020 17:27:18 GMT
EXPOSE 8200
# Fri, 28 Aug 2020 17:27:18 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 28 Aug 2020 17:27:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Aug 2020 17:27:18 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db8cb72614269ebdca496f772ca81b3add024e3eddbfa477c58274a8d71cfa87`  
		Last Modified: Fri, 28 Aug 2020 17:28:05 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84cda9aab617bcc558fbfb3a49ed057b804de42c83d33e1c553911217931de9d`  
		Last Modified: Fri, 28 Aug 2020 17:28:16 GMT  
		Size: 49.3 MB (49268849 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a3ed77f8040313fc3f7cbb8e2db7d974cafaae25c274ac2dfef39c897b585a7`  
		Last Modified: Fri, 28 Aug 2020 17:28:05 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a91f5e57d0848b57f04493dbc2342ea2da93cc068b6a4953c510325f37fc5a7e`  
		Last Modified: Fri, 28 Aug 2020 17:28:05 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.4.6` - linux; arm variant v6

```console
$ docker pull vault@sha256:09927f9a9b4887a75582ab3dfe851e9c705cb4a8a78b0ee58b8401f78982cbb0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48714068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5614f05ad1d13eba2ed96805e8c41b1d7ea9bdf3e85c7dd402cb28ea4617080`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:35 GMT
ADD file:ef75120295e25a8e67c5ef378df2cf4ce9f7b83b44709452fcaf247b54fabd16 in / 
# Thu, 23 Apr 2020 15:51:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Aug 2020 18:19:14 GMT
ARG VAULT_VERSION=1.4.6
# Fri, 28 Aug 2020 18:19:18 GMT
# ARGS: VAULT_VERSION=1.4.6
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 28 Aug 2020 18:19:30 GMT
# ARGS: VAULT_VERSION=1.4.6
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 28 Aug 2020 18:19:35 GMT
# ARGS: VAULT_VERSION=1.4.6
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 28 Aug 2020 18:19:36 GMT
VOLUME [/vault/logs]
# Fri, 28 Aug 2020 18:19:37 GMT
VOLUME [/vault/file]
# Fri, 28 Aug 2020 18:19:38 GMT
EXPOSE 8200
# Fri, 28 Aug 2020 18:19:38 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 28 Aug 2020 18:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Aug 2020 18:19:40 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:e745d1dc1c9e0be26166278da7632765ca98fa1be8179a7cc440b3bdc5671860`  
		Last Modified: Thu, 23 Apr 2020 15:52:15 GMT  
		Size: 2.6 MB (2572512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0529c64e3df85d14e404be8c5ebdc5578cd6ad4f705b488f2f7d3f57e7997711`  
		Last Modified: Fri, 28 Aug 2020 18:21:17 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f375b01d6083f30086740a91a2b2072b5af3ab3f02346916f9ed289df11cd1d5`  
		Last Modified: Fri, 28 Aug 2020 18:21:30 GMT  
		Size: 46.1 MB (46138260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4339ac5832f3bd1f5f23856c1452aef4dd8ec0f1ef5839e109a6be28e8e25bd`  
		Last Modified: Fri, 28 Aug 2020 18:21:17 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec03264b3dcb6b98679ef6344f59bb37ff294d5f53dae7325e2e83ad0cf2fe89`  
		Last Modified: Fri, 28 Aug 2020 18:21:17 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.4.6` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:5f95066fb5314a067ece5d9067e5783f9ca874b99df3db7511de44113d2cdd23
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48965579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:272bb7387cd3b3847425294f63f0a55a015396981531d772ca348f8b58c7a485`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:52 GMT
ADD file:75529f7e83edb6d0457a3b8bbfe33d4e3a12f339c5ace517d0f52dbedd9a146b in / 
# Fri, 24 Apr 2020 00:14:53 GMT
CMD ["/bin/sh"]
# Fri, 28 Aug 2020 19:12:04 GMT
ARG VAULT_VERSION=1.4.6
# Fri, 28 Aug 2020 19:12:08 GMT
# ARGS: VAULT_VERSION=1.4.6
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 28 Aug 2020 19:12:20 GMT
# ARGS: VAULT_VERSION=1.4.6
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 28 Aug 2020 19:12:25 GMT
# ARGS: VAULT_VERSION=1.4.6
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 28 Aug 2020 19:12:26 GMT
VOLUME [/vault/logs]
# Fri, 28 Aug 2020 19:12:27 GMT
VOLUME [/vault/file]
# Fri, 28 Aug 2020 19:12:28 GMT
EXPOSE 8200
# Fri, 28 Aug 2020 19:12:30 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 28 Aug 2020 19:12:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Aug 2020 19:12:33 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:b038bcb63e9c8905cc879c957302f686a9b43f24a18dcfc4186ab236ddf04cad`  
		Last Modified: Fri, 24 Apr 2020 00:15:54 GMT  
		Size: 2.7 MB (2718734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b78207c18d7be900e9133e13d8ce5dd9734abebb90de92f0f93935c6fe1b615`  
		Last Modified: Fri, 28 Aug 2020 19:13:57 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f365f5dbccb25a534f56dc48a0488f69fba9173b1081748a438e2076fe9083`  
		Last Modified: Fri, 28 Aug 2020 19:14:08 GMT  
		Size: 46.2 MB (46243547 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c480a4197252eedd4e289d8e6d105e9a76537fc7e7168306311b06dbbb688662`  
		Last Modified: Fri, 28 Aug 2020 19:13:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e53d4286f7e8800ac2bf07eed2fb5a0e83cdb48b4ae9a8a7e8beda156207d96`  
		Last Modified: Fri, 28 Aug 2020 19:13:57 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.4.6` - linux; 386

```console
$ docker pull vault@sha256:8b839c378192a844e3de5f853a7e7248ffde8c219e6e5b6e32d47490ef8528ca
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50208015 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2dadb4d0b4cf5483f8891668d84795b5f6082cc98a200bcb2013d09aa086227a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:11 GMT
ADD file:2e9fb162fdd20e7ac6e9edcb9e1ce9ece750f125c93824c5709a2800ae397f89 in / 
# Thu, 23 Apr 2020 21:16:11 GMT
CMD ["/bin/sh"]
# Fri, 28 Aug 2020 19:52:56 GMT
ARG VAULT_VERSION=1.4.6
# Fri, 28 Aug 2020 19:52:57 GMT
# ARGS: VAULT_VERSION=1.4.6
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 28 Aug 2020 19:53:03 GMT
# ARGS: VAULT_VERSION=1.4.6
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 28 Aug 2020 19:53:04 GMT
# ARGS: VAULT_VERSION=1.4.6
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 28 Aug 2020 19:53:04 GMT
VOLUME [/vault/logs]
# Fri, 28 Aug 2020 19:53:04 GMT
VOLUME [/vault/file]
# Fri, 28 Aug 2020 19:53:04 GMT
EXPOSE 8200
# Fri, 28 Aug 2020 19:53:05 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 28 Aug 2020 19:53:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Aug 2020 19:53:05 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:294658c31053f36b08a64158e37d4fb84478e6fe8f4d5127c51a6334c8a3c36d`  
		Last Modified: Thu, 23 Apr 2020 21:16:37 GMT  
		Size: 2.8 MB (2787128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02e9a686d7b2861e63b60a7d54d8ec5d40a00a51c274f9b6a6cdf39d05daa542`  
		Last Modified: Fri, 28 Aug 2020 19:54:02 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b62e2cd9dc6f94b8d3a9efa3ec556b3a4a55902736cd16b75edbfa4f9842d97b`  
		Last Modified: Fri, 28 Aug 2020 19:54:15 GMT  
		Size: 47.4 MB (47417648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b70bdbd13fbe7c2fe12173740a5e934cd11d80aa6e5be45ee345fa98fcf5a9c4`  
		Last Modified: Fri, 28 Aug 2020 19:54:01 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caea9d4557514eb11709d6e57f445331cc47e8241f6f3999690125ab44e3387d`  
		Last Modified: Fri, 28 Aug 2020 19:54:01 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.5.3`

```console
$ docker pull vault@sha256:14c29a6810974d3611c578509ad9398cadf44e8f6fa354c7d1ced62b5f26d372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.5.3` - linux; amd64

```console
$ docker pull vault@sha256:46d286d2ecfa1e60c463b253966e7184691ceff0ee21fbc0d4b1f204dc1c54bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55005912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac433bb6835d15f5848057eb42c34e349e7416ea14ec2317e5349af68c7163a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 28 Aug 2020 17:26:58 GMT
ARG VAULT_VERSION=1.5.3
# Fri, 28 Aug 2020 17:26:59 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 28 Aug 2020 17:27:04 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 28 Aug 2020 17:27:05 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 28 Aug 2020 17:27:05 GMT
VOLUME [/vault/logs]
# Fri, 28 Aug 2020 17:27:05 GMT
VOLUME [/vault/file]
# Fri, 28 Aug 2020 17:27:06 GMT
EXPOSE 8200
# Fri, 28 Aug 2020 17:27:06 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 28 Aug 2020 17:27:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Aug 2020 17:27:06 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deee0ea5f4ffbbc37e373ae9e9a9149080bbeaad4b7dd78d22b12228f8adb9a1`  
		Last Modified: Fri, 28 Aug 2020 17:27:52 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f2d86291ad1b7fbe95fbc250c00ae60a49fc5a3a4221d1b6068eaa3971ea24`  
		Last Modified: Fri, 28 Aug 2020 17:28:01 GMT  
		Size: 52.2 MB (52207096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1e74570dbfd69f48d2cdbd5c743f40c917987e1673e944d5c654a92da89b9b`  
		Last Modified: Fri, 28 Aug 2020 17:27:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b46ddde9811f65f594c37f5dd93f633dd7bf3accbade1b9400ec3cab8175a7b`  
		Last Modified: Fri, 28 Aug 2020 17:27:52 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.5.3` - linux; arm variant v6

```console
$ docker pull vault@sha256:8cd885e887c8f3486b4d70e373a2254ae3b4a5e7dbab2b3421a2369f1e1209d8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51549568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b543701dba8a513d06cd8ab66a9b938b1763f409845dddc2a8dde6403b6ab4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:35 GMT
ADD file:ef75120295e25a8e67c5ef378df2cf4ce9f7b83b44709452fcaf247b54fabd16 in / 
# Thu, 23 Apr 2020 15:51:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Aug 2020 18:18:41 GMT
ARG VAULT_VERSION=1.5.3
# Fri, 28 Aug 2020 18:18:43 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 28 Aug 2020 18:18:54 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 28 Aug 2020 18:19:00 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 28 Aug 2020 18:19:01 GMT
VOLUME [/vault/logs]
# Fri, 28 Aug 2020 18:19:02 GMT
VOLUME [/vault/file]
# Fri, 28 Aug 2020 18:19:03 GMT
EXPOSE 8200
# Fri, 28 Aug 2020 18:19:03 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 28 Aug 2020 18:19:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Aug 2020 18:19:05 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:e745d1dc1c9e0be26166278da7632765ca98fa1be8179a7cc440b3bdc5671860`  
		Last Modified: Thu, 23 Apr 2020 15:52:15 GMT  
		Size: 2.6 MB (2572512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c6c68999ed968aaacb949550bcbdaa49a7d716b46e7497824c33a7d063360e`  
		Last Modified: Fri, 28 Aug 2020 18:20:57 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7e70b8c80bee94dd4642f4a3dda3b53224a5e10c6af2d7dac81e4071fa9fe4`  
		Last Modified: Fri, 28 Aug 2020 18:21:11 GMT  
		Size: 49.0 MB (48973758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b14e4589266737fa431884053709a0df774b8c90afbc7de54e18738d5d279`  
		Last Modified: Fri, 28 Aug 2020 18:20:56 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2562e85dff964687e2d91fd127b6e3b0bfb91621880af9eb5049eee071093e96`  
		Last Modified: Fri, 28 Aug 2020 18:20:57 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.5.3` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:4b23938a347afe18aff84bd92fd34ef36f31b228d5ffd40aa3d94d12d42b213f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51920459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2615dc2842c24efd1de7b000a7a5483c6d639801ae3015748f4ccc5f65c1248`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:52 GMT
ADD file:75529f7e83edb6d0457a3b8bbfe33d4e3a12f339c5ace517d0f52dbedd9a146b in / 
# Fri, 24 Apr 2020 00:14:53 GMT
CMD ["/bin/sh"]
# Fri, 28 Aug 2020 19:11:27 GMT
ARG VAULT_VERSION=1.5.3
# Fri, 28 Aug 2020 19:11:32 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 28 Aug 2020 19:11:43 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 28 Aug 2020 19:11:49 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 28 Aug 2020 19:11:50 GMT
VOLUME [/vault/logs]
# Fri, 28 Aug 2020 19:11:51 GMT
VOLUME [/vault/file]
# Fri, 28 Aug 2020 19:11:52 GMT
EXPOSE 8200
# Fri, 28 Aug 2020 19:11:53 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 28 Aug 2020 19:11:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Aug 2020 19:11:55 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:b038bcb63e9c8905cc879c957302f686a9b43f24a18dcfc4186ab236ddf04cad`  
		Last Modified: Fri, 24 Apr 2020 00:15:54 GMT  
		Size: 2.7 MB (2718734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97271184b0383fc65dd9a90343785e751af1f9d5b6214380e70a972c95ff1a95`  
		Last Modified: Fri, 28 Aug 2020 19:13:37 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee095d7adc42f79a7e7a8103d57a44da2efd248b0004a241cb75a017a322155`  
		Last Modified: Fri, 28 Aug 2020 19:13:50 GMT  
		Size: 49.2 MB (49198423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a34a358be4e48c13106d56f967e7f9309b983a4f85f2021b30a3a6077c2031`  
		Last Modified: Fri, 28 Aug 2020 19:13:38 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06afae97cef764a4ba18c443009ed46fb48aaece5cc2aa43011da7cbd601f220`  
		Last Modified: Fri, 28 Aug 2020 19:13:37 GMT  
		Size: 1.8 KB (1824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.5.3` - linux; 386

```console
$ docker pull vault@sha256:b14be49027965193d7823ea0dedbcb883315dfdc6b8859b5429289ee22280d82
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53071432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0286e925fd6514133c411776fee67d5d56e1c6fba66de863ec19c1d6e58eea5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:11 GMT
ADD file:2e9fb162fdd20e7ac6e9edcb9e1ce9ece750f125c93824c5709a2800ae397f89 in / 
# Thu, 23 Apr 2020 21:16:11 GMT
CMD ["/bin/sh"]
# Fri, 28 Aug 2020 19:52:41 GMT
ARG VAULT_VERSION=1.5.3
# Fri, 28 Aug 2020 19:52:42 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 28 Aug 2020 19:52:48 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 28 Aug 2020 19:52:49 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 28 Aug 2020 19:52:50 GMT
VOLUME [/vault/logs]
# Fri, 28 Aug 2020 19:52:50 GMT
VOLUME [/vault/file]
# Fri, 28 Aug 2020 19:52:50 GMT
EXPOSE 8200
# Fri, 28 Aug 2020 19:52:50 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 28 Aug 2020 19:52:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Aug 2020 19:52:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:294658c31053f36b08a64158e37d4fb84478e6fe8f4d5127c51a6334c8a3c36d`  
		Last Modified: Thu, 23 Apr 2020 21:16:37 GMT  
		Size: 2.8 MB (2787128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf6e092fa3dd14b502ab1db190e6437d2852050ed457a3b81cfa006318e32d5`  
		Last Modified: Fri, 28 Aug 2020 19:53:45 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08fb7ef11f1e97bc17123c7fda631831c560115511cb51d4db9fd01030b5ae1`  
		Last Modified: Fri, 28 Aug 2020 19:53:57 GMT  
		Size: 50.3 MB (50281066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c457d41e798ca6dc5026dbd62f941e1abb540c7622bda40e34a9c210d4febf5`  
		Last Modified: Fri, 28 Aug 2020 19:53:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28712d4dcd9f6757d4191da8bfe5b5490004ba26fc3a2b79b256a8bfda3e7546`  
		Last Modified: Fri, 28 Aug 2020 19:53:44 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:latest`

```console
$ docker pull vault@sha256:14c29a6810974d3611c578509ad9398cadf44e8f6fa354c7d1ced62b5f26d372
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:46d286d2ecfa1e60c463b253966e7184691ceff0ee21fbc0d4b1f204dc1c54bf
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.0 MB (55005912 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aac433bb6835d15f5848057eb42c34e349e7416ea14ec2317e5349af68c7163a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 28 Aug 2020 17:26:58 GMT
ARG VAULT_VERSION=1.5.3
# Fri, 28 Aug 2020 17:26:59 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 28 Aug 2020 17:27:04 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 28 Aug 2020 17:27:05 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 28 Aug 2020 17:27:05 GMT
VOLUME [/vault/logs]
# Fri, 28 Aug 2020 17:27:05 GMT
VOLUME [/vault/file]
# Fri, 28 Aug 2020 17:27:06 GMT
EXPOSE 8200
# Fri, 28 Aug 2020 17:27:06 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 28 Aug 2020 17:27:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Aug 2020 17:27:06 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deee0ea5f4ffbbc37e373ae9e9a9149080bbeaad4b7dd78d22b12228f8adb9a1`  
		Last Modified: Fri, 28 Aug 2020 17:27:52 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3f2d86291ad1b7fbe95fbc250c00ae60a49fc5a3a4221d1b6068eaa3971ea24`  
		Last Modified: Fri, 28 Aug 2020 17:28:01 GMT  
		Size: 52.2 MB (52207096 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df1e74570dbfd69f48d2cdbd5c743f40c917987e1673e944d5c654a92da89b9b`  
		Last Modified: Fri, 28 Aug 2020 17:27:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b46ddde9811f65f594c37f5dd93f633dd7bf3accbade1b9400ec3cab8175a7b`  
		Last Modified: Fri, 28 Aug 2020 17:27:52 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:8cd885e887c8f3486b4d70e373a2254ae3b4a5e7dbab2b3421a2369f1e1209d8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.5 MB (51549568 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6b543701dba8a513d06cd8ab66a9b938b1763f409845dddc2a8dde6403b6ab4e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:35 GMT
ADD file:ef75120295e25a8e67c5ef378df2cf4ce9f7b83b44709452fcaf247b54fabd16 in / 
# Thu, 23 Apr 2020 15:51:36 GMT
CMD ["/bin/sh"]
# Fri, 28 Aug 2020 18:18:41 GMT
ARG VAULT_VERSION=1.5.3
# Fri, 28 Aug 2020 18:18:43 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 28 Aug 2020 18:18:54 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 28 Aug 2020 18:19:00 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 28 Aug 2020 18:19:01 GMT
VOLUME [/vault/logs]
# Fri, 28 Aug 2020 18:19:02 GMT
VOLUME [/vault/file]
# Fri, 28 Aug 2020 18:19:03 GMT
EXPOSE 8200
# Fri, 28 Aug 2020 18:19:03 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 28 Aug 2020 18:19:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Aug 2020 18:19:05 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:e745d1dc1c9e0be26166278da7632765ca98fa1be8179a7cc440b3bdc5671860`  
		Last Modified: Thu, 23 Apr 2020 15:52:15 GMT  
		Size: 2.6 MB (2572512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15c6c68999ed968aaacb949550bcbdaa49a7d716b46e7497824c33a7d063360e`  
		Last Modified: Fri, 28 Aug 2020 18:20:57 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e7e70b8c80bee94dd4642f4a3dda3b53224a5e10c6af2d7dac81e4071fa9fe4`  
		Last Modified: Fri, 28 Aug 2020 18:21:11 GMT  
		Size: 49.0 MB (48973758 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af8b14e4589266737fa431884053709a0df774b8c90afbc7de54e18738d5d279`  
		Last Modified: Fri, 28 Aug 2020 18:20:56 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2562e85dff964687e2d91fd127b6e3b0bfb91621880af9eb5049eee071093e96`  
		Last Modified: Fri, 28 Aug 2020 18:20:57 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:4b23938a347afe18aff84bd92fd34ef36f31b228d5ffd40aa3d94d12d42b213f
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.9 MB (51920459 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d2615dc2842c24efd1de7b000a7a5483c6d639801ae3015748f4ccc5f65c1248`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:52 GMT
ADD file:75529f7e83edb6d0457a3b8bbfe33d4e3a12f339c5ace517d0f52dbedd9a146b in / 
# Fri, 24 Apr 2020 00:14:53 GMT
CMD ["/bin/sh"]
# Fri, 28 Aug 2020 19:11:27 GMT
ARG VAULT_VERSION=1.5.3
# Fri, 28 Aug 2020 19:11:32 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 28 Aug 2020 19:11:43 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 28 Aug 2020 19:11:49 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 28 Aug 2020 19:11:50 GMT
VOLUME [/vault/logs]
# Fri, 28 Aug 2020 19:11:51 GMT
VOLUME [/vault/file]
# Fri, 28 Aug 2020 19:11:52 GMT
EXPOSE 8200
# Fri, 28 Aug 2020 19:11:53 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 28 Aug 2020 19:11:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Aug 2020 19:11:55 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:b038bcb63e9c8905cc879c957302f686a9b43f24a18dcfc4186ab236ddf04cad`  
		Last Modified: Fri, 24 Apr 2020 00:15:54 GMT  
		Size: 2.7 MB (2718734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97271184b0383fc65dd9a90343785e751af1f9d5b6214380e70a972c95ff1a95`  
		Last Modified: Fri, 28 Aug 2020 19:13:37 GMT  
		Size: 1.3 KB (1289 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ee095d7adc42f79a7e7a8103d57a44da2efd248b0004a241cb75a017a322155`  
		Last Modified: Fri, 28 Aug 2020 19:13:50 GMT  
		Size: 49.2 MB (49198423 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1a34a358be4e48c13106d56f967e7f9309b983a4f85f2021b30a3a6077c2031`  
		Last Modified: Fri, 28 Aug 2020 19:13:38 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06afae97cef764a4ba18c443009ed46fb48aaece5cc2aa43011da7cbd601f220`  
		Last Modified: Fri, 28 Aug 2020 19:13:37 GMT  
		Size: 1.8 KB (1824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:b14be49027965193d7823ea0dedbcb883315dfdc6b8859b5429289ee22280d82
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53071432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0286e925fd6514133c411776fee67d5d56e1c6fba66de863ec19c1d6e58eea5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:11 GMT
ADD file:2e9fb162fdd20e7ac6e9edcb9e1ce9ece750f125c93824c5709a2800ae397f89 in / 
# Thu, 23 Apr 2020 21:16:11 GMT
CMD ["/bin/sh"]
# Fri, 28 Aug 2020 19:52:41 GMT
ARG VAULT_VERSION=1.5.3
# Fri, 28 Aug 2020 19:52:42 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 28 Aug 2020 19:52:48 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 28 Aug 2020 19:52:49 GMT
# ARGS: VAULT_VERSION=1.5.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 28 Aug 2020 19:52:50 GMT
VOLUME [/vault/logs]
# Fri, 28 Aug 2020 19:52:50 GMT
VOLUME [/vault/file]
# Fri, 28 Aug 2020 19:52:50 GMT
EXPOSE 8200
# Fri, 28 Aug 2020 19:52:50 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 28 Aug 2020 19:52:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 28 Aug 2020 19:52:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:294658c31053f36b08a64158e37d4fb84478e6fe8f4d5127c51a6334c8a3c36d`  
		Last Modified: Thu, 23 Apr 2020 21:16:37 GMT  
		Size: 2.8 MB (2787128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3cf6e092fa3dd14b502ab1db190e6437d2852050ed457a3b81cfa006318e32d5`  
		Last Modified: Fri, 28 Aug 2020 19:53:45 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08fb7ef11f1e97bc17123c7fda631831c560115511cb51d4db9fd01030b5ae1`  
		Last Modified: Fri, 28 Aug 2020 19:53:57 GMT  
		Size: 50.3 MB (50281066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c457d41e798ca6dc5026dbd62f941e1abb540c7622bda40e34a9c210d4febf5`  
		Last Modified: Fri, 28 Aug 2020 19:53:45 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28712d4dcd9f6757d4191da8bfe5b5490004ba26fc3a2b79b256a8bfda3e7546`  
		Last Modified: Fri, 28 Aug 2020 19:53:44 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
