<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `vault`

-	[`vault:1.11.11`](#vault11111)
-	[`vault:1.12.7`](#vault1127)
-	[`vault:1.13.3`](#vault1133)

## `vault:1.11.11`

```console
$ docker pull vault@sha256:f58e102d587366567b7d6b804281f9b211fddec4438f09dfd31c892a372c21e8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.11.11` - linux; amd64

```console
$ docker pull vault@sha256:5b8b05e2084bd603ac432f3ff0bd583363804d208d6194022d7fe712bac188a3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81825297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1fe02c10c4b2372110afbcafdbe701abb88adf3411fb6c956557d738756d028b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:54:34 GMT
ARG VAULT_VERSION=1.11.11
# Sat, 27 Jan 2024 03:54:34 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN addgroup vault &&     adduser -S -G vault vault
# Sat, 27 Jan 2024 03:54:43 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Sat, 27 Jan 2024 03:54:44 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Sat, 27 Jan 2024 03:54:44 GMT
VOLUME [/vault/logs]
# Sat, 27 Jan 2024 03:54:44 GMT
VOLUME [/vault/file]
# Sat, 27 Jan 2024 03:54:44 GMT
EXPOSE 8200
# Sat, 27 Jan 2024 03:54:44 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 27 Jan 2024 03:54:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:54:44 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6173d10bee38bc61db135f78640fac2ea964777e14750a4373966d716924baf`  
		Last Modified: Sat, 27 Jan 2024 03:55:29 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a811318940f724d41a915fefd518a8ca557c0f56d5ec18cd30ccc23528355f28`  
		Last Modified: Sat, 27 Jan 2024 03:55:38 GMT  
		Size: 78.4 MB (78419487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf79f24fee50f56f82fe0a302ac0e305f73d1fdf1a34e3b8ea17fe7c7f8b451`  
		Last Modified: Sat, 27 Jan 2024 03:55:30 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:08640351d2284f2975194da863efcc4d9218b342c1fd14b8b48fdd7ad173fc43`  
		Last Modified: Sat, 27 Jan 2024 03:55:30 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.11.11` - linux; arm variant v6

```console
$ docker pull vault@sha256:201114bde0b07eb61117b65f844e663194e049885873ecdfae416aedc648d3a8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76870504 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1f23782eaa387a00ab4fb6a61f536cb64f97b8cbc773379e6fac042a394809f3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:39:43 GMT
ARG VAULT_VERSION=1.11.11
# Sat, 16 Mar 2024 06:39:43 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN addgroup vault &&     adduser -S -G vault vault
# Sat, 16 Mar 2024 06:39:53 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Sat, 16 Mar 2024 06:39:54 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Sat, 16 Mar 2024 06:39:54 GMT
VOLUME [/vault/logs]
# Sat, 16 Mar 2024 06:39:54 GMT
VOLUME [/vault/file]
# Sat, 16 Mar 2024 06:39:54 GMT
EXPOSE 8200
# Sat, 16 Mar 2024 06:39:54 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 16 Mar 2024 06:39:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 06:39:54 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a0df8eaafada82dc098bfc407cdf776eb689d9c97e0e7a11a8976c76a253f2d`  
		Last Modified: Sat, 16 Mar 2024 06:40:35 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce7f8848de05de48af0db5ef3fd1bbb78492e4c28a10419e3bdb2d4849b13935`  
		Last Modified: Sat, 16 Mar 2024 06:40:44 GMT  
		Size: 73.7 MB (73720171 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60a45df27b68c3973bdd77c1759cecdcb5c66e4d63676834aead19e3fba05e50`  
		Last Modified: Sat, 16 Mar 2024 06:40:35 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:27bc5f6524c2d7a76fc91271f81cb67a9ddc4db0151338e54bdfb562a972d4e2`  
		Last Modified: Sat, 16 Mar 2024 06:40:35 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.11.11` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:6196305b71d1f624311a6662dfe04cced18c22fa0efa5cbcd8066f17b59cfc76
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77144294 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d54d10d9c8088b6115cecfef092c074122a888a8ede4bc454568b70d4db01156`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:17:18 GMT
ARG VAULT_VERSION=1.11.11
# Sat, 16 Mar 2024 05:17:18 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN addgroup vault &&     adduser -S -G vault vault
# Sat, 16 Mar 2024 05:17:25 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Sat, 16 Mar 2024 05:17:26 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Sat, 16 Mar 2024 05:17:27 GMT
VOLUME [/vault/logs]
# Sat, 16 Mar 2024 05:17:27 GMT
VOLUME [/vault/file]
# Sat, 16 Mar 2024 05:17:27 GMT
EXPOSE 8200
# Sat, 16 Mar 2024 05:17:27 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 16 Mar 2024 05:17:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:17:27 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651a2e8695fa5bc10a37953a8416a94ef6d9d68309497c691779beb1b1677bcb`  
		Last Modified: Sat, 16 Mar 2024 05:18:00 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1f013d36e33be88c8dd8245f0dd69343fda5d9c57213dbfe32d90ed4ccd5913`  
		Last Modified: Sat, 16 Mar 2024 05:18:06 GMT  
		Size: 73.8 MB (73807660 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:112ad639eafc05c5f76d20e0379ada9dfec9c7760fd69b8acbb0427d78a428f2`  
		Last Modified: Sat, 16 Mar 2024 05:18:00 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9307050aeda6fc4033d59fee3566d92485ba3f63594a6bfbc3bf682a63c29f45`  
		Last Modified: Sat, 16 Mar 2024 05:18:00 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.11.11` - linux; 386

```console
$ docker pull vault@sha256:37e550351eac37a407577f63bafa5003340ebec52cf874ae1f5b0671b169c221
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78460239 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:36b8731fad21c0626e68481c96dc34e27e4871eac653f3211b29b9447b4ced44`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:09:22 GMT
ARG VAULT_VERSION=1.11.11
# Sat, 16 Mar 2024 05:09:23 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN addgroup vault &&     adduser -S -G vault vault
# Sat, 16 Mar 2024 05:09:34 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Sat, 16 Mar 2024 05:09:35 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Sat, 16 Mar 2024 05:09:35 GMT
VOLUME [/vault/logs]
# Sat, 16 Mar 2024 05:09:35 GMT
VOLUME [/vault/file]
# Sat, 16 Mar 2024 05:09:36 GMT
EXPOSE 8200
# Sat, 16 Mar 2024 05:09:36 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 16 Mar 2024 05:09:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:09:36 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e240deebc391ad09d2b0d762c8a1eee26171c85abb55aabad769c7d29fa9f9f`  
		Last Modified: Sat, 16 Mar 2024 05:10:25 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01d0603661bed89cc463798ec5f299bea0a4bcd9916f3fc94d3111bc95ad04a0`  
		Last Modified: Sat, 16 Mar 2024 05:10:37 GMT  
		Size: 75.2 MB (75217898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e774e8ffff95de0fc5327d5898b6bf7394aa6862adfffd5659ad57f77755cbe`  
		Last Modified: Sat, 16 Mar 2024 05:10:25 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd0ca0cb03ec753c792efb79392e55eb4d7cb8d5d8c64309847db51f17d1fabd`  
		Last Modified: Sat, 16 Mar 2024 05:10:25 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.12.7`

```console
$ docker pull vault@sha256:108b789b454b426c757c05e52ea6bdfc1652a9a15ce3674a7d1ab9feca210907
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.12.7` - linux; amd64

```console
$ docker pull vault@sha256:9ef554564a4a1ca90c0024ba541a1cada21c64af3242c44214fabbdec9988e28
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86571265 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:73d8bc3ae16ffda8a86c790d7272d0aa18c0f13ae8510134fd1b14e4e7363c69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:54:19 GMT
ARG VAULT_VERSION=1.12.7
# Sat, 27 Jan 2024 03:54:20 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN addgroup vault &&     adduser -S -G vault vault
# Sat, 27 Jan 2024 03:54:28 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Sat, 27 Jan 2024 03:54:29 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Sat, 27 Jan 2024 03:54:29 GMT
VOLUME [/vault/logs]
# Sat, 27 Jan 2024 03:54:29 GMT
VOLUME [/vault/file]
# Sat, 27 Jan 2024 03:54:29 GMT
EXPOSE 8200
# Sat, 27 Jan 2024 03:54:29 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 27 Jan 2024 03:54:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:54:29 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af9866ad2a5630431447e66636e9a23ba0f0c854dfff334f7eb32c54be9cb29a`  
		Last Modified: Sat, 27 Jan 2024 03:55:11 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e55998962c52b3b41517c39ab0257db56ec0f1530116505d2bbdad56b0a5b4`  
		Last Modified: Sat, 27 Jan 2024 03:55:23 GMT  
		Size: 83.2 MB (83165459 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7963751a4f785075325ecf95ddbc48068a97fb19a6efcc3ca08d6d9f1788e4d3`  
		Last Modified: Sat, 27 Jan 2024 03:55:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d3b5913a7627a15104cf184c3abb7b5e48501bc5306a376a32739203207e041d`  
		Last Modified: Sat, 27 Jan 2024 03:55:11 GMT  
		Size: 1.8 KB (1809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.12.7` - linux; arm variant v6

```console
$ docker pull vault@sha256:f2779336182a1a8de31e25fccfd858fa82ad78e66df0406c9a403c306f563e9a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81228766 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:413d12fb78ac676e98f8e5350b26c98af691c1b011fa9a0ef0932e9900f03c72`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:39:27 GMT
ARG VAULT_VERSION=1.12.7
# Sat, 16 Mar 2024 06:39:27 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN addgroup vault &&     adduser -S -G vault vault
# Sat, 16 Mar 2024 06:39:38 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Sat, 16 Mar 2024 06:39:39 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Sat, 16 Mar 2024 06:39:39 GMT
VOLUME [/vault/logs]
# Sat, 16 Mar 2024 06:39:39 GMT
VOLUME [/vault/file]
# Sat, 16 Mar 2024 06:39:39 GMT
EXPOSE 8200
# Sat, 16 Mar 2024 06:39:39 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 16 Mar 2024 06:39:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 06:39:40 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973bd61345bb259ed62b5d8ee59a967c4e00ca4062c335300af3ac7dcde1c274`  
		Last Modified: Sat, 16 Mar 2024 06:40:19 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b57c9d4e5be6463b7923c2a5c4c3bf85323acd7b84c93580c8262657ea9b2a1`  
		Last Modified: Sat, 16 Mar 2024 06:40:28 GMT  
		Size: 78.1 MB (78078431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43fca3a19b75f57bb6bc2f0e6ea103f139d0501e32079637c1a6ebdd0b80e191`  
		Last Modified: Sat, 16 Mar 2024 06:40:19 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57b5822946b2bc380e9375c5c73581ec43629758d6f52e0bc33771a4889fd94a`  
		Last Modified: Sat, 16 Mar 2024 06:40:19 GMT  
		Size: 1.8 KB (1816 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.12.7` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:8259754ca0f49888e454e19b38d99e91631f691c45be508111243534c190de13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81675247 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8001a4cf12b6e81172c13bb05be0a3d55cb172bdcbfc18a7a14694e15c7aa724`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:17:06 GMT
ARG VAULT_VERSION=1.12.7
# Sat, 16 Mar 2024 05:17:06 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN addgroup vault &&     adduser -S -G vault vault
# Sat, 16 Mar 2024 05:17:13 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Sat, 16 Mar 2024 05:17:15 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Sat, 16 Mar 2024 05:17:15 GMT
VOLUME [/vault/logs]
# Sat, 16 Mar 2024 05:17:15 GMT
VOLUME [/vault/file]
# Sat, 16 Mar 2024 05:17:15 GMT
EXPOSE 8200
# Sat, 16 Mar 2024 05:17:15 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 16 Mar 2024 05:17:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:17:15 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aff6839d79d72fda8160a1a5f2b286c63af011b8a0116eed9631cec4c4297d3`  
		Last Modified: Sat, 16 Mar 2024 05:17:48 GMT  
		Size: 1.3 KB (1272 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aa55cc16a89763275deb50ddee7130162d9ebaced4a7a5ada44f641ac26f0ce`  
		Last Modified: Sat, 16 Mar 2024 05:17:54 GMT  
		Size: 78.3 MB (78338611 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30c83c1ccbb729740625af8b6b6068710b3b9e0adab0e0fd40f6ca3672f3414f`  
		Last Modified: Sat, 16 Mar 2024 05:17:48 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23260fd080bab6b414271f73c60cffdf24b97663b249072e2f56ea41e1f412bc`  
		Last Modified: Sat, 16 Mar 2024 05:17:48 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.12.7` - linux; 386

```console
$ docker pull vault@sha256:1464fbfa0025699613326d8faaecc33de9c57213c9eb3507dffc0afe7ffbf8d9
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82844297 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bab7a316c45b2ec6abc445e8b302eb4990e8879005f85bf65ca5568bd215e9be`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:09:03 GMT
ARG VAULT_VERSION=1.12.7
# Sat, 16 Mar 2024 05:09:03 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN addgroup vault &&     adduser -S -G vault vault
# Sat, 16 Mar 2024 05:09:15 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Sat, 16 Mar 2024 05:09:16 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Sat, 16 Mar 2024 05:09:17 GMT
VOLUME [/vault/logs]
# Sat, 16 Mar 2024 05:09:17 GMT
VOLUME [/vault/file]
# Sat, 16 Mar 2024 05:09:17 GMT
EXPOSE 8200
# Sat, 16 Mar 2024 05:09:17 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 16 Mar 2024 05:09:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:09:17 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d385288c0e6bec2a774465973349ce4a8aa3afc12d6a703b7026e1bc5c35e21`  
		Last Modified: Sat, 16 Mar 2024 05:10:06 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e63886443052e6fcb5ab03d79cba8d7b0706598a89f5a4002d17e200b794ca5`  
		Last Modified: Sat, 16 Mar 2024 05:10:18 GMT  
		Size: 79.6 MB (79601959 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b00aac8cd39ffcf6ca32b9a7b315702062a002dfbb899e00f257a07cb913bcf8`  
		Last Modified: Sat, 16 Mar 2024 05:10:06 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:02ab531939db0c9dd3850dd3cfe3eb6fd670c35270dcc7a284d9fbb365572c8a`  
		Last Modified: Sat, 16 Mar 2024 05:10:06 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.13.3`

```console
$ docker pull vault@sha256:efca02e5d8c05c4207f255e54be5d9796e3c1bea34c941c47386180c4220234d
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.13.3` - linux; amd64

```console
$ docker pull vault@sha256:575ab3ff8a94d2fabbf11c612737ba43228c8c75624148e3753251ce74fb2eb6
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97612104 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5b948ecc0140cb256c0b5aba5f0e2a3edcd422d5dd80e544761c2ad6b37c836`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Sat, 27 Jan 2024 00:30:56 GMT
ADD file:8729f9c0258836b640e9e789c7ab029cf4547e0596557d54dd4a4d7d8e4a785f in / 
# Sat, 27 Jan 2024 00:30:56 GMT
CMD ["/bin/sh"]
# Sat, 27 Jan 2024 03:54:04 GMT
ARG VAULT_VERSION=1.13.3
# Sat, 27 Jan 2024 03:54:05 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN addgroup vault &&     adduser -S -G vault vault
# Sat, 27 Jan 2024 03:54:13 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Sat, 27 Jan 2024 03:54:14 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Sat, 27 Jan 2024 03:54:14 GMT
VOLUME [/vault/logs]
# Sat, 27 Jan 2024 03:54:15 GMT
VOLUME [/vault/file]
# Sat, 27 Jan 2024 03:54:15 GMT
EXPOSE 8200
# Sat, 27 Jan 2024 03:54:15 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 27 Jan 2024 03:54:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 27 Jan 2024 03:54:15 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:619be1103602d98e1963557998c954c892b3872986c27365e9f651f5bc27cab8`  
		Last Modified: Sat, 27 Jan 2024 00:31:36 GMT  
		Size: 3.4 MB (3402542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b881b8ce5c4e2f5afc175246433e032c15c05b470af780f0e7d3be0ace695ea7`  
		Last Modified: Sat, 27 Jan 2024 03:54:54 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:71eb4bbfa91d89294c1f35c5fe132afcb1e4a957ac94c5576ae0b4488cec2343`  
		Last Modified: Sat, 27 Jan 2024 03:55:04 GMT  
		Size: 94.2 MB (94206292 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b3a9527ca1fd896109f866f6b237dc9781be9a97d233b55146eaffc90b93a79`  
		Last Modified: Sat, 27 Jan 2024 03:54:54 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a81879914643cca206691519f8215117a2ae283b13f0aef1af4ad94527b95930`  
		Last Modified: Sat, 27 Jan 2024 03:54:54 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.13.3` - linux; arm variant v6

```console
$ docker pull vault@sha256:2e881a47821757e59ac4acc992d466e842b504ca8a1d7059fcf0f42d04e29aee
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91637773 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93c86834291bd1385cf46855b341535781b92b81c9a2420d51e602461b126e66`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 26 Jan 2024 23:49:20 GMT
ADD file:2aed4bf330381a82ec856eec00520036b6dd25910f7a42a0ac045d58ba2e08b5 in / 
# Fri, 26 Jan 2024 23:49:20 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 06:39:10 GMT
ARG VAULT_VERSION=1.13.3
# Sat, 16 Mar 2024 06:39:11 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN addgroup vault &&     adduser -S -G vault vault
# Sat, 16 Mar 2024 06:39:22 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Sat, 16 Mar 2024 06:39:23 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Sat, 16 Mar 2024 06:39:23 GMT
VOLUME [/vault/logs]
# Sat, 16 Mar 2024 06:39:23 GMT
VOLUME [/vault/file]
# Sat, 16 Mar 2024 06:39:23 GMT
EXPOSE 8200
# Sat, 16 Mar 2024 06:39:23 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 16 Mar 2024 06:39:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 06:39:24 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:bbb9926773f935f9bdf6315280ab3ea8b65cff91f2d416a791b5508579a3536c`  
		Last Modified: Fri, 26 Jan 2024 23:49:52 GMT  
		Size: 3.1 MB (3147059 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1af888a0e0d115526eb86cc56e3f045315e402c9704f9d07f84fdc0f811c9023`  
		Last Modified: Sat, 16 Mar 2024 06:40:02 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06e8a31809d991904ef04fc2cae25df96b7f5942d29c8b387ef75a929bbd59b1`  
		Last Modified: Sat, 16 Mar 2024 06:40:12 GMT  
		Size: 88.5 MB (88487439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c582f8d87054e568904e45c6ffae70269a4dd5625afb52e1f72c0fc3c24d882`  
		Last Modified: Sat, 16 Mar 2024 06:40:02 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50ab7c67c0a41030bcd27fdecc8d4ca99e239cb73f0e0b6d2da8ed3c42dc8338`  
		Last Modified: Sat, 16 Mar 2024 06:40:02 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.13.3` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:d14303dcbaef3f0f54676f94ca64d8fa7712bd1a0eb3647d57d8a20957c7544d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92163000 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f336f91e2f05f231fead3f7c800c8082e84e9aa43c8a4de5b62853dd525c0af1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 26 Jan 2024 23:44:55 GMT
ADD file:6dc287a22d6cc7723b0576dd3a9a644468d133c54d42c8a8eda403e3117648f7 in / 
# Fri, 26 Jan 2024 23:44:55 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:16:52 GMT
ARG VAULT_VERSION=1.13.3
# Sat, 16 Mar 2024 05:16:53 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN addgroup vault &&     adduser -S -G vault vault
# Sat, 16 Mar 2024 05:17:00 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Sat, 16 Mar 2024 05:17:02 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Sat, 16 Mar 2024 05:17:02 GMT
VOLUME [/vault/logs]
# Sat, 16 Mar 2024 05:17:02 GMT
VOLUME [/vault/file]
# Sat, 16 Mar 2024 05:17:02 GMT
EXPOSE 8200
# Sat, 16 Mar 2024 05:17:02 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 16 Mar 2024 05:17:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:17:02 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:c6b39de5b33961661dc939b997cc1d30cda01e38005a6c6625fd9c7e748bab44`  
		Last Modified: Fri, 26 Jan 2024 23:45:31 GMT  
		Size: 3.3 MB (3333361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d421e8c09e1413b0dbc3f4cd87105b8fe2778071294f9225e24d5239361df1c`  
		Last Modified: Sat, 16 Mar 2024 05:17:34 GMT  
		Size: 1.3 KB (1275 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9383f271018927a34878bdcca6dd506d5edaf0d3ede9bb7babd3e15d685376c7`  
		Last Modified: Sat, 16 Mar 2024 05:17:42 GMT  
		Size: 88.8 MB (88826364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76257ff1c0faf6ed4d9cdb468d858df6269f2645c6d0c555a8e8cec3c295717a`  
		Last Modified: Sat, 16 Mar 2024 05:17:34 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17ef69ee2b64bbcec70af57828f637505ee6acaf8b13b75437f1d17ba6305edb`  
		Last Modified: Sat, 16 Mar 2024 05:17:34 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.13.3` - linux; 386

```console
$ docker pull vault@sha256:bd75bcc64a7426be6b3ffd0dc272da683a037c3281d43875f1b2fed74d53f9ef
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93259356 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c6497d6f3b52c76b6f1a7d36e0fe561ee43492ba62325ad62cdad0677c2568a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Sat, 27 Jan 2024 00:38:23 GMT
ADD file:947294f5c09da3491734668abe74ce7c80f0034ae27d570578242b03ab6876a7 in / 
# Sat, 27 Jan 2024 00:38:23 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 05:08:43 GMT
ARG VAULT_VERSION=1.13.3
# Sat, 16 Mar 2024 05:08:44 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN addgroup vault &&     adduser -S -G vault vault
# Sat, 16 Mar 2024 05:08:56 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Sat, 16 Mar 2024 05:08:58 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Sat, 16 Mar 2024 05:08:58 GMT
VOLUME [/vault/logs]
# Sat, 16 Mar 2024 05:08:58 GMT
VOLUME [/vault/file]
# Sat, 16 Mar 2024 05:08:58 GMT
EXPOSE 8200
# Sat, 16 Mar 2024 05:08:58 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 16 Mar 2024 05:08:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 05:08:58 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:282e237e8e01cf628ae91590e0a44bcf58df98bbe01e9e62dadf2e94cd6301a0`  
		Last Modified: Sat, 27 Jan 2024 00:38:59 GMT  
		Size: 3.2 MB (3239065 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05673b90eed72b197234c786e1a9302fd8be9dce96df6fd81e796124f02ecb1`  
		Last Modified: Sat, 16 Mar 2024 05:09:45 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59e4dfc91532df12f93c5fb6089901309f94e96752a7161d318ea687db96265`  
		Last Modified: Sat, 16 Mar 2024 05:10:00 GMT  
		Size: 90.0 MB (90017019 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfbe95419b0ca6d4b514401d71b5dd431543900a5fee6304c866231f71442350`  
		Last Modified: Sat, 16 Mar 2024 05:09:45 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d19e8fc94163ff3dc23996fe8306830af5f6f056a120ef9ea4f3bc09b4a79edf`  
		Last Modified: Sat, 16 Mar 2024 05:09:45 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
