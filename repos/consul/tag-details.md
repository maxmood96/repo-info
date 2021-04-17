<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.10.0-beta`](#consul1100-beta)
-	[`consul:1.10.0-beta1`](#consul1100-beta1)
-	[`consul:1.7`](#consul17)
-	[`consul:1.7.14`](#consul1714)
-	[`consul:1.8`](#consul18)
-	[`consul:1.8.10`](#consul1810)
-	[`consul:1.9`](#consul19)
-	[`consul:1.9.5`](#consul195)
-	[`consul:latest`](#consullatest)

## `consul:1.10.0-beta`

```console
$ docker pull consul@sha256:d94fea53aa3d88db24ddfc20e5e100f761173d3c287947a5934f6646a2628944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10.0-beta` - linux; amd64

```console
$ docker pull consul@sha256:fb5014f4b2b6f02fe88cfde6d1607185312ac2ad709089cb46e738c86f267187
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47503502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76de456ba71225ef447948b90d316854fc896ed04f293934db36497159f7edd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:14:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:19:33 GMT
ARG CONSUL_VERSION=1.10.0-beta1
# Fri, 16 Apr 2021 21:19:33 GMT
LABEL org.opencontainers.image.version=1.10.0-beta1
# Fri, 16 Apr 2021 21:19:33 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:19:34 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:19:44 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:19:45 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:19:46 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:19:46 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:19:46 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:19:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:19:46 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:19:47 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:19:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:19:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f79b9234eaca4a038dc8e5395abf5ac8da836a87b5025daa14ad2080f042795`  
		Last Modified: Fri, 16 Apr 2021 21:20:51 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250682ddf3e296d4fe8d08fb34b6d1f085dafec387b0dd775edc517ec349ca9c`  
		Last Modified: Fri, 16 Apr 2021 21:21:02 GMT  
		Size: 44.7 MB (44699639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942a5dd6f7f6827ea88f1ead11abeb22bc800c96cc5bcc73e063f8745979ad58`  
		Last Modified: Fri, 16 Apr 2021 21:20:51 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf52fdcf176803266c5b3f0b75c7565183908ff4b30fa5b6bb515416a571ce5`  
		Last Modified: Fri, 16 Apr 2021 21:20:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bbb410103089b7272844bad1a6c95147978ec5048fa6bb469f4006422838e6`  
		Last Modified: Fri, 16 Apr 2021 21:20:51 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.0-beta` - linux; arm variant v6

```console
$ docker pull consul@sha256:e84991d048dd07b205cf82cd62af3fae7778e40b7087e406b230369811b8c334
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42591951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12715e27e813adb2250933e11a2df4d6dcf45f3593fd32ddd4ed452e1a38fd40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:48:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:49:29 GMT
ARG CONSUL_VERSION=1.10.0-beta1
# Fri, 16 Apr 2021 21:49:31 GMT
LABEL org.opencontainers.image.version=1.10.0-beta1
# Fri, 16 Apr 2021 21:49:32 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:49:40 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:55:21 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:55:24 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:55:29 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:55:29 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:55:30 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:55:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:55:33 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:55:34 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:55:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:55:36 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa2f02b2a5c8a1b5ecb1402397555144e0a45b44041f746178d06ab2d98cbd7`  
		Last Modified: Fri, 16 Apr 2021 21:58:29 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a00cec32c6b8c20f4e462c3c98299def2daa450dd4bdddccafb43a61551951`  
		Last Modified: Fri, 16 Apr 2021 21:58:45 GMT  
		Size: 40.0 MB (39983405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413a7207800f2d0e2b3497fe6d1ec386b5ba959f228282711ec84b6fd25bb26b`  
		Last Modified: Fri, 16 Apr 2021 21:58:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f403e1281979847a776a90caee981e4e90c93f49220e8fc8e1f946b13d775b00`  
		Last Modified: Fri, 16 Apr 2021 21:58:29 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc196bf633255e1801057483576330d49cae74b9f75f4600572a2cf35807a11`  
		Last Modified: Fri, 16 Apr 2021 21:58:29 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.0-beta` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:574515fb38a3e207613f8edf2b644b0a0e8c33835d3f9d4ecf7fdd7cc0561ef6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42863165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1211cf3fb4864b1909fe815c2836492a1e243a2b0e6f7dcbd0eeaae048f42bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:39:40 GMT
ARG CONSUL_VERSION=1.10.0-beta1
# Fri, 16 Apr 2021 21:39:40 GMT
LABEL org.opencontainers.image.version=1.10.0-beta1
# Fri, 16 Apr 2021 21:39:41 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:39:43 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:39:53 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:39:56 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:39:57 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:39:58 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:39:59 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:40:00 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:40:01 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:40:01 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:40:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:40:03 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3444680d687e9a3b25e1627b68c0a21aaee37a34d2e75b234bcadcda59c8f28f`  
		Last Modified: Fri, 16 Apr 2021 21:41:46 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1757438900952ebb3050dbbc0bb608ec2a0508a5942a5e69d714eab1a183dd12`  
		Last Modified: Fri, 16 Apr 2021 21:41:55 GMT  
		Size: 40.1 MB (40149179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9039abf2bd2f9adffb7c21e4c2100c3e142c06e91fe565994f8ca083d6362d`  
		Last Modified: Fri, 16 Apr 2021 21:41:46 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d7406f57576d3e04fc8e6e362fba16687bb79e93689547676654182522a09c`  
		Last Modified: Fri, 16 Apr 2021 21:41:46 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3d9b88b44b0f682a0fe185bff99d1d22e38ae3a9cca2600cd294f34f305a73`  
		Last Modified: Fri, 16 Apr 2021 21:41:46 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.0-beta` - linux; 386

```console
$ docker pull consul@sha256:6e210163e5c25d11ecc0a1d47fc61cbc23f79e08a78e367e7769fd072767511e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46874497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2f898f4cd4153cec0e41aa7643d7936dffb827dc56a0fa3f8a38676242e1a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:38:26 GMT
ARG CONSUL_VERSION=1.10.0-beta1
# Fri, 16 Apr 2021 21:38:26 GMT
LABEL org.opencontainers.image.version=1.10.0-beta1
# Fri, 16 Apr 2021 21:38:26 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:38:27 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:38:34 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:38:35 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:38:36 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:38:36 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:38:36 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:38:36 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:38:37 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:38:37 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:38:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:38:37 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76595b5704bab9706ed2a4691442047d3a4ec2cb823acfccdc92217a4b44263`  
		Last Modified: Fri, 16 Apr 2021 21:39:48 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a9da7d35ea8ddecbe4004117e25fc19041d3ede7a35a87932d71a865597ec0`  
		Last Modified: Fri, 16 Apr 2021 21:40:00 GMT  
		Size: 44.1 MB (44075409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06ffda73455c4cb399dff4b9e4a9010e210508b0003e1d08fd76f470517d1d6`  
		Last Modified: Fri, 16 Apr 2021 21:39:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed767556ce99af2b44482936d1edd7984bf1f045dae12814e5e14bef891f842e`  
		Last Modified: Fri, 16 Apr 2021 21:39:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbe87babf9d1a6debeb0af5b238df45d688ad66c0c5370666b2919ffbb4b45e`  
		Last Modified: Fri, 16 Apr 2021 21:39:48 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.10.0-beta1`

```console
$ docker pull consul@sha256:d94fea53aa3d88db24ddfc20e5e100f761173d3c287947a5934f6646a2628944
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10.0-beta1` - linux; amd64

```console
$ docker pull consul@sha256:fb5014f4b2b6f02fe88cfde6d1607185312ac2ad709089cb46e738c86f267187
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47503502 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:76de456ba71225ef447948b90d316854fc896ed04f293934db36497159f7edd9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:14:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:19:33 GMT
ARG CONSUL_VERSION=1.10.0-beta1
# Fri, 16 Apr 2021 21:19:33 GMT
LABEL org.opencontainers.image.version=1.10.0-beta1
# Fri, 16 Apr 2021 21:19:33 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:19:34 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:19:44 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:19:45 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:19:46 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:19:46 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:19:46 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:19:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:19:46 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:19:47 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:19:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:19:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f79b9234eaca4a038dc8e5395abf5ac8da836a87b5025daa14ad2080f042795`  
		Last Modified: Fri, 16 Apr 2021 21:20:51 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:250682ddf3e296d4fe8d08fb34b6d1f085dafec387b0dd775edc517ec349ca9c`  
		Last Modified: Fri, 16 Apr 2021 21:21:02 GMT  
		Size: 44.7 MB (44699639 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:942a5dd6f7f6827ea88f1ead11abeb22bc800c96cc5bcc73e063f8745979ad58`  
		Last Modified: Fri, 16 Apr 2021 21:20:51 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf52fdcf176803266c5b3f0b75c7565183908ff4b30fa5b6bb515416a571ce5`  
		Last Modified: Fri, 16 Apr 2021 21:20:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:91bbb410103089b7272844bad1a6c95147978ec5048fa6bb469f4006422838e6`  
		Last Modified: Fri, 16 Apr 2021 21:20:51 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.0-beta1` - linux; arm variant v6

```console
$ docker pull consul@sha256:e84991d048dd07b205cf82cd62af3fae7778e40b7087e406b230369811b8c334
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42591951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12715e27e813adb2250933e11a2df4d6dcf45f3593fd32ddd4ed452e1a38fd40`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:48:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:49:29 GMT
ARG CONSUL_VERSION=1.10.0-beta1
# Fri, 16 Apr 2021 21:49:31 GMT
LABEL org.opencontainers.image.version=1.10.0-beta1
# Fri, 16 Apr 2021 21:49:32 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:49:40 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:55:21 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:55:24 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:55:29 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:55:29 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:55:30 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:55:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:55:33 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:55:34 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:55:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:55:36 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3aa2f02b2a5c8a1b5ecb1402397555144e0a45b44041f746178d06ab2d98cbd7`  
		Last Modified: Fri, 16 Apr 2021 21:58:29 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a4a00cec32c6b8c20f4e462c3c98299def2daa450dd4bdddccafb43a61551951`  
		Last Modified: Fri, 16 Apr 2021 21:58:45 GMT  
		Size: 40.0 MB (39983405 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:413a7207800f2d0e2b3497fe6d1ec386b5ba959f228282711ec84b6fd25bb26b`  
		Last Modified: Fri, 16 Apr 2021 21:58:29 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f403e1281979847a776a90caee981e4e90c93f49220e8fc8e1f946b13d775b00`  
		Last Modified: Fri, 16 Apr 2021 21:58:29 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc196bf633255e1801057483576330d49cae74b9f75f4600572a2cf35807a11`  
		Last Modified: Fri, 16 Apr 2021 21:58:29 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.0-beta1` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:574515fb38a3e207613f8edf2b644b0a0e8c33835d3f9d4ecf7fdd7cc0561ef6
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42863165 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1211cf3fb4864b1909fe815c2836492a1e243a2b0e6f7dcbd0eeaae048f42bc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:39:40 GMT
ARG CONSUL_VERSION=1.10.0-beta1
# Fri, 16 Apr 2021 21:39:40 GMT
LABEL org.opencontainers.image.version=1.10.0-beta1
# Fri, 16 Apr 2021 21:39:41 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:39:43 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:39:53 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:39:56 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:39:57 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:39:58 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:39:59 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:40:00 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:40:01 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:40:01 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:40:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:40:03 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3444680d687e9a3b25e1627b68c0a21aaee37a34d2e75b234bcadcda59c8f28f`  
		Last Modified: Fri, 16 Apr 2021 21:41:46 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1757438900952ebb3050dbbc0bb608ec2a0508a5942a5e69d714eab1a183dd12`  
		Last Modified: Fri, 16 Apr 2021 21:41:55 GMT  
		Size: 40.1 MB (40149179 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c9039abf2bd2f9adffb7c21e4c2100c3e142c06e91fe565994f8ca083d6362d`  
		Last Modified: Fri, 16 Apr 2021 21:41:46 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7d7406f57576d3e04fc8e6e362fba16687bb79e93689547676654182522a09c`  
		Last Modified: Fri, 16 Apr 2021 21:41:46 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d3d9b88b44b0f682a0fe185bff99d1d22e38ae3a9cca2600cd294f34f305a73`  
		Last Modified: Fri, 16 Apr 2021 21:41:46 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.0-beta1` - linux; 386

```console
$ docker pull consul@sha256:6e210163e5c25d11ecc0a1d47fc61cbc23f79e08a78e367e7769fd072767511e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.9 MB (46874497 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8d2f898f4cd4153cec0e41aa7643d7936dffb827dc56a0fa3f8a38676242e1a6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:38:26 GMT
ARG CONSUL_VERSION=1.10.0-beta1
# Fri, 16 Apr 2021 21:38:26 GMT
LABEL org.opencontainers.image.version=1.10.0-beta1
# Fri, 16 Apr 2021 21:38:26 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:38:27 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:38:34 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:38:35 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:38:36 GMT
# ARGS: CONSUL_VERSION=1.10.0-beta1
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:38:36 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:38:36 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:38:36 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:38:37 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:38:37 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:38:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:38:37 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d76595b5704bab9706ed2a4691442047d3a4ec2cb823acfccdc92217a4b44263`  
		Last Modified: Fri, 16 Apr 2021 21:39:48 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a9a9da7d35ea8ddecbe4004117e25fc19041d3ede7a35a87932d71a865597ec0`  
		Last Modified: Fri, 16 Apr 2021 21:40:00 GMT  
		Size: 44.1 MB (44075409 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06ffda73455c4cb399dff4b9e4a9010e210508b0003e1d08fd76f470517d1d6`  
		Last Modified: Fri, 16 Apr 2021 21:39:48 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed767556ce99af2b44482936d1edd7984bf1f045dae12814e5e14bef891f842e`  
		Last Modified: Fri, 16 Apr 2021 21:39:48 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abbe87babf9d1a6debeb0af5b238df45d688ad66c0c5370666b2919ffbb4b45e`  
		Last Modified: Fri, 16 Apr 2021 21:39:48 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.7`

```console
$ docker pull consul@sha256:2d91cb12de631aeddcd35770fc9712d5b829dbd075d7e3e0d21e3bb459a2725a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.7` - linux; amd64

```console
$ docker pull consul@sha256:818d40c8362882bb646494dcf2224edcc219d23b561a6d528841920fa3b6fb8c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43631496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c3c645f3d5537617014ca0aefcf150ff1d225e7c4b5f971be7ffe1501bfb23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:14:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:20:22 GMT
ARG CONSUL_VERSION=1.7.14
# Fri, 16 Apr 2021 21:20:22 GMT
LABEL org.opencontainers.image.version=1.7.14
# Fri, 16 Apr 2021 21:20:22 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:20:23 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:20:28 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:20:29 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:20:30 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:20:30 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:20:30 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:20:30 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:20:30 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:20:31 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:20:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:20:31 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3500336ca0dccc760254ac4274787d6035ad80339bac4345fd22ebc79a955bac`  
		Last Modified: Fri, 16 Apr 2021 21:21:52 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a21bc5aae949f3aa53b146feb45d0f0000a27a4489ed523c907be4cb0ac2fc`  
		Last Modified: Fri, 16 Apr 2021 21:21:57 GMT  
		Size: 40.8 MB (40827636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1cafdad099707bebd937666b0df9097564007bcc4e65db587a6f2a59d7ca27`  
		Last Modified: Fri, 16 Apr 2021 21:21:52 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6b0acd8c713418f80e1e9bc97e0bc8ed9668a251098ca17446664b4b6926b2`  
		Last Modified: Fri, 16 Apr 2021 21:21:51 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6431c38b94db30457a6c0eeed7c83f4d78124647e20f70912c9b8b225ed93a`  
		Last Modified: Fri, 16 Apr 2021 21:21:52 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; arm variant v6

```console
$ docker pull consul@sha256:111a14468bd2592d00c26ee9e41ad5925ce2c384823b7295af29f3fff4ad10b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39265658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93422b103b3c6a6f88b99b04690ad01c85e3cf99a3b7ca3bcf56078908d64d7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:48:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:57:12 GMT
ARG CONSUL_VERSION=1.7.14
# Fri, 16 Apr 2021 21:57:14 GMT
LABEL org.opencontainers.image.version=1.7.14
# Fri, 16 Apr 2021 21:57:14 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:57:18 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:57:36 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:57:45 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:57:55 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:57:57 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:58:02 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:58:04 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:58:05 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:58:07 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:58:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:58:10 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5262634fe36fb0e798b90c10b4ef0d64415015c905ca56c9c660be3da5a93acf`  
		Last Modified: Fri, 16 Apr 2021 21:59:28 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c89140cea653353b0f0c7f58b0ee0ce8ad37dcdc275a5321994d7b6a787f2a3`  
		Last Modified: Fri, 16 Apr 2021 21:59:39 GMT  
		Size: 36.7 MB (36657112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0be8b6e0ca436b6eea91c51d6d272babc2d6f5b1bca53a94ca8d5a80cc609ac`  
		Last Modified: Fri, 16 Apr 2021 21:59:29 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b34354b4cac5f47c5f6fb3edb5f9c6aa6827227a7398fae048f0b9d9463183c`  
		Last Modified: Fri, 16 Apr 2021 21:59:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f60988c3aba4305f3a47379e4a0673726fbda45b7e4c81990ed3accc3e5db1`  
		Last Modified: Fri, 16 Apr 2021 21:59:29 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:6eaa97eed99c857441836579a11e1a361b8745cc2572c813584316f8c45ca6b4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39540160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e3236dc4250d7e1dc1b03f26aea0547323ee48144c970d15638ef31f8691da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:41:10 GMT
ARG CONSUL_VERSION=1.7.14
# Fri, 16 Apr 2021 21:41:11 GMT
LABEL org.opencontainers.image.version=1.7.14
# Fri, 16 Apr 2021 21:41:12 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:41:14 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:41:21 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:41:23 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:41:26 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:41:26 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:41:27 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:41:28 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:41:29 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:41:29 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:41:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:41:31 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b27a4ad2a0795e9f8ba72d575c043317cdfd82145646c20c317b7ad79d98d00`  
		Last Modified: Fri, 16 Apr 2021 21:42:40 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed3970d6c831b08946dc57ae23609569d7a4e5a735be5cb006766080ee868c1`  
		Last Modified: Fri, 16 Apr 2021 21:42:50 GMT  
		Size: 36.8 MB (36826170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea12b742b420a1d84d2bd3ff52b1d22fdc2863597a06bd546486785f6a42e9d`  
		Last Modified: Fri, 16 Apr 2021 21:42:40 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb646ba90de26f1acf0d1064dfa054e7fc490817c458763f1e1ed2129497b440`  
		Last Modified: Fri, 16 Apr 2021 21:42:40 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926ee3f1b9d95f22f033173994cf7acdf6cdb080dde5c4065794a70433ce7a10`  
		Last Modified: Fri, 16 Apr 2021 21:42:40 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7` - linux; 386

```console
$ docker pull consul@sha256:0980a7e84953cb23edde77f809b8465830cc68ef5764e217f862ba875e837e9e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42471268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c872fff70107db52e6e29ef5e4a84e406ef95e87fbc3b5f42d6e91fe7c4ec15e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:39:14 GMT
ARG CONSUL_VERSION=1.7.14
# Fri, 16 Apr 2021 21:39:15 GMT
LABEL org.opencontainers.image.version=1.7.14
# Fri, 16 Apr 2021 21:39:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:39:16 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:39:21 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:39:22 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:39:22 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:39:23 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:39:23 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:39:23 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:39:23 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:39:23 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:39:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:39:24 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d96f33ee206c0fa6e89a9f3e4b285df1c6822e288430f9c70ed09432729bd45`  
		Last Modified: Fri, 16 Apr 2021 21:40:59 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b51f580f8eb990d3d3ad9d3ea95690e224b801c3cf08998b1391e0d8208622`  
		Last Modified: Fri, 16 Apr 2021 21:41:04 GMT  
		Size: 39.7 MB (39672180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7fa2feebd115d949e043f8743a1c45a8d85e6628eca7bd66b950f2dde9edaf`  
		Last Modified: Fri, 16 Apr 2021 21:40:58 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7bfb4826e3717e270679ac454be787e176de4ca23a1fc6ce2bbca3f5da8aab`  
		Last Modified: Fri, 16 Apr 2021 21:41:00 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62c62762c3a1650beb7f92be116f7484caadf3925d1b670bd10923cd14760eb`  
		Last Modified: Fri, 16 Apr 2021 21:40:59 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.7.14`

```console
$ docker pull consul@sha256:2d91cb12de631aeddcd35770fc9712d5b829dbd075d7e3e0d21e3bb459a2725a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.7.14` - linux; amd64

```console
$ docker pull consul@sha256:818d40c8362882bb646494dcf2224edcc219d23b561a6d528841920fa3b6fb8c
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43631496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22c3c645f3d5537617014ca0aefcf150ff1d225e7c4b5f971be7ffe1501bfb23`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:14:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:20:22 GMT
ARG CONSUL_VERSION=1.7.14
# Fri, 16 Apr 2021 21:20:22 GMT
LABEL org.opencontainers.image.version=1.7.14
# Fri, 16 Apr 2021 21:20:22 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:20:23 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:20:28 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:20:29 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:20:30 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:20:30 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:20:30 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:20:30 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:20:30 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:20:31 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:20:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:20:31 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3500336ca0dccc760254ac4274787d6035ad80339bac4345fd22ebc79a955bac`  
		Last Modified: Fri, 16 Apr 2021 21:21:52 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0a21bc5aae949f3aa53b146feb45d0f0000a27a4489ed523c907be4cb0ac2fc`  
		Last Modified: Fri, 16 Apr 2021 21:21:57 GMT  
		Size: 40.8 MB (40827636 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e1cafdad099707bebd937666b0df9097564007bcc4e65db587a6f2a59d7ca27`  
		Last Modified: Fri, 16 Apr 2021 21:21:52 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e6b0acd8c713418f80e1e9bc97e0bc8ed9668a251098ca17446664b4b6926b2`  
		Last Modified: Fri, 16 Apr 2021 21:21:51 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a6431c38b94db30457a6c0eeed7c83f4d78124647e20f70912c9b8b225ed93a`  
		Last Modified: Fri, 16 Apr 2021 21:21:52 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7.14` - linux; arm variant v6

```console
$ docker pull consul@sha256:111a14468bd2592d00c26ee9e41ad5925ce2c384823b7295af29f3fff4ad10b2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39265658 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:93422b103b3c6a6f88b99b04690ad01c85e3cf99a3b7ca3bcf56078908d64d7f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:48:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:57:12 GMT
ARG CONSUL_VERSION=1.7.14
# Fri, 16 Apr 2021 21:57:14 GMT
LABEL org.opencontainers.image.version=1.7.14
# Fri, 16 Apr 2021 21:57:14 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:57:18 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:57:36 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:57:45 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:57:55 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:57:57 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:58:02 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:58:04 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:58:05 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:58:07 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:58:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:58:10 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5262634fe36fb0e798b90c10b4ef0d64415015c905ca56c9c660be3da5a93acf`  
		Last Modified: Fri, 16 Apr 2021 21:59:28 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c89140cea653353b0f0c7f58b0ee0ce8ad37dcdc275a5321994d7b6a787f2a3`  
		Last Modified: Fri, 16 Apr 2021 21:59:39 GMT  
		Size: 36.7 MB (36657112 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e0be8b6e0ca436b6eea91c51d6d272babc2d6f5b1bca53a94ca8d5a80cc609ac`  
		Last Modified: Fri, 16 Apr 2021 21:59:29 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b34354b4cac5f47c5f6fb3edb5f9c6aa6827227a7398fae048f0b9d9463183c`  
		Last Modified: Fri, 16 Apr 2021 21:59:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f60988c3aba4305f3a47379e4a0673726fbda45b7e4c81990ed3accc3e5db1`  
		Last Modified: Fri, 16 Apr 2021 21:59:29 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7.14` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:6eaa97eed99c857441836579a11e1a361b8745cc2572c813584316f8c45ca6b4
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39540160 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5e3236dc4250d7e1dc1b03f26aea0547323ee48144c970d15638ef31f8691da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:41:10 GMT
ARG CONSUL_VERSION=1.7.14
# Fri, 16 Apr 2021 21:41:11 GMT
LABEL org.opencontainers.image.version=1.7.14
# Fri, 16 Apr 2021 21:41:12 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:41:14 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:41:21 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:41:23 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:41:26 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:41:26 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:41:27 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:41:28 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:41:29 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:41:29 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:41:30 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:41:31 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b27a4ad2a0795e9f8ba72d575c043317cdfd82145646c20c317b7ad79d98d00`  
		Last Modified: Fri, 16 Apr 2021 21:42:40 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ed3970d6c831b08946dc57ae23609569d7a4e5a735be5cb006766080ee868c1`  
		Last Modified: Fri, 16 Apr 2021 21:42:50 GMT  
		Size: 36.8 MB (36826170 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ea12b742b420a1d84d2bd3ff52b1d22fdc2863597a06bd546486785f6a42e9d`  
		Last Modified: Fri, 16 Apr 2021 21:42:40 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb646ba90de26f1acf0d1064dfa054e7fc490817c458763f1e1ed2129497b440`  
		Last Modified: Fri, 16 Apr 2021 21:42:40 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:926ee3f1b9d95f22f033173994cf7acdf6cdb080dde5c4065794a70433ce7a10`  
		Last Modified: Fri, 16 Apr 2021 21:42:40 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.7.14` - linux; 386

```console
$ docker pull consul@sha256:0980a7e84953cb23edde77f809b8465830cc68ef5764e217f862ba875e837e9e
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42471268 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c872fff70107db52e6e29ef5e4a84e406ef95e87fbc3b5f42d6e91fe7c4ec15e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:39:14 GMT
ARG CONSUL_VERSION=1.7.14
# Fri, 16 Apr 2021 21:39:15 GMT
LABEL org.opencontainers.image.version=1.7.14
# Fri, 16 Apr 2021 21:39:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:39:16 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:39:21 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:39:22 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:39:22 GMT
# ARGS: CONSUL_VERSION=1.7.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:39:23 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:39:23 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:39:23 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:39:23 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:39:23 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:39:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:39:24 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d96f33ee206c0fa6e89a9f3e4b285df1c6822e288430f9c70ed09432729bd45`  
		Last Modified: Fri, 16 Apr 2021 21:40:59 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50b51f580f8eb990d3d3ad9d3ea95690e224b801c3cf08998b1391e0d8208622`  
		Last Modified: Fri, 16 Apr 2021 21:41:04 GMT  
		Size: 39.7 MB (39672180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb7fa2feebd115d949e043f8743a1c45a8d85e6628eca7bd66b950f2dde9edaf`  
		Last Modified: Fri, 16 Apr 2021 21:40:58 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae7bfb4826e3717e270679ac454be787e176de4ca23a1fc6ce2bbca3f5da8aab`  
		Last Modified: Fri, 16 Apr 2021 21:41:00 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c62c62762c3a1650beb7f92be116f7484caadf3925d1b670bd10923cd14760eb`  
		Last Modified: Fri, 16 Apr 2021 21:40:59 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8`

```console
$ docker pull consul@sha256:325cfbb0021d574db5f4ccd587c0e3615d654b00d6809c2dfcf889c540e8e299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8` - linux; amd64

```console
$ docker pull consul@sha256:dbbdc44d3b819cab3a9694035c647e88d9981deab979d299ff7039db91d9d75f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47026046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37f86189fb6538fb7b2b95dca88cfff199a8a760759ecef177ad7260701c085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:14:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:20:08 GMT
ARG CONSUL_VERSION=1.8.10
# Fri, 16 Apr 2021 21:20:09 GMT
LABEL org.opencontainers.image.version=1.8.10
# Fri, 16 Apr 2021 21:20:09 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:20:10 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:20:15 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:20:16 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:20:17 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:20:17 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:20:17 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:20:17 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:20:17 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:20:18 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:20:18 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31fd7759efe4085bbe76d93789a91b3632bc1789749ef935f4cc4ebb4e28792`  
		Last Modified: Fri, 16 Apr 2021 21:21:34 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d23412b1e1ea91a776f29169d5addd81f8bf7616d386d67f1f8cd04bbc82c08`  
		Last Modified: Fri, 16 Apr 2021 21:21:40 GMT  
		Size: 44.2 MB (44222187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8d8434b83e4a8aeb410623ae0ca5b64fdf0b4952df7aabe80b626ae97b0f20`  
		Last Modified: Fri, 16 Apr 2021 21:21:34 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3938e0362a67010e5ece54cbe7014ac22585d3e63f52aeac78223cef9cea99e0`  
		Last Modified: Fri, 16 Apr 2021 21:21:33 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13224b8ac7e12be0c7fcbada54765b21465da8ba01f7e08f5c2b19aa38bed0a8`  
		Last Modified: Fri, 16 Apr 2021 21:21:33 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm variant v6

```console
$ docker pull consul@sha256:ed859fb0e91040b17e5f460516cd81e5cec81dc94c11a8d63b710452e487d980
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42219308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee0646c09b62374fc0b0f9502f36470b60397ee320c55adde95296eba04e4b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:48:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:56:35 GMT
ARG CONSUL_VERSION=1.8.10
# Fri, 16 Apr 2021 21:56:35 GMT
LABEL org.opencontainers.image.version=1.8.10
# Fri, 16 Apr 2021 21:56:37 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:56:39 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:56:50 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:56:54 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:56:57 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:56:58 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:56:59 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:57:00 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:57:01 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:57:03 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:57:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:57:04 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675002a1a68b19d06e2736487641c5f05deb675397793969ee882f3305c3d141`  
		Last Modified: Fri, 16 Apr 2021 21:59:11 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15eb1b56ea1e902b6016f3cfa0e7cba3d0f050eb74a56d9c08ac9e56901ce88f`  
		Last Modified: Fri, 16 Apr 2021 21:59:21 GMT  
		Size: 39.6 MB (39610764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6131f9775fdb25d455f8eef327962645864d1a9400f9805dc0e6488893025c76`  
		Last Modified: Fri, 16 Apr 2021 21:59:11 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501d8ca0bfaa721b8ed4500dfdb9d7320dda8bddd1b95b9d5b61bd833a4924b8`  
		Last Modified: Fri, 16 Apr 2021 21:59:11 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd1840e20d77a5f7be7f65e65a37e535f458ab172608187fd7a931fa639d3ea`  
		Last Modified: Fri, 16 Apr 2021 21:59:11 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:9a975f7796f4ee589d977c3de492d5f47a4b89052ab3ac7564a989c5c0ed2007
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42450175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ca4c5bf9d7dadcf86bc99a8d6278182b8b62f48c8ef0967f58767abce0c50e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:40:43 GMT
ARG CONSUL_VERSION=1.8.10
# Fri, 16 Apr 2021 21:40:44 GMT
LABEL org.opencontainers.image.version=1.8.10
# Fri, 16 Apr 2021 21:40:44 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:40:47 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:40:53 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:40:56 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:40:58 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:40:59 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:41:00 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:41:01 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:41:02 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:41:02 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:41:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:41:04 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e84076eb9bf0d9df8a9719fcbef511c596df8b3a98029728b9a641fc1b1bb35c`  
		Last Modified: Fri, 16 Apr 2021 21:42:19 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee4a9108dc6bb133492e8977ba7a32ee6acccfee54f529c71c645f8b2c9e684`  
		Last Modified: Fri, 16 Apr 2021 21:42:33 GMT  
		Size: 39.7 MB (39736190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe14b7c04ccf9b1e88ada73bb69d8e933f1e010e9a03d1ef5e37a187619ce21`  
		Last Modified: Fri, 16 Apr 2021 21:42:19 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959d5cfd23cd2a3cf8b573953aab261e0d6d97770d5378914102525585ada93f`  
		Last Modified: Fri, 16 Apr 2021 21:42:19 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f0d925b26fd92ca7c680b60ef999a1057064f581b607538738c78fb5f8a0ea`  
		Last Modified: Fri, 16 Apr 2021 21:42:19 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; 386

```console
$ docker pull consul@sha256:e77f3069a7ef83df763cda8ee4990e01e0b8176738681b18dc7d81cb70191554
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46576440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4460157c628e78a5213d9b3311e793663110af32f33b3a5d3a9c8a382376af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:38:58 GMT
ARG CONSUL_VERSION=1.8.10
# Fri, 16 Apr 2021 21:38:58 GMT
LABEL org.opencontainers.image.version=1.8.10
# Fri, 16 Apr 2021 21:38:58 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:38:59 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:39:05 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:39:06 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:39:07 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:39:07 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:39:07 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:39:07 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:39:08 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:39:08 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:39:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:39:08 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f59dcd1edd92c70cabaf1b1d5a78dc21cdede8bd0d2c2650d0d0844ff1949da`  
		Last Modified: Fri, 16 Apr 2021 21:40:36 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f017cc0ee007613d2f19b3c5fd0666061540d1b68f4ed416627bfca7c0c1ffdc`  
		Last Modified: Fri, 16 Apr 2021 21:40:46 GMT  
		Size: 43.8 MB (43777355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204cda8e95a2f255f5e771a9b4c503535852cec35fdd7a6bbb240bd6fca8ee47`  
		Last Modified: Fri, 16 Apr 2021 21:40:36 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e9e64dc286d6b3d1015b39d24cfcdf13c7db995a70f0df97280f6d24f02f00`  
		Last Modified: Fri, 16 Apr 2021 21:40:36 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e22fdc27aa768275212c06319a6309186e1aa83ccb91d52fac2bac1a2dd93b`  
		Last Modified: Fri, 16 Apr 2021 21:40:36 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8.10`

```console
$ docker pull consul@sha256:325cfbb0021d574db5f4ccd587c0e3615d654b00d6809c2dfcf889c540e8e299
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8.10` - linux; amd64

```console
$ docker pull consul@sha256:dbbdc44d3b819cab3a9694035c647e88d9981deab979d299ff7039db91d9d75f
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (47026046 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a37f86189fb6538fb7b2b95dca88cfff199a8a760759ecef177ad7260701c085`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:14:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:20:08 GMT
ARG CONSUL_VERSION=1.8.10
# Fri, 16 Apr 2021 21:20:09 GMT
LABEL org.opencontainers.image.version=1.8.10
# Fri, 16 Apr 2021 21:20:09 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:20:10 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:20:15 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:20:16 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:20:17 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:20:17 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:20:17 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:20:17 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:20:17 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:20:18 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:20:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:20:18 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e31fd7759efe4085bbe76d93789a91b3632bc1789749ef935f4cc4ebb4e28792`  
		Last Modified: Fri, 16 Apr 2021 21:21:34 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d23412b1e1ea91a776f29169d5addd81f8bf7616d386d67f1f8cd04bbc82c08`  
		Last Modified: Fri, 16 Apr 2021 21:21:40 GMT  
		Size: 44.2 MB (44222187 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9c8d8434b83e4a8aeb410623ae0ca5b64fdf0b4952df7aabe80b626ae97b0f20`  
		Last Modified: Fri, 16 Apr 2021 21:21:34 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3938e0362a67010e5ece54cbe7014ac22585d3e63f52aeac78223cef9cea99e0`  
		Last Modified: Fri, 16 Apr 2021 21:21:33 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13224b8ac7e12be0c7fcbada54765b21465da8ba01f7e08f5c2b19aa38bed0a8`  
		Last Modified: Fri, 16 Apr 2021 21:21:33 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.10` - linux; arm variant v6

```console
$ docker pull consul@sha256:ed859fb0e91040b17e5f460516cd81e5cec81dc94c11a8d63b710452e487d980
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.2 MB (42219308 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eee0646c09b62374fc0b0f9502f36470b60397ee320c55adde95296eba04e4b6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:48:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:56:35 GMT
ARG CONSUL_VERSION=1.8.10
# Fri, 16 Apr 2021 21:56:35 GMT
LABEL org.opencontainers.image.version=1.8.10
# Fri, 16 Apr 2021 21:56:37 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:56:39 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:56:50 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:56:54 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:56:57 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:56:58 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:56:59 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:57:00 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:57:01 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:57:03 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:57:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:57:04 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675002a1a68b19d06e2736487641c5f05deb675397793969ee882f3305c3d141`  
		Last Modified: Fri, 16 Apr 2021 21:59:11 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15eb1b56ea1e902b6016f3cfa0e7cba3d0f050eb74a56d9c08ac9e56901ce88f`  
		Last Modified: Fri, 16 Apr 2021 21:59:21 GMT  
		Size: 39.6 MB (39610764 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6131f9775fdb25d455f8eef327962645864d1a9400f9805dc0e6488893025c76`  
		Last Modified: Fri, 16 Apr 2021 21:59:11 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:501d8ca0bfaa721b8ed4500dfdb9d7320dda8bddd1b95b9d5b61bd833a4924b8`  
		Last Modified: Fri, 16 Apr 2021 21:59:11 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dd1840e20d77a5f7be7f65e65a37e535f458ab172608187fd7a931fa639d3ea`  
		Last Modified: Fri, 16 Apr 2021 21:59:11 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.10` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:9a975f7796f4ee589d977c3de492d5f47a4b89052ab3ac7564a989c5c0ed2007
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42450175 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:25ca4c5bf9d7dadcf86bc99a8d6278182b8b62f48c8ef0967f58767abce0c50e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:40:43 GMT
ARG CONSUL_VERSION=1.8.10
# Fri, 16 Apr 2021 21:40:44 GMT
LABEL org.opencontainers.image.version=1.8.10
# Fri, 16 Apr 2021 21:40:44 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:40:47 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:40:53 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:40:56 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:40:58 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:40:59 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:41:00 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:41:01 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:41:02 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:41:02 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:41:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:41:04 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e84076eb9bf0d9df8a9719fcbef511c596df8b3a98029728b9a641fc1b1bb35c`  
		Last Modified: Fri, 16 Apr 2021 21:42:19 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ee4a9108dc6bb133492e8977ba7a32ee6acccfee54f529c71c645f8b2c9e684`  
		Last Modified: Fri, 16 Apr 2021 21:42:33 GMT  
		Size: 39.7 MB (39736190 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:efe14b7c04ccf9b1e88ada73bb69d8e933f1e010e9a03d1ef5e37a187619ce21`  
		Last Modified: Fri, 16 Apr 2021 21:42:19 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:959d5cfd23cd2a3cf8b573953aab261e0d6d97770d5378914102525585ada93f`  
		Last Modified: Fri, 16 Apr 2021 21:42:19 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21f0d925b26fd92ca7c680b60ef999a1057064f581b607538738c78fb5f8a0ea`  
		Last Modified: Fri, 16 Apr 2021 21:42:19 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.10` - linux; 386

```console
$ docker pull consul@sha256:e77f3069a7ef83df763cda8ee4990e01e0b8176738681b18dc7d81cb70191554
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.6 MB (46576440 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7c4460157c628e78a5213d9b3311e793663110af32f33b3a5d3a9c8a382376af`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:38:58 GMT
ARG CONSUL_VERSION=1.8.10
# Fri, 16 Apr 2021 21:38:58 GMT
LABEL org.opencontainers.image.version=1.8.10
# Fri, 16 Apr 2021 21:38:58 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:38:59 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:39:05 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:39:06 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:39:07 GMT
# ARGS: CONSUL_VERSION=1.8.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:39:07 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:39:07 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:39:07 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:39:08 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:39:08 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:39:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:39:08 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f59dcd1edd92c70cabaf1b1d5a78dc21cdede8bd0d2c2650d0d0844ff1949da`  
		Last Modified: Fri, 16 Apr 2021 21:40:36 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f017cc0ee007613d2f19b3c5fd0666061540d1b68f4ed416627bfca7c0c1ffdc`  
		Last Modified: Fri, 16 Apr 2021 21:40:46 GMT  
		Size: 43.8 MB (43777355 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:204cda8e95a2f255f5e771a9b4c503535852cec35fdd7a6bbb240bd6fca8ee47`  
		Last Modified: Fri, 16 Apr 2021 21:40:36 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88e9e64dc286d6b3d1015b39d24cfcdf13c7db995a70f0df97280f6d24f02f00`  
		Last Modified: Fri, 16 Apr 2021 21:40:36 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:18e22fdc27aa768275212c06319a6309186e1aa83ccb91d52fac2bac1a2dd93b`  
		Last Modified: Fri, 16 Apr 2021 21:40:36 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9`

```console
$ docker pull consul@sha256:0dc30c8081ea3cb4a90c908a571cb4aa469ae9e3d2b27d9fb713031127360e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9` - linux; amd64

```console
$ docker pull consul@sha256:bc63e8b5149b70532fcb74db60bfb895632bfc91adb9fdd016e9e5b6097dd0d5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46196768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53140f5924e9d0a77ab98fc52a77ca46f830556f7ca36a7f6801eef8f357507`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:14:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:19:50 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:19:50 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:19:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:19:51 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:20:00 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:20:01 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:20:02 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:20:02 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:20:03 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:20:03 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:20:03 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:20:03 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:20:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:20:04 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479a746f994b4de257e28938e880a5e4380264ebf8bb4a8acef9bde7198f8be1`  
		Last Modified: Fri, 16 Apr 2021 21:21:14 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e6c1395cf2dd1294071611a29706c7d3301d0fa60fe441caed89022e7a1913`  
		Last Modified: Fri, 16 Apr 2021 21:21:20 GMT  
		Size: 43.4 MB (43392904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ceaa195774c5627306fd4e22e4a4b6a9fd426699b0d7f247a28899a1708ac45`  
		Last Modified: Fri, 16 Apr 2021 21:21:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ff69bc8fb848d840bfe419b12f918eb83c8ddb34fd0da417935ebedb7e8faa`  
		Last Modified: Fri, 16 Apr 2021 21:21:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9b2ffb31124b25c09e5c9129fe582ba2417096da062bfd75a8e59cc3bb08f9`  
		Last Modified: Fri, 16 Apr 2021 21:21:14 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:2b85ff1cb6cc1656abec7eaebf88ccd49a8f9614fa81ab5db28e472a0f3164de
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41361659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e55eab332442fe9c3951efa2c70d596002fa3ae11da08d86f8aebcb587f9c1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:48:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:55:45 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:55:46 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:55:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:55:53 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:56:07 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:56:13 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:56:18 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:56:19 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:56:20 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:56:21 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:56:22 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:56:23 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:56:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:56:25 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84f8e6197803cc3f75f063412b83507573e2e4ff797e8bbde1e1ca9e7e52d96`  
		Last Modified: Fri, 16 Apr 2021 21:58:51 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683418c5d9facf35e881db09dc9052e3d3db78be163f0676c71da7f7266d0c18`  
		Last Modified: Fri, 16 Apr 2021 21:59:03 GMT  
		Size: 38.8 MB (38753109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c54ab05611419882090af3b6389481b7a150d5a015e06864d83001203d73bc6`  
		Last Modified: Fri, 16 Apr 2021 21:58:51 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2777b2b1864c636a0117233ed46faf5fd2a067e66c25984c40d8e91c3a37a7`  
		Last Modified: Fri, 16 Apr 2021 21:58:51 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8d64e715a1a7ff26f342c93f8a790fa6cfb3bb5224e40b0eac44a1026af0f2`  
		Last Modified: Fri, 16 Apr 2021 21:58:51 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:405aa75fa18a14c843e688bb0d83f696260f4e3a9b26007271adbf2a9cc31817
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41640623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576a424ee1563b94ed3d8c03e4beb40f394268d2378ae77c7a586f86e835cad1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:40:11 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:40:12 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:40:13 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:40:15 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:40:23 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:40:25 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:40:28 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:40:28 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:40:29 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:40:30 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:40:31 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:40:31 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:40:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:40:33 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020a69b8a99d7bbf9dce831b8be5e72108493aeaf37a20fed120c3f9076246d`  
		Last Modified: Fri, 16 Apr 2021 21:42:02 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfefe2b768463e2ac4ac80f6f6c6ed2e3c9c2493b1d4c23cf2b248ebac6cc140`  
		Last Modified: Fri, 16 Apr 2021 21:42:11 GMT  
		Size: 38.9 MB (38926635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87c24844a5c36f33c9ffb408296928d8d6632c1b275df933bf9db5968f712b0`  
		Last Modified: Fri, 16 Apr 2021 21:42:02 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b20e3c0eacfce35d670491b16ee271dd5b286fdfdd12c9e37acedcd5b9efc9b`  
		Last Modified: Fri, 16 Apr 2021 21:42:02 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1064fcab2dfa5b5e6af49d1712e9fd824f50e700cb6fa743dcb73587d1670430`  
		Last Modified: Fri, 16 Apr 2021 21:42:02 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; 386

```console
$ docker pull consul@sha256:db6b5d5bdd8788a3f9f4b73e226107344ecce1264fed4942b2de55c921946484
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45549712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eecf9b345773599c0c4b35ae10e7f3d039d09d57a7f92e7b5dbe46a5e8a5b0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:38:42 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:38:42 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:38:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:38:43 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:38:48 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:38:50 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:38:51 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:38:51 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:38:51 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:38:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:38:51 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:38:52 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:38:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:38:52 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3d83dc7299e5e15e47bb5da01c9d0bbbf3e73dd6efd0a3afc40bccf104d6de`  
		Last Modified: Fri, 16 Apr 2021 21:40:12 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ff57e2f1760ca4f15c0a6c893f224257110c429bbd84d59de210229c70a088`  
		Last Modified: Fri, 16 Apr 2021 21:40:20 GMT  
		Size: 42.8 MB (42750626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a66825478fa7c0bbf04398224269d47d90826045b3dc33f56722028424d302d`  
		Last Modified: Fri, 16 Apr 2021 21:40:12 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6184f47e1377ef660b7c944ae0d6a68bbc47f1e0ec7391f8e680e941b1ce91`  
		Last Modified: Fri, 16 Apr 2021 21:40:12 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56f9d7210c9c9ebf3e52dfb0d70a636f19e9642741c7dcfd57bfba44270d4dd`  
		Last Modified: Fri, 16 Apr 2021 21:40:12 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9.5`

```console
$ docker pull consul@sha256:0dc30c8081ea3cb4a90c908a571cb4aa469ae9e3d2b27d9fb713031127360e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9.5` - linux; amd64

```console
$ docker pull consul@sha256:bc63e8b5149b70532fcb74db60bfb895632bfc91adb9fdd016e9e5b6097dd0d5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46196768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53140f5924e9d0a77ab98fc52a77ca46f830556f7ca36a7f6801eef8f357507`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:14:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:19:50 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:19:50 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:19:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:19:51 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:20:00 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:20:01 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:20:02 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:20:02 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:20:03 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:20:03 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:20:03 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:20:03 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:20:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:20:04 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479a746f994b4de257e28938e880a5e4380264ebf8bb4a8acef9bde7198f8be1`  
		Last Modified: Fri, 16 Apr 2021 21:21:14 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e6c1395cf2dd1294071611a29706c7d3301d0fa60fe441caed89022e7a1913`  
		Last Modified: Fri, 16 Apr 2021 21:21:20 GMT  
		Size: 43.4 MB (43392904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ceaa195774c5627306fd4e22e4a4b6a9fd426699b0d7f247a28899a1708ac45`  
		Last Modified: Fri, 16 Apr 2021 21:21:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ff69bc8fb848d840bfe419b12f918eb83c8ddb34fd0da417935ebedb7e8faa`  
		Last Modified: Fri, 16 Apr 2021 21:21:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9b2ffb31124b25c09e5c9129fe582ba2417096da062bfd75a8e59cc3bb08f9`  
		Last Modified: Fri, 16 Apr 2021 21:21:14 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.5` - linux; arm variant v6

```console
$ docker pull consul@sha256:2b85ff1cb6cc1656abec7eaebf88ccd49a8f9614fa81ab5db28e472a0f3164de
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41361659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e55eab332442fe9c3951efa2c70d596002fa3ae11da08d86f8aebcb587f9c1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:48:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:55:45 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:55:46 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:55:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:55:53 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:56:07 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:56:13 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:56:18 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:56:19 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:56:20 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:56:21 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:56:22 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:56:23 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:56:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:56:25 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84f8e6197803cc3f75f063412b83507573e2e4ff797e8bbde1e1ca9e7e52d96`  
		Last Modified: Fri, 16 Apr 2021 21:58:51 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683418c5d9facf35e881db09dc9052e3d3db78be163f0676c71da7f7266d0c18`  
		Last Modified: Fri, 16 Apr 2021 21:59:03 GMT  
		Size: 38.8 MB (38753109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c54ab05611419882090af3b6389481b7a150d5a015e06864d83001203d73bc6`  
		Last Modified: Fri, 16 Apr 2021 21:58:51 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2777b2b1864c636a0117233ed46faf5fd2a067e66c25984c40d8e91c3a37a7`  
		Last Modified: Fri, 16 Apr 2021 21:58:51 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8d64e715a1a7ff26f342c93f8a790fa6cfb3bb5224e40b0eac44a1026af0f2`  
		Last Modified: Fri, 16 Apr 2021 21:58:51 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.5` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:405aa75fa18a14c843e688bb0d83f696260f4e3a9b26007271adbf2a9cc31817
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41640623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576a424ee1563b94ed3d8c03e4beb40f394268d2378ae77c7a586f86e835cad1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:40:11 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:40:12 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:40:13 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:40:15 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:40:23 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:40:25 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:40:28 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:40:28 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:40:29 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:40:30 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:40:31 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:40:31 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:40:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:40:33 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020a69b8a99d7bbf9dce831b8be5e72108493aeaf37a20fed120c3f9076246d`  
		Last Modified: Fri, 16 Apr 2021 21:42:02 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfefe2b768463e2ac4ac80f6f6c6ed2e3c9c2493b1d4c23cf2b248ebac6cc140`  
		Last Modified: Fri, 16 Apr 2021 21:42:11 GMT  
		Size: 38.9 MB (38926635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87c24844a5c36f33c9ffb408296928d8d6632c1b275df933bf9db5968f712b0`  
		Last Modified: Fri, 16 Apr 2021 21:42:02 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b20e3c0eacfce35d670491b16ee271dd5b286fdfdd12c9e37acedcd5b9efc9b`  
		Last Modified: Fri, 16 Apr 2021 21:42:02 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1064fcab2dfa5b5e6af49d1712e9fd824f50e700cb6fa743dcb73587d1670430`  
		Last Modified: Fri, 16 Apr 2021 21:42:02 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.5` - linux; 386

```console
$ docker pull consul@sha256:db6b5d5bdd8788a3f9f4b73e226107344ecce1264fed4942b2de55c921946484
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45549712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eecf9b345773599c0c4b35ae10e7f3d039d09d57a7f92e7b5dbe46a5e8a5b0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:38:42 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:38:42 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:38:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:38:43 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:38:48 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:38:50 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:38:51 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:38:51 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:38:51 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:38:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:38:51 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:38:52 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:38:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:38:52 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3d83dc7299e5e15e47bb5da01c9d0bbbf3e73dd6efd0a3afc40bccf104d6de`  
		Last Modified: Fri, 16 Apr 2021 21:40:12 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ff57e2f1760ca4f15c0a6c893f224257110c429bbd84d59de210229c70a088`  
		Last Modified: Fri, 16 Apr 2021 21:40:20 GMT  
		Size: 42.8 MB (42750626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a66825478fa7c0bbf04398224269d47d90826045b3dc33f56722028424d302d`  
		Last Modified: Fri, 16 Apr 2021 21:40:12 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6184f47e1377ef660b7c944ae0d6a68bbc47f1e0ec7391f8e680e941b1ce91`  
		Last Modified: Fri, 16 Apr 2021 21:40:12 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56f9d7210c9c9ebf3e52dfb0d70a636f19e9642741c7dcfd57bfba44270d4dd`  
		Last Modified: Fri, 16 Apr 2021 21:40:12 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:0dc30c8081ea3cb4a90c908a571cb4aa469ae9e3d2b27d9fb713031127360e42
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:bc63e8b5149b70532fcb74db60bfb895632bfc91adb9fdd016e9e5b6097dd0d5
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.2 MB (46196768 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d53140f5924e9d0a77ab98fc52a77ca46f830556f7ca36a7f6801eef8f357507`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:49 GMT
ADD file:4f526aa99067d82b341f7ca538f7826b7c23a628f1b615eea2883a2d434c1b90 in / 
# Wed, 14 Apr 2021 19:19:49 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 20:14:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:19:50 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:19:50 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:19:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:19:51 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:20:00 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:20:01 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:20:02 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:20:02 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:20:03 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:20:03 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:20:03 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:20:03 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:20:03 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:20:04 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:339de151aab4bc06eed8409daae147c408478cb538dacb90cc63f19ad4eba80b`  
		Last Modified: Wed, 14 Apr 2021 19:20:51 GMT  
		Size: 2.8 MB (2800567 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:479a746f994b4de257e28938e880a5e4380264ebf8bb4a8acef9bde7198f8be1`  
		Last Modified: Fri, 16 Apr 2021 21:21:14 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73e6c1395cf2dd1294071611a29706c7d3301d0fa60fe441caed89022e7a1913`  
		Last Modified: Fri, 16 Apr 2021 21:21:20 GMT  
		Size: 43.4 MB (43392904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5ceaa195774c5627306fd4e22e4a4b6a9fd426699b0d7f247a28899a1708ac45`  
		Last Modified: Fri, 16 Apr 2021 21:21:14 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:67ff69bc8fb848d840bfe419b12f918eb83c8ddb34fd0da417935ebedb7e8faa`  
		Last Modified: Fri, 16 Apr 2021 21:21:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9b2ffb31124b25c09e5c9129fe582ba2417096da062bfd75a8e59cc3bb08f9`  
		Last Modified: Fri, 16 Apr 2021 21:21:14 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:2b85ff1cb6cc1656abec7eaebf88ccd49a8f9614fa81ab5db28e472a0f3164de
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.4 MB (41361659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0e55eab332442fe9c3951efa2c70d596002fa3ae11da08d86f8aebcb587f9c1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:49:49 GMT
ADD file:82fa6a18d24e3f535c9061d2e111d63fe6d8a27710bb34a17b326e605ff478be in / 
# Wed, 14 Apr 2021 18:49:50 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:48:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:55:45 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:55:46 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:55:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:55:53 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:56:07 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:56:13 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:56:18 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:56:19 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:56:20 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:56:21 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:56:22 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:56:23 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:56:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:56:25 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:b452d2916bdfd021add56f1eda6bdea35400671ef07b38316ef82fce92a88fee`  
		Last Modified: Wed, 14 Apr 2021 18:50:38 GMT  
		Size: 2.6 MB (2605253 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d84f8e6197803cc3f75f063412b83507573e2e4ff797e8bbde1e1ca9e7e52d96`  
		Last Modified: Fri, 16 Apr 2021 21:58:51 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:683418c5d9facf35e881db09dc9052e3d3db78be163f0676c71da7f7266d0c18`  
		Last Modified: Fri, 16 Apr 2021 21:59:03 GMT  
		Size: 38.8 MB (38753109 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c54ab05611419882090af3b6389481b7a150d5a015e06864d83001203d73bc6`  
		Last Modified: Fri, 16 Apr 2021 21:58:51 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf2777b2b1864c636a0117233ed46faf5fd2a067e66c25984c40d8e91c3a37a7`  
		Last Modified: Fri, 16 Apr 2021 21:58:51 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d8d64e715a1a7ff26f342c93f8a790fa6cfb3bb5224e40b0eac44a1026af0f2`  
		Last Modified: Fri, 16 Apr 2021 21:58:51 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:405aa75fa18a14c843e688bb0d83f696260f4e3a9b26007271adbf2a9cc31817
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41640623 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:576a424ee1563b94ed3d8c03e4beb40f394268d2378ae77c7a586f86e835cad1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:42:54 GMT
ADD file:3db1e10ac5ebf1cb34939eff736f1384f7d3b17355758cec361489fa7a7e19ca in / 
# Wed, 14 Apr 2021 18:42:55 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 19:22:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:40:11 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:40:12 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:40:13 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:40:15 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:40:23 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:40:25 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:40:28 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:40:28 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:40:29 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:40:30 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:40:31 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:40:31 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:40:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:40:33 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d2f70382dc9a1658ea3491d7ab4439c22087e426c00e3eb7daf825b83be4ba9c`  
		Last Modified: Wed, 14 Apr 2021 18:43:55 GMT  
		Size: 2.7 MB (2710694 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8020a69b8a99d7bbf9dce831b8be5e72108493aeaf37a20fed120c3f9076246d`  
		Last Modified: Fri, 16 Apr 2021 21:42:02 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfefe2b768463e2ac4ac80f6f6c6ed2e3c9c2493b1d4c23cf2b248ebac6cc140`  
		Last Modified: Fri, 16 Apr 2021 21:42:11 GMT  
		Size: 38.9 MB (38926635 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b87c24844a5c36f33c9ffb408296928d8d6632c1b275df933bf9db5968f712b0`  
		Last Modified: Fri, 16 Apr 2021 21:42:02 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b20e3c0eacfce35d670491b16ee271dd5b286fdfdd12c9e37acedcd5b9efc9b`  
		Last Modified: Fri, 16 Apr 2021 21:42:02 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1064fcab2dfa5b5e6af49d1712e9fd824f50e700cb6fa743dcb73587d1670430`  
		Last Modified: Fri, 16 Apr 2021 21:42:02 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:db6b5d5bdd8788a3f9f4b73e226107344ecce1264fed4942b2de55c921946484
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.5 MB (45549712 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1eecf9b345773599c0c4b35ae10e7f3d039d09d57a7f92e7b5dbe46a5e8a5b0b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:36 GMT
ADD file:0a694887033953f24197dedcb1098d28a4b6e539b29386f53d82262107e208fb in / 
# Wed, 14 Apr 2021 18:38:36 GMT
CMD ["/bin/sh"]
# Wed, 14 Apr 2021 18:55:36 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 16 Apr 2021 21:38:42 GMT
ARG CONSUL_VERSION=1.9.5
# Fri, 16 Apr 2021 21:38:42 GMT
LABEL org.opencontainers.image.version=1.9.5
# Fri, 16 Apr 2021 21:38:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 16 Apr 2021 21:38:43 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 16 Apr 2021 21:38:48 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver pool.sks-keyservers.net --recv-keys 91A6E7F85D05C65630BEF18951852D87348FFC4C &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /bin consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 16 Apr 2021 21:38:50 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 16 Apr 2021 21:38:51 GMT
# ARGS: CONSUL_VERSION=1.9.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 16 Apr 2021 21:38:51 GMT
VOLUME [/consul/data]
# Fri, 16 Apr 2021 21:38:51 GMT
EXPOSE 8300
# Fri, 16 Apr 2021 21:38:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 16 Apr 2021 21:38:51 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 16 Apr 2021 21:38:52 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 16 Apr 2021 21:38:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 16 Apr 2021 21:38:52 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:7aa04a8f7710c18952348aa54b4346438ad013c87b6f7d476eb21ad756359bc3`  
		Last Modified: Wed, 14 Apr 2021 18:39:43 GMT  
		Size: 2.8 MB (2795795 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e3d83dc7299e5e15e47bb5da01c9d0bbbf3e73dd6efd0a3afc40bccf104d6de`  
		Last Modified: Fri, 16 Apr 2021 21:40:12 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:24ff57e2f1760ca4f15c0a6c893f224257110c429bbd84d59de210229c70a088`  
		Last Modified: Fri, 16 Apr 2021 21:40:20 GMT  
		Size: 42.8 MB (42750626 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a66825478fa7c0bbf04398224269d47d90826045b3dc33f56722028424d302d`  
		Last Modified: Fri, 16 Apr 2021 21:40:12 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6184f47e1377ef660b7c944ae0d6a68bbc47f1e0ec7391f8e680e941b1ce91`  
		Last Modified: Fri, 16 Apr 2021 21:40:12 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e56f9d7210c9c9ebf3e52dfb0d70a636f19e9642741c7dcfd57bfba44270d4dd`  
		Last Modified: Fri, 16 Apr 2021 21:40:12 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
