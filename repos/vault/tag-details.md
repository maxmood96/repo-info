<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `vault`

-	[`vault:1.5.8`](#vault158)
-	[`vault:1.6.4`](#vault164)
-	[`vault:1.7.1`](#vault171)
-	[`vault:latest`](#vaultlatest)

## `vault:1.5.8`

```console
$ docker pull vault@sha256:3b2209bedb1bbc70315fcd9e2187a49a1359f8f6f46cca7a51efcadb461fe98a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.5.8` - linux; amd64

```console
$ docker pull vault@sha256:cda92163485b23394603ff9e9686bb15825fab55423cec56d08c9854f36408bb
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55085644 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:382a655ce99daa8df42b12cffdb2596ce0f918ebf2cc37268095ef9a3f254d1f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 01:12:01 GMT
ARG VAULT_VERSION=1.5.8
# Thu, 22 Apr 2021 01:12:02 GMT
# ARGS: VAULT_VERSION=1.5.8
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 22 Apr 2021 01:12:08 GMT
# ARGS: VAULT_VERSION=1.5.8
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 22 Apr 2021 01:12:09 GMT
# ARGS: VAULT_VERSION=1.5.8
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 22 Apr 2021 01:12:09 GMT
VOLUME [/vault/logs]
# Thu, 22 Apr 2021 01:12:09 GMT
VOLUME [/vault/file]
# Thu, 22 Apr 2021 01:12:09 GMT
EXPOSE 8200
# Thu, 22 Apr 2021 01:12:10 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Apr 2021 01:12:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 01:12:10 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9512924e1f2c73fffbee79c2475231408d36476227ebe6dbc4ed48dd94a2c9`  
		Last Modified: Thu, 22 Apr 2021 01:12:59 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f328efea579ec1802afe73dfdd7674b2d431807f64c2ff200db0a2b120e756da`  
		Last Modified: Thu, 22 Apr 2021 01:13:08 GMT  
		Size: 52.3 MB (52270409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:03f4b3d754e1168b1d101ca6de40106c44aa15059c51ae61aa18f08b145a4f37`  
		Last Modified: Thu, 22 Apr 2021 01:12:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4816b1580929932ba5e934b0b470d182f51d2770f364127a194968e69e3f9458`  
		Last Modified: Thu, 22 Apr 2021 01:12:59 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.5.8` - linux; arm variant v6

```console
$ docker pull vault@sha256:f18350c9d5aad665027b2d384765fe98d0bb4c0d42c91a7f50bd0a12b4a397f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51661918 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:44dc4d5eaea4e72d43522917647e91cafc91818bcb247c66f5fa466946067234`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 00:04:28 GMT
ARG VAULT_VERSION=1.5.8
# Thu, 22 Apr 2021 00:04:30 GMT
# ARGS: VAULT_VERSION=1.5.8
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 22 Apr 2021 00:04:41 GMT
# ARGS: VAULT_VERSION=1.5.8
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 22 Apr 2021 00:04:44 GMT
# ARGS: VAULT_VERSION=1.5.8
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 22 Apr 2021 00:04:44 GMT
VOLUME [/vault/logs]
# Thu, 22 Apr 2021 00:04:45 GMT
VOLUME [/vault/file]
# Thu, 22 Apr 2021 00:04:46 GMT
EXPOSE 8200
# Thu, 22 Apr 2021 00:04:48 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Apr 2021 00:04:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 00:04:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32bdc1f9ac55521fd24dbd0d27942fa4b378f167dcd0b9cc7bdbd18686a991c9`  
		Last Modified: Thu, 22 Apr 2021 00:05:50 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:210dd010614d7549f089dc9de955a0ac1d34dbff15c479e5bf31a4b741c04c48`  
		Last Modified: Thu, 22 Apr 2021 00:06:03 GMT  
		Size: 49.0 MB (49036512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66f9f801fecf6a31b181deb54e278de3d3d480fa15bc4ff2cb73474eb6ce0635`  
		Last Modified: Thu, 22 Apr 2021 00:05:50 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7adcde9e98109a83bea324cc4488030af3306559b7e07a0c8b315128c5d47e54`  
		Last Modified: Thu, 22 Apr 2021 00:05:50 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.5.8` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:f2b3f2ccd9436a536e861197dec2922bcbab5dd067b9d2f368cc0b9763af0dc8
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.0 MB (51962311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5fc33416e1ffe4d02ec07694b4e9541bc67d29db2fc1b9382f8fdd343ee33725`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 21 Apr 2021 23:42:56 GMT
ARG VAULT_VERSION=1.5.8
# Wed, 21 Apr 2021 23:42:58 GMT
# ARGS: VAULT_VERSION=1.5.8
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 21 Apr 2021 23:43:05 GMT
# ARGS: VAULT_VERSION=1.5.8
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 21 Apr 2021 23:43:08 GMT
# ARGS: VAULT_VERSION=1.5.8
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 21 Apr 2021 23:43:09 GMT
VOLUME [/vault/logs]
# Wed, 21 Apr 2021 23:43:10 GMT
VOLUME [/vault/file]
# Wed, 21 Apr 2021 23:43:11 GMT
EXPOSE 8200
# Wed, 21 Apr 2021 23:43:11 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Apr 2021 23:43:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Apr 2021 23:43:13 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7154241c9ba79dd4ff63a1e9530fe20a30e01a9e549c9e6643ecd3daf6e19822`  
		Last Modified: Wed, 21 Apr 2021 23:44:06 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d60793cc6e6c24f72c334b97bef9067dfd9dac7475cad930eed43a35095eb523`  
		Last Modified: Wed, 21 Apr 2021 23:44:17 GMT  
		Size: 49.2 MB (49247015 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12231c480d4a49cac1195343831fc0134e0f64f5fb8b95e9eb0eb219717a4b83`  
		Last Modified: Wed, 21 Apr 2021 23:44:06 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ec7bed600171e35e7964c2d3b63a89f58ae56f9fc6ee7f897fc4da72d2daf36`  
		Last Modified: Wed, 21 Apr 2021 23:44:06 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.5.8` - linux; 386

```console
$ docker pull vault@sha256:6a78b6b67829aa22e4e07324488e9418908413ceeba14468f5feff284c1653c3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.2 MB (53161321 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51d17e9d2d146b993da4d21ba5e805b200b2040af2262eebf1c2abd3637bd4cd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Wed, 21 Apr 2021 23:41:58 GMT
ARG VAULT_VERSION=1.5.8
# Wed, 21 Apr 2021 23:41:59 GMT
# ARGS: VAULT_VERSION=1.5.8
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 21 Apr 2021 23:42:07 GMT
# ARGS: VAULT_VERSION=1.5.8
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 21 Apr 2021 23:42:08 GMT
# ARGS: VAULT_VERSION=1.5.8
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 21 Apr 2021 23:42:08 GMT
VOLUME [/vault/logs]
# Wed, 21 Apr 2021 23:42:08 GMT
VOLUME [/vault/file]
# Wed, 21 Apr 2021 23:42:09 GMT
EXPOSE 8200
# Wed, 21 Apr 2021 23:42:09 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Apr 2021 23:42:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Apr 2021 23:42:10 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6512227b3628ac3bd1132242cbd5f918ea6159b71df79980b2da39f92478ebe8`  
		Last Modified: Wed, 21 Apr 2021 23:43:17 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9023bade8a5f516b27c3c6bfdb849db04a776e2feef5b3b454add1521776a0c`  
		Last Modified: Wed, 21 Apr 2021 23:43:25 GMT  
		Size: 50.3 MB (50339159 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:040d5e75b78d2218ba5d129040c28d62f44e237d9612b7fddbd45ade8017b54b`  
		Last Modified: Wed, 21 Apr 2021 23:43:17 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26dfe2139edfadef9958c8fe2300299ba59be792c4aeec53dba0b76e62fbc196`  
		Last Modified: Wed, 21 Apr 2021 23:43:17 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.6.4`

```console
$ docker pull vault@sha256:c083624587c497a8e65b298680a57ffe20bedd1a26c1e74a09221845912d5a18
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.6.4` - linux; amd64

```console
$ docker pull vault@sha256:be084d88fdfea32ec0298ab70d19466a855e807d95b4a8833b66b9e7abd12081
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.0 MB (69027232 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ad6dce84d6cb95ed21fd5dceee0b218ed4dc20577c6aa1316441f7130c3c97ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 01:11:46 GMT
ARG VAULT_VERSION=1.6.4
# Thu, 22 Apr 2021 01:11:47 GMT
# ARGS: VAULT_VERSION=1.6.4
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 22 Apr 2021 01:11:56 GMT
# ARGS: VAULT_VERSION=1.6.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 22 Apr 2021 01:11:57 GMT
# ARGS: VAULT_VERSION=1.6.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 22 Apr 2021 01:11:58 GMT
VOLUME [/vault/logs]
# Thu, 22 Apr 2021 01:11:58 GMT
VOLUME [/vault/file]
# Thu, 22 Apr 2021 01:11:58 GMT
EXPOSE 8200
# Thu, 22 Apr 2021 01:11:58 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Apr 2021 01:11:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 01:11:59 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f1d199eb2268f61b78abb36186fa867c12e6cf630a719962a7c5242601eb4dd5`  
		Last Modified: Thu, 22 Apr 2021 01:12:40 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3302f3652619cef7e4877ffde78463b05fd0dc1797ccd686e45b5d1fe78b76a7`  
		Last Modified: Thu, 22 Apr 2021 01:12:49 GMT  
		Size: 66.2 MB (66211994 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebc30eb05a1ac9a57f3fec129778ad9b23d34177e531b9981275af3d49c78d8`  
		Last Modified: Thu, 22 Apr 2021 01:12:40 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bf4143c0a498e4ece423cde88e4d81360ded1697e148c047ffd34d59c5b2c12`  
		Last Modified: Thu, 22 Apr 2021 01:12:41 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.6.4` - linux; arm variant v6

```console
$ docker pull vault@sha256:b21e618598195a599cff3941b474270052894a29bea9cbd809297c2c1c873c8b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.8 MB (63773824 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9fb5145408852f9601bebbe3027409cc58cbe489be7388d31c80dcaf2faac8f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 00:03:57 GMT
ARG VAULT_VERSION=1.6.4
# Thu, 22 Apr 2021 00:03:59 GMT
# ARGS: VAULT_VERSION=1.6.4
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 22 Apr 2021 00:04:12 GMT
# ARGS: VAULT_VERSION=1.6.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 22 Apr 2021 00:04:15 GMT
# ARGS: VAULT_VERSION=1.6.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 22 Apr 2021 00:04:16 GMT
VOLUME [/vault/logs]
# Thu, 22 Apr 2021 00:04:16 GMT
VOLUME [/vault/file]
# Thu, 22 Apr 2021 00:04:17 GMT
EXPOSE 8200
# Thu, 22 Apr 2021 00:04:18 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Apr 2021 00:04:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 00:04:20 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35672d9b7fcf3d221996e861e5205c733c40a4c0ca1536ccd4f41d871ee837d1`  
		Last Modified: Thu, 22 Apr 2021 00:05:28 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28170922f026f71de00167b4fd05cda79959155dbade8ccaf5b2e31103e53101`  
		Last Modified: Thu, 22 Apr 2021 00:05:45 GMT  
		Size: 61.1 MB (61148424 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1900f2fa5f77005bafa21c62657d0688cac08935a79c82f4b537a38e6edf1f07`  
		Last Modified: Thu, 22 Apr 2021 00:05:28 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a5e250d06777cad1bd33dcde858129a3f1323460c572e2a75242be9184ea269`  
		Last Modified: Thu, 22 Apr 2021 00:05:28 GMT  
		Size: 1.8 KB (1824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.6.4` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:4fff170d65e7d3dbb09c2bf98176ec2651d382c794c4d878b9d3690c25a6e93f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.1 MB (65083845 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fbe7c1bf3a1f90f3c9b1d117f9153e8ec7933205e5d45e79078a8e6639574d79`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 21 Apr 2021 23:42:28 GMT
ARG VAULT_VERSION=1.6.4
# Wed, 21 Apr 2021 23:42:31 GMT
# ARGS: VAULT_VERSION=1.6.4
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 21 Apr 2021 23:42:39 GMT
# ARGS: VAULT_VERSION=1.6.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 21 Apr 2021 23:42:42 GMT
# ARGS: VAULT_VERSION=1.6.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 21 Apr 2021 23:42:43 GMT
VOLUME [/vault/logs]
# Wed, 21 Apr 2021 23:42:43 GMT
VOLUME [/vault/file]
# Wed, 21 Apr 2021 23:42:44 GMT
EXPOSE 8200
# Wed, 21 Apr 2021 23:42:45 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Apr 2021 23:42:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Apr 2021 23:42:47 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50294b5d755d2249f4414441cf2a04a945b63b2024f3926faf2f3c764b38596f`  
		Last Modified: Wed, 21 Apr 2021 23:43:47 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09dd7bd1d80a29624f7ebca85a5664568563ffe862111e48535ea8c5e8792589`  
		Last Modified: Wed, 21 Apr 2021 23:44:00 GMT  
		Size: 62.4 MB (62368554 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0ae1750e1a2b65b471bbc6a4d54cdff114745b3445e5cf25f829f17c535fa7a`  
		Last Modified: Wed, 21 Apr 2021 23:43:47 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0f7753d6cb4c359d0d37de39f9eec76bbec37f1ce5f6e3e1665e75fe8f4b7d`  
		Last Modified: Wed, 21 Apr 2021 23:43:47 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.6.4` - linux; 386

```console
$ docker pull vault@sha256:07e701574aeaed0362c33ca1de42e05c0cd749f35b684abfb275449a243c62f2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.1 MB (67084093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a88085405bb720e1f3a578894931047a6c04334c8ac45fb5bb7c9a5db013765c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Wed, 21 Apr 2021 23:41:41 GMT
ARG VAULT_VERSION=1.6.4
# Wed, 21 Apr 2021 23:41:42 GMT
# ARGS: VAULT_VERSION=1.6.4
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 21 Apr 2021 23:41:51 GMT
# ARGS: VAULT_VERSION=1.6.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 21 Apr 2021 23:41:52 GMT
# ARGS: VAULT_VERSION=1.6.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 21 Apr 2021 23:41:52 GMT
VOLUME [/vault/logs]
# Wed, 21 Apr 2021 23:41:52 GMT
VOLUME [/vault/file]
# Wed, 21 Apr 2021 23:41:53 GMT
EXPOSE 8200
# Wed, 21 Apr 2021 23:41:53 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Apr 2021 23:41:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Apr 2021 23:41:53 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c8a1c82f5aefb666dbda4c2180a6f8fdc5341e151dbe26efeb93ce8cb77f167`  
		Last Modified: Wed, 21 Apr 2021 23:42:56 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35b304a6475f19a929156e2fe68068211385a96949076c85c0ec96b226d32679`  
		Last Modified: Wed, 21 Apr 2021 23:43:07 GMT  
		Size: 64.3 MB (64261928 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5353d6012c66510fbcdd555ee06e5aecf9cf4fac6965a01462fc1798c58682a1`  
		Last Modified: Wed, 21 Apr 2021 23:42:56 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6c028691e43c0b2a70d80a2077ce50b0ca226a1ee506b8c5b34ddefdf9e84988`  
		Last Modified: Wed, 21 Apr 2021 23:42:56 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.7.1`

```console
$ docker pull vault@sha256:10f564c947706e021e60c84bd22b1e91559db133d6d3a57e930d32cd7e0cbf77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.7.1` - linux; amd64

```console
$ docker pull vault@sha256:7d07d64480897215cca86ce51750c888fae4d703529708517ecdd5fabba6cbb3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72739857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2a304f26b777cb8519d3f41d696a3afaf0d9d1b2d0918425350ea4dafe41aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 01:11:33 GMT
ARG VAULT_VERSION=1.7.1
# Thu, 22 Apr 2021 01:11:34 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 22 Apr 2021 01:11:40 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 22 Apr 2021 01:11:42 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 22 Apr 2021 01:11:42 GMT
VOLUME [/vault/logs]
# Thu, 22 Apr 2021 01:11:42 GMT
VOLUME [/vault/file]
# Thu, 22 Apr 2021 01:11:42 GMT
EXPOSE 8200
# Thu, 22 Apr 2021 01:11:42 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Apr 2021 01:11:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 01:11:43 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e67639d69ef396254b020b8996ad697bd3dc75c310a6838316a8fbe0b34975`  
		Last Modified: Thu, 22 Apr 2021 01:12:20 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc349bca401b4cc9376b314ab06f8af80c0cae8acc3a0303080f9b665d26640`  
		Last Modified: Thu, 22 Apr 2021 01:12:29 GMT  
		Size: 69.9 MB (69924621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0445e106649737b97635e87588c2520014d1c2c6009aef36cc176302d58b32d`  
		Last Modified: Thu, 22 Apr 2021 01:12:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef616976a08c8108362cbf479052fdaf16b7870fb76571447a603972115eecfb`  
		Last Modified: Thu, 22 Apr 2021 01:12:20 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.1` - linux; arm variant v6

```console
$ docker pull vault@sha256:75739463a8000a8bc3709b952e4dbc1e4577cd7d8f0a0ed2933f8a98f9104fb3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66746361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaeff817a9d594bfc213819fee619bdaeb2bc3dd8f71433ac0524d9aaa95bcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 00:03:22 GMT
ARG VAULT_VERSION=1.7.1
# Thu, 22 Apr 2021 00:03:25 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 22 Apr 2021 00:03:39 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 22 Apr 2021 00:03:42 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 22 Apr 2021 00:03:42 GMT
VOLUME [/vault/logs]
# Thu, 22 Apr 2021 00:03:43 GMT
VOLUME [/vault/file]
# Thu, 22 Apr 2021 00:03:44 GMT
EXPOSE 8200
# Thu, 22 Apr 2021 00:03:45 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Apr 2021 00:03:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 00:03:47 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3255facdf2728fe182f052e94f0479bbaf6cadfbe8cd4aa978c8803f8738f9e5`  
		Last Modified: Thu, 22 Apr 2021 00:05:06 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c547d8de9ec409e430255410de106de39ff878a36758d71f6818dc799566d252`  
		Last Modified: Thu, 22 Apr 2021 00:05:22 GMT  
		Size: 64.1 MB (64120962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b228f949e5779456017dd39918f3ae59a5d466e498b0cf054f7cc89bc27c515b`  
		Last Modified: Thu, 22 Apr 2021 00:05:06 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee2ad32bff6754a64decc8b1a5113e295eda8606423b3261cc2595d904cb556`  
		Last Modified: Thu, 22 Apr 2021 00:05:06 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.1` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:22bd3bd288973afbe2fe51004c64ad04f5803f51250c18def7b96b462e97b38d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68609349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f8c5f66a6428d7e372609f75666ad04b4ec688292e8d9b6f89ac0682b435ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 21 Apr 2021 23:42:02 GMT
ARG VAULT_VERSION=1.7.1
# Wed, 21 Apr 2021 23:42:04 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 21 Apr 2021 23:42:13 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 21 Apr 2021 23:42:16 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 21 Apr 2021 23:42:17 GMT
VOLUME [/vault/logs]
# Wed, 21 Apr 2021 23:42:18 GMT
VOLUME [/vault/file]
# Wed, 21 Apr 2021 23:42:18 GMT
EXPOSE 8200
# Wed, 21 Apr 2021 23:42:19 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Apr 2021 23:42:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Apr 2021 23:42:21 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afbab083caa522eaa170c65751dfbd70588d3d1339718ef76783388716ffafe`  
		Last Modified: Wed, 21 Apr 2021 23:43:25 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1878b93e8bf7428c9f64cc136aec8f260a6c45de1cc74dc1ba782370b8df6aec`  
		Last Modified: Wed, 21 Apr 2021 23:43:39 GMT  
		Size: 65.9 MB (65894058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f32296b0b49ad7b325c4acdae677d63b61cd73bd49a2cbf1bf078f30c7aa7f`  
		Last Modified: Wed, 21 Apr 2021 23:43:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabfc9e3c880ad5c72b17f06c96faa62a33b1214d14511abda81d059301e76c6`  
		Last Modified: Wed, 21 Apr 2021 23:43:25 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.7.1` - linux; 386

```console
$ docker pull vault@sha256:661c3c426525f8a7b246dcde3de08a1a06f1c80daddf963aaadcc60a8432dab1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70582514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab923df6f9daf4521d48e608fd79f5dc62e3e185f771f1a262335cab7b6e70d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Wed, 21 Apr 2021 23:41:23 GMT
ARG VAULT_VERSION=1.7.1
# Wed, 21 Apr 2021 23:41:24 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 21 Apr 2021 23:41:33 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 21 Apr 2021 23:41:34 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 21 Apr 2021 23:41:34 GMT
VOLUME [/vault/logs]
# Wed, 21 Apr 2021 23:41:34 GMT
VOLUME [/vault/file]
# Wed, 21 Apr 2021 23:41:35 GMT
EXPOSE 8200
# Wed, 21 Apr 2021 23:41:35 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Apr 2021 23:41:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Apr 2021 23:41:35 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1dd406aad66bc47a2a17b2d6a848d762f4787471afd3fabcb8318a4be343e3`  
		Last Modified: Wed, 21 Apr 2021 23:42:27 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d2281cd90daca415c01bd1088232356df75260fa2e29ae66817bfff7e0af45`  
		Last Modified: Wed, 21 Apr 2021 23:42:44 GMT  
		Size: 67.8 MB (67760352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bd8116cdd83cf85d77a626989b4f854834394a3900cdc4c87ac05d61795f9e`  
		Last Modified: Wed, 21 Apr 2021 23:42:27 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b240059e0c23ad083ef13f3846a09a02a372006486590acd1fff81c8aaff45`  
		Last Modified: Wed, 21 Apr 2021 23:42:27 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:latest`

```console
$ docker pull vault@sha256:10f564c947706e021e60c84bd22b1e91559db133d6d3a57e930d32cd7e0cbf77
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:7d07d64480897215cca86ce51750c888fae4d703529708517ecdd5fabba6cbb3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72739857 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd2a304f26b777cb8519d3f41d696a3afaf0d9d1b2d0918425350ea4dafe41aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 01:11:33 GMT
ARG VAULT_VERSION=1.7.1
# Thu, 22 Apr 2021 01:11:34 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 22 Apr 2021 01:11:40 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 22 Apr 2021 01:11:42 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 22 Apr 2021 01:11:42 GMT
VOLUME [/vault/logs]
# Thu, 22 Apr 2021 01:11:42 GMT
VOLUME [/vault/file]
# Thu, 22 Apr 2021 01:11:42 GMT
EXPOSE 8200
# Thu, 22 Apr 2021 01:11:42 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Apr 2021 01:11:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 01:11:43 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97e67639d69ef396254b020b8996ad697bd3dc75c310a6838316a8fbe0b34975`  
		Last Modified: Thu, 22 Apr 2021 01:12:20 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dc349bca401b4cc9376b314ab06f8af80c0cae8acc3a0303080f9b665d26640`  
		Last Modified: Thu, 22 Apr 2021 01:12:29 GMT  
		Size: 69.9 MB (69924621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a0445e106649737b97635e87588c2520014d1c2c6009aef36cc176302d58b32d`  
		Last Modified: Thu, 22 Apr 2021 01:12:20 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef616976a08c8108362cbf479052fdaf16b7870fb76571447a603972115eecfb`  
		Last Modified: Thu, 22 Apr 2021 01:12:20 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:75739463a8000a8bc3709b952e4dbc1e4577cd7d8f0a0ed2933f8a98f9104fb3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66746361 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ceaeff817a9d594bfc213819fee619bdaeb2bc3dd8f71433ac0524d9aaa95bcd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:39 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Wed, 14 Apr 2021 18:49:40 GMT
CMD ["/bin/sh"]
# Thu, 22 Apr 2021 00:03:22 GMT
ARG VAULT_VERSION=1.7.1
# Thu, 22 Apr 2021 00:03:25 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 22 Apr 2021 00:03:39 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 22 Apr 2021 00:03:42 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 22 Apr 2021 00:03:42 GMT
VOLUME [/vault/logs]
# Thu, 22 Apr 2021 00:03:43 GMT
VOLUME [/vault/file]
# Thu, 22 Apr 2021 00:03:44 GMT
EXPOSE 8200
# Thu, 22 Apr 2021 00:03:45 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 22 Apr 2021 00:03:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 22 Apr 2021 00:03:47 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3255facdf2728fe182f052e94f0479bbaf6cadfbe8cd4aa978c8803f8738f9e5`  
		Last Modified: Thu, 22 Apr 2021 00:05:06 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c547d8de9ec409e430255410de106de39ff878a36758d71f6818dc799566d252`  
		Last Modified: Thu, 22 Apr 2021 00:05:22 GMT  
		Size: 64.1 MB (64120962 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b228f949e5779456017dd39918f3ae59a5d466e498b0cf054f7cc89bc27c515b`  
		Last Modified: Thu, 22 Apr 2021 00:05:06 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fee2ad32bff6754a64decc8b1a5113e295eda8606423b3261cc2595d904cb556`  
		Last Modified: Thu, 22 Apr 2021 00:05:06 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:22bd3bd288973afbe2fe51004c64ad04f5803f51250c18def7b96b462e97b38d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.6 MB (68609349 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:29f8c5f66a6428d7e372609f75666ad04b4ec688292e8d9b6f89ac0682b435ed`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:37 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Wed, 14 Apr 2021 18:42:38 GMT
CMD ["/bin/sh"]
# Wed, 21 Apr 2021 23:42:02 GMT
ARG VAULT_VERSION=1.7.1
# Wed, 21 Apr 2021 23:42:04 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 21 Apr 2021 23:42:13 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 21 Apr 2021 23:42:16 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 21 Apr 2021 23:42:17 GMT
VOLUME [/vault/logs]
# Wed, 21 Apr 2021 23:42:18 GMT
VOLUME [/vault/file]
# Wed, 21 Apr 2021 23:42:18 GMT
EXPOSE 8200
# Wed, 21 Apr 2021 23:42:19 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Apr 2021 23:42:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Apr 2021 23:42:21 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2afbab083caa522eaa170c65751dfbd70588d3d1339718ef76783388716ffafe`  
		Last Modified: Wed, 21 Apr 2021 23:43:25 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1878b93e8bf7428c9f64cc136aec8f260a6c45de1cc74dc1ba782370b8df6aec`  
		Last Modified: Wed, 21 Apr 2021 23:43:39 GMT  
		Size: 65.9 MB (65894058 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74f32296b0b49ad7b325c4acdae677d63b61cd73bd49a2cbf1bf078f30c7aa7f`  
		Last Modified: Wed, 21 Apr 2021 23:43:26 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabfc9e3c880ad5c72b17f06c96faa62a33b1214d14511abda81d059301e76c6`  
		Last Modified: Wed, 21 Apr 2021 23:43:25 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:661c3c426525f8a7b246dcde3de08a1a06f1c80daddf963aaadcc60a8432dab1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70582514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9ab923df6f9daf4521d48e608fd79f5dc62e3e185f771f1a262335cab7b6e70d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Wed, 21 Apr 2021 23:41:23 GMT
ARG VAULT_VERSION=1.7.1
# Wed, 21 Apr 2021 23:41:24 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 21 Apr 2021 23:41:33 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 21 Apr 2021 23:41:34 GMT
# ARGS: VAULT_VERSION=1.7.1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 21 Apr 2021 23:41:34 GMT
VOLUME [/vault/logs]
# Wed, 21 Apr 2021 23:41:34 GMT
VOLUME [/vault/file]
# Wed, 21 Apr 2021 23:41:35 GMT
EXPOSE 8200
# Wed, 21 Apr 2021 23:41:35 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Apr 2021 23:41:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Apr 2021 23:41:35 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f1dd406aad66bc47a2a17b2d6a848d762f4787471afd3fabcb8318a4be343e3`  
		Last Modified: Wed, 21 Apr 2021 23:42:27 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43d2281cd90daca415c01bd1088232356df75260fa2e29ae66817bfff7e0af45`  
		Last Modified: Wed, 21 Apr 2021 23:42:44 GMT  
		Size: 67.8 MB (67760352 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:77bd8116cdd83cf85d77a626989b4f854834394a3900cdc4c87ac05d61795f9e`  
		Last Modified: Wed, 21 Apr 2021 23:42:27 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86b240059e0c23ad083ef13f3846a09a02a372006486590acd1fff81c8aaff45`  
		Last Modified: Wed, 21 Apr 2021 23:42:27 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
