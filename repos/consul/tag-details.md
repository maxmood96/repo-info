<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.10`](#consul110)
-	[`consul:1.10.9`](#consul1109)
-	[`consul:1.11`](#consul111)
-	[`consul:1.11.4`](#consul1114)
-	[`consul:1.9`](#consul19)
-	[`consul:1.9.16`](#consul1916)
-	[`consul:latest`](#consullatest)

## `consul:1.10`

```console
$ docker pull consul@sha256:95d1e6e3009d9858df048c14bf2ca88886c4f778c2f4e4f4bad5b15ddca2043c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10` - linux; amd64

```console
$ docker pull consul@sha256:17f53a8c175a98aa9b5d214b6c1c65dba74c84799891bb478533b915fe8662f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43749079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5fd65892192f381ecbbbae904bd17bc484cb299b26457d3b13766af273a68a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Tue, 01 Mar 2022 02:08:01 GMT
ARG CONSUL_VERSION=1.10.9
# Tue, 01 Mar 2022 02:08:01 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 01 Mar 2022 02:08:01 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 01 Mar 2022 02:08:02 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 01 Mar 2022 02:08:47 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 01 Mar 2022 02:08:47 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 01 Mar 2022 02:08:48 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Mar 2022 02:08:48 GMT
VOLUME [/consul/data]
# Tue, 01 Mar 2022 02:08:48 GMT
EXPOSE 8300
# Tue, 01 Mar 2022 02:08:48 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 01 Mar 2022 02:08:48 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 01 Mar 2022 02:08:48 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 01 Mar 2022 02:08:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:08:48 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3206213cb80b8563b090d7a3909c9823b121155bbb4f340924a98e4a96d6b7`  
		Last Modified: Tue, 01 Mar 2022 02:10:28 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64aa1b447a7a8b3a67a9c64c8f68c05894a4083f35ce5055f4543f02f038b06e`  
		Last Modified: Tue, 01 Mar 2022 02:10:34 GMT  
		Size: 40.9 MB (40923290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9f664ef6bc4b483b31613ca7d3d5f356ae34962216073bec1e08fc42e94dd8`  
		Last Modified: Tue, 01 Mar 2022 02:10:28 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a51dcd256c6437ce6c123728335285c0f0332d52e6d4c5651c1720643cdb15c`  
		Last Modified: Tue, 01 Mar 2022 02:10:28 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef16602b9a165c664d41e8e4227590dfe06a3df0471e29cf5ceefded15b17ee`  
		Last Modified: Tue, 01 Mar 2022 02:10:28 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm variant v6

```console
$ docker pull consul@sha256:113dabdbf5c2cb51df24729d5840fb6c7f816ed3b2023a6faf6fb5ccbaeda5ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41806201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8ae2c74d7d26813999b814ea5323c844a4f071c92bc978b99ac0003a536be1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:45 GMT
ADD file:85dfb53147cadaa6ec9595f75c71284523f862af4b9edb32c7f8ccebb0ef50a8 in / 
# Thu, 17 Mar 2022 14:32:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:01:54 GMT
ARG CONSUL_VERSION=1.10.9
# Thu, 17 Mar 2022 15:01:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 17 Mar 2022 15:01:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 17 Mar 2022 15:01:56 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 17 Mar 2022 15:02:25 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 17 Mar 2022 15:02:27 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 17 Mar 2022 15:02:28 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 15:02:29 GMT
VOLUME [/consul/data]
# Thu, 17 Mar 2022 15:02:29 GMT
EXPOSE 8300
# Thu, 17 Mar 2022 15:02:30 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 17 Mar 2022 15:02:30 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 17 Mar 2022 15:02:31 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 17 Mar 2022 15:02:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 15:02:31 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:84104bbf59c688eb09fa3dfa49f67ee18a001947cd8e75d4c8d09e92926d6b31`  
		Last Modified: Thu, 17 Mar 2022 14:34:22 GMT  
		Size: 2.6 MB (2627924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973431bb8cb6b431ddda12842fdb25ff83605f8d4ba530461b332a66e5cce059`  
		Last Modified: Thu, 17 Mar 2022 15:04:43 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edfaa24b3e799bad0740029a867b395d800f2a9d47fdf85888121ebf75501f6`  
		Last Modified: Thu, 17 Mar 2022 15:05:05 GMT  
		Size: 39.2 MB (39174901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d5d67ad40c156753ebbeb641bc6e25e616fadb2d38cbd74750c1cf53c3d6c4`  
		Last Modified: Thu, 17 Mar 2022 15:04:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473ccd6b631dbee3438b0730488ab227f541738dff775145ede51d4f47391f20`  
		Last Modified: Thu, 17 Mar 2022 15:04:43 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738f440dadea355e7787bceb157579978a3b1c1f5c2e2f219678caf0df14fb0b`  
		Last Modified: Thu, 17 Mar 2022 15:04:43 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:d9c30b12f708dd295f157bf8243528604264c96f9c7b7da096029ca4936da7ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41772654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf39ae1c6b8f991de1e118bf8c40b76a7f19ec277c6236173b971f422b5d3e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Tue, 01 Mar 2022 02:05:01 GMT
ARG CONSUL_VERSION=1.10.9
# Tue, 01 Mar 2022 02:05:02 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 01 Mar 2022 02:05:03 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 01 Mar 2022 02:05:04 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 01 Mar 2022 02:05:50 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 01 Mar 2022 02:05:50 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 01 Mar 2022 02:05:51 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Mar 2022 02:05:52 GMT
VOLUME [/consul/data]
# Tue, 01 Mar 2022 02:05:53 GMT
EXPOSE 8300
# Tue, 01 Mar 2022 02:05:54 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 01 Mar 2022 02:05:55 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 01 Mar 2022 02:05:57 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 01 Mar 2022 02:05:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:05:58 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898b6a3f2ff38bfc57f6d1de149d7231d678f13c3b6b0075b592238ab6979a07`  
		Last Modified: Tue, 01 Mar 2022 02:07:40 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216a34b3d798fd277c6fc735213c2fe435e0ba2d77d74b08752a72a0f2b09d79`  
		Last Modified: Tue, 01 Mar 2022 02:07:45 GMT  
		Size: 39.0 MB (39049699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e7159d6f79ac2852589bf74496e48e2e18ce25f62e55c9f4a551dc997fcefe`  
		Last Modified: Tue, 01 Mar 2022 02:07:40 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e5bda0b0788f1df277a571b497ced009a6901d2c72b7078383f0690a91218a`  
		Last Modified: Tue, 01 Mar 2022 02:07:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af5aebc2ffc00f16d63364367aac1f897d7b057d69771263d1a059d83663dcc`  
		Last Modified: Tue, 01 Mar 2022 02:07:40 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; 386

```console
$ docker pull consul@sha256:3628e720982924a4adc41322acb4d0287a78e657616bd2347ad628fd6cad280c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43118415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c9435c954bb6c2da729bdf46454f7994e03dc11de93e4fdd4c72b476615463`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Tue, 01 Mar 2022 02:03:19 GMT
ARG CONSUL_VERSION=1.10.9
# Tue, 01 Mar 2022 02:03:19 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 01 Mar 2022 02:03:19 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 01 Mar 2022 02:03:20 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 01 Mar 2022 02:04:02 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 01 Mar 2022 02:04:02 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 01 Mar 2022 02:04:03 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Mar 2022 02:04:03 GMT
VOLUME [/consul/data]
# Tue, 01 Mar 2022 02:04:03 GMT
EXPOSE 8300
# Tue, 01 Mar 2022 02:04:03 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 01 Mar 2022 02:04:03 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 01 Mar 2022 02:04:04 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 01 Mar 2022 02:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:04:04 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a70bc6500b8fd8b95656f886a61351fe8a789ef44cff8203160d2f33005fe23`  
		Last Modified: Tue, 01 Mar 2022 02:05:49 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7106cb8d848c66fa6cd8e95c324f354c3c8f83c29e4323148bc771b6b37d03`  
		Last Modified: Tue, 01 Mar 2022 02:05:56 GMT  
		Size: 40.3 MB (40286230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab99e66a59b6e871df5340969b2a3991037f6779bfd69ec88310964e956d7c1`  
		Last Modified: Tue, 01 Mar 2022 02:05:49 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2db7261b391bf2dda992288190e7d6bbfed0fc60637d9a36644c25c63fd76f4`  
		Last Modified: Tue, 01 Mar 2022 02:05:49 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d87d80a1bd5e92dc3d780a05181a64020c4252952364c0c576cfc29836a6174`  
		Last Modified: Tue, 01 Mar 2022 02:05:49 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.10.9`

```console
$ docker pull consul@sha256:95d1e6e3009d9858df048c14bf2ca88886c4f778c2f4e4f4bad5b15ddca2043c
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10.9` - linux; amd64

```console
$ docker pull consul@sha256:17f53a8c175a98aa9b5d214b6c1c65dba74c84799891bb478533b915fe8662f5
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43749079 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5fd65892192f381ecbbbae904bd17bc484cb299b26457d3b13766af273a68a1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Tue, 01 Mar 2022 02:08:01 GMT
ARG CONSUL_VERSION=1.10.9
# Tue, 01 Mar 2022 02:08:01 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 01 Mar 2022 02:08:01 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 01 Mar 2022 02:08:02 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 01 Mar 2022 02:08:47 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 01 Mar 2022 02:08:47 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 01 Mar 2022 02:08:48 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Mar 2022 02:08:48 GMT
VOLUME [/consul/data]
# Tue, 01 Mar 2022 02:08:48 GMT
EXPOSE 8300
# Tue, 01 Mar 2022 02:08:48 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 01 Mar 2022 02:08:48 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 01 Mar 2022 02:08:48 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 01 Mar 2022 02:08:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:08:48 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0f3206213cb80b8563b090d7a3909c9823b121155bbb4f340924a98e4a96d6b7`  
		Last Modified: Tue, 01 Mar 2022 02:10:28 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64aa1b447a7a8b3a67a9c64c8f68c05894a4083f35ce5055f4543f02f038b06e`  
		Last Modified: Tue, 01 Mar 2022 02:10:34 GMT  
		Size: 40.9 MB (40923290 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3e9f664ef6bc4b483b31613ca7d3d5f356ae34962216073bec1e08fc42e94dd8`  
		Last Modified: Tue, 01 Mar 2022 02:10:28 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4a51dcd256c6437ce6c123728335285c0f0332d52e6d4c5651c1720643cdb15c`  
		Last Modified: Tue, 01 Mar 2022 02:10:28 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ef16602b9a165c664d41e8e4227590dfe06a3df0471e29cf5ceefded15b17ee`  
		Last Modified: Tue, 01 Mar 2022 02:10:28 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:113dabdbf5c2cb51df24729d5840fb6c7f816ed3b2023a6faf6fb5ccbaeda5ae
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41806201 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ee8ae2c74d7d26813999b814ea5323c844a4f071c92bc978b99ac0003a536be1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:45 GMT
ADD file:85dfb53147cadaa6ec9595f75c71284523f862af4b9edb32c7f8ccebb0ef50a8 in / 
# Thu, 17 Mar 2022 14:32:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:01:54 GMT
ARG CONSUL_VERSION=1.10.9
# Thu, 17 Mar 2022 15:01:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 17 Mar 2022 15:01:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 17 Mar 2022 15:01:56 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 17 Mar 2022 15:02:25 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 17 Mar 2022 15:02:27 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 17 Mar 2022 15:02:28 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 15:02:29 GMT
VOLUME [/consul/data]
# Thu, 17 Mar 2022 15:02:29 GMT
EXPOSE 8300
# Thu, 17 Mar 2022 15:02:30 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 17 Mar 2022 15:02:30 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 17 Mar 2022 15:02:31 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 17 Mar 2022 15:02:31 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 15:02:31 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:84104bbf59c688eb09fa3dfa49f67ee18a001947cd8e75d4c8d09e92926d6b31`  
		Last Modified: Thu, 17 Mar 2022 14:34:22 GMT  
		Size: 2.6 MB (2627924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973431bb8cb6b431ddda12842fdb25ff83605f8d4ba530461b332a66e5cce059`  
		Last Modified: Thu, 17 Mar 2022 15:04:43 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7edfaa24b3e799bad0740029a867b395d800f2a9d47fdf85888121ebf75501f6`  
		Last Modified: Thu, 17 Mar 2022 15:05:05 GMT  
		Size: 39.2 MB (39174901 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86d5d67ad40c156753ebbeb641bc6e25e616fadb2d38cbd74750c1cf53c3d6c4`  
		Last Modified: Thu, 17 Mar 2022 15:04:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:473ccd6b631dbee3438b0730488ab227f541738dff775145ede51d4f47391f20`  
		Last Modified: Thu, 17 Mar 2022 15:04:43 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:738f440dadea355e7787bceb157579978a3b1c1f5c2e2f219678caf0df14fb0b`  
		Last Modified: Thu, 17 Mar 2022 15:04:43 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:d9c30b12f708dd295f157bf8243528604264c96f9c7b7da096029ca4936da7ed
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41772654 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bf39ae1c6b8f991de1e118bf8c40b76a7f19ec277c6236173b971f422b5d3e0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Tue, 01 Mar 2022 02:05:01 GMT
ARG CONSUL_VERSION=1.10.9
# Tue, 01 Mar 2022 02:05:02 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 01 Mar 2022 02:05:03 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 01 Mar 2022 02:05:04 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 01 Mar 2022 02:05:50 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 01 Mar 2022 02:05:50 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 01 Mar 2022 02:05:51 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Mar 2022 02:05:52 GMT
VOLUME [/consul/data]
# Tue, 01 Mar 2022 02:05:53 GMT
EXPOSE 8300
# Tue, 01 Mar 2022 02:05:54 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 01 Mar 2022 02:05:55 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 01 Mar 2022 02:05:57 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 01 Mar 2022 02:05:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:05:58 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:898b6a3f2ff38bfc57f6d1de149d7231d678f13c3b6b0075b592238ab6979a07`  
		Last Modified: Tue, 01 Mar 2022 02:07:40 GMT  
		Size: 1.2 KB (1231 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:216a34b3d798fd277c6fc735213c2fe435e0ba2d77d74b08752a72a0f2b09d79`  
		Last Modified: Tue, 01 Mar 2022 02:07:45 GMT  
		Size: 39.0 MB (39049699 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79e7159d6f79ac2852589bf74496e48e2e18ce25f62e55c9f4a551dc997fcefe`  
		Last Modified: Tue, 01 Mar 2022 02:07:40 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:60e5bda0b0788f1df277a571b497ced009a6901d2c72b7078383f0690a91218a`  
		Last Modified: Tue, 01 Mar 2022 02:07:40 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0af5aebc2ffc00f16d63364367aac1f897d7b057d69771263d1a059d83663dcc`  
		Last Modified: Tue, 01 Mar 2022 02:07:40 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.9` - linux; 386

```console
$ docker pull consul@sha256:3628e720982924a4adc41322acb4d0287a78e657616bd2347ad628fd6cad280c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43118415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d4c9435c954bb6c2da729bdf46454f7994e03dc11de93e4fdd4c72b476615463`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Tue, 01 Mar 2022 02:03:19 GMT
ARG CONSUL_VERSION=1.10.9
# Tue, 01 Mar 2022 02:03:19 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 01 Mar 2022 02:03:19 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 01 Mar 2022 02:03:20 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 01 Mar 2022 02:04:02 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 01 Mar 2022 02:04:02 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 01 Mar 2022 02:04:03 GMT
# ARGS: CONSUL_VERSION=1.10.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Mar 2022 02:04:03 GMT
VOLUME [/consul/data]
# Tue, 01 Mar 2022 02:04:03 GMT
EXPOSE 8300
# Tue, 01 Mar 2022 02:04:03 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 01 Mar 2022 02:04:03 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 01 Mar 2022 02:04:04 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 01 Mar 2022 02:04:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:04:04 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a70bc6500b8fd8b95656f886a61351fe8a789ef44cff8203160d2f33005fe23`  
		Last Modified: Tue, 01 Mar 2022 02:05:49 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c7106cb8d848c66fa6cd8e95c324f354c3c8f83c29e4323148bc771b6b37d03`  
		Last Modified: Tue, 01 Mar 2022 02:05:56 GMT  
		Size: 40.3 MB (40286230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ab99e66a59b6e871df5340969b2a3991037f6779bfd69ec88310964e956d7c1`  
		Last Modified: Tue, 01 Mar 2022 02:05:49 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2db7261b391bf2dda992288190e7d6bbfed0fc60637d9a36644c25c63fd76f4`  
		Last Modified: Tue, 01 Mar 2022 02:05:49 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d87d80a1bd5e92dc3d780a05181a64020c4252952364c0c576cfc29836a6174`  
		Last Modified: Tue, 01 Mar 2022 02:05:49 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.11`

```console
$ docker pull consul@sha256:47c97d29f37d1e7df0e4516ab3cb98048369429c9a5acd39e8cfa1834524a6cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.11` - linux; amd64

```console
$ docker pull consul@sha256:0dd8f7016f84462a841fdca73a9e58dc4f64ed33dc8f087acb2f1696f7f57bef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43947220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec96db0e7ba685574152bd300682c9cb8aaa545c9440f504eb7e21e695f46f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Tue, 01 Mar 2022 02:07:13 GMT
ARG CONSUL_VERSION=1.11.4
# Tue, 01 Mar 2022 02:07:13 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 01 Mar 2022 02:07:13 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 01 Mar 2022 02:07:14 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 01 Mar 2022 02:07:51 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 01 Mar 2022 02:07:52 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 01 Mar 2022 02:07:52 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Mar 2022 02:07:53 GMT
VOLUME [/consul/data]
# Tue, 01 Mar 2022 02:07:53 GMT
EXPOSE 8300
# Tue, 01 Mar 2022 02:07:53 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 01 Mar 2022 02:07:53 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 01 Mar 2022 02:07:53 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 01 Mar 2022 02:07:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:07:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a443d53d3f8ea4160ee69c8bade01d3a76db791c43aeec8a4df1632036bfdccc`  
		Last Modified: Tue, 01 Mar 2022 02:10:10 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddf97293f04383bdc3fca4bd3230f9e398d6f29bb085ea9256f0c4d4e479435`  
		Last Modified: Tue, 01 Mar 2022 02:10:16 GMT  
		Size: 41.1 MB (41121418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6560b30610da9f4ee48f7ef6ef1e67df4525600745350e46f1d33f9c6e9699c`  
		Last Modified: Tue, 01 Mar 2022 02:10:09 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26840f3e1ef52e9f78b48213767b49dcdc66df4a700358f287236b6054654203`  
		Last Modified: Tue, 01 Mar 2022 02:10:09 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48fe1e03676d1a884d8b15d685b0541f4b51159a3bb439844a027f9c9a34a281`  
		Last Modified: Tue, 01 Mar 2022 02:10:09 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11` - linux; arm variant v6

```console
$ docker pull consul@sha256:abf34e60affca0c66c7c3d14cb33629da18bbc0b8a3d4afc67da60f75b70ebeb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41706595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90c4a2d1cd3657045f42b44191a2a435e1c18d92642072739803fc5ea9e1d3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:45 GMT
ADD file:85dfb53147cadaa6ec9595f75c71284523f862af4b9edb32c7f8ccebb0ef50a8 in / 
# Thu, 17 Mar 2022 14:32:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:01:04 GMT
ARG CONSUL_VERSION=1.11.4
# Thu, 17 Mar 2022 15:01:04 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 17 Mar 2022 15:01:04 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 17 Mar 2022 15:01:06 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 17 Mar 2022 15:01:33 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 17 Mar 2022 15:01:35 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 17 Mar 2022 15:01:36 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 15:01:37 GMT
VOLUME [/consul/data]
# Thu, 17 Mar 2022 15:01:37 GMT
EXPOSE 8300
# Thu, 17 Mar 2022 15:01:38 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 17 Mar 2022 15:01:38 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 17 Mar 2022 15:01:38 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 17 Mar 2022 15:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 15:01:39 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:84104bbf59c688eb09fa3dfa49f67ee18a001947cd8e75d4c8d09e92926d6b31`  
		Last Modified: Thu, 17 Mar 2022 14:34:22 GMT  
		Size: 2.6 MB (2627924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b9c5bf708c984009dcf64d1f562e91fff73460ea160ca3e6d8834de6c5d64e2`  
		Last Modified: Thu, 17 Mar 2022 15:04:07 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2278ccd73c4449225c88fa7c1e01a3238466884d1614b87dc8943e3539f40a`  
		Last Modified: Thu, 17 Mar 2022 15:04:27 GMT  
		Size: 39.1 MB (39075299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430c6b92c0cee7151a7196b2d25e749a32a9ac97af68f404e66db04c6a24bb19`  
		Last Modified: Thu, 17 Mar 2022 15:04:06 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80895c4aa4b6075bdec5eb8c32c0134ff7b69b0908bd628e4758c8d455337b9b`  
		Last Modified: Thu, 17 Mar 2022 15:04:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3463c1727b45f270035d84ac880b1ba7bde5542753dca6bdc1b8eddabd04f064`  
		Last Modified: Thu, 17 Mar 2022 15:04:06 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:edb8537c3acc00645d048f7fe38b75e44f81cb8cf26c9bf097ece329a680e372
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41547360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1897d1eec7c3233f73f073fb0bb68911c10c7d860f151faed7a00ae27fa17c48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Tue, 01 Mar 2022 02:03:48 GMT
ARG CONSUL_VERSION=1.11.4
# Tue, 01 Mar 2022 02:03:49 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 01 Mar 2022 02:03:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 01 Mar 2022 02:03:51 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 01 Mar 2022 02:04:42 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 01 Mar 2022 02:04:42 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 01 Mar 2022 02:04:43 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Mar 2022 02:04:44 GMT
VOLUME [/consul/data]
# Tue, 01 Mar 2022 02:04:45 GMT
EXPOSE 8300
# Tue, 01 Mar 2022 02:04:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 01 Mar 2022 02:04:47 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 01 Mar 2022 02:04:49 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 01 Mar 2022 02:04:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:04:50 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1868b3065e523ec67a3abb01954e563f2d230fe576aa40a1d76005204fa75f`  
		Last Modified: Tue, 01 Mar 2022 02:07:20 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecaca720abadc7135975f7dc07aa13ef4bcef456790f581e71fbf0aaa1638ca`  
		Last Modified: Tue, 01 Mar 2022 02:07:26 GMT  
		Size: 38.8 MB (38824403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2789869782be34dc0e71e70cdd5d50d546b67dc96a86ca3ebfd7f1f3ff8a8d`  
		Last Modified: Tue, 01 Mar 2022 02:07:19 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a343cecaf2065ff33415187169e94b0553ca83d3854e2cc96ad37ea46bac9a`  
		Last Modified: Tue, 01 Mar 2022 02:07:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c48ccdfab507d057eb24f5b011958e13744f2ff3861cee7a7589ad285f9272a`  
		Last Modified: Tue, 01 Mar 2022 02:07:20 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11` - linux; 386

```console
$ docker pull consul@sha256:69768a50c60a117efaa10e04e0659e55d985a4db7a10dff1a3bb400fe749b273
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42771088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a43b9eae8ee2627bbab389826c22f9808779f3a4e4caa1aa88852478b912967`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Tue, 01 Mar 2022 02:02:09 GMT
ARG CONSUL_VERSION=1.11.4
# Tue, 01 Mar 2022 02:02:09 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 01 Mar 2022 02:02:09 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 01 Mar 2022 02:02:10 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 01 Mar 2022 02:03:03 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 01 Mar 2022 02:03:03 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 01 Mar 2022 02:03:04 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Mar 2022 02:03:04 GMT
VOLUME [/consul/data]
# Tue, 01 Mar 2022 02:03:04 GMT
EXPOSE 8300
# Tue, 01 Mar 2022 02:03:04 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 01 Mar 2022 02:03:04 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 01 Mar 2022 02:03:04 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 01 Mar 2022 02:03:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:03:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9511197d8c58e385cef16b6ebe4d92ea5c9b71a806edb0ec9b4f7e8e7c06d59f`  
		Last Modified: Tue, 01 Mar 2022 02:05:25 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed80181fb7718bb9dc52c775ecb1383acdf0efa7741d32185e2beefa273e1cd4`  
		Last Modified: Tue, 01 Mar 2022 02:05:33 GMT  
		Size: 39.9 MB (39938904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b097fcd480c2ad87b9b09d78159a35d11df7ad9ac8e5d7dc0660a94ca9d955aa`  
		Last Modified: Tue, 01 Mar 2022 02:05:25 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9022d17feed382bff697ebb156aaa949cac4b9efdbcc747155b41770283c2ea`  
		Last Modified: Tue, 01 Mar 2022 02:05:26 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611c003ed95e9356d5179651cd7c2446b77deeb98aa72498b9d830201e03722`  
		Last Modified: Tue, 01 Mar 2022 02:05:26 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.11.4`

```console
$ docker pull consul@sha256:47c97d29f37d1e7df0e4516ab3cb98048369429c9a5acd39e8cfa1834524a6cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.11.4` - linux; amd64

```console
$ docker pull consul@sha256:0dd8f7016f84462a841fdca73a9e58dc4f64ed33dc8f087acb2f1696f7f57bef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43947220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec96db0e7ba685574152bd300682c9cb8aaa545c9440f504eb7e21e695f46f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Tue, 01 Mar 2022 02:07:13 GMT
ARG CONSUL_VERSION=1.11.4
# Tue, 01 Mar 2022 02:07:13 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 01 Mar 2022 02:07:13 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 01 Mar 2022 02:07:14 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 01 Mar 2022 02:07:51 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 01 Mar 2022 02:07:52 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 01 Mar 2022 02:07:52 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Mar 2022 02:07:53 GMT
VOLUME [/consul/data]
# Tue, 01 Mar 2022 02:07:53 GMT
EXPOSE 8300
# Tue, 01 Mar 2022 02:07:53 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 01 Mar 2022 02:07:53 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 01 Mar 2022 02:07:53 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 01 Mar 2022 02:07:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:07:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a443d53d3f8ea4160ee69c8bade01d3a76db791c43aeec8a4df1632036bfdccc`  
		Last Modified: Tue, 01 Mar 2022 02:10:10 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddf97293f04383bdc3fca4bd3230f9e398d6f29bb085ea9256f0c4d4e479435`  
		Last Modified: Tue, 01 Mar 2022 02:10:16 GMT  
		Size: 41.1 MB (41121418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6560b30610da9f4ee48f7ef6ef1e67df4525600745350e46f1d33f9c6e9699c`  
		Last Modified: Tue, 01 Mar 2022 02:10:09 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26840f3e1ef52e9f78b48213767b49dcdc66df4a700358f287236b6054654203`  
		Last Modified: Tue, 01 Mar 2022 02:10:09 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48fe1e03676d1a884d8b15d685b0541f4b51159a3bb439844a027f9c9a34a281`  
		Last Modified: Tue, 01 Mar 2022 02:10:09 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.4` - linux; arm variant v6

```console
$ docker pull consul@sha256:abf34e60affca0c66c7c3d14cb33629da18bbc0b8a3d4afc67da60f75b70ebeb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41706595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90c4a2d1cd3657045f42b44191a2a435e1c18d92642072739803fc5ea9e1d3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:45 GMT
ADD file:85dfb53147cadaa6ec9595f75c71284523f862af4b9edb32c7f8ccebb0ef50a8 in / 
# Thu, 17 Mar 2022 14:32:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:01:04 GMT
ARG CONSUL_VERSION=1.11.4
# Thu, 17 Mar 2022 15:01:04 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 17 Mar 2022 15:01:04 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 17 Mar 2022 15:01:06 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 17 Mar 2022 15:01:33 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 17 Mar 2022 15:01:35 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 17 Mar 2022 15:01:36 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 15:01:37 GMT
VOLUME [/consul/data]
# Thu, 17 Mar 2022 15:01:37 GMT
EXPOSE 8300
# Thu, 17 Mar 2022 15:01:38 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 17 Mar 2022 15:01:38 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 17 Mar 2022 15:01:38 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 17 Mar 2022 15:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 15:01:39 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:84104bbf59c688eb09fa3dfa49f67ee18a001947cd8e75d4c8d09e92926d6b31`  
		Last Modified: Thu, 17 Mar 2022 14:34:22 GMT  
		Size: 2.6 MB (2627924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b9c5bf708c984009dcf64d1f562e91fff73460ea160ca3e6d8834de6c5d64e2`  
		Last Modified: Thu, 17 Mar 2022 15:04:07 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2278ccd73c4449225c88fa7c1e01a3238466884d1614b87dc8943e3539f40a`  
		Last Modified: Thu, 17 Mar 2022 15:04:27 GMT  
		Size: 39.1 MB (39075299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430c6b92c0cee7151a7196b2d25e749a32a9ac97af68f404e66db04c6a24bb19`  
		Last Modified: Thu, 17 Mar 2022 15:04:06 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80895c4aa4b6075bdec5eb8c32c0134ff7b69b0908bd628e4758c8d455337b9b`  
		Last Modified: Thu, 17 Mar 2022 15:04:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3463c1727b45f270035d84ac880b1ba7bde5542753dca6bdc1b8eddabd04f064`  
		Last Modified: Thu, 17 Mar 2022 15:04:06 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.4` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:edb8537c3acc00645d048f7fe38b75e44f81cb8cf26c9bf097ece329a680e372
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41547360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1897d1eec7c3233f73f073fb0bb68911c10c7d860f151faed7a00ae27fa17c48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Tue, 01 Mar 2022 02:03:48 GMT
ARG CONSUL_VERSION=1.11.4
# Tue, 01 Mar 2022 02:03:49 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 01 Mar 2022 02:03:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 01 Mar 2022 02:03:51 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 01 Mar 2022 02:04:42 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 01 Mar 2022 02:04:42 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 01 Mar 2022 02:04:43 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Mar 2022 02:04:44 GMT
VOLUME [/consul/data]
# Tue, 01 Mar 2022 02:04:45 GMT
EXPOSE 8300
# Tue, 01 Mar 2022 02:04:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 01 Mar 2022 02:04:47 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 01 Mar 2022 02:04:49 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 01 Mar 2022 02:04:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:04:50 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1868b3065e523ec67a3abb01954e563f2d230fe576aa40a1d76005204fa75f`  
		Last Modified: Tue, 01 Mar 2022 02:07:20 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecaca720abadc7135975f7dc07aa13ef4bcef456790f581e71fbf0aaa1638ca`  
		Last Modified: Tue, 01 Mar 2022 02:07:26 GMT  
		Size: 38.8 MB (38824403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2789869782be34dc0e71e70cdd5d50d546b67dc96a86ca3ebfd7f1f3ff8a8d`  
		Last Modified: Tue, 01 Mar 2022 02:07:19 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a343cecaf2065ff33415187169e94b0553ca83d3854e2cc96ad37ea46bac9a`  
		Last Modified: Tue, 01 Mar 2022 02:07:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c48ccdfab507d057eb24f5b011958e13744f2ff3861cee7a7589ad285f9272a`  
		Last Modified: Tue, 01 Mar 2022 02:07:20 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.4` - linux; 386

```console
$ docker pull consul@sha256:69768a50c60a117efaa10e04e0659e55d985a4db7a10dff1a3bb400fe749b273
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42771088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a43b9eae8ee2627bbab389826c22f9808779f3a4e4caa1aa88852478b912967`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Tue, 01 Mar 2022 02:02:09 GMT
ARG CONSUL_VERSION=1.11.4
# Tue, 01 Mar 2022 02:02:09 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 01 Mar 2022 02:02:09 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 01 Mar 2022 02:02:10 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 01 Mar 2022 02:03:03 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 01 Mar 2022 02:03:03 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 01 Mar 2022 02:03:04 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Mar 2022 02:03:04 GMT
VOLUME [/consul/data]
# Tue, 01 Mar 2022 02:03:04 GMT
EXPOSE 8300
# Tue, 01 Mar 2022 02:03:04 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 01 Mar 2022 02:03:04 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 01 Mar 2022 02:03:04 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 01 Mar 2022 02:03:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:03:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9511197d8c58e385cef16b6ebe4d92ea5c9b71a806edb0ec9b4f7e8e7c06d59f`  
		Last Modified: Tue, 01 Mar 2022 02:05:25 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed80181fb7718bb9dc52c775ecb1383acdf0efa7741d32185e2beefa273e1cd4`  
		Last Modified: Tue, 01 Mar 2022 02:05:33 GMT  
		Size: 39.9 MB (39938904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b097fcd480c2ad87b9b09d78159a35d11df7ad9ac8e5d7dc0660a94ca9d955aa`  
		Last Modified: Tue, 01 Mar 2022 02:05:25 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9022d17feed382bff697ebb156aaa949cac4b9efdbcc747155b41770283c2ea`  
		Last Modified: Tue, 01 Mar 2022 02:05:26 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611c003ed95e9356d5179651cd7c2446b77deeb98aa72498b9d830201e03722`  
		Last Modified: Tue, 01 Mar 2022 02:05:26 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9`

```console
$ docker pull consul@sha256:932c5583488fe7824769e74644d7ea1f7e51ef05cf00cea07db2ea32f02cec96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9` - linux; amd64

```console
$ docker pull consul@sha256:58223761c9e081382eacd41b97f451e7b8447ec0d589bfeb59c98e569cac53de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40156977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ce655101379df5daf5f5c6a8e7ed43f0b27067847a70c5e76c23a867d15cd6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Tue, 01 Mar 2022 02:08:59 GMT
ARG CONSUL_VERSION=1.9.16
# Tue, 01 Mar 2022 02:08:59 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 01 Mar 2022 02:08:59 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 01 Mar 2022 02:09:00 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 01 Mar 2022 02:09:44 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 01 Mar 2022 02:09:44 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 01 Mar 2022 02:09:45 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Mar 2022 02:09:45 GMT
VOLUME [/consul/data]
# Tue, 01 Mar 2022 02:09:45 GMT
EXPOSE 8300
# Tue, 01 Mar 2022 02:09:45 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 01 Mar 2022 02:09:45 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 01 Mar 2022 02:09:45 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 01 Mar 2022 02:09:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:09:45 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de20bec57603062f5c4d1e8fe6fc6b5504082f0ae0cad1f2200d236d420ec0ba`  
		Last Modified: Tue, 01 Mar 2022 02:10:44 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1510cc0bb728330a02cc28e451cad91b28222fc7ea8baba282c33a4dce768c`  
		Last Modified: Tue, 01 Mar 2022 02:10:50 GMT  
		Size: 37.3 MB (37331177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3441e72eaea91332d44c0b0741006a2ed972da3d4ba228abb3cc74bdd2ed3dd4`  
		Last Modified: Tue, 01 Mar 2022 02:10:44 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9bcbf580aa6574f0dcd72344b47b86330d30763282ff6c672a74b0066e61a66`  
		Last Modified: Tue, 01 Mar 2022 02:10:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d4581a629b5a9a1d062d04579a84311ad44a0877307397bc89386e9dd949b5`  
		Last Modified: Tue, 01 Mar 2022 02:10:44 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:8a1d9bc1fa91c78556f8d9eda80e34d7f4b1810ba50560d9efe583e84f32956a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38205080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201f6604c4d955de0069fc91b7530de3ca8572d3da8ba0166623e51b5b76801d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:45 GMT
ADD file:85dfb53147cadaa6ec9595f75c71284523f862af4b9edb32c7f8ccebb0ef50a8 in / 
# Thu, 17 Mar 2022 14:32:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:02:44 GMT
ARG CONSUL_VERSION=1.9.16
# Thu, 17 Mar 2022 15:02:45 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 17 Mar 2022 15:02:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 17 Mar 2022 15:02:47 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 17 Mar 2022 15:03:15 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 17 Mar 2022 15:03:16 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 17 Mar 2022 15:03:18 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 15:03:18 GMT
VOLUME [/consul/data]
# Thu, 17 Mar 2022 15:03:19 GMT
EXPOSE 8300
# Thu, 17 Mar 2022 15:03:19 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 17 Mar 2022 15:03:20 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 17 Mar 2022 15:03:20 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 17 Mar 2022 15:03:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 15:03:21 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:84104bbf59c688eb09fa3dfa49f67ee18a001947cd8e75d4c8d09e92926d6b31`  
		Last Modified: Thu, 17 Mar 2022 14:34:22 GMT  
		Size: 2.6 MB (2627924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca5a6486379980e79ce642f585ee3bd2ced7feccfcb63986b3022e78030208e`  
		Last Modified: Thu, 17 Mar 2022 15:05:18 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3163997b02164582d859f2aabd2033c0d724e9134786ee24879b69f800c742c`  
		Last Modified: Thu, 17 Mar 2022 15:05:36 GMT  
		Size: 35.6 MB (35573787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba661a8b1318f98603a54fa933125be61448a966e9a12705b44a24ab14b942a7`  
		Last Modified: Thu, 17 Mar 2022 15:05:18 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e026114e6b1612a5cdbf4543ece2f1931480a1bc0df978b4c4ff94f35796b8c`  
		Last Modified: Thu, 17 Mar 2022 15:05:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce093693994c134a364ff61cb65a0755b7c697f1cb778b06f4b2ae579ac82eb5`  
		Last Modified: Thu, 17 Mar 2022 15:05:18 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:bd21625e2548d8caf23f3adad843a1ffe6b06c8e778a94956d54819b2b132d3c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38168858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4e4a82fdfa06bdeec80229d3dc9806b20d27811f814d66685e604c219647ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Tue, 01 Mar 2022 02:06:03 GMT
ARG CONSUL_VERSION=1.9.16
# Tue, 01 Mar 2022 02:06:04 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 01 Mar 2022 02:06:05 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 01 Mar 2022 02:06:06 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 01 Mar 2022 02:06:43 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 01 Mar 2022 02:06:43 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 01 Mar 2022 02:06:44 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Mar 2022 02:06:45 GMT
VOLUME [/consul/data]
# Tue, 01 Mar 2022 02:06:46 GMT
EXPOSE 8300
# Tue, 01 Mar 2022 02:06:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 01 Mar 2022 02:06:48 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 01 Mar 2022 02:06:50 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 01 Mar 2022 02:06:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:06:51 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aaf6f45b756094bf280d5b1d5d0b24af03ccb596617748af1dd4497192252e7`  
		Last Modified: Tue, 01 Mar 2022 02:07:56 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2508d687ae17e81041f665794f705fb131da1b07e535cac20a366a5fac25773`  
		Last Modified: Tue, 01 Mar 2022 02:08:01 GMT  
		Size: 35.4 MB (35445904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1625d77484f8c0c66c46d5b4dc4ca8a35d7a46623378928829d5def95a5587`  
		Last Modified: Tue, 01 Mar 2022 02:07:56 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c226441a434e0c02604758abeee4548df30b5d3f675a41255ae4d7fef67bac6`  
		Last Modified: Tue, 01 Mar 2022 02:07:56 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b53625b273cc7cde0e8c2d3689a6cc17d04ce4e20d9553bde525b0a3778024d`  
		Last Modified: Tue, 01 Mar 2022 02:07:56 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; 386

```console
$ docker pull consul@sha256:f86c813984406d39d3991fd31e16bf8750caf291098b95c4109c8d14614f9557
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39515687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cecf06e370aec674af48da627037d681119af3dc13dbd91b6c6c8e2e068c297d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Tue, 01 Mar 2022 02:04:09 GMT
ARG CONSUL_VERSION=1.9.16
# Tue, 01 Mar 2022 02:04:09 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 01 Mar 2022 02:04:09 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 01 Mar 2022 02:04:10 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 01 Mar 2022 02:04:55 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 01 Mar 2022 02:04:56 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 01 Mar 2022 02:04:56 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Mar 2022 02:04:56 GMT
VOLUME [/consul/data]
# Tue, 01 Mar 2022 02:04:56 GMT
EXPOSE 8300
# Tue, 01 Mar 2022 02:04:57 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 01 Mar 2022 02:04:57 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 01 Mar 2022 02:04:57 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 01 Mar 2022 02:04:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:04:57 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfc7f9e90e738f44b615eb913a41ca3c06f9e9f644aa8ae7367108a487a4013`  
		Last Modified: Tue, 01 Mar 2022 02:06:07 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36ed7bb130b98d5b3941286a3b18e66106de11ab8fba756aefee5972065bd2f`  
		Last Modified: Tue, 01 Mar 2022 02:06:14 GMT  
		Size: 36.7 MB (36683502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545729e55c0df18e4995e742baa7a802e73eeca61e14358d588769aad6749a0a`  
		Last Modified: Tue, 01 Mar 2022 02:06:07 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598812672afaa386e0f3fb63af60ed9158615d9c828f0d21641df8d4c516b29`  
		Last Modified: Tue, 01 Mar 2022 02:06:07 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c5062862aa77b9344e5a9cd395108ff566cd5cad5bf0d6f80d6f26cdd31a0`  
		Last Modified: Tue, 01 Mar 2022 02:06:07 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9.16`

```console
$ docker pull consul@sha256:932c5583488fe7824769e74644d7ea1f7e51ef05cf00cea07db2ea32f02cec96
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9.16` - linux; amd64

```console
$ docker pull consul@sha256:58223761c9e081382eacd41b97f451e7b8447ec0d589bfeb59c98e569cac53de
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40156977 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:61ce655101379df5daf5f5c6a8e7ed43f0b27067847a70c5e76c23a867d15cd6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Tue, 01 Mar 2022 02:08:59 GMT
ARG CONSUL_VERSION=1.9.16
# Tue, 01 Mar 2022 02:08:59 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 01 Mar 2022 02:08:59 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 01 Mar 2022 02:09:00 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 01 Mar 2022 02:09:44 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 01 Mar 2022 02:09:44 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 01 Mar 2022 02:09:45 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Mar 2022 02:09:45 GMT
VOLUME [/consul/data]
# Tue, 01 Mar 2022 02:09:45 GMT
EXPOSE 8300
# Tue, 01 Mar 2022 02:09:45 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 01 Mar 2022 02:09:45 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 01 Mar 2022 02:09:45 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 01 Mar 2022 02:09:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:09:45 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de20bec57603062f5c4d1e8fe6fc6b5504082f0ae0cad1f2200d236d420ec0ba`  
		Last Modified: Tue, 01 Mar 2022 02:10:44 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c1510cc0bb728330a02cc28e451cad91b28222fc7ea8baba282c33a4dce768c`  
		Last Modified: Tue, 01 Mar 2022 02:10:50 GMT  
		Size: 37.3 MB (37331177 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3441e72eaea91332d44c0b0741006a2ed972da3d4ba228abb3cc74bdd2ed3dd4`  
		Last Modified: Tue, 01 Mar 2022 02:10:44 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e9bcbf580aa6574f0dcd72344b47b86330d30763282ff6c672a74b0066e61a66`  
		Last Modified: Tue, 01 Mar 2022 02:10:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d4581a629b5a9a1d062d04579a84311ad44a0877307397bc89386e9dd949b5`  
		Last Modified: Tue, 01 Mar 2022 02:10:44 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.16` - linux; arm variant v6

```console
$ docker pull consul@sha256:8a1d9bc1fa91c78556f8d9eda80e34d7f4b1810ba50560d9efe583e84f32956a
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38205080 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:201f6604c4d955de0069fc91b7530de3ca8572d3da8ba0166623e51b5b76801d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:45 GMT
ADD file:85dfb53147cadaa6ec9595f75c71284523f862af4b9edb32c7f8ccebb0ef50a8 in / 
# Thu, 17 Mar 2022 14:32:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:02:44 GMT
ARG CONSUL_VERSION=1.9.16
# Thu, 17 Mar 2022 15:02:45 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 17 Mar 2022 15:02:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 17 Mar 2022 15:02:47 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 17 Mar 2022 15:03:15 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 17 Mar 2022 15:03:16 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 17 Mar 2022 15:03:18 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 15:03:18 GMT
VOLUME [/consul/data]
# Thu, 17 Mar 2022 15:03:19 GMT
EXPOSE 8300
# Thu, 17 Mar 2022 15:03:19 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 17 Mar 2022 15:03:20 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 17 Mar 2022 15:03:20 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 17 Mar 2022 15:03:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 15:03:21 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:84104bbf59c688eb09fa3dfa49f67ee18a001947cd8e75d4c8d09e92926d6b31`  
		Last Modified: Thu, 17 Mar 2022 14:34:22 GMT  
		Size: 2.6 MB (2627924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bca5a6486379980e79ce642f585ee3bd2ced7feccfcb63986b3022e78030208e`  
		Last Modified: Thu, 17 Mar 2022 15:05:18 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c3163997b02164582d859f2aabd2033c0d724e9134786ee24879b69f800c742c`  
		Last Modified: Thu, 17 Mar 2022 15:05:36 GMT  
		Size: 35.6 MB (35573787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba661a8b1318f98603a54fa933125be61448a966e9a12705b44a24ab14b942a7`  
		Last Modified: Thu, 17 Mar 2022 15:05:18 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e026114e6b1612a5cdbf4543ece2f1931480a1bc0df978b4c4ff94f35796b8c`  
		Last Modified: Thu, 17 Mar 2022 15:05:18 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce093693994c134a364ff61cb65a0755b7c697f1cb778b06f4b2ae579ac82eb5`  
		Last Modified: Thu, 17 Mar 2022 15:05:18 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.16` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:bd21625e2548d8caf23f3adad843a1ffe6b06c8e778a94956d54819b2b132d3c
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38168858 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0d4e4a82fdfa06bdeec80229d3dc9806b20d27811f814d66685e604c219647ab`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Tue, 01 Mar 2022 02:06:03 GMT
ARG CONSUL_VERSION=1.9.16
# Tue, 01 Mar 2022 02:06:04 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 01 Mar 2022 02:06:05 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 01 Mar 2022 02:06:06 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 01 Mar 2022 02:06:43 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 01 Mar 2022 02:06:43 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 01 Mar 2022 02:06:44 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Mar 2022 02:06:45 GMT
VOLUME [/consul/data]
# Tue, 01 Mar 2022 02:06:46 GMT
EXPOSE 8300
# Tue, 01 Mar 2022 02:06:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 01 Mar 2022 02:06:48 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 01 Mar 2022 02:06:50 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 01 Mar 2022 02:06:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:06:51 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5aaf6f45b756094bf280d5b1d5d0b24af03ccb596617748af1dd4497192252e7`  
		Last Modified: Tue, 01 Mar 2022 02:07:56 GMT  
		Size: 1.2 KB (1233 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2508d687ae17e81041f665794f705fb131da1b07e535cac20a366a5fac25773`  
		Last Modified: Tue, 01 Mar 2022 02:08:01 GMT  
		Size: 35.4 MB (35445904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bf1625d77484f8c0c66c46d5b4dc4ca8a35d7a46623378928829d5def95a5587`  
		Last Modified: Tue, 01 Mar 2022 02:07:56 GMT  
		Size: 143.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c226441a434e0c02604758abeee4548df30b5d3f675a41255ae4d7fef67bac6`  
		Last Modified: Tue, 01 Mar 2022 02:07:56 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b53625b273cc7cde0e8c2d3689a6cc17d04ce4e20d9553bde525b0a3778024d`  
		Last Modified: Tue, 01 Mar 2022 02:07:56 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.16` - linux; 386

```console
$ docker pull consul@sha256:f86c813984406d39d3991fd31e16bf8750caf291098b95c4109c8d14614f9557
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39515687 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cecf06e370aec674af48da627037d681119af3dc13dbd91b6c6c8e2e068c297d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Tue, 01 Mar 2022 02:04:09 GMT
ARG CONSUL_VERSION=1.9.16
# Tue, 01 Mar 2022 02:04:09 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 01 Mar 2022 02:04:09 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 01 Mar 2022 02:04:10 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 01 Mar 2022 02:04:55 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 01 Mar 2022 02:04:56 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 01 Mar 2022 02:04:56 GMT
# ARGS: CONSUL_VERSION=1.9.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Mar 2022 02:04:56 GMT
VOLUME [/consul/data]
# Tue, 01 Mar 2022 02:04:56 GMT
EXPOSE 8300
# Tue, 01 Mar 2022 02:04:57 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 01 Mar 2022 02:04:57 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 01 Mar 2022 02:04:57 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 01 Mar 2022 02:04:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:04:57 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cfc7f9e90e738f44b615eb913a41ca3c06f9e9f644aa8ae7367108a487a4013`  
		Last Modified: Tue, 01 Mar 2022 02:06:07 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d36ed7bb130b98d5b3941286a3b18e66106de11ab8fba756aefee5972065bd2f`  
		Last Modified: Tue, 01 Mar 2022 02:06:14 GMT  
		Size: 36.7 MB (36683502 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:545729e55c0df18e4995e742baa7a802e73eeca61e14358d588769aad6749a0a`  
		Last Modified: Tue, 01 Mar 2022 02:06:07 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0598812672afaa386e0f3fb63af60ed9158615d9c828f0d21641df8d4c516b29`  
		Last Modified: Tue, 01 Mar 2022 02:06:07 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee9c5062862aa77b9344e5a9cd395108ff566cd5cad5bf0d6f80d6f26cdd31a0`  
		Last Modified: Tue, 01 Mar 2022 02:06:07 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:47c97d29f37d1e7df0e4516ab3cb98048369429c9a5acd39e8cfa1834524a6cf
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:0dd8f7016f84462a841fdca73a9e58dc4f64ed33dc8f087acb2f1696f7f57bef
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.9 MB (43947220 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:aec96db0e7ba685574152bd300682c9cb8aaa545c9440f504eb7e21e695f46f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Tue, 01 Mar 2022 02:07:13 GMT
ARG CONSUL_VERSION=1.11.4
# Tue, 01 Mar 2022 02:07:13 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 01 Mar 2022 02:07:13 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 01 Mar 2022 02:07:14 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 01 Mar 2022 02:07:51 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 01 Mar 2022 02:07:52 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 01 Mar 2022 02:07:52 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Mar 2022 02:07:53 GMT
VOLUME [/consul/data]
# Tue, 01 Mar 2022 02:07:53 GMT
EXPOSE 8300
# Tue, 01 Mar 2022 02:07:53 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 01 Mar 2022 02:07:53 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 01 Mar 2022 02:07:53 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 01 Mar 2022 02:07:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:07:53 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a443d53d3f8ea4160ee69c8bade01d3a76db791c43aeec8a4df1632036bfdccc`  
		Last Modified: Tue, 01 Mar 2022 02:10:10 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eddf97293f04383bdc3fca4bd3230f9e398d6f29bb085ea9256f0c4d4e479435`  
		Last Modified: Tue, 01 Mar 2022 02:10:16 GMT  
		Size: 41.1 MB (41121418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c6560b30610da9f4ee48f7ef6ef1e67df4525600745350e46f1d33f9c6e9699c`  
		Last Modified: Tue, 01 Mar 2022 02:10:09 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26840f3e1ef52e9f78b48213767b49dcdc66df4a700358f287236b6054654203`  
		Last Modified: Tue, 01 Mar 2022 02:10:09 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48fe1e03676d1a884d8b15d685b0541f4b51159a3bb439844a027f9c9a34a281`  
		Last Modified: Tue, 01 Mar 2022 02:10:09 GMT  
		Size: 1.8 KB (1790 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:abf34e60affca0c66c7c3d14cb33629da18bbc0b8a3d4afc67da60f75b70ebeb
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41706595 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e90c4a2d1cd3657045f42b44191a2a435e1c18d92642072739803fc5ea9e1d3a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 17 Mar 2022 14:32:45 GMT
ADD file:85dfb53147cadaa6ec9595f75c71284523f862af4b9edb32c7f8ccebb0ef50a8 in / 
# Thu, 17 Mar 2022 14:32:45 GMT
CMD ["/bin/sh"]
# Thu, 17 Mar 2022 15:01:04 GMT
ARG CONSUL_VERSION=1.11.4
# Thu, 17 Mar 2022 15:01:04 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Thu, 17 Mar 2022 15:01:04 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Thu, 17 Mar 2022 15:01:06 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Thu, 17 Mar 2022 15:01:33 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Thu, 17 Mar 2022 15:01:35 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Thu, 17 Mar 2022 15:01:36 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Thu, 17 Mar 2022 15:01:37 GMT
VOLUME [/consul/data]
# Thu, 17 Mar 2022 15:01:37 GMT
EXPOSE 8300
# Thu, 17 Mar 2022 15:01:38 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Thu, 17 Mar 2022 15:01:38 GMT
EXPOSE 8500 8600 8600/udp
# Thu, 17 Mar 2022 15:01:38 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Thu, 17 Mar 2022 15:01:39 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Thu, 17 Mar 2022 15:01:39 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:84104bbf59c688eb09fa3dfa49f67ee18a001947cd8e75d4c8d09e92926d6b31`  
		Last Modified: Thu, 17 Mar 2022 14:34:22 GMT  
		Size: 2.6 MB (2627924 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7b9c5bf708c984009dcf64d1f562e91fff73460ea160ca3e6d8834de6c5d64e2`  
		Last Modified: Thu, 17 Mar 2022 15:04:07 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8c2278ccd73c4449225c88fa7c1e01a3238466884d1614b87dc8943e3539f40a`  
		Last Modified: Thu, 17 Mar 2022 15:04:27 GMT  
		Size: 39.1 MB (39075299 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:430c6b92c0cee7151a7196b2d25e749a32a9ac97af68f404e66db04c6a24bb19`  
		Last Modified: Thu, 17 Mar 2022 15:04:06 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:80895c4aa4b6075bdec5eb8c32c0134ff7b69b0908bd628e4758c8d455337b9b`  
		Last Modified: Thu, 17 Mar 2022 15:04:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3463c1727b45f270035d84ac880b1ba7bde5542753dca6bdc1b8eddabd04f064`  
		Last Modified: Thu, 17 Mar 2022 15:04:06 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:edb8537c3acc00645d048f7fe38b75e44f81cb8cf26c9bf097ece329a680e372
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41547360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:1897d1eec7c3233f73f073fb0bb68911c10c7d860f151faed7a00ae27fa17c48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Tue, 01 Mar 2022 02:03:48 GMT
ARG CONSUL_VERSION=1.11.4
# Tue, 01 Mar 2022 02:03:49 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 01 Mar 2022 02:03:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 01 Mar 2022 02:03:51 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 01 Mar 2022 02:04:42 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 01 Mar 2022 02:04:42 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 01 Mar 2022 02:04:43 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Mar 2022 02:04:44 GMT
VOLUME [/consul/data]
# Tue, 01 Mar 2022 02:04:45 GMT
EXPOSE 8300
# Tue, 01 Mar 2022 02:04:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 01 Mar 2022 02:04:47 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 01 Mar 2022 02:04:49 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 01 Mar 2022 02:04:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:04:50 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c1868b3065e523ec67a3abb01954e563f2d230fe576aa40a1d76005204fa75f`  
		Last Modified: Tue, 01 Mar 2022 02:07:20 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ecaca720abadc7135975f7dc07aa13ef4bcef456790f581e71fbf0aaa1638ca`  
		Last Modified: Tue, 01 Mar 2022 02:07:26 GMT  
		Size: 38.8 MB (38824403 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7a2789869782be34dc0e71e70cdd5d50d546b67dc96a86ca3ebfd7f1f3ff8a8d`  
		Last Modified: Tue, 01 Mar 2022 02:07:19 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11a343cecaf2065ff33415187169e94b0553ca83d3854e2cc96ad37ea46bac9a`  
		Last Modified: Tue, 01 Mar 2022 02:07:19 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c48ccdfab507d057eb24f5b011958e13744f2ff3861cee7a7589ad285f9272a`  
		Last Modified: Tue, 01 Mar 2022 02:07:20 GMT  
		Size: 1.8 KB (1789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:69768a50c60a117efaa10e04e0659e55d985a4db7a10dff1a3bb400fe749b273
```

-	Docker Version: 20.10.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42771088 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a43b9eae8ee2627bbab389826c22f9808779f3a4e4caa1aa88852478b912967`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Tue, 01 Mar 2022 02:02:09 GMT
ARG CONSUL_VERSION=1.11.4
# Tue, 01 Mar 2022 02:02:09 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 01 Mar 2022 02:02:09 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 01 Mar 2022 02:02:10 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 01 Mar 2022 02:03:03 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 01 Mar 2022 02:03:03 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 01 Mar 2022 02:03:04 GMT
# ARGS: CONSUL_VERSION=1.11.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 01 Mar 2022 02:03:04 GMT
VOLUME [/consul/data]
# Tue, 01 Mar 2022 02:03:04 GMT
EXPOSE 8300
# Tue, 01 Mar 2022 02:03:04 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 01 Mar 2022 02:03:04 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 01 Mar 2022 02:03:04 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 01 Mar 2022 02:03:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 01 Mar 2022 02:03:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9511197d8c58e385cef16b6ebe4d92ea5c9b71a806edb0ec9b4f7e8e7c06d59f`  
		Last Modified: Tue, 01 Mar 2022 02:05:25 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ed80181fb7718bb9dc52c775ecb1383acdf0efa7741d32185e2beefa273e1cd4`  
		Last Modified: Tue, 01 Mar 2022 02:05:33 GMT  
		Size: 39.9 MB (39938904 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b097fcd480c2ad87b9b09d78159a35d11df7ad9ac8e5d7dc0660a94ca9d955aa`  
		Last Modified: Tue, 01 Mar 2022 02:05:25 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c9022d17feed382bff697ebb156aaa949cac4b9efdbcc747155b41770283c2ea`  
		Last Modified: Tue, 01 Mar 2022 02:05:26 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5611c003ed95e9356d5179651cd7c2446b77deeb98aa72498b9d830201e03722`  
		Last Modified: Tue, 01 Mar 2022 02:05:26 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
