## `vault:latest`

```console
$ docker pull vault@sha256:636539e5ab2dd0942061faeb232452774103a25e82bca969cb37945616aeae53
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `vault:latest` - linux; amd64

```console
$ docker pull vault@sha256:d51a9c82d0d45857acabea988c7b2ec673855438a7718138569d199e80db2ad3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **72.7 MB (72706694 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b359df68a663cd5d2528caab398298a176375aeaa13ae199d8b5f615c2a38bce`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:19:32 GMT
ADD file:6b081cabb4b256ee07587d249c4989b5b679375529542b81550a65b6f19f274e in / 
# Thu, 25 Mar 2021 22:19:32 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 05:02:55 GMT
ARG VAULT_VERSION=1.7.0
# Fri, 26 Mar 2021 05:02:56 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 05:03:07 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 05:03:09 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 05:03:09 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 05:03:09 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 05:03:10 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 05:03:10 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 05:03:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 05:03:11 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:9aae54b2144e5b2b00c610f8805128f4f86822e1e52d3714c463744a431f0f4a`  
		Last Modified: Thu, 25 Mar 2021 22:20:18 GMT  
		Size: 2.8 MB (2811681 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1d6dd05beb921063752a0e4b43d2dc08582069eaaeb4e32ffa7a370ede3515`  
		Last Modified: Fri, 26 Mar 2021 05:04:52 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4de46febc3613de2118ec655d1fffbe87968c11570858a476e7dc4fd74c6ff4`  
		Last Modified: Fri, 26 Mar 2021 05:05:03 GMT  
		Size: 69.9 MB (69891751 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc279c1e752b4ac2f1af5f2c54603b7bbf0e712414a1383d79b2c684b895ff4`  
		Last Modified: Fri, 26 Mar 2021 05:04:52 GMT  
		Size: 189.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e437bfd1f45e31c4442a7038debd89139a36421ac53cf2e579c1f773a45432ea`  
		Last Modified: Fri, 26 Mar 2021 05:04:52 GMT  
		Size: 1.8 KB (1818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm variant v6

```console
$ docker pull vault@sha256:dfe5c6742e2c313a574f34a2e4fd5ea5e60ca2633498e74cb6cf9577dd4d7e6c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **66.7 MB (66726546 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cc64e5a7e7875e54681c1a1766c6d5672947c5023851f4866771bd752b0f94a3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 17 Feb 2021 20:49:32 GMT
ADD file:c04fbd3b039001c592cfa14f8388f8934ed4223ccf274dbb926e75039e172af4 in / 
# Wed, 17 Feb 2021 20:49:33 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 01:03:46 GMT
ARG VAULT_VERSION=1.7.0
# Thu, 25 Mar 2021 01:03:51 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 25 Mar 2021 01:04:06 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 25 Mar 2021 01:04:10 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 25 Mar 2021 01:04:11 GMT
VOLUME [/vault/logs]
# Thu, 25 Mar 2021 01:04:13 GMT
VOLUME [/vault/file]
# Thu, 25 Mar 2021 01:04:13 GMT
EXPOSE 8200
# Thu, 25 Mar 2021 01:04:14 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 25 Mar 2021 01:04:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Mar 2021 01:04:16 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:1353527ebe111f9bb1e271264a3c182e909e4b36463f80d7dbde1be0713eb892`  
		Last Modified: Wed, 17 Feb 2021 20:50:06 GMT  
		Size: 2.6 MB (2622039 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c7303dbc8fff63055f01b5e582ca32737dc8a80653e1f42e05799670f9aed479`  
		Last Modified: Thu, 25 Mar 2021 01:05:27 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:624bbd3dfaaf5a4bfd1713635f9c6337c972967fc53cd2da82046cccfa6db258`  
		Last Modified: Thu, 25 Mar 2021 01:05:44 GMT  
		Size: 64.1 MB (64101238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fa2f5fb2239acd5f8ee0da5bded2d3f842e8f8d51dc7ed835a469f1adb16cd3a`  
		Last Modified: Thu, 25 Mar 2021 01:05:27 GMT  
		Size: 188.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1d198e7656fbdcaf409b9974f399ff8ab9abc75372b406403a538645b884240`  
		Last Modified: Thu, 25 Mar 2021 01:05:28 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; arm64 variant v8

```console
$ docker pull vault@sha256:7bb03087f1872bba59add852953ac3e35a54d63798a5a42d53cc147d335150d4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **68.5 MB (68535695 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ef7c6e9941803130f0b68e0749e872a59bd13cd4c57b0aae51a46a532a37a3d2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Thu, 25 Mar 2021 22:40:10 GMT
ADD file:8d7431f7e3e42b162a1626e7abf4ef7605146671dccc753d490de6b7fe429261 in / 
# Thu, 25 Mar 2021 22:40:23 GMT
CMD ["/bin/sh"]
# Fri, 26 Mar 2021 08:13:10 GMT
ARG VAULT_VERSION=1.7.0
# Fri, 26 Mar 2021 08:13:13 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Fri, 26 Mar 2021 08:13:22 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Fri, 26 Mar 2021 08:13:25 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Fri, 26 Mar 2021 08:13:27 GMT
VOLUME [/vault/logs]
# Fri, 26 Mar 2021 08:13:28 GMT
VOLUME [/vault/file]
# Fri, 26 Mar 2021 08:13:30 GMT
EXPOSE 8200
# Fri, 26 Mar 2021 08:13:31 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 26 Mar 2021 08:13:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 26 Mar 2021 08:13:33 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:5ceb5101e3b0d54efb5f18318982508a04b181b4d5ae52b096dd35dea3a006cc`  
		Last Modified: Thu, 25 Mar 2021 22:44:41 GMT  
		Size: 2.7 MB (2711898 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:532760a713fdcc47b0750cf149032179ac109897d27a4a7387254e873782ef5a`  
		Last Modified: Fri, 26 Mar 2021 08:16:21 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2da9e5d008656a72a376d31d7c1cf4c750c1d20fdc9725470e92748f3d902aeb`  
		Last Modified: Fri, 26 Mar 2021 08:16:38 GMT  
		Size: 65.8 MB (65820533 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6121bcad7cba7d37518917de5d2e4bb729cc62708b2c847ea1df48ccb757483f`  
		Last Modified: Fri, 26 Mar 2021 08:16:21 GMT  
		Size: 187.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8253019ed837881d065d263f197f95708f7073be3629b60a1e367d07f44a853c`  
		Last Modified: Fri, 26 Mar 2021 08:16:21 GMT  
		Size: 1.8 KB (1821 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `vault:latest` - linux; 386

```console
$ docker pull vault@sha256:9ca9c858c4c5fc19f6527c3a238cbdea0fa9c40201aa6dacb74ac8ecb44178c4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **70.6 MB (70570068 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6444ddc13b71ba29ad4262acb8347705e3186bce68856b0002722465f8fe8502`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["server","-dev"]`

```dockerfile
# Wed, 17 Feb 2021 21:38:34 GMT
ADD file:eaee53da3c87749799de55809e4a5b526c56855332b961a85b1184c660f1d65b in / 
# Wed, 17 Feb 2021 21:38:35 GMT
CMD ["/bin/sh"]
# Thu, 25 Mar 2021 00:53:26 GMT
ARG VAULT_VERSION=1.7.0
# Thu, 25 Mar 2021 00:53:27 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN addgroup vault &&     adduser -S -G vault vault
# Thu, 25 Mar 2021 00:53:35 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN set -eux;     apk add --no-cache ca-certificates gnupg openssl libcap su-exec dumb-init tzdata &&     apkArch="$(apk --print-arch)";     case "$apkArch" in         armhf) ARCH='arm' ;;         aarch64) ARCH='arm64' ;;         x86_64) ARCH='amd64' ;;         x86) ARCH='386' ;;         *) echo >&2 "error: unsupported architecture: $apkArch"; exit 1 ;;     esac &&     VAULT_GPGKEY=91A6E7F85D05C65630BEF18951852D87348FFC4C;     found='';     for server in         hkp://p80.pool.sks-keyservers.net:80         hkp://keyserver.ubuntu.com:80         hkp://pgp.mit.edu:80     ; do         echo "Fetching GPG key $VAULT_GPGKEY from $server";         gpg --batch --keyserver "$server" --recv-keys "$VAULT_GPGKEY" && found=yes && break;     done;     test -z "$found" && echo >&2 "error: failed to fetch GPG key $VAULT_GPGKEY" && exit 1;     mkdir -p /tmp/build &&     cd /tmp/build &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS &&     wget https://releases.hashicorp.com/vault/${VAULT_VERSION}/vault_${VAULT_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify vault_${VAULT_VERSION}_SHA256SUMS.sig vault_${VAULT_VERSION}_SHA256SUMS &&     grep vault_${VAULT_VERSION}_linux_${ARCH}.zip vault_${VAULT_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin vault_${VAULT_VERSION}_linux_${ARCH}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill dirmngr &&     gpgconf --kill gpg-agent &&     apk del gnupg openssl &&     rm -rf /root/.gnupg
# Thu, 25 Mar 2021 00:53:36 GMT
# ARGS: VAULT_VERSION=1.7.0
RUN mkdir -p /vault/logs &&     mkdir -p /vault/file &&     mkdir -p /vault/config &&     chown -R vault:vault /vault
# Thu, 25 Mar 2021 00:53:37 GMT
VOLUME [/vault/logs]
# Thu, 25 Mar 2021 00:53:37 GMT
VOLUME [/vault/file]
# Thu, 25 Mar 2021 00:53:37 GMT
EXPOSE 8200
# Thu, 25 Mar 2021 00:53:37 GMT
COPY file:a1e68ac70727f49824592e948e9a677097c8d3752a047b468122ba433b453fc4 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 25 Mar 2021 00:53:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 25 Mar 2021 00:53:38 GMT
CMD ["server" "-dev"]
```

-	Layers:
	-	`sha256:86205afa28f6bc624469015a543d16608258d2828411a92c662f4fdc6d276e18`  
		Last Modified: Wed, 17 Feb 2021 21:39:07 GMT  
		Size: 2.8 MB (2818177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca768045b18d821bd7431ec5078619ab1ef0c99fb0ff614bfdaaa9665278029`  
		Last Modified: Thu, 25 Mar 2021 00:54:32 GMT  
		Size: 1.3 KB (1253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:499c2c4856c3e0862f29ef4729b42c6eb0a5afde44966cd810da36db6716fc6e`  
		Last Modified: Thu, 25 Mar 2021 00:54:42 GMT  
		Size: 67.7 MB (67748633 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65a0103fd85fb669bfde787d1f69ca52754be530ed43599423687363e29e1948`  
		Last Modified: Thu, 25 Mar 2021 00:54:33 GMT  
		Size: 186.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17cea17112d0c6e8d055ddd4d3c66dca71c604283ca12327457059b643ef5d60`  
		Last Modified: Thu, 25 Mar 2021 00:54:32 GMT  
		Size: 1.8 KB (1819 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
