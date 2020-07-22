## `vault:latest`

```console
$ docker pull vault@sha256:9421e2fea27065ab03aa50f2f6810a52673aff6afaea35c3394a0d693507e4e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:71beaeca153c4cfb27fde00f778468ad5d8d3b6729aca29af5a6f530ac03b7ac
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.1 MB (52141093 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eeff8a0e63ad36dc9b200a6aa38aba61ba3a032d0c0523cb61f68490af4c00cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 24 Apr 2020 01:05:21 GMT
ADD file:66a440394c2442570f1f060e25c86613cb2d88a8af0c71c5a4154b3570e9a805 in / 
# Fri, 24 Apr 2020 01:05:21 GMT
CMD ["/bin/sh"]
# Fri, 03 Jul 2020 17:20:12 GMT
ARG VAULT_VERSION=1.4.3
# Fri, 03 Jul 2020 17:20:13 GMT
# ARGS: VAULT_VERSION=1.4.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 03 Jul 2020 17:20:18 GMT
# ARGS: VAULT_VERSION=1.4.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 03 Jul 2020 17:20:19 GMT
# ARGS: VAULT_VERSION=1.4.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 03 Jul 2020 17:20:19 GMT
VOLUME [/vault/logs]
# Fri, 03 Jul 2020 17:20:19 GMT
VOLUME [/vault/file]
# Fri, 03 Jul 2020 17:20:20 GMT
EXPOSE 8200
# Fri, 03 Jul 2020 17:20:20 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Jul 2020 17:20:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Jul 2020 17:20:20 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:21c83c5242199776c232920ddb58cfa2a46b17e42ed831ca9001c8dbc532d22d`  
		Last Modified: Fri, 24 Apr 2020 01:06:07 GMT  
		Size: 2.8 MB (2795580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b33636826a943396873384b2ee6b43c080db2f1920e418b8d2ea33104b5a3efc`  
		Last Modified: Fri, 03 Jul 2020 17:20:40 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d38d5932db2a5e4c40690f53207ac6b13b3ac2b3f3ce6b9fdf98e823bc698d15`  
		Last Modified: Fri, 03 Jul 2020 17:20:48 GMT  
		Size: 49.3 MB (49342274 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7982fbe652748b20a8efd499c18b93933b2af4ae182e8f1efd3e09b8ce70e3e`  
		Last Modified: Fri, 03 Jul 2020 17:20:40 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5723939fa01f464fa05b331dd1943283486bfa213cb85185fa09271f80854704`  
		Last Modified: Fri, 03 Jul 2020 17:20:40 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:c98e36d40935b8feed1ac85517759106583949c35cd5a813d4c3376c31ef2134
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.9 MB (50944469 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a03722336f638b24ea177e201b542c51dd99d43da1f9ae53b262ec74d4303483`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Apr 2020 15:51:35 GMT
ADD file:ef75120295e25a8e67c5ef378df2cf4ce9f7b83b44709452fcaf247b54fabd16 in / 
# Thu, 23 Apr 2020 15:51:36 GMT
CMD ["/bin/sh"]
# Wed, 22 Jul 2020 00:50:46 GMT
ARG VAULT_VERSION=1.5.0
# Wed, 22 Jul 2020 00:51:03 GMT
# ARGS: VAULT_VERSION=1.5.0
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 22 Jul 2020 00:51:14 GMT
# ARGS: VAULT_VERSION=1.5.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 22 Jul 2020 00:51:20 GMT
# ARGS: VAULT_VERSION=1.5.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 22 Jul 2020 00:51:21 GMT
VOLUME [/vault/logs]
# Wed, 22 Jul 2020 00:51:23 GMT
VOLUME [/vault/file]
# Wed, 22 Jul 2020 00:51:24 GMT
EXPOSE 8200
# Wed, 22 Jul 2020 00:51:25 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jul 2020 00:51:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jul 2020 00:51:27 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:e745d1dc1c9e0be26166278da7632765ca98fa1be8179a7cc440b3bdc5671860`  
		Last Modified: Thu, 23 Apr 2020 15:52:15 GMT  
		Size: 2.6 MB (2572512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac48023b44af172b456aaf562cf31228135c8f960841f3904767a216cf74ac1e`  
		Last Modified: Wed, 22 Jul 2020 00:51:36 GMT  
		Size: 1.3 KB (1288 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e25745cca31c5fd67cdee488b904fdcba1aa5e8cef71b17139767c6b06f3d65`  
		Last Modified: Wed, 22 Jul 2020 00:51:50 GMT  
		Size: 48.4 MB (48368658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6e02e93c7690f65c3bad424e95e1203ea589ee5f0490edc09a4c52fa07e4dcd`  
		Last Modified: Wed, 22 Jul 2020 00:51:37 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e3a6b5363e9e25d0081564d2ed3a786bcfd64269d0f514d2784a5f6a17ca4de`  
		Last Modified: Wed, 22 Jul 2020 00:51:36 GMT  
		Size: 1.8 KB (1824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:ff596cf9df78a300904af5808996eba930c8af17e2877536e88e723bfdbdc78c
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.3 MB (51261501 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2bc4ed95de203cae2ffac8294a9c0aaf470fd5f430e60f0a614c15d2448fc047`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 24 Apr 2020 00:14:52 GMT
ADD file:75529f7e83edb6d0457a3b8bbfe33d4e3a12f339c5ace517d0f52dbedd9a146b in / 
# Fri, 24 Apr 2020 00:14:53 GMT
CMD ["/bin/sh"]
# Wed, 22 Jul 2020 00:53:11 GMT
ARG VAULT_VERSION=1.5.0
# Wed, 22 Jul 2020 00:53:15 GMT
# ARGS: VAULT_VERSION=1.5.0
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 22 Jul 2020 00:53:23 GMT
# ARGS: VAULT_VERSION=1.5.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 22 Jul 2020 00:53:27 GMT
# ARGS: VAULT_VERSION=1.5.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 22 Jul 2020 00:53:28 GMT
VOLUME [/vault/logs]
# Wed, 22 Jul 2020 00:53:28 GMT
VOLUME [/vault/file]
# Wed, 22 Jul 2020 00:53:29 GMT
EXPOSE 8200
# Wed, 22 Jul 2020 00:53:30 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 22 Jul 2020 00:53:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 22 Jul 2020 00:53:31 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:b038bcb63e9c8905cc879c957302f686a9b43f24a18dcfc4186ab236ddf04cad`  
		Last Modified: Fri, 24 Apr 2020 00:15:54 GMT  
		Size: 2.7 MB (2718734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34f3c292160241915a90468ebd833263004f79dc31f19c6b55022c5bc23f425`  
		Last Modified: Wed, 22 Jul 2020 00:53:41 GMT  
		Size: 1.3 KB (1290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:969828cd481f598b339f4f94d09524a2385c07cf4cd41fdc64e76dbd30fd8b91`  
		Last Modified: Wed, 22 Jul 2020 00:53:53 GMT  
		Size: 48.5 MB (48539468 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f89bc576029a71c33adcb793b8ce72231f54246ca41bb41dc81ce149ff7212e7`  
		Last Modified: Wed, 22 Jul 2020 00:53:41 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b73d93c42445059eaf0931ec83de1981371fd2a665384e43b8d58f5f5471e1a3`  
		Last Modified: Wed, 22 Jul 2020 00:53:41 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:7caf492b22bc8582fd6d1dba77b22f1785c89ed81f942cbb63279f38d8ed8ada
```

-	Docker Version: 18.09.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.3 MB (50321413 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fff8c2a8230c66903334537ebb3a115c6502ffd2272ff924f8c8979f06919938`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 23 Apr 2020 21:16:11 GMT
ADD file:2e9fb162fdd20e7ac6e9edcb9e1ce9ece750f125c93824c5709a2800ae397f89 in / 
# Thu, 23 Apr 2020 21:16:11 GMT
CMD ["/bin/sh"]
# Fri, 03 Jul 2020 17:38:39 GMT
ARG VAULT_VERSION=1.4.3
# Fri, 03 Jul 2020 17:38:40 GMT
# ARGS: VAULT_VERSION=1.4.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 03 Jul 2020 17:38:46 GMT
# ARGS: VAULT_VERSION=1.4.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 03 Jul 2020 17:38:46 GMT
# ARGS: VAULT_VERSION=1.4.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 03 Jul 2020 17:38:47 GMT
VOLUME [/vault/logs]
# Fri, 03 Jul 2020 17:38:47 GMT
VOLUME [/vault/file]
# Fri, 03 Jul 2020 17:38:47 GMT
EXPOSE 8200
# Fri, 03 Jul 2020 17:38:47 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 03 Jul 2020 17:38:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 03 Jul 2020 17:38:48 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:294658c31053f36b08a64158e37d4fb84478e6fe8f4d5127c51a6334c8a3c36d`  
		Last Modified: Thu, 23 Apr 2020 21:16:37 GMT  
		Size: 2.8 MB (2787128 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff13f848775c9d55a090b4c35c7c93750023833d521af2829fcde84219c13e8f`  
		Last Modified: Fri, 03 Jul 2020 17:39:07 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c975e3a53e2c0538c9594f44a147058dc86ab6b60aca3af81d1cf286382deb79`  
		Last Modified: Fri, 03 Jul 2020 17:39:14 GMT  
		Size: 47.5 MB (47531051 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb155c6900964d76570ad5e74cffd2846234543be816719e525be2168a8c7dcc`  
		Last Modified: Fri, 03 Jul 2020 17:39:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:271e3b37bdae96f4bd21c37ade3be106356aead0a8e2358cfe0ea4c9e779c094`  
		Last Modified: Fri, 03 Jul 2020 17:39:07 GMT  
		Size: 1.8 KB (1820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
