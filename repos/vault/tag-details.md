<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `vault`

-	[`vault:1.10.11`](#vault11011)
-	[`vault:1.11.8`](#vault1118)
-	[`vault:1.12.4`](#vault1124)
-	[`vault:1.13.0`](#vault1130)
-	[`vault:latest`](#vaultlatest)

## `vault:1.10.11`

```console
$ docker pull vault@sha256:bac73136096f177d95254d25b25d28d717aa1a9b1b84a7fb706eae04c36de721
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.10.11` - linux; amd64

```console
$ docker pull vault@sha256:75d3f21a85bf56090b6618f69b5f5f26e28ba53a4143600304d7a45d801505db
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **85.3 MB (85316786 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b809bc2115c80c225ea47c43f07497ad2ad7df8d518646409ec94da84f7cf92d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:37 GMT
ADD file:9663235f252e072c52b0f9e25845841e4321cce2caa7467a0d736c6003b05c00 in / 
# Wed, 29 Mar 2023 18:19:37 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 02:09:40 GMT
ARG VAULT_VERSION=1.10.11
# Thu, 30 Mar 2023 02:09:40 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 30 Mar 2023 02:09:48 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 30 Mar 2023 02:09:49 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 30 Mar 2023 02:09:49 GMT
VOLUME [/vault/logs]
# Thu, 30 Mar 2023 02:09:49 GMT
VOLUME [/vault/file]
# Thu, 30 Mar 2023 02:09:49 GMT
EXPOSE 8200
# Thu, 30 Mar 2023 02:09:49 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 30 Mar 2023 02:09:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Mar 2023 02:09:49 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f7dab3ab2d6ec29aa28769bec35331fb485b5837501b1e8556413d8b5a79c9c8`  
		Last Modified: Wed, 29 Mar 2023 18:20:25 GMT  
		Size: 2.8 MB (2829647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a595cb706262d9ad4495290dbbee803e36483e0f8b0d65ed7294857e83cc7230`  
		Last Modified: Thu, 30 Mar 2023 02:10:44 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:95f98402efd4abc517916cab9d37d4dffa310fbe5493f03d4ed76141d33224c1`  
		Last Modified: Thu, 30 Mar 2023 02:10:53 GMT  
		Size: 82.5 MB (82483870 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42f0e2518f957cd7642dfae1aa486be2529cdde2144a32377280e87c7aa19daf`  
		Last Modified: Thu, 30 Mar 2023 02:10:45 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1adb5c23e4fa3350eb9c6b0956847253ad627f414d46c568e710f5098ec3da47`  
		Last Modified: Thu, 30 Mar 2023 02:10:44 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.10.11` - linux; arm variant v6

```console
$ docker pull vault@sha256:c0bc3eb3a1d74d2aa9646a7a384e7cf33372cbbe11666af766774f0576936684
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80432548 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a6692dd8a60216d409f9083c8c99fdf5a31e404d286b5b22e78825cea555d6e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:54 GMT
ADD file:767f6566ea2c075838c0a86ca644a37e446f309f68952f5f921970f046abd252 in / 
# Mon, 13 Mar 2023 16:12:54 GMT
CMD ["/bin/sh"]
# Tue, 14 Mar 2023 01:08:41 GMT
ARG VAULT_VERSION=1.10.11
# Tue, 14 Mar 2023 01:08:41 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 14 Mar 2023 01:08:53 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 14 Mar 2023 01:08:54 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 14 Mar 2023 01:08:54 GMT
VOLUME [/vault/logs]
# Tue, 14 Mar 2023 01:08:55 GMT
VOLUME [/vault/file]
# Tue, 14 Mar 2023 01:08:55 GMT
EXPOSE 8200
# Tue, 14 Mar 2023 01:08:55 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Mar 2023 01:08:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Mar 2023 01:08:55 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:7616dd32f4bf5fddffb2543afaac2355a5fc495348c01060cd67181e36343e96`  
		Last Modified: Fri, 10 Feb 2023 20:51:02 GMT  
		Size: 2.6 MB (2638152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bdaaa39af3ebd4e1a2c1e5e0f8fada532af76d318d6161fae9fd0e7246121191`  
		Last Modified: Tue, 14 Mar 2023 01:10:05 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b08063982b0590d14369ed26f4efecfef7f4dd33f08084b41e559e3c00d3b87`  
		Last Modified: Tue, 14 Mar 2023 01:10:14 GMT  
		Size: 77.8 MB (77791122 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92edc7727091255b10786215f6929512c5b4e9e92e29fa98e0d11104aa9d8a9e`  
		Last Modified: Tue, 14 Mar 2023 01:10:05 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc23da6b390f420b4b8f5d7dadf227fd775353d56887d3d42277ab0ff6ecb24c`  
		Last Modified: Tue, 14 Mar 2023 01:10:05 GMT  
		Size: 1.8 KB (1817 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.10.11` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:6d1232a24f83e2c2949997d041c16ea60ee2ce6a802c1dc08c816206dc146167
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80434734 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a474b176348a003fb273f7261c4e749bd2fde7f8ce8e8eaa6fb72b17169f648f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:19 GMT
ADD file:50a841463966858f1c3ca87143cf96145d1d52f7349ef516adfbf21cdd5684fe in / 
# Fri, 10 Feb 2023 21:24:19 GMT
CMD ["/bin/sh"]
# Tue, 07 Mar 2023 19:09:46 GMT
ARG VAULT_VERSION=1.10.11
# Tue, 07 Mar 2023 19:09:46 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 07 Mar 2023 19:09:54 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 07 Mar 2023 19:09:55 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 07 Mar 2023 19:09:55 GMT
VOLUME [/vault/logs]
# Tue, 07 Mar 2023 19:09:55 GMT
VOLUME [/vault/file]
# Tue, 07 Mar 2023 19:09:56 GMT
EXPOSE 8200
# Tue, 07 Mar 2023 19:09:56 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 07 Mar 2023 19:09:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Mar 2023 19:09:56 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:6f0e733d82e26042c603e231c39b56abbabdad66673a736ec71c69c65be95f41`  
		Last Modified: Fri, 10 Feb 2023 21:25:10 GMT  
		Size: 2.7 MB (2725026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44ba9a505a0f659279d8049035e0ff108d1340213e969f6dd0818781716c165`  
		Last Modified: Tue, 07 Mar 2023 19:10:52 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b59af14bcd07b86195c54d7ae9da5c31a8d3a1718efb68d984e938a9701f1121`  
		Last Modified: Tue, 07 Mar 2023 19:10:59 GMT  
		Size: 77.7 MB (77706439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63462dfb1b8b8be55ed24ac22ab9dccc86dea8d7b7dcd62d26d5b54e8a568ed6`  
		Last Modified: Tue, 07 Mar 2023 19:10:52 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1208d54a4f2d428f5602837373373d22d0d03c404a160863e54f250084361a14`  
		Last Modified: Tue, 07 Mar 2023 19:10:52 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.10.11` - linux; 386

```console
$ docker pull vault@sha256:5e4beab006468875f48feed52015fd23cd6fb5b6861a478ef8f5223177210af3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.1 MB (82076916 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c374289237b520251a9f980537c841e6b0dbf8219f3e61f2fb9f51873cc7c388`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:38 GMT
ADD file:0fbd9a88e784719a5d50377c069ea125f9a27568d6d02b43a9512c65ae72870d in / 
# Wed, 29 Mar 2023 17:38:39 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 01:40:02 GMT
ARG VAULT_VERSION=1.10.11
# Thu, 30 Mar 2023 01:40:03 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 30 Mar 2023 01:40:12 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 30 Mar 2023 01:40:14 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 30 Mar 2023 01:40:14 GMT
VOLUME [/vault/logs]
# Thu, 30 Mar 2023 01:40:14 GMT
VOLUME [/vault/file]
# Thu, 30 Mar 2023 01:40:14 GMT
EXPOSE 8200
# Thu, 30 Mar 2023 01:40:14 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 30 Mar 2023 01:40:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Mar 2023 01:40:14 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ebcdc7813a6f23dca055a9257561eabd5fc5c5c21d7a72bb208439bd92f47f70`  
		Last Modified: Wed, 29 Mar 2023 17:39:28 GMT  
		Size: 2.8 MB (2835200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa6b106cb9fa6d8655cfc1069b3cca334dc0e00866a45c769f0183009174685c`  
		Last Modified: Thu, 30 Mar 2023 01:41:15 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8617e2641ad7e45255e4cc0c48c0bd042ad1ff40559be20734eeb89f946a8b34`  
		Last Modified: Thu, 30 Mar 2023 01:41:27 GMT  
		Size: 79.2 MB (79238453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:130e603b6b6e6cf25d315c89244a3ab01f64e41665e7e68e1aba80d08f0be7b8`  
		Last Modified: Thu, 30 Mar 2023 01:41:15 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb234f1b29d32a5d33e570a1afcd3d171d020dae3141cba4e212943052eae796`  
		Last Modified: Thu, 30 Mar 2023 01:41:15 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.11.8`

```console
$ docker pull vault@sha256:6157956a11d93926f9244e801fb06bb9babb345372dc8e08420b6d9559bfe1b6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.11.8` - linux; amd64

```console
$ docker pull vault@sha256:98efc61800e497aa77b6e370980b0caecbb27b9ec77b52656b150fabfd704a0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81257687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:89a6ef58bbd5af21ce5e0b3714c6b0977a06ded66c3330209020a0b50ca11324`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:37 GMT
ADD file:9663235f252e072c52b0f9e25845841e4321cce2caa7467a0d736c6003b05c00 in / 
# Wed, 29 Mar 2023 18:19:37 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 02:09:28 GMT
ARG VAULT_VERSION=1.11.8
# Thu, 30 Mar 2023 02:09:29 GMT
# ARGS: VAULT_VERSION=1.11.8
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 30 Mar 2023 02:09:36 GMT
# ARGS: VAULT_VERSION=1.11.8
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 30 Mar 2023 02:09:37 GMT
# ARGS: VAULT_VERSION=1.11.8
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 30 Mar 2023 02:09:37 GMT
VOLUME [/vault/logs]
# Thu, 30 Mar 2023 02:09:37 GMT
VOLUME [/vault/file]
# Thu, 30 Mar 2023 02:09:37 GMT
EXPOSE 8200
# Thu, 30 Mar 2023 02:09:37 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 30 Mar 2023 02:09:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Mar 2023 02:09:37 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f7dab3ab2d6ec29aa28769bec35331fb485b5837501b1e8556413d8b5a79c9c8`  
		Last Modified: Wed, 29 Mar 2023 18:20:25 GMT  
		Size: 2.8 MB (2829647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5f2740e80bef5616c53d91689eff2cb299182e93b2b21ab8e1a39c43c94d808`  
		Last Modified: Thu, 30 Mar 2023 02:10:30 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3fe625bfc5b75b9306a4a117792d2e4921a7b7899b8a1ce3a09591f94d7e91e3`  
		Last Modified: Thu, 30 Mar 2023 02:10:38 GMT  
		Size: 78.4 MB (78424773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0914abc809b7d09bbabebad15cb118be583ef71016af00e794b38e2ed72e4c34`  
		Last Modified: Thu, 30 Mar 2023 02:10:30 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a5580ca7c488bbcf0ec946fdade24d0b925187cbde0a24858d8d349701284d9`  
		Last Modified: Thu, 30 Mar 2023 02:10:30 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.11.8` - linux; arm variant v6

```console
$ docker pull vault@sha256:a71db87ac37c333bc7597fdccfe9ce02eda1a933599c5b322fdb424a93bf950d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.3 MB (76347531 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d779c289c8dfc76bba710b1c1731480f746e8bd6865abc61ddc6c5b10bb2529`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:54 GMT
ADD file:767f6566ea2c075838c0a86ca644a37e446f309f68952f5f921970f046abd252 in / 
# Mon, 13 Mar 2023 16:12:54 GMT
CMD ["/bin/sh"]
# Tue, 14 Mar 2023 01:08:26 GMT
ARG VAULT_VERSION=1.11.8
# Tue, 14 Mar 2023 01:08:26 GMT
# ARGS: VAULT_VERSION=1.11.8
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 14 Mar 2023 01:08:36 GMT
# ARGS: VAULT_VERSION=1.11.8
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 14 Mar 2023 01:08:36 GMT
# ARGS: VAULT_VERSION=1.11.8
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 14 Mar 2023 01:08:37 GMT
VOLUME [/vault/logs]
# Tue, 14 Mar 2023 01:08:37 GMT
VOLUME [/vault/file]
# Tue, 14 Mar 2023 01:08:37 GMT
EXPOSE 8200
# Tue, 14 Mar 2023 01:08:37 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Mar 2023 01:08:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Mar 2023 01:08:37 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:7616dd32f4bf5fddffb2543afaac2355a5fc495348c01060cd67181e36343e96`  
		Last Modified: Fri, 10 Feb 2023 20:51:02 GMT  
		Size: 2.6 MB (2638152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20d6ce4483f53b61c967b4c3063c3c8913c4d7007dbe5f126112764cc420ffef`  
		Last Modified: Tue, 14 Mar 2023 01:09:50 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd6e9835902c6511d9a4b789aef30cdc1c104d14d44655cc9b3d9d4cd6102bbe`  
		Last Modified: Tue, 14 Mar 2023 01:09:58 GMT  
		Size: 73.7 MB (73706110 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f1297b627b1f689e232165254b29a7a5572038444414c3d941a42743af1f14e`  
		Last Modified: Tue, 14 Mar 2023 01:09:49 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9899bca454c65c30636082957b205404625583efc914737c15ca410cbfe7b7f9`  
		Last Modified: Tue, 14 Mar 2023 01:09:49 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.11.8` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:a062db024037c393173285f7efca28cc817fbb382544238e0012ee1e23f29b83
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.5 MB (76537467 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4feaf8c18b7514120d86cdb1b0ce0da4f2e54272b5988346876630a338ffbcb6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:19 GMT
ADD file:50a841463966858f1c3ca87143cf96145d1d52f7349ef516adfbf21cdd5684fe in / 
# Fri, 10 Feb 2023 21:24:19 GMT
CMD ["/bin/sh"]
# Tue, 07 Mar 2023 19:09:34 GMT
ARG VAULT_VERSION=1.11.8
# Tue, 07 Mar 2023 19:09:35 GMT
# ARGS: VAULT_VERSION=1.11.8
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 07 Mar 2023 19:09:42 GMT
# ARGS: VAULT_VERSION=1.11.8
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 07 Mar 2023 19:09:43 GMT
# ARGS: VAULT_VERSION=1.11.8
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 07 Mar 2023 19:09:43 GMT
VOLUME [/vault/logs]
# Tue, 07 Mar 2023 19:09:43 GMT
VOLUME [/vault/file]
# Tue, 07 Mar 2023 19:09:43 GMT
EXPOSE 8200
# Tue, 07 Mar 2023 19:09:44 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 07 Mar 2023 19:09:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Mar 2023 19:09:44 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:6f0e733d82e26042c603e231c39b56abbabdad66673a736ec71c69c65be95f41`  
		Last Modified: Fri, 10 Feb 2023 21:25:10 GMT  
		Size: 2.7 MB (2725026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:668897800d23315f0aae151cff49078d26e91bd34269d041d61494cfed5f951f`  
		Last Modified: Tue, 07 Mar 2023 19:10:40 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe325e46c155e962175b4dce22f793e8e0e5619fee62168f96d0103a72ca5ec2`  
		Last Modified: Tue, 07 Mar 2023 19:10:46 GMT  
		Size: 73.8 MB (73809174 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6e5319193f498d08b846ae93dd93c1bb16596908c24cf66bf18f38a93304dfa`  
		Last Modified: Tue, 07 Mar 2023 19:10:40 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4768cbf310e08a88b8b36c240e95058c45b3ad5b2dbc54158ebb6eb83f581b1`  
		Last Modified: Tue, 07 Mar 2023 19:10:40 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.11.8` - linux; 386

```console
$ docker pull vault@sha256:6d1f8666bc04ad3011179308bf0abe931530b4bc5773699c52e3c3ffd2771837
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78061290 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:abd50f13b71e10479785891445732da1a27377312cc6eaa17cb8317270ba3ff9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:38 GMT
ADD file:0fbd9a88e784719a5d50377c069ea125f9a27568d6d02b43a9512c65ae72870d in / 
# Wed, 29 Mar 2023 17:38:39 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 01:39:46 GMT
ARG VAULT_VERSION=1.11.8
# Thu, 30 Mar 2023 01:39:47 GMT
# ARGS: VAULT_VERSION=1.11.8
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 30 Mar 2023 01:39:58 GMT
# ARGS: VAULT_VERSION=1.11.8
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 30 Mar 2023 01:39:59 GMT
# ARGS: VAULT_VERSION=1.11.8
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 30 Mar 2023 01:39:59 GMT
VOLUME [/vault/logs]
# Thu, 30 Mar 2023 01:39:59 GMT
VOLUME [/vault/file]
# Thu, 30 Mar 2023 01:39:59 GMT
EXPOSE 8200
# Thu, 30 Mar 2023 01:40:00 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 30 Mar 2023 01:40:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Mar 2023 01:40:00 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ebcdc7813a6f23dca055a9257561eabd5fc5c5c21d7a72bb208439bd92f47f70`  
		Last Modified: Wed, 29 Mar 2023 17:39:28 GMT  
		Size: 2.8 MB (2835200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a47dd4eeb6b4e3cf979f8422c57193a394071f8e2fec9bd2ff9682dd74a6d367`  
		Last Modified: Thu, 30 Mar 2023 01:40:58 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff0b86b36c4ad8722e797e33bf619c78b77d9ebac09cc3451b9520712ae863b1`  
		Last Modified: Thu, 30 Mar 2023 01:41:09 GMT  
		Size: 75.2 MB (75222825 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d986f29a1139a80c0365442d5d4e43656dfcd3c0d40cd1d03d5c072c752d0a9`  
		Last Modified: Thu, 30 Mar 2023 01:40:58 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:582b5c55a363c3fec264644c342c4d00429604cc1a2118b49e6ef712661d1d3e`  
		Last Modified: Thu, 30 Mar 2023 01:40:58 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.12.4`

```console
$ docker pull vault@sha256:22fec5a849815423158b41926901d38fbc495f7307f9a880d8a076b7fe81126e
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.12.4` - linux; amd64

```console
$ docker pull vault@sha256:50a73a14cba68bae71ad567c1e8a4ac6022ebda29b6e524e602d02822b5c6a8b
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (85991206 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad8c26f209c68958ebc5bfb94a1ff6e6db9974b177891858a3af284246b7f90d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:37 GMT
ADD file:9663235f252e072c52b0f9e25845841e4321cce2caa7467a0d736c6003b05c00 in / 
# Wed, 29 Mar 2023 18:19:37 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 02:09:16 GMT
ARG VAULT_VERSION=1.12.4
# Thu, 30 Mar 2023 02:09:17 GMT
# ARGS: VAULT_VERSION=1.12.4
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 30 Mar 2023 02:09:25 GMT
# ARGS: VAULT_VERSION=1.12.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 30 Mar 2023 02:09:26 GMT
# ARGS: VAULT_VERSION=1.12.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 30 Mar 2023 02:09:26 GMT
VOLUME [/vault/logs]
# Thu, 30 Mar 2023 02:09:26 GMT
VOLUME [/vault/file]
# Thu, 30 Mar 2023 02:09:26 GMT
EXPOSE 8200
# Thu, 30 Mar 2023 02:09:26 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 30 Mar 2023 02:09:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Mar 2023 02:09:26 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f7dab3ab2d6ec29aa28769bec35331fb485b5837501b1e8556413d8b5a79c9c8`  
		Last Modified: Wed, 29 Mar 2023 18:20:25 GMT  
		Size: 2.8 MB (2829647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c37b0192340903b6f5b6e6e0ba19b7e8e900ad77ee72d4d0a053147e2f2ed614`  
		Last Modified: Thu, 30 Mar 2023 02:10:15 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:226d1a88c399d5ba0e92d0a1e448b60e543cb69b84a5a0af5945d71d8ea3c6b4`  
		Last Modified: Thu, 30 Mar 2023 02:10:24 GMT  
		Size: 83.2 MB (83158292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e51ec36a3a98b30b99edd1fc9905de0f4bd8c1a369c5aae3be17d94792b405a`  
		Last Modified: Thu, 30 Mar 2023 02:10:15 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaa55367b4a74e66fedd2813969ed926fe36cb53660f52685e9f84cf3d4cdc17`  
		Last Modified: Thu, 30 Mar 2023 02:10:15 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.12.4` - linux; arm variant v6

```console
$ docker pull vault@sha256:9623d63ee1ddf8d4801a0c12bfec03565688251d70d8644898ab62a3338872e3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80714395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3bf5cffcf2caf3f04099e172a367607d9c2586deaecc3bff2f1f48d53c015e4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:54 GMT
ADD file:767f6566ea2c075838c0a86ca644a37e446f309f68952f5f921970f046abd252 in / 
# Mon, 13 Mar 2023 16:12:54 GMT
CMD ["/bin/sh"]
# Tue, 14 Mar 2023 01:08:08 GMT
ARG VAULT_VERSION=1.12.4
# Tue, 14 Mar 2023 01:08:08 GMT
# ARGS: VAULT_VERSION=1.12.4
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 14 Mar 2023 01:08:18 GMT
# ARGS: VAULT_VERSION=1.12.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 14 Mar 2023 01:08:19 GMT
# ARGS: VAULT_VERSION=1.12.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 14 Mar 2023 01:08:20 GMT
VOLUME [/vault/logs]
# Tue, 14 Mar 2023 01:08:20 GMT
VOLUME [/vault/file]
# Tue, 14 Mar 2023 01:08:20 GMT
EXPOSE 8200
# Tue, 14 Mar 2023 01:08:20 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Mar 2023 01:08:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Mar 2023 01:08:20 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:7616dd32f4bf5fddffb2543afaac2355a5fc495348c01060cd67181e36343e96`  
		Last Modified: Fri, 10 Feb 2023 20:51:02 GMT  
		Size: 2.6 MB (2638152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43b69eb59307796ac9499c68c863b53eae5df412921c6a1a8babe0e5841881ef`  
		Last Modified: Tue, 14 Mar 2023 01:09:32 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:180941ebaca132219f17880162053fe4440d3df6860acfedf5974e0ea0b2d419`  
		Last Modified: Tue, 14 Mar 2023 01:09:42 GMT  
		Size: 78.1 MB (78072972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a36a6b800fc67317dcab559da4764a826aff9f208b8058e82b4d1120a9aace1b`  
		Last Modified: Tue, 14 Mar 2023 01:09:32 GMT  
		Size: 185.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f4c1f6f18ac4fa011c2c584aef7b02da0738ec5152e15b527fe497aca9e3f0d`  
		Last Modified: Tue, 14 Mar 2023 01:09:32 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.12.4` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:a7115357b9b76c9f66fe982e0ff59f5a8aca3fee3d0aa03c7389dddde201c98c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.0 MB (81039405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ac8ca5205576959a847c474f7f1e62a4aa1b45fee226d7cd8b7380f042396692`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:19 GMT
ADD file:50a841463966858f1c3ca87143cf96145d1d52f7349ef516adfbf21cdd5684fe in / 
# Fri, 10 Feb 2023 21:24:19 GMT
CMD ["/bin/sh"]
# Tue, 07 Mar 2023 19:09:20 GMT
ARG VAULT_VERSION=1.12.4
# Tue, 07 Mar 2023 19:09:21 GMT
# ARGS: VAULT_VERSION=1.12.4
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 07 Mar 2023 19:09:29 GMT
# ARGS: VAULT_VERSION=1.12.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 07 Mar 2023 19:09:30 GMT
# ARGS: VAULT_VERSION=1.12.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 07 Mar 2023 19:09:30 GMT
VOLUME [/vault/logs]
# Tue, 07 Mar 2023 19:09:31 GMT
VOLUME [/vault/file]
# Tue, 07 Mar 2023 19:09:31 GMT
EXPOSE 8200
# Tue, 07 Mar 2023 19:09:31 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 07 Mar 2023 19:09:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Mar 2023 19:09:31 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:6f0e733d82e26042c603e231c39b56abbabdad66673a736ec71c69c65be95f41`  
		Last Modified: Fri, 10 Feb 2023 21:25:10 GMT  
		Size: 2.7 MB (2725026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2f93f2182016fe7dd6ceb31a882e47abfab0eabd444c8c0def95c00c9a6566c`  
		Last Modified: Tue, 07 Mar 2023 19:10:26 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4810616f818085e664304c04c65b132a19384a8f56b748afa2792ca05c22fca`  
		Last Modified: Tue, 07 Mar 2023 19:10:34 GMT  
		Size: 78.3 MB (78311108 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:386db0471957d2eb1998d0649d0ec1cb67e398235f3cfd3122c39e3b6c500b95`  
		Last Modified: Tue, 07 Mar 2023 19:10:27 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17a05e0b1fb9261531e077287831f283cf7f1c3fac49bf9e46b936746004f7ac`  
		Last Modified: Tue, 07 Mar 2023 19:10:27 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.12.4` - linux; 386

```console
$ docker pull vault@sha256:9e382d2e94f0aa52618e297e5a30062af3b17ab0fc448dbc20a78a743a5f0901
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82459496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:447ae6c62cd74842239c2bd777f5faf004dd9c4a779aa31afee23488af554ee5`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:38 GMT
ADD file:0fbd9a88e784719a5d50377c069ea125f9a27568d6d02b43a9512c65ae72870d in / 
# Wed, 29 Mar 2023 17:38:39 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 01:39:30 GMT
ARG VAULT_VERSION=1.12.4
# Thu, 30 Mar 2023 01:39:31 GMT
# ARGS: VAULT_VERSION=1.12.4
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 30 Mar 2023 01:39:42 GMT
# ARGS: VAULT_VERSION=1.12.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 30 Mar 2023 01:39:43 GMT
# ARGS: VAULT_VERSION=1.12.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 30 Mar 2023 01:39:43 GMT
VOLUME [/vault/logs]
# Thu, 30 Mar 2023 01:39:43 GMT
VOLUME [/vault/file]
# Thu, 30 Mar 2023 01:39:43 GMT
EXPOSE 8200
# Thu, 30 Mar 2023 01:39:43 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 30 Mar 2023 01:39:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Mar 2023 01:39:43 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ebcdc7813a6f23dca055a9257561eabd5fc5c5c21d7a72bb208439bd92f47f70`  
		Last Modified: Wed, 29 Mar 2023 17:39:28 GMT  
		Size: 2.8 MB (2835200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e95eb95b478d9bc9b7aee39c5ebad36c04444d40121cbe6d06bb046e126b428`  
		Last Modified: Thu, 30 Mar 2023 01:40:40 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f1ff4f6f376992ca21579c8c8c2957f8b36c749da8f24561d9b1798b0bc17a6`  
		Last Modified: Thu, 30 Mar 2023 01:40:52 GMT  
		Size: 79.6 MB (79621027 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98c9a25b88e57ce0f1f03bdece095f6f81b08ddbc7c0195e2cc6846b2f2aaa48`  
		Last Modified: Thu, 30 Mar 2023 01:40:40 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dbf5db9be77a1f255c58f423082112b75cc0cdd9cffc5032ecc536202cfa488`  
		Last Modified: Thu, 30 Mar 2023 01:40:40 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.13.0`

```console
$ docker pull vault@sha256:9bbeb4ae37f6d1b39ea031d387bdf69ea5b92b92142ba4953f409f14467d55ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.13.0` - linux; amd64

```console
$ docker pull vault@sha256:cd50d80dfe2b6cc0089a54833fa6de847b72cf7b0e618043869d76c1f3111280
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53138944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c5cb6383af89a1fd3a33b08eb784b543a46a6b83239896c70c8ee64cba0240`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:37 GMT
ADD file:9663235f252e072c52b0f9e25845841e4321cce2caa7467a0d736c6003b05c00 in / 
# Wed, 29 Mar 2023 18:19:37 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 02:09:05 GMT
ARG VAULT_VERSION=1.13.0
# Thu, 30 Mar 2023 02:09:06 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 30 Mar 2023 02:09:13 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 30 Mar 2023 02:09:14 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 30 Mar 2023 02:09:14 GMT
VOLUME [/vault/logs]
# Thu, 30 Mar 2023 02:09:14 GMT
VOLUME [/vault/file]
# Thu, 30 Mar 2023 02:09:14 GMT
EXPOSE 8200
# Thu, 30 Mar 2023 02:09:14 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 30 Mar 2023 02:09:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Mar 2023 02:09:14 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f7dab3ab2d6ec29aa28769bec35331fb485b5837501b1e8556413d8b5a79c9c8`  
		Last Modified: Wed, 29 Mar 2023 18:20:25 GMT  
		Size: 2.8 MB (2829647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7705b3229b3bb47e3a84482feac8b37337715e6c3d7d3985f4230455eb9a82db`  
		Last Modified: Thu, 30 Mar 2023 02:09:59 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df544c15ab096bea8403986449760455b23be89491927213c85c084bf902561`  
		Last Modified: Thu, 30 Mar 2023 02:10:07 GMT  
		Size: 50.3 MB (50306029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cafd81487db97ea93eae88a0ca4f140360795306a5a6ad8ad285eddbffb2e1`  
		Last Modified: Thu, 30 Mar 2023 02:09:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4357a3a5c7b81f57ff8c4d55aaa18f2a95790360a2e872d52df6bd74947ba9`  
		Last Modified: Thu, 30 Mar 2023 02:09:59 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.13.0` - linux; arm variant v6

```console
$ docker pull vault@sha256:28fd98af546be1665a4678c88260774c694e454fd015257449bf75330cec027c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50197917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f73f1f67a340bae759cdf70ed9284b31f8cf3274b9463bcef009bb7bf6de53d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:54 GMT
ADD file:767f6566ea2c075838c0a86ca644a37e446f309f68952f5f921970f046abd252 in / 
# Mon, 13 Mar 2023 16:12:54 GMT
CMD ["/bin/sh"]
# Tue, 14 Mar 2023 01:07:47 GMT
ARG VAULT_VERSION=1.13.0
# Tue, 14 Mar 2023 01:07:47 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 14 Mar 2023 01:08:00 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 14 Mar 2023 01:08:01 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 14 Mar 2023 01:08:01 GMT
VOLUME [/vault/logs]
# Tue, 14 Mar 2023 01:08:01 GMT
VOLUME [/vault/file]
# Tue, 14 Mar 2023 01:08:01 GMT
EXPOSE 8200
# Tue, 14 Mar 2023 01:08:01 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Mar 2023 01:08:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Mar 2023 01:08:02 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:7616dd32f4bf5fddffb2543afaac2355a5fc495348c01060cd67181e36343e96`  
		Last Modified: Fri, 10 Feb 2023 20:51:02 GMT  
		Size: 2.6 MB (2638152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1f485ff8e71a4c9555fadeb7fc26b8afa61b20dff5999ee89bc8c25001cee9`  
		Last Modified: Tue, 14 Mar 2023 01:09:13 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65e162950b9bf88b60c75819366e58b386b353c914fc6555de166911c603774`  
		Last Modified: Tue, 14 Mar 2023 01:09:22 GMT  
		Size: 47.6 MB (47556494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c181b282de46200743298dc51b928ce30a1899f8c3c6a2e59802dd295866b91c`  
		Last Modified: Tue, 14 Mar 2023 01:09:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3d143ba6962baa20993b8e518583e42bc1a52523112d5bfe2476453d6c94cc`  
		Last Modified: Tue, 14 Mar 2023 01:09:13 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.13.0` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:405a411f0d9eaf30c667f4c8355bcd537db30a13558f700c6e73c273f8f1ac4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48962947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51306818dbce4efdbc437d66fefdbe69ca4d81f0417c20614fa9f0c84c1ce0af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:19 GMT
ADD file:50a841463966858f1c3ca87143cf96145d1d52f7349ef516adfbf21cdd5684fe in / 
# Fri, 10 Feb 2023 21:24:19 GMT
CMD ["/bin/sh"]
# Tue, 07 Mar 2023 19:09:07 GMT
ARG VAULT_VERSION=1.13.0
# Tue, 07 Mar 2023 19:09:07 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 07 Mar 2023 19:09:15 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 07 Mar 2023 19:09:16 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 07 Mar 2023 19:09:16 GMT
VOLUME [/vault/logs]
# Tue, 07 Mar 2023 19:09:16 GMT
VOLUME [/vault/file]
# Tue, 07 Mar 2023 19:09:16 GMT
EXPOSE 8200
# Tue, 07 Mar 2023 19:09:16 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 07 Mar 2023 19:09:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Mar 2023 19:09:17 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:6f0e733d82e26042c603e231c39b56abbabdad66673a736ec71c69c65be95f41`  
		Last Modified: Fri, 10 Feb 2023 21:25:10 GMT  
		Size: 2.7 MB (2725026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3a1f13beeed2834db1f1cfaf6d383325d5f58dc0fb56db3b77540615549cc2`  
		Last Modified: Tue, 07 Mar 2023 19:10:11 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fb88a3ba8fed11097e3414fc1abf54436e37f883824d1bce9c75e792449f01`  
		Last Modified: Tue, 07 Mar 2023 19:10:17 GMT  
		Size: 46.2 MB (46234652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273bacb9571802767a0f679e1d982123b12ddea2bfc0b34218770b8b861de379`  
		Last Modified: Tue, 07 Mar 2023 19:10:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78de7536ed89a538d88248bac9cb523f3d233a468af7be12eead7247497dd746`  
		Last Modified: Tue, 07 Mar 2023 19:10:11 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.13.0` - linux; 386

```console
$ docker pull vault@sha256:04ac00c319306d5b6db56d759651e609c6dedb9f3fbb7fb6530a063a23e18c52
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49813365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a37525d20b9d925c4dbc0f97e629b778f261433425d2ff5a666be48965317c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:38 GMT
ADD file:0fbd9a88e784719a5d50377c069ea125f9a27568d6d02b43a9512c65ae72870d in / 
# Wed, 29 Mar 2023 17:38:39 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 01:39:15 GMT
ARG VAULT_VERSION=1.13.0
# Thu, 30 Mar 2023 01:39:15 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 30 Mar 2023 01:39:26 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 30 Mar 2023 01:39:27 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 30 Mar 2023 01:39:27 GMT
VOLUME [/vault/logs]
# Thu, 30 Mar 2023 01:39:27 GMT
VOLUME [/vault/file]
# Thu, 30 Mar 2023 01:39:27 GMT
EXPOSE 8200
# Thu, 30 Mar 2023 01:39:27 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 30 Mar 2023 01:39:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Mar 2023 01:39:27 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ebcdc7813a6f23dca055a9257561eabd5fc5c5c21d7a72bb208439bd92f47f70`  
		Last Modified: Wed, 29 Mar 2023 17:39:28 GMT  
		Size: 2.8 MB (2835200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf3326cfa967ea979af5921e783c42acec3e399d211a751841b43d032b42402`  
		Last Modified: Thu, 30 Mar 2023 01:40:22 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed422c56b78da7cc7bb21ab31c3354f49a8eab5a5f6082629bd87bcb134eb6d3`  
		Last Modified: Thu, 30 Mar 2023 01:40:33 GMT  
		Size: 47.0 MB (46974897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810d43aaa62ab63d719c6c6363514f147e4929f22243bd411d4b3c3c07332dde`  
		Last Modified: Thu, 30 Mar 2023 01:40:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2a8e6e32b9b8bba8abfdeb5016573b1db62f1a589d40c156152824f165e194`  
		Last Modified: Thu, 30 Mar 2023 01:40:22 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:latest`

```console
$ docker pull vault@sha256:9bbeb4ae37f6d1b39ea031d387bdf69ea5b92b92142ba4953f409f14467d55ea
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:cd50d80dfe2b6cc0089a54833fa6de847b72cf7b0e618043869d76c1f3111280
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53138944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:79c5cb6383af89a1fd3a33b08eb784b543a46a6b83239896c70c8ee64cba0240`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:37 GMT
ADD file:9663235f252e072c52b0f9e25845841e4321cce2caa7467a0d736c6003b05c00 in / 
# Wed, 29 Mar 2023 18:19:37 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 02:09:05 GMT
ARG VAULT_VERSION=1.13.0
# Thu, 30 Mar 2023 02:09:06 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 30 Mar 2023 02:09:13 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 30 Mar 2023 02:09:14 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 30 Mar 2023 02:09:14 GMT
VOLUME [/vault/logs]
# Thu, 30 Mar 2023 02:09:14 GMT
VOLUME [/vault/file]
# Thu, 30 Mar 2023 02:09:14 GMT
EXPOSE 8200
# Thu, 30 Mar 2023 02:09:14 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 30 Mar 2023 02:09:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Mar 2023 02:09:14 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f7dab3ab2d6ec29aa28769bec35331fb485b5837501b1e8556413d8b5a79c9c8`  
		Last Modified: Wed, 29 Mar 2023 18:20:25 GMT  
		Size: 2.8 MB (2829647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7705b3229b3bb47e3a84482feac8b37337715e6c3d7d3985f4230455eb9a82db`  
		Last Modified: Thu, 30 Mar 2023 02:09:59 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3df544c15ab096bea8403986449760455b23be89491927213c85c084bf902561`  
		Last Modified: Thu, 30 Mar 2023 02:10:07 GMT  
		Size: 50.3 MB (50306029 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4cafd81487db97ea93eae88a0ca4f140360795306a5a6ad8ad285eddbffb2e1`  
		Last Modified: Thu, 30 Mar 2023 02:09:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e4357a3a5c7b81f57ff8c4d55aaa18f2a95790360a2e872d52df6bd74947ba9`  
		Last Modified: Thu, 30 Mar 2023 02:09:59 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:28fd98af546be1665a4678c88260774c694e454fd015257449bf75330cec027c
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50197917 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7f73f1f67a340bae759cdf70ed9284b31f8cf3274b9463bcef009bb7bf6de53d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 13 Mar 2023 16:12:54 GMT
ADD file:767f6566ea2c075838c0a86ca644a37e446f309f68952f5f921970f046abd252 in / 
# Mon, 13 Mar 2023 16:12:54 GMT
CMD ["/bin/sh"]
# Tue, 14 Mar 2023 01:07:47 GMT
ARG VAULT_VERSION=1.13.0
# Tue, 14 Mar 2023 01:07:47 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 14 Mar 2023 01:08:00 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 14 Mar 2023 01:08:01 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 14 Mar 2023 01:08:01 GMT
VOLUME [/vault/logs]
# Tue, 14 Mar 2023 01:08:01 GMT
VOLUME [/vault/file]
# Tue, 14 Mar 2023 01:08:01 GMT
EXPOSE 8200
# Tue, 14 Mar 2023 01:08:01 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Mar 2023 01:08:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Mar 2023 01:08:02 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:7616dd32f4bf5fddffb2543afaac2355a5fc495348c01060cd67181e36343e96`  
		Last Modified: Fri, 10 Feb 2023 20:51:02 GMT  
		Size: 2.6 MB (2638152 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f1f485ff8e71a4c9555fadeb7fc26b8afa61b20dff5999ee89bc8c25001cee9`  
		Last Modified: Tue, 14 Mar 2023 01:09:13 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f65e162950b9bf88b60c75819366e58b386b353c914fc6555de166911c603774`  
		Last Modified: Tue, 14 Mar 2023 01:09:22 GMT  
		Size: 47.6 MB (47556494 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c181b282de46200743298dc51b928ce30a1899f8c3c6a2e59802dd295866b91c`  
		Last Modified: Tue, 14 Mar 2023 01:09:13 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3d143ba6962baa20993b8e518583e42bc1a52523112d5bfe2476453d6c94cc`  
		Last Modified: Tue, 14 Mar 2023 01:09:13 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:405a411f0d9eaf30c667f4c8355bcd537db30a13558f700c6e73c273f8f1ac4d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48962947 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51306818dbce4efdbc437d66fefdbe69ca4d81f0417c20614fa9f0c84c1ce0af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:19 GMT
ADD file:50a841463966858f1c3ca87143cf96145d1d52f7349ef516adfbf21cdd5684fe in / 
# Fri, 10 Feb 2023 21:24:19 GMT
CMD ["/bin/sh"]
# Tue, 07 Mar 2023 19:09:07 GMT
ARG VAULT_VERSION=1.13.0
# Tue, 07 Mar 2023 19:09:07 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 07 Mar 2023 19:09:15 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 07 Mar 2023 19:09:16 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 07 Mar 2023 19:09:16 GMT
VOLUME [/vault/logs]
# Tue, 07 Mar 2023 19:09:16 GMT
VOLUME [/vault/file]
# Tue, 07 Mar 2023 19:09:16 GMT
EXPOSE 8200
# Tue, 07 Mar 2023 19:09:16 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 07 Mar 2023 19:09:16 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 07 Mar 2023 19:09:17 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:6f0e733d82e26042c603e231c39b56abbabdad66673a736ec71c69c65be95f41`  
		Last Modified: Fri, 10 Feb 2023 21:25:10 GMT  
		Size: 2.7 MB (2725026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d3a1f13beeed2834db1f1cfaf6d383325d5f58dc0fb56db3b77540615549cc2`  
		Last Modified: Tue, 07 Mar 2023 19:10:11 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18fb88a3ba8fed11097e3414fc1abf54436e37f883824d1bce9c75e792449f01`  
		Last Modified: Tue, 07 Mar 2023 19:10:17 GMT  
		Size: 46.2 MB (46234652 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:273bacb9571802767a0f679e1d982123b12ddea2bfc0b34218770b8b861de379`  
		Last Modified: Tue, 07 Mar 2023 19:10:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78de7536ed89a538d88248bac9cb523f3d233a468af7be12eead7247497dd746`  
		Last Modified: Tue, 07 Mar 2023 19:10:11 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:04ac00c319306d5b6db56d759651e609c6dedb9f3fbb7fb6530a063a23e18c52
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49813365 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44a37525d20b9d925c4dbc0f97e629b778f261433425d2ff5a666be48965317c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:38 GMT
ADD file:0fbd9a88e784719a5d50377c069ea125f9a27568d6d02b43a9512c65ae72870d in / 
# Wed, 29 Mar 2023 17:38:39 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 01:39:15 GMT
ARG VAULT_VERSION=1.13.0
# Thu, 30 Mar 2023 01:39:15 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 30 Mar 2023 01:39:26 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 30 Mar 2023 01:39:27 GMT
# ARGS: VAULT_VERSION=1.13.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 30 Mar 2023 01:39:27 GMT
VOLUME [/vault/logs]
# Thu, 30 Mar 2023 01:39:27 GMT
VOLUME [/vault/file]
# Thu, 30 Mar 2023 01:39:27 GMT
EXPOSE 8200
# Thu, 30 Mar 2023 01:39:27 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 30 Mar 2023 01:39:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Mar 2023 01:39:27 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ebcdc7813a6f23dca055a9257561eabd5fc5c5c21d7a72bb208439bd92f47f70`  
		Last Modified: Wed, 29 Mar 2023 17:39:28 GMT  
		Size: 2.8 MB (2835200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6bf3326cfa967ea979af5921e783c42acec3e399d211a751841b43d032b42402`  
		Last Modified: Thu, 30 Mar 2023 01:40:22 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed422c56b78da7cc7bb21ab31c3354f49a8eab5a5f6082629bd87bcb134eb6d3`  
		Last Modified: Thu, 30 Mar 2023 01:40:33 GMT  
		Size: 47.0 MB (46974897 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:810d43aaa62ab63d719c6c6363514f147e4929f22243bd411d4b3c3c07332dde`  
		Last Modified: Thu, 30 Mar 2023 01:40:22 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0d2a8e6e32b9b8bba8abfdeb5016573b1db62f1a589d40c156152824f165e194`  
		Last Modified: Thu, 30 Mar 2023 01:40:22 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
