## `consul:latest`

```console
$ docker pull consul@sha256:43cc31d422649c88fec7f5c146110854149da68ee70c505f5bbd667c71bc698a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:0ddc0dfddad8ff2b8ea64923383d4a84ddba21864b85a2a39b28f09b1d18c6a2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43912305 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5cebfabb812332fce28693fbc088cfbb79e55dd2d338af0cfcaa9e4fc569cbe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:19:31 GMT
ARG CONSUL_VERSION=1.11.2
# Fri, 14 Jan 2022 18:19:31 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:19:31 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:19:32 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:19:47 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:19:48 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:19:49 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:19:49 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:19:49 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:19:49 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:19:50 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:19:50 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:19:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:19:50 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b8172e279c1c8f35c79da13d439f1ce449c70895f6f918c8641f26978a051cbc`  
		Last Modified: Fri, 14 Jan 2022 18:21:29 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:55a0277f92f8d6f6e6698de8e5bebe73eda01da0b19d25fcb7d2599b4082668a`  
		Last Modified: Fri, 14 Jan 2022 18:21:37 GMT  
		Size: 41.1 MB (41086508 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4994383046332c8f84b52a6efe15f1adb4c79a81f429f8dde7b0f778e9ae698`  
		Last Modified: Fri, 14 Jan 2022 18:21:29 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:04bf5ee831d9822e74be0b1aea3215bee1e25cbc8d5d1e311bc8238d0cb03d36`  
		Last Modified: Fri, 14 Jan 2022 18:21:30 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f2ee0a4e8fce601328442d907bc0ae97b9abc1db1792545dc2dcc58160941fe`  
		Last Modified: Fri, 14 Jan 2022 18:21:31 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:85dd664f02f096c9f08ff4c41e018594f19c653c4eead9319b3940f080abcba8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41686584 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:264f906141b220db7b1efedc81eaaa92ff9190309fe23cf66c8698c4d5c4d781`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:49:40 GMT
ARG CONSUL_VERSION=1.11.2
# Fri, 14 Jan 2022 18:49:40 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:49:41 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:49:42 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:50:03 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:50:05 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:50:06 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:50:07 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:50:07 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:50:08 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:50:08 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:50:08 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:50:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:50:09 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30dcb28bf192ed1024d353f25e4a3689ffb8bb91967c5e00583fee70bf62472b`  
		Last Modified: Fri, 14 Jan 2022 18:52:06 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3edf419af3148ed969571635ba7bc761a66cfdf6febb8d33d2d95985730d7f82`  
		Last Modified: Fri, 14 Jan 2022 18:52:27 GMT  
		Size: 39.0 MB (39049862 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c512c3c9dce0b9e275691cb879ce844bc98f103225becb9552f10140aa6d1828`  
		Last Modified: Fri, 14 Jan 2022 18:52:06 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b16ed7c4477a43a43fc613683db7a5272613294539e99660f35360765c4d775c`  
		Last Modified: Fri, 14 Jan 2022 18:52:06 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ac816b06f399c1de60e70010d546b71f72c435577fb3702e13df7cb4a9045de`  
		Last Modified: Fri, 14 Jan 2022 18:52:06 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:7df6609e86fb72a0f623ff21519798b5f06597cd77e79d3dde53c86eedbdecfb
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41520118 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6665c9735fea0297e8e98b868bada7f411f257b6f80dbdbfba7202bedc77f4ef`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:39:34 GMT
ARG CONSUL_VERSION=1.11.2
# Fri, 14 Jan 2022 18:39:35 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:39:36 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:39:37 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:39:53 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:39:54 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:39:55 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:39:56 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:39:57 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:39:58 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:39:59 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:40:01 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:40:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:40:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c038088c0871b6cf21d44268e04b69630960f81ea50cbac71923dd4d755f14a`  
		Last Modified: Fri, 14 Jan 2022 18:41:20 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177d0d5d31460160d580ecbb087e91a8c604280bf9cd67fa71e6eb71c1187226`  
		Last Modified: Fri, 14 Jan 2022 18:41:26 GMT  
		Size: 38.8 MB (38797162 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4ead2c6b0b970b32503ce0c0a48cf2eaeb73b73b5ddb6e983a920a5fd981674`  
		Last Modified: Fri, 14 Jan 2022 18:41:20 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3181d6b79134cda51bfa818e966e88da033a76fbacfee2814c19f7114eea5f9a`  
		Last Modified: Fri, 14 Jan 2022 18:41:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64c8e41024fb0d850e8d0342ab7a1fc601fe7f969b25025568ee70f7c751ca62`  
		Last Modified: Fri, 14 Jan 2022 18:41:20 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:b672e1c9fe1ec04b98b7cb1800f644040e3cb97620909596a44a8de4fefaf6f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.7 MB (42739521 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a189b84f78db958493dde80c50caadfac0ea78e78665ff4f900486c5110f8029`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:38:21 GMT
ARG CONSUL_VERSION=1.11.2
# Fri, 14 Jan 2022 18:38:21 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:38:21 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:38:22 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:38:40 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:38:41 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:38:42 GMT
# ARGS: CONSUL_VERSION=1.11.2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:38:42 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:38:42 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:38:42 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:38:43 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:38:43 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:38:43 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:38:43 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d07a80a7dcd4fb483db4f25b26c1d64781a879afdf19881ee21e39492d1c19a`  
		Last Modified: Fri, 14 Jan 2022 18:39:54 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1e4d8a7db54d5a040bd0de9cb53ef81e54b85467c7cf28dfcfbcab9e77b8f814`  
		Last Modified: Fri, 14 Jan 2022 18:40:01 GMT  
		Size: 39.9 MB (39907338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa81b02f5bcabefa538c0d28b3f5c967d8ae02a4cf63c79339cc9cb247f62f92`  
		Last Modified: Fri, 14 Jan 2022 18:39:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1b576f5f809c32f5a26dce7397652bed5be6edf758a5d9aa11d3a3aaf3a5a1d8`  
		Last Modified: Fri, 14 Jan 2022 18:39:55 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de12c7bf6eacb4afe5816dd4c13039dde42e3ff69154a2ea977e1af431b54b9c`  
		Last Modified: Fri, 14 Jan 2022 18:39:54 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
