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
$ docker pull consul@sha256:a59a6e3c2f06c15e3607fd651dbd52431523d609d4703eed60b97520352eb6b0
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
$ docker pull consul@sha256:ea4b2f7dae7e36dccee7a0c068b29f4150d5db16ebb1da3df442c6a49ab5d8bd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47660867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754c3e40e0e05791271745f9c2cf6964c93800d649b7a633c71e51648a02901c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 10 Nov 2022 20:49:36 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Thu, 10 Nov 2022 20:49:36 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:49:59 GMT
ARG CONSUL_VERSION=1.12.9
# Fri, 27 Jan 2023 23:50:00 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:50:00 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:50:00 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:50:07 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:50:08 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:50:08 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:50:09 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:50:09 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:50:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:50:09 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:50:09 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:50:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:50:09 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9511c74e56fa361807ae74760ce0c477d91c7eff7b060af1d0276628757c6cd2`  
		Last Modified: Fri, 27 Jan 2023 23:51:18 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63641ca73fbede6ddf583351a69a6cf5871210ca750d7e8b5d7cbfdcaa0ca03`  
		Last Modified: Fri, 27 Jan 2023 23:51:25 GMT  
		Size: 45.0 MB (45026417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f71577fac5a575916616589729fdadac653822ee10dafceef526e1632f97c2`  
		Last Modified: Fri, 27 Jan 2023 23:51:18 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf48b00ecb6efc7b6c68c501ccd833c43e787dc0d782e951ef0a3e215f42a2a`  
		Last Modified: Fri, 27 Jan 2023 23:51:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a0288e3aaa77058071d6b18b3556e076701602b5c7a859052f354f520cb8ba`  
		Last Modified: Fri, 27 Jan 2023 23:51:18 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:b9344189cabd66bc01b954cef55e4e13eb0613556bf007b560f986b1143ed6f3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47443616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530938b00481456d98fef18f79c079e250417d1c4d4fa67f231db485381105d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:46 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Thu, 10 Nov 2022 20:39:46 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:44:01 GMT
ARG CONSUL_VERSION=1.12.9
# Fri, 27 Jan 2023 23:44:01 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:44:02 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:44:02 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:44:07 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:44:08 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:44:08 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:44:08 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:44:08 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:44:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:44:09 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:44:09 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:44:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:44:09 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cbd3a467cf004d30db4149ae00f4d07d4a0f137e59533c7ff3b9c894bc357f`  
		Last Modified: Fri, 27 Jan 2023 23:44:51 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4adeedc59de4872ecbe47791f5ad900fd7d3b14bd3636a622b20becac19bcd8a`  
		Last Modified: Fri, 27 Jan 2023 23:44:55 GMT  
		Size: 44.7 MB (44721794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24d49ee265602102fd0745dbf220639a057bdd1bac91d4c9d6a782457a98191`  
		Last Modified: Fri, 27 Jan 2023 23:44:51 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e15e7dfd8ac5b11d72b26ea918dda81d3e03290dd9589823b5f90d9afd239ef`  
		Last Modified: Fri, 27 Jan 2023 23:44:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8c973a302115214cff9fa1db73e31c0e3888f3d921c3bf9ab1555bed3bc16b`  
		Last Modified: Fri, 27 Jan 2023 23:44:51 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12` - linux; 386

```console
$ docker pull consul@sha256:349cb18e92ca9f193b87358c3283c694dd12264715700fb1d128b5c525d3be42
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48892021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a48d16f968337191e6115af87aa2cd7acb9956f6bd118deb100149671b55f5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:47 GMT
ADD file:d51bb92de86c49ee5486066d12194be78c8b9a8452c44577e2dfeef1945a0138 in / 
# Tue, 09 Aug 2022 17:38:47 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:41:16 GMT
ARG CONSUL_VERSION=1.12.9
# Fri, 27 Jan 2023 23:41:17 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:41:18 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:41:19 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:41:26 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:41:26 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:41:27 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:41:28 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:41:29 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:41:30 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:41:31 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:41:33 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:41:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:41:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f8c6eeaa55b0f135b7fddb3d7745a98ca4d8f06d2898611234b9ef99e1183073`  
		Last Modified: Tue, 09 Aug 2022 17:39:50 GMT  
		Size: 2.8 MB (2828516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10eb1f8d45d315e6ede9421830f1552b3e24dbc3d0857e33e947610077a98ec9`  
		Last Modified: Fri, 27 Jan 2023 23:42:30 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0242b55e8c9d1f0ab0e33c4d52ff2cb302709ab09c371eecca1969b6b40adc77`  
		Last Modified: Fri, 27 Jan 2023 23:42:35 GMT  
		Size: 46.1 MB (46060178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b68d20f7c8761c8f0e73efc095b4e07c448babef3534a36a3310f3b6190d43`  
		Last Modified: Fri, 27 Jan 2023 23:42:30 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f025bc4bc43e1acd1a54c18a642accfa7117d647318f751515d04f7028d25ec6`  
		Last Modified: Fri, 27 Jan 2023 23:42:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e695eb60977a0d0ec6ea653d466ddaa17ea2c338fb7a63953c026d451b0c13`  
		Last Modified: Fri, 27 Jan 2023 23:42:30 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.12.9`

```console
$ docker pull consul@sha256:a59a6e3c2f06c15e3607fd651dbd52431523d609d4703eed60b97520352eb6b0
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
$ docker pull consul@sha256:ea4b2f7dae7e36dccee7a0c068b29f4150d5db16ebb1da3df442c6a49ab5d8bd
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.7 MB (47660867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:754c3e40e0e05791271745f9c2cf6964c93800d649b7a633c71e51648a02901c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 10 Nov 2022 20:49:36 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Thu, 10 Nov 2022 20:49:36 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:49:59 GMT
ARG CONSUL_VERSION=1.12.9
# Fri, 27 Jan 2023 23:50:00 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:50:00 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:50:00 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:50:07 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:50:08 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:50:08 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:50:09 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:50:09 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:50:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:50:09 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:50:09 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:50:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:50:09 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9511c74e56fa361807ae74760ce0c477d91c7eff7b060af1d0276628757c6cd2`  
		Last Modified: Fri, 27 Jan 2023 23:51:18 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c63641ca73fbede6ddf583351a69a6cf5871210ca750d7e8b5d7cbfdcaa0ca03`  
		Last Modified: Fri, 27 Jan 2023 23:51:25 GMT  
		Size: 45.0 MB (45026417 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64f71577fac5a575916616589729fdadac653822ee10dafceef526e1632f97c2`  
		Last Modified: Fri, 27 Jan 2023 23:51:18 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3bf48b00ecb6efc7b6c68c501ccd833c43e787dc0d782e951ef0a3e215f42a2a`  
		Last Modified: Fri, 27 Jan 2023 23:51:18 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2a0288e3aaa77058071d6b18b3556e076701602b5c7a859052f354f520cb8ba`  
		Last Modified: Fri, 27 Jan 2023 23:51:18 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:b9344189cabd66bc01b954cef55e4e13eb0613556bf007b560f986b1143ed6f3
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47443616 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:530938b00481456d98fef18f79c079e250417d1c4d4fa67f231db485381105d6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:46 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Thu, 10 Nov 2022 20:39:46 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:44:01 GMT
ARG CONSUL_VERSION=1.12.9
# Fri, 27 Jan 2023 23:44:01 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:44:02 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:44:02 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:44:07 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:44:08 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:44:08 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:44:08 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:44:08 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:44:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:44:09 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:44:09 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:44:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:44:09 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64cbd3a467cf004d30db4149ae00f4d07d4a0f137e59533c7ff3b9c894bc357f`  
		Last Modified: Fri, 27 Jan 2023 23:44:51 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4adeedc59de4872ecbe47791f5ad900fd7d3b14bd3636a622b20becac19bcd8a`  
		Last Modified: Fri, 27 Jan 2023 23:44:55 GMT  
		Size: 44.7 MB (44721794 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f24d49ee265602102fd0745dbf220639a057bdd1bac91d4c9d6a782457a98191`  
		Last Modified: Fri, 27 Jan 2023 23:44:51 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e15e7dfd8ac5b11d72b26ea918dda81d3e03290dd9589823b5f90d9afd239ef`  
		Last Modified: Fri, 27 Jan 2023 23:44:51 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2d8c973a302115214cff9fa1db73e31c0e3888f3d921c3bf9ab1555bed3bc16b`  
		Last Modified: Fri, 27 Jan 2023 23:44:51 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12.9` - linux; 386

```console
$ docker pull consul@sha256:349cb18e92ca9f193b87358c3283c694dd12264715700fb1d128b5c525d3be42
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.9 MB (48892021 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4a48d16f968337191e6115af87aa2cd7acb9956f6bd118deb100149671b55f5a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:47 GMT
ADD file:d51bb92de86c49ee5486066d12194be78c8b9a8452c44577e2dfeef1945a0138 in / 
# Tue, 09 Aug 2022 17:38:47 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:41:16 GMT
ARG CONSUL_VERSION=1.12.9
# Fri, 27 Jan 2023 23:41:17 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:41:18 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:41:19 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:41:26 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:41:26 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:41:27 GMT
# ARGS: CONSUL_VERSION=1.12.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:41:28 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:41:29 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:41:30 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:41:31 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:41:33 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:41:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:41:34 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f8c6eeaa55b0f135b7fddb3d7745a98ca4d8f06d2898611234b9ef99e1183073`  
		Last Modified: Tue, 09 Aug 2022 17:39:50 GMT  
		Size: 2.8 MB (2828516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10eb1f8d45d315e6ede9421830f1552b3e24dbc3d0857e33e947610077a98ec9`  
		Last Modified: Fri, 27 Jan 2023 23:42:30 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0242b55e8c9d1f0ab0e33c4d52ff2cb302709ab09c371eecca1969b6b40adc77`  
		Last Modified: Fri, 27 Jan 2023 23:42:35 GMT  
		Size: 46.1 MB (46060178 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e6b68d20f7c8761c8f0e73efc095b4e07c448babef3534a36a3310f3b6190d43`  
		Last Modified: Fri, 27 Jan 2023 23:42:30 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f025bc4bc43e1acd1a54c18a642accfa7117d647318f751515d04f7028d25ec6`  
		Last Modified: Fri, 27 Jan 2023 23:42:30 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e695eb60977a0d0ec6ea653d466ddaa17ea2c338fb7a63953c026d451b0c13`  
		Last Modified: Fri, 27 Jan 2023 23:42:30 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.13`

```console
$ docker pull consul@sha256:f0461a3eec0fa3dc8a86e18a2a19d92a8eb638c74a04d8d1f3b5a1d5253a0e70
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
$ docker pull consul@sha256:9a913e7911c871050287166bb381b20bc815fe3231f31c3df3f2710d29dd4c2c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49990254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e139e945cd30c3ae467f02c04cc501d7addc6123cb6bc1bef930ccc47c4b9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 10 Nov 2022 20:49:36 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Thu, 10 Nov 2022 20:49:36 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:49:39 GMT
ARG CONSUL_VERSION=1.13.6
# Fri, 27 Jan 2023 23:49:39 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.6 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:49:40 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:49:40 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:49:47 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:49:49 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:49:50 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:49:50 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:49:51 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:49:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:49:51 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:49:52 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:49:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:49:52 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97c7b303342ec3c1020083aca0c889926901c707a72f381fb45b8bf4a8f9af3`  
		Last Modified: Fri, 27 Jan 2023 23:50:59 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00dc1d0dacc88893374cbddfd6562aa9ee5ce3a7a5b79b40729a87bb800adce5`  
		Last Modified: Fri, 27 Jan 2023 23:51:06 GMT  
		Size: 47.4 MB (47355800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15047983587587598daf6346d9c51bab950842d83992a2fe429096088c50bb2b`  
		Last Modified: Fri, 27 Jan 2023 23:50:59 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00772305a57e112487b444eb9a5a43aef922856791463dc85b5f087861fea169`  
		Last Modified: Fri, 27 Jan 2023 23:50:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1617a51f02286e7afa91df45cd04ddf4caea2609723efad81565c618fb133378`  
		Last Modified: Fri, 27 Jan 2023 23:50:59 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:7e8c03354815e336f928b97f8fedbce37e1f00b784de299ee8b5b9dbf0be0d7f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49473887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff8ed06dbdf9183dc2a9e035c48aedd1ed866bc3b471626c7883251874da45a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:46 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Thu, 10 Nov 2022 20:39:46 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:43:50 GMT
ARG CONSUL_VERSION=1.13.6
# Fri, 27 Jan 2023 23:43:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.6 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:43:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:43:51 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:43:56 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:43:57 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:43:58 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:43:58 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:43:58 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:43:58 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:43:58 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:43:58 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:43:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:43:58 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbfcce044e6ec1fa2b335bb59bd421f96edd6511ce58dc8d8ff20fa7c3b480c`  
		Last Modified: Fri, 27 Jan 2023 23:44:38 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eebb94d3846bfcc78d0cbd4c8b1048abbcc7ff106da4cba1b1c4419b99e482f`  
		Last Modified: Fri, 27 Jan 2023 23:44:43 GMT  
		Size: 46.8 MB (46752067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4eff9e15ffc198dc467cbff1ffe6156fbd7966e88fea8608dc03b03732ed1d3`  
		Last Modified: Fri, 27 Jan 2023 23:44:38 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63444f3d1368299ffbd410abddddf191e3656cfcf9f923f486f40a84191abbaf`  
		Last Modified: Fri, 27 Jan 2023 23:44:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517d80ba16447b1667536d7d146384b0020486c3a267e348c120dc72f407d204`  
		Last Modified: Fri, 27 Jan 2023 23:44:38 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13` - linux; 386

```console
$ docker pull consul@sha256:5d91c59468d6f3da632239d73e99025203b62d2e73f7c46087bba643cd263910
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51099757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c4a04c95e65e42597c9414ed6068b3253d1c7cd2c1acbd2eb131720f7533ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:47 GMT
ADD file:d51bb92de86c49ee5486066d12194be78c8b9a8452c44577e2dfeef1945a0138 in / 
# Tue, 09 Aug 2022 17:38:47 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:40:49 GMT
ARG CONSUL_VERSION=1.13.6
# Fri, 27 Jan 2023 23:40:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.6 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:40:51 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:40:52 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:40:59 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:41:00 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:41:01 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:41:02 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:41:03 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:41:04 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:41:05 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:41:07 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:41:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:41:08 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f8c6eeaa55b0f135b7fddb3d7745a98ca4d8f06d2898611234b9ef99e1183073`  
		Last Modified: Tue, 09 Aug 2022 17:39:50 GMT  
		Size: 2.8 MB (2828516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38596db7ab094f0c4c47f862ff3e9c6dfed9d275c7a2e97fa796d6e17cd7f246`  
		Last Modified: Fri, 27 Jan 2023 23:42:14 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d237a22ce9c08a4c923a52f8f5b4f68c58bc377cebc35ce534bb5b068abd4bd0`  
		Last Modified: Fri, 27 Jan 2023 23:42:20 GMT  
		Size: 48.3 MB (48267915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebd73a2af60e935c0cf453e366789fbf347a6ee7f4ae3212c26f8879631f8da`  
		Last Modified: Fri, 27 Jan 2023 23:42:14 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd3ef40a646dbff4bd30525d0d3ff8234a754a3d0f8f14c4a19b780606cdd12`  
		Last Modified: Fri, 27 Jan 2023 23:42:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c6fedd30a29236331b5c20f7a18294f9da110963c561adf076bafc5b8c073d`  
		Last Modified: Fri, 27 Jan 2023 23:42:15 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.13.6`

```console
$ docker pull consul@sha256:f0461a3eec0fa3dc8a86e18a2a19d92a8eb638c74a04d8d1f3b5a1d5253a0e70
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
$ docker pull consul@sha256:9a913e7911c871050287166bb381b20bc815fe3231f31c3df3f2710d29dd4c2c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.0 MB (49990254 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a6e139e945cd30c3ae467f02c04cc501d7addc6123cb6bc1bef930ccc47c4b9a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 10 Nov 2022 20:49:36 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Thu, 10 Nov 2022 20:49:36 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:49:39 GMT
ARG CONSUL_VERSION=1.13.6
# Fri, 27 Jan 2023 23:49:39 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.6 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:49:40 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:49:40 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:49:47 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:49:49 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:49:50 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:49:50 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:49:51 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:49:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:49:51 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:49:52 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:49:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:49:52 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d97c7b303342ec3c1020083aca0c889926901c707a72f381fb45b8bf4a8f9af3`  
		Last Modified: Fri, 27 Jan 2023 23:50:59 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00dc1d0dacc88893374cbddfd6562aa9ee5ce3a7a5b79b40729a87bb800adce5`  
		Last Modified: Fri, 27 Jan 2023 23:51:06 GMT  
		Size: 47.4 MB (47355800 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15047983587587598daf6346d9c51bab950842d83992a2fe429096088c50bb2b`  
		Last Modified: Fri, 27 Jan 2023 23:50:59 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00772305a57e112487b444eb9a5a43aef922856791463dc85b5f087861fea169`  
		Last Modified: Fri, 27 Jan 2023 23:50:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1617a51f02286e7afa91df45cd04ddf4caea2609723efad81565c618fb133378`  
		Last Modified: Fri, 27 Jan 2023 23:50:59 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13.6` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:7e8c03354815e336f928b97f8fedbce37e1f00b784de299ee8b5b9dbf0be0d7f
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49473887 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:eff8ed06dbdf9183dc2a9e035c48aedd1ed866bc3b471626c7883251874da45a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:46 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Thu, 10 Nov 2022 20:39:46 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:43:50 GMT
ARG CONSUL_VERSION=1.13.6
# Fri, 27 Jan 2023 23:43:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.6 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:43:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:43:51 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:43:56 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:43:57 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:43:58 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:43:58 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:43:58 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:43:58 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:43:58 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:43:58 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:43:58 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:43:58 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fbbfcce044e6ec1fa2b335bb59bd421f96edd6511ce58dc8d8ff20fa7c3b480c`  
		Last Modified: Fri, 27 Jan 2023 23:44:38 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9eebb94d3846bfcc78d0cbd4c8b1048abbcc7ff106da4cba1b1c4419b99e482f`  
		Last Modified: Fri, 27 Jan 2023 23:44:43 GMT  
		Size: 46.8 MB (46752067 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4eff9e15ffc198dc467cbff1ffe6156fbd7966e88fea8608dc03b03732ed1d3`  
		Last Modified: Fri, 27 Jan 2023 23:44:38 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63444f3d1368299ffbd410abddddf191e3656cfcf9f923f486f40a84191abbaf`  
		Last Modified: Fri, 27 Jan 2023 23:44:38 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:517d80ba16447b1667536d7d146384b0020486c3a267e348c120dc72f407d204`  
		Last Modified: Fri, 27 Jan 2023 23:44:38 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13.6` - linux; 386

```console
$ docker pull consul@sha256:5d91c59468d6f3da632239d73e99025203b62d2e73f7c46087bba643cd263910
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.1 MB (51099757 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:71c4a04c95e65e42597c9414ed6068b3253d1c7cd2c1acbd2eb131720f7533ba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:47 GMT
ADD file:d51bb92de86c49ee5486066d12194be78c8b9a8452c44577e2dfeef1945a0138 in / 
# Tue, 09 Aug 2022 17:38:47 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:40:49 GMT
ARG CONSUL_VERSION=1.13.6
# Fri, 27 Jan 2023 23:40:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.6 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:40:51 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:40:52 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:40:59 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:41:00 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:41:01 GMT
# ARGS: CONSUL_VERSION=1.13.6
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:41:02 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:41:03 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:41:04 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:41:05 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:41:07 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:41:07 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:41:08 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f8c6eeaa55b0f135b7fddb3d7745a98ca4d8f06d2898611234b9ef99e1183073`  
		Last Modified: Tue, 09 Aug 2022 17:39:50 GMT  
		Size: 2.8 MB (2828516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38596db7ab094f0c4c47f862ff3e9c6dfed9d275c7a2e97fa796d6e17cd7f246`  
		Last Modified: Fri, 27 Jan 2023 23:42:14 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d237a22ce9c08a4c923a52f8f5b4f68c58bc377cebc35ce534bb5b068abd4bd0`  
		Last Modified: Fri, 27 Jan 2023 23:42:20 GMT  
		Size: 48.3 MB (48267915 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ebd73a2af60e935c0cf453e366789fbf347a6ee7f4ae3212c26f8879631f8da`  
		Last Modified: Fri, 27 Jan 2023 23:42:14 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3dd3ef40a646dbff4bd30525d0d3ff8234a754a3d0f8f14c4a19b780606cdd12`  
		Last Modified: Fri, 27 Jan 2023 23:42:15 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26c6fedd30a29236331b5c20f7a18294f9da110963c561adf076bafc5b8c073d`  
		Last Modified: Fri, 27 Jan 2023 23:42:15 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.14`

```console
$ docker pull consul@sha256:16cf26cb9bec8a45ff1c98906d41446f62197e9349fd50505ade6ebe842472c2
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
$ docker pull consul@sha256:a5159cea5355bfe83a0b0dbf4a78144ebf84cef0d582315f9f6e131f75ef6b47
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53712449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:482adf681c047e4fd9c5fc429b3efa4e0596beab8f5f0fb6f206788faee14a98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 10 Nov 2022 20:49:36 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Thu, 10 Nov 2022 20:49:36 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:49:22 GMT
ARG CONSUL_VERSION=1.14.4
# Fri, 27 Jan 2023 23:49:22 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:49:22 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:49:23 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:49:30 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:49:31 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:49:32 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:49:32 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:49:32 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:49:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:49:32 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:49:33 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:49:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:49:33 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e476de1e832ca208c00529853e398b34cffa335d39d60e3effab8e79b5e3aa4`  
		Last Modified: Fri, 27 Jan 2023 23:50:37 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5be245177f11ce028b40de290a24155c937901314a3bda85d4c3d75db37390`  
		Last Modified: Fri, 27 Jan 2023 23:50:44 GMT  
		Size: 51.1 MB (51077996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4890650d5428ae04892a83c2d028fce6d6ed861aa33c16d225d5e7e7e14ec86f`  
		Last Modified: Fri, 27 Jan 2023 23:50:37 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9a2fe3d8dde774668aa123b1088b34a9ee4f1350178674cb3247bebd4bc467`  
		Last Modified: Fri, 27 Jan 2023 23:50:37 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a2535e1679d48e07c04072e491606782210cb9c60c61c243f60fa09181e602`  
		Last Modified: Fri, 27 Jan 2023 23:50:36 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:25266128565c7b6e3e846da51729d7d630c32194ce7d0e5e0282e23d6de58d8c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53138314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0a925c10e880415cd0bf47b624a9965d234ba8cecc79645e6ce1c1402e3f75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:46 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Thu, 10 Nov 2022 20:39:46 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:43:39 GMT
ARG CONSUL_VERSION=1.14.4
# Fri, 27 Jan 2023 23:43:39 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:43:39 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:43:39 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:43:45 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:43:46 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:43:47 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:43:47 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:43:47 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:43:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:43:47 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:43:47 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:43:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:43:48 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab0af25db5d09570fa024e21e5f3889a1cde79dff4e5285c22e6d165e7933ba`  
		Last Modified: Fri, 27 Jan 2023 23:44:22 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50002003933b71d9f66367fa318f42256c6ee5560988866d470e81ac215595d9`  
		Last Modified: Fri, 27 Jan 2023 23:44:27 GMT  
		Size: 50.4 MB (50416492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a351fb9de957733e0567673e9801f4af220d22068dd7a173968fbc0b9a24ffda`  
		Last Modified: Fri, 27 Jan 2023 23:44:22 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df9ae926082d6607053e3064d3b06057d1e53e9766c39af5f4c411f6432d60d`  
		Last Modified: Fri, 27 Jan 2023 23:44:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15340828b065d4ca03533873ff7108f17fc4f57d0d5106e331d5d3fdbb1f9dad`  
		Last Modified: Fri, 27 Jan 2023 23:44:22 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14` - linux; 386

```console
$ docker pull consul@sha256:3fbbb7fedfdd3737528c99af7ef00e96cde537ea5f26c63871f44f92e025241b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55101894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69cc5bdc8849c8ef31324c9c12eb6daacd511f5d7be69e42cde12d2113cb555`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:47 GMT
ADD file:d51bb92de86c49ee5486066d12194be78c8b9a8452c44577e2dfeef1945a0138 in / 
# Tue, 09 Aug 2022 17:38:47 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:40:27 GMT
ARG CONSUL_VERSION=1.14.4
# Fri, 27 Jan 2023 23:40:27 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:40:28 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:40:29 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:40:36 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:40:37 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:40:38 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:40:39 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:40:40 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:40:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:40:42 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:40:44 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:40:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:40:45 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f8c6eeaa55b0f135b7fddb3d7745a98ca4d8f06d2898611234b9ef99e1183073`  
		Last Modified: Tue, 09 Aug 2022 17:39:50 GMT  
		Size: 2.8 MB (2828516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5135c4eb22aad12b652fcf42d7ff50d71e245601a528a20e6483d981d7d00f4c`  
		Last Modified: Fri, 27 Jan 2023 23:41:56 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86477d176b878273e606d8ed24230277f2ee3588150bd87be77b592f581b582`  
		Last Modified: Fri, 27 Jan 2023 23:42:01 GMT  
		Size: 52.3 MB (52270054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70068056f281ee2c4e0d71ec5bb16fb8884af183bb25e41c825d49f05d35bda1`  
		Last Modified: Fri, 27 Jan 2023 23:41:56 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429794b926e291861d73c622d7d8762fdc4a3eda01f0f7920f9be539ea525ff5`  
		Last Modified: Fri, 27 Jan 2023 23:41:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f290e689b3f673aeadba029fcedc8830b16b171e6870134204d3972817c3ae4`  
		Last Modified: Fri, 27 Jan 2023 23:41:56 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.14.4`

```console
$ docker pull consul@sha256:16cf26cb9bec8a45ff1c98906d41446f62197e9349fd50505ade6ebe842472c2
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
$ docker pull consul@sha256:a5159cea5355bfe83a0b0dbf4a78144ebf84cef0d582315f9f6e131f75ef6b47
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53712449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:482adf681c047e4fd9c5fc429b3efa4e0596beab8f5f0fb6f206788faee14a98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 10 Nov 2022 20:49:36 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Thu, 10 Nov 2022 20:49:36 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:49:22 GMT
ARG CONSUL_VERSION=1.14.4
# Fri, 27 Jan 2023 23:49:22 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:49:22 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:49:23 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:49:30 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:49:31 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:49:32 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:49:32 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:49:32 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:49:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:49:32 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:49:33 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:49:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:49:33 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e476de1e832ca208c00529853e398b34cffa335d39d60e3effab8e79b5e3aa4`  
		Last Modified: Fri, 27 Jan 2023 23:50:37 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5be245177f11ce028b40de290a24155c937901314a3bda85d4c3d75db37390`  
		Last Modified: Fri, 27 Jan 2023 23:50:44 GMT  
		Size: 51.1 MB (51077996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4890650d5428ae04892a83c2d028fce6d6ed861aa33c16d225d5e7e7e14ec86f`  
		Last Modified: Fri, 27 Jan 2023 23:50:37 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9a2fe3d8dde774668aa123b1088b34a9ee4f1350178674cb3247bebd4bc467`  
		Last Modified: Fri, 27 Jan 2023 23:50:37 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a2535e1679d48e07c04072e491606782210cb9c60c61c243f60fa09181e602`  
		Last Modified: Fri, 27 Jan 2023 23:50:36 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14.4` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:25266128565c7b6e3e846da51729d7d630c32194ce7d0e5e0282e23d6de58d8c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53138314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0a925c10e880415cd0bf47b624a9965d234ba8cecc79645e6ce1c1402e3f75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:46 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Thu, 10 Nov 2022 20:39:46 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:43:39 GMT
ARG CONSUL_VERSION=1.14.4
# Fri, 27 Jan 2023 23:43:39 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:43:39 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:43:39 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:43:45 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:43:46 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:43:47 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:43:47 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:43:47 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:43:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:43:47 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:43:47 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:43:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:43:48 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab0af25db5d09570fa024e21e5f3889a1cde79dff4e5285c22e6d165e7933ba`  
		Last Modified: Fri, 27 Jan 2023 23:44:22 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50002003933b71d9f66367fa318f42256c6ee5560988866d470e81ac215595d9`  
		Last Modified: Fri, 27 Jan 2023 23:44:27 GMT  
		Size: 50.4 MB (50416492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a351fb9de957733e0567673e9801f4af220d22068dd7a173968fbc0b9a24ffda`  
		Last Modified: Fri, 27 Jan 2023 23:44:22 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df9ae926082d6607053e3064d3b06057d1e53e9766c39af5f4c411f6432d60d`  
		Last Modified: Fri, 27 Jan 2023 23:44:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15340828b065d4ca03533873ff7108f17fc4f57d0d5106e331d5d3fdbb1f9dad`  
		Last Modified: Fri, 27 Jan 2023 23:44:22 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14.4` - linux; 386

```console
$ docker pull consul@sha256:3fbbb7fedfdd3737528c99af7ef00e96cde537ea5f26c63871f44f92e025241b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55101894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69cc5bdc8849c8ef31324c9c12eb6daacd511f5d7be69e42cde12d2113cb555`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:47 GMT
ADD file:d51bb92de86c49ee5486066d12194be78c8b9a8452c44577e2dfeef1945a0138 in / 
# Tue, 09 Aug 2022 17:38:47 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:40:27 GMT
ARG CONSUL_VERSION=1.14.4
# Fri, 27 Jan 2023 23:40:27 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:40:28 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:40:29 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:40:36 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:40:37 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:40:38 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:40:39 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:40:40 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:40:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:40:42 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:40:44 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:40:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:40:45 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f8c6eeaa55b0f135b7fddb3d7745a98ca4d8f06d2898611234b9ef99e1183073`  
		Last Modified: Tue, 09 Aug 2022 17:39:50 GMT  
		Size: 2.8 MB (2828516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5135c4eb22aad12b652fcf42d7ff50d71e245601a528a20e6483d981d7d00f4c`  
		Last Modified: Fri, 27 Jan 2023 23:41:56 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86477d176b878273e606d8ed24230277f2ee3588150bd87be77b592f581b582`  
		Last Modified: Fri, 27 Jan 2023 23:42:01 GMT  
		Size: 52.3 MB (52270054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70068056f281ee2c4e0d71ec5bb16fb8884af183bb25e41c825d49f05d35bda1`  
		Last Modified: Fri, 27 Jan 2023 23:41:56 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429794b926e291861d73c622d7d8762fdc4a3eda01f0f7920f9be539ea525ff5`  
		Last Modified: Fri, 27 Jan 2023 23:41:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f290e689b3f673aeadba029fcedc8830b16b171e6870134204d3972817c3ae4`  
		Last Modified: Fri, 27 Jan 2023 23:41:56 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:16cf26cb9bec8a45ff1c98906d41446f62197e9349fd50505ade6ebe842472c2
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
$ docker pull consul@sha256:a5159cea5355bfe83a0b0dbf4a78144ebf84cef0d582315f9f6e131f75ef6b47
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.7 MB (53712449 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:482adf681c047e4fd9c5fc429b3efa4e0596beab8f5f0fb6f206788faee14a98`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 10 Nov 2022 20:49:36 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Thu, 10 Nov 2022 20:49:36 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:49:22 GMT
ARG CONSUL_VERSION=1.14.4
# Fri, 27 Jan 2023 23:49:22 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:49:22 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:49:23 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:49:30 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:49:31 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:49:32 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:49:32 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:49:32 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:49:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:49:32 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:49:33 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:49:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:49:33 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e476de1e832ca208c00529853e398b34cffa335d39d60e3effab8e79b5e3aa4`  
		Last Modified: Fri, 27 Jan 2023 23:50:37 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a5be245177f11ce028b40de290a24155c937901314a3bda85d4c3d75db37390`  
		Last Modified: Fri, 27 Jan 2023 23:50:44 GMT  
		Size: 51.1 MB (51077996 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4890650d5428ae04892a83c2d028fce6d6ed861aa33c16d225d5e7e7e14ec86f`  
		Last Modified: Fri, 27 Jan 2023 23:50:37 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e9a2fe3d8dde774668aa123b1088b34a9ee4f1350178674cb3247bebd4bc467`  
		Last Modified: Fri, 27 Jan 2023 23:50:37 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e2a2535e1679d48e07c04072e491606782210cb9c60c61c243f60fa09181e602`  
		Last Modified: Fri, 27 Jan 2023 23:50:36 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:25266128565c7b6e3e846da51729d7d630c32194ce7d0e5e0282e23d6de58d8c
```

-	Docker Version: 20.10.17
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.1 MB (53138314 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5b0a925c10e880415cd0bf47b624a9965d234ba8cecc79645e6ce1c1402e3f75`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 10 Nov 2022 20:39:46 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Thu, 10 Nov 2022 20:39:46 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:43:39 GMT
ARG CONSUL_VERSION=1.14.4
# Fri, 27 Jan 2023 23:43:39 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:43:39 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:43:39 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:43:45 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:43:46 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:43:47 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:43:47 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:43:47 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:43:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:43:47 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:43:47 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:43:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:43:48 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ab0af25db5d09570fa024e21e5f3889a1cde79dff4e5285c22e6d165e7933ba`  
		Last Modified: Fri, 27 Jan 2023 23:44:22 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50002003933b71d9f66367fa318f42256c6ee5560988866d470e81ac215595d9`  
		Last Modified: Fri, 27 Jan 2023 23:44:27 GMT  
		Size: 50.4 MB (50416492 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a351fb9de957733e0567673e9801f4af220d22068dd7a173968fbc0b9a24ffda`  
		Last Modified: Fri, 27 Jan 2023 23:44:22 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7df9ae926082d6607053e3064d3b06057d1e53e9766c39af5f4c411f6432d60d`  
		Last Modified: Fri, 27 Jan 2023 23:44:22 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15340828b065d4ca03533873ff7108f17fc4f57d0d5106e331d5d3fdbb1f9dad`  
		Last Modified: Fri, 27 Jan 2023 23:44:22 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:3fbbb7fedfdd3737528c99af7ef00e96cde537ea5f26c63871f44f92e025241b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.1 MB (55101894 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e69cc5bdc8849c8ef31324c9c12eb6daacd511f5d7be69e42cde12d2113cb555`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:47 GMT
ADD file:d51bb92de86c49ee5486066d12194be78c8b9a8452c44577e2dfeef1945a0138 in / 
# Tue, 09 Aug 2022 17:38:47 GMT
CMD ["/bin/sh"]
# Fri, 27 Jan 2023 23:40:27 GMT
ARG CONSUL_VERSION=1.14.4
# Fri, 27 Jan 2023 23:40:27 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 27 Jan 2023 23:40:28 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 27 Jan 2023 23:40:29 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 27 Jan 2023 23:40:36 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 27 Jan 2023 23:40:37 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 27 Jan 2023 23:40:38 GMT
# ARGS: CONSUL_VERSION=1.14.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 27 Jan 2023 23:40:39 GMT
VOLUME [/consul/data]
# Fri, 27 Jan 2023 23:40:40 GMT
EXPOSE 8300
# Fri, 27 Jan 2023 23:40:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 27 Jan 2023 23:40:42 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 27 Jan 2023 23:40:44 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 27 Jan 2023 23:40:44 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 27 Jan 2023 23:40:45 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f8c6eeaa55b0f135b7fddb3d7745a98ca4d8f06d2898611234b9ef99e1183073`  
		Last Modified: Tue, 09 Aug 2022 17:39:50 GMT  
		Size: 2.8 MB (2828516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5135c4eb22aad12b652fcf42d7ff50d71e245601a528a20e6483d981d7d00f4c`  
		Last Modified: Fri, 27 Jan 2023 23:41:56 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a86477d176b878273e606d8ed24230277f2ee3588150bd87be77b592f581b582`  
		Last Modified: Fri, 27 Jan 2023 23:42:01 GMT  
		Size: 52.3 MB (52270054 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:70068056f281ee2c4e0d71ec5bb16fb8884af183bb25e41c825d49f05d35bda1`  
		Last Modified: Fri, 27 Jan 2023 23:41:56 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:429794b926e291861d73c622d7d8762fdc4a3eda01f0f7920f9be539ea525ff5`  
		Last Modified: Fri, 27 Jan 2023 23:41:56 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f290e689b3f673aeadba029fcedc8830b16b171e6870134204d3972817c3ae4`  
		Last Modified: Fri, 27 Jan 2023 23:41:56 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
