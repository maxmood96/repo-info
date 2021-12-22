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
