<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.7`](#consul17)
-	[`consul:1.7.13`](#consul1713)
-	[`consul:1.8`](#consul18)
-	[`consul:1.8.9`](#consul189)
-	[`consul:1.9`](#consul19)
-	[`consul:1.9.4`](#consul194)
-	[`consul:latest`](#consullatest)

## `consul:1.7`

```console
$ docker pull consul@sha256:16138bedd4cfae1a21873116f45c87f32e4fb1d2763bfee8c441467bdad15473
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.7` - linux; amd64

```console
$ docker pull consul@sha256:73d7837259fe925e083bc5c4299377409df977ab1e4a3f7cf6d12f7dedb51c92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43109497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:540024263411f620aa8a17c93efaa51bd9eca28dde5c8661ce2f921728f1d181`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:19:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 24 Feb 2021 21:19:57 GMT
ARG CONSUL_VERSION=1.7.12
# Wed, 24 Feb 2021 21:19:57 GMT
LABEL org.opencontainers.image.version=1.7.12
# Wed, 24 Feb 2021 21:19:58 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 24 Feb 2021 21:19:59 GMT
# ARGS: CONSUL_VERSION=1.7.12
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 24 Feb 2021 21:20:08 GMT
# ARGS: CONSUL_VERSION=1.7.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 24 Feb 2021 21:20:09 GMT
# ARGS: CONSUL_VERSION=1.7.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 24 Feb 2021 21:20:10 GMT
# ARGS: CONSUL_VERSION=1.7.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 21:20:10 GMT
VOLUME [/consul/data]
# Wed, 24 Feb 2021 21:20:10 GMT
EXPOSE 8300
# Wed, 24 Feb 2021 21:20:10 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 24 Feb 2021 21:20:11 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 24 Feb 2021 21:20:11 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 21:20:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 21:20:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2785cec4ba498fcba748252781799fc4f401dec767f24a4af3be0ecf2fbec00f`  
		Last Modified: Wed, 24 Feb 2021 21:21:01 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3de04a3634d5da9ea8428384d03ba055e1224c525dcfc701b229e330574eddb0`  
		Last Modified: Wed, 24 Feb 2021 21:21:08 GMT  
		Size: 40.3 MB (40306774 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1ca2e0f91f93554273dff9d4632eb9474975b9c41b5e804a85f9ec93fb149ec`  
		Last Modified: Wed, 24 Feb 2021 21:21:02 GMT  
		Size: 140.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7dc98d1bf879ed15433b27102ab01a64d0a28be1e85cfe7730dddf7ea77184d0`  
		Last Modified: Wed, 24 Feb 2021 21:21:01 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbfa6885d14da90f8a2159d7971593d7e96c079930a47092b1108d6576a07e83`  
		Last Modified: Wed, 24 Feb 2021 21:21:01 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; arm variant v6

```console
$ docker pull consul@sha256:f990ab1abc0120ed522baf18b24eeacecf565f506a8918fe2875790455dde7cd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.8 MB (38816046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3666a38695e4da70cac3c9f0bfdc7a092d915d2a260ed5a56d3ddf3aed7840d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 24 Feb 2021 20:50:34 GMT
ADD file:8bbb59eeaad0cbcf11559bc6e2b4492aadf6822d1935ed50c710f8bed858b7b5 in / 
# Wed, 24 Feb 2021 20:50:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:08:49 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 24 Feb 2021 21:09:57 GMT
ARG CONSUL_VERSION=1.7.12
# Wed, 24 Feb 2021 21:09:57 GMT
LABEL org.opencontainers.image.version=1.7.12
# Wed, 24 Feb 2021 21:09:58 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 24 Feb 2021 21:10:00 GMT
# ARGS: CONSUL_VERSION=1.7.12
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 24 Feb 2021 21:10:08 GMT
# ARGS: CONSUL_VERSION=1.7.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 24 Feb 2021 21:10:10 GMT
# ARGS: CONSUL_VERSION=1.7.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 24 Feb 2021 21:10:13 GMT
# ARGS: CONSUL_VERSION=1.7.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 21:10:13 GMT
VOLUME [/consul/data]
# Wed, 24 Feb 2021 21:10:15 GMT
EXPOSE 8300
# Wed, 24 Feb 2021 21:10:17 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 24 Feb 2021 21:10:20 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 24 Feb 2021 21:10:21 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 21:10:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 21:10:22 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:55242616b0494f68f44470d864da746cd2a8f8f2d1ffca698114de64032247ef`  
		Last Modified: Wed, 24 Feb 2021 20:51:17 GMT  
		Size: 2.6 MB (2604518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c944bf641ab7727bd02b3d0fd27da04f983dbbcff042669224998d9f5c311d6e`  
		Last Modified: Wed, 24 Feb 2021 21:11:16 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09b8700f3feeda3267c0e8af869831c37486fabd7026c169c931b50a098c1cab`  
		Last Modified: Wed, 24 Feb 2021 21:11:26 GMT  
		Size: 36.2 MB (36208240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6aa67fb0c9696d36f3a30187f1d28d7f5470854b503aa00b85b0b7f7b3ea6ef`  
		Last Modified: Wed, 24 Feb 2021 21:11:16 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fee136c9d66710e539278fea63f3f449532b2095717b24a543795ed8cca6835`  
		Last Modified: Wed, 24 Feb 2021 21:11:16 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce15a176cd671ecd64c0a7d8288d90e82b84b9e4f731164d22a6ce970536a060`  
		Last Modified: Wed, 24 Feb 2021 21:11:16 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:221cfec66905a2877b5a297623d93920722f90fc95d1c877c29d81116cbf59f6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.0 MB (39015063 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:28e7df078f7211f34bd7c42fb0d92832886f4205551a885cadead6c6dc2fd85f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:39 GMT
ADD file:7e82858ef85f6db90c131ed835a390d736cfdbd1a0cf8bccaeed8f7e30172ddb in / 
# Wed, 24 Feb 2021 20:39:40 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:29:40 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 24 Feb 2021 21:30:45 GMT
ARG CONSUL_VERSION=1.7.12
# Wed, 24 Feb 2021 21:30:46 GMT
LABEL org.opencontainers.image.version=1.7.12
# Wed, 24 Feb 2021 21:30:46 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 24 Feb 2021 21:30:49 GMT
# ARGS: CONSUL_VERSION=1.7.12
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 24 Feb 2021 21:30:57 GMT
# ARGS: CONSUL_VERSION=1.7.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 24 Feb 2021 21:30:59 GMT
# ARGS: CONSUL_VERSION=1.7.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 24 Feb 2021 21:31:01 GMT
# ARGS: CONSUL_VERSION=1.7.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 21:31:02 GMT
VOLUME [/consul/data]
# Wed, 24 Feb 2021 21:31:03 GMT
EXPOSE 8300
# Wed, 24 Feb 2021 21:31:05 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 24 Feb 2021 21:31:06 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 24 Feb 2021 21:31:07 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 21:31:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 21:31:09 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dce8679b510e95d136241d02ababff86469dd14220812a7ce9202833c0e32f66`  
		Last Modified: Wed, 24 Feb 2021 20:40:26 GMT  
		Size: 2.7 MB (2709880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5633e226e7a80bf920472cd374e9c6d332ab949a7816c64d230fddd3e0618995`  
		Last Modified: Wed, 24 Feb 2021 21:32:01 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:916236d799b9d2e6c72ae504a1177b79afa47d92adb53a02790ce00e6795f976`  
		Last Modified: Wed, 24 Feb 2021 21:32:09 GMT  
		Size: 36.3 MB (36301891 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e3811ea402e70972bb503e465519a20dc863196116ff53da1124a81f9bc114a`  
		Last Modified: Wed, 24 Feb 2021 21:32:01 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12ae5d6aea682a2cfb5d9ec521c644623e092ea8846323b226de89419ab2b44d`  
		Last Modified: Wed, 24 Feb 2021 21:32:01 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d9e0d6d32b20832849b44a92ceb055c8f8139b49d9b0b8bd60d4b4ef479b66f`  
		Last Modified: Wed, 24 Feb 2021 21:32:01 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; 386

```console
$ docker pull consul@sha256:815a213b1201ea1e86b5fa5a27722916ea4c6a1e3e247463acfb4d04215f92c3
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41906837 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:789515f75590466ba33f0adad049207cd0d99a1b56438833f1a6f6d31b0f309f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 24 Feb 2021 20:38:41 GMT
ADD file:1f1a1b55522505e78fcc069edb6c793371f78991e90dcb464e4ddac7efd6588c in / 
# Wed, 24 Feb 2021 20:38:41 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:55:01 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 24 Feb 2021 20:55:38 GMT
ARG CONSUL_VERSION=1.7.12
# Wed, 24 Feb 2021 20:55:38 GMT
LABEL org.opencontainers.image.version=1.7.12
# Wed, 24 Feb 2021 20:55:38 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 24 Feb 2021 20:55:39 GMT
# ARGS: CONSUL_VERSION=1.7.12
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 24 Feb 2021 20:55:45 GMT
# ARGS: CONSUL_VERSION=1.7.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 24 Feb 2021 20:55:45 GMT
# ARGS: CONSUL_VERSION=1.7.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 24 Feb 2021 20:55:46 GMT
# ARGS: CONSUL_VERSION=1.7.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:55:46 GMT
VOLUME [/consul/data]
# Wed, 24 Feb 2021 20:55:47 GMT
EXPOSE 8300
# Wed, 24 Feb 2021 20:55:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 24 Feb 2021 20:55:47 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 24 Feb 2021 20:55:47 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 20:55:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 20:55:48 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:045e8056601208133bee5c98e76028f9b97e055c738892f8d6283205e1006173`  
		Last Modified: Wed, 24 Feb 2021 20:39:27 GMT  
		Size: 2.8 MB (2794750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eea8f950aeecbcc7d559863b8a06226a5594acefed366f1da98bb69137cd8c4e`  
		Last Modified: Wed, 24 Feb 2021 20:56:29 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb86e71274113ef1614b90fdee71ad0ec2ab1c3faee59924aa45099d56c1f71a`  
		Last Modified: Wed, 24 Feb 2021 20:56:37 GMT  
		Size: 39.1 MB (39108856 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd4f863928d80df77b389bea2ba52577d3be9ee13c4ecfcbbe8454948060965`  
		Last Modified: Wed, 24 Feb 2021 20:56:29 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:36a473c6fbbc3f4b1499570ea27d3bc9c12fa1ee368b544f99cf80929f2afcc3`  
		Last Modified: Wed, 24 Feb 2021 20:56:29 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38901b4c81ccc34f16b011871ef0c5192180dc38bd532770a8dc4b3cdcd63ba9`  
		Last Modified: Wed, 24 Feb 2021 20:56:29 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.7.13`

```console
$ docker pull consul@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `consul:1.8`

```console
$ docker pull consul@sha256:b5d42cca79b2ea0f53644d19c7ab36009d148b93558fbc38a5f34037fb8e401a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8` - linux; amd64

```console
$ docker pull consul@sha256:2eebae1a25cfb180a454335d3574fb8d234b97300ec73a648b6380642a2b7cb0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.5 MB (46506320 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a612af4eda80843e370c1bdc92c8e10a5d7a9674e536586f7c2f09d57df9fb6b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:19:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 24 Feb 2021 21:19:43 GMT
ARG CONSUL_VERSION=1.8.8
# Wed, 24 Feb 2021 21:19:43 GMT
LABEL org.opencontainers.image.version=1.8.8
# Wed, 24 Feb 2021 21:19:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 24 Feb 2021 21:19:44 GMT
# ARGS: CONSUL_VERSION=1.8.8
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 24 Feb 2021 21:19:49 GMT
# ARGS: CONSUL_VERSION=1.8.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 24 Feb 2021 21:19:50 GMT
# ARGS: CONSUL_VERSION=1.8.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 24 Feb 2021 21:19:51 GMT
# ARGS: CONSUL_VERSION=1.8.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 21:19:51 GMT
VOLUME [/consul/data]
# Wed, 24 Feb 2021 21:19:52 GMT
EXPOSE 8300
# Wed, 24 Feb 2021 21:19:52 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 24 Feb 2021 21:19:52 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 24 Feb 2021 21:19:52 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 21:19:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 21:19:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40ee609be1391429b3766e6ac4288a5f3d309438ad51d9e9025ed047858574e2`  
		Last Modified: Wed, 24 Feb 2021 21:20:48 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b951ddc6c7a6aa3278bc0cdd01b56e438bb2a0109bfdbd75b6ebeb2acbb2b9df`  
		Last Modified: Wed, 24 Feb 2021 21:20:54 GMT  
		Size: 43.7 MB (43703595 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a042aef537b5d5dc1e80dc21a4c5afc925583db3ba63dea0bee61afd96695a9`  
		Last Modified: Wed, 24 Feb 2021 21:20:47 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:87ac6df9e8395ca5777cc0faedd032cf9abe70cc8cca5bdd89a39942decd05f7`  
		Last Modified: Wed, 24 Feb 2021 21:20:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a80219dd727c080fc4d07e0dccf78cecbaca68d08db0e62c8d7121c34e35a81`  
		Last Modified: Wed, 24 Feb 2021 21:20:47 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm variant v6

```console
$ docker pull consul@sha256:4208f9855f94c1b0bdc951de869bf47c18291283ae37d85832ed823c6b6ed974
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41745513 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f357ab8536d159a2b5c40bb122e459ee1cc3de7bf448c9b01fdd2eb629224d7e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 24 Feb 2021 20:50:34 GMT
ADD file:8bbb59eeaad0cbcf11559bc6e2b4492aadf6822d1935ed50c710f8bed858b7b5 in / 
# Wed, 24 Feb 2021 20:50:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:08:49 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 24 Feb 2021 21:09:20 GMT
ARG CONSUL_VERSION=1.8.8
# Wed, 24 Feb 2021 21:09:21 GMT
LABEL org.opencontainers.image.version=1.8.8
# Wed, 24 Feb 2021 21:09:22 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 24 Feb 2021 21:09:24 GMT
# ARGS: CONSUL_VERSION=1.8.8
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 24 Feb 2021 21:09:34 GMT
# ARGS: CONSUL_VERSION=1.8.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 24 Feb 2021 21:09:37 GMT
# ARGS: CONSUL_VERSION=1.8.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 24 Feb 2021 21:09:41 GMT
# ARGS: CONSUL_VERSION=1.8.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 21:09:43 GMT
VOLUME [/consul/data]
# Wed, 24 Feb 2021 21:09:43 GMT
EXPOSE 8300
# Wed, 24 Feb 2021 21:09:44 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 24 Feb 2021 21:09:45 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 24 Feb 2021 21:09:45 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 21:09:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 21:09:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:55242616b0494f68f44470d864da746cd2a8f8f2d1ffca698114de64032247ef`  
		Last Modified: Wed, 24 Feb 2021 20:51:17 GMT  
		Size: 2.6 MB (2604518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a624acb5782d537bec3ebbc06b492ab18264da3fceb8a58b7d6c0463255ba7c9`  
		Last Modified: Wed, 24 Feb 2021 21:10:59 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fafdd6bbe777f3ac096731af12be1cb68b67dc88bbfb9dbd91d88b25d478ac88`  
		Last Modified: Wed, 24 Feb 2021 21:11:09 GMT  
		Size: 39.1 MB (39137704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5962639564ef4d1701b799b93d89ffec0dc3775d50b3c52a1b94b3585d86afd7`  
		Last Modified: Wed, 24 Feb 2021 21:10:58 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d46797e1cb6362e800129f9f2ff33d1ef1fcb9c943aa44d8853e48110afa347b`  
		Last Modified: Wed, 24 Feb 2021 21:10:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c917ef79b148aadc1687888d14638604c9577f5939eee904c9d2076048912c23`  
		Last Modified: Wed, 24 Feb 2021 21:10:58 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:05e9edb1ab48b670f27933a2efbd0babb695a03390764ecf55a465882c427c92
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.9 MB (41926626 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:249877c49ddbdf3612e3472c152e172ee9cf24d94e3e8417f651349826f40035`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:39 GMT
ADD file:7e82858ef85f6db90c131ed835a390d736cfdbd1a0cf8bccaeed8f7e30172ddb in / 
# Wed, 24 Feb 2021 20:39:40 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:29:40 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 24 Feb 2021 21:30:11 GMT
ARG CONSUL_VERSION=1.8.8
# Wed, 24 Feb 2021 21:30:12 GMT
LABEL org.opencontainers.image.version=1.8.8
# Wed, 24 Feb 2021 21:30:13 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 24 Feb 2021 21:30:15 GMT
# ARGS: CONSUL_VERSION=1.8.8
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 24 Feb 2021 21:30:22 GMT
# ARGS: CONSUL_VERSION=1.8.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 24 Feb 2021 21:30:25 GMT
# ARGS: CONSUL_VERSION=1.8.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 24 Feb 2021 21:30:28 GMT
# ARGS: CONSUL_VERSION=1.8.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 21:30:29 GMT
VOLUME [/consul/data]
# Wed, 24 Feb 2021 21:30:29 GMT
EXPOSE 8300
# Wed, 24 Feb 2021 21:30:30 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 24 Feb 2021 21:30:31 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 24 Feb 2021 21:30:32 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 21:30:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 21:30:33 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dce8679b510e95d136241d02ababff86469dd14220812a7ce9202833c0e32f66`  
		Last Modified: Wed, 24 Feb 2021 20:40:26 GMT  
		Size: 2.7 MB (2709880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7376d370ff1a729797a96e6655c5a52c2100b17bd235a893bebe860740d4713`  
		Last Modified: Wed, 24 Feb 2021 21:31:45 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e3b6c1cb2740592e0bca0b11c83d46e94c19eee255cee7c1b6650694b19a588`  
		Last Modified: Wed, 24 Feb 2021 21:31:54 GMT  
		Size: 39.2 MB (39213451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35d6a53338189d4afbadf4f53a485dfa2c57db71af6e44c6c4f6f9c4078a6a85`  
		Last Modified: Wed, 24 Feb 2021 21:31:45 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:da378580ccd5fb002f365b7ad68ec97ab7cbd759cf8a11a5869abef05a0ec73e`  
		Last Modified: Wed, 24 Feb 2021 21:31:45 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15429189cdc8c9be8f8f0912d20bb9e78ebd804094b6e637cca0750ecc577bec`  
		Last Modified: Wed, 24 Feb 2021 21:31:45 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; 386

```console
$ docker pull consul@sha256:545df4dfc31f93f06e557a8620b5c6101bb57525719f48ca3ccc63a494100c7e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.0 MB (46005161 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:85a2629fc939833aec7de29e23d0cae93467093afc2de7af97fb9eac28597307`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 24 Feb 2021 20:38:41 GMT
ADD file:1f1a1b55522505e78fcc069edb6c793371f78991e90dcb464e4ddac7efd6588c in / 
# Wed, 24 Feb 2021 20:38:41 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:55:01 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 24 Feb 2021 20:55:18 GMT
ARG CONSUL_VERSION=1.8.8
# Wed, 24 Feb 2021 20:55:19 GMT
LABEL org.opencontainers.image.version=1.8.8
# Wed, 24 Feb 2021 20:55:19 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 24 Feb 2021 20:55:20 GMT
# ARGS: CONSUL_VERSION=1.8.8
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 24 Feb 2021 20:55:30 GMT
# ARGS: CONSUL_VERSION=1.8.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 24 Feb 2021 20:55:31 GMT
# ARGS: CONSUL_VERSION=1.8.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 24 Feb 2021 20:55:32 GMT
# ARGS: CONSUL_VERSION=1.8.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:55:32 GMT
VOLUME [/consul/data]
# Wed, 24 Feb 2021 20:55:32 GMT
EXPOSE 8300
# Wed, 24 Feb 2021 20:55:33 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 24 Feb 2021 20:55:33 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 24 Feb 2021 20:55:33 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 20:55:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 20:55:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:045e8056601208133bee5c98e76028f9b97e055c738892f8d6283205e1006173`  
		Last Modified: Wed, 24 Feb 2021 20:39:27 GMT  
		Size: 2.8 MB (2794750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:53618af4970523c2bca671a34cd38b368cf818b1400f18722b45bfd6b6df6b1c`  
		Last Modified: Wed, 24 Feb 2021 20:56:15 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5a3f61853569fc014b13fcba9e37275765b2196d3c5bdf29f995c151e53ffb46`  
		Last Modified: Wed, 24 Feb 2021 20:56:24 GMT  
		Size: 43.2 MB (43207179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dcd836d41cf73d3f346500e9acab45d986e33334fab498cf6488eaf64ed4bba6`  
		Last Modified: Wed, 24 Feb 2021 20:56:15 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10e07c782896de40fd9b34cff71aa41ff5970981581ff7391af04514011c3270`  
		Last Modified: Wed, 24 Feb 2021 20:56:15 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5200aff1394c7ee8ba0b78e139075a200b6b2c21d453864f01e9c278c68c62b5`  
		Last Modified: Wed, 24 Feb 2021 20:56:15 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8.9`

```console
$ docker pull consul@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `consul:1.9`

```console
$ docker pull consul@sha256:e9530d78c42bb2731948d2c7057d53f215e68a963b9455fb913fde99846f8c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9` - linux; amd64

```console
$ docker pull consul@sha256:adbf5269451afbfdc6fc5119fe4edf01b530f443969cb3cff0a00109613db349
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45605807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881134d490742be947022560fe1dc94f58a6d4de2cc356e00a9aac59392538f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:19:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 24 Feb 2021 21:19:29 GMT
ARG CONSUL_VERSION=1.9.3
# Wed, 24 Feb 2021 21:19:29 GMT
LABEL org.opencontainers.image.version=1.9.3
# Wed, 24 Feb 2021 21:19:30 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 24 Feb 2021 21:19:31 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 24 Feb 2021 21:19:35 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 24 Feb 2021 21:19:36 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 24 Feb 2021 21:19:37 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 21:19:38 GMT
VOLUME [/consul/data]
# Wed, 24 Feb 2021 21:19:38 GMT
EXPOSE 8300
# Wed, 24 Feb 2021 21:19:38 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 24 Feb 2021 21:19:38 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 24 Feb 2021 21:19:38 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 21:19:39 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea52006ac511368e3c6bcb4a73d30678c542c0c3fb8a37d65f827068653579f6`  
		Last Modified: Wed, 24 Feb 2021 21:20:31 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e14090bc9d8bfe39c13dfb297d4bcf1538266cec537752e4ad6efabd891756`  
		Last Modified: Wed, 24 Feb 2021 21:20:40 GMT  
		Size: 42.8 MB (42803082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592cff81a0c3344b1ac69a78209a4d49549b47f75103613029c2b371ec7db7c9`  
		Last Modified: Wed, 24 Feb 2021 21:20:30 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9aa5162537717ccc5634c8a34f89e58b1c4731856fee3c87fc09a800bd54898`  
		Last Modified: Wed, 24 Feb 2021 21:20:29 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8e3c9e516b9424db7cd5c9c8f4f6f2ceae55ed0afaad8cecd7abedc5975740`  
		Last Modified: Wed, 24 Feb 2021 21:20:29 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:e41722bc53a600ed9b6b6fcd1608e9bd20249bd40191c6af2cb508329cfdaa69
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40859913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b835ce0d86f3c852ecba7dafa68b53c6517044e969e563985bc059dca7d869`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 24 Feb 2021 20:50:34 GMT
ADD file:8bbb59eeaad0cbcf11559bc6e2b4492aadf6822d1935ed50c710f8bed858b7b5 in / 
# Wed, 24 Feb 2021 20:50:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:08:49 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 24 Feb 2021 21:08:49 GMT
ARG CONSUL_VERSION=1.9.3
# Wed, 24 Feb 2021 21:08:50 GMT
LABEL org.opencontainers.image.version=1.9.3
# Wed, 24 Feb 2021 21:08:51 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 24 Feb 2021 21:08:52 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 24 Feb 2021 21:09:03 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 24 Feb 2021 21:09:06 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 24 Feb 2021 21:09:08 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 21:09:09 GMT
VOLUME [/consul/data]
# Wed, 24 Feb 2021 21:09:09 GMT
EXPOSE 8300
# Wed, 24 Feb 2021 21:09:10 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 24 Feb 2021 21:09:11 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 24 Feb 2021 21:09:11 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 21:09:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 21:09:12 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:55242616b0494f68f44470d864da746cd2a8f8f2d1ffca698114de64032247ef`  
		Last Modified: Wed, 24 Feb 2021 20:51:17 GMT  
		Size: 2.6 MB (2604518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb44b55f96ee001a4432da8272d7ffe73f0183ffb389a82f7667d28d0f07c26`  
		Last Modified: Wed, 24 Feb 2021 21:10:39 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5cd7d068879fd65d6274f175aec93067fe49c4889288e5612c3081bdc2bc11`  
		Last Modified: Wed, 24 Feb 2021 21:10:50 GMT  
		Size: 38.3 MB (38252105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188f40afa3bfa764ad72775287e9c6d1d545dee4297004580f7ed356b81f36bc`  
		Last Modified: Wed, 24 Feb 2021 21:10:39 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7dd591ff83643e7b76fb5c0ec9663a8308008861886ab6746c8c01ffd9d8ab`  
		Last Modified: Wed, 24 Feb 2021 21:10:39 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b12c42aa58449544394a012ea612b0f79a16e875e7e9c3ea8c2d0d4a2aea8f`  
		Last Modified: Wed, 24 Feb 2021 21:10:38 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:ba026ed01032d20a1a820a2a77acaa0afecaa03ca90077a6c7458c31ec2aca30
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41083538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0119551dc9d961a19f7d069b7693f3a5e8d9d3b4839539adfa075d3928b9736`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:39 GMT
ADD file:7e82858ef85f6db90c131ed835a390d736cfdbd1a0cf8bccaeed8f7e30172ddb in / 
# Wed, 24 Feb 2021 20:39:40 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:29:40 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 24 Feb 2021 21:29:41 GMT
ARG CONSUL_VERSION=1.9.3
# Wed, 24 Feb 2021 21:29:42 GMT
LABEL org.opencontainers.image.version=1.9.3
# Wed, 24 Feb 2021 21:29:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 24 Feb 2021 21:29:45 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 24 Feb 2021 21:29:52 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 24 Feb 2021 21:29:54 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 24 Feb 2021 21:29:56 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 21:29:57 GMT
VOLUME [/consul/data]
# Wed, 24 Feb 2021 21:29:58 GMT
EXPOSE 8300
# Wed, 24 Feb 2021 21:29:58 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 24 Feb 2021 21:29:59 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 24 Feb 2021 21:30:00 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 21:30:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 21:30:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dce8679b510e95d136241d02ababff86469dd14220812a7ce9202833c0e32f66`  
		Last Modified: Wed, 24 Feb 2021 20:40:26 GMT  
		Size: 2.7 MB (2709880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2cc2046d54b68e05b97d89063b0fb734fcb614068a9696992bb1ce4c69445f9`  
		Last Modified: Wed, 24 Feb 2021 21:31:23 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7013c29a3b7b22d36bccdd822922143df6d8d08cc6fd53b047187dfa0c4cfd`  
		Last Modified: Wed, 24 Feb 2021 21:31:36 GMT  
		Size: 38.4 MB (38370368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9223d45cdfdedeb253ed549dc365f3358bc97575e31c1394898f5a278c318528`  
		Last Modified: Wed, 24 Feb 2021 21:31:24 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f13575aa7031107847957acec156e196115cbd4a6d3ec50047762b62978b31`  
		Last Modified: Wed, 24 Feb 2021 21:31:23 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0016fa33719e94e99da5b406c5aa9c07e5c5b3edbea62e5b5ac540ccceeb36d5`  
		Last Modified: Wed, 24 Feb 2021 21:31:23 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; 386

```console
$ docker pull consul@sha256:035c25bb69369d460af645c9b0c7054d1f7898b0c6846dc79c29153a76af41f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44931903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9278ff98c7391c7667b2aa6b4fa34542b6789fc023bcbfaf8c3e46a4aa60727`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 24 Feb 2021 20:38:41 GMT
ADD file:1f1a1b55522505e78fcc069edb6c793371f78991e90dcb464e4ddac7efd6588c in / 
# Wed, 24 Feb 2021 20:38:41 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:55:01 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 24 Feb 2021 20:55:02 GMT
ARG CONSUL_VERSION=1.9.3
# Wed, 24 Feb 2021 20:55:02 GMT
LABEL org.opencontainers.image.version=1.9.3
# Wed, 24 Feb 2021 20:55:02 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 24 Feb 2021 20:55:03 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 24 Feb 2021 20:55:09 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 24 Feb 2021 20:55:10 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 24 Feb 2021 20:55:11 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:55:12 GMT
VOLUME [/consul/data]
# Wed, 24 Feb 2021 20:55:12 GMT
EXPOSE 8300
# Wed, 24 Feb 2021 20:55:12 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 24 Feb 2021 20:55:12 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 24 Feb 2021 20:55:13 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 20:55:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 20:55:13 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:045e8056601208133bee5c98e76028f9b97e055c738892f8d6283205e1006173`  
		Last Modified: Wed, 24 Feb 2021 20:39:27 GMT  
		Size: 2.8 MB (2794750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb2681bebeadff1ca0914e09619d419e7d4e39d6bec343d93e66fcede66d82e`  
		Last Modified: Wed, 24 Feb 2021 20:56:02 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100266ffa9756a72fe161c8439fb8111b7db8c074946f18e76824e6cfd9a79e8`  
		Last Modified: Wed, 24 Feb 2021 20:56:10 GMT  
		Size: 42.1 MB (42133919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73ff495a1d55d7f730f76ec25ae78705097b748f948b8297a401704f8a5c5d9`  
		Last Modified: Wed, 24 Feb 2021 20:56:05 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3087a92a4fe968273b0a7c2f115e35fb4a583a69c1263ee803510c407823241`  
		Last Modified: Wed, 24 Feb 2021 20:56:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f513b227a70e0d8ddefaa0a1a53aeb0c26f4ef3e0644adeaf2156636c002b9`  
		Last Modified: Wed, 24 Feb 2021 20:56:01 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9.4`

```console
$ docker pull consul@sha256:a8409dff6597f2ef5f7ecd3c672671bb2af9a390073efd74f95c54aa41cba22a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:

## `consul:latest`

```console
$ docker pull consul@sha256:e9530d78c42bb2731948d2c7057d53f215e68a963b9455fb913fde99846f8c03
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:adbf5269451afbfdc6fc5119fe4edf01b530f443969cb3cff0a00109613db349
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45605807 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:881134d490742be947022560fe1dc94f58a6d4de2cc356e00a9aac59392538f6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 24 Feb 2021 20:20:03 GMT
ADD file:0dbb1cd66f708f54f7e6663eabf24095fcd53747bfb09912a118a77e737d9617 in / 
# Wed, 24 Feb 2021 20:20:03 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:19:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 24 Feb 2021 21:19:29 GMT
ARG CONSUL_VERSION=1.9.3
# Wed, 24 Feb 2021 21:19:29 GMT
LABEL org.opencontainers.image.version=1.9.3
# Wed, 24 Feb 2021 21:19:30 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 24 Feb 2021 21:19:31 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 24 Feb 2021 21:19:35 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 24 Feb 2021 21:19:36 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 24 Feb 2021 21:19:37 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 21:19:38 GMT
VOLUME [/consul/data]
# Wed, 24 Feb 2021 21:19:38 GMT
EXPOSE 8300
# Wed, 24 Feb 2021 21:19:38 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 24 Feb 2021 21:19:38 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 24 Feb 2021 21:19:38 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 21:19:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 21:19:39 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f84cab65f19f5d625a4b5f895cdf37ad9f21e160bf201ec59a48d95b2a430145`  
		Last Modified: Wed, 24 Feb 2021 20:20:39 GMT  
		Size: 2.8 MB (2799493 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea52006ac511368e3c6bcb4a73d30678c542c0c3fb8a37d65f827068653579f6`  
		Last Modified: Wed, 24 Feb 2021 21:20:31 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91e14090bc9d8bfe39c13dfb297d4bcf1538266cec537752e4ad6efabd891756`  
		Last Modified: Wed, 24 Feb 2021 21:20:40 GMT  
		Size: 42.8 MB (42803082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:592cff81a0c3344b1ac69a78209a4d49549b47f75103613029c2b371ec7db7c9`  
		Last Modified: Wed, 24 Feb 2021 21:20:30 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9aa5162537717ccc5634c8a34f89e58b1c4731856fee3c87fc09a800bd54898`  
		Last Modified: Wed, 24 Feb 2021 21:20:29 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2b8e3c9e516b9424db7cd5c9c8f4f6f2ceae55ed0afaad8cecd7abedc5975740`  
		Last Modified: Wed, 24 Feb 2021 21:20:29 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:e41722bc53a600ed9b6b6fcd1608e9bd20249bd40191c6af2cb508329cfdaa69
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40859913 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:40b835ce0d86f3c852ecba7dafa68b53c6517044e969e563985bc059dca7d869`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 24 Feb 2021 20:50:34 GMT
ADD file:8bbb59eeaad0cbcf11559bc6e2b4492aadf6822d1935ed50c710f8bed858b7b5 in / 
# Wed, 24 Feb 2021 20:50:35 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:08:49 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 24 Feb 2021 21:08:49 GMT
ARG CONSUL_VERSION=1.9.3
# Wed, 24 Feb 2021 21:08:50 GMT
LABEL org.opencontainers.image.version=1.9.3
# Wed, 24 Feb 2021 21:08:51 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 24 Feb 2021 21:08:52 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 24 Feb 2021 21:09:03 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 24 Feb 2021 21:09:06 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 24 Feb 2021 21:09:08 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 21:09:09 GMT
VOLUME [/consul/data]
# Wed, 24 Feb 2021 21:09:09 GMT
EXPOSE 8300
# Wed, 24 Feb 2021 21:09:10 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 24 Feb 2021 21:09:11 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 24 Feb 2021 21:09:11 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 21:09:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 21:09:12 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:55242616b0494f68f44470d864da746cd2a8f8f2d1ffca698114de64032247ef`  
		Last Modified: Wed, 24 Feb 2021 20:51:17 GMT  
		Size: 2.6 MB (2604518 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9bb44b55f96ee001a4432da8272d7ffe73f0183ffb389a82f7667d28d0f07c26`  
		Last Modified: Wed, 24 Feb 2021 21:10:39 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6a5cd7d068879fd65d6274f175aec93067fe49c4889288e5612c3081bdc2bc11`  
		Last Modified: Wed, 24 Feb 2021 21:10:50 GMT  
		Size: 38.3 MB (38252105 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:188f40afa3bfa764ad72775287e9c6d1d545dee4297004580f7ed356b81f36bc`  
		Last Modified: Wed, 24 Feb 2021 21:10:39 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c7dd591ff83643e7b76fb5c0ec9663a8308008861886ab6746c8c01ffd9d8ab`  
		Last Modified: Wed, 24 Feb 2021 21:10:39 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4b12c42aa58449544394a012ea612b0f79a16e875e7e9c3ea8c2d0d4a2aea8f`  
		Last Modified: Wed, 24 Feb 2021 21:10:38 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:ba026ed01032d20a1a820a2a77acaa0afecaa03ca90077a6c7458c31ec2aca30
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41083538 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0119551dc9d961a19f7d069b7693f3a5e8d9d3b4839539adfa075d3928b9736`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 24 Feb 2021 20:39:39 GMT
ADD file:7e82858ef85f6db90c131ed835a390d736cfdbd1a0cf8bccaeed8f7e30172ddb in / 
# Wed, 24 Feb 2021 20:39:40 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 21:29:40 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 24 Feb 2021 21:29:41 GMT
ARG CONSUL_VERSION=1.9.3
# Wed, 24 Feb 2021 21:29:42 GMT
LABEL org.opencontainers.image.version=1.9.3
# Wed, 24 Feb 2021 21:29:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 24 Feb 2021 21:29:45 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 24 Feb 2021 21:29:52 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 24 Feb 2021 21:29:54 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 24 Feb 2021 21:29:56 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 21:29:57 GMT
VOLUME [/consul/data]
# Wed, 24 Feb 2021 21:29:58 GMT
EXPOSE 8300
# Wed, 24 Feb 2021 21:29:58 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 24 Feb 2021 21:29:59 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 24 Feb 2021 21:30:00 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 21:30:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 21:30:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:dce8679b510e95d136241d02ababff86469dd14220812a7ce9202833c0e32f66`  
		Last Modified: Wed, 24 Feb 2021 20:40:26 GMT  
		Size: 2.7 MB (2709880 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2cc2046d54b68e05b97d89063b0fb734fcb614068a9696992bb1ce4c69445f9`  
		Last Modified: Wed, 24 Feb 2021 21:31:23 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d7013c29a3b7b22d36bccdd822922143df6d8d08cc6fd53b047187dfa0c4cfd`  
		Last Modified: Wed, 24 Feb 2021 21:31:36 GMT  
		Size: 38.4 MB (38370368 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9223d45cdfdedeb253ed549dc365f3358bc97575e31c1394898f5a278c318528`  
		Last Modified: Wed, 24 Feb 2021 21:31:24 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12f13575aa7031107847957acec156e196115cbd4a6d3ec50047762b62978b31`  
		Last Modified: Wed, 24 Feb 2021 21:31:23 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0016fa33719e94e99da5b406c5aa9c07e5c5b3edbea62e5b5ac540ccceeb36d5`  
		Last Modified: Wed, 24 Feb 2021 21:31:23 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:035c25bb69369d460af645c9b0c7054d1f7898b0c6846dc79c29153a76af41f9
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44931903 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9278ff98c7391c7667b2aa6b4fa34542b6789fc023bcbfaf8c3e46a4aa60727`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 24 Feb 2021 20:38:41 GMT
ADD file:1f1a1b55522505e78fcc069edb6c793371f78991e90dcb464e4ddac7efd6588c in / 
# Wed, 24 Feb 2021 20:38:41 GMT
CMD ["/bin/sh"]
# Wed, 24 Feb 2021 20:55:01 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Wed, 24 Feb 2021 20:55:02 GMT
ARG CONSUL_VERSION=1.9.3
# Wed, 24 Feb 2021 20:55:02 GMT
LABEL org.opencontainers.image.version=1.9.3
# Wed, 24 Feb 2021 20:55:02 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 24 Feb 2021 20:55:03 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 24 Feb 2021 20:55:09 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 24 Feb 2021 20:55:10 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 24 Feb 2021 20:55:11 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 24 Feb 2021 20:55:12 GMT
VOLUME [/consul/data]
# Wed, 24 Feb 2021 20:55:12 GMT
EXPOSE 8300
# Wed, 24 Feb 2021 20:55:12 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 24 Feb 2021 20:55:12 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 24 Feb 2021 20:55:13 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 24 Feb 2021 20:55:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 24 Feb 2021 20:55:13 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:045e8056601208133bee5c98e76028f9b97e055c738892f8d6283205e1006173`  
		Last Modified: Wed, 24 Feb 2021 20:39:27 GMT  
		Size: 2.8 MB (2794750 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecb2681bebeadff1ca0914e09619d419e7d4e39d6bec343d93e66fcede66d82e`  
		Last Modified: Wed, 24 Feb 2021 20:56:02 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:100266ffa9756a72fe161c8439fb8111b7db8c074946f18e76824e6cfd9a79e8`  
		Last Modified: Wed, 24 Feb 2021 20:56:10 GMT  
		Size: 42.1 MB (42133919 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c73ff495a1d55d7f730f76ec25ae78705097b748f948b8297a401704f8a5c5d9`  
		Last Modified: Wed, 24 Feb 2021 20:56:05 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3087a92a4fe968273b0a7c2f115e35fb4a583a69c1263ee803510c407823241`  
		Last Modified: Wed, 24 Feb 2021 20:56:02 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2f513b227a70e0d8ddefaa0a1a53aeb0c26f4ef3e0644adeaf2156636c002b9`  
		Last Modified: Wed, 24 Feb 2021 20:56:01 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
