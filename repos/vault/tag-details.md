<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `vault`

-	[`vault:1.11.11`](#vault11111)
-	[`vault:1.12.7`](#vault1127)
-	[`vault:1.13.3`](#vault1133)

## `vault:1.11.11`

```console
$ docker pull vault@sha256:129b11496a43d9ba4bf8d83a2c51b9e4f4e0d035586aedd042a9968501c7bf5a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.11.11` - linux; amd64

```console
$ docker pull vault@sha256:a23439e085e4c50067bdb6aa40b7f9f1cf16fc01e25fdfdb998ff62bebb92986
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.8 MB (81824306 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dd85824e359d4e41493ed08e2823b892d6375af97b24402ac56f221afeb65c25`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 00:07:06 GMT
ARG VAULT_VERSION=1.11.11
# Fri, 29 Sep 2023 00:07:06 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 29 Sep 2023 00:07:14 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 29 Sep 2023 00:07:15 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 29 Sep 2023 00:07:15 GMT
VOLUME [/vault/logs]
# Fri, 29 Sep 2023 00:07:15 GMT
VOLUME [/vault/file]
# Fri, 29 Sep 2023 00:07:15 GMT
EXPOSE 8200
# Fri, 29 Sep 2023 00:07:15 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 29 Sep 2023 00:07:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 00:07:15 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf2c9ab0ded498575f799a79107c1c80e28b1a4392b3d2559908df8d42ca4bfb`  
		Last Modified: Fri, 29 Sep 2023 00:07:59 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92493ca771cec79212603df7fff2364c0292dd40e7dc37d48c467b8f8bfd1a74`  
		Last Modified: Fri, 29 Sep 2023 00:08:09 GMT  
		Size: 78.4 MB (78419071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5695a5b0b8e124c51c179f7c76b6130199f10b745b9c8f563f17d57cb1f85638`  
		Last Modified: Fri, 29 Sep 2023 00:07:59 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c06141266126e408e01e2ac36e9de1ae0b1354523195fcdc8802dbb669f5d87`  
		Last Modified: Fri, 29 Sep 2023 00:07:59 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.11.11` - linux; arm variant v6

```console
$ docker pull vault@sha256:b420f0002255d2c48eba876d529493e9562d0f386f3d9d79c8f08684b8247098
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **76.9 MB (76870059 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:58e512df1a2149adbc0b33b0394ccbd03269b013a0fc490bdbe7410fdbc00f91`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:38:26 GMT
ARG VAULT_VERSION=1.11.11
# Tue, 08 Aug 2023 23:38:26 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 08 Aug 2023 23:38:37 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 08 Aug 2023 23:38:37 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 08 Aug 2023 23:38:38 GMT
VOLUME [/vault/logs]
# Tue, 08 Aug 2023 23:38:38 GMT
VOLUME [/vault/file]
# Tue, 08 Aug 2023 23:38:38 GMT
EXPOSE 8200
# Tue, 08 Aug 2023 23:38:38 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 08 Aug 2023 23:38:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 23:38:38 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:280f2e276e7d0773e3d17d726bdb6aa4dc0bb77a54c2b26e0e2ac24a77f9879a`  
		Last Modified: Tue, 08 Aug 2023 23:39:26 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6a36d2ef0efea12bd35890856d8aa91db7b0f19db07e30a48fcab08508fc107`  
		Last Modified: Tue, 08 Aug 2023 23:39:36 GMT  
		Size: 73.7 MB (73721982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44f58cdaef8d2d7d420b30f2aaa7c93d8eb3abb1f95730024c25a12de362373`  
		Last Modified: Tue, 08 Aug 2023 23:39:26 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ca35828012cf3788c2be96ddef1974c97077907c10d522188597622d0cbc09c`  
		Last Modified: Tue, 08 Aug 2023 23:39:27 GMT  
		Size: 1.8 KB (1810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.11.11` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:818336490860f6d59955a4a69f78418ee6d2109cabce93aa2ed064aac2062f17
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **77.1 MB (77143597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d724f7dea59ffc9c97e8c9d55832a4bc36998176c69437a3693b429327e322b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 04:31:56 GMT
ARG VAULT_VERSION=1.11.11
# Wed, 09 Aug 2023 04:31:57 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 09 Aug 2023 04:32:05 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 09 Aug 2023 04:32:07 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 09 Aug 2023 04:32:07 GMT
VOLUME [/vault/logs]
# Wed, 09 Aug 2023 04:32:07 GMT
VOLUME [/vault/file]
# Wed, 09 Aug 2023 04:32:07 GMT
EXPOSE 8200
# Wed, 09 Aug 2023 04:32:07 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 09 Aug 2023 04:32:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Aug 2023 04:32:07 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fadfa6c8d27df7a004387659b7b617a6616bb3ce6ee3a8fefdd38b5bd7bc74f6`  
		Last Modified: Wed, 09 Aug 2023 04:32:45 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f0016785c5a0e363ef871a16b191d6869f90e531fb8176b411d57b555e18a7`  
		Last Modified: Wed, 09 Aug 2023 04:32:52 GMT  
		Size: 73.8 MB (73809564 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ae39bc44a876e6b79e422d7b9520ebd4bf8dba1b3f20040ee8dfb80d481c341`  
		Last Modified: Wed, 09 Aug 2023 04:32:45 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ac497e4707d69f1171854dc837e3247fc6acc67305860216c5b055a2ce8f16`  
		Last Modified: Wed, 09 Aug 2023 04:32:45 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.11.11` - linux; 386

```console
$ docker pull vault@sha256:ce680c4922336c8e97f7fcd315645d1eb7ffbb42a83bf06cfcbe096e4d982ea5
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **78.5 MB (78457993 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a17d0eae8f4e29a945769473d6524958215fa478338215c67650b3038da04df9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:26 GMT
ADD file:4b33c52e11b19fde30197c62ead0b77bde28d34edaa08346a5302cd892d3cebe in / 
# Mon, 07 Aug 2023 19:38:27 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 22:32:10 GMT
ARG VAULT_VERSION=1.11.11
# Tue, 08 Aug 2023 22:32:10 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 08 Aug 2023 22:32:22 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 08 Aug 2023 22:32:23 GMT
# ARGS: VAULT_VERSION=1.11.11
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 08 Aug 2023 22:32:23 GMT
VOLUME [/vault/logs]
# Tue, 08 Aug 2023 22:32:23 GMT
VOLUME [/vault/file]
# Tue, 08 Aug 2023 22:32:23 GMT
EXPOSE 8200
# Tue, 08 Aug 2023 22:32:24 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 08 Aug 2023 22:32:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 22:32:24 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:95dc695758361a4038a2d9026959d72e1f531114edb0341be7ce47d912ef069e`  
		Last Modified: Mon, 07 Aug 2023 19:38:56 GMT  
		Size: 3.2 MB (3235144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78432155bee69bdecb1efdad9ade62fb81c3beae5a600d1a1503ead3013ade0f`  
		Last Modified: Tue, 08 Aug 2023 22:33:11 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69f87d16f57c7acbf968d12685494f576980434cfd9aee05709380946fb379be`  
		Last Modified: Tue, 08 Aug 2023 22:33:23 GMT  
		Size: 75.2 MB (75219585 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29eb17d89eebe793cdf44310e2986c8e3ac92b604f886f4e004910596c3233af`  
		Last Modified: Tue, 08 Aug 2023 22:33:11 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f058d67e13ff2c9f62b95ec4a3050f4d59008cf79d88c35887f312250f6f5c77`  
		Last Modified: Tue, 08 Aug 2023 22:33:11 GMT  
		Size: 1.8 KB (1811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.12.7`

```console
$ docker pull vault@sha256:80fbd66d4c58fcc6721bc7a3604f28b30fc6284919cecb6bcf38fed81241fcc7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.12.7` - linux; amd64

```console
$ docker pull vault@sha256:515f333eb10b95d9fa27a3d318f017541829e315dbf3b515309835706f821131
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **86.6 MB (86570224 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:08fc0d6f8f6d0aaac20ae5b75374e5b82f09270311945ae986d3719682e5cfa8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 00:06:51 GMT
ARG VAULT_VERSION=1.12.7
# Fri, 29 Sep 2023 00:06:52 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 29 Sep 2023 00:07:00 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 29 Sep 2023 00:07:01 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 29 Sep 2023 00:07:01 GMT
VOLUME [/vault/logs]
# Fri, 29 Sep 2023 00:07:01 GMT
VOLUME [/vault/file]
# Fri, 29 Sep 2023 00:07:01 GMT
EXPOSE 8200
# Fri, 29 Sep 2023 00:07:01 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 29 Sep 2023 00:07:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 00:07:01 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e57ce1274ceb300782691e4a9af2c963d665e1463760085bdfaf6de26e80a47b`  
		Last Modified: Fri, 29 Sep 2023 00:07:43 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6366ea4566160a176342530fc9951b055f855a139aeb25a6f54f41df7350b22`  
		Last Modified: Fri, 29 Sep 2023 00:07:53 GMT  
		Size: 83.2 MB (83164989 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6cc4e80bac95e7cf32632d02b9d7127941929eee8d4bd6425204098d9ab02cf`  
		Last Modified: Fri, 29 Sep 2023 00:07:43 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b59a4bc4e88ec41daeef117fbc6a59732dcebba5bb8c7bd83c2f85e9af1af75`  
		Last Modified: Fri, 29 Sep 2023 00:07:43 GMT  
		Size: 1.8 KB (1812 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.12.7` - linux; arm variant v6

```console
$ docker pull vault@sha256:68e227f17e69579301fd6f738697dc747890e4eb5b9fd73c0ebcc697c2c62e13
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.2 MB (81228181 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c52e7e47fdd5c35032612c8b61ec7ddf94a2fe27903d584bdb5c6385934e2a84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:38:10 GMT
ARG VAULT_VERSION=1.12.7
# Tue, 08 Aug 2023 23:38:10 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 08 Aug 2023 23:38:22 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 08 Aug 2023 23:38:23 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 08 Aug 2023 23:38:23 GMT
VOLUME [/vault/logs]
# Tue, 08 Aug 2023 23:38:23 GMT
VOLUME [/vault/file]
# Tue, 08 Aug 2023 23:38:24 GMT
EXPOSE 8200
# Tue, 08 Aug 2023 23:38:24 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 08 Aug 2023 23:38:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 23:38:24 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37f1ed961eb968c889c9733f49dfd6a0fdb94b5f952d840d20de026fb5c15ae9`  
		Last Modified: Tue, 08 Aug 2023 23:39:06 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2440a58fb6e310b1cfe8f42026ff3170911938596bf28be0116a6bbf9891314f`  
		Last Modified: Tue, 08 Aug 2023 23:39:20 GMT  
		Size: 78.1 MB (78080103 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:406c30921d229b68ddbe7e2c17ef688b432c96dbaebf7b9bc988b2eb74b7c3e0`  
		Last Modified: Tue, 08 Aug 2023 23:39:06 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3ce40be8d676ef8010de8fb68f1ccfa2c0c1465e4d871d0f7127359f453cdcf`  
		Last Modified: Tue, 08 Aug 2023 23:39:06 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.12.7` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:a57ea9548a8b1209869005844e8680773ece61d205c19e8ff64e9b217699ee0a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **81.7 MB (81674464 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:06dea4e4f269c403dc1c03605139cb96fdde50991adf1823da1580e79a9d84d9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 04:31:43 GMT
ARG VAULT_VERSION=1.12.7
# Wed, 09 Aug 2023 04:31:43 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 09 Aug 2023 04:31:51 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 09 Aug 2023 04:31:53 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 09 Aug 2023 04:31:53 GMT
VOLUME [/vault/logs]
# Wed, 09 Aug 2023 04:31:53 GMT
VOLUME [/vault/file]
# Wed, 09 Aug 2023 04:31:53 GMT
EXPOSE 8200
# Wed, 09 Aug 2023 04:31:53 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 09 Aug 2023 04:31:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Aug 2023 04:31:53 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c29256805d4abfd620876c2ae53eeb4e546bb9fa2330fe8a584296d67295daa8`  
		Last Modified: Wed, 09 Aug 2023 04:32:32 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40e7e474fd9c19ec87128f0b49685aa2f41357249cdc0bdfd2c9cbd55fbe2cf0`  
		Last Modified: Wed, 09 Aug 2023 04:32:39 GMT  
		Size: 78.3 MB (78340429 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a9a22b1c9507c9014110ecfa0cbba3e7ff4b401bb14139db9aeb1a38488db7`  
		Last Modified: Wed, 09 Aug 2023 04:32:32 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e5c628ae9e61fdb909243df83c6e3de40c50d3dafc84a280b85db9c2e6462e78`  
		Last Modified: Wed, 09 Aug 2023 04:32:33 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.12.7` - linux; 386

```console
$ docker pull vault@sha256:1e646b0fc35ca5fadf605e6a943df59c78c1f374cc681574c12470f7ecf2fdeb
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **82.8 MB (82842079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7cc054fc4559095c0d96d2a0f9d99045464d2ae6979ce12bd58af2173b41c502`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:26 GMT
ADD file:4b33c52e11b19fde30197c62ead0b77bde28d34edaa08346a5302cd892d3cebe in / 
# Mon, 07 Aug 2023 19:38:27 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 22:31:54 GMT
ARG VAULT_VERSION=1.12.7
# Tue, 08 Aug 2023 22:31:54 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 08 Aug 2023 22:32:06 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 08 Aug 2023 22:32:07 GMT
# ARGS: VAULT_VERSION=1.12.7
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 08 Aug 2023 22:32:08 GMT
VOLUME [/vault/logs]
# Tue, 08 Aug 2023 22:32:08 GMT
VOLUME [/vault/file]
# Tue, 08 Aug 2023 22:32:08 GMT
EXPOSE 8200
# Tue, 08 Aug 2023 22:32:08 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 08 Aug 2023 22:32:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 22:32:08 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:95dc695758361a4038a2d9026959d72e1f531114edb0341be7ce47d912ef069e`  
		Last Modified: Mon, 07 Aug 2023 19:38:56 GMT  
		Size: 3.2 MB (3235144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f16bfe3cbbd55209f3f2097992a7d28016c7a36a211fc28aed97a00da42300f6`  
		Last Modified: Tue, 08 Aug 2023 22:32:53 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2eb5a9d42b224a0d4baeabc30826aa769763d8e890df06744b2dd87d8593f44`  
		Last Modified: Tue, 08 Aug 2023 22:33:05 GMT  
		Size: 79.6 MB (79603664 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69900e1ee56d826803c24d494c8a80ceecd7c57c343f7f297c48e83a89d64153`  
		Last Modified: Tue, 08 Aug 2023 22:32:53 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1930cb953612fbff81f510170d60691ba8587a597bf60e5789f6421bd1c1ca5e`  
		Last Modified: Tue, 08 Aug 2023 22:32:53 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `vault:1.13.3`

```console
$ docker pull vault@sha256:6a22c0a835c675dd7eba13eb394fb8a4740c7fbce3d123eece89dd19b875f680
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:1.13.3` - linux; amd64

```console
$ docker pull vault@sha256:d639ad7bebc3ddcbc88f529b4f8baa85743a9a24248c4285d958f90f56682836
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **97.6 MB (97610963 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6d1fcd1a47eb84358f17a6918352cdf576f606d9fc9d36e8d13d9c9315ad89f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 28 Sep 2023 21:19:27 GMT
ADD file:756183bba9c7f4593c2b216e98e4208b9163c4c962ea0837ef88bd917609d001 in / 
# Thu, 28 Sep 2023 21:19:27 GMT
CMD ["/bin/sh"]
# Fri, 29 Sep 2023 00:06:37 GMT
ARG VAULT_VERSION=1.13.3
# Fri, 29 Sep 2023 00:06:37 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 29 Sep 2023 00:06:46 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 29 Sep 2023 00:06:47 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 29 Sep 2023 00:06:47 GMT
VOLUME [/vault/logs]
# Fri, 29 Sep 2023 00:06:47 GMT
VOLUME [/vault/file]
# Fri, 29 Sep 2023 00:06:47 GMT
EXPOSE 8200
# Fri, 29 Sep 2023 00:06:47 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 29 Sep 2023 00:06:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 29 Sep 2023 00:06:47 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:96526aa774ef0126ad0fe9e9a95764c5fc37f409ab9e97021e7b4775d82bf6fa`  
		Last Modified: Thu, 28 Sep 2023 21:22:06 GMT  
		Size: 3.4 MB (3401967 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb96b81cd1906c01728b67a48938978114de18094c6bc88ae674b58bf343f853`  
		Last Modified: Fri, 29 Sep 2023 00:07:24 GMT  
		Size: 1.3 KB (1271 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29f5d86fa0f2da37d5dc8672c53fe2d4895073dcec759fdeed587f279afcbe83`  
		Last Modified: Fri, 29 Sep 2023 00:07:37 GMT  
		Size: 94.2 MB (94205728 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01c0e14a2dc26dfa04dbee8d5ed1efd8f8de4df2da04a915a4e376d8a296ef26`  
		Last Modified: Fri, 29 Sep 2023 00:07:24 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:28703b214f38bf539e7163a2bfeaa31e5cd42d0e84f7262ecd8e1ecc0b07d4a9`  
		Last Modified: Fri, 29 Sep 2023 00:07:24 GMT  
		Size: 1.8 KB (1810 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.13.3` - linux; arm variant v6

```console
$ docker pull vault@sha256:70007bcc604f014cbd13fe57d4600e80827156751c9ca7a99b632e40fbeaeb74
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **91.6 MB (91637405 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:560a797bd44045aa6fb590eefe9833c8d80efb1ccc815a9432b35483a0fc1e84`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 07 Aug 2023 19:49:14 GMT
ADD file:9882e99e5f94ab2db05c029648ac5be7cf0f063a8701394fcbb543a7ef5d4b90 in / 
# Mon, 07 Aug 2023 19:49:15 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 23:37:53 GMT
ARG VAULT_VERSION=1.13.3
# Tue, 08 Aug 2023 23:37:54 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 08 Aug 2023 23:38:05 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 08 Aug 2023 23:38:07 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 08 Aug 2023 23:38:07 GMT
VOLUME [/vault/logs]
# Tue, 08 Aug 2023 23:38:07 GMT
VOLUME [/vault/file]
# Tue, 08 Aug 2023 23:38:07 GMT
EXPOSE 8200
# Tue, 08 Aug 2023 23:38:07 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 08 Aug 2023 23:38:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 23:38:07 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:af09961d4a43b504efc76e38b50918977c28be73eeb8b926247783a00e8b9f2f`  
		Last Modified: Mon, 07 Aug 2023 19:49:38 GMT  
		Size: 3.1 MB (3144809 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2156767444d4c31743363ccd2aa55fd4f3f406ca0b35343c702fcc160a90c1c4`  
		Last Modified: Tue, 08 Aug 2023 23:38:49 GMT  
		Size: 1.3 KB (1270 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f82bf6bf5a1fcab510985e0eaf07f14b682cc3bf1f4e3d25f6cc08b92f346643`  
		Last Modified: Tue, 08 Aug 2023 23:39:00 GMT  
		Size: 88.5 MB (88489324 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0234085ac76da44f2307b1fa0b21abf4232e3177f3377d469340c2f642fc13f3`  
		Last Modified: Tue, 08 Aug 2023 23:38:49 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f34958d632052bda83e7fd75880233f6651c374f5b2397f9d772e9c4d2d97c63`  
		Last Modified: Tue, 08 Aug 2023 23:38:49 GMT  
		Size: 1.8 KB (1813 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.13.3` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:bb869710a10265c9e5d8c53c282de2a2ca6eacf572fc8742c55789b92e199edd
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **92.2 MB (92162384 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9b6f142cf0e35552b4b37cbfcad60e1349d1d62499905731360feb1696cf20ae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:19 GMT
ADD file:b2e7eaa7e41f08853dbe08d84439a7f9fd32fc58c3aa1e298f3f60343b2b683a in / 
# Mon, 07 Aug 2023 19:39:19 GMT
CMD ["/bin/sh"]
# Wed, 09 Aug 2023 04:31:29 GMT
ARG VAULT_VERSION=1.13.3
# Wed, 09 Aug 2023 04:31:30 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN addgroup vault &&     adduser -S -G vault vault
# Wed, 09 Aug 2023 04:31:38 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Wed, 09 Aug 2023 04:31:40 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Wed, 09 Aug 2023 04:31:40 GMT
VOLUME [/vault/logs]
# Wed, 09 Aug 2023 04:31:40 GMT
VOLUME [/vault/file]
# Wed, 09 Aug 2023 04:31:40 GMT
EXPOSE 8200
# Wed, 09 Aug 2023 04:31:40 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 09 Aug 2023 04:31:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 09 Aug 2023 04:31:40 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:9fda8d8052c61740409c4bea888859c141fd8cc3f58ac61943144ff6d1681b2d`  
		Last Modified: Mon, 07 Aug 2023 19:39:45 GMT  
		Size: 3.3 MB (3330767 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a232d2dfa356ddae491bd7f90e42bec5e86453bf37a2f6948d4c5f2ce8645fd8`  
		Last Modified: Wed, 09 Aug 2023 04:32:18 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f068f41cc0b60a3ac41fc05aeab5857d8d7ee6ac3f265e7e11647c46f25f9f3`  
		Last Modified: Wed, 09 Aug 2023 04:32:26 GMT  
		Size: 88.8 MB (88828350 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cdf3a449b0392098bd785d1cc0b95a28ef3e049813c4126c57567687d1980ef3`  
		Last Modified: Wed, 09 Aug 2023 04:32:18 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67c169708548e77e21de14173dd9b1974dd5d6ebc8113a879b59df63f88dec3b`  
		Last Modified: Wed, 09 Aug 2023 04:32:18 GMT  
		Size: 1.8 KB (1814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:1.13.3` - linux; 386

```console
$ docker pull vault@sha256:3b0be5ed26c804a59b66991f429f59ed0e786a9b6a89662dd4e4720b0d4c8876
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **93.3 MB (93257289 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8247e8f3f2cfca6802846969de74f3fd2f686c85f789b17e90784aa2d0cb4b37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:26 GMT
ADD file:4b33c52e11b19fde30197c62ead0b77bde28d34edaa08346a5302cd892d3cebe in / 
# Mon, 07 Aug 2023 19:38:27 GMT
CMD ["/bin/sh"]
# Tue, 08 Aug 2023 22:31:37 GMT
ARG VAULT_VERSION=1.13.3
# Tue, 08 Aug 2023 22:31:38 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN addgroup vault &&     adduser -S -G vault vault
# Tue, 08 Aug 2023 22:31:49 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=C874011F0AB405110D02105534365D9472D7468F;     found='';     for server in         hkps://keys.openpgp.org         hkps://keyserver.ubuntu.com         hkps://pgp.mit.edu     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cp /tmp/build/vault /bin/vault &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/EULA.txt /usr/share/doc/vault/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/vault; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/vault/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Tue, 08 Aug 2023 22:31:50 GMT
# ARGS: VAULT_VERSION=1.13.3
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Tue, 08 Aug 2023 22:31:50 GMT
VOLUME [/vault/logs]
# Tue, 08 Aug 2023 22:31:50 GMT
VOLUME [/vault/file]
# Tue, 08 Aug 2023 22:31:50 GMT
EXPOSE 8200
# Tue, 08 Aug 2023 22:31:51 GMT
COPY file:284725e82dfade67c8b2092585f70a151b8782d83106082a5b4852b996b7e550 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 08 Aug 2023 22:31:51 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 08 Aug 2023 22:31:51 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:95dc695758361a4038a2d9026959d72e1f531114edb0341be7ce47d912ef069e`  
		Last Modified: Mon, 07 Aug 2023 19:38:56 GMT  
		Size: 3.2 MB (3235144 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:364df086ffbef3c77794150521f7047346239d4c91fe1e708831a4e5228fb4c8`  
		Last Modified: Tue, 08 Aug 2023 22:32:34 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bf07ad172204b23bf5cac2621f4f81ea847b615983ebf08f1027815cf66b919`  
		Last Modified: Tue, 08 Aug 2023 22:32:47 GMT  
		Size: 90.0 MB (90018882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a64676d5c3b49dc2e26606cb55ce22a9dacde41bf5404dadccbcdcba2ef49b7`  
		Last Modified: Tue, 08 Aug 2023 22:32:33 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:61b41fe279b5833f91f809955d3a1e29ba45f23fc554182bd05dd45f0144dd22`  
		Last Modified: Tue, 08 Aug 2023 22:32:33 GMT  
		Size: 1.8 KB (1807 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
