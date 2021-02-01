## `consul:latest`

```console
$ docker pull consul@sha256:580216906940fcb76d5c2c5599a82a6bc83da452c6489542a18d45c68fd9aeec
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:fe7238a5f4a603f91e12159941de558006b8285236579ee43d33fde841ff6d20
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45605385 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f810e362b00c096b76f787e18ec3471fdc7340ed4d07a65e2293df3f064e5e8e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 17 Dec 2020 00:19:41 GMT
ADD file:ec475c2abb2d46435286b5ae5efacf5b50b1a9e3b6293b69db3c0172b5b9658b in / 
# Thu, 17 Dec 2020 00:19:42 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 13:01:24 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Mon, 01 Feb 2021 20:21:26 GMT
ARG CONSUL_VERSION=1.9.3
# Mon, 01 Feb 2021 20:21:26 GMT
LABEL org.opencontainers.image.version=1.9.3
# Mon, 01 Feb 2021 20:21:26 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Mon, 01 Feb 2021 20:21:27 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN addgroup consul &&     adduser -S -G consul consul
# Mon, 01 Feb 2021 20:21:33 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Mon, 01 Feb 2021 20:21:34 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Mon, 01 Feb 2021 20:21:35 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 01 Feb 2021 20:21:35 GMT
VOLUME [/consul/data]
# Mon, 01 Feb 2021 20:21:35 GMT
EXPOSE 8300
# Mon, 01 Feb 2021 20:21:35 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Mon, 01 Feb 2021 20:21:35 GMT
EXPOSE 8500 8600 8600/udp
# Mon, 01 Feb 2021 20:21:36 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 01 Feb 2021 20:21:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Feb 2021 20:21:36 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:801bfaa63ef2094d770c809815b9e2b9c1194728e5e754ef7bc764030e140cea`  
		Last Modified: Wed, 16 Dec 2020 19:34:50 GMT  
		Size: 2.8 MB (2799066 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:021e9de7890535915a3a46f25de9f0032ba6256ce8b38bd5bc4df0c82aba7d42`  
		Last Modified: Mon, 01 Feb 2021 20:21:55 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b1838740bd6bdc45be23c572b996d659b367b3f8160e93660001cf22ad310e59`  
		Last Modified: Mon, 01 Feb 2021 20:22:01 GMT  
		Size: 42.8 MB (42803079 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f34846985109154d36557a96fed6a26ecc3085273ea91880db874b0ea4735ee`  
		Last Modified: Mon, 01 Feb 2021 20:21:55 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:813272cbb3e34605019391b6c837c0f4102c4587c6d2c2c5669ebea029b5dc55`  
		Last Modified: Mon, 01 Feb 2021 20:21:55 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6188a45b98782aadbccc6832c650f49e1028a9bfd1fb97609bbcd378d6c3966`  
		Last Modified: Mon, 01 Feb 2021 20:21:55 GMT  
		Size: 1.7 KB (1710 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:2f1e52ccd2e90a37c078db47b4045c60b42786f55ee534c93d0068ffc6d7075c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.9 MB (40859579 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e44da9c49c5e185ce87f23c4235ba348d0c617f420f972b399411b944e8d82f7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 16 Dec 2020 23:49:43 GMT
ADD file:0a16715e2d0e5811c3c578945d618db0e269847a799340248f9ba8d393c9eec2 in / 
# Wed, 16 Dec 2020 23:49:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:15:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Mon, 01 Feb 2021 20:00:35 GMT
ARG CONSUL_VERSION=1.9.3
# Mon, 01 Feb 2021 20:00:36 GMT
LABEL org.opencontainers.image.version=1.9.3
# Mon, 01 Feb 2021 20:00:37 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Mon, 01 Feb 2021 20:00:39 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN addgroup consul &&     adduser -S -G consul consul
# Mon, 01 Feb 2021 20:00:48 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Mon, 01 Feb 2021 20:00:51 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Mon, 01 Feb 2021 20:00:54 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 01 Feb 2021 20:00:55 GMT
VOLUME [/consul/data]
# Mon, 01 Feb 2021 20:00:55 GMT
EXPOSE 8300
# Mon, 01 Feb 2021 20:00:56 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Mon, 01 Feb 2021 20:00:57 GMT
EXPOSE 8500 8600 8600/udp
# Mon, 01 Feb 2021 20:00:58 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 01 Feb 2021 20:00:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Feb 2021 20:00:59 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:93247449aef3c56eb4f7ab7b3fed95743c974b823def6dd86ec84008126e7903`  
		Last Modified: Wed, 16 Dec 2020 23:50:24 GMT  
		Size: 2.6 MB (2604163 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a50de3f25bd5af6d170821f4f6bb704c780c12c7975bc079aef69b20186a2eb`  
		Last Modified: Mon, 01 Feb 2021 20:01:25 GMT  
		Size: 1.3 KB (1261 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d0e8d3cac7004b75270c66b8482c6e21c7a2a27ec49dc40400bcc867a330fc8`  
		Last Modified: Mon, 01 Feb 2021 20:01:35 GMT  
		Size: 38.3 MB (38252123 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63dbc1d633d3dc8d9d0a331127458a791627c139a77de6c1284451a00ee63f46`  
		Last Modified: Mon, 01 Feb 2021 20:01:25 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6244f877acdfd5b17f8e7c703f67ee1003de254cc56508ac5f26d97a31ac89fd`  
		Last Modified: Mon, 01 Feb 2021 20:01:24 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d548b7fca730a509b8fe9af7aa1795c1579d62296d4ee60a24c646858a17f8e`  
		Last Modified: Mon, 01 Feb 2021 20:01:24 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:f1f7a9abf33306a16867c8dcdc2cd85cd0411b5d268fef3ebcc6a6b7129571db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41082727 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fa7a6ba2ec9497bcfb11e9ef83fa8d7ab902e117586432d5e1160b9b506e7dde`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 16 Dec 2020 23:40:26 GMT
ADD file:a4845c3840a3fd0e41e4635a179cce20c81afc6c02e34e3fd5bd2d535698918b in / 
# Wed, 16 Dec 2020 23:40:29 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 00:36:45 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Mon, 01 Feb 2021 20:54:14 GMT
ARG CONSUL_VERSION=1.9.3
# Mon, 01 Feb 2021 20:54:15 GMT
LABEL org.opencontainers.image.version=1.9.3
# Mon, 01 Feb 2021 20:54:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Mon, 01 Feb 2021 20:54:17 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN addgroup consul &&     adduser -S -G consul consul
# Mon, 01 Feb 2021 20:54:24 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Mon, 01 Feb 2021 20:54:26 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Mon, 01 Feb 2021 20:54:28 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 01 Feb 2021 20:54:29 GMT
VOLUME [/consul/data]
# Mon, 01 Feb 2021 20:54:29 GMT
EXPOSE 8300
# Mon, 01 Feb 2021 20:54:30 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Mon, 01 Feb 2021 20:54:31 GMT
EXPOSE 8500 8600 8600/udp
# Mon, 01 Feb 2021 20:54:31 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 01 Feb 2021 20:54:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Feb 2021 20:54:33 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:159e5727ea618dfe8b08811112e2c51f5bd2b9ae7db9eb214914a65249f70ca0`  
		Last Modified: Wed, 16 Dec 2020 23:41:08 GMT  
		Size: 2.7 MB (2709048 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f3292c5629151a0baa53317f2134cccbd2155c91650d3164e85c56b34ea0c2f1`  
		Last Modified: Mon, 01 Feb 2021 20:54:56 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ff91ef6052bcf46c3fa739adeaabb389297415c25cccf3ac384d7a0939fee95`  
		Last Modified: Mon, 01 Feb 2021 20:55:04 GMT  
		Size: 38.4 MB (38370382 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96651e02b7fc670e133a82e47e6d325064d8e73f77a427288499efa9024dfd3f`  
		Last Modified: Mon, 01 Feb 2021 20:54:56 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1165370b6109a69edf309532d1f7bb0d80881fc95b4f4dfaa57fe3e06cf98b4c`  
		Last Modified: Mon, 01 Feb 2021 20:54:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c1c4569223cda0493bef8c27a419736e23bf25e99551ec925c7131c8325dd67b`  
		Last Modified: Mon, 01 Feb 2021 20:54:56 GMT  
		Size: 1.7 KB (1712 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:429597ecea843e3edcd9a766210aab0958d6c80ebb734b5688e35ec7aaee5895
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.9 MB (44931311 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:38959c7a3021a3325bfaf5f6fc9d733718981f7c944620a903de554b32732500`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 17 Dec 2020 00:38:32 GMT
ADD file:de33fda50a142403e842620d20bc4404e66fc4ace16edc6946c4539e8a797458 in / 
# Thu, 17 Dec 2020 00:38:32 GMT
CMD ["/bin/sh"]
# Thu, 17 Dec 2020 01:24:05 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Mon, 01 Feb 2021 20:40:22 GMT
ARG CONSUL_VERSION=1.9.3
# Mon, 01 Feb 2021 20:40:22 GMT
LABEL org.opencontainers.image.version=1.9.3
# Mon, 01 Feb 2021 20:40:22 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Mon, 01 Feb 2021 20:40:24 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN addgroup consul &&     adduser -S -G consul consul
# Mon, 01 Feb 2021 20:40:30 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Mon, 01 Feb 2021 20:40:31 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Mon, 01 Feb 2021 20:40:31 GMT
# ARGS: CONSUL_VERSION=1.9.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 01 Feb 2021 20:40:32 GMT
VOLUME [/consul/data]
# Mon, 01 Feb 2021 20:40:32 GMT
EXPOSE 8300
# Mon, 01 Feb 2021 20:40:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Mon, 01 Feb 2021 20:40:32 GMT
EXPOSE 8500 8600 8600/udp
# Mon, 01 Feb 2021 20:40:33 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 01 Feb 2021 20:40:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 01 Feb 2021 20:40:33 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:455793c72b878001f0905634ed52a2524ba51796e7377bf00683a85123f7dce9`  
		Last Modified: Thu, 17 Dec 2020 00:39:18 GMT  
		Size: 2.8 MB (2794130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2b4ad37e8a4970a9617d38d3bc59137630f5b633166def72f71805c3704164`  
		Last Modified: Mon, 01 Feb 2021 20:40:56 GMT  
		Size: 1.2 KB (1234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d88674bb71671d63a5bbb90f341a431c04872cdc42392285659768fa4ca20c7f`  
		Last Modified: Mon, 01 Feb 2021 20:41:05 GMT  
		Size: 42.1 MB (42133943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57db5a2d43f9e9b65d210e2a2b692c4a8f1659a90fc8bbeddf99f9c33099f5ff`  
		Last Modified: Mon, 01 Feb 2021 20:40:57 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f0aedee93c4f9074e55cd1df18d442796a53c0cfae32540a43ad4b97caf8b51b`  
		Last Modified: Mon, 01 Feb 2021 20:40:56 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbace861b73135d261cf8050e2bbe2e16f7b91c45b9036eec3fd18475659b3c5`  
		Last Modified: Mon, 01 Feb 2021 20:40:57 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
