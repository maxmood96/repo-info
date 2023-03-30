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
