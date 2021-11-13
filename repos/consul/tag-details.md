<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.10`](#consul110)
-	[`consul:1.10.3`](#consul1103)
-	[`consul:1.11.0-beta`](#consul1110-beta)
-	[`consul:1.11.0-beta2`](#consul1110-beta2)
-	[`consul:1.8`](#consul18)
-	[`consul:1.8.16`](#consul1816)
-	[`consul:1.9`](#consul19)
-	[`consul:1.9.10`](#consul1910)
-	[`consul:latest`](#consullatest)

## `consul:1.10`

```console
$ docker pull consul@sha256:9806c8b77144ec19d594bf6d8a6e04634ebe63a2d734539c484bbe0d10b8e6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10` - linux; amd64

```console
$ docker pull consul@sha256:4fc771d6614f6d7af92653e006157b9c98a05098e43dc485d29d9c846abcc33d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43242800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9814b25e52bae10d44d9953bad57d86e8577283652bc9443be9738031389c48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:58:14 GMT
ARG CONSUL_VERSION=1.10.3
# Fri, 12 Nov 2021 21:58:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 12 Nov 2021 21:58:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 12 Nov 2021 21:58:17 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 12 Nov 2021 21:58:30 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 12 Nov 2021 21:58:32 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 12 Nov 2021 21:58:35 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:58:35 GMT
VOLUME [/consul/data]
# Fri, 12 Nov 2021 21:58:36 GMT
EXPOSE 8300
# Fri, 12 Nov 2021 21:58:36 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 12 Nov 2021 21:58:36 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 12 Nov 2021 21:58:37 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 21:58:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 21:58:38 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79efaa79e0b89d613b7eeb02676f2c706bf77bac920e8657f0f9badfb6205340`  
		Last Modified: Fri, 12 Nov 2021 22:00:01 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b6fccdd38073e2a0303fb7450154fb88dd5211f8abbd8ab1b55e2514a24cb1`  
		Last Modified: Fri, 12 Nov 2021 22:00:07 GMT  
		Size: 40.4 MB (40417007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a1a23e6dad553737585a3b60948d19896dd3c8aeb3ec7e62e0bf03560f416e`  
		Last Modified: Fri, 12 Nov 2021 22:00:01 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae16349669345cc0fb16abc18cd48c1dbf94910caaee5431326c3cf34882559`  
		Last Modified: Fri, 12 Nov 2021 22:00:01 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96fa79365c2a7793d97996a84e1a8e28dec95f530224a746f6d4cdca6dfe5f73`  
		Last Modified: Fri, 12 Nov 2021 22:00:01 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm variant v6

```console
$ docker pull consul@sha256:89cd92136a7b8ebd035cb1a0e39b8e96abc49edf60c9200a27f117054b53932c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39269139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4b0d9415b5a09650d466ee78ea76f2f5f821de5e796590f9339aa0c50e30b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:03:14 GMT
ARG CONSUL_VERSION=1.10.3
# Sat, 13 Nov 2021 06:03:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 13 Nov 2021 06:03:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 13 Nov 2021 06:03:17 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 13 Nov 2021 06:03:29 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 13 Nov 2021 06:03:31 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 13 Nov 2021 06:03:33 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 06:03:34 GMT
VOLUME [/consul/data]
# Sat, 13 Nov 2021 06:03:34 GMT
EXPOSE 8300
# Sat, 13 Nov 2021 06:03:35 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 13 Nov 2021 06:03:35 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 13 Nov 2021 06:03:36 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Nov 2021 06:03:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 06:03:37 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95e092b4de70f76b87ef5e2952153af28de56b56c428d170b0f028fb6afbf1d`  
		Last Modified: Sat, 13 Nov 2021 06:06:08 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598923641df439f939be74ba7dc244ef98d48641e316ff947702b24a279c956d`  
		Last Modified: Sat, 13 Nov 2021 06:06:27 GMT  
		Size: 36.6 MB (36632428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b856a08c888ad010360a1dd58e1196cab9d0a174889c005fd0dd1c23a5225c4`  
		Last Modified: Sat, 13 Nov 2021 06:06:08 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4ced118232a40da2c756413e2ca1148a45efc645d9f750f232a1dcd7f945f`  
		Last Modified: Sat, 13 Nov 2021 06:06:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e826ae63c559c7b16801bd6e94f70546fbf8739bbb8a33eae3edd323fd2797b7`  
		Last Modified: Sat, 13 Nov 2021 06:06:08 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:34988991d554ab9d710529135c77747ba808b12654d1062c5811cb3465078221
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39190366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d494725d24cc77ece20111697554c7e44d02326ac63bac482f6c5c7c520a427c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Tue, 02 Nov 2021 19:39:58 GMT
ARG CONSUL_VERSION=1.10.3
# Tue, 02 Nov 2021 19:39:59 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 02 Nov 2021 19:40:00 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 02 Nov 2021 19:40:01 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 02 Nov 2021 19:40:14 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 02 Nov 2021 19:40:15 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 02 Nov 2021 19:40:16 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 02 Nov 2021 19:40:17 GMT
VOLUME [/consul/data]
# Tue, 02 Nov 2021 19:40:18 GMT
EXPOSE 8300
# Tue, 02 Nov 2021 19:40:19 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 02 Nov 2021 19:40:20 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 02 Nov 2021 19:40:22 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 02 Nov 2021 19:40:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Nov 2021 19:40:23 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37670a2a9dc09fe75ad47ca2b119cfaed5f2978da6f457430dee234dada7ea43`  
		Last Modified: Tue, 02 Nov 2021 19:42:09 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919087a5490ea994435e800db080ee62a36ba94db46d8b2279447371e06648ad`  
		Last Modified: Tue, 02 Nov 2021 19:42:14 GMT  
		Size: 36.5 MB (36474046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b44e0042b56affa731efc3552e6d27a1c1a27c113ef7c2303abe8fb4a8c6c2`  
		Last Modified: Tue, 02 Nov 2021 19:42:09 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b020cd44b1a8b856d502623a20f69a02ed6f581b1955a5951159a088820f6052`  
		Last Modified: Tue, 02 Nov 2021 19:42:09 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43e375f5a466436cb3909f15c21a61e93bf531c521f1ba1b6bb737296f910fa`  
		Last Modified: Tue, 02 Nov 2021 19:42:09 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; 386

```console
$ docker pull consul@sha256:f6d4990606abae58cfa07041438a83774585b1976889aa17ecfb69c10582149d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42624588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0266e05a345c091de13c2cf497e8d5c997539a31384988e30a540f6338d8e095`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:18:54 GMT
ARG CONSUL_VERSION=1.10.3
# Sat, 13 Nov 2021 06:18:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 13 Nov 2021 06:18:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 13 Nov 2021 06:18:56 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 13 Nov 2021 06:19:06 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 13 Nov 2021 06:19:07 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 13 Nov 2021 06:19:08 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 06:19:08 GMT
VOLUME [/consul/data]
# Sat, 13 Nov 2021 06:19:08 GMT
EXPOSE 8300
# Sat, 13 Nov 2021 06:19:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 13 Nov 2021 06:19:09 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 13 Nov 2021 06:19:09 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Nov 2021 06:19:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 06:19:10 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ad71c51a3aaa36ca93ff2d29be265437f8d6a6a3265229463a32d757ab063c`  
		Last Modified: Sat, 13 Nov 2021 06:20:36 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264e1a84ec19e245b5b17560ae89a7a20d673c5065b8e31ad33e1dec79c3a5fc`  
		Last Modified: Sat, 13 Nov 2021 06:20:42 GMT  
		Size: 39.8 MB (39792406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52249b1ddd029a0a2974e3e28a7d4ba4eb74ba1428eba364aab8c0634680193`  
		Last Modified: Sat, 13 Nov 2021 06:20:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1e3c995ef13035d9e1361df724e4dbb2f695c7fdf5a1a5dac866ececfd2f54`  
		Last Modified: Sat, 13 Nov 2021 06:20:36 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefa7778ca9c4c1248a35f60f616d57440c6dda91f0b4afcbf7b464258fa72cf`  
		Last Modified: Sat, 13 Nov 2021 06:20:36 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.10.3`

```console
$ docker pull consul@sha256:9806c8b77144ec19d594bf6d8a6e04634ebe63a2d734539c484bbe0d10b8e6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10.3` - linux; amd64

```console
$ docker pull consul@sha256:4fc771d6614f6d7af92653e006157b9c98a05098e43dc485d29d9c846abcc33d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43242800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9814b25e52bae10d44d9953bad57d86e8577283652bc9443be9738031389c48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:58:14 GMT
ARG CONSUL_VERSION=1.10.3
# Fri, 12 Nov 2021 21:58:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 12 Nov 2021 21:58:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 12 Nov 2021 21:58:17 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 12 Nov 2021 21:58:30 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 12 Nov 2021 21:58:32 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 12 Nov 2021 21:58:35 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:58:35 GMT
VOLUME [/consul/data]
# Fri, 12 Nov 2021 21:58:36 GMT
EXPOSE 8300
# Fri, 12 Nov 2021 21:58:36 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 12 Nov 2021 21:58:36 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 12 Nov 2021 21:58:37 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 21:58:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 21:58:38 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79efaa79e0b89d613b7eeb02676f2c706bf77bac920e8657f0f9badfb6205340`  
		Last Modified: Fri, 12 Nov 2021 22:00:01 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b6fccdd38073e2a0303fb7450154fb88dd5211f8abbd8ab1b55e2514a24cb1`  
		Last Modified: Fri, 12 Nov 2021 22:00:07 GMT  
		Size: 40.4 MB (40417007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a1a23e6dad553737585a3b60948d19896dd3c8aeb3ec7e62e0bf03560f416e`  
		Last Modified: Fri, 12 Nov 2021 22:00:01 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae16349669345cc0fb16abc18cd48c1dbf94910caaee5431326c3cf34882559`  
		Last Modified: Fri, 12 Nov 2021 22:00:01 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96fa79365c2a7793d97996a84e1a8e28dec95f530224a746f6d4cdca6dfe5f73`  
		Last Modified: Fri, 12 Nov 2021 22:00:01 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.3` - linux; arm variant v6

```console
$ docker pull consul@sha256:89cd92136a7b8ebd035cb1a0e39b8e96abc49edf60c9200a27f117054b53932c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39269139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4b0d9415b5a09650d466ee78ea76f2f5f821de5e796590f9339aa0c50e30b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:03:14 GMT
ARG CONSUL_VERSION=1.10.3
# Sat, 13 Nov 2021 06:03:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 13 Nov 2021 06:03:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 13 Nov 2021 06:03:17 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 13 Nov 2021 06:03:29 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 13 Nov 2021 06:03:31 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 13 Nov 2021 06:03:33 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 06:03:34 GMT
VOLUME [/consul/data]
# Sat, 13 Nov 2021 06:03:34 GMT
EXPOSE 8300
# Sat, 13 Nov 2021 06:03:35 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 13 Nov 2021 06:03:35 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 13 Nov 2021 06:03:36 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Nov 2021 06:03:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 06:03:37 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95e092b4de70f76b87ef5e2952153af28de56b56c428d170b0f028fb6afbf1d`  
		Last Modified: Sat, 13 Nov 2021 06:06:08 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598923641df439f939be74ba7dc244ef98d48641e316ff947702b24a279c956d`  
		Last Modified: Sat, 13 Nov 2021 06:06:27 GMT  
		Size: 36.6 MB (36632428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b856a08c888ad010360a1dd58e1196cab9d0a174889c005fd0dd1c23a5225c4`  
		Last Modified: Sat, 13 Nov 2021 06:06:08 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4ced118232a40da2c756413e2ca1148a45efc645d9f750f232a1dcd7f945f`  
		Last Modified: Sat, 13 Nov 2021 06:06:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e826ae63c559c7b16801bd6e94f70546fbf8739bbb8a33eae3edd323fd2797b7`  
		Last Modified: Sat, 13 Nov 2021 06:06:08 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.3` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:34988991d554ab9d710529135c77747ba808b12654d1062c5811cb3465078221
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39190366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d494725d24cc77ece20111697554c7e44d02326ac63bac482f6c5c7c520a427c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Tue, 02 Nov 2021 19:39:58 GMT
ARG CONSUL_VERSION=1.10.3
# Tue, 02 Nov 2021 19:39:59 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 02 Nov 2021 19:40:00 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 02 Nov 2021 19:40:01 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 02 Nov 2021 19:40:14 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 02 Nov 2021 19:40:15 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 02 Nov 2021 19:40:16 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 02 Nov 2021 19:40:17 GMT
VOLUME [/consul/data]
# Tue, 02 Nov 2021 19:40:18 GMT
EXPOSE 8300
# Tue, 02 Nov 2021 19:40:19 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 02 Nov 2021 19:40:20 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 02 Nov 2021 19:40:22 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 02 Nov 2021 19:40:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Nov 2021 19:40:23 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37670a2a9dc09fe75ad47ca2b119cfaed5f2978da6f457430dee234dada7ea43`  
		Last Modified: Tue, 02 Nov 2021 19:42:09 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919087a5490ea994435e800db080ee62a36ba94db46d8b2279447371e06648ad`  
		Last Modified: Tue, 02 Nov 2021 19:42:14 GMT  
		Size: 36.5 MB (36474046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b44e0042b56affa731efc3552e6d27a1c1a27c113ef7c2303abe8fb4a8c6c2`  
		Last Modified: Tue, 02 Nov 2021 19:42:09 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b020cd44b1a8b856d502623a20f69a02ed6f581b1955a5951159a088820f6052`  
		Last Modified: Tue, 02 Nov 2021 19:42:09 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43e375f5a466436cb3909f15c21a61e93bf531c521f1ba1b6bb737296f910fa`  
		Last Modified: Tue, 02 Nov 2021 19:42:09 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.3` - linux; 386

```console
$ docker pull consul@sha256:f6d4990606abae58cfa07041438a83774585b1976889aa17ecfb69c10582149d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42624588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0266e05a345c091de13c2cf497e8d5c997539a31384988e30a540f6338d8e095`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:18:54 GMT
ARG CONSUL_VERSION=1.10.3
# Sat, 13 Nov 2021 06:18:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 13 Nov 2021 06:18:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 13 Nov 2021 06:18:56 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 13 Nov 2021 06:19:06 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 13 Nov 2021 06:19:07 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 13 Nov 2021 06:19:08 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 06:19:08 GMT
VOLUME [/consul/data]
# Sat, 13 Nov 2021 06:19:08 GMT
EXPOSE 8300
# Sat, 13 Nov 2021 06:19:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 13 Nov 2021 06:19:09 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 13 Nov 2021 06:19:09 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Nov 2021 06:19:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 06:19:10 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ad71c51a3aaa36ca93ff2d29be265437f8d6a6a3265229463a32d757ab063c`  
		Last Modified: Sat, 13 Nov 2021 06:20:36 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264e1a84ec19e245b5b17560ae89a7a20d673c5065b8e31ad33e1dec79c3a5fc`  
		Last Modified: Sat, 13 Nov 2021 06:20:42 GMT  
		Size: 39.8 MB (39792406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52249b1ddd029a0a2974e3e28a7d4ba4eb74ba1428eba364aab8c0634680193`  
		Last Modified: Sat, 13 Nov 2021 06:20:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1e3c995ef13035d9e1361df724e4dbb2f695c7fdf5a1a5dac866ececfd2f54`  
		Last Modified: Sat, 13 Nov 2021 06:20:36 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefa7778ca9c4c1248a35f60f616d57440c6dda91f0b4afcbf7b464258fa72cf`  
		Last Modified: Sat, 13 Nov 2021 06:20:36 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.11.0-beta`

```console
$ docker pull consul@sha256:fd8d9fe41bfcd4dcff5f5391d027e8cc46380fb031c1298105c225c6b9cb9cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.11.0-beta` - linux; amd64

```console
$ docker pull consul@sha256:e57b5bd1735f5669571dd93cb358dafcc1274e123f85ec9878f40ba0b506bf22
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43713511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a1fbcf9760adfc346281ab93087515248a09acd754cfa38ad65dd048a23e67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:57:45 GMT
ARG CONSUL_VERSION=1.11.0-beta2
# Fri, 12 Nov 2021 21:57:45 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0-beta2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 12 Nov 2021 21:57:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 12 Nov 2021 21:57:46 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 12 Nov 2021 21:58:02 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 12 Nov 2021 21:58:05 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 12 Nov 2021 21:58:07 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:58:07 GMT
VOLUME [/consul/data]
# Fri, 12 Nov 2021 21:58:08 GMT
EXPOSE 8300
# Fri, 12 Nov 2021 21:58:08 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 12 Nov 2021 21:58:09 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 12 Nov 2021 21:58:09 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 21:58:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 21:58:10 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9dd9907ca9dba4bf6d73592e3433bb41bfd6758f9fda5deee3ba72629b90c0`  
		Last Modified: Fri, 12 Nov 2021 21:59:45 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ce0fdfb8f1545e60331c6ceb496bd4ff2cedab6c4e0533ab3d9c5132308624`  
		Last Modified: Fri, 12 Nov 2021 21:59:51 GMT  
		Size: 40.9 MB (40887721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c10085b0fae3b6f6041a1de3e35988aa036d8fd1e5a6f67aaff584f889545d`  
		Last Modified: Fri, 12 Nov 2021 21:59:45 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99692da936ecbe3f732798a699a03861ea39fc25a2664db7e8fd96fa3a05b24c`  
		Last Modified: Fri, 12 Nov 2021 21:59:46 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518e52fae0f8177dd8b49904fe878aaeabaa0eb44d2e78187ff1357a4e88eba7`  
		Last Modified: Fri, 12 Nov 2021 21:59:45 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.0-beta` - linux; arm variant v6

```console
$ docker pull consul@sha256:409f4b4355391f1bcc0b8bd49175b308adcc70ddca9bd5dc2dcb3977c5eb23aa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39508868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2fcd863378dba6a3d8e0d211cb0030306cf1eeda473f430c45b66185d9f40dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:02:39 GMT
ARG CONSUL_VERSION=1.11.0-beta2
# Sat, 13 Nov 2021 06:02:40 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0-beta2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 13 Nov 2021 06:02:40 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 13 Nov 2021 06:02:42 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 13 Nov 2021 06:02:55 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 13 Nov 2021 06:02:57 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 13 Nov 2021 06:02:59 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 06:02:59 GMT
VOLUME [/consul/data]
# Sat, 13 Nov 2021 06:03:00 GMT
EXPOSE 8300
# Sat, 13 Nov 2021 06:03:00 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 13 Nov 2021 06:03:01 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 13 Nov 2021 06:03:01 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Nov 2021 06:03:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 06:03:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2d7260b8a655c8d28c28f40ef7d386ecdf21ec4e683fca1ada03fb077990b1`  
		Last Modified: Sat, 13 Nov 2021 06:05:43 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d05d8b05f792a5f378b768ab68755d34efcd88553097ba4c11fe6fd0a4fe9b7`  
		Last Modified: Sat, 13 Nov 2021 06:05:56 GMT  
		Size: 36.9 MB (36872153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4c08e221c3a9944278928e0d5a5349f02e20378f200537c7bc0abc72fc4c5b`  
		Last Modified: Sat, 13 Nov 2021 06:05:43 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc684001062a2334874602425ae1f7f3321952ce632b97090c30715e183b3b6e`  
		Last Modified: Sat, 13 Nov 2021 06:05:43 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5703c46ca3d761e767f57a57cc7a942a7fd182112bbb0067a92544c78775fec6`  
		Last Modified: Sat, 13 Nov 2021 06:05:43 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.0-beta` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:a8d66ee95c5aa8743a06c6f90fa3177d5fc275535e275a0a539143385bddd5f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39280619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f18f696646a7240afa3aa9aebf958fc571a80f8698151bae40f54cd4f06e90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Tue, 02 Nov 2021 19:39:27 GMT
ARG CONSUL_VERSION=1.11.0-beta2
# Tue, 02 Nov 2021 19:39:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0-beta2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 02 Nov 2021 19:39:29 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 02 Nov 2021 19:39:30 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 02 Nov 2021 19:39:42 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 02 Nov 2021 19:39:43 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 02 Nov 2021 19:39:44 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 02 Nov 2021 19:39:45 GMT
VOLUME [/consul/data]
# Tue, 02 Nov 2021 19:39:46 GMT
EXPOSE 8300
# Tue, 02 Nov 2021 19:39:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 02 Nov 2021 19:39:48 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 02 Nov 2021 19:39:50 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 02 Nov 2021 19:39:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Nov 2021 19:39:51 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38e03b4a2d20bbf14f632859993ac46d9a456f4e63ee8250d97ab3b17ae775c`  
		Last Modified: Tue, 02 Nov 2021 19:41:52 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2339f7564b2332ee170cf608cfa8334783908fabb5a55fa374212ae9a1986c4`  
		Last Modified: Tue, 02 Nov 2021 19:41:58 GMT  
		Size: 36.6 MB (36564296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ee872d3decdee5f90f67f9ea5ae7cf3358ca5818b22b94b8678e38da47ec6d`  
		Last Modified: Tue, 02 Nov 2021 19:41:53 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2075ce661067f7b710232633aa4535449a02f57bcacba7ab5182abb02325665`  
		Last Modified: Tue, 02 Nov 2021 19:41:53 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91c407512d7c7aad5bb7a7c9fdb1ffcce547c49c86d90f6c3531e2cff2f289e`  
		Last Modified: Tue, 02 Nov 2021 19:41:52 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.0-beta` - linux; 386

```console
$ docker pull consul@sha256:c329aff5d47eba46e1f6992fbe91dcf9010d6f80005286be9155f965921e7975
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42543628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb87f43018f823068831b78d7e4d452fe84225256e1edaf0aa81e8387567bbc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:18:29 GMT
ARG CONSUL_VERSION=1.11.0-beta2
# Sat, 13 Nov 2021 06:18:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0-beta2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 13 Nov 2021 06:18:30 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 13 Nov 2021 06:18:31 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 13 Nov 2021 06:18:45 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 13 Nov 2021 06:18:46 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 13 Nov 2021 06:18:47 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 06:18:47 GMT
VOLUME [/consul/data]
# Sat, 13 Nov 2021 06:18:47 GMT
EXPOSE 8300
# Sat, 13 Nov 2021 06:18:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 13 Nov 2021 06:18:48 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 13 Nov 2021 06:18:48 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Nov 2021 06:18:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 06:18:48 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177c847a2ae3f27130e208c92ba400b0bc215dfbd6e6dc859cd2e39ad3aa520a`  
		Last Modified: Sat, 13 Nov 2021 06:20:17 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746a3c64b15b1543034c6e04bb4f1ffb5db0907892bf0e51163848219a87482d`  
		Last Modified: Sat, 13 Nov 2021 06:20:24 GMT  
		Size: 39.7 MB (39711445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bfeef4b841e5af9bbff9cb8f23fcee225725b3fede95993108c92b9061c9e9`  
		Last Modified: Sat, 13 Nov 2021 06:20:17 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472433ffd68a273b7d32b1483f7cd063212e7d8dab63fec46149bda5b1bd7012`  
		Last Modified: Sat, 13 Nov 2021 06:20:17 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6aec6a6bafe0942f394cf46f8857811ba95bf92af292b58b37ef99635d59af`  
		Last Modified: Sat, 13 Nov 2021 06:20:17 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.11.0-beta2`

```console
$ docker pull consul@sha256:fd8d9fe41bfcd4dcff5f5391d027e8cc46380fb031c1298105c225c6b9cb9cd7
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.11.0-beta2` - linux; amd64

```console
$ docker pull consul@sha256:e57b5bd1735f5669571dd93cb358dafcc1274e123f85ec9878f40ba0b506bf22
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43713511 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:33a1fbcf9760adfc346281ab93087515248a09acd754cfa38ad65dd048a23e67`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:57:45 GMT
ARG CONSUL_VERSION=1.11.0-beta2
# Fri, 12 Nov 2021 21:57:45 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0-beta2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 12 Nov 2021 21:57:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 12 Nov 2021 21:57:46 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 12 Nov 2021 21:58:02 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 12 Nov 2021 21:58:05 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 12 Nov 2021 21:58:07 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:58:07 GMT
VOLUME [/consul/data]
# Fri, 12 Nov 2021 21:58:08 GMT
EXPOSE 8300
# Fri, 12 Nov 2021 21:58:08 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 12 Nov 2021 21:58:09 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 12 Nov 2021 21:58:09 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 21:58:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 21:58:10 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0a9dd9907ca9dba4bf6d73592e3433bb41bfd6758f9fda5deee3ba72629b90c0`  
		Last Modified: Fri, 12 Nov 2021 21:59:45 GMT  
		Size: 1.3 KB (1255 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2ce0fdfb8f1545e60331c6ceb496bd4ff2cedab6c4e0533ab3d9c5132308624`  
		Last Modified: Fri, 12 Nov 2021 21:59:51 GMT  
		Size: 40.9 MB (40887721 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6c10085b0fae3b6f6041a1de3e35988aa036d8fd1e5a6f67aaff584f889545d`  
		Last Modified: Fri, 12 Nov 2021 21:59:45 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:99692da936ecbe3f732798a699a03861ea39fc25a2664db7e8fd96fa3a05b24c`  
		Last Modified: Fri, 12 Nov 2021 21:59:46 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:518e52fae0f8177dd8b49904fe878aaeabaa0eb44d2e78187ff1357a4e88eba7`  
		Last Modified: Fri, 12 Nov 2021 21:59:45 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.0-beta2` - linux; arm variant v6

```console
$ docker pull consul@sha256:409f4b4355391f1bcc0b8bd49175b308adcc70ddca9bd5dc2dcb3977c5eb23aa
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39508868 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e2fcd863378dba6a3d8e0d211cb0030306cf1eeda473f430c45b66185d9f40dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:02:39 GMT
ARG CONSUL_VERSION=1.11.0-beta2
# Sat, 13 Nov 2021 06:02:40 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0-beta2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 13 Nov 2021 06:02:40 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 13 Nov 2021 06:02:42 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 13 Nov 2021 06:02:55 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 13 Nov 2021 06:02:57 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 13 Nov 2021 06:02:59 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 06:02:59 GMT
VOLUME [/consul/data]
# Sat, 13 Nov 2021 06:03:00 GMT
EXPOSE 8300
# Sat, 13 Nov 2021 06:03:00 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 13 Nov 2021 06:03:01 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 13 Nov 2021 06:03:01 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Nov 2021 06:03:01 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 06:03:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5b2d7260b8a655c8d28c28f40ef7d386ecdf21ec4e683fca1ada03fb077990b1`  
		Last Modified: Sat, 13 Nov 2021 06:05:43 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6d05d8b05f792a5f378b768ab68755d34efcd88553097ba4c11fe6fd0a4fe9b7`  
		Last Modified: Sat, 13 Nov 2021 06:05:56 GMT  
		Size: 36.9 MB (36872153 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f4c08e221c3a9944278928e0d5a5349f02e20378f200537c7bc0abc72fc4c5b`  
		Last Modified: Sat, 13 Nov 2021 06:05:43 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc684001062a2334874602425ae1f7f3321952ce632b97090c30715e183b3b6e`  
		Last Modified: Sat, 13 Nov 2021 06:05:43 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5703c46ca3d761e767f57a57cc7a942a7fd182112bbb0067a92544c78775fec6`  
		Last Modified: Sat, 13 Nov 2021 06:05:43 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.0-beta2` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:a8d66ee95c5aa8743a06c6f90fa3177d5fc275535e275a0a539143385bddd5f3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39280619 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:74f18f696646a7240afa3aa9aebf958fc571a80f8698151bae40f54cd4f06e90`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Tue, 02 Nov 2021 19:39:27 GMT
ARG CONSUL_VERSION=1.11.0-beta2
# Tue, 02 Nov 2021 19:39:28 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0-beta2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 02 Nov 2021 19:39:29 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 02 Nov 2021 19:39:30 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 02 Nov 2021 19:39:42 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 02 Nov 2021 19:39:43 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 02 Nov 2021 19:39:44 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 02 Nov 2021 19:39:45 GMT
VOLUME [/consul/data]
# Tue, 02 Nov 2021 19:39:46 GMT
EXPOSE 8300
# Tue, 02 Nov 2021 19:39:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 02 Nov 2021 19:39:48 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 02 Nov 2021 19:39:50 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 02 Nov 2021 19:39:50 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Nov 2021 19:39:51 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c38e03b4a2d20bbf14f632859993ac46d9a456f4e63ee8250d97ab3b17ae775c`  
		Last Modified: Tue, 02 Nov 2021 19:41:52 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2339f7564b2332ee170cf608cfa8334783908fabb5a55fa374212ae9a1986c4`  
		Last Modified: Tue, 02 Nov 2021 19:41:58 GMT  
		Size: 36.6 MB (36564296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19ee872d3decdee5f90f67f9ea5ae7cf3358ca5818b22b94b8678e38da47ec6d`  
		Last Modified: Tue, 02 Nov 2021 19:41:53 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a2075ce661067f7b710232633aa4535449a02f57bcacba7ab5182abb02325665`  
		Last Modified: Tue, 02 Nov 2021 19:41:53 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f91c407512d7c7aad5bb7a7c9fdb1ffcce547c49c86d90f6c3531e2cff2f289e`  
		Last Modified: Tue, 02 Nov 2021 19:41:52 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.11.0-beta2` - linux; 386

```console
$ docker pull consul@sha256:c329aff5d47eba46e1f6992fbe91dcf9010d6f80005286be9155f965921e7975
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.5 MB (42543628 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bdb87f43018f823068831b78d7e4d452fe84225256e1edaf0aa81e8387567bbc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:18:29 GMT
ARG CONSUL_VERSION=1.11.0-beta2
# Sat, 13 Nov 2021 06:18:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.11.0-beta2 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 13 Nov 2021 06:18:30 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 13 Nov 2021 06:18:31 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 13 Nov 2021 06:18:45 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 13 Nov 2021 06:18:46 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 13 Nov 2021 06:18:47 GMT
# ARGS: CONSUL_VERSION=1.11.0-beta2
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 06:18:47 GMT
VOLUME [/consul/data]
# Sat, 13 Nov 2021 06:18:47 GMT
EXPOSE 8300
# Sat, 13 Nov 2021 06:18:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 13 Nov 2021 06:18:48 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 13 Nov 2021 06:18:48 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Nov 2021 06:18:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 06:18:48 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:177c847a2ae3f27130e208c92ba400b0bc215dfbd6e6dc859cd2e39ad3aa520a`  
		Last Modified: Sat, 13 Nov 2021 06:20:17 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:746a3c64b15b1543034c6e04bb4f1ffb5db0907892bf0e51163848219a87482d`  
		Last Modified: Sat, 13 Nov 2021 06:20:24 GMT  
		Size: 39.7 MB (39711445 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9bfeef4b841e5af9bbff9cb8f23fcee225725b3fede95993108c92b9061c9e9`  
		Last Modified: Sat, 13 Nov 2021 06:20:17 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:472433ffd68a273b7d32b1483f7cd063212e7d8dab63fec46149bda5b1bd7012`  
		Last Modified: Sat, 13 Nov 2021 06:20:17 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb6aec6a6bafe0942f394cf46f8857811ba95bf92af292b58b37ef99635d59af`  
		Last Modified: Sat, 13 Nov 2021 06:20:17 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8`

```console
$ docker pull consul@sha256:2d6489b3c2c01bf75eb4aa93cf43a5275110aeb26d48fabf7dbb106340247673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8` - linux; amd64

```console
$ docker pull consul@sha256:546d194b2fa656448e8b8dc8c82e14aa74df609b01cc1a7512a548d68c3a59a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47442415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594e22f602fd253a4ccf65411b17591b42f00b3c73337ac7b600dc437ec0e1e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:59:08 GMT
ARG CONSUL_VERSION=1.8.16
# Fri, 12 Nov 2021 21:59:08 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 12 Nov 2021 21:59:08 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 12 Nov 2021 21:59:09 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 12 Nov 2021 21:59:22 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 12 Nov 2021 21:59:23 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 12 Nov 2021 21:59:24 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:59:24 GMT
VOLUME [/consul/data]
# Fri, 12 Nov 2021 21:59:25 GMT
EXPOSE 8300
# Fri, 12 Nov 2021 21:59:25 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 12 Nov 2021 21:59:25 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 12 Nov 2021 21:59:25 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 21:59:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 21:59:26 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf254dbeaa3fef95c5677f071ae3d345825fa845e6f4b5ed890c45f76871dfd`  
		Last Modified: Fri, 12 Nov 2021 22:00:37 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c95ea807a3d5777523ccb77a9277ec7e2aa1ab3739ff5cadde9a79db9a5179`  
		Last Modified: Fri, 12 Nov 2021 22:00:43 GMT  
		Size: 44.6 MB (44616621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b1a4a14828149fa5edc5044f90b651985c756dd381e637361fe837e055e236`  
		Last Modified: Fri, 12 Nov 2021 22:00:37 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651f3beee8b2a2a0a5fbef50eacae52d3d8b8e5f323a5ac23face007bfb8dba7`  
		Last Modified: Fri, 12 Nov 2021 22:00:37 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053af3dfc6f8374f6aec29ada8e523e370405df63219e60f9b6625f86a38e9e2`  
		Last Modified: Fri, 12 Nov 2021 22:00:37 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm variant v6

```console
$ docker pull consul@sha256:4edfc14afdc0f37429cebb0dbe241231461df005386af7bd9c753623f98d5df2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42647095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d314364247bfbb6794e1fcebbf3f5d52a52a695123bc7872399cd62a0e48edf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:04:25 GMT
ARG CONSUL_VERSION=1.8.16
# Sat, 13 Nov 2021 06:04:26 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 13 Nov 2021 06:04:26 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 13 Nov 2021 06:04:29 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 13 Nov 2021 06:04:40 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 13 Nov 2021 06:04:43 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 13 Nov 2021 06:04:45 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 06:04:46 GMT
VOLUME [/consul/data]
# Sat, 13 Nov 2021 06:04:46 GMT
EXPOSE 8300
# Sat, 13 Nov 2021 06:04:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 13 Nov 2021 06:04:47 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 13 Nov 2021 06:04:48 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Nov 2021 06:04:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 06:04:49 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf4ef515c98c7a84eb35f5f5720cd2828c46fa3cc928aaaa143ae8cf1e2f3b0`  
		Last Modified: Sat, 13 Nov 2021 06:07:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf2a49b395d46e338b5f9aa342bf8c5fed30384e74a4938eb77b32e43dd8658`  
		Last Modified: Sat, 13 Nov 2021 06:07:22 GMT  
		Size: 40.0 MB (40010378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd78246daf38720d3035adde8b92496db5795856ae20c1a2806df6ca2b557ad8`  
		Last Modified: Sat, 13 Nov 2021 06:07:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88374c41dbe010b7a63d28ae07dc13e2a768612e3c5beed3ef1ac6988bc1dd2`  
		Last Modified: Sat, 13 Nov 2021 06:07:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fa636a5abd48d6a8dd0cec8c360d3c933de0b2416a11a621b79f7dd0360b74`  
		Last Modified: Sat, 13 Nov 2021 06:07:10 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:63ebdf3cdec6f9de9f5e81a0b9725652cc8f5f661bf19448b5cbf2bb0e606abe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42833149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ed7ea3306cdadf65bb608d7b7d63559603c0502e530ac190a4fc9f0c2e7720`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Tue, 02 Nov 2021 19:41:01 GMT
ARG CONSUL_VERSION=1.8.16
# Tue, 02 Nov 2021 19:41:02 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 02 Nov 2021 19:41:03 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 02 Nov 2021 19:41:04 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 02 Nov 2021 19:41:14 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 02 Nov 2021 19:41:15 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 02 Nov 2021 19:41:16 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 02 Nov 2021 19:41:17 GMT
VOLUME [/consul/data]
# Tue, 02 Nov 2021 19:41:18 GMT
EXPOSE 8300
# Tue, 02 Nov 2021 19:41:19 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 02 Nov 2021 19:41:20 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 02 Nov 2021 19:41:22 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 02 Nov 2021 19:41:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Nov 2021 19:41:23 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5e08520c6a6c13998ee67f4723d0936c944a1303ee767ece56747215c240d2`  
		Last Modified: Tue, 02 Nov 2021 19:42:44 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9ee0b3b0323a479b69a6ba5a64ae9c661df2b7bb25947dae3a0bbaf5abbc37`  
		Last Modified: Tue, 02 Nov 2021 19:42:49 GMT  
		Size: 40.1 MB (40116831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c170f4adc01a379af6cbb87e2460d6525439feffef4af1d60679cdb45430565`  
		Last Modified: Tue, 02 Nov 2021 19:42:44 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483f0f6ff67c8f024e472fcd99832c1e485a4b7bed52923d15aabe146a1c4268`  
		Last Modified: Tue, 02 Nov 2021 19:42:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb796399f053961433f610fda51636a8d2e604dcf33fcdd7d669b6a9c025e06f`  
		Last Modified: Tue, 02 Nov 2021 19:42:44 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; 386

```console
$ docker pull consul@sha256:b5417e0c8383a779c8a901b4c03301e2419ebacd39241574bb000ec17f355cf8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46997597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3801dceae3828af9b3aceb1ce1074f927daf33acd795456a4589098baf43324f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:19:35 GMT
ARG CONSUL_VERSION=1.8.16
# Sat, 13 Nov 2021 06:19:35 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 13 Nov 2021 06:19:35 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 13 Nov 2021 06:19:36 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 13 Nov 2021 06:19:44 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 13 Nov 2021 06:19:45 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 13 Nov 2021 06:19:46 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 06:19:46 GMT
VOLUME [/consul/data]
# Sat, 13 Nov 2021 06:19:47 GMT
EXPOSE 8300
# Sat, 13 Nov 2021 06:19:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 13 Nov 2021 06:19:47 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 13 Nov 2021 06:19:47 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Nov 2021 06:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 06:19:48 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd997c8b6363c68575b61009e8ca5d1384341243dd890de5eeda3eb497f77bb`  
		Last Modified: Sat, 13 Nov 2021 06:21:17 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f76a08b1620e00334bdb461749243b6a43e767557e948b776d4672a08a4f137`  
		Last Modified: Sat, 13 Nov 2021 06:21:23 GMT  
		Size: 44.2 MB (44165418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f744f10f839222456505d1523f900e18b943259c3096857a2592395f77b084`  
		Last Modified: Sat, 13 Nov 2021 06:21:17 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e80487615705b444e547ffcd0bb3ea8aceca2dd68b6ceef1c3ab95347f16452`  
		Last Modified: Sat, 13 Nov 2021 06:21:17 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c137926072307d795ed8d9de2f02e6a20c9788cf901d3bb619ec49f20292439e`  
		Last Modified: Sat, 13 Nov 2021 06:21:17 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8.16`

```console
$ docker pull consul@sha256:2d6489b3c2c01bf75eb4aa93cf43a5275110aeb26d48fabf7dbb106340247673
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8.16` - linux; amd64

```console
$ docker pull consul@sha256:546d194b2fa656448e8b8dc8c82e14aa74df609b01cc1a7512a548d68c3a59a4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47442415 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:594e22f602fd253a4ccf65411b17591b42f00b3c73337ac7b600dc437ec0e1e1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:59:08 GMT
ARG CONSUL_VERSION=1.8.16
# Fri, 12 Nov 2021 21:59:08 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 12 Nov 2021 21:59:08 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 12 Nov 2021 21:59:09 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 12 Nov 2021 21:59:22 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 12 Nov 2021 21:59:23 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 12 Nov 2021 21:59:24 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:59:24 GMT
VOLUME [/consul/data]
# Fri, 12 Nov 2021 21:59:25 GMT
EXPOSE 8300
# Fri, 12 Nov 2021 21:59:25 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 12 Nov 2021 21:59:25 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 12 Nov 2021 21:59:25 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 21:59:25 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 21:59:26 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ebf254dbeaa3fef95c5677f071ae3d345825fa845e6f4b5ed890c45f76871dfd`  
		Last Modified: Fri, 12 Nov 2021 22:00:37 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c95ea807a3d5777523ccb77a9277ec7e2aa1ab3739ff5cadde9a79db9a5179`  
		Last Modified: Fri, 12 Nov 2021 22:00:43 GMT  
		Size: 44.6 MB (44616621 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:13b1a4a14828149fa5edc5044f90b651985c756dd381e637361fe837e055e236`  
		Last Modified: Fri, 12 Nov 2021 22:00:37 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651f3beee8b2a2a0a5fbef50eacae52d3d8b8e5f323a5ac23face007bfb8dba7`  
		Last Modified: Fri, 12 Nov 2021 22:00:37 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:053af3dfc6f8374f6aec29ada8e523e370405df63219e60f9b6625f86a38e9e2`  
		Last Modified: Fri, 12 Nov 2021 22:00:37 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.16` - linux; arm variant v6

```console
$ docker pull consul@sha256:4edfc14afdc0f37429cebb0dbe241231461df005386af7bd9c753623f98d5df2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42647095 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d314364247bfbb6794e1fcebbf3f5d52a52a695123bc7872399cd62a0e48edf1`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:04:25 GMT
ARG CONSUL_VERSION=1.8.16
# Sat, 13 Nov 2021 06:04:26 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 13 Nov 2021 06:04:26 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 13 Nov 2021 06:04:29 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 13 Nov 2021 06:04:40 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 13 Nov 2021 06:04:43 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 13 Nov 2021 06:04:45 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 06:04:46 GMT
VOLUME [/consul/data]
# Sat, 13 Nov 2021 06:04:46 GMT
EXPOSE 8300
# Sat, 13 Nov 2021 06:04:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 13 Nov 2021 06:04:47 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 13 Nov 2021 06:04:48 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Nov 2021 06:04:49 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 06:04:49 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcf4ef515c98c7a84eb35f5f5720cd2828c46fa3cc928aaaa143ae8cf1e2f3b0`  
		Last Modified: Sat, 13 Nov 2021 06:07:09 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cf2a49b395d46e338b5f9aa342bf8c5fed30384e74a4938eb77b32e43dd8658`  
		Last Modified: Sat, 13 Nov 2021 06:07:22 GMT  
		Size: 40.0 MB (40010378 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd78246daf38720d3035adde8b92496db5795856ae20c1a2806df6ca2b557ad8`  
		Last Modified: Sat, 13 Nov 2021 06:07:09 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a88374c41dbe010b7a63d28ae07dc13e2a768612e3c5beed3ef1ac6988bc1dd2`  
		Last Modified: Sat, 13 Nov 2021 06:07:09 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12fa636a5abd48d6a8dd0cec8c360d3c933de0b2416a11a621b79f7dd0360b74`  
		Last Modified: Sat, 13 Nov 2021 06:07:10 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.16` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:63ebdf3cdec6f9de9f5e81a0b9725652cc8f5f661bf19448b5cbf2bb0e606abe
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.8 MB (42833149 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5ed7ea3306cdadf65bb608d7b7d63559603c0502e530ac190a4fc9f0c2e7720`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Tue, 02 Nov 2021 19:41:01 GMT
ARG CONSUL_VERSION=1.8.16
# Tue, 02 Nov 2021 19:41:02 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 02 Nov 2021 19:41:03 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 02 Nov 2021 19:41:04 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 02 Nov 2021 19:41:14 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 02 Nov 2021 19:41:15 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 02 Nov 2021 19:41:16 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 02 Nov 2021 19:41:17 GMT
VOLUME [/consul/data]
# Tue, 02 Nov 2021 19:41:18 GMT
EXPOSE 8300
# Tue, 02 Nov 2021 19:41:19 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 02 Nov 2021 19:41:20 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 02 Nov 2021 19:41:22 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 02 Nov 2021 19:41:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Nov 2021 19:41:23 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2e5e08520c6a6c13998ee67f4723d0936c944a1303ee767ece56747215c240d2`  
		Last Modified: Tue, 02 Nov 2021 19:42:44 GMT  
		Size: 1.2 KB (1229 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3a9ee0b3b0323a479b69a6ba5a64ae9c661df2b7bb25947dae3a0bbaf5abbc37`  
		Last Modified: Tue, 02 Nov 2021 19:42:49 GMT  
		Size: 40.1 MB (40116831 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c170f4adc01a379af6cbb87e2460d6525439feffef4af1d60679cdb45430565`  
		Last Modified: Tue, 02 Nov 2021 19:42:44 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:483f0f6ff67c8f024e472fcd99832c1e485a4b7bed52923d15aabe146a1c4268`  
		Last Modified: Tue, 02 Nov 2021 19:42:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fb796399f053961433f610fda51636a8d2e604dcf33fcdd7d669b6a9c025e06f`  
		Last Modified: Tue, 02 Nov 2021 19:42:44 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.16` - linux; 386

```console
$ docker pull consul@sha256:b5417e0c8383a779c8a901b4c03301e2419ebacd39241574bb000ec17f355cf8
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.0 MB (46997597 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3801dceae3828af9b3aceb1ce1074f927daf33acd795456a4589098baf43324f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:19:35 GMT
ARG CONSUL_VERSION=1.8.16
# Sat, 13 Nov 2021 06:19:35 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.8.16 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 13 Nov 2021 06:19:35 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 13 Nov 2021 06:19:36 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 13 Nov 2021 06:19:44 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 13 Nov 2021 06:19:45 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 13 Nov 2021 06:19:46 GMT
# ARGS: CONSUL_VERSION=1.8.16
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 06:19:46 GMT
VOLUME [/consul/data]
# Sat, 13 Nov 2021 06:19:47 GMT
EXPOSE 8300
# Sat, 13 Nov 2021 06:19:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 13 Nov 2021 06:19:47 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 13 Nov 2021 06:19:47 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Nov 2021 06:19:48 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 06:19:48 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cd997c8b6363c68575b61009e8ca5d1384341243dd890de5eeda3eb497f77bb`  
		Last Modified: Sat, 13 Nov 2021 06:21:17 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3f76a08b1620e00334bdb461749243b6a43e767557e948b776d4672a08a4f137`  
		Last Modified: Sat, 13 Nov 2021 06:21:23 GMT  
		Size: 44.2 MB (44165418 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d4f744f10f839222456505d1523f900e18b943259c3096857a2592395f77b084`  
		Last Modified: Sat, 13 Nov 2021 06:21:17 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e80487615705b444e547ffcd0bb3ea8aceca2dd68b6ceef1c3ab95347f16452`  
		Last Modified: Sat, 13 Nov 2021 06:21:17 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c137926072307d795ed8d9de2f02e6a20c9788cf901d3bb619ec49f20292439e`  
		Last Modified: Sat, 13 Nov 2021 06:21:17 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9`

```console
$ docker pull consul@sha256:58c1d631daffc64432f8eae1d6e14c84b7f034dbf9080aa9d9eae78c250a27ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9` - linux; amd64

```console
$ docker pull consul@sha256:d13741d433f3ee09978212eea3816f30d05bcee5eae19dbbec480770326c65df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45906650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8caacaa9c797a072acd2548987b06e63f13aeaf90d3e8b7745e6451f19d436c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:58:44 GMT
ARG CONSUL_VERSION=1.9.10
# Fri, 12 Nov 2021 21:58:44 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.10 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 12 Nov 2021 21:58:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 12 Nov 2021 21:58:46 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 12 Nov 2021 21:58:58 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 12 Nov 2021 21:58:59 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 12 Nov 2021 21:59:01 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:59:02 GMT
VOLUME [/consul/data]
# Fri, 12 Nov 2021 21:59:02 GMT
EXPOSE 8300
# Fri, 12 Nov 2021 21:59:03 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 12 Nov 2021 21:59:03 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 12 Nov 2021 21:59:04 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 21:59:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 21:59:04 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e2c1f7906065a4cd42e4d62b6b0bb1210343968bec2332b455f12275ad80c7`  
		Last Modified: Fri, 12 Nov 2021 22:00:20 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726648a6f1d4dfbdd112cdebd05f18100c5faa4393a314bd14be947e20de583f`  
		Last Modified: Fri, 12 Nov 2021 22:00:27 GMT  
		Size: 43.1 MB (43080860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb402eaf5bebb1aa06118318c62217955732df2610d038250b4320665cb28a60`  
		Last Modified: Fri, 12 Nov 2021 22:00:20 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a7593bd225039971e09dd20556347c1ef097f2d4ca4b61534b49dd04743715`  
		Last Modified: Fri, 12 Nov 2021 22:00:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe1eecc2c3ab6ff464433c7bcd422b6852761752b1569a34d24a7c35918b236`  
		Last Modified: Fri, 12 Nov 2021 22:00:20 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:68735b0af8ad58f5783892d9cd7a072367e3c5acc9841deff279771c6610ef52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41089948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510575fe5907c1ea33f4f5381765bfa9f9e7d35967335233de5050651722bd71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:03:50 GMT
ARG CONSUL_VERSION=1.9.10
# Sat, 13 Nov 2021 06:03:51 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.10 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 13 Nov 2021 06:03:51 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 13 Nov 2021 06:03:54 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 13 Nov 2021 06:04:05 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 13 Nov 2021 06:04:07 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 13 Nov 2021 06:04:10 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 06:04:10 GMT
VOLUME [/consul/data]
# Sat, 13 Nov 2021 06:04:11 GMT
EXPOSE 8300
# Sat, 13 Nov 2021 06:04:12 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 13 Nov 2021 06:04:12 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 13 Nov 2021 06:04:13 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Nov 2021 06:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 06:04:14 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f2254d0cdcef69ac73640a6cc81362f1ef51b50d379756688f4812fcd571af`  
		Last Modified: Sat, 13 Nov 2021 06:06:44 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b99f6f7345bc41a816ddc999ed6e1200cdc60082abe484180bd44f1dd471172`  
		Last Modified: Sat, 13 Nov 2021 06:06:57 GMT  
		Size: 38.5 MB (38453237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa73ecab166d1aa41bbb57b7f8cdad4e68e22ea5ca6e27eb9e844ca2cdcc6b9`  
		Last Modified: Sat, 13 Nov 2021 06:06:44 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d112ea0b69b8c2f4cbad40bb296032d9e14b28179c046e7185c621264fb4026`  
		Last Modified: Sat, 13 Nov 2021 06:06:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e29fe5d164369c89b9a2d187450583c34069ecdf4cce4892d8514aab525592a`  
		Last Modified: Sat, 13 Nov 2021 06:06:44 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:864847995ea6be6b70f59cdf7ac09a652343c54d3b8fa82a33e6ba71b10d27f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41339682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c78c38f9224fd6fe3efc7c5cb5cba24b156615776d4cc4d75540a22994bbd2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Tue, 02 Nov 2021 19:40:30 GMT
ARG CONSUL_VERSION=1.9.10
# Tue, 02 Nov 2021 19:40:30 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.10 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 02 Nov 2021 19:40:31 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 02 Nov 2021 19:40:32 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 02 Nov 2021 19:40:46 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 02 Nov 2021 19:40:46 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 02 Nov 2021 19:40:47 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 02 Nov 2021 19:40:48 GMT
VOLUME [/consul/data]
# Tue, 02 Nov 2021 19:40:49 GMT
EXPOSE 8300
# Tue, 02 Nov 2021 19:40:50 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 02 Nov 2021 19:40:51 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 02 Nov 2021 19:40:53 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 02 Nov 2021 19:40:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Nov 2021 19:40:54 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b436b54f47049e6069259d7fc8339393760698cc1b644764a7ba3d25b08133c3`  
		Last Modified: Tue, 02 Nov 2021 19:42:28 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b563fadf7d77e4fdcb2a5d95a7071a01cf9bde18eb503f089382d2a4336e415b`  
		Last Modified: Tue, 02 Nov 2021 19:42:33 GMT  
		Size: 38.6 MB (38623361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789f0f14457535ac15fe8eae7c0dd83c57b78fc71b27555e8a997190c33f1cc2`  
		Last Modified: Tue, 02 Nov 2021 19:42:28 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee0a2b3ba01475b1b01cca9cbaa1976af2ae0372971eb8787e0378ef013245b`  
		Last Modified: Tue, 02 Nov 2021 19:42:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d351a6b3f0c4ebbb0653488b417036bc49e2bb02a5ad5bceba0874235489e38b`  
		Last Modified: Tue, 02 Nov 2021 19:42:28 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; 386

```console
$ docker pull consul@sha256:55669dfe9f36283013fe5df4242a4018d0f867c48edbed31865846791264572b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45280360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67273333547d454a13e319b3d146cb12cfb8fe64a6744d026015afb23657d7f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:19:16 GMT
ARG CONSUL_VERSION=1.9.10
# Sat, 13 Nov 2021 06:19:16 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.10 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 13 Nov 2021 06:19:16 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 13 Nov 2021 06:19:17 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 13 Nov 2021 06:19:25 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 13 Nov 2021 06:19:26 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 13 Nov 2021 06:19:27 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 06:19:27 GMT
VOLUME [/consul/data]
# Sat, 13 Nov 2021 06:19:28 GMT
EXPOSE 8300
# Sat, 13 Nov 2021 06:19:28 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 13 Nov 2021 06:19:28 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 13 Nov 2021 06:19:28 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Nov 2021 06:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 06:19:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77ae2949f0c68422ea7eb3c79cdee4b8016a48f3c056625d981fda2126a4f92`  
		Last Modified: Sat, 13 Nov 2021 06:20:58 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333790003bf543bc1470abdabe948ff03bfc53fae887d0928559e96eaf0fac3f`  
		Last Modified: Sat, 13 Nov 2021 06:21:05 GMT  
		Size: 42.4 MB (42448180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c44e93225d9f849ee5d8490adcfd304fd24cc989d6637b07d32aa67c9d7a6d`  
		Last Modified: Sat, 13 Nov 2021 06:20:57 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a156e59d99bb9c6105ba227d4028a1add1fac8f08518475a70849a924c136a`  
		Last Modified: Sat, 13 Nov 2021 06:20:57 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59ca8eeaf0ca7d2fde65e0b7259bf8923ba973e6dfa858596c7ee50c019d736`  
		Last Modified: Sat, 13 Nov 2021 06:20:57 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9.10`

```console
$ docker pull consul@sha256:58c1d631daffc64432f8eae1d6e14c84b7f034dbf9080aa9d9eae78c250a27ad
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9.10` - linux; amd64

```console
$ docker pull consul@sha256:d13741d433f3ee09978212eea3816f30d05bcee5eae19dbbec480770326c65df
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.9 MB (45906650 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8caacaa9c797a072acd2548987b06e63f13aeaf90d3e8b7745e6451f19d436c6`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:58:44 GMT
ARG CONSUL_VERSION=1.9.10
# Fri, 12 Nov 2021 21:58:44 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.10 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 12 Nov 2021 21:58:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 12 Nov 2021 21:58:46 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 12 Nov 2021 21:58:58 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 12 Nov 2021 21:58:59 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 12 Nov 2021 21:59:01 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:59:02 GMT
VOLUME [/consul/data]
# Fri, 12 Nov 2021 21:59:02 GMT
EXPOSE 8300
# Fri, 12 Nov 2021 21:59:03 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 12 Nov 2021 21:59:03 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 12 Nov 2021 21:59:04 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 21:59:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 21:59:04 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:81e2c1f7906065a4cd42e4d62b6b0bb1210343968bec2332b455f12275ad80c7`  
		Last Modified: Fri, 12 Nov 2021 22:00:20 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:726648a6f1d4dfbdd112cdebd05f18100c5faa4393a314bd14be947e20de583f`  
		Last Modified: Fri, 12 Nov 2021 22:00:27 GMT  
		Size: 43.1 MB (43080860 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb402eaf5bebb1aa06118318c62217955732df2610d038250b4320665cb28a60`  
		Last Modified: Fri, 12 Nov 2021 22:00:20 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1a7593bd225039971e09dd20556347c1ef097f2d4ca4b61534b49dd04743715`  
		Last Modified: Fri, 12 Nov 2021 22:00:20 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfe1eecc2c3ab6ff464433c7bcd422b6852761752b1569a34d24a7c35918b236`  
		Last Modified: Fri, 12 Nov 2021 22:00:20 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.10` - linux; arm variant v6

```console
$ docker pull consul@sha256:68735b0af8ad58f5783892d9cd7a072367e3c5acc9841deff279771c6610ef52
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.1 MB (41089948 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:510575fe5907c1ea33f4f5381765bfa9f9e7d35967335233de5050651722bd71`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:03:50 GMT
ARG CONSUL_VERSION=1.9.10
# Sat, 13 Nov 2021 06:03:51 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.10 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 13 Nov 2021 06:03:51 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 13 Nov 2021 06:03:54 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 13 Nov 2021 06:04:05 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 13 Nov 2021 06:04:07 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 13 Nov 2021 06:04:10 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 06:04:10 GMT
VOLUME [/consul/data]
# Sat, 13 Nov 2021 06:04:11 GMT
EXPOSE 8300
# Sat, 13 Nov 2021 06:04:12 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 13 Nov 2021 06:04:12 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 13 Nov 2021 06:04:13 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Nov 2021 06:04:13 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 06:04:14 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:94f2254d0cdcef69ac73640a6cc81362f1ef51b50d379756688f4812fcd571af`  
		Last Modified: Sat, 13 Nov 2021 06:06:44 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b99f6f7345bc41a816ddc999ed6e1200cdc60082abe484180bd44f1dd471172`  
		Last Modified: Sat, 13 Nov 2021 06:06:57 GMT  
		Size: 38.5 MB (38453237 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6fa73ecab166d1aa41bbb57b7f8cdad4e68e22ea5ca6e27eb9e844ca2cdcc6b9`  
		Last Modified: Sat, 13 Nov 2021 06:06:44 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d112ea0b69b8c2f4cbad40bb296032d9e14b28179c046e7185c621264fb4026`  
		Last Modified: Sat, 13 Nov 2021 06:06:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5e29fe5d164369c89b9a2d187450583c34069ecdf4cce4892d8514aab525592a`  
		Last Modified: Sat, 13 Nov 2021 06:06:44 GMT  
		Size: 1.8 KB (1782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.10` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:864847995ea6be6b70f59cdf7ac09a652343c54d3b8fa82a33e6ba71b10d27f0
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.3 MB (41339682 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d5c78c38f9224fd6fe3efc7c5cb5cba24b156615776d4cc4d75540a22994bbd2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Tue, 02 Nov 2021 19:40:30 GMT
ARG CONSUL_VERSION=1.9.10
# Tue, 02 Nov 2021 19:40:30 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.10 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 02 Nov 2021 19:40:31 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 02 Nov 2021 19:40:32 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 02 Nov 2021 19:40:46 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 02 Nov 2021 19:40:46 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 02 Nov 2021 19:40:47 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 02 Nov 2021 19:40:48 GMT
VOLUME [/consul/data]
# Tue, 02 Nov 2021 19:40:49 GMT
EXPOSE 8300
# Tue, 02 Nov 2021 19:40:50 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 02 Nov 2021 19:40:51 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 02 Nov 2021 19:40:53 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 02 Nov 2021 19:40:53 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Nov 2021 19:40:54 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b436b54f47049e6069259d7fc8339393760698cc1b644764a7ba3d25b08133c3`  
		Last Modified: Tue, 02 Nov 2021 19:42:28 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b563fadf7d77e4fdcb2a5d95a7071a01cf9bde18eb503f089382d2a4336e415b`  
		Last Modified: Tue, 02 Nov 2021 19:42:33 GMT  
		Size: 38.6 MB (38623361 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:789f0f14457535ac15fe8eae7c0dd83c57b78fc71b27555e8a997190c33f1cc2`  
		Last Modified: Tue, 02 Nov 2021 19:42:28 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0ee0a2b3ba01475b1b01cca9cbaa1976af2ae0372971eb8787e0378ef013245b`  
		Last Modified: Tue, 02 Nov 2021 19:42:28 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d351a6b3f0c4ebbb0653488b417036bc49e2bb02a5ad5bceba0874235489e38b`  
		Last Modified: Tue, 02 Nov 2021 19:42:28 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.10` - linux; 386

```console
$ docker pull consul@sha256:55669dfe9f36283013fe5df4242a4018d0f867c48edbed31865846791264572b
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.3 MB (45280360 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:67273333547d454a13e319b3d146cb12cfb8fe64a6744d026015afb23657d7f9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:19:16 GMT
ARG CONSUL_VERSION=1.9.10
# Sat, 13 Nov 2021 06:19:16 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.10 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 13 Nov 2021 06:19:16 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 13 Nov 2021 06:19:17 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 13 Nov 2021 06:19:25 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 13 Nov 2021 06:19:26 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 13 Nov 2021 06:19:27 GMT
# ARGS: CONSUL_VERSION=1.9.10
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 06:19:27 GMT
VOLUME [/consul/data]
# Sat, 13 Nov 2021 06:19:28 GMT
EXPOSE 8300
# Sat, 13 Nov 2021 06:19:28 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 13 Nov 2021 06:19:28 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 13 Nov 2021 06:19:28 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Nov 2021 06:19:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 06:19:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c77ae2949f0c68422ea7eb3c79cdee4b8016a48f3c056625d981fda2126a4f92`  
		Last Modified: Sat, 13 Nov 2021 06:20:58 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:333790003bf543bc1470abdabe948ff03bfc53fae887d0928559e96eaf0fac3f`  
		Last Modified: Sat, 13 Nov 2021 06:21:05 GMT  
		Size: 42.4 MB (42448180 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:51c44e93225d9f849ee5d8490adcfd304fd24cc989d6637b07d32aa67c9d7a6d`  
		Last Modified: Sat, 13 Nov 2021 06:20:57 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63a156e59d99bb9c6105ba227d4028a1add1fac8f08518475a70849a924c136a`  
		Last Modified: Sat, 13 Nov 2021 06:20:57 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c59ca8eeaf0ca7d2fde65e0b7259bf8923ba973e6dfa858596c7ee50c019d736`  
		Last Modified: Sat, 13 Nov 2021 06:20:57 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:9806c8b77144ec19d594bf6d8a6e04634ebe63a2d734539c484bbe0d10b8e6ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:4fc771d6614f6d7af92653e006157b9c98a05098e43dc485d29d9c846abcc33d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43242800 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d9814b25e52bae10d44d9953bad57d86e8577283652bc9443be9738031389c48`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 12 Nov 2021 21:58:14 GMT
ARG CONSUL_VERSION=1.10.3
# Fri, 12 Nov 2021 21:58:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 12 Nov 2021 21:58:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 12 Nov 2021 21:58:17 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 12 Nov 2021 21:58:30 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 12 Nov 2021 21:58:32 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 12 Nov 2021 21:58:35 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 12 Nov 2021 21:58:35 GMT
VOLUME [/consul/data]
# Fri, 12 Nov 2021 21:58:36 GMT
EXPOSE 8300
# Fri, 12 Nov 2021 21:58:36 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 12 Nov 2021 21:58:36 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 12 Nov 2021 21:58:37 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 12 Nov 2021 21:58:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 12 Nov 2021 21:58:38 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:79efaa79e0b89d613b7eeb02676f2c706bf77bac920e8657f0f9badfb6205340`  
		Last Modified: Fri, 12 Nov 2021 22:00:01 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d0b6fccdd38073e2a0303fb7450154fb88dd5211f8abbd8ab1b55e2514a24cb1`  
		Last Modified: Fri, 12 Nov 2021 22:00:07 GMT  
		Size: 40.4 MB (40417007 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:73a1a23e6dad553737585a3b60948d19896dd3c8aeb3ec7e62e0bf03560f416e`  
		Last Modified: Fri, 12 Nov 2021 22:00:01 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ae16349669345cc0fb16abc18cd48c1dbf94910caaee5431326c3cf34882559`  
		Last Modified: Fri, 12 Nov 2021 22:00:01 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96fa79365c2a7793d97996a84e1a8e28dec95f530224a746f6d4cdca6dfe5f73`  
		Last Modified: Fri, 12 Nov 2021 22:00:01 GMT  
		Size: 1.8 KB (1785 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:89cd92136a7b8ebd035cb1a0e39b8e96abc49edf60c9200a27f117054b53932c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.3 MB (39269139 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bd4b0d9415b5a09650d466ee78ea76f2f5f821de5e796590f9339aa0c50e30b8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:03:14 GMT
ARG CONSUL_VERSION=1.10.3
# Sat, 13 Nov 2021 06:03:15 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 13 Nov 2021 06:03:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 13 Nov 2021 06:03:17 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 13 Nov 2021 06:03:29 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 13 Nov 2021 06:03:31 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 13 Nov 2021 06:03:33 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 06:03:34 GMT
VOLUME [/consul/data]
# Sat, 13 Nov 2021 06:03:34 GMT
EXPOSE 8300
# Sat, 13 Nov 2021 06:03:35 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 13 Nov 2021 06:03:35 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 13 Nov 2021 06:03:36 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Nov 2021 06:03:36 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 06:03:37 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b95e092b4de70f76b87ef5e2952153af28de56b56c428d170b0f028fb6afbf1d`  
		Last Modified: Sat, 13 Nov 2021 06:06:08 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:598923641df439f939be74ba7dc244ef98d48641e316ff947702b24a279c956d`  
		Last Modified: Sat, 13 Nov 2021 06:06:27 GMT  
		Size: 36.6 MB (36632428 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9b856a08c888ad010360a1dd58e1196cab9d0a174889c005fd0dd1c23a5225c4`  
		Last Modified: Sat, 13 Nov 2021 06:06:08 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fde4ced118232a40da2c756413e2ca1148a45efc645d9f750f232a1dcd7f945f`  
		Last Modified: Sat, 13 Nov 2021 06:06:08 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e826ae63c559c7b16801bd6e94f70546fbf8739bbb8a33eae3edd323fd2797b7`  
		Last Modified: Sat, 13 Nov 2021 06:06:08 GMT  
		Size: 1.8 KB (1781 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:34988991d554ab9d710529135c77747ba808b12654d1062c5811cb3465078221
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.2 MB (39190366 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d494725d24cc77ece20111697554c7e44d02326ac63bac482f6c5c7c520a427c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 01 Sep 2021 02:50:45 GMT
ADD file:924de68748d5d710724ceb45b3bff9d38eedcad50d5744be4ce74f8f731a791f in / 
# Wed, 01 Sep 2021 02:50:45 GMT
CMD ["/bin/sh"]
# Tue, 02 Nov 2021 19:39:58 GMT
ARG CONSUL_VERSION=1.10.3
# Tue, 02 Nov 2021 19:39:59 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Tue, 02 Nov 2021 19:40:00 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 02 Nov 2021 19:40:01 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 02 Nov 2021 19:40:14 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 02 Nov 2021 19:40:15 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 02 Nov 2021 19:40:16 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 02 Nov 2021 19:40:17 GMT
VOLUME [/consul/data]
# Tue, 02 Nov 2021 19:40:18 GMT
EXPOSE 8300
# Tue, 02 Nov 2021 19:40:19 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 02 Nov 2021 19:40:20 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 02 Nov 2021 19:40:22 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 02 Nov 2021 19:40:22 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 02 Nov 2021 19:40:23 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:bbf911997326f5b56d515142e8dbdbe01d2f308276938ddbce3ab347584ed8ce`  
		Last Modified: Wed, 01 Sep 2021 02:51:37 GMT  
		Size: 2.7 MB (2713008 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:37670a2a9dc09fe75ad47ca2b119cfaed5f2978da6f457430dee234dada7ea43`  
		Last Modified: Tue, 02 Nov 2021 19:42:09 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:919087a5490ea994435e800db080ee62a36ba94db46d8b2279447371e06648ad`  
		Last Modified: Tue, 02 Nov 2021 19:42:14 GMT  
		Size: 36.5 MB (36474046 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46b44e0042b56affa731efc3552e6d27a1c1a27c113ef7c2303abe8fb4a8c6c2`  
		Last Modified: Tue, 02 Nov 2021 19:42:09 GMT  
		Size: 141.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b020cd44b1a8b856d502623a20f69a02ed6f581b1955a5951159a088820f6052`  
		Last Modified: Tue, 02 Nov 2021 19:42:09 GMT  
		Size: 152.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f43e375f5a466436cb3909f15c21a61e93bf531c521f1ba1b6bb737296f910fa`  
		Last Modified: Tue, 02 Nov 2021 19:42:09 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:f6d4990606abae58cfa07041438a83774585b1976889aa17ecfb69c10582149d
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **42.6 MB (42624588 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0266e05a345c091de13c2cf497e8d5c997539a31384988e30a540f6338d8e095`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Sat, 13 Nov 2021 06:18:54 GMT
ARG CONSUL_VERSION=1.10.3
# Sat, 13 Nov 2021 06:18:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.3 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 13 Nov 2021 06:18:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 13 Nov 2021 06:18:56 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 13 Nov 2021 06:19:06 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 13 Nov 2021 06:19:07 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 13 Nov 2021 06:19:08 GMT
# ARGS: CONSUL_VERSION=1.10.3
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 13 Nov 2021 06:19:08 GMT
VOLUME [/consul/data]
# Sat, 13 Nov 2021 06:19:08 GMT
EXPOSE 8300
# Sat, 13 Nov 2021 06:19:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 13 Nov 2021 06:19:09 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 13 Nov 2021 06:19:09 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 13 Nov 2021 06:19:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 13 Nov 2021 06:19:10 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:74ad71c51a3aaa36ca93ff2d29be265437f8d6a6a3265229463a32d757ab063c`  
		Last Modified: Sat, 13 Nov 2021 06:20:36 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:264e1a84ec19e245b5b17560ae89a7a20d673c5065b8e31ad33e1dec79c3a5fc`  
		Last Modified: Sat, 13 Nov 2021 06:20:42 GMT  
		Size: 39.8 MB (39792406 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a52249b1ddd029a0a2974e3e28a7d4ba4eb74ba1428eba364aab8c0634680193`  
		Last Modified: Sat, 13 Nov 2021 06:20:36 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eb1e3c995ef13035d9e1361df724e4dbb2f695c7fdf5a1a5dac866ececfd2f54`  
		Last Modified: Sat, 13 Nov 2021 06:20:36 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eefa7778ca9c4c1248a35f60f616d57440c6dda91f0b4afcbf7b464258fa72cf`  
		Last Modified: Sat, 13 Nov 2021 06:20:36 GMT  
		Size: 1.8 KB (1784 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
