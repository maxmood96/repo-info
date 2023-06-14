## `consul:latest`

```console
$ docker pull consul@sha256:5b94f657cb0f4424ae2b72252aa960581834bc57550fe80f9ee300e88412305f
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:3e1bd5bccd3e78b0aedb6c145ea6d5541f56d1a1156285a1323662367f52fc92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **60.7 MB (60732422 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a99d8a688dd368dfc01d7c582a58cce6499b05073367a431a0f1923ae1e75a37`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:19:33 GMT
ADD file:08ad6c1c886a26e30ae4ab103ff377ee6cfbc1be2437fa227ec28a335c63d78a in / 
# Wed, 29 Mar 2023 18:19:33 GMT
CMD ["/bin/sh"]
# Sun, 04 Jun 2023 17:39:56 GMT
ARG CONSUL_VERSION=1.15.3
# Sun, 04 Jun 2023 17:39:56 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sun, 04 Jun 2023 17:39:56 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sun, 04 Jun 2023 17:39:57 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Sun, 04 Jun 2023 17:40:03 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sun, 04 Jun 2023 17:40:04 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sun, 04 Jun 2023 17:40:04 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sun, 04 Jun 2023 17:40:04 GMT
VOLUME [/consul/data]
# Sun, 04 Jun 2023 17:40:04 GMT
EXPOSE 8300
# Sun, 04 Jun 2023 17:40:04 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sun, 04 Jun 2023 17:40:04 GMT
EXPOSE 8500 8600 8600/udp
# Sun, 04 Jun 2023 17:40:05 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Sun, 04 Jun 2023 17:40:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sun, 04 Jun 2023 17:40:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:0ce1dd7918a48990ab749aab2e805c26f691a3a8103495530e7ea5a1d168af4a`  
		Last Modified: Wed, 29 Mar 2023 18:20:17 GMT  
		Size: 2.8 MB (2826596 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b915e8f855b6690f0165f7483cef7426ea7282acab6c7b3702b3717021dd89a`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fab4e1ebead2514ccc0c2dbe58db284c6cf68996f3c4810d393e144eaccd0ab0`  
		Last Modified: Sun, 04 Jun 2023 17:40:25 GMT  
		Size: 57.9 MB (57902395 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fef376008726bca2cf9c89957ce3f2d98b94b8fe38125f5250510378ab918391`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d06ea914c246d6fc3771aef0af68d090aa389bace0ea5039e9814bc4fccccd3b`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:16c5462ee475b4cfd8b65edf36981eb63a7db89e1112e7939e1c26b79fbec28c`  
		Last Modified: Sun, 04 Jun 2023 17:40:19 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:ffc0b9ac394e56f9f3464d459d68491b0b87cf755ac047d3238f8031c6fc7548
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.4 MB (56396434 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:637faabcc495bd1314e04284dbfe69a8d2c5fce1fd748bd7b73e40271a43afb6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 18:01:13 GMT
ADD file:3fb55ad8134002858be264c3c2477d784e4a60f2f6501afa7cf3b10bfede51aa in / 
# Wed, 29 Mar 2023 18:01:13 GMT
CMD ["/bin/sh"]
# Fri, 02 Jun 2023 18:49:14 GMT
ARG CONSUL_VERSION=1.15.3
# Fri, 02 Jun 2023 18:49:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 02 Jun 2023 18:49:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 02 Jun 2023 18:49:15 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 02 Jun 2023 18:49:27 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 02 Jun 2023 18:49:28 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 02 Jun 2023 18:49:29 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 02 Jun 2023 18:49:29 GMT
VOLUME [/consul/data]
# Fri, 02 Jun 2023 18:49:29 GMT
EXPOSE 8300
# Fri, 02 Jun 2023 18:49:29 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 02 Jun 2023 18:49:29 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 02 Jun 2023 18:49:29 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jun 2023 18:49:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jun 2023 18:49:30 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:872c99a87729fa48dce303fb615edbb1a5da837f627a0b3d28495a0400ca8335`  
		Last Modified: Wed, 29 Mar 2023 18:02:12 GMT  
		Size: 2.6 MB (2634030 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eaed5ddc617d0eb1a14dae5dad411f7c5d20b584fe3f689ba445c1a0204dbeab`  
		Last Modified: Fri, 02 Jun 2023 18:49:44 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e1ad912b6763ca763bcd669566ef1af9dec649f9b2b8dc0af37f55c5ef58263a`  
		Last Modified: Fri, 02 Jun 2023 18:49:57 GMT  
		Size: 53.8 MB (53758972 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:476da9112b22e4239b61f986e54301aff2cd2b892b9c5cf84b6ef94381b2c44d`  
		Last Modified: Fri, 02 Jun 2023 18:49:44 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:deec611eb874877b4b97f4937d152d9c78150a6e77f4a08a243089130115b57c`  
		Last Modified: Fri, 02 Jun 2023 18:49:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2f7b1985432074aa9e1b042577f8edfef38cbb20bea5a0017ba682a762e8899d`  
		Last Modified: Fri, 02 Jun 2023 18:49:44 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:733356ad5c3089b578aaad28a9f2bbb31b220ac5f07e3fa008569ae458d15c04
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55564525 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6a85d69e11c0e9880128d4a99fa858fad196c1e933a34b6f0885502aca09164a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Jun 2023 20:49:10 GMT
ADD file:2b463f242cb7bf946452bb4781838348ecbe80da144fbab09f51d7e050dc68f3 in / 
# Wed, 14 Jun 2023 20:49:11 GMT
CMD ["/bin/sh"]
# Wed, 14 Jun 2023 22:38:06 GMT
ARG CONSUL_VERSION=1.15.3
# Wed, 14 Jun 2023 22:38:07 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Wed, 14 Jun 2023 22:38:07 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Wed, 14 Jun 2023 22:38:07 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Wed, 14 Jun 2023 22:38:13 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Wed, 14 Jun 2023 22:38:14 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Wed, 14 Jun 2023 22:38:14 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Wed, 14 Jun 2023 22:38:14 GMT
VOLUME [/consul/data]
# Wed, 14 Jun 2023 22:38:14 GMT
EXPOSE 8300
# Wed, 14 Jun 2023 22:38:15 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Wed, 14 Jun 2023 22:38:15 GMT
EXPOSE 8500 8600 8600/udp
# Wed, 14 Jun 2023 22:38:15 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Wed, 14 Jun 2023 22:38:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Wed, 14 Jun 2023 22:38:15 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:a147224bf413aeffbbfcdcb5104d35c647256a5c32083f4d8134f09a4e74ddeb`  
		Last Modified: Wed, 14 Jun 2023 20:49:52 GMT  
		Size: 2.7 MB (2720801 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2dd6ecb287f8b815309167e72faab910b64cb461ee06c98450cb4c084d0e9d4f`  
		Last Modified: Wed, 14 Jun 2023 22:38:47 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c82182ccdd08bc2d5e0f933a67cb0222fa72719c4dc5effd2e04ca976bb9a806`  
		Last Modified: Wed, 14 Jun 2023 22:38:52 GMT  
		Size: 52.8 MB (52840295 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89685cf8b3738470c953cfd090b45530b5acab8d954dbf7f225ec8ac2d93f1dc`  
		Last Modified: Wed, 14 Jun 2023 22:38:47 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7d34fe79a71e3ab6ab5fa8d70274cf1e5baa9167ded20425153a6ab99ff2f926`  
		Last Modified: Wed, 14 Jun 2023 22:38:48 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fdca9688632f01af824b8c4402a9a0380aac986343ae5ad4d9783c460a6d1ea5`  
		Last Modified: Wed, 14 Jun 2023 22:38:48 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:01b108a1a2a8326c056229a0a0632bf5d9a1aa5624fcf03d071b5b7cd65a1b92
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **59.3 MB (59272636 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a81b0671c7828f178893775dc3a974e950af0fb0ca6832cad2ccb775c5e25b0f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 29 Mar 2023 17:38:36 GMT
ADD file:fca96dde137b6b045359aec9d24257996738ac6cb7cce9518460a66802a27bd7 in / 
# Wed, 29 Mar 2023 17:38:36 GMT
CMD ["/bin/sh"]
# Fri, 02 Jun 2023 19:38:14 GMT
ARG CONSUL_VERSION=1.15.3
# Fri, 02 Jun 2023 19:38:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 02 Jun 2023 19:38:14 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 02 Jun 2023 19:38:15 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 02 Jun 2023 19:38:30 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 02 Jun 2023 19:38:31 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 02 Jun 2023 19:38:31 GMT
# ARGS: CONSUL_VERSION=1.15.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 02 Jun 2023 19:38:31 GMT
VOLUME [/consul/data]
# Fri, 02 Jun 2023 19:38:31 GMT
EXPOSE 8300
# Fri, 02 Jun 2023 19:38:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 02 Jun 2023 19:38:32 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 02 Jun 2023 19:38:32 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 02 Jun 2023 19:38:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 02 Jun 2023 19:38:32 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:333f5f619d7efe58316b2d71276f19d0a59bcb471f4dadaa85762b2c9e02775c`  
		Last Modified: Wed, 29 Mar 2023 17:39:19 GMT  
		Size: 2.8 MB (2832576 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4d32ca13c154fa47b1489aaa22373c89c457e0dc2749f7c49957951b934fdb62`  
		Last Modified: Fri, 02 Jun 2023 19:38:43 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c083da367850361ff166d595d2444cf0498464b453bf44a769713cd1a6774d1`  
		Last Modified: Fri, 02 Jun 2023 19:38:52 GMT  
		Size: 56.4 MB (56436631 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f5b5968913b40daee57281517d5f32722a7ee3954d3cc13ef610eeae053c79f3`  
		Last Modified: Fri, 02 Jun 2023 19:38:43 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:86bc4d621b13451b0f62bc5463f6474a46b43f0ad70e4d85931e1a2e1a662c13`  
		Last Modified: Fri, 02 Jun 2023 19:38:43 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:64a70266e0f7ce261d87f054a6dece387e39d558065144bf4379d9b1bfa7f630`  
		Last Modified: Fri, 02 Jun 2023 19:38:43 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
