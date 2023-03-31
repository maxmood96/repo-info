## `vault:latest`

```console
$ docker pull vault@sha256:2a83da216a42c8541a36038ff79a797e1f6a9c39dd64f38ca45e152c8ed68533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:17e6bd0e4c861200f982f2620b209215d997d427a14649466da3702a1a7e7151
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53141757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a1ffdd512ce98dd6da262f530fb83d215481229df4bad79c71ade9e06e8075c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:37 GMT
ADD file:9663235f252e072c52b0f9e25845841e4321cce2caa7467a0d736c6003b05c00 in / 
# Wed, 29 Mar 2023 18:19:37 GMT
CMD ["/bin/sh"]
# Fri, 31 Mar 2023 00:26:01 GMT
ARG VAULT_VERSION=1.13.1
# Fri, 31 Mar 2023 00:26:01 GMT
# ARGS: VAULT_VERSION=1.13.1
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 31 Mar 2023 00:26:10 GMT
# ARGS: VAULT_VERSION=1.13.1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 31 Mar 2023 00:26:10 GMT
# ARGS: VAULT_VERSION=1.13.1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 31 Mar 2023 00:26:10 GMT
VOLUME [/vault/logs]
# Fri, 31 Mar 2023 00:26:11 GMT
VOLUME [/vault/file]
# Fri, 31 Mar 2023 00:26:11 GMT
EXPOSE 8200
# Fri, 31 Mar 2023 00:26:11 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 31 Mar 2023 00:26:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 00:26:11 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f7dab3ab2d6ec29aa28769bec35331fb485b5837501b1e8556413d8b5a79c9c8`  
		Last Modified: Wed, 29 Mar 2023 18:20:25 GMT  
		Size: 2.8 MB (2829647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:241d381452e9a9337597cdca8eb007f95fd87c889e1ac69829c1c8a4355ccfa3`  
		Last Modified: Fri, 31 Mar 2023 00:26:48 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e11c05b90e112637cf74d021505debd87ba8a99e63d52efd98c632d9aae74af`  
		Last Modified: Fri, 31 Mar 2023 00:26:56 GMT  
		Size: 50.3 MB (50308842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18c0c0a001e0e9173ef520931c260919a91f3a88202e5120eb4540854729c45f`  
		Last Modified: Fri, 31 Mar 2023 00:26:48 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18febc7f864fbfdfaf7fb9794c6286120690b251b5d03f20ddb18d322703a511`  
		Last Modified: Fri, 31 Mar 2023 00:26:48 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:a6f1243fcebc284e7a4555cb11d3fd873944e3bd1b5ce11082c0c8b529d00b23
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.2 MB (50202147 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5cc1a98fd9542a34c56eeb5a1c31f871ae6e5ca1802cd273f7a810e66c91df29`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:15 GMT
ADD file:1039802413c644346f599dac53a7c6dabd123027756231b9d8f64a1068c9779d in / 
# Wed, 29 Mar 2023 18:01:15 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 23:49:26 GMT
ARG VAULT_VERSION=1.13.1
# Thu, 30 Mar 2023 23:49:27 GMT
# ARGS: VAULT_VERSION=1.13.1
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 30 Mar 2023 23:49:38 GMT
# ARGS: VAULT_VERSION=1.13.1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 30 Mar 2023 23:49:39 GMT
# ARGS: VAULT_VERSION=1.13.1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 30 Mar 2023 23:49:39 GMT
VOLUME [/vault/logs]
# Thu, 30 Mar 2023 23:49:39 GMT
VOLUME [/vault/file]
# Thu, 30 Mar 2023 23:49:39 GMT
EXPOSE 8200
# Thu, 30 Mar 2023 23:49:39 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 30 Mar 2023 23:49:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Mar 2023 23:49:40 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ffeb76b9ee2f52d46487f4f9a7074ea62dea819a2dd53c9a2c6d703ca7b5aa06`  
		Last Modified: Wed, 29 Mar 2023 18:02:21 GMT  
		Size: 2.6 MB (2638259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:092b4bc92ab9199946dfc7e25cabeae4763b42e4cff126c7a6f0ab5358b58d33`  
		Last Modified: Thu, 30 Mar 2023 23:50:19 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69a2a2f2cbe3c5a98e694e5ab6fb8e1dbd4dd61008793375203cbbf0c2e039b7`  
		Last Modified: Thu, 30 Mar 2023 23:50:28 GMT  
		Size: 47.6 MB (47560619 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec960735600b2e742849c1bcd101bed8b40ab79de6ae5095edfd8c362fd6f7a2`  
		Last Modified: Thu, 30 Mar 2023 23:50:19 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ad79280fc7903208f263c1648e52b8492b9cd3461a6ab25d5be6bfe67f4a0a1`  
		Last Modified: Thu, 30 Mar 2023 23:50:19 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:faa29e5e61998e8250a04afa0ca347555050984612f01c834317642af56374f5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (48966929 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6a22797424be24af0737ae607708fa77b42d14723df24829a051b81428dd021`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:25 GMT
ADD file:c3d52cc254959a9ff493e7347e6b1bc25c0ccfdcf9532dbf43173ddd182d0e4d in / 
# Wed, 29 Mar 2023 17:39:25 GMT
CMD ["/bin/sh"]
# Fri, 31 Mar 2023 00:47:00 GMT
ARG VAULT_VERSION=1.13.1
# Fri, 31 Mar 2023 00:47:01 GMT
# ARGS: VAULT_VERSION=1.13.1
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 31 Mar 2023 00:47:08 GMT
# ARGS: VAULT_VERSION=1.13.1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 31 Mar 2023 00:47:10 GMT
# ARGS: VAULT_VERSION=1.13.1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 31 Mar 2023 00:47:10 GMT
VOLUME [/vault/logs]
# Fri, 31 Mar 2023 00:47:10 GMT
VOLUME [/vault/file]
# Fri, 31 Mar 2023 00:47:10 GMT
EXPOSE 8200
# Fri, 31 Mar 2023 00:47:10 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 31 Mar 2023 00:47:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 00:47:10 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:422ed46b1a92579f7c475c0c19fade6880a8d98f23a2b4ccfb77c265d4f72dfc`  
		Last Modified: Wed, 29 Mar 2023 17:40:13 GMT  
		Size: 2.7 MB (2725148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cc12ce430d424163a6641ff7cfd12ecb6dd2e41d1167b1e610980caefbf5b8f`  
		Last Modified: Fri, 31 Mar 2023 00:47:44 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:59f62de6eb58f35fbd6fff6fad7aee1614709fd5fe585e2ac2326c0ef1f6d497`  
		Last Modified: Fri, 31 Mar 2023 00:47:49 GMT  
		Size: 46.2 MB (46238512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46913d530368362b6c06a1c15a529537551160b47eb49ee51807ba06d8f8ab6d`  
		Last Modified: Fri, 31 Mar 2023 00:47:44 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c25d335e966e22bfa515af53e3380414a329505643e90c68151b327445f2d1c`  
		Last Modified: Fri, 31 Mar 2023 00:47:43 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:70352e31bdd8876eaed69c7d445d04d8d1d3df58c360f07261d92070e2f28b10
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.8 MB (49822515 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c307c1f5a98730fafadcc3e72f35920d9d16f23322a66532181dcad7c92fe4e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:38 GMT
ADD file:0fbd9a88e784719a5d50377c069ea125f9a27568d6d02b43a9512c65ae72870d in / 
# Wed, 29 Mar 2023 17:38:39 GMT
CMD ["/bin/sh"]
# Fri, 31 Mar 2023 00:44:27 GMT
ARG VAULT_VERSION=1.13.1
# Fri, 31 Mar 2023 00:44:28 GMT
# ARGS: VAULT_VERSION=1.13.1
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 31 Mar 2023 00:44:39 GMT
# ARGS: VAULT_VERSION=1.13.1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 31 Mar 2023 00:44:39 GMT
# ARGS: VAULT_VERSION=1.13.1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 31 Mar 2023 00:44:40 GMT
VOLUME [/vault/logs]
# Fri, 31 Mar 2023 00:44:40 GMT
VOLUME [/vault/file]
# Fri, 31 Mar 2023 00:44:40 GMT
EXPOSE 8200
# Fri, 31 Mar 2023 00:44:40 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 31 Mar 2023 00:44:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 00:44:40 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ebcdc7813a6f23dca055a9257561eabd5fc5c5c21d7a72bb208439bd92f47f70`  
		Last Modified: Wed, 29 Mar 2023 17:39:28 GMT  
		Size: 2.8 MB (2835200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6900aaf5d02fbdb58f0a7e556c01731d5ea937f7c00552c8ec027b6d11eb0b`  
		Last Modified: Fri, 31 Mar 2023 00:45:19 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb4accdefaa15181151c2d22079c25605abefd2be499a6f83af8e828a04f1fff`  
		Last Modified: Fri, 31 Mar 2023 00:45:29 GMT  
		Size: 47.0 MB (46984045 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2062669ca51dca07278f6e40deca8bbe939d9de774156ab5ac45113feffa2894`  
		Last Modified: Fri, 31 Mar 2023 00:45:19 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91475eff1e00374c9f0a7050ab316dd4327bb13cfddb810acd3ac1a7bcefe27c`  
		Last Modified: Fri, 31 Mar 2023 00:45:19 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
