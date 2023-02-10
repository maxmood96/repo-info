<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.12`](#consul112)
-	[`consul:1.12.9`](#consul1129)
-	[`consul:1.13`](#consul113)
-	[`consul:1.13.6`](#consul1136)
-	[`consul:1.14`](#consul114)
-	[`consul:1.14.4`](#consul1144)
-	[`consul:latest`](#consullatest)

## `consul:1.12`

```console
$ docker pull consul@sha256:50d2a229c077c18f153b910fec4b9ee1990f842f043f94785847ee7e5393f0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.12` - linux; amd64

```console
$ docker pull consul@sha256:d6eeca317fec3efce05e1c611590215597d77747642d172ec5471b7e6b197a22
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49886988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af2d11d4809762265b544c1463a3c500097cc80a7ca82b72205ced31767cbae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:22:37 GMT
ARG CONSUL_VERSION=1.12.9
# Fri, 27 Jan 2023 23:22:37 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:22:37 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:22:37 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:22:43 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:22:44 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:22:44 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:22:44 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:22:45 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:22:45 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:22:45 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:22:45 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:22:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:22:45 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf9cf862ebaa129b9ef5e81097caa57180847fd32780c4e48323a90f3394021`  
		Last Modified: Fri, 27 Jan 2023 23:23:32 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d310b534574f8aa4a7ce8276ca9541f56851bf0cfa812be074285a73e50ffd44`  
		Last Modified: Fri, 27 Jan 2023 23:23:38 GMT  
		Size: 47.1 MB (47060094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8048a287deb35f6c0458c2255ef846a380f9eb4aa9226206e311544360023f44`  
		Last Modified: Fri, 27 Jan 2023 23:23:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a19cd6278f8bd233d67f7bec954409aa7938522d10de880bc00ee0f5279122`  
		Last Modified: Fri, 27 Jan 2023 23:23:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9e0d34525d8ba2292749e3e794c91fd345426cee7062354d29e77ff0dd27c6`  
		Last Modified: Fri, 27 Jan 2023 23:23:32 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12` - linux; arm variant v6

```console
$ docker pull consul@sha256:718d2d1761a080b4178498b0af1877a2f74913fe08a6b1b47924f79fc8fd699a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47663406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e6d54429057d702d13cbface93bbc6c15c80745642bda14a42872f0e5aba69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:37 GMT
ADD file:141468a99f598ddb90dbb73978d10c0f00d01ece185e157ac33a0a1414d45944 in / 
# Fri, 10 Feb 2023 20:49:37 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:30:58 GMT
ARG CONSUL_VERSION=1.12.9
# Fri, 10 Feb 2023 21:30:58 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 10 Feb 2023 21:30:58 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 10 Feb 2023 21:30:59 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 10 Feb 2023 21:31:06 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 10 Feb 2023 21:31:06 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 10 Feb 2023 21:31:07 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Feb 2023 21:31:07 GMT
VOLUME [/consul/data]
# Fri, 10 Feb 2023 21:31:07 GMT
EXPOSE 8300
# Fri, 10 Feb 2023 21:31:07 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 10 Feb 2023 21:31:07 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 10 Feb 2023 21:31:07 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Feb 2023 21:31:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 21:31:08 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ed6cbaa656dcebfe8d252792a339ccf10dddd695875f07c9636d59a5baf85f3f`  
		Last Modified: Fri, 10 Feb 2023 20:50:51 GMT  
		Size: 2.6 MB (2633649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6671f72fb5d91a5075ba7ac0e22abad8f0f99f78db8a80b8cf7ca3b0d01781`  
		Last Modified: Fri, 10 Feb 2023 21:32:13 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527085c25c4d5d4b37707661a7c8e9cdea50726fa496248a6af79d5d0c059376`  
		Last Modified: Fri, 10 Feb 2023 21:32:20 GMT  
		Size: 45.0 MB (45026438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e38f919acc4a88160a4c58f54cd481c56df736a277b7602a82b859487e7d4a0`  
		Last Modified: Fri, 10 Feb 2023 21:32:13 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901289275813ae3d3bdf12f81db25ef5aeb9e55f2e1ee4a97f7a4862ce7036f2`  
		Last Modified: Fri, 10 Feb 2023 21:32:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdcad7d307510279e64781186ebec2d538236488431b9ed963d31ae499b71688`  
		Last Modified: Fri, 10 Feb 2023 21:32:13 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:e12aec828ab7bc6b370462ef1a7af2a9906d9f4bfedb3aca852a4ff7910482ee
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47446749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85cc5f54cccbfa65c33688860a1c029aa6dd9f878b85471b970d79934ce601f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:16 GMT
ADD file:a73970ac03f28a1d3b9aaee19e859d958867b42fb91f29efb1259fbddc66ffb1 in / 
# Fri, 10 Feb 2023 21:24:16 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:01:49 GMT
ARG CONSUL_VERSION=1.12.9
# Fri, 10 Feb 2023 22:01:49 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 10 Feb 2023 22:01:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 10 Feb 2023 22:01:50 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 10 Feb 2023 22:01:56 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 10 Feb 2023 22:01:57 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 10 Feb 2023 22:01:57 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:01:57 GMT
VOLUME [/consul/data]
# Fri, 10 Feb 2023 22:01:57 GMT
EXPOSE 8300
# Fri, 10 Feb 2023 22:01:57 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 10 Feb 2023 22:01:58 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 10 Feb 2023 22:01:58 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:01:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:01:58 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:404f35918b797abb27547df3b530ec55a77c499c4dce88f3b90867115087f9e7`  
		Last Modified: Fri, 10 Feb 2023 21:25:01 GMT  
		Size: 2.7 MB (2721556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6227b2125cc3863b0dea841bb674758d3a0d9b17f98e4af88fa50e85e2473b`  
		Last Modified: Fri, 10 Feb 2023 22:02:41 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bb0f695f1413b22af04e6c958602b467c764b1f61f26d1622bb43194e92029`  
		Last Modified: Fri, 10 Feb 2023 22:02:46 GMT  
		Size: 44.7 MB (44721814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2eb42ffd8b07e52a11ce454cb1725bfc89c6a8d1f4cd5d67fdbbb21a7b024c`  
		Last Modified: Fri, 10 Feb 2023 22:02:41 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8a093aea0c739defbd05f7e978365e8462194cf5057bd611e5fc6cf960dec9`  
		Last Modified: Fri, 10 Feb 2023 22:02:41 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f5c12f4d94ed2a7bf3eda65c3e72206285a02070bbd6b1bcf9f3ae09670455`  
		Last Modified: Fri, 10 Feb 2023 22:02:41 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12` - linux; 386

```console
$ docker pull consul@sha256:1f438086e3dd1d562bb2193137f0807b39876c1de5b6c6c586fe01f586dcdbb1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48895871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f70fc0fdb0617e9f7d28c627d7b7fc853abc189a14898badae112205c5378b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:34 GMT
ADD file:35855658886412913d05c0f9e29bf8f650c0d37e20100a9de118b468f86f7f30 in / 
# Fri, 10 Feb 2023 21:24:34 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:03:47 GMT
ARG CONSUL_VERSION=1.12.9
# Fri, 10 Feb 2023 22:03:48 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 10 Feb 2023 22:03:49 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 10 Feb 2023 22:03:50 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 10 Feb 2023 22:03:57 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 10 Feb 2023 22:03:57 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 10 Feb 2023 22:03:58 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:59 GMT
VOLUME [/consul/data]
# Fri, 10 Feb 2023 22:04:00 GMT
EXPOSE 8300
# Fri, 10 Feb 2023 22:04:01 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 10 Feb 2023 22:04:02 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 10 Feb 2023 22:04:04 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:04:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:13a1d7e543968b1c2bd92ca5f2fb2e964b31713fc7707305c1cdfb935ca3e631`  
		Last Modified: Fri, 10 Feb 2023 21:25:40 GMT  
		Size: 2.8 MB (2832331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb63960e3bf0f6870f9fe02be59be54f70c980f94b02a49a1b1290c4ca893aa2`  
		Last Modified: Fri, 10 Feb 2023 22:05:03 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988eb664dd1d3af0d7f22b9dc7cddb66008da499ea48a816c3f36d10ff0714f0`  
		Last Modified: Fri, 10 Feb 2023 22:05:08 GMT  
		Size: 46.1 MB (46060219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94dc43c37cdf2b1f38cc1a3b73236e3c37bf43d8721c6dc255c6e9bbb5f5cfdd`  
		Last Modified: Fri, 10 Feb 2023 22:05:03 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0d3b029148595b1e56d1e92135ac934a35ebd9f4f5c976c02249b12d9e3596`  
		Last Modified: Fri, 10 Feb 2023 22:05:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8a6df7ec2cd2ff3335b8aac44c372de5c8b6369f19893154464ac6fe093569`  
		Last Modified: Fri, 10 Feb 2023 22:05:03 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.12.9`

```console
$ docker pull consul@sha256:50d2a229c077c18f153b910fec4b9ee1990f842f043f94785847ee7e5393f0b8
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.12.9` - linux; amd64

```console
$ docker pull consul@sha256:d6eeca317fec3efce05e1c611590215597d77747642d172ec5471b7e6b197a22
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49886988 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7af2d11d4809762265b544c1463a3c500097cc80a7ca82b72205ced31767cbae`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:22:37 GMT
ARG CONSUL_VERSION=1.12.9
# Fri, 27 Jan 2023 23:22:37 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:22:37 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:22:37 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:22:43 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:22:44 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:22:44 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:22:44 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:22:45 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:22:45 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:22:45 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:22:45 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:22:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:22:45 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cbf9cf862ebaa129b9ef5e81097caa57180847fd32780c4e48323a90f3394021`  
		Last Modified: Fri, 27 Jan 2023 23:23:32 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d310b534574f8aa4a7ce8276ca9541f56851bf0cfa812be074285a73e50ffd44`  
		Last Modified: Fri, 27 Jan 2023 23:23:38 GMT  
		Size: 47.1 MB (47060094 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8048a287deb35f6c0458c2255ef846a380f9eb4aa9226206e311544360023f44`  
		Last Modified: Fri, 27 Jan 2023 23:23:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f4a19cd6278f8bd233d67f7bec954409aa7938522d10de880bc00ee0f5279122`  
		Last Modified: Fri, 27 Jan 2023 23:23:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d9e0d34525d8ba2292749e3e794c91fd345426cee7062354d29e77ff0dd27c6`  
		Last Modified: Fri, 27 Jan 2023 23:23:32 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:718d2d1761a080b4178498b0af1877a2f74913fe08a6b1b47924f79fc8fd699a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47663406 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:15e6d54429057d702d13cbface93bbc6c15c80745642bda14a42872f0e5aba69`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:37 GMT
ADD file:141468a99f598ddb90dbb73978d10c0f00d01ece185e157ac33a0a1414d45944 in / 
# Fri, 10 Feb 2023 20:49:37 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:30:58 GMT
ARG CONSUL_VERSION=1.12.9
# Fri, 10 Feb 2023 21:30:58 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 10 Feb 2023 21:30:58 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 10 Feb 2023 21:30:59 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 10 Feb 2023 21:31:06 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 10 Feb 2023 21:31:06 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 10 Feb 2023 21:31:07 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Feb 2023 21:31:07 GMT
VOLUME [/consul/data]
# Fri, 10 Feb 2023 21:31:07 GMT
EXPOSE 8300
# Fri, 10 Feb 2023 21:31:07 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 10 Feb 2023 21:31:07 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 10 Feb 2023 21:31:07 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Feb 2023 21:31:08 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 21:31:08 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ed6cbaa656dcebfe8d252792a339ccf10dddd695875f07c9636d59a5baf85f3f`  
		Last Modified: Fri, 10 Feb 2023 20:50:51 GMT  
		Size: 2.6 MB (2633649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe6671f72fb5d91a5075ba7ac0e22abad8f0f99f78db8a80b8cf7ca3b0d01781`  
		Last Modified: Fri, 10 Feb 2023 21:32:13 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:527085c25c4d5d4b37707661a7c8e9cdea50726fa496248a6af79d5d0c059376`  
		Last Modified: Fri, 10 Feb 2023 21:32:20 GMT  
		Size: 45.0 MB (45026438 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e38f919acc4a88160a4c58f54cd481c56df736a277b7602a82b859487e7d4a0`  
		Last Modified: Fri, 10 Feb 2023 21:32:13 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:901289275813ae3d3bdf12f81db25ef5aeb9e55f2e1ee4a97f7a4862ce7036f2`  
		Last Modified: Fri, 10 Feb 2023 21:32:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdcad7d307510279e64781186ebec2d538236488431b9ed963d31ae499b71688`  
		Last Modified: Fri, 10 Feb 2023 21:32:13 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:e12aec828ab7bc6b370462ef1a7af2a9906d9f4bfedb3aca852a4ff7910482ee
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47446749 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f85cc5f54cccbfa65c33688860a1c029aa6dd9f878b85471b970d79934ce601f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:16 GMT
ADD file:a73970ac03f28a1d3b9aaee19e859d958867b42fb91f29efb1259fbddc66ffb1 in / 
# Fri, 10 Feb 2023 21:24:16 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:01:49 GMT
ARG CONSUL_VERSION=1.12.9
# Fri, 10 Feb 2023 22:01:49 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 10 Feb 2023 22:01:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 10 Feb 2023 22:01:50 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 10 Feb 2023 22:01:56 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 10 Feb 2023 22:01:57 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 10 Feb 2023 22:01:57 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:01:57 GMT
VOLUME [/consul/data]
# Fri, 10 Feb 2023 22:01:57 GMT
EXPOSE 8300
# Fri, 10 Feb 2023 22:01:57 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 10 Feb 2023 22:01:58 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 10 Feb 2023 22:01:58 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:01:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:01:58 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:404f35918b797abb27547df3b530ec55a77c499c4dce88f3b90867115087f9e7`  
		Last Modified: Fri, 10 Feb 2023 21:25:01 GMT  
		Size: 2.7 MB (2721556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ac6227b2125cc3863b0dea841bb674758d3a0d9b17f98e4af88fa50e85e2473b`  
		Last Modified: Fri, 10 Feb 2023 22:02:41 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80bb0f695f1413b22af04e6c958602b467c764b1f61f26d1622bb43194e92029`  
		Last Modified: Fri, 10 Feb 2023 22:02:46 GMT  
		Size: 44.7 MB (44721814 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e2eb42ffd8b07e52a11ce454cb1725bfc89c6a8d1f4cd5d67fdbbb21a7b024c`  
		Last Modified: Fri, 10 Feb 2023 22:02:41 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d8a093aea0c739defbd05f7e978365e8462194cf5057bd611e5fc6cf960dec9`  
		Last Modified: Fri, 10 Feb 2023 22:02:41 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0f5c12f4d94ed2a7bf3eda65c3e72206285a02070bbd6b1bcf9f3ae09670455`  
		Last Modified: Fri, 10 Feb 2023 22:02:41 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12.9` - linux; 386

```console
$ docker pull consul@sha256:1f438086e3dd1d562bb2193137f0807b39876c1de5b6c6c586fe01f586dcdbb1
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48895871 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:56f70fc0fdb0617e9f7d28c627d7b7fc853abc189a14898badae112205c5378b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:34 GMT
ADD file:35855658886412913d05c0f9e29bf8f650c0d37e20100a9de118b468f86f7f30 in / 
# Fri, 10 Feb 2023 21:24:34 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:03:47 GMT
ARG CONSUL_VERSION=1.12.9
# Fri, 10 Feb 2023 22:03:48 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 10 Feb 2023 22:03:49 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 10 Feb 2023 22:03:50 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 10 Feb 2023 22:03:57 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 10 Feb 2023 22:03:57 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 10 Feb 2023 22:03:58 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:59 GMT
VOLUME [/consul/data]
# Fri, 10 Feb 2023 22:04:00 GMT
EXPOSE 8300
# Fri, 10 Feb 2023 22:04:01 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 10 Feb 2023 22:04:02 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 10 Feb 2023 22:04:04 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:04:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:13a1d7e543968b1c2bd92ca5f2fb2e964b31713fc7707305c1cdfb935ca3e631`  
		Last Modified: Fri, 10 Feb 2023 21:25:40 GMT  
		Size: 2.8 MB (2832331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb63960e3bf0f6870f9fe02be59be54f70c980f94b02a49a1b1290c4ca893aa2`  
		Last Modified: Fri, 10 Feb 2023 22:05:03 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:988eb664dd1d3af0d7f22b9dc7cddb66008da499ea48a816c3f36d10ff0714f0`  
		Last Modified: Fri, 10 Feb 2023 22:05:08 GMT  
		Size: 46.1 MB (46060219 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94dc43c37cdf2b1f38cc1a3b73236e3c37bf43d8721c6dc255c6e9bbb5f5cfdd`  
		Last Modified: Fri, 10 Feb 2023 22:05:03 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e0d3b029148595b1e56d1e92135ac934a35ebd9f4f5c976c02249b12d9e3596`  
		Last Modified: Fri, 10 Feb 2023 22:05:03 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea8a6df7ec2cd2ff3335b8aac44c372de5c8b6369f19893154464ac6fe093569`  
		Last Modified: Fri, 10 Feb 2023 22:05:03 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.13`

```console
$ docker pull consul@sha256:fd8ca56fc8bb4b307c6c56bc1558325ac6973f333da20f119aef87fd55dd64bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.13` - linux; amd64

```console
$ docker pull consul@sha256:bb5d06c0608ff7738fbfe9dd2dfe1ff2e47584df4d30b643c86b5dd52f1225a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52259668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c255782b910a08a35c05aa7037d6a589941c810e14b3aae84fc6df7f9c2bc3c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:22:25 GMT
ARG CONSUL_VERSION=1.13.6
# Fri, 27 Jan 2023 23:22:25 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.6 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:22:25 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:22:26 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:22:32 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:22:33 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:22:34 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:22:34 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:22:34 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:22:34 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:22:34 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:22:34 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:22:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:22:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d5b7d642aeea4f3c571ff84c1718b78787eb6f9b65a4c1da0d6939039407f7`  
		Last Modified: Fri, 27 Jan 2023 23:23:17 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223ca554c4c10498a2aa07b7fd2a2b4b175ff6ef5e1513822768a6da61e6b609`  
		Last Modified: Fri, 27 Jan 2023 23:23:24 GMT  
		Size: 49.4 MB (49432771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098020b32602ed9fb3c916dac93aa71d2dc723ec3a5bdfcbdced3a63528d3a39`  
		Last Modified: Fri, 27 Jan 2023 23:23:18 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13024f719284913d712c9bd22fa0f30f6c2d659f26cc0fc277e86a51e3270a67`  
		Last Modified: Fri, 27 Jan 2023 23:23:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcfab706cab18abfef47070bdc9154a099c77b6397e150aa83163778c3240947`  
		Last Modified: Fri, 27 Jan 2023 23:23:17 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13` - linux; arm variant v6

```console
$ docker pull consul@sha256:ab4a8762e7b0db96fad0335d4511b16660857e480955dfbd0ea0a88e1f04809a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49992760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bde051138ee6429cd35893afd82014027c2b07267a21b08c7c3c790f0bba8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:37 GMT
ADD file:141468a99f598ddb90dbb73978d10c0f00d01ece185e157ac33a0a1414d45944 in / 
# Fri, 10 Feb 2023 20:49:37 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:30:43 GMT
ARG CONSUL_VERSION=1.13.6
# Fri, 10 Feb 2023 21:30:43 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.6 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 10 Feb 2023 21:30:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 10 Feb 2023 21:30:44 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 10 Feb 2023 21:30:51 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 10 Feb 2023 21:30:52 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 10 Feb 2023 21:30:53 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Feb 2023 21:30:53 GMT
VOLUME [/consul/data]
# Fri, 10 Feb 2023 21:30:53 GMT
EXPOSE 8300
# Fri, 10 Feb 2023 21:30:53 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 10 Feb 2023 21:30:53 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 10 Feb 2023 21:30:53 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Feb 2023 21:30:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 21:30:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ed6cbaa656dcebfe8d252792a339ccf10dddd695875f07c9636d59a5baf85f3f`  
		Last Modified: Fri, 10 Feb 2023 20:50:51 GMT  
		Size: 2.6 MB (2633649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a203144cd99d27ad8026f35ce058776d4ecfdf97a6e631470755b3e0ab72c09`  
		Last Modified: Fri, 10 Feb 2023 21:31:55 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd0f1f22d72191452316da6668b0678108c06ff40482cf58207f45a7cdd59d7`  
		Last Modified: Fri, 10 Feb 2023 21:32:02 GMT  
		Size: 47.4 MB (47355793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6990c0599a8e1441e534bf4fe3d414bd2a5ec6d62dd3989a35873c862120bdb9`  
		Last Modified: Fri, 10 Feb 2023 21:31:55 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17085c9fbbcc776b0c21a61afc5ccf19332369d6bb37b6fe802384864ee10000`  
		Last Modified: Fri, 10 Feb 2023 21:31:55 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40167d9375b0fe1116a601bb0c337b1f96dcbfdf15ec4f884a0191f645bcfbd5`  
		Last Modified: Fri, 10 Feb 2023 21:31:55 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:cc34a54ce28264593ccfa395890a6687d22a7ba363a0a731248b7e1ce8da455f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49477028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4525bb7e0c28b613b571a39d5234a929f369694b167ba25560d386a3c5309d61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:16 GMT
ADD file:a73970ac03f28a1d3b9aaee19e859d958867b42fb91f29efb1259fbddc66ffb1 in / 
# Fri, 10 Feb 2023 21:24:16 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:01:38 GMT
ARG CONSUL_VERSION=1.13.6
# Fri, 10 Feb 2023 22:01:38 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.6 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 10 Feb 2023 22:01:38 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 10 Feb 2023 22:01:38 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 10 Feb 2023 22:01:44 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 10 Feb 2023 22:01:45 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 10 Feb 2023 22:01:46 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:01:46 GMT
VOLUME [/consul/data]
# Fri, 10 Feb 2023 22:01:46 GMT
EXPOSE 8300
# Fri, 10 Feb 2023 22:01:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 10 Feb 2023 22:01:46 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 10 Feb 2023 22:01:46 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:01:46 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:404f35918b797abb27547df3b530ec55a77c499c4dce88f3b90867115087f9e7`  
		Last Modified: Fri, 10 Feb 2023 21:25:01 GMT  
		Size: 2.7 MB (2721556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478927a30de417c03bdd408b7ca5da00b21dc15193298aca9c443aecaaf793d9`  
		Last Modified: Fri, 10 Feb 2023 22:02:29 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01361edbe24ab319960c2afe4008ab6b2be34b7501a415ef27acc53310e7dff4`  
		Last Modified: Fri, 10 Feb 2023 22:02:33 GMT  
		Size: 46.8 MB (46752091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4bb18b1fc6d3283090e0200dd958c01dc19086beb605a3c93ba9b80b6634cf`  
		Last Modified: Fri, 10 Feb 2023 22:02:28 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbcb79adf5399e3b4d77c2afa78efdef76825f6253e474648c77199b77a90ac`  
		Last Modified: Fri, 10 Feb 2023 22:02:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd5fa1afae393b3e16ae75e072f091a42f8e532a2f21db71406ef9cb53ca702`  
		Last Modified: Fri, 10 Feb 2023 22:02:28 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13` - linux; 386

```console
$ docker pull consul@sha256:a5646227868691c8ceb6113fd990abf9815dc8bf655315afae5cd2d22dd994c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51103557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd9c553bc28ec0551a625418290acaa17f9f2470a95df906a79f238d9afd7f9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:34 GMT
ADD file:35855658886412913d05c0f9e29bf8f650c0d37e20100a9de118b468f86f7f30 in / 
# Fri, 10 Feb 2023 21:24:34 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:03:25 GMT
ARG CONSUL_VERSION=1.13.6
# Fri, 10 Feb 2023 22:03:25 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.6 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 10 Feb 2023 22:03:26 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 10 Feb 2023 22:03:27 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 10 Feb 2023 22:03:33 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 10 Feb 2023 22:03:34 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 10 Feb 2023 22:03:35 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:36 GMT
VOLUME [/consul/data]
# Fri, 10 Feb 2023 22:03:37 GMT
EXPOSE 8300
# Fri, 10 Feb 2023 22:03:38 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 10 Feb 2023 22:03:39 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 10 Feb 2023 22:03:41 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:03:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:13a1d7e543968b1c2bd92ca5f2fb2e964b31713fc7707305c1cdfb935ca3e631`  
		Last Modified: Fri, 10 Feb 2023 21:25:40 GMT  
		Size: 2.8 MB (2832331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ef7336dc444a6681ae6f81ee98295bcc132fb3a90957a79117d58c0e66ed5c`  
		Last Modified: Fri, 10 Feb 2023 22:04:47 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfad87e02ca1e94e68f35fcb6a5317dbecde789c57403664ebdd0c04ed09034e`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 48.3 MB (48267904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283fa2ba6508dfcf7ecb4341d52f110a5ede13aea8920ce02d55dadfd434f400`  
		Last Modified: Fri, 10 Feb 2023 22:04:47 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6be70978ac17dcc81ff685a11309cf99a37c80ef80eb20af3d6c1732949690c`  
		Last Modified: Fri, 10 Feb 2023 22:04:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabf93ae76480c129c5e310c20c3f3ca3fd931d3610dc533030db14252f2034e`  
		Last Modified: Fri, 10 Feb 2023 22:04:47 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.13.6`

```console
$ docker pull consul@sha256:fd8ca56fc8bb4b307c6c56bc1558325ac6973f333da20f119aef87fd55dd64bd
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.13.6` - linux; amd64

```console
$ docker pull consul@sha256:bb5d06c0608ff7738fbfe9dd2dfe1ff2e47584df4d30b643c86b5dd52f1225a9
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.3 MB (52259668 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c255782b910a08a35c05aa7037d6a589941c810e14b3aae84fc6df7f9c2bc3c1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:22:25 GMT
ARG CONSUL_VERSION=1.13.6
# Fri, 27 Jan 2023 23:22:25 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.6 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:22:25 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:22:26 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:22:32 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:22:33 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:22:34 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:22:34 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:22:34 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:22:34 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:22:34 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:22:34 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:22:34 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:22:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d2d5b7d642aeea4f3c571ff84c1718b78787eb6f9b65a4c1da0d6939039407f7`  
		Last Modified: Fri, 27 Jan 2023 23:23:17 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:223ca554c4c10498a2aa07b7fd2a2b4b175ff6ef5e1513822768a6da61e6b609`  
		Last Modified: Fri, 27 Jan 2023 23:23:24 GMT  
		Size: 49.4 MB (49432771 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:098020b32602ed9fb3c916dac93aa71d2dc723ec3a5bdfcbdced3a63528d3a39`  
		Last Modified: Fri, 27 Jan 2023 23:23:18 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13024f719284913d712c9bd22fa0f30f6c2d659f26cc0fc277e86a51e3270a67`  
		Last Modified: Fri, 27 Jan 2023 23:23:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcfab706cab18abfef47070bdc9154a099c77b6397e150aa83163778c3240947`  
		Last Modified: Fri, 27 Jan 2023 23:23:17 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13.6` - linux; arm variant v6

```console
$ docker pull consul@sha256:ab4a8762e7b0db96fad0335d4511b16660857e480955dfbd0ea0a88e1f04809a
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49992760 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:23bde051138ee6429cd35893afd82014027c2b07267a21b08c7c3c790f0bba8d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:37 GMT
ADD file:141468a99f598ddb90dbb73978d10c0f00d01ece185e157ac33a0a1414d45944 in / 
# Fri, 10 Feb 2023 20:49:37 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:30:43 GMT
ARG CONSUL_VERSION=1.13.6
# Fri, 10 Feb 2023 21:30:43 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.6 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 10 Feb 2023 21:30:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 10 Feb 2023 21:30:44 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 10 Feb 2023 21:30:51 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 10 Feb 2023 21:30:52 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 10 Feb 2023 21:30:53 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Feb 2023 21:30:53 GMT
VOLUME [/consul/data]
# Fri, 10 Feb 2023 21:30:53 GMT
EXPOSE 8300
# Fri, 10 Feb 2023 21:30:53 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 10 Feb 2023 21:30:53 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 10 Feb 2023 21:30:53 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Feb 2023 21:30:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 21:30:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ed6cbaa656dcebfe8d252792a339ccf10dddd695875f07c9636d59a5baf85f3f`  
		Last Modified: Fri, 10 Feb 2023 20:50:51 GMT  
		Size: 2.6 MB (2633649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a203144cd99d27ad8026f35ce058776d4ecfdf97a6e631470755b3e0ab72c09`  
		Last Modified: Fri, 10 Feb 2023 21:31:55 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ecd0f1f22d72191452316da6668b0678108c06ff40482cf58207f45a7cdd59d7`  
		Last Modified: Fri, 10 Feb 2023 21:32:02 GMT  
		Size: 47.4 MB (47355793 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6990c0599a8e1441e534bf4fe3d414bd2a5ec6d62dd3989a35873c862120bdb9`  
		Last Modified: Fri, 10 Feb 2023 21:31:55 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:17085c9fbbcc776b0c21a61afc5ccf19332369d6bb37b6fe802384864ee10000`  
		Last Modified: Fri, 10 Feb 2023 21:31:55 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:40167d9375b0fe1116a601bb0c337b1f96dcbfdf15ec4f884a0191f645bcfbd5`  
		Last Modified: Fri, 10 Feb 2023 21:31:55 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13.6` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:cc34a54ce28264593ccfa395890a6687d22a7ba363a0a731248b7e1ce8da455f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49477028 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4525bb7e0c28b613b571a39d5234a929f369694b167ba25560d386a3c5309d61`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:16 GMT
ADD file:a73970ac03f28a1d3b9aaee19e859d958867b42fb91f29efb1259fbddc66ffb1 in / 
# Fri, 10 Feb 2023 21:24:16 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:01:38 GMT
ARG CONSUL_VERSION=1.13.6
# Fri, 10 Feb 2023 22:01:38 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.6 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 10 Feb 2023 22:01:38 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 10 Feb 2023 22:01:38 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 10 Feb 2023 22:01:44 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 10 Feb 2023 22:01:45 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 10 Feb 2023 22:01:46 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:01:46 GMT
VOLUME [/consul/data]
# Fri, 10 Feb 2023 22:01:46 GMT
EXPOSE 8300
# Fri, 10 Feb 2023 22:01:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 10 Feb 2023 22:01:46 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 10 Feb 2023 22:01:46 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:01:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:01:46 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:404f35918b797abb27547df3b530ec55a77c499c4dce88f3b90867115087f9e7`  
		Last Modified: Fri, 10 Feb 2023 21:25:01 GMT  
		Size: 2.7 MB (2721556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:478927a30de417c03bdd408b7ca5da00b21dc15193298aca9c443aecaaf793d9`  
		Last Modified: Fri, 10 Feb 2023 22:02:29 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01361edbe24ab319960c2afe4008ab6b2be34b7501a415ef27acc53310e7dff4`  
		Last Modified: Fri, 10 Feb 2023 22:02:33 GMT  
		Size: 46.8 MB (46752091 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb4bb18b1fc6d3283090e0200dd958c01dc19086beb605a3c93ba9b80b6634cf`  
		Last Modified: Fri, 10 Feb 2023 22:02:28 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7cbcb79adf5399e3b4d77c2afa78efdef76825f6253e474648c77199b77a90ac`  
		Last Modified: Fri, 10 Feb 2023 22:02:28 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd5fa1afae393b3e16ae75e072f091a42f8e532a2f21db71406ef9cb53ca702`  
		Last Modified: Fri, 10 Feb 2023 22:02:28 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13.6` - linux; 386

```console
$ docker pull consul@sha256:a5646227868691c8ceb6113fd990abf9815dc8bf655315afae5cd2d22dd994c2
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51103557 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fd9c553bc28ec0551a625418290acaa17f9f2470a95df906a79f238d9afd7f9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:34 GMT
ADD file:35855658886412913d05c0f9e29bf8f650c0d37e20100a9de118b468f86f7f30 in / 
# Fri, 10 Feb 2023 21:24:34 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:03:25 GMT
ARG CONSUL_VERSION=1.13.6
# Fri, 10 Feb 2023 22:03:25 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.6 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 10 Feb 2023 22:03:26 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 10 Feb 2023 22:03:27 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 10 Feb 2023 22:03:33 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 10 Feb 2023 22:03:34 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 10 Feb 2023 22:03:35 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:36 GMT
VOLUME [/consul/data]
# Fri, 10 Feb 2023 22:03:37 GMT
EXPOSE 8300
# Fri, 10 Feb 2023 22:03:38 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 10 Feb 2023 22:03:39 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 10 Feb 2023 22:03:41 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:03:41 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:13a1d7e543968b1c2bd92ca5f2fb2e964b31713fc7707305c1cdfb935ca3e631`  
		Last Modified: Fri, 10 Feb 2023 21:25:40 GMT  
		Size: 2.8 MB (2832331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20ef7336dc444a6681ae6f81ee98295bcc132fb3a90957a79117d58c0e66ed5c`  
		Last Modified: Fri, 10 Feb 2023 22:04:47 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfad87e02ca1e94e68f35fcb6a5317dbecde789c57403664ebdd0c04ed09034e`  
		Last Modified: Fri, 10 Feb 2023 22:04:52 GMT  
		Size: 48.3 MB (48267904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:283fa2ba6508dfcf7ecb4341d52f110a5ede13aea8920ce02d55dadfd434f400`  
		Last Modified: Fri, 10 Feb 2023 22:04:47 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b6be70978ac17dcc81ff685a11309cf99a37c80ef80eb20af3d6c1732949690c`  
		Last Modified: Fri, 10 Feb 2023 22:04:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fabf93ae76480c129c5e310c20c3f3ca3fd931d3610dc533030db14252f2034e`  
		Last Modified: Fri, 10 Feb 2023 22:04:47 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.14`

```console
$ docker pull consul@sha256:99a33ee1421b1eb47e6bbebd8a28627cf18c8afe584aace165abe72fad43b28f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.14` - linux; amd64

```console
$ docker pull consul@sha256:e94f0bb628021e8b4b0ea3ff3db15d11d6ccd58ca13f8dd6a7cc9fc3e7fa1486
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56313718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e08ca30757a317d8a2e1e5b99a1560e06c6fa47df0760b33b04d1ad1bb948fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:22:13 GMT
ARG CONSUL_VERSION=1.14.4
# Fri, 27 Jan 2023 23:22:13 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:22:14 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:22:14 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:22:20 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:22:21 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:22:22 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:22:22 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:22:22 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:22:22 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:22:22 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:22:23 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:22:23 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d0af5b93a96bd4a9544ee9e435635ebecd7b738d875fc4a2a76c3cd308d611`  
		Last Modified: Fri, 27 Jan 2023 23:23:00 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1774eabcfec8e042c60791a6da342e9f9b461bd6d6aba998bb69bcc28d2c8c5`  
		Last Modified: Fri, 27 Jan 2023 23:23:07 GMT  
		Size: 53.5 MB (53486820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78c262c5cc2055d2ebfd5115cebf2ced39525d7fb32e0292c588128d588e334`  
		Last Modified: Fri, 27 Jan 2023 23:23:00 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e9961ee380dad2f5f672a848788c40255013bc431045ed1b2f70f69233d166`  
		Last Modified: Fri, 27 Jan 2023 23:23:00 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e4f665c34e561401ea9354fac75fed922fe3035bc8bb516b7d55eab144a880`  
		Last Modified: Fri, 27 Jan 2023 23:23:00 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14` - linux; arm variant v6

```console
$ docker pull consul@sha256:a10b8a74730b73ea84dbd0a0678e87a6af8e9e20652ca57a0608af254fe69d6d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53714998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2229f0feda5c42cde7eaaefc16b767a6146c21233f43deaebdf230e869a9cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:37 GMT
ADD file:141468a99f598ddb90dbb73978d10c0f00d01ece185e157ac33a0a1414d45944 in / 
# Fri, 10 Feb 2023 20:49:37 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:30:26 GMT
ARG CONSUL_VERSION=1.14.4
# Fri, 10 Feb 2023 21:30:26 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 10 Feb 2023 21:30:26 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 10 Feb 2023 21:30:27 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 10 Feb 2023 21:30:35 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 10 Feb 2023 21:30:36 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 10 Feb 2023 21:30:36 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Feb 2023 21:30:36 GMT
VOLUME [/consul/data]
# Fri, 10 Feb 2023 21:30:37 GMT
EXPOSE 8300
# Fri, 10 Feb 2023 21:30:37 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 10 Feb 2023 21:30:37 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 10 Feb 2023 21:30:37 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Feb 2023 21:30:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 21:30:37 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ed6cbaa656dcebfe8d252792a339ccf10dddd695875f07c9636d59a5baf85f3f`  
		Last Modified: Fri, 10 Feb 2023 20:50:51 GMT  
		Size: 2.6 MB (2633649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15679575500979d2c802ec409d24aac6ccebfec03aa0c84f2ab09ac81e74139`  
		Last Modified: Fri, 10 Feb 2023 21:31:33 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7cfc00fb1b7349584d66f1706a34434f152ee5dd20cfad3f3749652d01833c`  
		Last Modified: Fri, 10 Feb 2023 21:31:40 GMT  
		Size: 51.1 MB (51078033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e6df18df0cf026ae82acec2971fa7305c95363f66344e749876b349ed21612`  
		Last Modified: Fri, 10 Feb 2023 21:31:33 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69191e4c2d1de20f3c7bf3ddf5ac48fce16c885577861e20f9f713cdc33cab43`  
		Last Modified: Fri, 10 Feb 2023 21:31:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed4f90a9a21bf4d09a519cb7986d166297834a036cd9bc4afda7dbf06462916`  
		Last Modified: Fri, 10 Feb 2023 21:31:33 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:57355f6f632f1a78305ffc430d940e6630c809eb9a80db54c498489dac3504a1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53141443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d655387a1164567de86de6dd008ac7777c23224421b37ede5ddec85dedbdaf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:16 GMT
ADD file:a73970ac03f28a1d3b9aaee19e859d958867b42fb91f29efb1259fbddc66ffb1 in / 
# Fri, 10 Feb 2023 21:24:16 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:01:26 GMT
ARG CONSUL_VERSION=1.14.4
# Fri, 10 Feb 2023 22:01:26 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 10 Feb 2023 22:01:26 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 10 Feb 2023 22:01:27 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 10 Feb 2023 22:01:33 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 10 Feb 2023 22:01:34 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 10 Feb 2023 22:01:34 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:01:34 GMT
VOLUME [/consul/data]
# Fri, 10 Feb 2023 22:01:34 GMT
EXPOSE 8300
# Fri, 10 Feb 2023 22:01:35 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 10 Feb 2023 22:01:35 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 10 Feb 2023 22:01:35 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:01:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:01:35 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:404f35918b797abb27547df3b530ec55a77c499c4dce88f3b90867115087f9e7`  
		Last Modified: Fri, 10 Feb 2023 21:25:01 GMT  
		Size: 2.7 MB (2721556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5f5a93605265de2bf7d1ce0a04b31e9206424042dd482959fa40ae232e004c`  
		Last Modified: Fri, 10 Feb 2023 22:02:11 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2643ebb7531da6503768460e59c74886ed8290708898a767795e01cc43ff35d`  
		Last Modified: Fri, 10 Feb 2023 22:02:16 GMT  
		Size: 50.4 MB (50416508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d229f64652a58dfbe39028360c58d336eeb0d20c9d25472dd0530766bb84bf`  
		Last Modified: Fri, 10 Feb 2023 22:02:11 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833943f861feda487a0c0d67bd4db9cb122b2a3c32160d897d3b30ae71e01924`  
		Last Modified: Fri, 10 Feb 2023 22:02:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8986cc9f0209a2e424ae170ce3a41bdcf3a0e14e1d6ff01d0106d0c979a1eecb`  
		Last Modified: Fri, 10 Feb 2023 22:02:11 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14` - linux; 386

```console
$ docker pull consul@sha256:0c1d3d2994ca511f1bc535f1c8c676edb05fc71cf8f72539219d07a4dcfd9eb0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55105674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3605988f2c033cffa95d60c18b54f2ccb59d1e7fa3e4e388a650401eaecd5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:34 GMT
ADD file:35855658886412913d05c0f9e29bf8f650c0d37e20100a9de118b468f86f7f30 in / 
# Fri, 10 Feb 2023 21:24:34 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:03:02 GMT
ARG CONSUL_VERSION=1.14.4
# Fri, 10 Feb 2023 22:03:03 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 10 Feb 2023 22:03:04 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 10 Feb 2023 22:03:05 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 10 Feb 2023 22:03:12 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 10 Feb 2023 22:03:12 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 10 Feb 2023 22:03:13 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:14 GMT
VOLUME [/consul/data]
# Fri, 10 Feb 2023 22:03:15 GMT
EXPOSE 8300
# Fri, 10 Feb 2023 22:03:16 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 10 Feb 2023 22:03:17 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 10 Feb 2023 22:03:19 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:03:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:20 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:13a1d7e543968b1c2bd92ca5f2fb2e964b31713fc7707305c1cdfb935ca3e631`  
		Last Modified: Fri, 10 Feb 2023 21:25:40 GMT  
		Size: 2.8 MB (2832331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0626ffa155376b749904ceb751a1ae408838cca2e5721c6580008f030426cdc7`  
		Last Modified: Fri, 10 Feb 2023 22:04:27 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd233d2be3a37dbe1751e1366adbcd99e61856297d5c6539625a8daeaed6dde7`  
		Last Modified: Fri, 10 Feb 2023 22:04:33 GMT  
		Size: 52.3 MB (52270026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d486f1c16831806e60d70ae53f27852ec83746e1cb76828000bea84f2ae5bc5e`  
		Last Modified: Fri, 10 Feb 2023 22:04:27 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0c72a0c71ba3fd81b8af6ab034d8bb7457187e133e1748c405137bd7e84bb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:27 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f96af6f4f778791cb130d71bcc0562bcf25d75d234daa29044417547c52e44`  
		Last Modified: Fri, 10 Feb 2023 22:04:27 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.14.4`

```console
$ docker pull consul@sha256:99a33ee1421b1eb47e6bbebd8a28627cf18c8afe584aace165abe72fad43b28f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.14.4` - linux; amd64

```console
$ docker pull consul@sha256:e94f0bb628021e8b4b0ea3ff3db15d11d6ccd58ca13f8dd6a7cc9fc3e7fa1486
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56313718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e08ca30757a317d8a2e1e5b99a1560e06c6fa47df0760b33b04d1ad1bb948fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:22:13 GMT
ARG CONSUL_VERSION=1.14.4
# Fri, 27 Jan 2023 23:22:13 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:22:14 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:22:14 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:22:20 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:22:21 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:22:22 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:22:22 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:22:22 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:22:22 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:22:22 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:22:23 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:22:23 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d0af5b93a96bd4a9544ee9e435635ebecd7b738d875fc4a2a76c3cd308d611`  
		Last Modified: Fri, 27 Jan 2023 23:23:00 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1774eabcfec8e042c60791a6da342e9f9b461bd6d6aba998bb69bcc28d2c8c5`  
		Last Modified: Fri, 27 Jan 2023 23:23:07 GMT  
		Size: 53.5 MB (53486820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78c262c5cc2055d2ebfd5115cebf2ced39525d7fb32e0292c588128d588e334`  
		Last Modified: Fri, 27 Jan 2023 23:23:00 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e9961ee380dad2f5f672a848788c40255013bc431045ed1b2f70f69233d166`  
		Last Modified: Fri, 27 Jan 2023 23:23:00 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e4f665c34e561401ea9354fac75fed922fe3035bc8bb516b7d55eab144a880`  
		Last Modified: Fri, 27 Jan 2023 23:23:00 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14.4` - linux; arm variant v6

```console
$ docker pull consul@sha256:a10b8a74730b73ea84dbd0a0678e87a6af8e9e20652ca57a0608af254fe69d6d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53714998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2229f0feda5c42cde7eaaefc16b767a6146c21233f43deaebdf230e869a9cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:37 GMT
ADD file:141468a99f598ddb90dbb73978d10c0f00d01ece185e157ac33a0a1414d45944 in / 
# Fri, 10 Feb 2023 20:49:37 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:30:26 GMT
ARG CONSUL_VERSION=1.14.4
# Fri, 10 Feb 2023 21:30:26 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 10 Feb 2023 21:30:26 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 10 Feb 2023 21:30:27 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 10 Feb 2023 21:30:35 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 10 Feb 2023 21:30:36 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 10 Feb 2023 21:30:36 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Feb 2023 21:30:36 GMT
VOLUME [/consul/data]
# Fri, 10 Feb 2023 21:30:37 GMT
EXPOSE 8300
# Fri, 10 Feb 2023 21:30:37 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 10 Feb 2023 21:30:37 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 10 Feb 2023 21:30:37 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Feb 2023 21:30:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 21:30:37 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ed6cbaa656dcebfe8d252792a339ccf10dddd695875f07c9636d59a5baf85f3f`  
		Last Modified: Fri, 10 Feb 2023 20:50:51 GMT  
		Size: 2.6 MB (2633649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15679575500979d2c802ec409d24aac6ccebfec03aa0c84f2ab09ac81e74139`  
		Last Modified: Fri, 10 Feb 2023 21:31:33 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7cfc00fb1b7349584d66f1706a34434f152ee5dd20cfad3f3749652d01833c`  
		Last Modified: Fri, 10 Feb 2023 21:31:40 GMT  
		Size: 51.1 MB (51078033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e6df18df0cf026ae82acec2971fa7305c95363f66344e749876b349ed21612`  
		Last Modified: Fri, 10 Feb 2023 21:31:33 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69191e4c2d1de20f3c7bf3ddf5ac48fce16c885577861e20f9f713cdc33cab43`  
		Last Modified: Fri, 10 Feb 2023 21:31:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed4f90a9a21bf4d09a519cb7986d166297834a036cd9bc4afda7dbf06462916`  
		Last Modified: Fri, 10 Feb 2023 21:31:33 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14.4` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:57355f6f632f1a78305ffc430d940e6630c809eb9a80db54c498489dac3504a1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53141443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d655387a1164567de86de6dd008ac7777c23224421b37ede5ddec85dedbdaf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:16 GMT
ADD file:a73970ac03f28a1d3b9aaee19e859d958867b42fb91f29efb1259fbddc66ffb1 in / 
# Fri, 10 Feb 2023 21:24:16 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:01:26 GMT
ARG CONSUL_VERSION=1.14.4
# Fri, 10 Feb 2023 22:01:26 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 10 Feb 2023 22:01:26 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 10 Feb 2023 22:01:27 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 10 Feb 2023 22:01:33 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 10 Feb 2023 22:01:34 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 10 Feb 2023 22:01:34 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:01:34 GMT
VOLUME [/consul/data]
# Fri, 10 Feb 2023 22:01:34 GMT
EXPOSE 8300
# Fri, 10 Feb 2023 22:01:35 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 10 Feb 2023 22:01:35 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 10 Feb 2023 22:01:35 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:01:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:01:35 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:404f35918b797abb27547df3b530ec55a77c499c4dce88f3b90867115087f9e7`  
		Last Modified: Fri, 10 Feb 2023 21:25:01 GMT  
		Size: 2.7 MB (2721556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5f5a93605265de2bf7d1ce0a04b31e9206424042dd482959fa40ae232e004c`  
		Last Modified: Fri, 10 Feb 2023 22:02:11 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2643ebb7531da6503768460e59c74886ed8290708898a767795e01cc43ff35d`  
		Last Modified: Fri, 10 Feb 2023 22:02:16 GMT  
		Size: 50.4 MB (50416508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d229f64652a58dfbe39028360c58d336eeb0d20c9d25472dd0530766bb84bf`  
		Last Modified: Fri, 10 Feb 2023 22:02:11 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833943f861feda487a0c0d67bd4db9cb122b2a3c32160d897d3b30ae71e01924`  
		Last Modified: Fri, 10 Feb 2023 22:02:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8986cc9f0209a2e424ae170ce3a41bdcf3a0e14e1d6ff01d0106d0c979a1eecb`  
		Last Modified: Fri, 10 Feb 2023 22:02:11 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14.4` - linux; 386

```console
$ docker pull consul@sha256:0c1d3d2994ca511f1bc535f1c8c676edb05fc71cf8f72539219d07a4dcfd9eb0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55105674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3605988f2c033cffa95d60c18b54f2ccb59d1e7fa3e4e388a650401eaecd5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:34 GMT
ADD file:35855658886412913d05c0f9e29bf8f650c0d37e20100a9de118b468f86f7f30 in / 
# Fri, 10 Feb 2023 21:24:34 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:03:02 GMT
ARG CONSUL_VERSION=1.14.4
# Fri, 10 Feb 2023 22:03:03 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 10 Feb 2023 22:03:04 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 10 Feb 2023 22:03:05 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 10 Feb 2023 22:03:12 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 10 Feb 2023 22:03:12 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 10 Feb 2023 22:03:13 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:14 GMT
VOLUME [/consul/data]
# Fri, 10 Feb 2023 22:03:15 GMT
EXPOSE 8300
# Fri, 10 Feb 2023 22:03:16 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 10 Feb 2023 22:03:17 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 10 Feb 2023 22:03:19 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:03:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:20 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:13a1d7e543968b1c2bd92ca5f2fb2e964b31713fc7707305c1cdfb935ca3e631`  
		Last Modified: Fri, 10 Feb 2023 21:25:40 GMT  
		Size: 2.8 MB (2832331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0626ffa155376b749904ceb751a1ae408838cca2e5721c6580008f030426cdc7`  
		Last Modified: Fri, 10 Feb 2023 22:04:27 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd233d2be3a37dbe1751e1366adbcd99e61856297d5c6539625a8daeaed6dde7`  
		Last Modified: Fri, 10 Feb 2023 22:04:33 GMT  
		Size: 52.3 MB (52270026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d486f1c16831806e60d70ae53f27852ec83746e1cb76828000bea84f2ae5bc5e`  
		Last Modified: Fri, 10 Feb 2023 22:04:27 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0c72a0c71ba3fd81b8af6ab034d8bb7457187e133e1748c405137bd7e84bb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:27 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f96af6f4f778791cb130d71bcc0562bcf25d75d234daa29044417547c52e44`  
		Last Modified: Fri, 10 Feb 2023 22:04:27 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:99a33ee1421b1eb47e6bbebd8a28627cf18c8afe584aace165abe72fad43b28f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:e94f0bb628021e8b4b0ea3ff3db15d11d6ccd58ca13f8dd6a7cc9fc3e7fa1486
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.3 MB (56313718 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1e08ca30757a317d8a2e1e5b99a1560e06c6fa47df0760b33b04d1ad1bb948fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:22:13 GMT
ARG CONSUL_VERSION=1.14.4
# Fri, 27 Jan 2023 23:22:13 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:22:14 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:22:14 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:22:20 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:22:21 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:22:22 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:22:22 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:22:22 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:22:22 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:22:22 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:22:23 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:22:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:22:23 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82d0af5b93a96bd4a9544ee9e435635ebecd7b738d875fc4a2a76c3cd308d611`  
		Last Modified: Fri, 27 Jan 2023 23:23:00 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1774eabcfec8e042c60791a6da342e9f9b461bd6d6aba998bb69bcc28d2c8c5`  
		Last Modified: Fri, 27 Jan 2023 23:23:07 GMT  
		Size: 53.5 MB (53486820 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f78c262c5cc2055d2ebfd5115cebf2ced39525d7fb32e0292c588128d588e334`  
		Last Modified: Fri, 27 Jan 2023 23:23:00 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38e9961ee380dad2f5f672a848788c40255013bc431045ed1b2f70f69233d166`  
		Last Modified: Fri, 27 Jan 2023 23:23:00 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2e4f665c34e561401ea9354fac75fed922fe3035bc8bb516b7d55eab144a880`  
		Last Modified: Fri, 27 Jan 2023 23:23:00 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:a10b8a74730b73ea84dbd0a0678e87a6af8e9e20652ca57a0608af254fe69d6d
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53714998 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0a2229f0feda5c42cde7eaaefc16b767a6146c21233f43deaebdf230e869a9cc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 20:49:37 GMT
ADD file:141468a99f598ddb90dbb73978d10c0f00d01ece185e157ac33a0a1414d45944 in / 
# Fri, 10 Feb 2023 20:49:37 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 21:30:26 GMT
ARG CONSUL_VERSION=1.14.4
# Fri, 10 Feb 2023 21:30:26 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 10 Feb 2023 21:30:26 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 10 Feb 2023 21:30:27 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 10 Feb 2023 21:30:35 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 10 Feb 2023 21:30:36 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 10 Feb 2023 21:30:36 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Feb 2023 21:30:36 GMT
VOLUME [/consul/data]
# Fri, 10 Feb 2023 21:30:37 GMT
EXPOSE 8300
# Fri, 10 Feb 2023 21:30:37 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 10 Feb 2023 21:30:37 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 10 Feb 2023 21:30:37 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Feb 2023 21:30:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 21:30:37 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ed6cbaa656dcebfe8d252792a339ccf10dddd695875f07c9636d59a5baf85f3f`  
		Last Modified: Fri, 10 Feb 2023 20:50:51 GMT  
		Size: 2.6 MB (2633649 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b15679575500979d2c802ec409d24aac6ccebfec03aa0c84f2ab09ac81e74139`  
		Last Modified: Fri, 10 Feb 2023 21:31:33 GMT  
		Size: 1.2 KB (1238 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe7cfc00fb1b7349584d66f1706a34434f152ee5dd20cfad3f3749652d01833c`  
		Last Modified: Fri, 10 Feb 2023 21:31:40 GMT  
		Size: 51.1 MB (51078033 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5e6df18df0cf026ae82acec2971fa7305c95363f66344e749876b349ed21612`  
		Last Modified: Fri, 10 Feb 2023 21:31:33 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:69191e4c2d1de20f3c7bf3ddf5ac48fce16c885577861e20f9f713cdc33cab43`  
		Last Modified: Fri, 10 Feb 2023 21:31:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fed4f90a9a21bf4d09a519cb7986d166297834a036cd9bc4afda7dbf06462916`  
		Last Modified: Fri, 10 Feb 2023 21:31:33 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:57355f6f632f1a78305ffc430d940e6630c809eb9a80db54c498489dac3504a1
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53141443 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9d655387a1164567de86de6dd008ac7777c23224421b37ede5ddec85dedbdaf2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:16 GMT
ADD file:a73970ac03f28a1d3b9aaee19e859d958867b42fb91f29efb1259fbddc66ffb1 in / 
# Fri, 10 Feb 2023 21:24:16 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:01:26 GMT
ARG CONSUL_VERSION=1.14.4
# Fri, 10 Feb 2023 22:01:26 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 10 Feb 2023 22:01:26 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 10 Feb 2023 22:01:27 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 10 Feb 2023 22:01:33 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 10 Feb 2023 22:01:34 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 10 Feb 2023 22:01:34 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:01:34 GMT
VOLUME [/consul/data]
# Fri, 10 Feb 2023 22:01:34 GMT
EXPOSE 8300
# Fri, 10 Feb 2023 22:01:35 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 10 Feb 2023 22:01:35 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 10 Feb 2023 22:01:35 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:01:35 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:01:35 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:404f35918b797abb27547df3b530ec55a77c499c4dce88f3b90867115087f9e7`  
		Last Modified: Fri, 10 Feb 2023 21:25:01 GMT  
		Size: 2.7 MB (2721556 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f5f5a93605265de2bf7d1ce0a04b31e9206424042dd482959fa40ae232e004c`  
		Last Modified: Fri, 10 Feb 2023 22:02:11 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2643ebb7531da6503768460e59c74886ed8290708898a767795e01cc43ff35d`  
		Last Modified: Fri, 10 Feb 2023 22:02:16 GMT  
		Size: 50.4 MB (50416508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94d229f64652a58dfbe39028360c58d336eeb0d20c9d25472dd0530766bb84bf`  
		Last Modified: Fri, 10 Feb 2023 22:02:11 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:833943f861feda487a0c0d67bd4db9cb122b2a3c32160d897d3b30ae71e01924`  
		Last Modified: Fri, 10 Feb 2023 22:02:11 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8986cc9f0209a2e424ae170ce3a41bdcf3a0e14e1d6ff01d0106d0c979a1eecb`  
		Last Modified: Fri, 10 Feb 2023 22:02:11 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:0c1d3d2994ca511f1bc535f1c8c676edb05fc71cf8f72539219d07a4dcfd9eb0
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55105674 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee3605988f2c033cffa95d60c18b54f2ccb59d1e7fa3e4e388a650401eaecd5e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 10 Feb 2023 21:24:34 GMT
ADD file:35855658886412913d05c0f9e29bf8f650c0d37e20100a9de118b468f86f7f30 in / 
# Fri, 10 Feb 2023 21:24:34 GMT
CMD ["/bin/sh"]
# Fri, 10 Feb 2023 22:03:02 GMT
ARG CONSUL_VERSION=1.14.4
# Fri, 10 Feb 2023 22:03:03 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 10 Feb 2023 22:03:04 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 10 Feb 2023 22:03:05 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 10 Feb 2023 22:03:12 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 10 Feb 2023 22:03:12 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 10 Feb 2023 22:03:13 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 10 Feb 2023 22:03:14 GMT
VOLUME [/consul/data]
# Fri, 10 Feb 2023 22:03:15 GMT
EXPOSE 8300
# Fri, 10 Feb 2023 22:03:16 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 10 Feb 2023 22:03:17 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 10 Feb 2023 22:03:19 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 10 Feb 2023 22:03:19 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 10 Feb 2023 22:03:20 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:13a1d7e543968b1c2bd92ca5f2fb2e964b31713fc7707305c1cdfb935ca3e631`  
		Last Modified: Fri, 10 Feb 2023 21:25:40 GMT  
		Size: 2.8 MB (2832331 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0626ffa155376b749904ceb751a1ae408838cca2e5721c6580008f030426cdc7`  
		Last Modified: Fri, 10 Feb 2023 22:04:27 GMT  
		Size: 1.2 KB (1239 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd233d2be3a37dbe1751e1366adbcd99e61856297d5c6539625a8daeaed6dde7`  
		Last Modified: Fri, 10 Feb 2023 22:04:33 GMT  
		Size: 52.3 MB (52270026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d486f1c16831806e60d70ae53f27852ec83746e1cb76828000bea84f2ae5bc5e`  
		Last Modified: Fri, 10 Feb 2023 22:04:27 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b0c72a0c71ba3fd81b8af6ab034d8bb7457187e133e1748c405137bd7e84bb6`  
		Last Modified: Fri, 10 Feb 2023 22:04:27 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4f96af6f4f778791cb130d71bcc0562bcf25d75d234daa29044417547c52e44`  
		Last Modified: Fri, 10 Feb 2023 22:04:27 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
