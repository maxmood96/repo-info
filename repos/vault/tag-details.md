<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `vault`

-	[`vault:1.5.9`](#vault159)
-	[`vault:1.6.7`](#vault167)
-	[`vault:1.7.5`](#vault175)
-	[`vault:1.8.4`](#vault184)
-	[`vault:latest`](#vaultlatest)

## `vault:1.5.9`

```console
$ docker pull vault@sha256:5c14e115abe0663e76a0029328f5f394030bdb8e9892ee3b42652e4a909af2d3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.5.9` - linux; amd64

```console
$ docker pull vault@sha256:173212142be586a2558b2ff8cf701632c49dcd46cd522c69ff55265258d5bb74
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55101261 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9be2afbafea177c86d7b64ed1ff6882843a7e3d4c6630ee73fcf0af5d066f960`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 31 Aug 2021 23:18:16 GMT
ADD file:ecdfb91a737d6c292265c1b77ffd3d82ba810dd43ea4ef79714b66b1da74a5aa in / 
# Tue, 31 Aug 2021 23:18:16 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 06:17:28 GMT
ARG VAULT_VERSION=1.5.9
# Wed, 01 Sep 2021 06:17:29 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 01 Sep 2021 06:17:38 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 01 Sep 2021 06:17:39 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 01 Sep 2021 06:17:39 GMT
VOLUME [/vault/logs]
# Wed, 01 Sep 2021 06:17:39 GMT
VOLUME [/vault/file]
# Wed, 01 Sep 2021 06:17:39 GMT
EXPOSE 8200
# Wed, 01 Sep 2021 06:17:40 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 06:17:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 06:17:40 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:4e9f2cdf438714c2c4533e28c6c41a89cc6c1b46cf77e54c488db30ca4f5b6f3`  
		Last Modified: Tue, 31 Aug 2021 23:18:55 GMT  
		Size: 2.8 MB (2814079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6aff56fc2a66d6bdeb572825b481b1f259938d30c7986413d03f8ac63de529e`  
		Last Modified: Wed, 01 Sep 2021 06:17:56 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4f81065ca5f94fdf96731590daeaf8625fe6d2ea5400126d45786af2ddc2389d`  
		Last Modified: Wed, 01 Sep 2021 06:18:04 GMT  
		Size: 52.3 MB (52283917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6ec1ddb9f38f190ec9c39107d0be9b4c858b4393f22a66ddba652cb4acb6088`  
		Last Modified: Wed, 01 Sep 2021 06:17:57 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9dcfeccf207be3e2d11842039700746f151e2b4ad65f253f23141b4517e4e6`  
		Last Modified: Wed, 01 Sep 2021 06:17:56 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.5.9` - linux; arm variant v6

```console
$ docker pull vault@sha256:4cfcea87ecabed6cd3ccf97ee3a3d0e5703cba0270996945a32aa417e4e4ce75
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51678088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e96b2c38c3c2127ca6c4e2487bc683075a0be6a2dceeddcc2e6fe6e50e6d5ea`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 31 Aug 2021 22:30:33 GMT
ADD file:ed2b5e0fbd1e7ae37ab8f808c827d23c6841ce1edd7427552d5bf741d67ebcc0 in / 
# Tue, 31 Aug 2021 22:30:33 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 07:07:21 GMT
ARG VAULT_VERSION=1.5.9
# Wed, 01 Sep 2021 07:07:23 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 01 Sep 2021 07:07:44 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 01 Sep 2021 07:07:46 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 01 Sep 2021 07:07:46 GMT
VOLUME [/vault/logs]
# Wed, 01 Sep 2021 07:07:47 GMT
VOLUME [/vault/file]
# Wed, 01 Sep 2021 07:07:47 GMT
EXPOSE 8200
# Wed, 01 Sep 2021 07:07:48 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 07:07:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 07:07:49 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:840d18d84f6afdc3231d126fdd3f84f23f0335b61cbfa9cb8808b888a4308919`  
		Last Modified: Tue, 31 Aug 2021 22:32:11 GMT  
		Size: 2.6 MB (2623761 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2107291f0e709da064928dd447aaf165be6a0b712b651e5b0ff0b609cdc65033`  
		Last Modified: Wed, 01 Sep 2021 07:08:29 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e401f7fbd59182ba7d9c0e35d40dd847288edfde0971c0c319361381898fa02b`  
		Last Modified: Wed, 01 Sep 2021 07:08:55 GMT  
		Size: 49.1 MB (49051063 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ede0959067494ad5fe9751f205afaff5a47b89e34d43f96406aca555547edd04`  
		Last Modified: Wed, 01 Sep 2021 07:08:29 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3f48e0dfa7371c6003bc8fb359287257b9f6f941a2932ff196dbf0c6765ab3`  
		Last Modified: Wed, 01 Sep 2021 07:08:29 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.5.9` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:5c7da6e9f0e0be128791488a81f3bb4cb386d498fedb07c012308242f64a309a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51981485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:efd758eda9d38a7e22dab74280d97abf4d88a78584befb12d0c56c2092dd3057`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 15:21:57 GMT
ARG VAULT_VERSION=1.5.9
# Wed, 01 Sep 2021 15:21:58 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 01 Sep 2021 15:22:11 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 01 Sep 2021 15:22:12 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 01 Sep 2021 15:22:12 GMT
VOLUME [/vault/logs]
# Wed, 01 Sep 2021 15:22:12 GMT
VOLUME [/vault/file]
# Wed, 01 Sep 2021 15:22:13 GMT
EXPOSE 8200
# Wed, 01 Sep 2021 15:22:13 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 15:22:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 15:22:13 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a69615552dc7e07cf7daeca634a5553eae4d36ca94fc0cee88872940f758559`  
		Last Modified: Wed, 01 Sep 2021 15:22:39 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be976a139b9997a7e7cd04a9ecdbf1602ab4a2006bdeae813d3c191b08fda241`  
		Last Modified: Wed, 01 Sep 2021 15:22:46 GMT  
		Size: 49.3 MB (49265211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05a36c855fe11a18eb102fd36acc375f6363283954c5c14ea9d1f889be59a3ed`  
		Last Modified: Wed, 01 Sep 2021 15:22:39 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d797221c93433e245a71c4b3367566756a54e3fa8bc8623226af389fb3b7d339`  
		Last Modified: Wed, 01 Sep 2021 15:22:39 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.5.9` - linux; 386

```console
$ docker pull vault@sha256:8eda22213ebaa53d0da65d60aa5d165fb15d5ef50d0b75b7746c83751bd6a062
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53174898 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56ed990de33c2864ce228635346696542eb4a96fedc8c641fde94dcd874495cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 31 Aug 2021 21:23:28 GMT
ADD file:fb9d541cffc3a5660d23426ba847aa696b59a9d7f14e00ba0a63b28c9ec272c0 in / 
# Tue, 31 Aug 2021 21:23:29 GMT
CMD ["/bin/sh"]
# Wed, 01 Sep 2021 03:08:38 GMT
ARG VAULT_VERSION=1.5.9
# Wed, 01 Sep 2021 03:08:39 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 01 Sep 2021 03:08:49 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 01 Sep 2021 03:08:51 GMT
# ARGS: VAULT_VERSION=1.5.9
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 01 Sep 2021 03:08:51 GMT
VOLUME [/vault/logs]
# Wed, 01 Sep 2021 03:08:51 GMT
VOLUME [/vault/file]
# Wed, 01 Sep 2021 03:08:52 GMT
EXPOSE 8200
# Wed, 01 Sep 2021 03:08:52 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 01 Sep 2021 03:08:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 01 Sep 2021 03:08:52 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:4ed7d06bd90bc8d13b87220ccc6204a7d235ec943be9fb4289d856f9ff0a5b7b`  
		Last Modified: Tue, 31 Aug 2021 21:24:28 GMT  
		Size: 2.8 MB (2821095 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:523ce25561ac0325674e64884dc7c4eb1cb6c4aa1147eee148249b2983cc1718`  
		Last Modified: Wed, 01 Sep 2021 03:09:16 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:585e9123868f1da6989289e30eeac6d3d3aae86e5bec1a20b184128ba2d3d206`  
		Last Modified: Wed, 01 Sep 2021 03:09:24 GMT  
		Size: 50.4 MB (50350539 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bd4b9ddbe59055723675960178d1e9604bf23b4079b9d11caa540fe35663293`  
		Last Modified: Wed, 01 Sep 2021 03:09:16 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:682e0037c325651603faa67fa8ff2cb19b175402882ebd9747a5bbf95954085f`  
		Last Modified: Wed, 01 Sep 2021 03:09:16 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.6.7`

```console
$ docker pull vault@sha256:8116fe8e4fcf4e44d4f845420a4d811e02046dd2793dd0e6241dcb49a3c34510
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.6.7` - linux; amd64

```console
$ docker pull vault@sha256:2d8756c6fca35d543fc46fd80053e0796f324df3d1bdca531067a9d3d4b3d498
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69116075 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac3dd301251a36c603611e32e0e3bb70efd1674f536f5f589fd61bc447e22ecd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 29 Sep 2021 23:21:28 GMT
ARG VAULT_VERSION=1.6.7
# Wed, 29 Sep 2021 23:21:29 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 29 Sep 2021 23:21:38 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 29 Sep 2021 23:21:39 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 29 Sep 2021 23:21:39 GMT
VOLUME [/vault/logs]
# Wed, 29 Sep 2021 23:21:39 GMT
VOLUME [/vault/file]
# Wed, 29 Sep 2021 23:21:40 GMT
EXPOSE 8200
# Wed, 29 Sep 2021 23:21:40 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Sep 2021 23:21:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Sep 2021 23:21:40 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c809dc7df9d461752a3095819fbc3b8b6aa86cd941ac83b88d80bf6302c9e08e`  
		Last Modified: Wed, 29 Sep 2021 23:22:30 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc277f62c9d01426a993bc060c1f619915558d1184993d042f3a608ec805778`  
		Last Modified: Wed, 29 Sep 2021 23:22:39 GMT  
		Size: 66.3 MB (66298355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a5a556b4be5c34f8d1c1ea7cace44793c58e0533b33d7c4d8026aa1c18de8d83`  
		Last Modified: Wed, 29 Sep 2021 23:22:30 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b617bd7d7c1e1e40d6948ddbfbbb58c6d865bdaa4011a3d698acbed28095621`  
		Last Modified: Wed, 29 Sep 2021 23:22:30 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.6.7` - linux; arm variant v6

```console
$ docker pull vault@sha256:6ba577725b49717624ac4f44b226f3db46328b1b11b10c10a5f8b8c0420a41e4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63848880 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85eaef2d95593c47b92f33af01aaf89af9c3b0fa530b7b5168318c44dd477b1e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Sep 2021 00:03:22 GMT
ARG VAULT_VERSION=1.6.7
# Thu, 30 Sep 2021 00:03:23 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 30 Sep 2021 00:03:43 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 30 Sep 2021 00:03:45 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 30 Sep 2021 00:03:46 GMT
VOLUME [/vault/logs]
# Thu, 30 Sep 2021 00:03:46 GMT
VOLUME [/vault/file]
# Thu, 30 Sep 2021 00:03:47 GMT
EXPOSE 8200
# Thu, 30 Sep 2021 00:03:47 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 30 Sep 2021 00:03:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Sep 2021 00:03:48 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:841a4942881c001052d328110df75e1bcb3b7363bb805dc2d15fdc42b17607a7`  
		Last Modified: Thu, 30 Sep 2021 00:05:55 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2a97fa1cf3cee6494775f48aefbb72d289524609329fe55743edbaf4e9a9e9`  
		Last Modified: Thu, 30 Sep 2021 00:06:28 GMT  
		Size: 61.2 MB (61218158 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a4e30d4882c25b3f0f4b9c21bfd2489227f87460a1e1b3f8a8ee23e3a7b5631`  
		Last Modified: Thu, 30 Sep 2021 00:05:55 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:906676deb9c98b785d3d7a69d2710a0628a143fcd0570bfeb6b941b603afc1b8`  
		Last Modified: Thu, 30 Sep 2021 00:05:55 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.6.7` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:f8bf88d9eb6d4a67a57d3d11578062465bbef60e0d6a2b3fc2b704585f425561
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65138248 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3d0911adade516abdba290d0114c10336a6642495a265dc55fad9b6cdb9b32a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 29 Sep 2021 23:41:07 GMT
ARG VAULT_VERSION=1.6.7
# Wed, 29 Sep 2021 23:41:08 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 29 Sep 2021 23:41:15 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 29 Sep 2021 23:41:16 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 29 Sep 2021 23:41:16 GMT
VOLUME [/vault/logs]
# Wed, 29 Sep 2021 23:41:16 GMT
VOLUME [/vault/file]
# Wed, 29 Sep 2021 23:41:16 GMT
EXPOSE 8200
# Wed, 29 Sep 2021 23:41:17 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Sep 2021 23:41:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Sep 2021 23:41:17 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9768bab26359e676c87ff027a78ba73ec51e18a8d883fc8f66c43a2a9db2586a`  
		Last Modified: Wed, 29 Sep 2021 23:42:15 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24d674ecd800138c4722fce65a7adc958a2143d8e7f173a9f7c41d07a5218935`  
		Last Modified: Wed, 29 Sep 2021 23:42:23 GMT  
		Size: 62.4 MB (62423144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518668c8a9dffe1dff8c728cea81d641e65b487c85d0d1faa8146a2cdaa72fd2`  
		Last Modified: Wed, 29 Sep 2021 23:42:15 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f65af9f691afd8a964e1b18710ac477d2840ffb48fe32572dfe8d83254f399d`  
		Last Modified: Wed, 29 Sep 2021 23:42:15 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.6.7` - linux; 386

```console
$ docker pull vault@sha256:1c56b5514265b60a121b4c77c6dc267ea204072a4e6d2b052f83b281e6679f8c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67159779 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8dbc816bfa42ff48fcad8de858da4569b9f64dc206d57fabfda78e4be80e6840`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:38:29 GMT
ADD file:42a7bc5a08b546b47049dd0f89ae4e7a8c86342f87000f39ade3ff52916a6c2e in / 
# Fri, 27 Aug 2021 17:38:30 GMT
CMD ["/bin/sh"]
# Wed, 29 Sep 2021 23:39:41 GMT
ARG VAULT_VERSION=1.6.7
# Wed, 29 Sep 2021 23:39:42 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 29 Sep 2021 23:39:52 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 29 Sep 2021 23:39:53 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 29 Sep 2021 23:39:53 GMT
VOLUME [/vault/logs]
# Wed, 29 Sep 2021 23:39:54 GMT
VOLUME [/vault/file]
# Wed, 29 Sep 2021 23:39:54 GMT
EXPOSE 8200
# Wed, 29 Sep 2021 23:39:54 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Sep 2021 23:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Sep 2021 23:39:54 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:b11ae9fc5d8a106cfed3a6f6c75e5b5b5797c566fac4411622b4055df6541286`  
		Last Modified: Fri, 27 Aug 2021 17:39:18 GMT  
		Size: 2.8 MB (2822857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb9d6d62fe7297dc5d2afe3f092caa978a15ffbfe1511f859ecffc2453c0e983`  
		Last Modified: Wed, 29 Sep 2021 23:40:55 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1158f36614fe9f0c66bf4a63fd5f9257520f7432259fb0ff96c5dd65662bc9e`  
		Last Modified: Wed, 29 Sep 2021 23:41:05 GMT  
		Size: 64.3 MB (64333646 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aff394e2c20767d90f6b3222beee1ca5fa7689d94d1342d3d3745ee4110b01a3`  
		Last Modified: Wed, 29 Sep 2021 23:40:55 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:779a32e6f3cbab4b35f2ce12af48da75260fb5ecf388087a29ea5fa36ea74de9`  
		Last Modified: Wed, 29 Sep 2021 23:40:56 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.7.5`

```console
$ docker pull vault@sha256:aae7ec843318b90ae9257637d6b90215863675c6c7968d3c02e78640592e9b5d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.7.5` - linux; amd64

```console
$ docker pull vault@sha256:bff1a692def49176d3cca4f343c3fd5397cf2a4fc6a13a68aece01056fc872ff
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.0 MB (74019314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:20f06c604e6ee2df719ec10d003d66582821cd2fea7c64cd4244866e906f5cbb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 29 Sep 2021 23:21:13 GMT
ARG VAULT_VERSION=1.7.5
# Wed, 29 Sep 2021 23:21:14 GMT
# ARGS: VAULT_VERSION=1.7.5
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 29 Sep 2021 23:21:23 GMT
# ARGS: VAULT_VERSION=1.7.5
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 29 Sep 2021 23:21:24 GMT
# ARGS: VAULT_VERSION=1.7.5
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 29 Sep 2021 23:21:25 GMT
VOLUME [/vault/logs]
# Wed, 29 Sep 2021 23:21:25 GMT
VOLUME [/vault/file]
# Wed, 29 Sep 2021 23:21:25 GMT
EXPOSE 8200
# Wed, 29 Sep 2021 23:21:25 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Sep 2021 23:21:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Sep 2021 23:21:26 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d14e3004401f8c3589847e4f2cde6660f82b080f452c3655333ef1ce7fb4cb15`  
		Last Modified: Wed, 29 Sep 2021 23:22:14 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9c7a7a510d4cef0c9d563a07e4b89eb812b4634c911411902e5c892033e469b`  
		Last Modified: Wed, 29 Sep 2021 23:22:23 GMT  
		Size: 71.2 MB (71201588 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0346bcbdcec5dfcc8607f695b07ba29d196224fe73a44626cc1fe3b7ff46cec2`  
		Last Modified: Wed, 29 Sep 2021 23:22:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d03541e4691b01661949d5d01dde72966eb713cba646a9d893a85dc53c4333df`  
		Last Modified: Wed, 29 Sep 2021 23:22:14 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.5` - linux; arm variant v6

```console
$ docker pull vault@sha256:eeea98f9652e0f0128f41ff10871bb2e2b3f07e9121e7b633c74ba84cf0203a3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.8 MB (67840566 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:19f894a10e6097f7008a5a184f3acd013a86a1f336e06ddee1a3d55127416906`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Thu, 30 Sep 2021 00:02:40 GMT
ARG VAULT_VERSION=1.7.5
# Thu, 30 Sep 2021 00:02:41 GMT
# ARGS: VAULT_VERSION=1.7.5
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 30 Sep 2021 00:03:05 GMT
# ARGS: VAULT_VERSION=1.7.5
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 30 Sep 2021 00:03:07 GMT
# ARGS: VAULT_VERSION=1.7.5
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 30 Sep 2021 00:03:07 GMT
VOLUME [/vault/logs]
# Thu, 30 Sep 2021 00:03:08 GMT
VOLUME [/vault/file]
# Thu, 30 Sep 2021 00:03:08 GMT
EXPOSE 8200
# Thu, 30 Sep 2021 00:03:08 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 30 Sep 2021 00:03:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Sep 2021 00:03:09 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93282f8d256ccac74657511720fb031f9aa2450e3f9c7540aca0a5c784059300`  
		Last Modified: Thu, 30 Sep 2021 00:05:14 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4e8aeb9ffaeff9bf6f9046076d8c1679187f6311b24a6ae964ef1527e6d8fb1`  
		Last Modified: Thu, 30 Sep 2021 00:05:47 GMT  
		Size: 65.2 MB (65209839 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dae2b5f220755a908d0417b439722bf9d2ebbf0b2092c1740065551c91a9ba5b`  
		Last Modified: Thu, 30 Sep 2021 00:05:14 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90ad88b5fcb8edc71c4441fc2809fd39af1d09851ae2fb6cbab4821434eae4cb`  
		Last Modified: Thu, 30 Sep 2021 00:05:14 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.5` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:ec0f662a71fc70d4c29f023fcac292c4831383bfe7716c3263e028fe4cc838cd
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.8 MB (69775451 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ba93c081cabf181385211d3a30826e5f93124fb628d51bbc65b1b42b8f71895`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 29 Sep 2021 23:40:50 GMT
ARG VAULT_VERSION=1.7.5
# Wed, 29 Sep 2021 23:40:51 GMT
# ARGS: VAULT_VERSION=1.7.5
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 29 Sep 2021 23:40:59 GMT
# ARGS: VAULT_VERSION=1.7.5
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 29 Sep 2021 23:41:00 GMT
# ARGS: VAULT_VERSION=1.7.5
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 29 Sep 2021 23:41:01 GMT
VOLUME [/vault/logs]
# Wed, 29 Sep 2021 23:41:01 GMT
VOLUME [/vault/file]
# Wed, 29 Sep 2021 23:41:01 GMT
EXPOSE 8200
# Wed, 29 Sep 2021 23:41:01 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Sep 2021 23:41:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Sep 2021 23:41:02 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78a3a342333fddeb45acf5797d89b55acdf4ec6ffc2a030972afc497252fb21f`  
		Last Modified: Wed, 29 Sep 2021 23:41:58 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3db626f56b03320d9d56b66167107269537d746d3b6cb037a65c72c4f0c263af`  
		Last Modified: Wed, 29 Sep 2021 23:42:07 GMT  
		Size: 67.1 MB (67060349 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2941e00646e261374db402d565e3a10c44d236b69bfe89a4109ffa7e704247d4`  
		Last Modified: Wed, 29 Sep 2021 23:41:58 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ad13d6b32d645a6c6d78bb5f44c5193d6c0e60092386077db7d5400491e5d19`  
		Last Modified: Wed, 29 Sep 2021 23:41:57 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.5` - linux; 386

```console
$ docker pull vault@sha256:0fd52a64f482451a2f757602eab157c1df8eccb5b3e6d4fa8cd85517149261a0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **71.9 MB (71860263 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2617a5371b65f3c1f6cd46ee40ec5740a9b1ebc17d5c83e0d7645f94b4912756`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:38:29 GMT
ADD file:42a7bc5a08b546b47049dd0f89ae4e7a8c86342f87000f39ade3ff52916a6c2e in / 
# Fri, 27 Aug 2021 17:38:30 GMT
CMD ["/bin/sh"]
# Wed, 29 Sep 2021 23:39:22 GMT
ARG VAULT_VERSION=1.7.5
# Wed, 29 Sep 2021 23:39:23 GMT
# ARGS: VAULT_VERSION=1.7.5
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 29 Sep 2021 23:39:32 GMT
# ARGS: VAULT_VERSION=1.7.5
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 29 Sep 2021 23:39:33 GMT
# ARGS: VAULT_VERSION=1.7.5
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 29 Sep 2021 23:39:34 GMT
VOLUME [/vault/logs]
# Wed, 29 Sep 2021 23:39:34 GMT
VOLUME [/vault/file]
# Wed, 29 Sep 2021 23:39:34 GMT
EXPOSE 8200
# Wed, 29 Sep 2021 23:39:34 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 29 Sep 2021 23:39:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 29 Sep 2021 23:39:35 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:b11ae9fc5d8a106cfed3a6f6c75e5b5b5797c566fac4411622b4055df6541286`  
		Last Modified: Fri, 27 Aug 2021 17:39:18 GMT  
		Size: 2.8 MB (2822857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f25ed6da7489b6da2545dd6ebefc65fa56e1e38caf65b77cddf89af38775c15b`  
		Last Modified: Wed, 29 Sep 2021 23:40:38 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624f200a3384a6d117c3bb3a6875aa1909b1317b9deb439476b57e31063fd495`  
		Last Modified: Wed, 29 Sep 2021 23:40:48 GMT  
		Size: 69.0 MB (69034131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eeefe3ffb35b7c52936b246e98bae003e63565603577d8762f870a2343a513b`  
		Last Modified: Wed, 29 Sep 2021 23:40:38 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:baaf7afa48d954a2167a388853c868768a510a93a8a05ca607a929afca3e62d6`  
		Last Modified: Wed, 29 Sep 2021 23:40:38 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.8.4`

```console
$ docker pull vault@sha256:a75b8996586ddaf57866c3e89fc1fadcecbb8c2b85dc6fb70e3613674d771161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.8.4` - linux; amd64

```console
$ docker pull vault@sha256:b98869b86956112ea98ee1ae4dfa5574841e9972b952fd14164b3cf2b654c311
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70536212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc15db720d794cf9b1e24f2e9e07794d8a48d1aa3241bd12503088613c273624`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 06 Oct 2021 22:20:55 GMT
ARG VAULT_VERSION=1.8.4
# Wed, 06 Oct 2021 22:20:55 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 06 Oct 2021 22:21:07 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 06 Oct 2021 22:21:09 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 06 Oct 2021 22:21:09 GMT
VOLUME [/vault/logs]
# Wed, 06 Oct 2021 22:21:09 GMT
VOLUME [/vault/file]
# Wed, 06 Oct 2021 22:21:09 GMT
EXPOSE 8200
# Wed, 06 Oct 2021 22:21:09 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 06 Oct 2021 22:21:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Oct 2021 22:21:10 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a0b2a356fb97c26c3888e6b65e634f0af19ec5858a2344272d1b87c8e02111`  
		Last Modified: Wed, 06 Oct 2021 22:21:28 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acd76c99acf20e737c7b03f1a834c465c09d1dbd99c8ade96290c4b373e1e90`  
		Last Modified: Wed, 06 Oct 2021 22:21:37 GMT  
		Size: 67.7 MB (67718488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a97b985888087de353b7f7fe93cb50be2e95b706384e683810af72445bd9c69`  
		Last Modified: Wed, 06 Oct 2021 22:21:28 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd6c1e6597ed862cbb5c7f0fa3f5f07b33663ff61cf3c55313aacf64afbe2bf`  
		Last Modified: Wed, 06 Oct 2021 22:21:28 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.8.4` - linux; arm variant v6

```console
$ docker pull vault@sha256:989065ca9f6334c558e67ff6a3366536efdc9176018ba9bb27e5a7d33f111712
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64891610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5371dcb3996108bd1fc4ef8d740fed712af691992b9dde4eb1156bd131f607cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Wed, 06 Oct 2021 22:02:09 GMT
ARG VAULT_VERSION=1.8.4
# Wed, 06 Oct 2021 22:02:10 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 06 Oct 2021 22:02:34 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 06 Oct 2021 22:02:36 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 06 Oct 2021 22:02:37 GMT
VOLUME [/vault/logs]
# Wed, 06 Oct 2021 22:02:37 GMT
VOLUME [/vault/file]
# Wed, 06 Oct 2021 22:02:38 GMT
EXPOSE 8200
# Wed, 06 Oct 2021 22:02:38 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 06 Oct 2021 22:02:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Oct 2021 22:02:39 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5fcf9b2802305a79ef85aaf0fcab4c55bf2ef968bef4ad8dd3ced1aebc2d11`  
		Last Modified: Wed, 06 Oct 2021 22:03:37 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6be599b2e6bd3541209874bf6d7aace11d371dc892c686a07c3cb03361d65c`  
		Last Modified: Wed, 06 Oct 2021 22:04:10 GMT  
		Size: 62.3 MB (62260889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7936e9ffeca20a2d874e2e18bb168a78522f6a76ed776d9db7fef08028b58006`  
		Last Modified: Wed, 06 Oct 2021 22:03:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4965a11b47a390c3a0e65ae43aece8b3b7a2576f823dc7c9447bd32c2c45ffe6`  
		Last Modified: Wed, 06 Oct 2021 22:03:37 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.8.4` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:393f19c5bf721b16ac8ce6af0069ed43b5390b25e7e66edcefbaf750bc5e862d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66795822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed257a1f0ebad8f36b6b087c9b8c303eb0ded006cc18b998624e9a855882e4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 06 Oct 2021 23:43:52 GMT
ARG VAULT_VERSION=1.8.4
# Wed, 06 Oct 2021 23:43:53 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 06 Oct 2021 23:44:08 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 06 Oct 2021 23:44:09 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 06 Oct 2021 23:44:09 GMT
VOLUME [/vault/logs]
# Wed, 06 Oct 2021 23:44:10 GMT
VOLUME [/vault/file]
# Wed, 06 Oct 2021 23:44:10 GMT
EXPOSE 8200
# Wed, 06 Oct 2021 23:44:10 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 06 Oct 2021 23:44:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Oct 2021 23:44:10 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465855d633a2005eb2e71345743f5a64caabe56471c026734ae763a5131e9fc7`  
		Last Modified: Wed, 06 Oct 2021 23:44:42 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a10f7a2125af14df20d5ce7a24dd3e6e18356b84b7fe05cba9b388dfe35b46`  
		Last Modified: Wed, 06 Oct 2021 23:44:51 GMT  
		Size: 64.1 MB (64080715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1182c975f3af5dda004a703f1158f8b8bf43666c39098d32622096807a17637c`  
		Last Modified: Wed, 06 Oct 2021 23:44:42 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f50aef442c3db2d5c72b08d7d89ee8a2a80e48d6935202af274aacf46172c00`  
		Last Modified: Wed, 06 Oct 2021 23:44:42 GMT  
		Size: 1.8 KB (1824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.8.4` - linux; 386

```console
$ docker pull vault@sha256:7aabaea7c095411d0175c419ae2b02192969fddf64dd921a46562e8f678ccb2f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68250749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a1a17c0d9280087ade640342a45d552c9d5a50d2ec0d61560f4649dff0f59b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:38:29 GMT
ADD file:42a7bc5a08b546b47049dd0f89ae4e7a8c86342f87000f39ade3ff52916a6c2e in / 
# Fri, 27 Aug 2021 17:38:30 GMT
CMD ["/bin/sh"]
# Wed, 06 Oct 2021 21:39:02 GMT
ARG VAULT_VERSION=1.8.4
# Wed, 06 Oct 2021 21:39:03 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 06 Oct 2021 21:39:19 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 06 Oct 2021 21:39:20 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 06 Oct 2021 21:39:21 GMT
VOLUME [/vault/logs]
# Wed, 06 Oct 2021 21:39:21 GMT
VOLUME [/vault/file]
# Wed, 06 Oct 2021 21:39:21 GMT
EXPOSE 8200
# Wed, 06 Oct 2021 21:39:22 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 06 Oct 2021 21:39:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Oct 2021 21:39:22 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:b11ae9fc5d8a106cfed3a6f6c75e5b5b5797c566fac4411622b4055df6541286`  
		Last Modified: Fri, 27 Aug 2021 17:39:18 GMT  
		Size: 2.8 MB (2822857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a90621346841424613ab1f005e94f30ca2d5cdc83f952f00f2c228774b5a9e`  
		Last Modified: Wed, 06 Oct 2021 21:39:54 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae41f0482d51ff1bf741ea90ac88a27292b52a207e7835f41aa0c3b103f15658`  
		Last Modified: Wed, 06 Oct 2021 21:40:04 GMT  
		Size: 65.4 MB (65424614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1463a499a206c971b3958e089750333ce64de8dbf79f0e67426eb7fe4f2446`  
		Last Modified: Wed, 06 Oct 2021 21:39:54 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f360b5634a04aae373d70ee4722dd0b93fe20d47b88a23f7107297b9e6eb09fb`  
		Last Modified: Wed, 06 Oct 2021 21:39:54 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:latest`

```console
$ docker pull vault@sha256:a75b8996586ddaf57866c3e89fc1fadcecbb8c2b85dc6fb70e3613674d771161
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:b98869b86956112ea98ee1ae4dfa5574841e9972b952fd14164b3cf2b654c311
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.5 MB (70536212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc15db720d794cf9b1e24f2e9e07794d8a48d1aa3241bd12503088613c273624`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:19:45 GMT
ADD file:aad4290d27580cc1a094ffaf98c3ca2fc5d699fe695dfb8e6e9fac20f1129450 in / 
# Fri, 27 Aug 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Wed, 06 Oct 2021 22:20:55 GMT
ARG VAULT_VERSION=1.8.4
# Wed, 06 Oct 2021 22:20:55 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 06 Oct 2021 22:21:07 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 06 Oct 2021 22:21:09 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 06 Oct 2021 22:21:09 GMT
VOLUME [/vault/logs]
# Wed, 06 Oct 2021 22:21:09 GMT
VOLUME [/vault/file]
# Wed, 06 Oct 2021 22:21:09 GMT
EXPOSE 8200
# Wed, 06 Oct 2021 22:21:09 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 06 Oct 2021 22:21:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Oct 2021 22:21:10 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:a0d0a0d46f8b52473982a3c466318f479767577551a53ffc9074c9fa7035982e`  
		Last Modified: Fri, 27 Aug 2021 17:20:13 GMT  
		Size: 2.8 MB (2814446 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1a0b2a356fb97c26c3888e6b65e634f0af19ec5858a2344272d1b87c8e02111`  
		Last Modified: Wed, 06 Oct 2021 22:21:28 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7acd76c99acf20e737c7b03f1a834c465c09d1dbd99c8ade96290c4b373e1e90`  
		Last Modified: Wed, 06 Oct 2021 22:21:37 GMT  
		Size: 67.7 MB (67718488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2a97b985888087de353b7f7fe93cb50be2e95b706384e683810af72445bd9c69`  
		Last Modified: Wed, 06 Oct 2021 22:21:28 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7fd6c1e6597ed862cbb5c7f0fa3f5f07b33663ff61cf3c55313aacf64afbe2bf`  
		Last Modified: Wed, 06 Oct 2021 22:21:28 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:989065ca9f6334c558e67ff6a3366536efdc9176018ba9bb27e5a7d33f111712
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64891610 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5371dcb3996108bd1fc4ef8d740fed712af691992b9dde4eb1156bd131f607cb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:49:29 GMT
ADD file:1c1c4520d49cb6e8f795f3b953d1ed3c3c77868b98b53a455169c254fcec5acd in / 
# Fri, 27 Aug 2021 17:49:30 GMT
CMD ["/bin/sh"]
# Wed, 06 Oct 2021 22:02:09 GMT
ARG VAULT_VERSION=1.8.4
# Wed, 06 Oct 2021 22:02:10 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 06 Oct 2021 22:02:34 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 06 Oct 2021 22:02:36 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 06 Oct 2021 22:02:37 GMT
VOLUME [/vault/logs]
# Wed, 06 Oct 2021 22:02:37 GMT
VOLUME [/vault/file]
# Wed, 06 Oct 2021 22:02:38 GMT
EXPOSE 8200
# Wed, 06 Oct 2021 22:02:38 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 06 Oct 2021 22:02:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Oct 2021 22:02:39 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:2e78c0f86ba9a1fed30df20cb48c9cc73e9626399f12749d36b892ff99c0ecf5`  
		Last Modified: Fri, 27 Aug 2021 17:50:55 GMT  
		Size: 2.6 MB (2627447 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab5fcf9b2802305a79ef85aaf0fcab4c55bf2ef968bef4ad8dd3ced1aebc2d11`  
		Last Modified: Wed, 06 Oct 2021 22:03:37 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b6be599b2e6bd3541209874bf6d7aace11d371dc892c686a07c3cb03361d65c`  
		Last Modified: Wed, 06 Oct 2021 22:04:10 GMT  
		Size: 62.3 MB (62260889 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7936e9ffeca20a2d874e2e18bb168a78522f6a76ed776d9db7fef08028b58006`  
		Last Modified: Wed, 06 Oct 2021 22:03:37 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4965a11b47a390c3a0e65ae43aece8b3b7a2576f823dc7c9447bd32c2c45ffe6`  
		Last Modified: Wed, 06 Oct 2021 22:03:37 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:393f19c5bf721b16ac8ce6af0069ed43b5390b25e7e66edcefbaf750bc5e862d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.8 MB (66795822 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2ed257a1f0ebad8f36b6b087c9b8c303eb0ded006cc18b998624e9a855882e4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:39:33 GMT
ADD file:dc8af9c7bfe9f9541e1db38dea01c4201609f3075b31e108f2073ffed8c5e4b9 in / 
# Fri, 27 Aug 2021 17:39:33 GMT
CMD ["/bin/sh"]
# Wed, 06 Oct 2021 23:43:52 GMT
ARG VAULT_VERSION=1.8.4
# Wed, 06 Oct 2021 23:43:53 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 06 Oct 2021 23:44:08 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 06 Oct 2021 23:44:09 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 06 Oct 2021 23:44:09 GMT
VOLUME [/vault/logs]
# Wed, 06 Oct 2021 23:44:10 GMT
VOLUME [/vault/file]
# Wed, 06 Oct 2021 23:44:10 GMT
EXPOSE 8200
# Wed, 06 Oct 2021 23:44:10 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 06 Oct 2021 23:44:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Oct 2021 23:44:10 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:552d1f2373af9bfe12033568ebbfb0ccbb0de11279f9a415a29207e264d7f4d9`  
		Last Modified: Fri, 27 Aug 2021 17:40:18 GMT  
		Size: 2.7 MB (2711827 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:465855d633a2005eb2e71345743f5a64caabe56471c026734ae763a5131e9fc7`  
		Last Modified: Wed, 06 Oct 2021 23:44:42 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8a10f7a2125af14df20d5ce7a24dd3e6e18356b84b7fe05cba9b388dfe35b46`  
		Last Modified: Wed, 06 Oct 2021 23:44:51 GMT  
		Size: 64.1 MB (64080715 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1182c975f3af5dda004a703f1158f8b8bf43666c39098d32622096807a17637c`  
		Last Modified: Wed, 06 Oct 2021 23:44:42 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f50aef442c3db2d5c72b08d7d89ee8a2a80e48d6935202af274aacf46172c00`  
		Last Modified: Wed, 06 Oct 2021 23:44:42 GMT  
		Size: 1.8 KB (1824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:7aabaea7c095411d0175c419ae2b02192969fddf64dd921a46562e8f678ccb2f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.3 MB (68250749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:03a1a17c0d9280087ade640342a45d552c9d5a50d2ec0d61560f4649dff0f59b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 27 Aug 2021 17:38:29 GMT
ADD file:42a7bc5a08b546b47049dd0f89ae4e7a8c86342f87000f39ade3ff52916a6c2e in / 
# Fri, 27 Aug 2021 17:38:30 GMT
CMD ["/bin/sh"]
# Wed, 06 Oct 2021 21:39:02 GMT
ARG VAULT_VERSION=1.8.4
# Wed, 06 Oct 2021 21:39:03 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 06 Oct 2021 21:39:19 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 06 Oct 2021 21:39:20 GMT
# ARGS: VAULT_VERSION=1.8.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 06 Oct 2021 21:39:21 GMT
VOLUME [/vault/logs]
# Wed, 06 Oct 2021 21:39:21 GMT
VOLUME [/vault/file]
# Wed, 06 Oct 2021 21:39:21 GMT
EXPOSE 8200
# Wed, 06 Oct 2021 21:39:22 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 06 Oct 2021 21:39:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 06 Oct 2021 21:39:22 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:b11ae9fc5d8a106cfed3a6f6c75e5b5b5797c566fac4411622b4055df6541286`  
		Last Modified: Fri, 27 Aug 2021 17:39:18 GMT  
		Size: 2.8 MB (2822857 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67a90621346841424613ab1f005e94f30ca2d5cdc83f952f00f2c228774b5a9e`  
		Last Modified: Wed, 06 Oct 2021 21:39:54 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae41f0482d51ff1bf741ea90ac88a27292b52a207e7835f41aa0c3b103f15658`  
		Last Modified: Wed, 06 Oct 2021 21:40:04 GMT  
		Size: 65.4 MB (65424614 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1463a499a206c971b3958e089750333ce64de8dbf79f0e67426eb7fe4f2446`  
		Last Modified: Wed, 06 Oct 2021 21:39:54 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f360b5634a04aae373d70ee4722dd0b93fe20d47b88a23f7107297b9e6eb09fb`  
		Last Modified: Wed, 06 Oct 2021 21:39:54 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
