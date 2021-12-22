<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `vault`

-	[`vault:1.6.7`](#vault167)
-	[`vault:1.7.8`](#vault178)
-	[`vault:1.8.7`](#vault187)
-	[`vault:1.9.2`](#vault192)
-	[`vault:latest`](#vaultlatest)

## `vault:1.6.7`

```console
$ docker pull vault@sha256:dcfe67d671880c5153f6ab135ec36a3ab98a3f412c890eb551b1443e5b18da9b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.6.7` - linux; amd64

```console
$ docker pull vault@sha256:769e4cdeeb80e60b64be43783670b59eca416e42c9c5cb184e9d1b505c70dd8a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69121489 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:becb85347e6688c9bc15931bdf41748d9d12109b8c0ead7e29289ff0a09c45a5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 11:12:51 GMT
ARG VAULT_VERSION=1.6.7
# Sat, 13 Nov 2021 11:12:52 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN addgroup vault &&     adduser -S -G vault vault
# Sat, 13 Nov 2021 11:12:59 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Sat, 13 Nov 2021 11:13:00 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Sat, 13 Nov 2021 11:13:00 GMT
VOLUME [/vault/logs]
# Sat, 13 Nov 2021 11:13:00 GMT
VOLUME [/vault/file]
# Sat, 13 Nov 2021 11:13:01 GMT
EXPOSE 8200
# Sat, 13 Nov 2021 11:13:01 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Nov 2021 11:13:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 11:13:01 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:afaffc7ab46f2e497d3fb4e21a99a803da7d654be027e36819fa6f6c1c9e68fb`  
		Last Modified: Sat, 13 Nov 2021 11:14:19 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d934042901383baf557fcb244d4883cacb82e94e53e22071768422a6181192b`  
		Last Modified: Sat, 13 Nov 2021 11:14:28 GMT  
		Size: 66.3 MB (66295235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b98d7be0c6c8866d70de848c0e68b133ccd24844a508c5c0a79c9105a7b2337`  
		Last Modified: Sat, 13 Nov 2021 11:14:19 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24fafcbd97f1dab71c56fd8e24b30e816d46d3d3202b64b9f977fea9c88978b`  
		Last Modified: Sat, 13 Nov 2021 11:14:19 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.6.7` - linux; arm variant v6

```console
$ docker pull vault@sha256:524d99d3f73246fb85d3956ffdaf38c9ac8849dc4fa0ba874738d16dedc33183
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.9 MB (63853498 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4eee87097f71ffdac45b773de6ddd2aa95dd6b52b1ac0376428ef6b40203a18b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:46:42 GMT
ARG VAULT_VERSION=1.6.7
# Sat, 13 Nov 2021 06:46:46 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN addgroup vault &&     adduser -S -G vault vault
# Sat, 13 Nov 2021 06:47:05 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Sat, 13 Nov 2021 06:47:10 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Sat, 13 Nov 2021 06:47:10 GMT
VOLUME [/vault/logs]
# Sat, 13 Nov 2021 06:47:12 GMT
VOLUME [/vault/file]
# Sat, 13 Nov 2021 06:47:13 GMT
EXPOSE 8200
# Sat, 13 Nov 2021 06:47:14 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Nov 2021 06:47:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 06:47:15 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf07e0c178c265c14436ade2f994d8bce9a650a2b903083fd332697ada637be`  
		Last Modified: Sat, 13 Nov 2021 06:50:13 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a25890671871c62dbcd9511dd45731941a32275c161a9c1a0d9ca57a79f57c22`  
		Last Modified: Sat, 13 Nov 2021 06:50:33 GMT  
		Size: 61.2 MB (61214831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a0966e2693f83897cd8eae486972ef1437b6d73e7c7482b9f2e8e6dfccee197`  
		Last Modified: Sat, 13 Nov 2021 06:50:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f49a35b52f2c6bf2170c927ae58b3266d8b8b5b51fbd26970c0d841b3262f39`  
		Last Modified: Sat, 13 Nov 2021 06:50:13 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.6.7` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:8840b7d40be013e9cdab9d2d3fd7be773c393b7fc54d9397b31685079acb82f9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65140796 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33d1a77203679f54ddf4caeae615c322f45566c862584011b5cadf9a71440381`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 18:13:56 GMT
ARG VAULT_VERSION=1.6.7
# Fri, 12 Nov 2021 18:13:57 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 12 Nov 2021 18:14:06 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 12 Nov 2021 18:14:06 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 12 Nov 2021 18:14:07 GMT
VOLUME [/vault/logs]
# Fri, 12 Nov 2021 18:14:08 GMT
VOLUME [/vault/file]
# Fri, 12 Nov 2021 18:14:09 GMT
EXPOSE 8200
# Fri, 12 Nov 2021 18:14:11 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 18:14:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 18:14:12 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3935f9db61a7b34b1919b3b80256bba49848c270324a2bd588211470b1dff16e`  
		Last Modified: Fri, 12 Nov 2021 18:15:45 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8dff2b8919eb42c25188a65f6e57a79078ba59cd83d05523de7da486c63a194`  
		Last Modified: Fri, 12 Nov 2021 18:15:54 GMT  
		Size: 62.4 MB (62419882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2280cedd357aedae89538f83f73221c1532723e29e2b1238ea78213a11f5797`  
		Last Modified: Fri, 12 Nov 2021 18:15:46 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c647a93f11944fbcdebdbd789ed54da45d27b7bfe5d5b610986a0e5800a9dc18`  
		Last Modified: Fri, 12 Nov 2021 18:15:45 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.6.7` - linux; 386

```console
$ docker pull vault@sha256:967f16406d097d62460fbc18b68cb72d2a722ae1a772b97ee851af7970662ba7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.2 MB (67164972 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8f64270dc212452748714f3e270f2e08ed6fdaef36b141351bc4a050fa213460`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:42 GMT
ADD file:403428c2903dd9dea10d069185873cb2c2c3149c553797807c69f22aa3d12fe3 in / 
# Fri, 12 Nov 2021 16:38:42 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 17:32:53 GMT
ARG VAULT_VERSION=1.6.7
# Fri, 12 Nov 2021 17:32:54 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 12 Nov 2021 17:33:11 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 12 Nov 2021 17:33:13 GMT
# ARGS: VAULT_VERSION=1.6.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 12 Nov 2021 17:33:13 GMT
VOLUME [/vault/logs]
# Fri, 12 Nov 2021 17:33:14 GMT
VOLUME [/vault/file]
# Fri, 12 Nov 2021 17:33:14 GMT
EXPOSE 8200
# Fri, 12 Nov 2021 17:33:14 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 17:33:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 17:33:15 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:5420e0d28c84ecb16748cb90cc6acf8e2a81dab10cb1f674f3eee8533e53c62a`  
		Last Modified: Fri, 12 Nov 2021 16:39:36 GMT  
		Size: 2.8 MB (2830948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5687af1e758a81cb56968feabeb4df42f60ba6f22267571b48e04f30c8b669`  
		Last Modified: Fri, 12 Nov 2021 17:35:38 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e6d591c10a0632df92caf56171ceda32aea7eaf3cf2605bbb78b4958e868552`  
		Last Modified: Fri, 12 Nov 2021 17:35:53 GMT  
		Size: 64.3 MB (64330751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926a723f3932c401b81e4a0896005dd52ff449a3fcd29f2ca4b10d842f48d9c2`  
		Last Modified: Fri, 12 Nov 2021 17:35:38 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280f02b1aec09a9f6bba587e771bafcad59c851053c9f0fa1963b5d0413dc981`  
		Last Modified: Fri, 12 Nov 2021 17:35:38 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.7.8`

```console
$ docker pull vault@sha256:f5d7e01d95d0e0d5cd8d2b87a9bb3d094a1128c60113286c78a707d77fead1d9
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm variant v6

### `vault:1.7.8` - linux; arm variant v6

```console
$ docker pull vault@sha256:69a3805cbf808c9aa2b8d60b6417a93173a2a5157b487e48421d2c44f7a762a9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **62.9 MB (62870632 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca7ef1e3aadefd6516e5c8c2a8da223d4ae170bb00013025514dc3521423c9b7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Wed, 22 Dec 2021 18:53:31 GMT
ARG VAULT_VERSION=1.7.8
# Wed, 22 Dec 2021 18:53:33 GMT
# ARGS: VAULT_VERSION=1.7.8
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 22 Dec 2021 18:53:54 GMT
# ARGS: VAULT_VERSION=1.7.8
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 22 Dec 2021 18:53:56 GMT
# ARGS: VAULT_VERSION=1.7.8
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 22 Dec 2021 18:53:57 GMT
VOLUME [/vault/logs]
# Wed, 22 Dec 2021 18:53:57 GMT
VOLUME [/vault/file]
# Wed, 22 Dec 2021 18:53:57 GMT
EXPOSE 8200
# Wed, 22 Dec 2021 18:53:58 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Dec 2021 18:53:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Dec 2021 18:53:59 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d0adcb6de320f9bbc16e1483ee9b57f4a15476beff0cb4c9183e1936d297044`  
		Last Modified: Wed, 22 Dec 2021 18:56:01 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78359d04791c737043581aadd1464e81403b2502d5e8c31b66f0c49f2486b2a4`  
		Last Modified: Wed, 22 Dec 2021 18:56:31 GMT  
		Size: 60.2 MB (60231961 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bab1b9250e548a667000b23c12f5e96ce6f7eb389e78e3a911c3aa530af27f81`  
		Last Modified: Wed, 22 Dec 2021 18:56:01 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0255ce4cf462c28cbadc00e5fbcb60e3380a343f070e5b7de01f78e69e212381`  
		Last Modified: Wed, 22 Dec 2021 18:56:01 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.8.7`

```console
$ docker pull vault@sha256:65f23eaf96a8085a0765f6989270d61de10bce7ccc144d0c0ea0e1fbb94b48f6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm variant v6

### `vault:1.8.7` - linux; arm variant v6

```console
$ docker pull vault@sha256:d06188ed1cc33531d8e87b260c6e807522920673b8742474f440a8ab25d06d6d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **64.9 MB (64945329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:374d09249f327b0e4e5fac6998bbbb78ef7fa1ee35293aa18dd2e6621ab7595b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Wed, 22 Dec 2021 18:52:52 GMT
ARG VAULT_VERSION=1.8.7
# Wed, 22 Dec 2021 18:52:54 GMT
# ARGS: VAULT_VERSION=1.8.7
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 22 Dec 2021 18:53:16 GMT
# ARGS: VAULT_VERSION=1.8.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 22 Dec 2021 18:53:18 GMT
# ARGS: VAULT_VERSION=1.8.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 22 Dec 2021 18:53:19 GMT
VOLUME [/vault/logs]
# Wed, 22 Dec 2021 18:53:19 GMT
VOLUME [/vault/file]
# Wed, 22 Dec 2021 18:53:19 GMT
EXPOSE 8200
# Wed, 22 Dec 2021 18:53:20 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Dec 2021 18:53:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Dec 2021 18:53:21 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe9f6137f34f978c8aaa242b7b2b4d34b82867aa2ea75c8a2aac2ff07e901c38`  
		Last Modified: Wed, 22 Dec 2021 18:55:23 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18ac03000e5fb89485810d5f9c1c6bc67e66a2dc9c37a98311c899f9b7dbb49f`  
		Last Modified: Wed, 22 Dec 2021 18:55:53 GMT  
		Size: 62.3 MB (62306657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:751503ece84a110522b2806a652eae62461e994cf882c191a3d6719852cef2c4`  
		Last Modified: Wed, 22 Dec 2021 18:55:23 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7130722044028a7bb4a8520667a2af0b439b34fbf020b1b5b9168d9cc790f6ca`  
		Last Modified: Wed, 22 Dec 2021 18:55:23 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.9.2`

```console
$ docker pull vault@sha256:0bfbf2ba8b82a9f2012d44a144d5d36aa50f233d3fb7b2d288bf0de5861fce9c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 1
	-	linux; arm variant v6

### `vault:1.9.2` - linux; arm variant v6

```console
$ docker pull vault@sha256:76b197761a6bf77dfb6940f47db781306b0e4a99bfe395ca4669ff664bbb5291
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66295841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ba640002891c65168c01e7a6e1b8cec7febed127e265b4379ef85cbc7c9916`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Wed, 22 Dec 2021 18:52:08 GMT
ARG VAULT_VERSION=1.9.2
# Wed, 22 Dec 2021 18:52:10 GMT
# ARGS: VAULT_VERSION=1.9.2
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 22 Dec 2021 18:52:33 GMT
# ARGS: VAULT_VERSION=1.9.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 22 Dec 2021 18:52:36 GMT
# ARGS: VAULT_VERSION=1.9.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 22 Dec 2021 18:52:36 GMT
VOLUME [/vault/logs]
# Wed, 22 Dec 2021 18:52:37 GMT
VOLUME [/vault/file]
# Wed, 22 Dec 2021 18:52:37 GMT
EXPOSE 8200
# Wed, 22 Dec 2021 18:52:38 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Dec 2021 18:52:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Dec 2021 18:52:39 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5fbd7bbaabf55cbd282ff7af64151efb458e0edee017c68d7bdf7766677e4e`  
		Last Modified: Wed, 22 Dec 2021 18:54:39 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e9009a848717349f1d6242a89736d2b8073aa576394471f6aa24d964989fa3`  
		Last Modified: Wed, 22 Dec 2021 18:55:11 GMT  
		Size: 63.7 MB (63657167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51995fc39f8fc00b85e75f5783bfaf923f5b06eefedadfb2adb76b66abe3777`  
		Last Modified: Wed, 22 Dec 2021 18:54:39 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021ac818a2ef8ca123fcea90c7a99d831184f6304756725821e2df1dd7f3fc15`  
		Last Modified: Wed, 22 Dec 2021 18:54:38 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:latest`

```console
$ docker pull vault@sha256:20a01586b75c862755a389c9a503022892c973644f23936a9e074b843c1c6384
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:b7ef561ec7465fb621972b53a0066ccc047b3795d65288b128d5d171d69241c9
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.9 MB (72927265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:86e4a044afe8e1129dd37f99814a5c9f5a8356e34800aa8f3122360accbcdc6c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:44 GMT
ADD file:762c899ec0505d1a32930ee804c5b008825f41611161be104076cba33b7e5b2b in / 
# Fri, 12 Nov 2021 17:19:45 GMT
CMD ["/bin/sh"]
# Mon, 13 Dec 2021 19:44:26 GMT
ARG VAULT_VERSION=1.9.1
# Mon, 13 Dec 2021 19:44:27 GMT
# ARGS: VAULT_VERSION=1.9.1
RUN addgroup vault &&     adduser -S -G vault vault
# Mon, 13 Dec 2021 19:44:35 GMT
# ARGS: VAULT_VERSION=1.9.1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Mon, 13 Dec 2021 19:44:36 GMT
# ARGS: VAULT_VERSION=1.9.1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Mon, 13 Dec 2021 19:44:36 GMT
VOLUME [/vault/logs]
# Mon, 13 Dec 2021 19:44:36 GMT
VOLUME [/vault/file]
# Mon, 13 Dec 2021 19:44:36 GMT
EXPOSE 8200
# Mon, 13 Dec 2021 19:44:37 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 13 Dec 2021 19:44:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Dec 2021 19:44:37 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:97518928ae5f3d52d4164b314a7e73654eb686ecd8aafa0b79acd980773a740d`  
		Last Modified: Fri, 12 Nov 2021 17:20:39 GMT  
		Size: 2.8 MB (2822981 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c8134eb28c5f76c18ff8dcbdc1e7bcf3f85c537f483544c3a94a55f81b5eb4a`  
		Last Modified: Mon, 13 Dec 2021 19:45:15 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3eca4491f3cbd3c9676950d3d96163cc5e9ce9c391c6cd8b457f413609e789fe`  
		Last Modified: Mon, 13 Dec 2021 19:45:24 GMT  
		Size: 70.1 MB (70101008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2eb32be767320ece833a678270d78dee72ec32c0faf108ba02d9029127b7f088`  
		Last Modified: Mon, 13 Dec 2021 19:45:15 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df14db3151b7ff2bc993aa0e2f89b9e341f9514820aaef788ea98fafbd989521`  
		Last Modified: Mon, 13 Dec 2021 19:45:15 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:76b197761a6bf77dfb6940f47db781306b0e4a99bfe395ca4669ff664bbb5291
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.3 MB (66295841 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f1ba640002891c65168c01e7a6e1b8cec7febed127e265b4379ef85cbc7c9916`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:42 GMT
ADD file:6daf1fe862c00673bf9cf4d7e20b0bf253a56e7fb8ed5e730a4466ab9186e18a in / 
# Fri, 12 Nov 2021 16:49:44 GMT
CMD ["/bin/sh"]
# Wed, 22 Dec 2021 18:52:08 GMT
ARG VAULT_VERSION=1.9.2
# Wed, 22 Dec 2021 18:52:10 GMT
# ARGS: VAULT_VERSION=1.9.2
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 22 Dec 2021 18:52:33 GMT
# ARGS: VAULT_VERSION=1.9.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 22 Dec 2021 18:52:36 GMT
# ARGS: VAULT_VERSION=1.9.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 22 Dec 2021 18:52:36 GMT
VOLUME [/vault/logs]
# Wed, 22 Dec 2021 18:52:37 GMT
VOLUME [/vault/file]
# Wed, 22 Dec 2021 18:52:37 GMT
EXPOSE 8200
# Wed, 22 Dec 2021 18:52:38 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Dec 2021 18:52:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Dec 2021 18:52:39 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:56afcfda5d78cc243287acbaad250c5e8c0f47aae620dd7c51985b0d3c9b2728`  
		Last Modified: Fri, 12 Nov 2021 16:51:32 GMT  
		Size: 2.6 MB (2635392 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5fbd7bbaabf55cbd282ff7af64151efb458e0edee017c68d7bdf7766677e4e`  
		Last Modified: Wed, 22 Dec 2021 18:54:39 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05e9009a848717349f1d6242a89736d2b8073aa576394471f6aa24d964989fa3`  
		Last Modified: Wed, 22 Dec 2021 18:55:11 GMT  
		Size: 63.7 MB (63657167 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c51995fc39f8fc00b85e75f5783bfaf923f5b06eefedadfb2adb76b66abe3777`  
		Last Modified: Wed, 22 Dec 2021 18:54:39 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021ac818a2ef8ca123fcea90c7a99d831184f6304756725821e2df1dd7f3fc15`  
		Last Modified: Wed, 22 Dec 2021 18:54:38 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:037de4d08a744892ed0fa746782de38c145b24ef71c82dcba0d51142f55f6c8f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.0 MB (68033485 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91a38ab4113a7298132be393d4f8e2a17848ee2ed01927e61191c801e54cacb9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 16:39:58 GMT
ADD file:400c0466b29ccad54e0f6c0acef22542992828678c96693ef1f9f4d0551935d8 in / 
# Fri, 12 Nov 2021 16:39:58 GMT
CMD ["/bin/sh"]
# Mon, 13 Dec 2021 19:44:01 GMT
ARG VAULT_VERSION=1.9.1
# Mon, 13 Dec 2021 19:44:02 GMT
# ARGS: VAULT_VERSION=1.9.1
RUN addgroup vault &&     adduser -S -G vault vault
# Mon, 13 Dec 2021 19:44:15 GMT
# ARGS: VAULT_VERSION=1.9.1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Mon, 13 Dec 2021 19:44:16 GMT
# ARGS: VAULT_VERSION=1.9.1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Mon, 13 Dec 2021 19:44:17 GMT
VOLUME [/vault/logs]
# Mon, 13 Dec 2021 19:44:18 GMT
VOLUME [/vault/file]
# Mon, 13 Dec 2021 19:44:19 GMT
EXPOSE 8200
# Mon, 13 Dec 2021 19:44:21 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 13 Dec 2021 19:44:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Dec 2021 19:44:22 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:be307f383ecc62b27a29b599c3fc9d3129693a798e7fcce614f09174cfe2d354`  
		Last Modified: Fri, 12 Nov 2021 16:40:59 GMT  
		Size: 2.7 MB (2717700 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d11eb70e5cb277241306401f60d51199681773b711ddcf6a8d55d870ed1d49bb`  
		Last Modified: Mon, 13 Dec 2021 19:45:31 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:db74ee04d55839a0644ef31e98a1751c9e6360dece887fa5ef69445cec6b627a`  
		Last Modified: Mon, 13 Dec 2021 19:45:40 GMT  
		Size: 65.3 MB (65312571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3988615defc2738bc46a7968d1c0fbbdbc8f7462ae2c913589a0a448fdfb78a0`  
		Last Modified: Mon, 13 Dec 2021 19:45:31 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0a19cc4948163cab7dd49e1cde6533b7908c655ff607d48a2a794b1a44ac995`  
		Last Modified: Mon, 13 Dec 2021 19:45:31 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:0bf5f661b65e4cc7a00576bcd597d39983255b24b72ba2b567d2068e825b1063
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.3 MB (69319106 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6c523b34cd9fb0d6c0cf354cc2ce1a8cc320d857f7e264b7cd9acd286959a54e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:42 GMT
ADD file:403428c2903dd9dea10d069185873cb2c2c3149c553797807c69f22aa3d12fe3 in / 
# Fri, 12 Nov 2021 16:38:42 GMT
CMD ["/bin/sh"]
# Mon, 13 Dec 2021 19:41:42 GMT
ARG VAULT_VERSION=1.9.1
# Mon, 13 Dec 2021 19:41:43 GMT
# ARGS: VAULT_VERSION=1.9.1
RUN addgroup vault &&     adduser -S -G vault vault
# Mon, 13 Dec 2021 19:41:58 GMT
# ARGS: VAULT_VERSION=1.9.1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Mon, 13 Dec 2021 19:42:00 GMT
# ARGS: VAULT_VERSION=1.9.1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Mon, 13 Dec 2021 19:42:00 GMT
VOLUME [/vault/logs]
# Mon, 13 Dec 2021 19:42:00 GMT
VOLUME [/vault/file]
# Mon, 13 Dec 2021 19:42:01 GMT
EXPOSE 8200
# Mon, 13 Dec 2021 19:42:01 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 13 Dec 2021 19:42:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Dec 2021 19:42:01 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:5420e0d28c84ecb16748cb90cc6acf8e2a81dab10cb1f674f3eee8533e53c62a`  
		Last Modified: Fri, 12 Nov 2021 16:39:36 GMT  
		Size: 2.8 MB (2830948 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429e272a33341697e8b434bd6da811e08fdd827dc60ed6921b085b2a3e294a67`  
		Last Modified: Mon, 13 Dec 2021 19:43:10 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00c4aae10f8128807aa28ad4acf1916e26f95852080e26efc3534b538926f333`  
		Last Modified: Mon, 13 Dec 2021 19:43:22 GMT  
		Size: 66.5 MB (66484877 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1260e81fa2498903b32934e4c729fd789a4a11a5087089735d0475288ad31eb4`  
		Last Modified: Mon, 13 Dec 2021 19:43:10 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:84dc82fda0e2c0e7147133cec27d5ae83cf59436ce05cea1ab1bad2ecfd2224c`  
		Last Modified: Mon, 13 Dec 2021 19:43:10 GMT  
		Size: 1.8 KB (1825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
