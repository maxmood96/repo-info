<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.10`](#consul110)
-	[`consul:1.10.5`](#consul1105)
-	[`consul:1.11`](#consul111)
-	[`consul:1.11.0`](#consul1110)
-	[`consul:1.9`](#consul19)
-	[`consul:1.9.12`](#consul1912)
-	[`consul:latest`](#consullatest)

## `consul:1.10`

```console
$ docker pull consul@sha256:e4be41d10951d8adfba93d2d1a92dba879a7c5668fa88ab16593d880e4574e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10` - linux; amd64

```console
$ docker pull consul@sha256:4475b8159e056762094fddccfc4ee04cb2fa27168ab1e2fe5602fc0321797573
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43681368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3539c821b8d51285cccc20d1146f06adcf4eb7462ac74f89c0e29e324cb3e7aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:20:45 GMT
ARG CONSUL_VERSION=1.10.5
# Tue, 14 Dec 2021 20:20:45 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:20:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:20:46 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:20:52 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:20:54 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:20:54 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:20:55 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:20:55 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:20:55 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:20:55 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:20:55 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:20:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a31878686a1a40acb3733831b5a7977a1dd15481c4fa1b284f0b2ec7c7d368`  
		Last Modified: Tue, 14 Dec 2021 20:21:42 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8a9b91a9748569616113217fd3037a4404d3e6fed1b00b3fd776da6bf88430`  
		Last Modified: Tue, 14 Dec 2021 20:21:48 GMT  
		Size: 40.9 MB (40855570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44901b3a103ad21cb27e4943d04146ec890159259fd545231fc8edb6b4de44f`  
		Last Modified: Tue, 14 Dec 2021 20:21:42 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964fca1b89e646eeea82bd99676942a41d53336385078346d0d0cb55e52c8f7f`  
		Last Modified: Tue, 14 Dec 2021 20:21:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06001403e520ac36329d871362a618fca50e6758455ef4788e34d656a3ab2db4`  
		Last Modified: Tue, 14 Dec 2021 20:21:42 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm variant v6

```console
$ docker pull consul@sha256:26f6c9499d42f73064f17b21d437bafc9fa61a3bf57bc7a7bc7540531d95eb3f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41747103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a429113e2ccc547f1ee16878d329fac41000ab084f7b6b11471fd7dafe758982`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 19:49:42 GMT
ARG CONSUL_VERSION=1.10.5
# Tue, 14 Dec 2021 19:49:42 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 19:49:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 19:49:44 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 19:49:59 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 19:50:01 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 19:50:02 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 19:50:03 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 19:50:03 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 19:50:03 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 19:50:04 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 19:50:04 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 19:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 19:50:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8738eec68152c08f93f0bc71941e91f6fe264b9630c9caba638107049fa1bc4`  
		Last Modified: Tue, 14 Dec 2021 19:52:08 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cfdb687b1dc02c4107c9139d0f53c12cbf3277b217201770d9ae8b2885b88c`  
		Last Modified: Tue, 14 Dec 2021 19:52:28 GMT  
		Size: 39.1 MB (39110381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47fa8e27beaff857f03fc8210cf70f6fabe906382ed2c0339765cadee8c6cbe`  
		Last Modified: Tue, 14 Dec 2021 19:52:08 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c210f4cc2d698fd83ed20044938c48fa52e2cf08e9dfa365e7934863cfe3e94`  
		Last Modified: Tue, 14 Dec 2021 19:52:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f007675b8db5768f9232d3d0f90275fc72f85204b03e85393dd52bd7ee68f7c0`  
		Last Modified: Tue, 14 Dec 2021 19:52:08 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:56ab516709703801f86014f2c8c01444507fd43032564c5f805d2cad08fe4747
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41699391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50953a41d2fdcad5e29f0cd8a6a1a6a4f6e5ef655e077cf6adbf4ab0cff93221`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:42:07 GMT
ARG CONSUL_VERSION=1.10.5
# Tue, 14 Dec 2021 20:42:08 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:42:09 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:42:10 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:42:21 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:42:22 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:42:23 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:42:24 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:42:25 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:42:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:42:27 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:42:29 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:42:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:42:30 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a2c1bd6c357bc002e6a58e4dba209c567c829b5c3d67a98785cc945075c119`  
		Last Modified: Tue, 14 Dec 2021 20:43:44 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeffb4866022338f09341cba456bc786d9a24021b9def25d3c52dfc1b44fc06f`  
		Last Modified: Tue, 14 Dec 2021 20:43:49 GMT  
		Size: 39.0 MB (38976434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00761f25345de261175f4c5295c54ca88591886261a2d8b6df4349fc125c02ee`  
		Last Modified: Tue, 14 Dec 2021 20:43:44 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef726733fba0795bb822948e4c778b0905a5817dece0dab82e9c748f348bd6a`  
		Last Modified: Tue, 14 Dec 2021 20:43:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e926b3c440264449b5bdd90f02c671539c8a02a514fb4c0b00b77b8ee8715c04`  
		Last Modified: Tue, 14 Dec 2021 20:43:44 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; 386

```console
$ docker pull consul@sha256:4f528d2bec02d5a9bd173c1853d1977b0cbc62deba36c3a0c749a750d75208b6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43063020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b8d0dfb97fd1d3e95de17901bec6860d509acc08a8df1e1f2d8b5533b27826`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:38:28 GMT
ARG CONSUL_VERSION=1.10.5
# Tue, 14 Dec 2021 20:38:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:38:29 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:38:30 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:38:38 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:38:39 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:38:40 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:38:41 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:38:41 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:38:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:38:41 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:38:42 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:38:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:38:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c775a942206ecfd17cfc4806f59ef3add5887dd9bd84253e7df754248313fb`  
		Last Modified: Tue, 14 Dec 2021 20:39:46 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38feef64f936ed8a2a9497c4e414fb4bea21d20ce99b0fdaadfb333895526b8e`  
		Last Modified: Tue, 14 Dec 2021 20:39:52 GMT  
		Size: 40.2 MB (40230838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a916f75ced95121585c99f1bdd61d718b2f36035c24eec0145be385d1b57bfa6`  
		Last Modified: Tue, 14 Dec 2021 20:39:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f64d8c3662188233d828bfd67724f06d0e8c34fa06b283f0ade188c81f5d16`  
		Last Modified: Tue, 14 Dec 2021 20:39:46 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d01e24ff602a70f89473df922920c3b2f1f19e3eed68efe936ff140ce0a159c`  
		Last Modified: Tue, 14 Dec 2021 20:39:46 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.10.5`

```console
$ docker pull consul@sha256:e4be41d10951d8adfba93d2d1a92dba879a7c5668fa88ab16593d880e4574e57
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10.5` - linux; amd64

```console
$ docker pull consul@sha256:4475b8159e056762094fddccfc4ee04cb2fa27168ab1e2fe5602fc0321797573
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43681368 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3539c821b8d51285cccc20d1146f06adcf4eb7462ac74f89c0e29e324cb3e7aa`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:20:45 GMT
ARG CONSUL_VERSION=1.10.5
# Tue, 14 Dec 2021 20:20:45 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:20:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:20:46 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:20:52 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:20:54 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:20:54 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:20:55 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:20:55 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:20:55 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:20:55 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:20:55 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:20:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:20:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:76a31878686a1a40acb3733831b5a7977a1dd15481c4fa1b284f0b2ec7c7d368`  
		Last Modified: Tue, 14 Dec 2021 20:21:42 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b8a9b91a9748569616113217fd3037a4404d3e6fed1b00b3fd776da6bf88430`  
		Last Modified: Tue, 14 Dec 2021 20:21:48 GMT  
		Size: 40.9 MB (40855570 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d44901b3a103ad21cb27e4943d04146ec890159259fd545231fc8edb6b4de44f`  
		Last Modified: Tue, 14 Dec 2021 20:21:42 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:964fca1b89e646eeea82bd99676942a41d53336385078346d0d0cb55e52c8f7f`  
		Last Modified: Tue, 14 Dec 2021 20:21:42 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:06001403e520ac36329d871362a618fca50e6758455ef4788e34d656a3ab2db4`  
		Last Modified: Tue, 14 Dec 2021 20:21:42 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.5` - linux; arm variant v6

```console
$ docker pull consul@sha256:26f6c9499d42f73064f17b21d437bafc9fa61a3bf57bc7a7bc7540531d95eb3f
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41747103 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a429113e2ccc547f1ee16878d329fac41000ab084f7b6b11471fd7dafe758982`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 19:49:42 GMT
ARG CONSUL_VERSION=1.10.5
# Tue, 14 Dec 2021 19:49:42 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 19:49:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 19:49:44 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 19:49:59 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 19:50:01 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 19:50:02 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 19:50:03 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 19:50:03 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 19:50:03 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 19:50:04 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 19:50:04 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 19:50:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 19:50:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8738eec68152c08f93f0bc71941e91f6fe264b9630c9caba638107049fa1bc4`  
		Last Modified: Tue, 14 Dec 2021 19:52:08 GMT  
		Size: 1.3 KB (1264 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3cfdb687b1dc02c4107c9139d0f53c12cbf3277b217201770d9ae8b2885b88c`  
		Last Modified: Tue, 14 Dec 2021 19:52:28 GMT  
		Size: 39.1 MB (39110381 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d47fa8e27beaff857f03fc8210cf70f6fabe906382ed2c0339765cadee8c6cbe`  
		Last Modified: Tue, 14 Dec 2021 19:52:08 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c210f4cc2d698fd83ed20044938c48fa52e2cf08e9dfa365e7934863cfe3e94`  
		Last Modified: Tue, 14 Dec 2021 19:52:08 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f007675b8db5768f9232d3d0f90275fc72f85204b03e85393dd52bd7ee68f7c0`  
		Last Modified: Tue, 14 Dec 2021 19:52:08 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.5` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:56ab516709703801f86014f2c8c01444507fd43032564c5f805d2cad08fe4747
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41699391 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:50953a41d2fdcad5e29f0cd8a6a1a6a4f6e5ef655e077cf6adbf4ab0cff93221`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:42:07 GMT
ARG CONSUL_VERSION=1.10.5
# Tue, 14 Dec 2021 20:42:08 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:42:09 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:42:10 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:42:21 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:42:22 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:42:23 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:42:24 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:42:25 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:42:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:42:27 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:42:29 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:42:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:42:30 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16a2c1bd6c357bc002e6a58e4dba209c567c829b5c3d67a98785cc945075c119`  
		Last Modified: Tue, 14 Dec 2021 20:43:44 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eeffb4866022338f09341cba456bc786d9a24021b9def25d3c52dfc1b44fc06f`  
		Last Modified: Tue, 14 Dec 2021 20:43:49 GMT  
		Size: 39.0 MB (38976434 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00761f25345de261175f4c5295c54ca88591886261a2d8b6df4349fc125c02ee`  
		Last Modified: Tue, 14 Dec 2021 20:43:44 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ef726733fba0795bb822948e4c778b0905a5817dece0dab82e9c748f348bd6a`  
		Last Modified: Tue, 14 Dec 2021 20:43:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e926b3c440264449b5bdd90f02c671539c8a02a514fb4c0b00b77b8ee8715c04`  
		Last Modified: Tue, 14 Dec 2021 20:43:44 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.5` - linux; 386

```console
$ docker pull consul@sha256:4f528d2bec02d5a9bd173c1853d1977b0cbc62deba36c3a0c749a750d75208b6
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43063020 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:07b8d0dfb97fd1d3e95de17901bec6860d509acc08a8df1e1f2d8b5533b27826`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:38:28 GMT
ARG CONSUL_VERSION=1.10.5
# Tue, 14 Dec 2021 20:38:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.5 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:38:29 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:38:30 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:38:38 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:38:39 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:38:40 GMT
# ARGS: CONSUL_VERSION=1.10.5
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:38:41 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:38:41 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:38:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:38:41 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:38:42 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:38:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:38:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75c775a942206ecfd17cfc4806f59ef3add5887dd9bd84253e7df754248313fb`  
		Last Modified: Tue, 14 Dec 2021 20:39:46 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38feef64f936ed8a2a9497c4e414fb4bea21d20ce99b0fdaadfb333895526b8e`  
		Last Modified: Tue, 14 Dec 2021 20:39:52 GMT  
		Size: 40.2 MB (40230838 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a916f75ced95121585c99f1bdd61d718b2f36035c24eec0145be385d1b57bfa6`  
		Last Modified: Tue, 14 Dec 2021 20:39:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:93f64d8c3662188233d828bfd67724f06d0e8c34fa06b283f0ade188c81f5d16`  
		Last Modified: Tue, 14 Dec 2021 20:39:46 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d01e24ff602a70f89473df922920c3b2f1f19e3eed68efe936ff140ce0a159c`  
		Last Modified: Tue, 14 Dec 2021 20:39:46 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.11`

```console
$ docker pull consul@sha256:0176bef257d22f8e4083c3ab4723289a851ec3e36a4ce9634571f103deaffbaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.11` - linux; amd64

```console
$ docker pull consul@sha256:df9710b85dffd84d054772f4d185c65981ecb865c6f7f71da8b9d1e180f6d972
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43882340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a1096e6f84c6bfb4ab9c68775dc4684476d0aa640cfa0647de7db7f08be98e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 18:27:57 GMT
ARG CONSUL_VERSION=1.11.0
# Wed, 15 Dec 2021 18:27:58 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 15 Dec 2021 18:27:58 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 15 Dec 2021 18:27:59 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 15 Dec 2021 18:28:09 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 15 Dec 2021 18:28:10 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 15 Dec 2021 18:28:11 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 18:28:11 GMT
VOLUME [/consul/data]
# Wed, 15 Dec 2021 18:28:12 GMT
EXPOSE 8300
# Wed, 15 Dec 2021 18:28:12 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 15 Dec 2021 18:28:12 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 15 Dec 2021 18:28:12 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 15 Dec 2021 18:28:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 18:28:13 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635dda4fdcf196da48e1c6353f31cdcb1a6de96016ad36eefc229e751ae824d6`  
		Last Modified: Wed, 15 Dec 2021 18:28:31 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5b2066ba25fa0975d5e9cd35509e3dcec5335b16346da929e4d54b4fed9993`  
		Last Modified: Wed, 15 Dec 2021 18:28:36 GMT  
		Size: 41.1 MB (41056544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33a02f5623f4605408707ca7bb24846fc9e80c51aa892c88efd5fcfb53bc56d`  
		Last Modified: Wed, 15 Dec 2021 18:28:31 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4342462e108adcf02ed48ca77706ecd090af2b6c2a26fdbcba3a832d312f16aa`  
		Last Modified: Wed, 15 Dec 2021 18:28:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37e5081ff990d1808444a26bde3660aeb5b843bc4defabb6120274c55b4d27d`  
		Last Modified: Wed, 15 Dec 2021 18:28:31 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11` - linux; arm variant v6

```console
$ docker pull consul@sha256:40fb4481f861b1ad045fc3a27cf42f22430da59b509e9f407e26652eee1f8e3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41655276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ddd4264bd29e14e9e26584bf6aa7b79b4c721d3d95f3d94959ae275dd262ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 18:50:01 GMT
ARG CONSUL_VERSION=1.11.0
# Wed, 15 Dec 2021 18:50:02 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 15 Dec 2021 18:50:02 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 15 Dec 2021 18:50:04 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 15 Dec 2021 18:50:17 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 15 Dec 2021 18:50:19 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 15 Dec 2021 18:50:20 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 18:50:21 GMT
VOLUME [/consul/data]
# Wed, 15 Dec 2021 18:50:21 GMT
EXPOSE 8300
# Wed, 15 Dec 2021 18:50:22 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 15 Dec 2021 18:50:22 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 15 Dec 2021 18:50:23 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 15 Dec 2021 18:50:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 18:50:23 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdae79ce83a93d6ef550db8423bc32e4a7e1c16c6e03cbbdbced4078fefc337`  
		Last Modified: Wed, 15 Dec 2021 18:51:32 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07feda131bda41603dcd7b373ffd8f7119e0779c6fb355f0302641a65cb0199`  
		Last Modified: Wed, 15 Dec 2021 18:51:53 GMT  
		Size: 39.0 MB (39018558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c8a75e4c0c8d126952b53668e7edb5c2759f64aa3d4eaecf1e2869a2c3c91e`  
		Last Modified: Wed, 15 Dec 2021 18:51:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f8f3f4679384bfdfad64ce6cde2febb0a0400065d98db7b643ce1ee6d684bc`  
		Last Modified: Wed, 15 Dec 2021 18:51:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6d625759bd3fc872aa12f957521bc5051c7b7ded02501f5237932e0781e03e`  
		Last Modified: Wed, 15 Dec 2021 18:51:32 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:b411d7fbb5a0be8d3c52c9265d51fbaeaf0ac5c83b0a55cd2e1ac640109e7522
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41479899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f11600dbeef9cf2e1e9150756a94768be4d467eac1356bb813ab3d621ce1a2fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 18:39:31 GMT
ARG CONSUL_VERSION=1.11.0
# Wed, 15 Dec 2021 18:39:32 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 15 Dec 2021 18:39:33 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 15 Dec 2021 18:39:34 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 15 Dec 2021 18:39:45 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 15 Dec 2021 18:39:46 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 15 Dec 2021 18:39:46 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 18:39:47 GMT
VOLUME [/consul/data]
# Wed, 15 Dec 2021 18:39:48 GMT
EXPOSE 8300
# Wed, 15 Dec 2021 18:39:49 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 15 Dec 2021 18:39:50 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 15 Dec 2021 18:39:52 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 15 Dec 2021 18:39:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 18:39:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e1df28d8f1cdeaddb586c03b3f00b7d506147c7b09d4a83304fd56a7b623cc`  
		Last Modified: Wed, 15 Dec 2021 18:40:22 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738a93d6435ca0f7bb2fc9d97d279e885006d4b42cce7bd137678e85d9ff3e87`  
		Last Modified: Wed, 15 Dec 2021 18:40:28 GMT  
		Size: 38.8 MB (38756943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf9b4c652e79289b20fc7a94e69a0223b458a8b5cf7a579cdd622c6a874bc79`  
		Last Modified: Wed, 15 Dec 2021 18:40:22 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3228efcf3903885242d1d1bbb064690c6a30ff7f4c0466110c70fb6f27106d63`  
		Last Modified: Wed, 15 Dec 2021 18:40:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296b628ec17f163bbb5c1d636e24e5911d428dd8b323f2c4880124f4d1186d21`  
		Last Modified: Wed, 15 Dec 2021 18:40:22 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11` - linux; 386

```console
$ docker pull consul@sha256:548433ee32a7bb1abc863f901169ff652d6336cc027c2263c304c46fd69cc400
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42706723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d32d43848bb677366c7b137458a1cd2a6dd4fdaa6fa4a451f23f975077cf09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 18:38:23 GMT
ARG CONSUL_VERSION=1.11.0
# Wed, 15 Dec 2021 18:38:23 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 15 Dec 2021 18:38:23 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 15 Dec 2021 18:38:24 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 15 Dec 2021 18:38:37 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 15 Dec 2021 18:38:38 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 15 Dec 2021 18:38:39 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 18:38:39 GMT
VOLUME [/consul/data]
# Wed, 15 Dec 2021 18:38:39 GMT
EXPOSE 8300
# Wed, 15 Dec 2021 18:38:39 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 15 Dec 2021 18:38:40 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 15 Dec 2021 18:38:40 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 15 Dec 2021 18:38:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 18:38:40 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd61499e9c80943de4083f9d5ee8148a3da330f13192d112c334045cf8f1195`  
		Last Modified: Wed, 15 Dec 2021 18:39:10 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82adabb18b1d559ab6f0471f29cbd72afdcf7e3b62de9d9f863c1bf0f189fc50`  
		Last Modified: Wed, 15 Dec 2021 18:39:16 GMT  
		Size: 39.9 MB (39874542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf82d2fd4c58853f92cd86490445f3c57cae47b31393417e6e54e4d2bb5f8ddb`  
		Last Modified: Wed, 15 Dec 2021 18:39:10 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ce8ba4784ff51d9f93f7af1d92de31d32dea0f64d051986ccbf34535b272cc`  
		Last Modified: Wed, 15 Dec 2021 18:39:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943b3b802bef07597c17246e97d241e882b8d68299e9d01404ae42418e485dc2`  
		Last Modified: Wed, 15 Dec 2021 18:39:10 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.11.0`

```console
$ docker pull consul@sha256:0176bef257d22f8e4083c3ab4723289a851ec3e36a4ce9634571f103deaffbaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.11.0` - linux; amd64

```console
$ docker pull consul@sha256:df9710b85dffd84d054772f4d185c65981ecb865c6f7f71da8b9d1e180f6d972
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43882340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a1096e6f84c6bfb4ab9c68775dc4684476d0aa640cfa0647de7db7f08be98e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 18:27:57 GMT
ARG CONSUL_VERSION=1.11.0
# Wed, 15 Dec 2021 18:27:58 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 15 Dec 2021 18:27:58 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 15 Dec 2021 18:27:59 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 15 Dec 2021 18:28:09 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 15 Dec 2021 18:28:10 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 15 Dec 2021 18:28:11 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 18:28:11 GMT
VOLUME [/consul/data]
# Wed, 15 Dec 2021 18:28:12 GMT
EXPOSE 8300
# Wed, 15 Dec 2021 18:28:12 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 15 Dec 2021 18:28:12 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 15 Dec 2021 18:28:12 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 15 Dec 2021 18:28:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 18:28:13 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635dda4fdcf196da48e1c6353f31cdcb1a6de96016ad36eefc229e751ae824d6`  
		Last Modified: Wed, 15 Dec 2021 18:28:31 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5b2066ba25fa0975d5e9cd35509e3dcec5335b16346da929e4d54b4fed9993`  
		Last Modified: Wed, 15 Dec 2021 18:28:36 GMT  
		Size: 41.1 MB (41056544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33a02f5623f4605408707ca7bb24846fc9e80c51aa892c88efd5fcfb53bc56d`  
		Last Modified: Wed, 15 Dec 2021 18:28:31 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4342462e108adcf02ed48ca77706ecd090af2b6c2a26fdbcba3a832d312f16aa`  
		Last Modified: Wed, 15 Dec 2021 18:28:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37e5081ff990d1808444a26bde3660aeb5b843bc4defabb6120274c55b4d27d`  
		Last Modified: Wed, 15 Dec 2021 18:28:31 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.0` - linux; arm variant v6

```console
$ docker pull consul@sha256:40fb4481f861b1ad045fc3a27cf42f22430da59b509e9f407e26652eee1f8e3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41655276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ddd4264bd29e14e9e26584bf6aa7b79b4c721d3d95f3d94959ae275dd262ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 18:50:01 GMT
ARG CONSUL_VERSION=1.11.0
# Wed, 15 Dec 2021 18:50:02 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 15 Dec 2021 18:50:02 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 15 Dec 2021 18:50:04 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 15 Dec 2021 18:50:17 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 15 Dec 2021 18:50:19 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 15 Dec 2021 18:50:20 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 18:50:21 GMT
VOLUME [/consul/data]
# Wed, 15 Dec 2021 18:50:21 GMT
EXPOSE 8300
# Wed, 15 Dec 2021 18:50:22 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 15 Dec 2021 18:50:22 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 15 Dec 2021 18:50:23 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 15 Dec 2021 18:50:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 18:50:23 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdae79ce83a93d6ef550db8423bc32e4a7e1c16c6e03cbbdbced4078fefc337`  
		Last Modified: Wed, 15 Dec 2021 18:51:32 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07feda131bda41603dcd7b373ffd8f7119e0779c6fb355f0302641a65cb0199`  
		Last Modified: Wed, 15 Dec 2021 18:51:53 GMT  
		Size: 39.0 MB (39018558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c8a75e4c0c8d126952b53668e7edb5c2759f64aa3d4eaecf1e2869a2c3c91e`  
		Last Modified: Wed, 15 Dec 2021 18:51:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f8f3f4679384bfdfad64ce6cde2febb0a0400065d98db7b643ce1ee6d684bc`  
		Last Modified: Wed, 15 Dec 2021 18:51:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6d625759bd3fc872aa12f957521bc5051c7b7ded02501f5237932e0781e03e`  
		Last Modified: Wed, 15 Dec 2021 18:51:32 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.0` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:b411d7fbb5a0be8d3c52c9265d51fbaeaf0ac5c83b0a55cd2e1ac640109e7522
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41479899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f11600dbeef9cf2e1e9150756a94768be4d467eac1356bb813ab3d621ce1a2fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 18:39:31 GMT
ARG CONSUL_VERSION=1.11.0
# Wed, 15 Dec 2021 18:39:32 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 15 Dec 2021 18:39:33 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 15 Dec 2021 18:39:34 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 15 Dec 2021 18:39:45 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 15 Dec 2021 18:39:46 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 15 Dec 2021 18:39:46 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 18:39:47 GMT
VOLUME [/consul/data]
# Wed, 15 Dec 2021 18:39:48 GMT
EXPOSE 8300
# Wed, 15 Dec 2021 18:39:49 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 15 Dec 2021 18:39:50 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 15 Dec 2021 18:39:52 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 15 Dec 2021 18:39:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 18:39:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e1df28d8f1cdeaddb586c03b3f00b7d506147c7b09d4a83304fd56a7b623cc`  
		Last Modified: Wed, 15 Dec 2021 18:40:22 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738a93d6435ca0f7bb2fc9d97d279e885006d4b42cce7bd137678e85d9ff3e87`  
		Last Modified: Wed, 15 Dec 2021 18:40:28 GMT  
		Size: 38.8 MB (38756943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf9b4c652e79289b20fc7a94e69a0223b458a8b5cf7a579cdd622c6a874bc79`  
		Last Modified: Wed, 15 Dec 2021 18:40:22 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3228efcf3903885242d1d1bbb064690c6a30ff7f4c0466110c70fb6f27106d63`  
		Last Modified: Wed, 15 Dec 2021 18:40:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296b628ec17f163bbb5c1d636e24e5911d428dd8b323f2c4880124f4d1186d21`  
		Last Modified: Wed, 15 Dec 2021 18:40:22 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.0` - linux; 386

```console
$ docker pull consul@sha256:548433ee32a7bb1abc863f901169ff652d6336cc027c2263c304c46fd69cc400
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42706723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d32d43848bb677366c7b137458a1cd2a6dd4fdaa6fa4a451f23f975077cf09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 18:38:23 GMT
ARG CONSUL_VERSION=1.11.0
# Wed, 15 Dec 2021 18:38:23 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 15 Dec 2021 18:38:23 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 15 Dec 2021 18:38:24 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 15 Dec 2021 18:38:37 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 15 Dec 2021 18:38:38 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 15 Dec 2021 18:38:39 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 18:38:39 GMT
VOLUME [/consul/data]
# Wed, 15 Dec 2021 18:38:39 GMT
EXPOSE 8300
# Wed, 15 Dec 2021 18:38:39 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 15 Dec 2021 18:38:40 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 15 Dec 2021 18:38:40 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 15 Dec 2021 18:38:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 18:38:40 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd61499e9c80943de4083f9d5ee8148a3da330f13192d112c334045cf8f1195`  
		Last Modified: Wed, 15 Dec 2021 18:39:10 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82adabb18b1d559ab6f0471f29cbd72afdcf7e3b62de9d9f863c1bf0f189fc50`  
		Last Modified: Wed, 15 Dec 2021 18:39:16 GMT  
		Size: 39.9 MB (39874542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf82d2fd4c58853f92cd86490445f3c57cae47b31393417e6e54e4d2bb5f8ddb`  
		Last Modified: Wed, 15 Dec 2021 18:39:10 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ce8ba4784ff51d9f93f7af1d92de31d32dea0f64d051986ccbf34535b272cc`  
		Last Modified: Wed, 15 Dec 2021 18:39:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943b3b802bef07597c17246e97d241e882b8d68299e9d01404ae42418e485dc2`  
		Last Modified: Wed, 15 Dec 2021 18:39:10 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9`

```console
$ docker pull consul@sha256:c1401ff3cb72322e72983eb837c0655445f418dfd52842ea50d32d1de9220fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9` - linux; amd64

```console
$ docker pull consul@sha256:414000fc660049d2566f607e1bb5138e74e3d2bb2ad4f073495418ba35917531
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46347283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b1b850029f6abff01847817129e319da7f85e22ff6ce3ee8452d8d22def883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:20:58 GMT
ARG CONSUL_VERSION=1.9.12
# Tue, 14 Dec 2021 20:20:58 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:20:59 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:20:59 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:21:07 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:21:08 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:21:09 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:21:09 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:21:09 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:21:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:21:09 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:21:10 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:21:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:21:10 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757ae26b350794d2fa7287fb89434cbe0b66fafab1d8ba1bd6b5b7406d0ae111`  
		Last Modified: Tue, 14 Dec 2021 20:22:00 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4ba7257335ed3cc6d28ec7be06c9965df9d90cd1821024371221a0b315425d`  
		Last Modified: Tue, 14 Dec 2021 20:22:06 GMT  
		Size: 43.5 MB (43521487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e034957fd950b917007c48bd9777c799d472a17116b5a6a4305e83cb22c2144`  
		Last Modified: Tue, 14 Dec 2021 20:22:00 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddc88c68c55accb56303e9bb0bbe718f3aeff268b447260af5502b8b30d49d7`  
		Last Modified: Tue, 14 Dec 2021 20:22:00 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64b78141e0daaf4545c9403bcf81891f8b5456e2c00e3eee3ae5ce73908552c`  
		Last Modified: Tue, 14 Dec 2021 20:22:00 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:a7105c62cfb3f0e40ba51cb4a7a51d909694a6cc218213e8e5e88839743b9f22
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43630043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebf8bd2a2f91043ea2800786b2704e71df2576168d75614baedccb327857e20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 19:50:18 GMT
ARG CONSUL_VERSION=1.9.12
# Tue, 14 Dec 2021 19:50:18 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 19:50:19 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 19:50:20 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 19:50:33 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 19:50:35 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 19:50:36 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 19:50:37 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 19:50:37 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 19:50:38 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 19:50:38 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 19:50:39 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 19:50:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 19:50:39 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738aaaed04bbd7697fdeaa9d74a8accd8958ed8179919906c5b737f6f836cbe0`  
		Last Modified: Tue, 14 Dec 2021 19:52:44 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11aa60632f4b82d88ecbc5d28163c03404c0266707d9b231ffad298fa1bae3f0`  
		Last Modified: Tue, 14 Dec 2021 19:53:06 GMT  
		Size: 41.0 MB (40993320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7330cf0a1f14d749ce5047705ee3383d1b9cecd6031edcfaa1dfebf3d5954c`  
		Last Modified: Tue, 14 Dec 2021 19:52:44 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d426972319eebc1a0fe09d30b557863794f1d16a309451e35c4b7ca3c8e2d6`  
		Last Modified: Tue, 14 Dec 2021 19:52:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5c5118bab9327394112ea78c084e7e160abcdf72c22555468f9e8eac0f2fcc`  
		Last Modified: Tue, 14 Dec 2021 19:52:44 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:25ca83fd0b136d9f122c03d25f63f42e08395e49dbb7a2649bf7c23f6b324dcb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43917815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ed12ef44ef801c92388227129b79c623b47bba97f0d109dc940cf95c14c621`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:42:38 GMT
ARG CONSUL_VERSION=1.9.12
# Tue, 14 Dec 2021 20:42:39 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:42:40 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:42:41 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:42:48 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:42:48 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:42:49 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:42:50 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:42:51 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:42:52 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:42:53 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:42:55 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:42:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:42:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08fd8ec1ab1ca61fd03e0b39e52ba153f0052bf13c3466094a6a26779fed8c2`  
		Last Modified: Tue, 14 Dec 2021 20:44:03 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3bf82943d743f743e3f356b5bc9a5ff3cde6f0e3e1e3d203f4a4f91757c91f`  
		Last Modified: Tue, 14 Dec 2021 20:44:08 GMT  
		Size: 41.2 MB (41194864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a999ae667c9bcb8227f07b7c61c9aae978a328cd3256003672bf1cf0d8bf05d`  
		Last Modified: Tue, 14 Dec 2021 20:44:03 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1d6502de310c0cd222ce8b76b1de977e73bb28d465f44ea9db4adbb69e723a`  
		Last Modified: Tue, 14 Dec 2021 20:44:03 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbc67176a0724ecdb3bfebf97423fa213a6275c6b7514cc0b90baa6aad1bed`  
		Last Modified: Tue, 14 Dec 2021 20:44:03 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; 386

```console
$ docker pull consul@sha256:5bb412b4e60ea4b1890b4a54b91a8a1f627380965c1ad965944ec31a641e3caa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45728780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3860d9bbc588dc8f7010b7bfcb80a248dc155327801cfb06aba563ca8645e1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:38:48 GMT
ARG CONSUL_VERSION=1.9.12
# Tue, 14 Dec 2021 20:38:49 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:38:49 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:38:50 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:38:57 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:38:58 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:38:59 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:38:59 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:39:00 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:39:00 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:39:00 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:39:01 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:39:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:39:01 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d99b58bd55e9a552c1b5df8ad17486a4dfea641ded9190dc2068da8a525944`  
		Last Modified: Tue, 14 Dec 2021 20:40:07 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0842f2031276fce7ab6cc94d8215180a1c6535ca04883da838937d62f0af9f`  
		Last Modified: Tue, 14 Dec 2021 20:40:14 GMT  
		Size: 42.9 MB (42896600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc80f747f1b2611b42db8f51d5fefea94c70103585b856281b5bed1d23c3af26`  
		Last Modified: Tue, 14 Dec 2021 20:40:07 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6507305b927578884055029b7d8729ece2610479e23564e6e864dc86f502b08`  
		Last Modified: Tue, 14 Dec 2021 20:40:07 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3450ca70d07687f9dd9db2509f7490bdb3f0e1ed3c13b416f1dbec8acaece95`  
		Last Modified: Tue, 14 Dec 2021 20:40:07 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9.12`

```console
$ docker pull consul@sha256:c1401ff3cb72322e72983eb837c0655445f418dfd52842ea50d32d1de9220fa3
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9.12` - linux; amd64

```console
$ docker pull consul@sha256:414000fc660049d2566f607e1bb5138e74e3d2bb2ad4f073495418ba35917531
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46347283 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d1b1b850029f6abff01847817129e319da7f85e22ff6ce3ee8452d8d22def883`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:20:58 GMT
ARG CONSUL_VERSION=1.9.12
# Tue, 14 Dec 2021 20:20:58 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:20:59 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:20:59 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:21:07 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:21:08 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:21:09 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:21:09 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:21:09 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:21:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:21:09 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:21:10 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:21:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:21:10 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:757ae26b350794d2fa7287fb89434cbe0b66fafab1d8ba1bd6b5b7406d0ae111`  
		Last Modified: Tue, 14 Dec 2021 20:22:00 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca4ba7257335ed3cc6d28ec7be06c9965df9d90cd1821024371221a0b315425d`  
		Last Modified: Tue, 14 Dec 2021 20:22:06 GMT  
		Size: 43.5 MB (43521487 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e034957fd950b917007c48bd9777c799d472a17116b5a6a4305e83cb22c2144`  
		Last Modified: Tue, 14 Dec 2021 20:22:00 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ddc88c68c55accb56303e9bb0bbe718f3aeff268b447260af5502b8b30d49d7`  
		Last Modified: Tue, 14 Dec 2021 20:22:00 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a64b78141e0daaf4545c9403bcf81891f8b5456e2c00e3eee3ae5ce73908552c`  
		Last Modified: Tue, 14 Dec 2021 20:22:00 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.12` - linux; arm variant v6

```console
$ docker pull consul@sha256:a7105c62cfb3f0e40ba51cb4a7a51d909694a6cc218213e8e5e88839743b9f22
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43630043 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1ebf8bd2a2f91043ea2800786b2704e71df2576168d75614baedccb327857e20`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 19:50:18 GMT
ARG CONSUL_VERSION=1.9.12
# Tue, 14 Dec 2021 19:50:18 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 19:50:19 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 19:50:20 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 19:50:33 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 19:50:35 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 19:50:36 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 19:50:37 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 19:50:37 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 19:50:38 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 19:50:38 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 19:50:39 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 19:50:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 19:50:39 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738aaaed04bbd7697fdeaa9d74a8accd8958ed8179919906c5b737f6f836cbe0`  
		Last Modified: Tue, 14 Dec 2021 19:52:44 GMT  
		Size: 1.3 KB (1263 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11aa60632f4b82d88ecbc5d28163c03404c0266707d9b231ffad298fa1bae3f0`  
		Last Modified: Tue, 14 Dec 2021 19:53:06 GMT  
		Size: 41.0 MB (40993320 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7330cf0a1f14d749ce5047705ee3383d1b9cecd6031edcfaa1dfebf3d5954c`  
		Last Modified: Tue, 14 Dec 2021 19:52:44 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d426972319eebc1a0fe09d30b557863794f1d16a309451e35c4b7ca3c8e2d6`  
		Last Modified: Tue, 14 Dec 2021 19:52:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a5c5118bab9327394112ea78c084e7e160abcdf72c22555468f9e8eac0f2fcc`  
		Last Modified: Tue, 14 Dec 2021 19:52:44 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.12` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:25ca83fd0b136d9f122c03d25f63f42e08395e49dbb7a2649bf7c23f6b324dcb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43917815 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:30ed12ef44ef801c92388227129b79c623b47bba97f0d109dc940cf95c14c621`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:42:38 GMT
ARG CONSUL_VERSION=1.9.12
# Tue, 14 Dec 2021 20:42:39 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:42:40 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:42:41 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:42:48 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:42:48 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:42:49 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:42:50 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:42:51 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:42:52 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:42:53 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:42:55 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:42:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:42:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a08fd8ec1ab1ca61fd03e0b39e52ba153f0052bf13c3466094a6a26779fed8c2`  
		Last Modified: Tue, 14 Dec 2021 20:44:03 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1d3bf82943d743f743e3f356b5bc9a5ff3cde6f0e3e1e3d203f4a4f91757c91f`  
		Last Modified: Tue, 14 Dec 2021 20:44:08 GMT  
		Size: 41.2 MB (41194864 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a999ae667c9bcb8227f07b7c61c9aae978a328cd3256003672bf1cf0d8bf05d`  
		Last Modified: Tue, 14 Dec 2021 20:44:03 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3c1d6502de310c0cd222ce8b76b1de977e73bb28d465f44ea9db4adbb69e723a`  
		Last Modified: Tue, 14 Dec 2021 20:44:03 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d6fbc67176a0724ecdb3bfebf97423fa213a6275c6b7514cc0b90baa6aad1bed`  
		Last Modified: Tue, 14 Dec 2021 20:44:03 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.12` - linux; 386

```console
$ docker pull consul@sha256:5bb412b4e60ea4b1890b4a54b91a8a1f627380965c1ad965944ec31a641e3caa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.7 MB (45728780 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f3860d9bbc588dc8f7010b7bfcb80a248dc155327801cfb06aba563ca8645e1b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Tue, 14 Dec 2021 20:38:48 GMT
ARG CONSUL_VERSION=1.9.12
# Tue, 14 Dec 2021 20:38:49 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.12 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 14 Dec 2021 20:38:49 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 14 Dec 2021 20:38:50 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 14 Dec 2021 20:38:57 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 14 Dec 2021 20:38:58 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 14 Dec 2021 20:38:59 GMT
# ARGS: CONSUL_VERSION=1.9.12
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 14 Dec 2021 20:38:59 GMT
VOLUME [/consul/data]
# Tue, 14 Dec 2021 20:39:00 GMT
EXPOSE 8300
# Tue, 14 Dec 2021 20:39:00 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 14 Dec 2021 20:39:00 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 14 Dec 2021 20:39:01 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 14 Dec 2021 20:39:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 14 Dec 2021 20:39:01 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75d99b58bd55e9a552c1b5df8ad17486a4dfea641ded9190dc2068da8a525944`  
		Last Modified: Tue, 14 Dec 2021 20:40:07 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1a0842f2031276fce7ab6cc94d8215180a1c6535ca04883da838937d62f0af9f`  
		Last Modified: Tue, 14 Dec 2021 20:40:14 GMT  
		Size: 42.9 MB (42896600 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc80f747f1b2611b42db8f51d5fefea94c70103585b856281b5bed1d23c3af26`  
		Last Modified: Tue, 14 Dec 2021 20:40:07 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6507305b927578884055029b7d8729ece2610479e23564e6e864dc86f502b08`  
		Last Modified: Tue, 14 Dec 2021 20:40:07 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b3450ca70d07687f9dd9db2509f7490bdb3f0e1ed3c13b416f1dbec8acaece95`  
		Last Modified: Tue, 14 Dec 2021 20:40:07 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:0176bef257d22f8e4083c3ab4723289a851ec3e36a4ce9634571f103deaffbaa
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:df9710b85dffd84d054772f4d185c65981ecb865c6f7f71da8b9d1e180f6d972
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43882340 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b9a1096e6f84c6bfb4ab9c68775dc4684476d0aa640cfa0647de7db7f08be98e`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 18:27:57 GMT
ARG CONSUL_VERSION=1.11.0
# Wed, 15 Dec 2021 18:27:58 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 15 Dec 2021 18:27:58 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 15 Dec 2021 18:27:59 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 15 Dec 2021 18:28:09 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 15 Dec 2021 18:28:10 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 15 Dec 2021 18:28:11 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 18:28:11 GMT
VOLUME [/consul/data]
# Wed, 15 Dec 2021 18:28:12 GMT
EXPOSE 8300
# Wed, 15 Dec 2021 18:28:12 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 15 Dec 2021 18:28:12 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 15 Dec 2021 18:28:12 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 15 Dec 2021 18:28:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 18:28:13 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:635dda4fdcf196da48e1c6353f31cdcb1a6de96016ad36eefc229e751ae824d6`  
		Last Modified: Wed, 15 Dec 2021 18:28:31 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8b5b2066ba25fa0975d5e9cd35509e3dcec5335b16346da929e4d54b4fed9993`  
		Last Modified: Wed, 15 Dec 2021 18:28:36 GMT  
		Size: 41.1 MB (41056544 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d33a02f5623f4605408707ca7bb24846fc9e80c51aa892c88efd5fcfb53bc56d`  
		Last Modified: Wed, 15 Dec 2021 18:28:31 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4342462e108adcf02ed48ca77706ecd090af2b6c2a26fdbcba3a832d312f16aa`  
		Last Modified: Wed, 15 Dec 2021 18:28:31 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b37e5081ff990d1808444a26bde3660aeb5b843bc4defabb6120274c55b4d27d`  
		Last Modified: Wed, 15 Dec 2021 18:28:31 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:40fb4481f861b1ad045fc3a27cf42f22430da59b509e9f407e26652eee1f8e3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41655276 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:01ddd4264bd29e14e9e26584bf6aa7b79b4c721d3d95f3d94959ae275dd262ff`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 18:50:01 GMT
ARG CONSUL_VERSION=1.11.0
# Wed, 15 Dec 2021 18:50:02 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 15 Dec 2021 18:50:02 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 15 Dec 2021 18:50:04 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 15 Dec 2021 18:50:17 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 15 Dec 2021 18:50:19 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 15 Dec 2021 18:50:20 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 18:50:21 GMT
VOLUME [/consul/data]
# Wed, 15 Dec 2021 18:50:21 GMT
EXPOSE 8300
# Wed, 15 Dec 2021 18:50:22 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 15 Dec 2021 18:50:22 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 15 Dec 2021 18:50:23 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 15 Dec 2021 18:50:23 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 18:50:23 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bdae79ce83a93d6ef550db8423bc32e4a7e1c16c6e03cbbdbced4078fefc337`  
		Last Modified: Wed, 15 Dec 2021 18:51:32 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f07feda131bda41603dcd7b373ffd8f7119e0779c6fb355f0302641a65cb0199`  
		Last Modified: Wed, 15 Dec 2021 18:51:53 GMT  
		Size: 39.0 MB (39018558 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:92c8a75e4c0c8d126952b53668e7edb5c2759f64aa3d4eaecf1e2869a2c3c91e`  
		Last Modified: Wed, 15 Dec 2021 18:51:32 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7f8f3f4679384bfdfad64ce6cde2febb0a0400065d98db7b643ce1ee6d684bc`  
		Last Modified: Wed, 15 Dec 2021 18:51:32 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e6d625759bd3fc872aa12f957521bc5051c7b7ded02501f5237932e0781e03e`  
		Last Modified: Wed, 15 Dec 2021 18:51:32 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:b411d7fbb5a0be8d3c52c9265d51fbaeaf0ac5c83b0a55cd2e1ac640109e7522
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41479899 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f11600dbeef9cf2e1e9150756a94768be4d467eac1356bb813ab3d621ce1a2fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 18:39:31 GMT
ARG CONSUL_VERSION=1.11.0
# Wed, 15 Dec 2021 18:39:32 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 15 Dec 2021 18:39:33 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 15 Dec 2021 18:39:34 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 15 Dec 2021 18:39:45 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 15 Dec 2021 18:39:46 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 15 Dec 2021 18:39:46 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 18:39:47 GMT
VOLUME [/consul/data]
# Wed, 15 Dec 2021 18:39:48 GMT
EXPOSE 8300
# Wed, 15 Dec 2021 18:39:49 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 15 Dec 2021 18:39:50 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 15 Dec 2021 18:39:52 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 15 Dec 2021 18:39:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 18:39:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55e1df28d8f1cdeaddb586c03b3f00b7d506147c7b09d4a83304fd56a7b623cc`  
		Last Modified: Wed, 15 Dec 2021 18:40:22 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738a93d6435ca0f7bb2fc9d97d279e885006d4b42cce7bd137678e85d9ff3e87`  
		Last Modified: Wed, 15 Dec 2021 18:40:28 GMT  
		Size: 38.8 MB (38756943 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:abf9b4c652e79289b20fc7a94e69a0223b458a8b5cf7a579cdd622c6a874bc79`  
		Last Modified: Wed, 15 Dec 2021 18:40:22 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3228efcf3903885242d1d1bbb064690c6a30ff7f4c0466110c70fb6f27106d63`  
		Last Modified: Wed, 15 Dec 2021 18:40:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296b628ec17f163bbb5c1d636e24e5911d428dd8b323f2c4880124f4d1186d21`  
		Last Modified: Wed, 15 Dec 2021 18:40:22 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:548433ee32a7bb1abc863f901169ff652d6336cc027c2263c304c46fd69cc400
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42706723 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:91d32d43848bb677366c7b137458a1cd2a6dd4fdaa6fa4a451f23f975077cf09`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Wed, 15 Dec 2021 18:38:23 GMT
ARG CONSUL_VERSION=1.11.0
# Wed, 15 Dec 2021 18:38:23 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 15 Dec 2021 18:38:23 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 15 Dec 2021 18:38:24 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 15 Dec 2021 18:38:37 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 15 Dec 2021 18:38:38 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 15 Dec 2021 18:38:39 GMT
# ARGS: CONSUL_VERSION=1.11.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 15 Dec 2021 18:38:39 GMT
VOLUME [/consul/data]
# Wed, 15 Dec 2021 18:38:39 GMT
EXPOSE 8300
# Wed, 15 Dec 2021 18:38:39 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 15 Dec 2021 18:38:40 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 15 Dec 2021 18:38:40 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 15 Dec 2021 18:38:40 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 15 Dec 2021 18:38:40 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0bd61499e9c80943de4083f9d5ee8148a3da330f13192d112c334045cf8f1195`  
		Last Modified: Wed, 15 Dec 2021 18:39:10 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:82adabb18b1d559ab6f0471f29cbd72afdcf7e3b62de9d9f863c1bf0f189fc50`  
		Last Modified: Wed, 15 Dec 2021 18:39:16 GMT  
		Size: 39.9 MB (39874542 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf82d2fd4c58853f92cd86490445f3c57cae47b31393417e6e54e4d2bb5f8ddb`  
		Last Modified: Wed, 15 Dec 2021 18:39:10 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83ce8ba4784ff51d9f93f7af1d92de31d32dea0f64d051986ccbf34535b272cc`  
		Last Modified: Wed, 15 Dec 2021 18:39:10 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:943b3b802bef07597c17246e97d241e882b8d68299e9d01404ae42418e485dc2`  
		Last Modified: Wed, 15 Dec 2021 18:39:10 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
