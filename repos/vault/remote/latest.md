## `vault:latest`

```console
$ docker pull vault@sha256:1722d3a087c59230b8ad8e3b97da2188e19658ecd9ecc758770c6f1768bacbba
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:195b9f8b680fed50fdec2573a6fd3018496fc5289860ef87fe56fbdc8b91c509
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **74.1 MB (74052027 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62f6f5bc220f1cadd0d3692ff1cb307f818a81881884e0c1e3bff11030897d6d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Tue, 05 Apr 2022 00:20:08 GMT
ADD file:b9eae64dc6ab27fdaa048b7cda06fcb5c7655e1b327e098e2775d095cb657b01 in / 
# Tue, 05 Apr 2022 00:20:08 GMT
CMD ["/bin/sh"]
# Mon, 13 Jun 2022 17:58:04 GMT
ARG VAULT_VERSION=1.10.4
# Mon, 13 Jun 2022 17:58:05 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN addgroup vault &&     adduser -S -G vault vault
# Mon, 13 Jun 2022 17:58:12 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Mon, 13 Jun 2022 17:58:13 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Mon, 13 Jun 2022 17:58:13 GMT
VOLUME [/vault/logs]
# Mon, 13 Jun 2022 17:58:14 GMT
VOLUME [/vault/file]
# Mon, 13 Jun 2022 17:58:14 GMT
EXPOSE 8200
# Mon, 13 Jun 2022 17:58:14 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 13 Jun 2022 17:58:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jun 2022 17:58:14 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:8663204ce13b2961da55026a2034abb9e5afaaccf6a9cfb44ad71406dcd07c7b`  
		Last Modified: Tue, 05 Apr 2022 00:20:51 GMT  
		Size: 2.8 MB (2818370 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19abc3dad2129795974a57bd6acb53044335a0982a227ed888c63615ec446d24`  
		Last Modified: Mon, 13 Jun 2022 17:59:14 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:173010f863ffc554afafe6e4c801a56ed92848a9e96267ce0573ca3d47ec722c`  
		Last Modified: Mon, 13 Jun 2022 17:59:23 GMT  
		Size: 71.2 MB (71230385 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:065ab21f6595eadc59064aacb38d26b0b44de9f7be3b357674079c45ae03da08`  
		Last Modified: Mon, 13 Jun 2022 17:59:14 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8069c9e05cbc2041706a540392fea7dce464048d8556a9b80f6d169ccc723a5e`  
		Last Modified: Mon, 13 Jun 2022 17:59:14 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:764f075252b60cb5ea09c33c0aa9739599aa8422f781eae08cfe474b999c3677
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **67.3 MB (67334395 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd0b7fed9555e5596dbd9e8fd6e8a507bc533346d964b587038b07d0897cd4c2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 04 Apr 2022 23:49:55 GMT
ADD file:2e4db0cea3f5eecfbb82c5abd09eb100749fed0189fc30d2c51980d2560e3ccb in / 
# Mon, 04 Apr 2022 23:49:56 GMT
CMD ["/bin/sh"]
# Mon, 13 Jun 2022 17:54:54 GMT
ARG VAULT_VERSION=1.10.4
# Mon, 13 Jun 2022 17:54:56 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN addgroup vault &&     adduser -S -G vault vault
# Mon, 13 Jun 2022 17:55:13 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Mon, 13 Jun 2022 17:55:15 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Mon, 13 Jun 2022 17:55:16 GMT
VOLUME [/vault/logs]
# Mon, 13 Jun 2022 17:55:16 GMT
VOLUME [/vault/file]
# Mon, 13 Jun 2022 17:55:17 GMT
EXPOSE 8200
# Mon, 13 Jun 2022 17:55:17 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 13 Jun 2022 17:55:17 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jun 2022 17:55:18 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:f9f2e4e531ad51ee917e8311e91a223a4893c1d754acb8246af87375ea60c6aa`  
		Last Modified: Mon, 04 Apr 2022 23:51:47 GMT  
		Size: 2.6 MB (2626056 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:768193988085f0299c2c56bff8505bafc8e7ef254178c023311a91f9fb5400b6`  
		Last Modified: Mon, 13 Jun 2022 17:57:54 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e76c4e81347d8848a6cc055156b657ea7387369c8fce1fffb2cdc495f4a9070`  
		Last Modified: Mon, 13 Jun 2022 17:58:32 GMT  
		Size: 64.7 MB (64705073 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd2d524ba77680ee349468953b499c602e499884db91375c0a435df02591073e`  
		Last Modified: Mon, 13 Jun 2022 17:57:55 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe4e405e281407fc2bdfcc09a4feeadf0fa82d04df527f6a6616bb14bb8cc58d`  
		Last Modified: Mon, 13 Jun 2022 17:57:55 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:02ac21617aa273224711d6c6abf40b1dbb44d39628215501fb3157c2c6974250
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **69.1 MB (69101307 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ebd479fe8703857bad69d68f40432f17834172ae53e39507ed1b46c8af4df4ad`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 04 Apr 2022 23:39:39 GMT
ADD file:66f473ec586f45376eb1941936c7829f636b90cad2022233cacf3186ac747ef9 in / 
# Mon, 04 Apr 2022 23:39:39 GMT
CMD ["/bin/sh"]
# Mon, 13 Jun 2022 18:16:36 GMT
ARG VAULT_VERSION=1.10.4
# Mon, 13 Jun 2022 18:16:37 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN addgroup vault &&     adduser -S -G vault vault
# Mon, 13 Jun 2022 18:16:44 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Mon, 13 Jun 2022 18:16:45 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Mon, 13 Jun 2022 18:16:46 GMT
VOLUME [/vault/logs]
# Mon, 13 Jun 2022 18:16:47 GMT
VOLUME [/vault/file]
# Mon, 13 Jun 2022 18:16:48 GMT
EXPOSE 8200
# Mon, 13 Jun 2022 18:16:50 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 13 Jun 2022 18:16:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jun 2022 18:16:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:455c02918c4592a9beeeae47df541266f3ea53ed573feb767e5e8ab8dcee146e`  
		Last Modified: Mon, 04 Apr 2022 23:40:41 GMT  
		Size: 2.7 MB (2717389 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1506755f7238e40d0f86f538246192225b4d68cd22ed8e18cb1d264e244f6e61`  
		Last Modified: Mon, 13 Jun 2022 18:18:10 GMT  
		Size: 1.2 KB (1235 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1935b8650f6f5d196ab7114ad31bc9b922a984b417e3f71551291782f267bfdf`  
		Last Modified: Mon, 13 Jun 2022 18:18:19 GMT  
		Size: 66.4 MB (66380713 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b7b94a32356ab47070ebff58e82c3b71c99ef66e7771c6758b157b8ef217a76`  
		Last Modified: Mon, 13 Jun 2022 18:18:10 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0866c6bdd34f367391c3914133395d61df7fcc9830ed130b1cb6061c41a84f67`  
		Last Modified: Mon, 13 Jun 2022 18:18:10 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:c2773c965e56d4c50b87568b9456fa2e2ce8717bf3bec0c913dd424377898da8
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.4 MB (70416231 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a7e72275edecb6fea728b22ae034f6c111218eda4c5f6206d79775d612335ffe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 04 Apr 2022 23:38:32 GMT
ADD file:6508514d43b69774a3307679ef8f6dba0faf707e62ad6c6c1c8cf40d84e12d1d in / 
# Mon, 04 Apr 2022 23:38:32 GMT
CMD ["/bin/sh"]
# Mon, 13 Jun 2022 18:13:55 GMT
ARG VAULT_VERSION=1.10.4
# Mon, 13 Jun 2022 18:13:56 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN addgroup vault &&     adduser -S -G vault vault
# Mon, 13 Jun 2022 18:14:03 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Mon, 13 Jun 2022 18:14:04 GMT
# ARGS: VAULT_VERSION=1.10.4
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Mon, 13 Jun 2022 18:14:05 GMT
VOLUME [/vault/logs]
# Mon, 13 Jun 2022 18:14:06 GMT
VOLUME [/vault/file]
# Mon, 13 Jun 2022 18:14:07 GMT
EXPOSE 8200
# Mon, 13 Jun 2022 18:14:09 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 13 Jun 2022 18:14:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 13 Jun 2022 18:14:10 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:c11e5e1035714514f6e237dffd1836a4d03b48af64e55a8e08f9bd9e998e24a9`  
		Last Modified: Mon, 04 Apr 2022 23:39:35 GMT  
		Size: 2.8 MB (2821213 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4e1d9390f44be2481e68855bbacbc26bda53df65c485f2bfaf96e56c07d76fb`  
		Last Modified: Mon, 13 Jun 2022 18:15:34 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2e119de0d80e6722bd60c1468bb9db0c68680e6651bb9080e90652e5279a538`  
		Last Modified: Mon, 13 Jun 2022 18:15:41 GMT  
		Size: 67.6 MB (67591806 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8e600ecb98fcc365bbc6a8a4e0aa99019104ac77e7f130b18fdce9a8f111cf6`  
		Last Modified: Mon, 13 Jun 2022 18:15:34 GMT  
		Size: 156.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11ef0168d92e1c9e7db9ff79fd56ca4d9cb77257ad9eba22bd8b9a4be1ec589c`  
		Last Modified: Mon, 13 Jun 2022 18:15:34 GMT  
		Size: 1.8 KB (1815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
