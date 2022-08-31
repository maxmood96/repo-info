<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `vault`

-	[`vault:1.10.6`](#vault1106)
-	[`vault:1.11.3`](#vault1113)
-	[`vault:1.8.12`](#vault1812)
-	[`vault:1.9.9`](#vault199)
-	[`vault:latest`](#vaultlatest)

## `vault:1.10.6`

**does not exist** (yet?)

## `vault:1.11.3`

**does not exist** (yet?)

## `vault:1.8.12`

```console
$ docker pull vault@sha256:0cc664bf6b94b299b0d38324a568c472181395beffbbc2975ce0cfae3ffd4f3b
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.8.12` - linux; amd64

```console
$ docker pull vault@sha256:68f1682b1398535f86c3ecc09c9cde329520b4a67b801da5fa16c92d02641805
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.7 MB (70650989 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4df9d919fd4756f45ab5c06c05a9eaf2a30867eb5879d2f0859938450515a50f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 01:27:31 GMT
ARG VAULT_VERSION=1.8.12
# Wed, 10 Aug 2022 01:27:31 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 10 Aug 2022 01:27:39 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 10 Aug 2022 01:27:40 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 10 Aug 2022 01:27:40 GMT
VOLUME [/vault/logs]
# Wed, 10 Aug 2022 01:27:40 GMT
VOLUME [/vault/file]
# Wed, 10 Aug 2022 01:27:40 GMT
EXPOSE 8200
# Wed, 10 Aug 2022 01:27:40 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 Aug 2022 01:27:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 01:27:40 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53c699ea2f983cbe4bbb320b0b24d2ca4e1f5dab55991affbd9d716508728ce3`  
		Last Modified: Wed, 10 Aug 2022 01:28:41 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:589d0c73806458dde55a3c4388d26f54502d3f4e5abf10249a9e06737e51e54e`  
		Last Modified: Wed, 10 Aug 2022 01:28:51 GMT  
		Size: 67.8 MB (67820233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c5594347fcf83dd3374582fc6cb35e5570af2304daae67aabc85736eb5ea4c1`  
		Last Modified: Wed, 10 Aug 2022 01:28:42 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:957abd22bbfede163b1d7a2bf3fd8d4b02b7a3704e8effd5420d54bad2f97e65`  
		Last Modified: Wed, 10 Aug 2022 01:28:41 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.8.12` - linux; arm variant v6

```console
$ docker pull vault@sha256:df35696f78627af5c87335be699c09c3aaba3b57e88405a60339ff72ee87391b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (64979329 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b4b06af3699f89f815b16584b7140b34663df5a4b2abdd3d1bb61d4f00560294`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:35 GMT
ADD file:8ff80989f06f5a8ffe16c56e00538928dcb1e46faa2b58ab9c14c7227a6cd8f9 in / 
# Tue, 09 Aug 2022 17:49:35 GMT
CMD ["/bin/sh"]
# Thu, 11 Aug 2022 00:39:18 GMT
ARG VAULT_VERSION=1.8.12
# Thu, 11 Aug 2022 00:39:19 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 11 Aug 2022 00:39:27 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 11 Aug 2022 00:39:27 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 11 Aug 2022 00:39:27 GMT
VOLUME [/vault/logs]
# Thu, 11 Aug 2022 00:39:27 GMT
VOLUME [/vault/file]
# Thu, 11 Aug 2022 00:39:28 GMT
EXPOSE 8200
# Thu, 11 Aug 2022 00:39:28 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 11 Aug 2022 00:39:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Aug 2022 00:39:28 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:7d147289082e6aa6ef510c09d7c0ac8b5026e0b591f1bfcaf01ceada43c9ec65`  
		Last Modified: Tue, 09 Aug 2022 17:51:04 GMT  
		Size: 2.6 MB (2635498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80507948872f98adb21bf90308df85f8f14fd6bf78b494048a1c2df54173107e`  
		Last Modified: Thu, 11 Aug 2022 00:40:41 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8ee86e3c44c3a78d335c6dba79086c6a17794fd6688ab976211e81635162be7`  
		Last Modified: Thu, 11 Aug 2022 00:40:49 GMT  
		Size: 62.3 MB (62340561 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:85a18fa6d1ca7c11d0fa8d02521be3cbeb32f9ec098c947ba89f236c7a96e880`  
		Last Modified: Thu, 11 Aug 2022 00:40:42 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dfa1d16b2af971034dc6975b6af3c8c26b534193b95ffdda15f7a42e8351b02`  
		Last Modified: Thu, 11 Aug 2022 00:40:41 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.8.12` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:af9f850ac3772bc779d576ba64da9b1f56ee557f057dd2ebb2c32f101de83a28
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.9 MB (66912119 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7756cfd35375d5a8f6af3ba87bbfa6bb7bc6dce28aa686c8de4282ccf2eecf4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:59 GMT
ADD file:b312c8f512719efd09811d17c2b250bbad03cf3f90c135a00695cc8e152f4ee2 in / 
# Tue, 09 Aug 2022 17:39:59 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 06:22:40 GMT
ARG VAULT_VERSION=1.8.12
# Wed, 10 Aug 2022 06:22:41 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 10 Aug 2022 06:22:49 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 10 Aug 2022 06:22:49 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 10 Aug 2022 06:22:50 GMT
VOLUME [/vault/logs]
# Wed, 10 Aug 2022 06:22:51 GMT
VOLUME [/vault/file]
# Wed, 10 Aug 2022 06:22:52 GMT
EXPOSE 8200
# Wed, 10 Aug 2022 06:22:54 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 Aug 2022 06:22:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 06:22:55 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:90cda3b7c32511829cd5ae9074240c36c34507085acb6e55b96f993740d2be93`  
		Last Modified: Tue, 09 Aug 2022 17:41:06 GMT  
		Size: 2.7 MB (2722153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a4ff73e0df6cdb90ca1a83460da75b2cb653a02ea996b9c4acc2d7b36d6c475`  
		Last Modified: Wed, 10 Aug 2022 06:24:11 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e382d9dd47cfcba359cb759708414caaf1880e8e5afa9a5a365da38b2213232c`  
		Last Modified: Wed, 10 Aug 2022 06:24:19 GMT  
		Size: 64.2 MB (64186762 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9cec19ed89bb76bae1a3f36b5772229e77d13589beb6ba54f0bb6987dfaeef9`  
		Last Modified: Wed, 10 Aug 2022 06:24:11 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c4ebac347c03ab4322d1931725e558a8b0dbdedff1eeeb637fbdf869343f7f1`  
		Last Modified: Wed, 10 Aug 2022 06:24:11 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.8.12` - linux; 386

```console
$ docker pull vault@sha256:770e659d0eec23e23f4a01203b7b9bb6665cc7c2893d2e678743742f4101a5f2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.4 MB (68350476 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:706ae3042de1317568c9d824ac6096cbe0af6f93becc8ff08f4b5672c4c87599`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:54 GMT
ADD file:fea8a3ba06779852956b0d3a2dd7514ab33217b1fd395231864c443797f077f6 in / 
# Tue, 09 Aug 2022 17:38:54 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 00:14:46 GMT
ARG VAULT_VERSION=1.8.12
# Wed, 10 Aug 2022 00:14:47 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 10 Aug 2022 00:14:57 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 10 Aug 2022 00:14:57 GMT
# ARGS: VAULT_VERSION=1.8.12
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 10 Aug 2022 00:14:58 GMT
VOLUME [/vault/logs]
# Wed, 10 Aug 2022 00:14:59 GMT
VOLUME [/vault/file]
# Wed, 10 Aug 2022 00:15:00 GMT
EXPOSE 8200
# Wed, 10 Aug 2022 00:15:02 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 Aug 2022 00:15:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 00:15:03 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:2c44f983a875883421e7d5bc471f6437e0e377e6e7343b52c856caee71064d31`  
		Last Modified: Tue, 09 Aug 2022 17:40:01 GMT  
		Size: 2.8 MB (2832612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30d5d18c74e1fbdfe601565cc2bc0d42ac70a255339ed77f0a129d71fef15c5c`  
		Last Modified: Wed, 10 Aug 2022 00:16:30 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81c502c38af5250b35fe68bc131779469e8da9589b6a054257fcc0a56787b918`  
		Last Modified: Wed, 10 Aug 2022 00:16:37 GMT  
		Size: 65.5 MB (65514657 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38c00963d2baa2486178f1d1d0cf2685e4b381f62bc3616e7ea48b1584c81787`  
		Last Modified: Wed, 10 Aug 2022 00:16:30 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68592ac5ae287cfe31dac3a2bb3bebbbb2088143f4200e61330c5d6635d63aca`  
		Last Modified: Wed, 10 Aug 2022 00:16:30 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.9.9`

**does not exist** (yet?)

## `vault:latest`

```console
$ docker pull vault@sha256:f2c0f82d1bde88a6608f26468258306e48ac46a4d353db2151e26e0fd00928bb
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:7a238778738551ab26e07ef2c4ac9d9d9e8d393ec9e766301c9b3bb0fa5f2b55
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.5 MB (77492763 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22fdc6314051df714eb280680c24524ed01d0ed2eddff1358cc40d528c82579e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:07 GMT
ADD file:b9bd10cf83356cb7281baa0fbaca5186cf27491f59eda87abe57f83a5aaf5ec1 in / 
# Tue, 09 Aug 2022 17:20:08 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 01:26:51 GMT
ARG VAULT_VERSION=1.11.2
# Wed, 10 Aug 2022 01:26:52 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 10 Aug 2022 01:27:00 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 10 Aug 2022 01:27:01 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 10 Aug 2022 01:27:01 GMT
VOLUME [/vault/logs]
# Wed, 10 Aug 2022 01:27:01 GMT
VOLUME [/vault/file]
# Wed, 10 Aug 2022 01:27:01 GMT
EXPOSE 8200
# Wed, 10 Aug 2022 01:27:01 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 Aug 2022 01:27:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 01:27:01 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:c7ed990a2339ee598662849de4f56e2241399f5a32340c8c4a7bbd5378a12b5f`  
		Last Modified: Tue, 09 Aug 2022 17:21:06 GMT  
		Size: 2.8 MB (2827489 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8967aa5130c8a6f6bb7143c8391df393368db6921ab770555efde013985a9d28`  
		Last Modified: Wed, 10 Aug 2022 01:27:51 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db9d0afc6ab490c62cd716176a04cfd75c36714cb67b9e30a2cda0ef0be75f0`  
		Last Modified: Wed, 10 Aug 2022 01:28:01 GMT  
		Size: 74.7 MB (74662006 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0119f940dd249e511bdcf111cbe3b317d64b16eaa192d25fb6b9d83326f33acb`  
		Last Modified: Wed, 10 Aug 2022 01:27:51 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98184bebb2e9dc29170e6960d8239418e57b92f48ef4edd5a62482071df9c373`  
		Last Modified: Wed, 10 Aug 2022 01:27:51 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:9ce1ce2a1aba504a1a02cd1f917a1d97411882dddcfd340a1385e94192dbd220
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.3 MB (70260923 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44017ce173fa5a5ed60d44736f6d5c3814bd716a24a133d7d2e8377bf4758447`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:35 GMT
ADD file:8ff80989f06f5a8ffe16c56e00538928dcb1e46faa2b58ab9c14c7227a6cd8f9 in / 
# Tue, 09 Aug 2022 17:49:35 GMT
CMD ["/bin/sh"]
# Thu, 11 Aug 2022 00:38:29 GMT
ARG VAULT_VERSION=1.11.2
# Thu, 11 Aug 2022 00:38:29 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 11 Aug 2022 00:38:39 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 11 Aug 2022 00:38:40 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 11 Aug 2022 00:38:40 GMT
VOLUME [/vault/logs]
# Thu, 11 Aug 2022 00:38:40 GMT
VOLUME [/vault/file]
# Thu, 11 Aug 2022 00:38:40 GMT
EXPOSE 8200
# Thu, 11 Aug 2022 00:38:40 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 11 Aug 2022 00:38:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 11 Aug 2022 00:38:40 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:7d147289082e6aa6ef510c09d7c0ac8b5026e0b591f1bfcaf01ceada43c9ec65`  
		Last Modified: Tue, 09 Aug 2022 17:51:04 GMT  
		Size: 2.6 MB (2635498 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6f022ae8acd57774b0fc99bff80118bd5f9dacd749f4df8487481645a168438c`  
		Last Modified: Thu, 11 Aug 2022 00:39:48 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dd633fbb4c2d3817516b124f430ecc1a5529194056b5fe01a2cc8d4c79a10f6b`  
		Last Modified: Thu, 11 Aug 2022 00:39:57 GMT  
		Size: 67.6 MB (67622154 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e5a54af2f7e4af80f38c901a6475dbbdb65cc7a6c13dd532dcd5d9e4c335919`  
		Last Modified: Thu, 11 Aug 2022 00:39:48 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc50ef627848a9ab6ccd550b2d5ea4af066ea58fa659d547b7fdcbcb5d0af71f`  
		Last Modified: Thu, 11 Aug 2022 00:39:48 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:80151a9dbdd243c62774b8a1113224c6f519194e6d4571634718d111de4ce50e
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.3 MB (72285316 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9f88fbcce3222d1f7b9912a9b142a8e9e5f245d278638b972bc1eed09289c78`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:59 GMT
ADD file:b312c8f512719efd09811d17c2b250bbad03cf3f90c135a00695cc8e152f4ee2 in / 
# Tue, 09 Aug 2022 17:39:59 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 06:21:33 GMT
ARG VAULT_VERSION=1.11.2
# Wed, 10 Aug 2022 06:21:34 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 10 Aug 2022 06:21:43 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 10 Aug 2022 06:21:44 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 10 Aug 2022 06:21:45 GMT
VOLUME [/vault/logs]
# Wed, 10 Aug 2022 06:21:46 GMT
VOLUME [/vault/file]
# Wed, 10 Aug 2022 06:21:47 GMT
EXPOSE 8200
# Wed, 10 Aug 2022 06:21:49 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 Aug 2022 06:21:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 06:21:50 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:90cda3b7c32511829cd5ae9074240c36c34507085acb6e55b96f993740d2be93`  
		Last Modified: Tue, 09 Aug 2022 17:41:06 GMT  
		Size: 2.7 MB (2722153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef788ff86a429eec5ae34e7396476bf848be89528ee0c96459e592c54feeed2c`  
		Last Modified: Wed, 10 Aug 2022 06:23:16 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b036828efcfb812eb451a703d86dbba576fe28421489fa6275556eb67492dcf`  
		Last Modified: Wed, 10 Aug 2022 06:23:25 GMT  
		Size: 69.6 MB (69559958 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20314912d5144dfe025ddedf1e6e18748a9822da6d162118f0d6b2defff4a25b`  
		Last Modified: Wed, 10 Aug 2022 06:23:16 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8371e722544e476f70a12d21ea938e136e06b2199fbf7dfc1d7beb3e3250c32b`  
		Last Modified: Wed, 10 Aug 2022 06:23:16 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:556137692bc84155dc5886a12ae852d4ce1d5bb058e207d43a07f5ce716f0808
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **73.6 MB (73567722 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a9c7a4e16b968a99b1ef223d5cde6b79ad51103581802e72741be70c9ea5db3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:54 GMT
ADD file:fea8a3ba06779852956b0d3a2dd7514ab33217b1fd395231864c443797f077f6 in / 
# Tue, 09 Aug 2022 17:38:54 GMT
CMD ["/bin/sh"]
# Wed, 10 Aug 2022 00:13:39 GMT
ARG VAULT_VERSION=1.11.2
# Wed, 10 Aug 2022 00:13:40 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 10 Aug 2022 00:13:49 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 10 Aug 2022 00:13:50 GMT
# ARGS: VAULT_VERSION=1.11.2
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 10 Aug 2022 00:13:51 GMT
VOLUME [/vault/logs]
# Wed, 10 Aug 2022 00:13:52 GMT
VOLUME [/vault/file]
# Wed, 10 Aug 2022 00:13:53 GMT
EXPOSE 8200
# Wed, 10 Aug 2022 00:13:55 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 10 Aug 2022 00:13:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 10 Aug 2022 00:13:56 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:2c44f983a875883421e7d5bc471f6437e0e377e6e7343b52c856caee71064d31`  
		Last Modified: Tue, 09 Aug 2022 17:40:01 GMT  
		Size: 2.8 MB (2832612 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5fdb4858833cdfc5a5714d5a19c93b337a0e778ec7d80ef77189fac0471c7566`  
		Last Modified: Wed, 10 Aug 2022 00:15:25 GMT  
		Size: 1.2 KB (1237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1cb24cb72e1a2fdb06de8d1a5f75cd0a549f107b77909b2a0c1b20f9e2d74d29`  
		Last Modified: Wed, 10 Aug 2022 00:15:36 GMT  
		Size: 70.7 MB (70731906 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a7744188d2a7166aef058bb6d424153beba212e4c8749f465cf86914a226ca7`  
		Last Modified: Wed, 10 Aug 2022 00:15:25 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e90460ac0bbb803713f9962bf787cb7021494e0163af9926e3ac5956d65c240d`  
		Last Modified: Wed, 10 Aug 2022 00:15:25 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
