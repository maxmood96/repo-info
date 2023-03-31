<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `vault`

-	[`vault:1.10.11`](#vault11011)
-	[`vault:1.11.9`](#vault1119)
-	[`vault:1.12.5`](#vault1125)
-	[`vault:1.13.1`](#vault1131)
-	[`vault:latest`](#vaultlatest)

## `vault:1.10.11`

```console
$ docker pull vault@sha256:50d5bd215f38ba19c81dc79c0fa7a4af7f07f9138dcef7a48e80cb0baeb5c15f
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
$ docker pull vault@sha256:906dcbae9aaba8ccf17dc95d9f677ed4c5f24067c41301065fb1b8d1a6bb4e66
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80432324 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:27b6c49afcd39e5f79f60f2f6f7adc4211a74de6185f4e70adc446cd80b20fb4`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:15 GMT
ADD file:1039802413c644346f599dac53a7c6dabd123027756231b9d8f64a1068c9779d in / 
# Wed, 29 Mar 2023 18:01:15 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 00:36:39 GMT
ARG VAULT_VERSION=1.10.11
# Thu, 30 Mar 2023 00:36:40 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 30 Mar 2023 00:36:50 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 30 Mar 2023 00:36:51 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 30 Mar 2023 00:36:51 GMT
VOLUME [/vault/logs]
# Thu, 30 Mar 2023 00:36:51 GMT
VOLUME [/vault/file]
# Thu, 30 Mar 2023 00:36:51 GMT
EXPOSE 8200
# Thu, 30 Mar 2023 00:36:51 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 30 Mar 2023 00:36:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Mar 2023 00:36:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ffeb76b9ee2f52d46487f4f9a7074ea62dea819a2dd53c9a2c6d703ca7b5aa06`  
		Last Modified: Wed, 29 Mar 2023 18:02:21 GMT  
		Size: 2.6 MB (2638259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97278dfb127bd4709df09cdd936a6ab3af4c9d2d2dd3e25a7bd1c5b0b634608a`  
		Last Modified: Thu, 30 Mar 2023 23:51:07 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2281f965dc065abfa35c2fc06bd03df4bd56f2297d4d98dcd289398626901f3c`  
		Last Modified: Thu, 30 Mar 2023 23:51:16 GMT  
		Size: 77.8 MB (77790799 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:552a5bfae99f19c489b29955c5c28990f94b437d83f4ed55b7f32850fbd87f90`  
		Last Modified: Thu, 30 Mar 2023 23:51:07 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1a3329135580172f19bcfc9aee00870ae87e490d8511bbce4645f074de4cb99`  
		Last Modified: Thu, 30 Mar 2023 23:51:07 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.10.11` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:640bab2894464de6520fc3fd7eff6b27a0afa35aa64ffaa31454d3d525312667
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.4 MB (80433961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1561994ce7554b6e098bcf471073761381ff00f486b3404083242656a8616706`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:25 GMT
ADD file:c3d52cc254959a9ff493e7347e6b1bc25c0ccfdcf9532dbf43173ddd182d0e4d in / 
# Wed, 29 Mar 2023 17:39:25 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 03:29:18 GMT
ARG VAULT_VERSION=1.10.11
# Thu, 30 Mar 2023 03:29:18 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 30 Mar 2023 03:29:26 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 30 Mar 2023 03:29:28 GMT
# ARGS: VAULT_VERSION=1.10.11
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 30 Mar 2023 03:29:28 GMT
VOLUME [/vault/logs]
# Thu, 30 Mar 2023 03:29:28 GMT
VOLUME [/vault/file]
# Thu, 30 Mar 2023 03:29:28 GMT
EXPOSE 8200
# Thu, 30 Mar 2023 03:29:28 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 30 Mar 2023 03:29:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Mar 2023 03:29:28 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:422ed46b1a92579f7c475c0c19fade6880a8d98f23a2b4ccfb77c265d4f72dfc`  
		Last Modified: Wed, 29 Mar 2023 17:40:13 GMT  
		Size: 2.7 MB (2725148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da0f19ec15f778ed9e8591fff8d298a3e6198c19c9acc840b8bb6c4cc9353a85`  
		Last Modified: Thu, 30 Mar 2023 03:30:15 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aace7303cdb787ab8d7ef93516a0e2bcd4826fd0caaa2ec81884a37d6586d3f`  
		Last Modified: Thu, 30 Mar 2023 03:30:22 GMT  
		Size: 77.7 MB (77705543 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28cab760b48c2c74483d454fdd28fdbc4f4ea243f804f0cda25834aef171eeed`  
		Last Modified: Thu, 30 Mar 2023 03:30:16 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c263c747704609fd576d2cf4b944e0bc5ffd0ac0dc60b84ba2131be6f600e143`  
		Last Modified: Thu, 30 Mar 2023 03:30:16 GMT  
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

## `vault:1.11.9`

```console
$ docker pull vault@sha256:564ea47a78271ec73eaa932ed97c3d3c43a2c048e3ae121b46d1e4cda7eb8f48
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.11.9` - linux; amd64

```console
$ docker pull vault@sha256:c3a3d85d33636472c10ed0b6b647b1cf4b6c8d2a6559720c16a8e7f98cc65316
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.3 MB (81265748 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e07faccbe9aac1439cadba8caf812aedee04a09b7b6c7a34001e17bc4b2689ee`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:37 GMT
ADD file:9663235f252e072c52b0f9e25845841e4321cce2caa7467a0d736c6003b05c00 in / 
# Wed, 29 Mar 2023 18:19:37 GMT
CMD ["/bin/sh"]
# Fri, 31 Mar 2023 00:26:26 GMT
ARG VAULT_VERSION=1.11.9
# Fri, 31 Mar 2023 00:26:27 GMT
# ARGS: VAULT_VERSION=1.11.9
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 31 Mar 2023 00:26:34 GMT
# ARGS: VAULT_VERSION=1.11.9
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 31 Mar 2023 00:26:35 GMT
# ARGS: VAULT_VERSION=1.11.9
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 31 Mar 2023 00:26:35 GMT
VOLUME [/vault/logs]
# Fri, 31 Mar 2023 00:26:35 GMT
VOLUME [/vault/file]
# Fri, 31 Mar 2023 00:26:35 GMT
EXPOSE 8200
# Fri, 31 Mar 2023 00:26:35 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 31 Mar 2023 00:26:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 00:26:36 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f7dab3ab2d6ec29aa28769bec35331fb485b5837501b1e8556413d8b5a79c9c8`  
		Last Modified: Wed, 29 Mar 2023 18:20:25 GMT  
		Size: 2.8 MB (2829647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64e9e669e22fd29d4ced18d93c505114144986443d105942c2e088f7c5483413`  
		Last Modified: Fri, 31 Mar 2023 00:27:20 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be4b8f53c44d4812079e979f1e3b30f259a96950657b9d6a1364a10768bddd95`  
		Last Modified: Fri, 31 Mar 2023 00:27:29 GMT  
		Size: 78.4 MB (78432831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:caa7adc21ab2ec92339437475e4d19dfb5e0d7b2720a81dd7cd42db34978a3c0`  
		Last Modified: Fri, 31 Mar 2023 00:27:20 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4df99bcbb8b9569865784486006cdcc596cbdf6a8ed7056ae3eb86895dd5592d`  
		Last Modified: Fri, 31 Mar 2023 00:27:20 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.11.9` - linux; arm variant v6

```console
$ docker pull vault@sha256:ab7e54ab7c165334579f5ce4005fb6c3ba5988eba9453b004c8efbfb4648243a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.4 MB (76368961 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b90c457d128f9c1d3249f51f712462e18fde5678a3c69a05ff870c541ab43ba8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:15 GMT
ADD file:1039802413c644346f599dac53a7c6dabd123027756231b9d8f64a1068c9779d in / 
# Wed, 29 Mar 2023 18:01:15 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 23:49:58 GMT
ARG VAULT_VERSION=1.11.9
# Thu, 30 Mar 2023 23:49:58 GMT
# ARGS: VAULT_VERSION=1.11.9
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 30 Mar 2023 23:50:07 GMT
# ARGS: VAULT_VERSION=1.11.9
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 30 Mar 2023 23:50:08 GMT
# ARGS: VAULT_VERSION=1.11.9
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 30 Mar 2023 23:50:08 GMT
VOLUME [/vault/logs]
# Thu, 30 Mar 2023 23:50:08 GMT
VOLUME [/vault/file]
# Thu, 30 Mar 2023 23:50:09 GMT
EXPOSE 8200
# Thu, 30 Mar 2023 23:50:09 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 30 Mar 2023 23:50:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Mar 2023 23:50:09 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ffeb76b9ee2f52d46487f4f9a7074ea62dea819a2dd53c9a2c6d703ca7b5aa06`  
		Last Modified: Wed, 29 Mar 2023 18:02:21 GMT  
		Size: 2.6 MB (2638259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a3aef42c3ad0181e2649ff0f3bde18080f57c084fbcf2626466d7251af6c7567`  
		Last Modified: Thu, 30 Mar 2023 23:50:52 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4936ab51504cb9b944c211d33396b9c28e1afb7390653fbc3075972863063694`  
		Last Modified: Thu, 30 Mar 2023 23:51:00 GMT  
		Size: 73.7 MB (73727440 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cfa3084fd08c874d890de6e50b5760131ea4a284c194660b2f22f573753f7b2c`  
		Last Modified: Thu, 30 Mar 2023 23:50:51 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccd16ba9ebf3a51af2e66784f85698d68dcb46c1190e79274f8b0b2f047f5cfc`  
		Last Modified: Thu, 30 Mar 2023 23:50:51 GMT  
		Size: 1.8 KB (1808 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.11.9` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:43c41d54013b01d52c84da66df2ee3c47f9ee36f82a922151f8e4c569c3ebdb0
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.6 MB (76553804 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:846e11a9d609a834b3774f9d8f06716ea24585c2b488c9f59c6f497809dbd5c8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:25 GMT
ADD file:c3d52cc254959a9ff493e7347e6b1bc25c0ccfdcf9532dbf43173ddd182d0e4d in / 
# Wed, 29 Mar 2023 17:39:25 GMT
CMD ["/bin/sh"]
# Fri, 31 Mar 2023 00:47:25 GMT
ARG VAULT_VERSION=1.11.9
# Fri, 31 Mar 2023 00:47:25 GMT
# ARGS: VAULT_VERSION=1.11.9
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 31 Mar 2023 00:47:32 GMT
# ARGS: VAULT_VERSION=1.11.9
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 31 Mar 2023 00:47:34 GMT
# ARGS: VAULT_VERSION=1.11.9
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 31 Mar 2023 00:47:34 GMT
VOLUME [/vault/logs]
# Fri, 31 Mar 2023 00:47:34 GMT
VOLUME [/vault/file]
# Fri, 31 Mar 2023 00:47:34 GMT
EXPOSE 8200
# Fri, 31 Mar 2023 00:47:34 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 31 Mar 2023 00:47:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 00:47:34 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:422ed46b1a92579f7c475c0c19fade6880a8d98f23a2b4ccfb77c265d4f72dfc`  
		Last Modified: Wed, 29 Mar 2023 17:40:13 GMT  
		Size: 2.7 MB (2725148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7bacdfe9e7e4e0960251579644950c678307b6b823e64a42f4509c62184acc`  
		Last Modified: Fri, 31 Mar 2023 00:48:10 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09947f7b37dd416eb57953629b57e84a1c6170569acc038c33173ff0484d5f86`  
		Last Modified: Fri, 31 Mar 2023 00:48:16 GMT  
		Size: 73.8 MB (73825387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f07bdbc8e7e793a90779a4f2010e2fb3c50800f1ed3079d4bd44bbb1587f57b`  
		Last Modified: Fri, 31 Mar 2023 00:48:09 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:255d641021a414a1b5e14f401fd79aa7d1b5a0744fd3f336acac05386bf03d97`  
		Last Modified: Fri, 31 Mar 2023 00:48:10 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.11.9` - linux; 386

```console
$ docker pull vault@sha256:a0f1d754404a44b0d427845beb87a8d9a186f0233abde96c221feae6921102c4
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.1 MB (78075307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0ce8963af687a2d9014e678f39ac9bd13cf979dccb80689e04a86e8a97963c2c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:38 GMT
ADD file:0fbd9a88e784719a5d50377c069ea125f9a27568d6d02b43a9512c65ae72870d in / 
# Wed, 29 Mar 2023 17:38:39 GMT
CMD ["/bin/sh"]
# Fri, 31 Mar 2023 00:44:59 GMT
ARG VAULT_VERSION=1.11.9
# Fri, 31 Mar 2023 00:45:00 GMT
# ARGS: VAULT_VERSION=1.11.9
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 31 Mar 2023 00:45:09 GMT
# ARGS: VAULT_VERSION=1.11.9
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 31 Mar 2023 00:45:10 GMT
# ARGS: VAULT_VERSION=1.11.9
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 31 Mar 2023 00:45:10 GMT
VOLUME [/vault/logs]
# Fri, 31 Mar 2023 00:45:10 GMT
VOLUME [/vault/file]
# Fri, 31 Mar 2023 00:45:10 GMT
EXPOSE 8200
# Fri, 31 Mar 2023 00:45:10 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 31 Mar 2023 00:45:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 00:45:10 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ebcdc7813a6f23dca055a9257561eabd5fc5c5c21d7a72bb208439bd92f47f70`  
		Last Modified: Wed, 29 Mar 2023 17:39:28 GMT  
		Size: 2.8 MB (2835200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a5c9ef16ea3ede3ae5aaa411de6bdd28741ccc9612cea2c8ee802e31429be80`  
		Last Modified: Fri, 31 Mar 2023 00:45:56 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:303ee975ebcd4053083ff189dcc1fb8bb4ac3e6bc4f3b5977b188fe343bfd21f`  
		Last Modified: Fri, 31 Mar 2023 00:46:07 GMT  
		Size: 75.2 MB (75236842 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518fe2fffd607e5bed233b7580bbcab84df3763e9701704f72517ad5bc75231a`  
		Last Modified: Fri, 31 Mar 2023 00:45:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d7db704bb4dfa08944b31591300e93c99ae0623389363bdb944e8e76530d907`  
		Last Modified: Fri, 31 Mar 2023 00:45:56 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.12.5`

```console
$ docker pull vault@sha256:fa8fdfcaa027fa79310033a478140eed00b5180b9f8288703a1f9502561c3487
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.12.5` - linux; amd64

```console
$ docker pull vault@sha256:e7d7b1d0cbe8a5f32913bd797ba18fb318dc33e40c9386983a9aaff68d4c2227
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.0 MB (86001059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c489101c5a8948de8f419d440511bf8aad109bbd1d1f5a6b28ceae25d66ef901`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:37 GMT
ADD file:9663235f252e072c52b0f9e25845841e4321cce2caa7467a0d736c6003b05c00 in / 
# Wed, 29 Mar 2023 18:19:37 GMT
CMD ["/bin/sh"]
# Fri, 31 Mar 2023 00:26:14 GMT
ARG VAULT_VERSION=1.12.5
# Fri, 31 Mar 2023 00:26:15 GMT
# ARGS: VAULT_VERSION=1.12.5
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 31 Mar 2023 00:26:22 GMT
# ARGS: VAULT_VERSION=1.12.5
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 31 Mar 2023 00:26:23 GMT
# ARGS: VAULT_VERSION=1.12.5
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 31 Mar 2023 00:26:23 GMT
VOLUME [/vault/logs]
# Fri, 31 Mar 2023 00:26:23 GMT
VOLUME [/vault/file]
# Fri, 31 Mar 2023 00:26:24 GMT
EXPOSE 8200
# Fri, 31 Mar 2023 00:26:24 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 31 Mar 2023 00:26:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 00:26:24 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f7dab3ab2d6ec29aa28769bec35331fb485b5837501b1e8556413d8b5a79c9c8`  
		Last Modified: Wed, 29 Mar 2023 18:20:25 GMT  
		Size: 2.8 MB (2829647 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69eb2f8341669dd93bc4a36ec7e4ec70b22c40c66c694c6eb46b7782cbd27f19`  
		Last Modified: Fri, 31 Mar 2023 00:27:05 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9c24407d520ff4a02171268d843c660d48e0c0f5d8ac7b3925b5d2f1d2464a0`  
		Last Modified: Fri, 31 Mar 2023 00:27:14 GMT  
		Size: 83.2 MB (83168147 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61d38776c765e33f47fbd8c7d1af3a592ce053c438aaae5e3b7039406924a6c4`  
		Last Modified: Fri, 31 Mar 2023 00:27:05 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:90fb03b9dc9689f1023a07753a17322eda86d713d2679be795c5a96ad3cc4e82`  
		Last Modified: Fri, 31 Mar 2023 00:27:05 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.12.5` - linux; arm variant v6

```console
$ docker pull vault@sha256:84d2b62351312a0dea460c91ab5ccdb7a45d9e1f63bae21bf0b63963f98ae852
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **80.7 MB (80717384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e26e6e1e72bd0d6a97da3bde526607670f21d7343706c84cd8c58ed506d15d9d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:15 GMT
ADD file:1039802413c644346f599dac53a7c6dabd123027756231b9d8f64a1068c9779d in / 
# Wed, 29 Mar 2023 18:01:15 GMT
CMD ["/bin/sh"]
# Thu, 30 Mar 2023 23:49:42 GMT
ARG VAULT_VERSION=1.12.5
# Thu, 30 Mar 2023 23:49:42 GMT
# ARGS: VAULT_VERSION=1.12.5
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 30 Mar 2023 23:49:53 GMT
# ARGS: VAULT_VERSION=1.12.5
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 30 Mar 2023 23:49:54 GMT
# ARGS: VAULT_VERSION=1.12.5
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 30 Mar 2023 23:49:54 GMT
VOLUME [/vault/logs]
# Thu, 30 Mar 2023 23:49:54 GMT
VOLUME [/vault/file]
# Thu, 30 Mar 2023 23:49:54 GMT
EXPOSE 8200
# Thu, 30 Mar 2023 23:49:54 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 30 Mar 2023 23:49:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 30 Mar 2023 23:49:55 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ffeb76b9ee2f52d46487f4f9a7074ea62dea819a2dd53c9a2c6d703ca7b5aa06`  
		Last Modified: Wed, 29 Mar 2023 18:02:21 GMT  
		Size: 2.6 MB (2638259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:069762fc82984318ab8a181400661c749bd8ba0ede3e7f02038b9e0d84ceda9d`  
		Last Modified: Thu, 30 Mar 2023 23:50:36 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5ec3e47bb7256ef2b489091b7f178e8238aa07095ee237cfa030c2230e7ba56`  
		Last Modified: Thu, 30 Mar 2023 23:50:45 GMT  
		Size: 78.1 MB (78075855 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a6ae572acb00f9894844ebd2193bbaeccd39156895d2ad9a4c50adea93f40a5`  
		Last Modified: Thu, 30 Mar 2023 23:50:36 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0b151773fb4530a4101b9af9f3943a7141403fe54f0c042adab794b15176e1c`  
		Last Modified: Thu, 30 Mar 2023 23:50:36 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.12.5` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:791032b7172f07916946c1897569c54c21746751789e57f00eca82e551516f37
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.1 MB (81067877 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c0571b1896d1b8fd263a4de4fe9162ffc446842327a95fcc0d2109043d806856`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:39:25 GMT
ADD file:c3d52cc254959a9ff493e7347e6b1bc25c0ccfdcf9532dbf43173ddd182d0e4d in / 
# Wed, 29 Mar 2023 17:39:25 GMT
CMD ["/bin/sh"]
# Fri, 31 Mar 2023 00:47:11 GMT
ARG VAULT_VERSION=1.12.5
# Fri, 31 Mar 2023 00:47:12 GMT
# ARGS: VAULT_VERSION=1.12.5
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 31 Mar 2023 00:47:19 GMT
# ARGS: VAULT_VERSION=1.12.5
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 31 Mar 2023 00:47:21 GMT
# ARGS: VAULT_VERSION=1.12.5
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 31 Mar 2023 00:47:21 GMT
VOLUME [/vault/logs]
# Fri, 31 Mar 2023 00:47:21 GMT
VOLUME [/vault/file]
# Fri, 31 Mar 2023 00:47:21 GMT
EXPOSE 8200
# Fri, 31 Mar 2023 00:47:21 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 31 Mar 2023 00:47:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 00:47:21 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:422ed46b1a92579f7c475c0c19fade6880a8d98f23a2b4ccfb77c265d4f72dfc`  
		Last Modified: Wed, 29 Mar 2023 17:40:13 GMT  
		Size: 2.7 MB (2725148 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b4c27a3e7d4085f48563eadbee865397436f971e5f8f0670d466ec9f246b1d`  
		Last Modified: Fri, 31 Mar 2023 00:47:57 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:358767a7e9b58ea102b8eefb145c46c7174193ff0920ded9c8972123aafdd65f`  
		Last Modified: Fri, 31 Mar 2023 00:48:04 GMT  
		Size: 78.3 MB (78339461 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:56ad16384b58ef7ee19660b0f91b7be58bb1c76bbbdd82cca9d97b1bacbedf81`  
		Last Modified: Fri, 31 Mar 2023 00:47:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e3ce8e40cef8be2dbfa9c369c32302df383b553aae7344bdde2547787dd7485`  
		Last Modified: Fri, 31 Mar 2023 00:47:57 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.12.5` - linux; 386

```console
$ docker pull vault@sha256:8e33d0b3d44f204dd56edb6fb9c723e2177fb7d40953c26ae6d3d0978fdabc08
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.5 MB (82470966 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25eb822ae00c411f7a1631fa89347b7d9c11b3cc7071c91d4315fe5be1759ba0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:38 GMT
ADD file:0fbd9a88e784719a5d50377c069ea125f9a27568d6d02b43a9512c65ae72870d in / 
# Wed, 29 Mar 2023 17:38:39 GMT
CMD ["/bin/sh"]
# Fri, 31 Mar 2023 00:44:43 GMT
ARG VAULT_VERSION=1.12.5
# Fri, 31 Mar 2023 00:44:44 GMT
# ARGS: VAULT_VERSION=1.12.5
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 31 Mar 2023 00:44:55 GMT
# ARGS: VAULT_VERSION=1.12.5
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 31 Mar 2023 00:44:56 GMT
# ARGS: VAULT_VERSION=1.12.5
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 31 Mar 2023 00:44:56 GMT
VOLUME [/vault/logs]
# Fri, 31 Mar 2023 00:44:56 GMT
VOLUME [/vault/file]
# Fri, 31 Mar 2023 00:44:56 GMT
EXPOSE 8200
# Fri, 31 Mar 2023 00:44:57 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 31 Mar 2023 00:44:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 31 Mar 2023 00:44:57 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:ebcdc7813a6f23dca055a9257561eabd5fc5c5c21d7a72bb208439bd92f47f70`  
		Last Modified: Wed, 29 Mar 2023 17:39:28 GMT  
		Size: 2.8 MB (2835200 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3921467c630c4fe79f60dbe73dd9a9f200b39fd8d529edabb23a1b71db911a83`  
		Last Modified: Fri, 31 Mar 2023 00:45:38 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c210a9937ada09ab2cfa5e5a174be72f9e80a0e686cf4f24fe3ebd1d2291e2f3`  
		Last Modified: Fri, 31 Mar 2023 00:45:49 GMT  
		Size: 79.6 MB (79632499 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a25da182a43fd8a51915250923d279038c966b17fd16edb1b1466b0cb6d439`  
		Last Modified: Fri, 31 Mar 2023 00:45:38 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bd1c9b4955f82071499afafc9dcae610b0844795e64a191d9c93df1681a5162`  
		Last Modified: Fri, 31 Mar 2023 00:45:38 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.13.1`

```console
$ docker pull vault@sha256:2a83da216a42c8541a36038ff79a797e1f6a9c39dd64f38ca45e152c8ed68533
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.13.1` - linux; amd64

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

### `vault:1.13.1` - linux; arm variant v6

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

### `vault:1.13.1` - linux; arm64 variant v8

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

### `vault:1.13.1` - linux; 386

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
