<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.11`](#consul111)
-	[`consul:1.11.10`](#consul11110)
-	[`consul:1.12`](#consul112)
-	[`consul:1.12.5`](#consul1125)
-	[`consul:1.13`](#consul113)
-	[`consul:1.13.2`](#consul1132)
-	[`consul:latest`](#consullatest)

## `consul:1.11`

```console
$ docker pull consul@sha256:85732997fc8f0b321c66574a687eb48f64a4aa7793f7dd9952d5aa786cbe5b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.11` - linux; amd64

```console
$ docker pull consul@sha256:576d28ac5e237d853da7136dddaad6df4c9aae90fede5c338c00cf9bcc19c026
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44061895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc989be13aaf736971280b2fd27f992e067cc9611d4db0583a73ef52e0faf85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Fri, 23 Sep 2022 00:19:28 GMT
ARG CONSUL_VERSION=1.11.10
# Fri, 23 Sep 2022 00:19:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.10 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 23 Sep 2022 00:19:28 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Sep 2022 00:19:29 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Sep 2022 00:19:35 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Sep 2022 00:19:36 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Sep 2022 00:19:36 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Sep 2022 00:19:36 GMT
VOLUME [/consul/data]
# Fri, 23 Sep 2022 00:19:36 GMT
EXPOSE 8300
# Fri, 23 Sep 2022 00:19:37 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Sep 2022 00:19:37 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Sep 2022 00:19:37 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Sep 2022 00:19:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Sep 2022 00:19:37 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165126922ba2a6e341220c760a8c5bec7d43465ff1449b4b9edd1a4af2f45136`  
		Last Modified: Fri, 23 Sep 2022 00:19:52 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3f1607b242f75f4c7304cdb9f922d8fd9285e258215c2f898a09f5f82cd305`  
		Last Modified: Fri, 23 Sep 2022 00:19:57 GMT  
		Size: 41.2 MB (41234995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc47fb896ac60a969026ba146b54838d503615fb5982cde0ecce4a815ee2e72f`  
		Last Modified: Fri, 23 Sep 2022 00:19:52 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804c6d5a993f1f778bda4ccd366e31ce6b16e6143d148634819e6a57e77b5c48`  
		Last Modified: Fri, 23 Sep 2022 00:19:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e933c1b15040eeac3cbb2f4971c7d7050318ae3121ce06b070bf5fc580569b`  
		Last Modified: Fri, 23 Sep 2022 00:19:52 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11` - linux; arm variant v6

```console
$ docker pull consul@sha256:346953b67a44b228f24132746b6acb9abc00bd9b21aee1c886e3df93829f1b27
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41815492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2f4edafc851a562b3d8fd0459ac2a4fda86eb9b5c4cb5c540ddf711391367e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Fri, 23 Sep 2022 00:49:32 GMT
ARG CONSUL_VERSION=1.11.10
# Fri, 23 Sep 2022 00:49:32 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.10 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 23 Sep 2022 00:49:32 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Sep 2022 00:49:33 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Sep 2022 00:49:40 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Sep 2022 00:49:41 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Sep 2022 00:49:42 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Sep 2022 00:49:42 GMT
VOLUME [/consul/data]
# Fri, 23 Sep 2022 00:49:42 GMT
EXPOSE 8300
# Fri, 23 Sep 2022 00:49:42 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Sep 2022 00:49:42 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Sep 2022 00:49:43 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Sep 2022 00:49:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Sep 2022 00:49:43 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a11e51ca536f1ed29b2d47a56bee15e886fee7d83607d7896338cda72f7a8a`  
		Last Modified: Fri, 23 Sep 2022 00:50:14 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafba2110be1c3296192eaa81253498fc6ad6afa99ee31dea22448a50d1eb336`  
		Last Modified: Fri, 23 Sep 2022 00:50:21 GMT  
		Size: 39.2 MB (39180982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450434008f4c955801ad64d4d127368af0b21d0af49962ad5aadcf040434a427`  
		Last Modified: Fri, 23 Sep 2022 00:50:14 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edff2d413904899215a021cc17cbb3eb23dcacef1cfa7876e981ab3d11d0e43e`  
		Last Modified: Fri, 23 Sep 2022 00:50:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35dc41f713534e327fce3064a405a7eb009e50a05448c655ddbd0cbe51cb16ce`  
		Last Modified: Fri, 23 Sep 2022 00:50:14 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:49ab196c4415641a729bb1596cd03de4942ab1ca896ffa9fc5885b9df4e596df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41641262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153bc4e485094243de90358adb3b271cbb4657faf41a78e18be918b940a77d8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Fri, 23 Sep 2022 00:39:36 GMT
ARG CONSUL_VERSION=1.11.10
# Fri, 23 Sep 2022 00:39:37 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.10 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 23 Sep 2022 00:39:38 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Sep 2022 00:39:39 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Sep 2022 00:39:46 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Sep 2022 00:39:46 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Sep 2022 00:39:47 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Sep 2022 00:39:48 GMT
VOLUME [/consul/data]
# Fri, 23 Sep 2022 00:39:49 GMT
EXPOSE 8300
# Fri, 23 Sep 2022 00:39:50 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Sep 2022 00:39:51 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Sep 2022 00:39:53 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Sep 2022 00:39:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Sep 2022 00:39:54 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dcfe4fb9ab3e72523b7e0d69dbb88c4b35ed410e5dc35ec900515a3e66d75f`  
		Last Modified: Fri, 23 Sep 2022 00:40:18 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd90294a82ec3de981868a9344318fc8d07b457e88a943a7b2e3bc482a005d8`  
		Last Modified: Fri, 23 Sep 2022 00:40:23 GMT  
		Size: 38.9 MB (38919502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc2d6b4340880f81205986027d763759d32a7a23735b92ca401cc3b37719190`  
		Last Modified: Fri, 23 Sep 2022 00:40:18 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2109e54013ef86ce8e2c9332f1e81e2ba19b16cbb52b51b27f5a0130fb46ba53`  
		Last Modified: Fri, 23 Sep 2022 00:40:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e483869899cb3127f01f82dfd05e59f634cbc81f05decdbd2fdd7568fe95182f`  
		Last Modified: Fri, 23 Sep 2022 00:40:18 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11` - linux; 386

```console
$ docker pull consul@sha256:33332e9e4ca8a884c70e06b6fefd0a6be255e0d6c3cd20525cb4b441c7d3de52
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42872299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825a6c4124fea9f30ebb9ccba787ecbb914566211a58c6c10155a25112bd6d06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:47 GMT
ADD file:d51bb92de86c49ee5486066d12194be78c8b9a8452c44577e2dfeef1945a0138 in / 
# Tue, 09 Aug 2022 17:38:47 GMT
CMD ["/bin/sh"]
# Fri, 23 Sep 2022 00:38:32 GMT
ARG CONSUL_VERSION=1.11.10
# Fri, 23 Sep 2022 00:38:33 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.10 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 23 Sep 2022 00:38:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Sep 2022 00:38:35 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Sep 2022 00:38:43 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Sep 2022 00:38:43 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Sep 2022 00:38:44 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Sep 2022 00:38:45 GMT
VOLUME [/consul/data]
# Fri, 23 Sep 2022 00:38:46 GMT
EXPOSE 8300
# Fri, 23 Sep 2022 00:38:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Sep 2022 00:38:48 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Sep 2022 00:38:50 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Sep 2022 00:38:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Sep 2022 00:38:51 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f8c6eeaa55b0f135b7fddb3d7745a98ca4d8f06d2898611234b9ef99e1183073`  
		Last Modified: Tue, 09 Aug 2022 17:39:50 GMT  
		Size: 2.8 MB (2828516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bba52b48d7ee5509bece0dfad382976440615cd4548f97a6040a267724f5b3`  
		Last Modified: Fri, 23 Sep 2022 00:39:18 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefe6a7df86cecb76741ed287e9f1adfcebe6fc18e65af0eb5b875bdc111748a`  
		Last Modified: Fri, 23 Sep 2022 00:39:22 GMT  
		Size: 40.0 MB (40040460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a823dd5d5253e2a9cf0204ee977e97df42769856e0891a5fa238d2ae31c51d`  
		Last Modified: Fri, 23 Sep 2022 00:39:18 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55209beba3399fd54baeac1a853b7a37144fd186d2a301b5133a4eebb1fa0cdd`  
		Last Modified: Fri, 23 Sep 2022 00:39:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9db084042118a58cf87bbb1c77081c7e932388d5c146d3638422edd84b9ab3a`  
		Last Modified: Fri, 23 Sep 2022 00:39:18 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.11.10`

```console
$ docker pull consul@sha256:85732997fc8f0b321c66574a687eb48f64a4aa7793f7dd9952d5aa786cbe5b2c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.11.10` - linux; amd64

```console
$ docker pull consul@sha256:576d28ac5e237d853da7136dddaad6df4c9aae90fede5c338c00cf9bcc19c026
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **44.1 MB (44061895 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dcc989be13aaf736971280b2fd27f992e067cc9611d4db0583a73ef52e0faf85`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Fri, 23 Sep 2022 00:19:28 GMT
ARG CONSUL_VERSION=1.11.10
# Fri, 23 Sep 2022 00:19:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.10 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 23 Sep 2022 00:19:28 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Sep 2022 00:19:29 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Sep 2022 00:19:35 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Sep 2022 00:19:36 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Sep 2022 00:19:36 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Sep 2022 00:19:36 GMT
VOLUME [/consul/data]
# Fri, 23 Sep 2022 00:19:36 GMT
EXPOSE 8300
# Fri, 23 Sep 2022 00:19:37 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Sep 2022 00:19:37 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Sep 2022 00:19:37 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Sep 2022 00:19:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Sep 2022 00:19:37 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:165126922ba2a6e341220c760a8c5bec7d43465ff1449b4b9edd1a4af2f45136`  
		Last Modified: Fri, 23 Sep 2022 00:19:52 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3f1607b242f75f4c7304cdb9f922d8fd9285e258215c2f898a09f5f82cd305`  
		Last Modified: Fri, 23 Sep 2022 00:19:57 GMT  
		Size: 41.2 MB (41234995 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc47fb896ac60a969026ba146b54838d503615fb5982cde0ecce4a815ee2e72f`  
		Last Modified: Fri, 23 Sep 2022 00:19:52 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:804c6d5a993f1f778bda4ccd366e31ce6b16e6143d148634819e6a57e77b5c48`  
		Last Modified: Fri, 23 Sep 2022 00:19:52 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7e933c1b15040eeac3cbb2f4971c7d7050318ae3121ce06b070bf5fc580569b`  
		Last Modified: Fri, 23 Sep 2022 00:19:52 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.10` - linux; arm variant v6

```console
$ docker pull consul@sha256:346953b67a44b228f24132746b6acb9abc00bd9b21aee1c886e3df93829f1b27
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41815492 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e2f4edafc851a562b3d8fd0459ac2a4fda86eb9b5c4cb5c540ddf711391367e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Fri, 23 Sep 2022 00:49:32 GMT
ARG CONSUL_VERSION=1.11.10
# Fri, 23 Sep 2022 00:49:32 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.10 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 23 Sep 2022 00:49:32 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Sep 2022 00:49:33 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Sep 2022 00:49:40 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Sep 2022 00:49:41 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Sep 2022 00:49:42 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Sep 2022 00:49:42 GMT
VOLUME [/consul/data]
# Fri, 23 Sep 2022 00:49:42 GMT
EXPOSE 8300
# Fri, 23 Sep 2022 00:49:42 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Sep 2022 00:49:42 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Sep 2022 00:49:43 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Sep 2022 00:49:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Sep 2022 00:49:43 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01a11e51ca536f1ed29b2d47a56bee15e886fee7d83607d7896338cda72f7a8a`  
		Last Modified: Fri, 23 Sep 2022 00:50:14 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dafba2110be1c3296192eaa81253498fc6ad6afa99ee31dea22448a50d1eb336`  
		Last Modified: Fri, 23 Sep 2022 00:50:21 GMT  
		Size: 39.2 MB (39180982 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:450434008f4c955801ad64d4d127368af0b21d0af49962ad5aadcf040434a427`  
		Last Modified: Fri, 23 Sep 2022 00:50:14 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:edff2d413904899215a021cc17cbb3eb23dcacef1cfa7876e981ab3d11d0e43e`  
		Last Modified: Fri, 23 Sep 2022 00:50:14 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35dc41f713534e327fce3064a405a7eb009e50a05448c655ddbd0cbe51cb16ce`  
		Last Modified: Fri, 23 Sep 2022 00:50:14 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.10` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:49ab196c4415641a729bb1596cd03de4942ab1ca896ffa9fc5885b9df4e596df
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.6 MB (41641262 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:153bc4e485094243de90358adb3b271cbb4657faf41a78e18be918b940a77d8c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Fri, 23 Sep 2022 00:39:36 GMT
ARG CONSUL_VERSION=1.11.10
# Fri, 23 Sep 2022 00:39:37 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.10 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 23 Sep 2022 00:39:38 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Sep 2022 00:39:39 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Sep 2022 00:39:46 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Sep 2022 00:39:46 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Sep 2022 00:39:47 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Sep 2022 00:39:48 GMT
VOLUME [/consul/data]
# Fri, 23 Sep 2022 00:39:49 GMT
EXPOSE 8300
# Fri, 23 Sep 2022 00:39:50 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Sep 2022 00:39:51 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Sep 2022 00:39:53 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Sep 2022 00:39:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Sep 2022 00:39:54 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49dcfe4fb9ab3e72523b7e0d69dbb88c4b35ed410e5dc35ec900515a3e66d75f`  
		Last Modified: Fri, 23 Sep 2022 00:40:18 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fd90294a82ec3de981868a9344318fc8d07b457e88a943a7b2e3bc482a005d8`  
		Last Modified: Fri, 23 Sep 2022 00:40:23 GMT  
		Size: 38.9 MB (38919502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1fc2d6b4340880f81205986027d763759d32a7a23735b92ca401cc3b37719190`  
		Last Modified: Fri, 23 Sep 2022 00:40:18 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2109e54013ef86ce8e2c9332f1e81e2ba19b16cbb52b51b27f5a0130fb46ba53`  
		Last Modified: Fri, 23 Sep 2022 00:40:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e483869899cb3127f01f82dfd05e59f634cbc81f05decdbd2fdd7568fe95182f`  
		Last Modified: Fri, 23 Sep 2022 00:40:18 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.10` - linux; 386

```console
$ docker pull consul@sha256:33332e9e4ca8a884c70e06b6fefd0a6be255e0d6c3cd20525cb4b441c7d3de52
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.9 MB (42872299 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:825a6c4124fea9f30ebb9ccba787ecbb914566211a58c6c10155a25112bd6d06`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:47 GMT
ADD file:d51bb92de86c49ee5486066d12194be78c8b9a8452c44577e2dfeef1945a0138 in / 
# Tue, 09 Aug 2022 17:38:47 GMT
CMD ["/bin/sh"]
# Fri, 23 Sep 2022 00:38:32 GMT
ARG CONSUL_VERSION=1.11.10
# Fri, 23 Sep 2022 00:38:33 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.10 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 23 Sep 2022 00:38:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Sep 2022 00:38:35 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Sep 2022 00:38:43 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Sep 2022 00:38:43 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Sep 2022 00:38:44 GMT
# ARGS: CONSUL_VERSION=1.11.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Sep 2022 00:38:45 GMT
VOLUME [/consul/data]
# Fri, 23 Sep 2022 00:38:46 GMT
EXPOSE 8300
# Fri, 23 Sep 2022 00:38:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Sep 2022 00:38:48 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Sep 2022 00:38:50 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Sep 2022 00:38:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Sep 2022 00:38:51 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f8c6eeaa55b0f135b7fddb3d7745a98ca4d8f06d2898611234b9ef99e1183073`  
		Last Modified: Tue, 09 Aug 2022 17:39:50 GMT  
		Size: 2.8 MB (2828516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35bba52b48d7ee5509bece0dfad382976440615cd4548f97a6040a267724f5b3`  
		Last Modified: Fri, 23 Sep 2022 00:39:18 GMT  
		Size: 1.2 KB (1240 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cefe6a7df86cecb76741ed287e9f1adfcebe6fc18e65af0eb5b875bdc111748a`  
		Last Modified: Fri, 23 Sep 2022 00:39:22 GMT  
		Size: 40.0 MB (40040460 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47a823dd5d5253e2a9cf0204ee977e97df42769856e0891a5fa238d2ae31c51d`  
		Last Modified: Fri, 23 Sep 2022 00:39:18 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55209beba3399fd54baeac1a853b7a37144fd186d2a301b5133a4eebb1fa0cdd`  
		Last Modified: Fri, 23 Sep 2022 00:39:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d9db084042118a58cf87bbb1c77081c7e932388d5c146d3638422edd84b9ab3a`  
		Last Modified: Fri, 23 Sep 2022 00:39:18 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.12`

```console
$ docker pull consul@sha256:8cfdd5bd6020ca6ccb462ad0f45e4fa851f5a7866e75aecd2fa49a0750f6b4bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.12` - linux; amd64

```console
$ docker pull consul@sha256:00c896caa466082c3ad46f8342370d329704e80745ead2bb083fdafcc8fd6faa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49593540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d85f8aed8fcaeeca2b3a4d22e9fa16c053abc051f987231c5659d7b0ebf595`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Wed, 21 Sep 2022 18:19:43 GMT
ARG CONSUL_VERSION=1.12.5
# Wed, 21 Sep 2022 18:19:43 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 21 Sep 2022 18:19:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 21 Sep 2022 18:19:44 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 21 Sep 2022 18:19:49 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 21 Sep 2022 18:19:50 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 21 Sep 2022 18:19:51 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 21 Sep 2022 18:19:51 GMT
VOLUME [/consul/data]
# Wed, 21 Sep 2022 18:19:51 GMT
EXPOSE 8300
# Wed, 21 Sep 2022 18:19:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 21 Sep 2022 18:19:51 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 21 Sep 2022 18:19:52 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Sep 2022 18:19:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Sep 2022 18:19:52 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd8eae600c02f9cd19623833d4a743b847e4c2a5609c013ad60983c90bd9706`  
		Last Modified: Wed, 21 Sep 2022 18:20:35 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfd094a20f14a488fa1a575040130bcf7474be62bd6d60e4b3c1c172150b72b`  
		Last Modified: Wed, 21 Sep 2022 18:20:41 GMT  
		Size: 46.8 MB (46766648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2960448de0c76ca4e56ebd1124ca8253f2a397e8d16e0e1bee39ebf0e484f6`  
		Last Modified: Wed, 21 Sep 2022 18:20:35 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e30a822aef020ea0bee951ccc22a7d54e9d4fe14c42f6c6ef4ef9881ea0a953`  
		Last Modified: Wed, 21 Sep 2022 18:20:35 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e1d847b64430cfb47b8685357a86d088bd7dfe548a140a4a7cca2b568823fc`  
		Last Modified: Wed, 21 Sep 2022 18:20:35 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12` - linux; arm variant v6

```console
$ docker pull consul@sha256:80ed101c7b179c5f9909b22f313362f0e2f27832facee67e7e517d95c47997ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47460255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90762a727f1baee9a3092e2e937cb8ea0319dffab5c88601c0024d7465a34af0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Wed, 21 Sep 2022 17:49:44 GMT
ARG CONSUL_VERSION=1.12.5
# Wed, 21 Sep 2022 17:49:44 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 21 Sep 2022 17:49:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 21 Sep 2022 17:49:45 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 21 Sep 2022 17:49:53 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 21 Sep 2022 17:49:54 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 21 Sep 2022 17:49:54 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 21 Sep 2022 17:49:54 GMT
VOLUME [/consul/data]
# Wed, 21 Sep 2022 17:49:54 GMT
EXPOSE 8300
# Wed, 21 Sep 2022 17:49:55 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 21 Sep 2022 17:49:55 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 21 Sep 2022 17:49:55 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Sep 2022 17:49:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Sep 2022 17:49:55 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c219a9b8facfd460aa0d385b2a107427939acc2b5d1a90c4fff32e78efc6d9fb`  
		Last Modified: Wed, 21 Sep 2022 17:51:06 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf762e67bbc7e95743f5e3bf5434be6c05930194d6a3da57d806626125ba6c4`  
		Last Modified: Wed, 21 Sep 2022 17:51:15 GMT  
		Size: 44.8 MB (44825741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb42b6a4d4cb42aa0270291c490aba724479fc641cfbadf413bde9be4d56b90`  
		Last Modified: Wed, 21 Sep 2022 17:51:06 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21320170ec8d683fbcf0ad9d5e5ef92e297f3d1678aeeaea141d492d8931fb20`  
		Last Modified: Wed, 21 Sep 2022 17:51:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e33de35b3be84bd215518910ea33ef21b3b505af714a05e3a74a67ff1172474`  
		Last Modified: Wed, 21 Sep 2022 17:51:06 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:8e8f271afb41d1d394878ec41d44723f1abfff6a9dfd9ed0c995b591764c353d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47192775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a64cae51a1ce6ba560db52c04b40fbcf8acb07aa40edecf0506e06aa8c41fbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Wed, 21 Sep 2022 17:39:55 GMT
ARG CONSUL_VERSION=1.12.5
# Wed, 21 Sep 2022 17:39:56 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 21 Sep 2022 17:39:57 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 21 Sep 2022 17:39:58 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 21 Sep 2022 17:40:04 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 21 Sep 2022 17:40:05 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 21 Sep 2022 17:40:06 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 21 Sep 2022 17:40:07 GMT
VOLUME [/consul/data]
# Wed, 21 Sep 2022 17:40:08 GMT
EXPOSE 8300
# Wed, 21 Sep 2022 17:40:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 21 Sep 2022 17:40:10 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 21 Sep 2022 17:40:12 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Sep 2022 17:40:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Sep 2022 17:40:13 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5725814cd7393cbf05a9c8f22bc1a9d5da5e0c01cc0ef37c5b049418c4128b`  
		Last Modified: Wed, 21 Sep 2022 17:41:17 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3ecf11a51834d2ab602abc4af3a891ffbd376003af4e9f3b23c2bd702c8728`  
		Last Modified: Wed, 21 Sep 2022 17:41:23 GMT  
		Size: 44.5 MB (44471009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea919de09393eae0302701bb428054cec96c36d43050f86ad3bc2a43e2b67c2`  
		Last Modified: Wed, 21 Sep 2022 17:41:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139ac4388ae9391908781efe3bb30ae556cabf513fb9c74bf4541a98ed90c47b`  
		Last Modified: Wed, 21 Sep 2022 17:41:17 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef91580f4580a96493a2c9d9ecf022c4162af41fb1902a8d1fe5bcb4fcb53ac8`  
		Last Modified: Wed, 21 Sep 2022 17:41:17 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12` - linux; 386

```console
$ docker pull consul@sha256:d03eb8655b8b2df53b4b30dfcb227d405f6ec6ce7f2f2acd1663f5def87d351b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48658944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c32fa7e7efd44d29b63b75e0ee2d580e43a612eab52fcc114a1d70b9b728acb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:47 GMT
ADD file:d51bb92de86c49ee5486066d12194be78c8b9a8452c44577e2dfeef1945a0138 in / 
# Tue, 09 Aug 2022 17:38:47 GMT
CMD ["/bin/sh"]
# Wed, 21 Sep 2022 17:38:53 GMT
ARG CONSUL_VERSION=1.12.5
# Wed, 21 Sep 2022 17:38:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 21 Sep 2022 17:38:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 21 Sep 2022 17:38:56 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 21 Sep 2022 17:39:03 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 21 Sep 2022 17:39:03 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 21 Sep 2022 17:39:04 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 21 Sep 2022 17:39:05 GMT
VOLUME [/consul/data]
# Wed, 21 Sep 2022 17:39:06 GMT
EXPOSE 8300
# Wed, 21 Sep 2022 17:39:07 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 21 Sep 2022 17:39:08 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 21 Sep 2022 17:39:10 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Sep 2022 17:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Sep 2022 17:39:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f8c6eeaa55b0f135b7fddb3d7745a98ca4d8f06d2898611234b9ef99e1183073`  
		Last Modified: Tue, 09 Aug 2022 17:39:50 GMT  
		Size: 2.8 MB (2828516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74732828c2e853c2126024b8fd6dc6baa68f7fdfec22e271dbde40c2b93ce0d`  
		Last Modified: Wed, 21 Sep 2022 17:40:19 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47617cd2d54035423cbd7b4a8756c415126be375b7c1ba6bb0edfcf11eb0c52f`  
		Last Modified: Wed, 21 Sep 2022 17:40:24 GMT  
		Size: 45.8 MB (45827102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999989a8d4a7a21f12c28e8bd53ece7060121d09cf683dd87d5758fb1c249fe9`  
		Last Modified: Wed, 21 Sep 2022 17:40:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791128eac9d9df2c5533c3283a2e40a22160efad74bad6ba909eb9aba4ad31cd`  
		Last Modified: Wed, 21 Sep 2022 17:40:19 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1344da65a6f7d2069d9db1dd131df7aeddee8b4ae62c9ff4279f27dcabe2e8`  
		Last Modified: Wed, 21 Sep 2022 17:40:20 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.12.5`

```console
$ docker pull consul@sha256:8cfdd5bd6020ca6ccb462ad0f45e4fa851f5a7866e75aecd2fa49a0750f6b4bc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.12.5` - linux; amd64

```console
$ docker pull consul@sha256:00c896caa466082c3ad46f8342370d329704e80745ead2bb083fdafcc8fd6faa
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.6 MB (49593540 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0d85f8aed8fcaeeca2b3a4d22e9fa16c053abc051f987231c5659d7b0ebf595`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Wed, 21 Sep 2022 18:19:43 GMT
ARG CONSUL_VERSION=1.12.5
# Wed, 21 Sep 2022 18:19:43 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 21 Sep 2022 18:19:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 21 Sep 2022 18:19:44 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 21 Sep 2022 18:19:49 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 21 Sep 2022 18:19:50 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 21 Sep 2022 18:19:51 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 21 Sep 2022 18:19:51 GMT
VOLUME [/consul/data]
# Wed, 21 Sep 2022 18:19:51 GMT
EXPOSE 8300
# Wed, 21 Sep 2022 18:19:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 21 Sep 2022 18:19:51 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 21 Sep 2022 18:19:52 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Sep 2022 18:19:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Sep 2022 18:19:52 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fd8eae600c02f9cd19623833d4a743b847e4c2a5609c013ad60983c90bd9706`  
		Last Modified: Wed, 21 Sep 2022 18:20:35 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdfd094a20f14a488fa1a575040130bcf7474be62bd6d60e4b3c1c172150b72b`  
		Last Modified: Wed, 21 Sep 2022 18:20:41 GMT  
		Size: 46.8 MB (46766648 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc2960448de0c76ca4e56ebd1124ca8253f2a397e8d16e0e1bee39ebf0e484f6`  
		Last Modified: Wed, 21 Sep 2022 18:20:35 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e30a822aef020ea0bee951ccc22a7d54e9d4fe14c42f6c6ef4ef9881ea0a953`  
		Last Modified: Wed, 21 Sep 2022 18:20:35 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13e1d847b64430cfb47b8685357a86d088bd7dfe548a140a4a7cca2b568823fc`  
		Last Modified: Wed, 21 Sep 2022 18:20:35 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12.5` - linux; arm variant v6

```console
$ docker pull consul@sha256:80ed101c7b179c5f9909b22f313362f0e2f27832facee67e7e517d95c47997ab
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.5 MB (47460255 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:90762a727f1baee9a3092e2e937cb8ea0319dffab5c88601c0024d7465a34af0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Wed, 21 Sep 2022 17:49:44 GMT
ARG CONSUL_VERSION=1.12.5
# Wed, 21 Sep 2022 17:49:44 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 21 Sep 2022 17:49:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 21 Sep 2022 17:49:45 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 21 Sep 2022 17:49:53 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 21 Sep 2022 17:49:54 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 21 Sep 2022 17:49:54 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 21 Sep 2022 17:49:54 GMT
VOLUME [/consul/data]
# Wed, 21 Sep 2022 17:49:54 GMT
EXPOSE 8300
# Wed, 21 Sep 2022 17:49:55 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 21 Sep 2022 17:49:55 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 21 Sep 2022 17:49:55 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Sep 2022 17:49:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Sep 2022 17:49:55 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c219a9b8facfd460aa0d385b2a107427939acc2b5d1a90c4fff32e78efc6d9fb`  
		Last Modified: Wed, 21 Sep 2022 17:51:06 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaf762e67bbc7e95743f5e3bf5434be6c05930194d6a3da57d806626125ba6c4`  
		Last Modified: Wed, 21 Sep 2022 17:51:15 GMT  
		Size: 44.8 MB (44825741 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cb42b6a4d4cb42aa0270291c490aba724479fc641cfbadf413bde9be4d56b90`  
		Last Modified: Wed, 21 Sep 2022 17:51:06 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21320170ec8d683fbcf0ad9d5e5ef92e297f3d1678aeeaea141d492d8931fb20`  
		Last Modified: Wed, 21 Sep 2022 17:51:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e33de35b3be84bd215518910ea33ef21b3b505af714a05e3a74a67ff1172474`  
		Last Modified: Wed, 21 Sep 2022 17:51:06 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12.5` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:8e8f271afb41d1d394878ec41d44723f1abfff6a9dfd9ed0c995b591764c353d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.2 MB (47192775 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9a64cae51a1ce6ba560db52c04b40fbcf8acb07aa40edecf0506e06aa8c41fbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Wed, 21 Sep 2022 17:39:55 GMT
ARG CONSUL_VERSION=1.12.5
# Wed, 21 Sep 2022 17:39:56 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 21 Sep 2022 17:39:57 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 21 Sep 2022 17:39:58 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 21 Sep 2022 17:40:04 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 21 Sep 2022 17:40:05 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 21 Sep 2022 17:40:06 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 21 Sep 2022 17:40:07 GMT
VOLUME [/consul/data]
# Wed, 21 Sep 2022 17:40:08 GMT
EXPOSE 8300
# Wed, 21 Sep 2022 17:40:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 21 Sep 2022 17:40:10 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 21 Sep 2022 17:40:12 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Sep 2022 17:40:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Sep 2022 17:40:13 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba5725814cd7393cbf05a9c8f22bc1a9d5da5e0c01cc0ef37c5b049418c4128b`  
		Last Modified: Wed, 21 Sep 2022 17:41:17 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc3ecf11a51834d2ab602abc4af3a891ffbd376003af4e9f3b23c2bd702c8728`  
		Last Modified: Wed, 21 Sep 2022 17:41:23 GMT  
		Size: 44.5 MB (44471009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ea919de09393eae0302701bb428054cec96c36d43050f86ad3bc2a43e2b67c2`  
		Last Modified: Wed, 21 Sep 2022 17:41:17 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:139ac4388ae9391908781efe3bb30ae556cabf513fb9c74bf4541a98ed90c47b`  
		Last Modified: Wed, 21 Sep 2022 17:41:17 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef91580f4580a96493a2c9d9ecf022c4162af41fb1902a8d1fe5bcb4fcb53ac8`  
		Last Modified: Wed, 21 Sep 2022 17:41:17 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.12.5` - linux; 386

```console
$ docker pull consul@sha256:d03eb8655b8b2df53b4b30dfcb227d405f6ec6ce7f2f2acd1663f5def87d351b
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **48.7 MB (48658944 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3c32fa7e7efd44d29b63b75e0ee2d580e43a612eab52fcc114a1d70b9b728acb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:47 GMT
ADD file:d51bb92de86c49ee5486066d12194be78c8b9a8452c44577e2dfeef1945a0138 in / 
# Tue, 09 Aug 2022 17:38:47 GMT
CMD ["/bin/sh"]
# Wed, 21 Sep 2022 17:38:53 GMT
ARG CONSUL_VERSION=1.12.5
# Wed, 21 Sep 2022 17:38:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.12.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 21 Sep 2022 17:38:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 21 Sep 2022 17:38:56 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 21 Sep 2022 17:39:03 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 21 Sep 2022 17:39:03 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 21 Sep 2022 17:39:04 GMT
# ARGS: CONSUL_VERSION=1.12.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 21 Sep 2022 17:39:05 GMT
VOLUME [/consul/data]
# Wed, 21 Sep 2022 17:39:06 GMT
EXPOSE 8300
# Wed, 21 Sep 2022 17:39:07 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 21 Sep 2022 17:39:08 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 21 Sep 2022 17:39:10 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Sep 2022 17:39:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Sep 2022 17:39:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f8c6eeaa55b0f135b7fddb3d7745a98ca4d8f06d2898611234b9ef99e1183073`  
		Last Modified: Tue, 09 Aug 2022 17:39:50 GMT  
		Size: 2.8 MB (2828516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b74732828c2e853c2126024b8fd6dc6baa68f7fdfec22e271dbde40c2b93ce0d`  
		Last Modified: Wed, 21 Sep 2022 17:40:19 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:47617cd2d54035423cbd7b4a8756c415126be375b7c1ba6bb0edfcf11eb0c52f`  
		Last Modified: Wed, 21 Sep 2022 17:40:24 GMT  
		Size: 45.8 MB (45827102 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:999989a8d4a7a21f12c28e8bd53ece7060121d09cf683dd87d5758fb1c249fe9`  
		Last Modified: Wed, 21 Sep 2022 17:40:19 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:791128eac9d9df2c5533c3283a2e40a22160efad74bad6ba909eb9aba4ad31cd`  
		Last Modified: Wed, 21 Sep 2022 17:40:19 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b1344da65a6f7d2069d9db1dd131df7aeddee8b4ae62c9ff4279f27dcabe2e8`  
		Last Modified: Wed, 21 Sep 2022 17:40:20 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.13`

```console
$ docker pull consul@sha256:2f3c54ba26a0ecd54208b878921c9b180d6c8aa42c64d3c2eabf06bf8fcac84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.13` - linux; amd64

```console
$ docker pull consul@sha256:09b47d4804c772f145901984cde17965438aa9db2520051363c11ec7ea72bc5d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51849383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d9adf47b726d5beec999918b325fd05a164405191545c9220b0d73d377bdec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Wed, 21 Sep 2022 18:19:31 GMT
ARG CONSUL_VERSION=1.13.2
# Wed, 21 Sep 2022 18:19:31 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 21 Sep 2022 18:19:31 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 21 Sep 2022 18:19:32 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 21 Sep 2022 18:19:38 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 21 Sep 2022 18:19:38 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 21 Sep 2022 18:19:39 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 21 Sep 2022 18:19:39 GMT
VOLUME [/consul/data]
# Wed, 21 Sep 2022 18:19:39 GMT
EXPOSE 8300
# Wed, 21 Sep 2022 18:19:39 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 21 Sep 2022 18:19:39 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 21 Sep 2022 18:19:40 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Sep 2022 18:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Sep 2022 18:19:40 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cf2d2428952d64420a8997dbfb7278eb46fca7b4bb855b8bc358f3a6d55539`  
		Last Modified: Wed, 21 Sep 2022 18:20:17 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7099ab39c598e2877f13dae979473db64c099ca44105925aca7ba070603f2d`  
		Last Modified: Wed, 21 Sep 2022 18:20:23 GMT  
		Size: 49.0 MB (49022488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32dc117d3f9aa7fbba03b84fd078b6b0760afe9fbd3305e0d6e3d413bb117fb1`  
		Last Modified: Wed, 21 Sep 2022 18:20:17 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0af04033d5e6b2b92e3e75964f3b270a40d0e4db5ad37f7d549516ead87964e`  
		Last Modified: Wed, 21 Sep 2022 18:20:17 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed93c3dae33ec219ff7f199b0d4aec9def7320804d80f7d019ee629329e00876`  
		Last Modified: Wed, 21 Sep 2022 18:20:17 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13` - linux; arm variant v6

```console
$ docker pull consul@sha256:36735808b84796cfe144235400a81140c1991998bbe3e7dd61e54acfa0a99e39
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49455721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368d37d67c67430a444997736b380da7653561f878749c0eb20061fa043576c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Wed, 21 Sep 2022 17:49:27 GMT
ARG CONSUL_VERSION=1.13.2
# Wed, 21 Sep 2022 17:49:27 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 21 Sep 2022 17:49:27 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 21 Sep 2022 17:49:28 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 21 Sep 2022 17:49:35 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 21 Sep 2022 17:49:36 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 21 Sep 2022 17:49:37 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 21 Sep 2022 17:49:37 GMT
VOLUME [/consul/data]
# Wed, 21 Sep 2022 17:49:37 GMT
EXPOSE 8300
# Wed, 21 Sep 2022 17:49:37 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 21 Sep 2022 17:49:38 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 21 Sep 2022 17:49:38 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Sep 2022 17:49:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Sep 2022 17:49:38 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57da5fd8cf2f3b25f15fc2d4073b35722074fb28c048fb00a36007d0980af741`  
		Last Modified: Wed, 21 Sep 2022 17:50:40 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444a1ab040843677ec1107d0478afe96c829cd6ebba3045354aa779fdcd304bc`  
		Last Modified: Wed, 21 Sep 2022 17:50:50 GMT  
		Size: 46.8 MB (46821211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67aa617c2bcfe781e84a37f36faa26c996e99490d42819f03c7e47eb5db12e5`  
		Last Modified: Wed, 21 Sep 2022 17:50:40 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8c43dbbdf8d0f76f6b25d5bff59226009aa6d88e074f7f8455b3265ef239b9`  
		Last Modified: Wed, 21 Sep 2022 17:50:40 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f1aefca22203f52943cc9a13b3962ef14fbe85b2b9061eccf6bff6082b13d3`  
		Last Modified: Wed, 21 Sep 2022 17:50:40 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:6b1d435910e6a135ac6f66f52746035520a12dfb596b1b7dce76e271c5890ace
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49011362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb0def4f434c96bff0444edc6c5ab96c2d9aaf31413cd868c76e24a4fcedacd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Wed, 21 Sep 2022 17:39:31 GMT
ARG CONSUL_VERSION=1.13.2
# Wed, 21 Sep 2022 17:39:32 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 21 Sep 2022 17:39:33 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 21 Sep 2022 17:39:34 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 21 Sep 2022 17:39:41 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 21 Sep 2022 17:39:41 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 21 Sep 2022 17:39:42 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 21 Sep 2022 17:39:43 GMT
VOLUME [/consul/data]
# Wed, 21 Sep 2022 17:39:44 GMT
EXPOSE 8300
# Wed, 21 Sep 2022 17:39:45 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 21 Sep 2022 17:39:46 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 21 Sep 2022 17:39:48 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Sep 2022 17:39:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Sep 2022 17:39:49 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db8b00244cb4c2274de54641dfdd6bf19ad2d0224050fc3b4d22b691e30a582`  
		Last Modified: Wed, 21 Sep 2022 17:40:57 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba967e4bf27e45cebcd68e75e436e6195daeb5bceb60ce6e0f95a7ebb2b43d16`  
		Last Modified: Wed, 21 Sep 2022 17:41:03 GMT  
		Size: 46.3 MB (46289598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec033f4b49eea680f6a78c0a344293d64783eaa1d5008e5c5c86865e657d2f0`  
		Last Modified: Wed, 21 Sep 2022 17:40:57 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e945f53214e008477a972db759b80c507bd9774f040f5c2a7076e385a4c7c3`  
		Last Modified: Wed, 21 Sep 2022 17:40:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca2ee2053e190a66e5194d9df4dc47823ef463c989347c463fa8038d0b2ddb1`  
		Last Modified: Wed, 21 Sep 2022 17:40:57 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13` - linux; 386

```console
$ docker pull consul@sha256:1ba6cf75fda76b54f90e34d49848c1268a6b1cbe626677b6bb4a409efe9eaf70
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50733162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba30676764f86a3ec716f6cc4d937ee1ac9e5440b0a6823e1662c984c574689`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:47 GMT
ADD file:d51bb92de86c49ee5486066d12194be78c8b9a8452c44577e2dfeef1945a0138 in / 
# Tue, 09 Aug 2022 17:38:47 GMT
CMD ["/bin/sh"]
# Wed, 21 Sep 2022 17:38:29 GMT
ARG CONSUL_VERSION=1.13.2
# Wed, 21 Sep 2022 17:38:30 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 21 Sep 2022 17:38:31 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 21 Sep 2022 17:38:32 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 21 Sep 2022 17:38:39 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 21 Sep 2022 17:38:40 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 21 Sep 2022 17:38:40 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 21 Sep 2022 17:38:41 GMT
VOLUME [/consul/data]
# Wed, 21 Sep 2022 17:38:42 GMT
EXPOSE 8300
# Wed, 21 Sep 2022 17:38:43 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 21 Sep 2022 17:38:44 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 21 Sep 2022 17:38:46 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Sep 2022 17:38:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Sep 2022 17:38:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f8c6eeaa55b0f135b7fddb3d7745a98ca4d8f06d2898611234b9ef99e1183073`  
		Last Modified: Tue, 09 Aug 2022 17:39:50 GMT  
		Size: 2.8 MB (2828516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca1813e698fca87ded402574eca79317a33772a0efe35072d49c22b90be32c9`  
		Last Modified: Wed, 21 Sep 2022 17:40:00 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe39d6207bc0c4454d20ec1ee1c34adbed87d1e4945829ca8ae3bc5ab9fd527`  
		Last Modified: Wed, 21 Sep 2022 17:40:05 GMT  
		Size: 47.9 MB (47901321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dced650cc345c8e1da5100a9f581e5839438182c9797967eeb4acef3a2b8aaf`  
		Last Modified: Wed, 21 Sep 2022 17:40:00 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d47bc05138d2dbd1a41b0505a7e367f08b4e8579db00b92f35858d8a4a3f88`  
		Last Modified: Wed, 21 Sep 2022 17:40:00 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749954feb4cfdec6abfe6ffeac74ba342e766e8eab76e7680b97fc6216f3b80d`  
		Last Modified: Wed, 21 Sep 2022 17:40:00 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.13.2`

```console
$ docker pull consul@sha256:2f3c54ba26a0ecd54208b878921c9b180d6c8aa42c64d3c2eabf06bf8fcac84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.13.2` - linux; amd64

```console
$ docker pull consul@sha256:09b47d4804c772f145901984cde17965438aa9db2520051363c11ec7ea72bc5d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51849383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d9adf47b726d5beec999918b325fd05a164405191545c9220b0d73d377bdec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Wed, 21 Sep 2022 18:19:31 GMT
ARG CONSUL_VERSION=1.13.2
# Wed, 21 Sep 2022 18:19:31 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 21 Sep 2022 18:19:31 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 21 Sep 2022 18:19:32 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 21 Sep 2022 18:19:38 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 21 Sep 2022 18:19:38 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 21 Sep 2022 18:19:39 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 21 Sep 2022 18:19:39 GMT
VOLUME [/consul/data]
# Wed, 21 Sep 2022 18:19:39 GMT
EXPOSE 8300
# Wed, 21 Sep 2022 18:19:39 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 21 Sep 2022 18:19:39 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 21 Sep 2022 18:19:40 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Sep 2022 18:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Sep 2022 18:19:40 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cf2d2428952d64420a8997dbfb7278eb46fca7b4bb855b8bc358f3a6d55539`  
		Last Modified: Wed, 21 Sep 2022 18:20:17 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7099ab39c598e2877f13dae979473db64c099ca44105925aca7ba070603f2d`  
		Last Modified: Wed, 21 Sep 2022 18:20:23 GMT  
		Size: 49.0 MB (49022488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32dc117d3f9aa7fbba03b84fd078b6b0760afe9fbd3305e0d6e3d413bb117fb1`  
		Last Modified: Wed, 21 Sep 2022 18:20:17 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0af04033d5e6b2b92e3e75964f3b270a40d0e4db5ad37f7d549516ead87964e`  
		Last Modified: Wed, 21 Sep 2022 18:20:17 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed93c3dae33ec219ff7f199b0d4aec9def7320804d80f7d019ee629329e00876`  
		Last Modified: Wed, 21 Sep 2022 18:20:17 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13.2` - linux; arm variant v6

```console
$ docker pull consul@sha256:36735808b84796cfe144235400a81140c1991998bbe3e7dd61e54acfa0a99e39
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49455721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368d37d67c67430a444997736b380da7653561f878749c0eb20061fa043576c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Wed, 21 Sep 2022 17:49:27 GMT
ARG CONSUL_VERSION=1.13.2
# Wed, 21 Sep 2022 17:49:27 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 21 Sep 2022 17:49:27 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 21 Sep 2022 17:49:28 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 21 Sep 2022 17:49:35 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 21 Sep 2022 17:49:36 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 21 Sep 2022 17:49:37 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 21 Sep 2022 17:49:37 GMT
VOLUME [/consul/data]
# Wed, 21 Sep 2022 17:49:37 GMT
EXPOSE 8300
# Wed, 21 Sep 2022 17:49:37 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 21 Sep 2022 17:49:38 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 21 Sep 2022 17:49:38 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Sep 2022 17:49:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Sep 2022 17:49:38 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57da5fd8cf2f3b25f15fc2d4073b35722074fb28c048fb00a36007d0980af741`  
		Last Modified: Wed, 21 Sep 2022 17:50:40 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444a1ab040843677ec1107d0478afe96c829cd6ebba3045354aa779fdcd304bc`  
		Last Modified: Wed, 21 Sep 2022 17:50:50 GMT  
		Size: 46.8 MB (46821211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67aa617c2bcfe781e84a37f36faa26c996e99490d42819f03c7e47eb5db12e5`  
		Last Modified: Wed, 21 Sep 2022 17:50:40 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8c43dbbdf8d0f76f6b25d5bff59226009aa6d88e074f7f8455b3265ef239b9`  
		Last Modified: Wed, 21 Sep 2022 17:50:40 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f1aefca22203f52943cc9a13b3962ef14fbe85b2b9061eccf6bff6082b13d3`  
		Last Modified: Wed, 21 Sep 2022 17:50:40 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13.2` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:6b1d435910e6a135ac6f66f52746035520a12dfb596b1b7dce76e271c5890ace
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49011362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb0def4f434c96bff0444edc6c5ab96c2d9aaf31413cd868c76e24a4fcedacd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Wed, 21 Sep 2022 17:39:31 GMT
ARG CONSUL_VERSION=1.13.2
# Wed, 21 Sep 2022 17:39:32 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 21 Sep 2022 17:39:33 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 21 Sep 2022 17:39:34 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 21 Sep 2022 17:39:41 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 21 Sep 2022 17:39:41 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 21 Sep 2022 17:39:42 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 21 Sep 2022 17:39:43 GMT
VOLUME [/consul/data]
# Wed, 21 Sep 2022 17:39:44 GMT
EXPOSE 8300
# Wed, 21 Sep 2022 17:39:45 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 21 Sep 2022 17:39:46 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 21 Sep 2022 17:39:48 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Sep 2022 17:39:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Sep 2022 17:39:49 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db8b00244cb4c2274de54641dfdd6bf19ad2d0224050fc3b4d22b691e30a582`  
		Last Modified: Wed, 21 Sep 2022 17:40:57 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba967e4bf27e45cebcd68e75e436e6195daeb5bceb60ce6e0f95a7ebb2b43d16`  
		Last Modified: Wed, 21 Sep 2022 17:41:03 GMT  
		Size: 46.3 MB (46289598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec033f4b49eea680f6a78c0a344293d64783eaa1d5008e5c5c86865e657d2f0`  
		Last Modified: Wed, 21 Sep 2022 17:40:57 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e945f53214e008477a972db759b80c507bd9774f040f5c2a7076e385a4c7c3`  
		Last Modified: Wed, 21 Sep 2022 17:40:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca2ee2053e190a66e5194d9df4dc47823ef463c989347c463fa8038d0b2ddb1`  
		Last Modified: Wed, 21 Sep 2022 17:40:57 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13.2` - linux; 386

```console
$ docker pull consul@sha256:1ba6cf75fda76b54f90e34d49848c1268a6b1cbe626677b6bb4a409efe9eaf70
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50733162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba30676764f86a3ec716f6cc4d937ee1ac9e5440b0a6823e1662c984c574689`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:47 GMT
ADD file:d51bb92de86c49ee5486066d12194be78c8b9a8452c44577e2dfeef1945a0138 in / 
# Tue, 09 Aug 2022 17:38:47 GMT
CMD ["/bin/sh"]
# Wed, 21 Sep 2022 17:38:29 GMT
ARG CONSUL_VERSION=1.13.2
# Wed, 21 Sep 2022 17:38:30 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 21 Sep 2022 17:38:31 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 21 Sep 2022 17:38:32 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 21 Sep 2022 17:38:39 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 21 Sep 2022 17:38:40 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 21 Sep 2022 17:38:40 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 21 Sep 2022 17:38:41 GMT
VOLUME [/consul/data]
# Wed, 21 Sep 2022 17:38:42 GMT
EXPOSE 8300
# Wed, 21 Sep 2022 17:38:43 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 21 Sep 2022 17:38:44 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 21 Sep 2022 17:38:46 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Sep 2022 17:38:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Sep 2022 17:38:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f8c6eeaa55b0f135b7fddb3d7745a98ca4d8f06d2898611234b9ef99e1183073`  
		Last Modified: Tue, 09 Aug 2022 17:39:50 GMT  
		Size: 2.8 MB (2828516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca1813e698fca87ded402574eca79317a33772a0efe35072d49c22b90be32c9`  
		Last Modified: Wed, 21 Sep 2022 17:40:00 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe39d6207bc0c4454d20ec1ee1c34adbed87d1e4945829ca8ae3bc5ab9fd527`  
		Last Modified: Wed, 21 Sep 2022 17:40:05 GMT  
		Size: 47.9 MB (47901321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dced650cc345c8e1da5100a9f581e5839438182c9797967eeb4acef3a2b8aaf`  
		Last Modified: Wed, 21 Sep 2022 17:40:00 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d47bc05138d2dbd1a41b0505a7e367f08b4e8579db00b92f35858d8a4a3f88`  
		Last Modified: Wed, 21 Sep 2022 17:40:00 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749954feb4cfdec6abfe6ffeac74ba342e766e8eab76e7680b97fc6216f3b80d`  
		Last Modified: Wed, 21 Sep 2022 17:40:00 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:2f3c54ba26a0ecd54208b878921c9b180d6c8aa42c64d3c2eabf06bf8fcac84a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:09b47d4804c772f145901984cde17965438aa9db2520051363c11ec7ea72bc5d
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.8 MB (51849383 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c3d9adf47b726d5beec999918b325fd05a164405191545c9220b0d73d377bdec`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:20:00 GMT
ADD file:f77e3f51f020890d22997e6c2ca98968b75b8bc8c463341a2010ff0655d4c88f in / 
# Tue, 09 Aug 2022 17:20:01 GMT
CMD ["/bin/sh"]
# Wed, 21 Sep 2022 18:19:31 GMT
ARG CONSUL_VERSION=1.13.2
# Wed, 21 Sep 2022 18:19:31 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 21 Sep 2022 18:19:31 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 21 Sep 2022 18:19:32 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 21 Sep 2022 18:19:38 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 21 Sep 2022 18:19:38 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 21 Sep 2022 18:19:39 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 21 Sep 2022 18:19:39 GMT
VOLUME [/consul/data]
# Wed, 21 Sep 2022 18:19:39 GMT
EXPOSE 8300
# Wed, 21 Sep 2022 18:19:39 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 21 Sep 2022 18:19:39 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 21 Sep 2022 18:19:40 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Sep 2022 18:19:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Sep 2022 18:19:40 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:9621f1afde84053b2f9b6ff34fc7f7460712247c01cbab483c5fa7132cf782ca`  
		Last Modified: Tue, 09 Aug 2022 17:20:52 GMT  
		Size: 2.8 MB (2823512 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f9cf2d2428952d64420a8997dbfb7278eb46fca7b4bb855b8bc358f3a6d55539`  
		Last Modified: Wed, 21 Sep 2022 18:20:17 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3d7099ab39c598e2877f13dae979473db64c099ca44105925aca7ba070603f2d`  
		Last Modified: Wed, 21 Sep 2022 18:20:23 GMT  
		Size: 49.0 MB (49022488 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:32dc117d3f9aa7fbba03b84fd078b6b0760afe9fbd3305e0d6e3d413bb117fb1`  
		Last Modified: Wed, 21 Sep 2022 18:20:17 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b0af04033d5e6b2b92e3e75964f3b270a40d0e4db5ad37f7d549516ead87964e`  
		Last Modified: Wed, 21 Sep 2022 18:20:17 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed93c3dae33ec219ff7f199b0d4aec9def7320804d80f7d019ee629329e00876`  
		Last Modified: Wed, 21 Sep 2022 18:20:17 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:36735808b84796cfe144235400a81140c1991998bbe3e7dd61e54acfa0a99e39
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.5 MB (49455721 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:368d37d67c67430a444997736b380da7653561f878749c0eb20061fa043576c0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:49:29 GMT
ADD file:89cb25f97e17bed5c56311280efe5cfa78422d8ffbe36232195d13f94d67417e in / 
# Tue, 09 Aug 2022 17:49:29 GMT
CMD ["/bin/sh"]
# Wed, 21 Sep 2022 17:49:27 GMT
ARG CONSUL_VERSION=1.13.2
# Wed, 21 Sep 2022 17:49:27 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 21 Sep 2022 17:49:27 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 21 Sep 2022 17:49:28 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 21 Sep 2022 17:49:35 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 21 Sep 2022 17:49:36 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 21 Sep 2022 17:49:37 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 21 Sep 2022 17:49:37 GMT
VOLUME [/consul/data]
# Wed, 21 Sep 2022 17:49:37 GMT
EXPOSE 8300
# Wed, 21 Sep 2022 17:49:37 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 21 Sep 2022 17:49:38 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 21 Sep 2022 17:49:38 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Sep 2022 17:49:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Sep 2022 17:49:38 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:293b708aa6fb80967f27727d5c9c53ac9ba9cac376bed2ad02c17a5cca317b35`  
		Last Modified: Tue, 09 Aug 2022 17:50:52 GMT  
		Size: 2.6 MB (2631127 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57da5fd8cf2f3b25f15fc2d4073b35722074fb28c048fb00a36007d0980af741`  
		Last Modified: Wed, 21 Sep 2022 17:50:40 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:444a1ab040843677ec1107d0478afe96c829cd6ebba3045354aa779fdcd304bc`  
		Last Modified: Wed, 21 Sep 2022 17:50:50 GMT  
		Size: 46.8 MB (46821211 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f67aa617c2bcfe781e84a37f36faa26c996e99490d42819f03c7e47eb5db12e5`  
		Last Modified: Wed, 21 Sep 2022 17:50:40 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd8c43dbbdf8d0f76f6b25d5bff59226009aa6d88e074f7f8455b3265ef239b9`  
		Last Modified: Wed, 21 Sep 2022 17:50:40 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06f1aefca22203f52943cc9a13b3962ef14fbe85b2b9061eccf6bff6082b13d3`  
		Last Modified: Wed, 21 Sep 2022 17:50:40 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:6b1d435910e6a135ac6f66f52746035520a12dfb596b1b7dce76e271c5890ace
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.0 MB (49011362 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0eb0def4f434c96bff0444edc6c5ab96c2d9aaf31413cd868c76e24a4fcedacd`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:39:51 GMT
ADD file:4b51a9d40f20d2beb29d0759b161d2b9403493453beb509de4e86a5d98513f16 in / 
# Tue, 09 Aug 2022 17:39:51 GMT
CMD ["/bin/sh"]
# Wed, 21 Sep 2022 17:39:31 GMT
ARG CONSUL_VERSION=1.13.2
# Wed, 21 Sep 2022 17:39:32 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 21 Sep 2022 17:39:33 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 21 Sep 2022 17:39:34 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 21 Sep 2022 17:39:41 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 21 Sep 2022 17:39:41 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 21 Sep 2022 17:39:42 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 21 Sep 2022 17:39:43 GMT
VOLUME [/consul/data]
# Wed, 21 Sep 2022 17:39:44 GMT
EXPOSE 8300
# Wed, 21 Sep 2022 17:39:45 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 21 Sep 2022 17:39:46 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 21 Sep 2022 17:39:48 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Sep 2022 17:39:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Sep 2022 17:39:49 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:47517142f6ba87eca6b7bdca1e0df160b74671c81e4b9605dad38c1862a43be3`  
		Last Modified: Tue, 09 Aug 2022 17:40:55 GMT  
		Size: 2.7 MB (2718439 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1db8b00244cb4c2274de54641dfdd6bf19ad2d0224050fc3b4d22b691e30a582`  
		Last Modified: Wed, 21 Sep 2022 17:40:57 GMT  
		Size: 1.2 KB (1241 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba967e4bf27e45cebcd68e75e436e6195daeb5bceb60ce6e0f95a7ebb2b43d16`  
		Last Modified: Wed, 21 Sep 2022 17:41:03 GMT  
		Size: 46.3 MB (46289598 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dec033f4b49eea680f6a78c0a344293d64783eaa1d5008e5c5c86865e657d2f0`  
		Last Modified: Wed, 21 Sep 2022 17:40:57 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:31e945f53214e008477a972db759b80c507bd9774f040f5c2a7076e385a4c7c3`  
		Last Modified: Wed, 21 Sep 2022 17:40:57 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ca2ee2053e190a66e5194d9df4dc47823ef463c989347c463fa8038d0b2ddb1`  
		Last Modified: Wed, 21 Sep 2022 17:40:57 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:1ba6cf75fda76b54f90e34d49848c1268a6b1cbe626677b6bb4a409efe9eaf70
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.7 MB (50733162 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5ba30676764f86a3ec716f6cc4d937ee1ac9e5440b0a6823e1662c984c574689`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 09 Aug 2022 17:38:47 GMT
ADD file:d51bb92de86c49ee5486066d12194be78c8b9a8452c44577e2dfeef1945a0138 in / 
# Tue, 09 Aug 2022 17:38:47 GMT
CMD ["/bin/sh"]
# Wed, 21 Sep 2022 17:38:29 GMT
ARG CONSUL_VERSION=1.13.2
# Wed, 21 Sep 2022 17:38:30 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 21 Sep 2022 17:38:31 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 21 Sep 2022 17:38:32 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 21 Sep 2022 17:38:39 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 21 Sep 2022 17:38:40 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 21 Sep 2022 17:38:40 GMT
# ARGS: CONSUL_VERSION=1.13.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 21 Sep 2022 17:38:41 GMT
VOLUME [/consul/data]
# Wed, 21 Sep 2022 17:38:42 GMT
EXPOSE 8300
# Wed, 21 Sep 2022 17:38:43 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 21 Sep 2022 17:38:44 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 21 Sep 2022 17:38:46 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 21 Sep 2022 17:38:46 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 21 Sep 2022 17:38:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:f8c6eeaa55b0f135b7fddb3d7745a98ca4d8f06d2898611234b9ef99e1183073`  
		Last Modified: Tue, 09 Aug 2022 17:39:50 GMT  
		Size: 2.8 MB (2828516 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ca1813e698fca87ded402574eca79317a33772a0efe35072d49c22b90be32c9`  
		Last Modified: Wed, 21 Sep 2022 17:40:00 GMT  
		Size: 1.2 KB (1242 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fe39d6207bc0c4454d20ec1ee1c34adbed87d1e4945829ca8ae3bc5ab9fd527`  
		Last Modified: Wed, 21 Sep 2022 17:40:05 GMT  
		Size: 47.9 MB (47901321 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8dced650cc345c8e1da5100a9f581e5839438182c9797967eeb4acef3a2b8aaf`  
		Last Modified: Wed, 21 Sep 2022 17:40:00 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50d47bc05138d2dbd1a41b0505a7e367f08b4e8579db00b92f35858d8a4a3f88`  
		Last Modified: Wed, 21 Sep 2022 17:40:00 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:749954feb4cfdec6abfe6ffeac74ba342e766e8eab76e7680b97fc6216f3b80d`  
		Last Modified: Wed, 21 Sep 2022 17:40:00 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
