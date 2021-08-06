## `vault:latest`

```console
$ docker pull vault@sha256:17c8fb627a230a25d2ca1073ee501b4dfd5deda47ea811ac101a989666c00170
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:20600e76f92c6500ba0aeb99e645a08eb3cf299c8e0749d98be19944c73dfd43
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.7 MB (68658727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e03ae6c19e95a5101c148544ca077b273dbfb14309d2bf3dd85366a9321e8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 05 Aug 2021 23:47:28 GMT
ARG VAULT_VERSION=1.8.1
# Thu, 05 Aug 2021 23:47:29 GMT
# ARGS: VAULT_VERSION=1.8.1
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 05 Aug 2021 23:47:36 GMT
# ARGS: VAULT_VERSION=1.8.1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 05 Aug 2021 23:47:38 GMT
# ARGS: VAULT_VERSION=1.8.1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 05 Aug 2021 23:47:38 GMT
VOLUME [/vault/logs]
# Thu, 05 Aug 2021 23:47:38 GMT
VOLUME [/vault/file]
# Thu, 05 Aug 2021 23:47:38 GMT
EXPOSE 8200
# Thu, 05 Aug 2021 23:47:38 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 05 Aug 2021 23:47:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Aug 2021 23:47:39 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:330b7790b6e327077511aae57c245c357d8c16b63b9416ec380f00067c07b5bf`  
		Last Modified: Thu, 05 Aug 2021 23:48:00 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:43a57bb7fb09793086c514eb635b7703e9110bedd2e51dc08f8d2efce2236411`  
		Last Modified: Thu, 05 Aug 2021 23:48:09 GMT  
		Size: 65.8 MB (65843493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a01323451d73bdac0e7c5d8ac59a920ba49de60f72989fff90e2ef8e3df5437`  
		Last Modified: Thu, 05 Aug 2021 23:48:00 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2880dfa93295dba80a22671ef3385df45cda739b3275e00f263227b402b621d9`  
		Last Modified: Thu, 05 Aug 2021 23:48:00 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:7b55492806389fbc288ca428113261e15552e6853c5d876f02954447d00b5e30
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **63.3 MB (63319051 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:311751981dd2aa97acf7d4839bf1fdea1b5b69e2fbe09a7ce10880d52fcfeed7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Fri, 30 Jul 2021 17:49:55 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Fri, 30 Jul 2021 17:49:55 GMT
CMD ["/bin/sh"]
# Thu, 05 Aug 2021 23:00:30 GMT
ARG VAULT_VERSION=1.8.1
# Thu, 05 Aug 2021 23:00:32 GMT
# ARGS: VAULT_VERSION=1.8.1
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 05 Aug 2021 23:00:49 GMT
# ARGS: VAULT_VERSION=1.8.1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 05 Aug 2021 23:00:51 GMT
# ARGS: VAULT_VERSION=1.8.1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 05 Aug 2021 23:00:51 GMT
VOLUME [/vault/logs]
# Thu, 05 Aug 2021 23:00:52 GMT
VOLUME [/vault/file]
# Thu, 05 Aug 2021 23:00:52 GMT
EXPOSE 8200
# Thu, 05 Aug 2021 23:00:53 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 05 Aug 2021 23:00:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Aug 2021 23:00:53 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f17badbe9cf834e3558ad4e55181d9c67b39ea368c775fb984169abe5ab41b6d`  
		Last Modified: Thu, 05 Aug 2021 23:01:50 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c610ff3b560894dbbfd6a46460eb5feec30e1dd98214a4e2c17ee7f5e54aa233`  
		Last Modified: Thu, 05 Aug 2021 23:02:23 GMT  
		Size: 60.7 MB (60693648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f65de4c88119b077c85f8d7b68b306ddb0310f221b6fa5efb16c0692f5992bb`  
		Last Modified: Thu, 05 Aug 2021 23:01:50 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0356d6d9c4c47509e97b45aa1df1eb771911e6f2569219c14d2382f698b0da51`  
		Last Modified: Thu, 05 Aug 2021 23:01:50 GMT  
		Size: 1.8 KB (1823 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:a061795cb48fd626de868369b888660aeeecbea3a20f602cfbb52818f1c18569
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **65.0 MB (65039661 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33e344ed30e3bfca2820bafbcad5675851167fe140a3e4f59291b28dd2bd4e7b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Thu, 05 Aug 2021 23:53:15 GMT
ARG VAULT_VERSION=1.8.1
# Thu, 05 Aug 2021 23:53:16 GMT
# ARGS: VAULT_VERSION=1.8.1
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 05 Aug 2021 23:53:22 GMT
# ARGS: VAULT_VERSION=1.8.1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 05 Aug 2021 23:53:23 GMT
# ARGS: VAULT_VERSION=1.8.1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 05 Aug 2021 23:53:23 GMT
VOLUME [/vault/logs]
# Thu, 05 Aug 2021 23:53:24 GMT
VOLUME [/vault/file]
# Thu, 05 Aug 2021 23:53:24 GMT
EXPOSE 8200
# Thu, 05 Aug 2021 23:53:24 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 05 Aug 2021 23:53:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Aug 2021 23:53:24 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35afde4a65174c031183b74bf8c5e175bd1ac07812de77e1ec92cf3fcdcd570c`  
		Last Modified: Thu, 05 Aug 2021 23:53:57 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db9ab5b756a6d02344ff86eaa2099823454e5676703042f64e136ed0af83bbf`  
		Last Modified: Thu, 05 Aug 2021 23:54:06 GMT  
		Size: 62.3 MB (62324366 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:848103d2a172a93029ef7f09bf8350578344f01c6a6d7b59da161ee563227575`  
		Last Modified: Thu, 05 Aug 2021 23:53:57 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf3c846ae50b6b88bd8a9b42fc4c56ddc9b8e8acee63051485f19b0043931a1a`  
		Last Modified: Thu, 05 Aug 2021 23:53:57 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:52912ca28994c0969521074b5c175a1e4ce9cf88a27d3e3e6d8c3ca78685cbe7
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.5 MB (66535552 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6dc5a6b9374d6b41ce15c3b7b654adcbfb20239bd1bf8d3162f9f172a269bb86`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 05 Aug 2021 23:35:21 GMT
ARG VAULT_VERSION=1.8.1
# Thu, 05 Aug 2021 23:35:22 GMT
# ARGS: VAULT_VERSION=1.8.1
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 05 Aug 2021 23:35:32 GMT
# ARGS: VAULT_VERSION=1.8.1
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 05 Aug 2021 23:35:33 GMT
# ARGS: VAULT_VERSION=1.8.1
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 05 Aug 2021 23:35:33 GMT
VOLUME [/vault/logs]
# Thu, 05 Aug 2021 23:35:33 GMT
VOLUME [/vault/file]
# Thu, 05 Aug 2021 23:35:33 GMT
EXPOSE 8200
# Thu, 05 Aug 2021 23:35:34 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 05 Aug 2021 23:35:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 05 Aug 2021 23:35:34 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a6ebb41201a112b1f3299b2f20a530021eb5715e91761cc913b947a80c11f14f`  
		Last Modified: Thu, 05 Aug 2021 23:36:05 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f250e9e296accfbb3c31af3f3a1c43e87b1189e8d452f9086c31e27dccbf1f3`  
		Last Modified: Thu, 05 Aug 2021 23:36:14 GMT  
		Size: 63.7 MB (63713383 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33bd14a411d8b8b09a030d6419c32025d8f83aaebce6fbe1ab4d51ae5639974`  
		Last Modified: Thu, 05 Aug 2021 23:36:05 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4fe5fe1189ae2ac80638ba09f49ea4c57c9b1e8c23cc54661dcd9d77d240f591`  
		Last Modified: Thu, 05 Aug 2021 23:36:05 GMT  
		Size: 1.8 KB (1822 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
