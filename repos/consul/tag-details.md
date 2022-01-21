<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.10`](#consul110)
-	[`consul:1.10.7`](#consul1107)
-	[`consul:1.11`](#consul111)
-	[`consul:1.11.2`](#consul1112)
-	[`consul:1.9`](#consul19)
-	[`consul:1.9.14`](#consul1914)
-	[`consul:latest`](#consullatest)

## `consul:1.10`

```console
$ docker pull consul@sha256:6fd8fab69596a095a780f4123531c44460a39e0bcf228090f2bf03e03cad55ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10` - linux; amd64

```console
$ docker pull consul@sha256:64bb8a400463ba49f5d7df6a03bf3e24dd60c58388eb50768f5e5d218bc8cc18
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43702129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2448a121106f91690ef1735213740106070d1b2fc2a906eec6ccd18bc8b726c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:19:54 GMT
ARG CONSUL_VERSION=1.10.7
# Fri, 14 Jan 2022 18:19:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:19:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:19:55 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:20:09 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:20:10 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:20:11 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:20:11 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:20:11 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:20:12 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:20:12 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:20:12 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:20:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:20:12 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6386278449b4403e5f923aac925a34ffa25337b82712c40ca70b934d3676ed31`  
		Last Modified: Fri, 14 Jan 2022 18:22:23 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d494b414b865191a9d497d3835f3e50e93e6b6d6fdd86de4d63a0db9d9fe7285`  
		Last Modified: Fri, 14 Jan 2022 18:22:29 GMT  
		Size: 40.9 MB (40876330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5ac0b6f22d44c76dad4a624baed2d802668d239f7fc1776fa2722a8b040eff`  
		Last Modified: Fri, 14 Jan 2022 18:22:23 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d32c50e5a3bd7e41f92e7dd23998d0364bb09eb86577543fc2eb1f77b8250c`  
		Last Modified: Fri, 14 Jan 2022 18:22:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc85959dfa405726f5adc6a22712fa59e307977ed41311a0cfcf3cbbe200884c`  
		Last Modified: Fri, 14 Jan 2022 18:22:23 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm variant v6

```console
$ docker pull consul@sha256:26b5a5a297a209db8889449cc8b9c439cbd59b5d856194e5fe22284cdde3eed1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41769455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db170642d388c18767c9117341bfa67420ab5e4e927eeff5dea81766488c7091`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:50:22 GMT
ARG CONSUL_VERSION=1.10.7
# Fri, 14 Jan 2022 18:50:22 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:50:23 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:50:24 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:50:39 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:50:41 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:50:42 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:50:42 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:50:43 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:50:43 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:50:44 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:50:44 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:50:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:50:45 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cc1c9cbe3d9a91665c55d7dd3a87951cfbad0f6a8159d57f5515ffe04e8aa7`  
		Last Modified: Fri, 14 Jan 2022 18:52:43 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d0595c26bc2bb714750ef98706571d732aae3e4f9248d640dec7fded960efb`  
		Last Modified: Fri, 14 Jan 2022 18:53:04 GMT  
		Size: 39.1 MB (39132740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e0ac3812cf0da12454107d2954fdcce544000c8aab536a1998775b7cd9e445`  
		Last Modified: Fri, 14 Jan 2022 18:52:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbdb539115e0abc73145ca1a05d6eee1b93c3f387d8c67b59257725f044ffee`  
		Last Modified: Fri, 14 Jan 2022 18:52:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674045c72057e39e1144f095d8afa30a3a63baf2861efc44d289b0a31c71f7bf`  
		Last Modified: Fri, 14 Jan 2022 18:52:43 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:cd5ec37f682d4f5998bb84f5cc17d18a111f445026e2786897ca8768ea62a872
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41715478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c19bfeda29c379abb37f674152c071f4a3cc76203229fcd2999628899f06dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:40:11 GMT
ARG CONSUL_VERSION=1.10.7
# Fri, 14 Jan 2022 18:40:12 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:40:13 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:40:14 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:40:25 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:40:26 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:40:26 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:40:27 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:40:28 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:40:29 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:40:30 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:40:32 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:40:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:40:33 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced2d5fdae89a98eb6a468152f0c8f1733d8b50be03db3287cd7a463a161c489`  
		Last Modified: Fri, 14 Jan 2022 18:41:40 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2877b7539508f4b04e834ce7af2f7a67ce9725d5b4b2897eeabc79ea91886eb`  
		Last Modified: Fri, 14 Jan 2022 18:41:45 GMT  
		Size: 39.0 MB (38992524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1b75107d00040bfda8eb53591367afb62a5c493adfe258a3a18b17f37ea8ad`  
		Last Modified: Fri, 14 Jan 2022 18:41:40 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7fc7f191dd1df6a3b31dfa66172ecf4ab927d9c6a7e0ee4ad5b5829e8522e4`  
		Last Modified: Fri, 14 Jan 2022 18:41:40 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:845f76ea5b7d91648c13339a4892ca1d4b1eadbe818d31bfc46e09ac8bb17d96`  
		Last Modified: Fri, 14 Jan 2022 18:41:40 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; 386

```console
$ docker pull consul@sha256:1b25779d901641251467cc535e30141a1ca1719ec4307ca837dd21cbc90c9577
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43080959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe309fb03fefad62d805a508de077eada66369a53e1c931b288d7adb0c035d52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:38:50 GMT
ARG CONSUL_VERSION=1.10.7
# Fri, 14 Jan 2022 18:38:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:38:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:38:52 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:39:08 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:39:09 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:39:10 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:39:10 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:39:10 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:39:10 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:39:11 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:39:11 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:39:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:39:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0593031475fe4b1cfe875e6681c58de6da51c9b33be9afa4b8e5f97337a9c109`  
		Last Modified: Fri, 14 Jan 2022 18:40:16 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea8851cb9959ddbdf897338dd56be75b3d9bf9561fd0f5a47eb818cc40cc045`  
		Last Modified: Fri, 14 Jan 2022 18:40:22 GMT  
		Size: 40.2 MB (40248775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2687225400f52b25b70b94f2a4ce14356b08da7e5f448c7a679c55726bffd3`  
		Last Modified: Fri, 14 Jan 2022 18:40:17 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e73d721b0d8751ef5b3779e876e4d61f1fbb5d2745e80294e4d47063281e21`  
		Last Modified: Fri, 14 Jan 2022 18:40:16 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bf7ae7a318ad43d67e8f6d315365749e207fab4e2f6dd5a10447ba5887b5f4`  
		Last Modified: Fri, 14 Jan 2022 18:40:16 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.10.7`

```console
$ docker pull consul@sha256:6fd8fab69596a095a780f4123531c44460a39e0bcf228090f2bf03e03cad55ef
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10.7` - linux; amd64

```console
$ docker pull consul@sha256:64bb8a400463ba49f5d7df6a03bf3e24dd60c58388eb50768f5e5d218bc8cc18
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.7 MB (43702129 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:2448a121106f91690ef1735213740106070d1b2fc2a906eec6ccd18bc8b726c7`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:19:54 GMT
ARG CONSUL_VERSION=1.10.7
# Fri, 14 Jan 2022 18:19:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:19:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:19:55 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:20:09 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:20:10 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:20:11 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:20:11 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:20:11 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:20:12 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:20:12 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:20:12 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:20:12 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:20:12 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6386278449b4403e5f923aac925a34ffa25337b82712c40ca70b934d3676ed31`  
		Last Modified: Fri, 14 Jan 2022 18:22:23 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d494b414b865191a9d497d3835f3e50e93e6b6d6fdd86de4d63a0db9d9fe7285`  
		Last Modified: Fri, 14 Jan 2022 18:22:29 GMT  
		Size: 40.9 MB (40876330 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee5ac0b6f22d44c76dad4a624baed2d802668d239f7fc1776fa2722a8b040eff`  
		Last Modified: Fri, 14 Jan 2022 18:22:23 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:05d32c50e5a3bd7e41f92e7dd23998d0364bb09eb86577543fc2eb1f77b8250c`  
		Last Modified: Fri, 14 Jan 2022 18:22:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cc85959dfa405726f5adc6a22712fa59e307977ed41311a0cfcf3cbbe200884c`  
		Last Modified: Fri, 14 Jan 2022 18:22:23 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.7` - linux; arm variant v6

```console
$ docker pull consul@sha256:26b5a5a297a209db8889449cc8b9c439cbd59b5d856194e5fe22284cdde3eed1
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.8 MB (41769455 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:db170642d388c18767c9117341bfa67420ab5e4e927eeff5dea81766488c7091`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:50:22 GMT
ARG CONSUL_VERSION=1.10.7
# Fri, 14 Jan 2022 18:50:22 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:50:23 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:50:24 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:50:39 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:50:41 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:50:42 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:50:42 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:50:43 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:50:43 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:50:44 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:50:44 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:50:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:50:45 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e8cc1c9cbe3d9a91665c55d7dd3a87951cfbad0f6a8159d57f5515ffe04e8aa7`  
		Last Modified: Fri, 14 Jan 2022 18:52:43 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f6d0595c26bc2bb714750ef98706571d732aae3e4f9248d640dec7fded960efb`  
		Last Modified: Fri, 14 Jan 2022 18:53:04 GMT  
		Size: 39.1 MB (39132740 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f8e0ac3812cf0da12454107d2954fdcce544000c8aab536a1998775b7cd9e445`  
		Last Modified: Fri, 14 Jan 2022 18:52:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bfbdb539115e0abc73145ca1a05d6eee1b93c3f387d8c67b59257725f044ffee`  
		Last Modified: Fri, 14 Jan 2022 18:52:44 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:674045c72057e39e1144f095d8afa30a3a63baf2861efc44d289b0a31c71f7bf`  
		Last Modified: Fri, 14 Jan 2022 18:52:43 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.7` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:cd5ec37f682d4f5998bb84f5cc17d18a111f445026e2786897ca8768ea62a872
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41715478 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:35c19bfeda29c379abb37f674152c071f4a3cc76203229fcd2999628899f06dc`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:40:11 GMT
ARG CONSUL_VERSION=1.10.7
# Fri, 14 Jan 2022 18:40:12 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:40:13 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:40:14 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:40:25 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:40:26 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:40:26 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:40:27 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:40:28 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:40:29 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:40:30 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:40:32 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:40:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:40:33 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ced2d5fdae89a98eb6a468152f0c8f1733d8b50be03db3287cd7a463a161c489`  
		Last Modified: Fri, 14 Jan 2022 18:41:40 GMT  
		Size: 1.2 KB (1230 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2877b7539508f4b04e834ce7af2f7a67ce9725d5b4b2897eeabc79ea91886eb`  
		Last Modified: Fri, 14 Jan 2022 18:41:45 GMT  
		Size: 39.0 MB (38992524 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe1b75107d00040bfda8eb53591367afb62a5c493adfe258a3a18b17f37ea8ad`  
		Last Modified: Fri, 14 Jan 2022 18:41:40 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e7fc7f191dd1df6a3b31dfa66172ecf4ab927d9c6a7e0ee4ad5b5829e8522e4`  
		Last Modified: Fri, 14 Jan 2022 18:41:40 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:845f76ea5b7d91648c13339a4892ca1d4b1eadbe818d31bfc46e09ac8bb17d96`  
		Last Modified: Fri, 14 Jan 2022 18:41:40 GMT  
		Size: 1.8 KB (1788 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.7` - linux; 386

```console
$ docker pull consul@sha256:1b25779d901641251467cc535e30141a1ca1719ec4307ca837dd21cbc90c9577
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.1 MB (43080959 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:fe309fb03fefad62d805a508de077eada66369a53e1c931b288d7adb0c035d52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:38:50 GMT
ARG CONSUL_VERSION=1.10.7
# Fri, 14 Jan 2022 18:38:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.10.7 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:38:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:38:52 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:39:08 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:39:09 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:39:10 GMT
# ARGS: CONSUL_VERSION=1.10.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:39:10 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:39:10 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:39:10 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:39:11 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:39:11 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:39:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:39:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0593031475fe4b1cfe875e6681c58de6da51c9b33be9afa4b8e5f97337a9c109`  
		Last Modified: Fri, 14 Jan 2022 18:40:16 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7ea8851cb9959ddbdf897338dd56be75b3d9bf9561fd0f5a47eb818cc40cc045`  
		Last Modified: Fri, 14 Jan 2022 18:40:22 GMT  
		Size: 40.2 MB (40248775 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae2687225400f52b25b70b94f2a4ce14356b08da7e5f448c7a679c55726bffd3`  
		Last Modified: Fri, 14 Jan 2022 18:40:17 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d7e73d721b0d8751ef5b3779e876e4d61f1fbb5d2745e80294e4d47063281e21`  
		Last Modified: Fri, 14 Jan 2022 18:40:16 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a8bf7ae7a318ad43d67e8f6d315365749e207fab4e2f6dd5a10447ba5887b5f4`  
		Last Modified: Fri, 14 Jan 2022 18:40:16 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.11`

```console
$ docker pull consul@sha256:43cc31d422649c88fec7f5c146110854149da68ee70c505f5bbd667c71bc698a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.11` - linux; amd64

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

### `consul:1.11` - linux; arm variant v6

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

### `consul:1.11` - linux; arm64 variant v8

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

### `consul:1.11` - linux; 386

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

## `consul:1.11.2`

```console
$ docker pull consul@sha256:43cc31d422649c88fec7f5c146110854149da68ee70c505f5bbd667c71bc698a
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.11.2` - linux; amd64

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

### `consul:1.11.2` - linux; arm variant v6

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

### `consul:1.11.2` - linux; arm64 variant v8

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

### `consul:1.11.2` - linux; 386

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

## `consul:1.9`

```console
$ docker pull consul@sha256:2f35f9d3ee051fa25311894c2740d3915fd08c8c9c1ca1648e180abf20aa21dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9` - linux; amd64

```console
$ docker pull consul@sha256:6aa8b6869809d0e522cf3098abb8164749a9a9642e6458ca084a81546fd7af24
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40186817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fec3b64b99ae4a4f5a0213ea4b17ef35b361adccd5fdb2572ecc96810ceb22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:20:17 GMT
ARG CONSUL_VERSION=1.9.14
# Fri, 14 Jan 2022 18:20:17 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.14 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:20:17 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:20:18 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:20:52 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:20:53 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:20:54 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:20:54 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:20:55 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:20:55 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:20:55 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:20:55 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:20:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9404fc309f18dec67cc01caf7f46c70d5063f23b93e5cf58c794dff89e9dffb8`  
		Last Modified: Fri, 14 Jan 2022 18:23:00 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db6fd1d712f19f5e37518a8928338690f0aea86b37a79e115229dd3e7f62688`  
		Last Modified: Fri, 14 Jan 2022 18:23:05 GMT  
		Size: 37.4 MB (37361020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef22807f8bd72cf8f2e407f8840a9b9236326a08b747bf4cbe5fe288231302e`  
		Last Modified: Fri, 14 Jan 2022 18:22:59 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296f4b2065d929c8308b295c4257e2af845e2b47d637f11249c644d8b912200b`  
		Last Modified: Fri, 14 Jan 2022 18:23:00 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfae83c0341b8317db13a32e6abed487c1bd04a028fb837fef096ede4cb5b7d1`  
		Last Modified: Fri, 14 Jan 2022 18:23:00 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:c4ff550d3c26885898398e3503ad129563748adb1dbed17d161fa52954b0bf5a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38229593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6bf67f42b8800b42c2976a6e2dc9eda8d98cd90f82c0b87f268899308615a62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:50:56 GMT
ARG CONSUL_VERSION=1.9.14
# Fri, 14 Jan 2022 18:50:57 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.14 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:50:57 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:50:58 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:51:15 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:51:17 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:51:18 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:51:18 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:51:19 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:51:19 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:51:20 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:51:20 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:51:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:51:21 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeeb953e65a969234147e418dc7d5d6822a7384f598603d4a95620ce8f5179c`  
		Last Modified: Fri, 14 Jan 2022 18:53:17 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a91f6fa6034693705cebe373c62a151d41f576860cb443215588ac62bcb719`  
		Last Modified: Fri, 14 Jan 2022 18:53:39 GMT  
		Size: 35.6 MB (35592874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9000f488aab2e68600c706e45ee8576bd01cdcd104bab5e19e92f511fb2c293`  
		Last Modified: Fri, 14 Jan 2022 18:53:17 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee55390692ee4742da5fa6f048994225671e35aae6100b56a0ee59eee8b14431`  
		Last Modified: Fri, 14 Jan 2022 18:53:17 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9794ebdc34347e3b4fa1f624b90c0cc2215e7164a7f9460d1aa36e7afd1d6901`  
		Last Modified: Fri, 14 Jan 2022 18:53:17 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:003be37312a0ee2537a271b4ef2b36e6b89892e50653b4e3ed8eb2c1cd8e34a3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38179861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3365225d1b2f36bbcd210b7b3a577202deb80bd065ca0b065da292d42c768549`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:40:38 GMT
ARG CONSUL_VERSION=1.9.14
# Fri, 14 Jan 2022 18:40:39 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.14 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:40:40 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:40:41 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:40:52 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:40:52 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:40:53 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:40:54 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:40:55 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:40:56 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:40:57 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:40:59 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:40:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:41:00 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7439133698bbbd600cf9d81057f5df91f92892e449e5bd2f672c09d8417570`  
		Last Modified: Fri, 14 Jan 2022 18:41:56 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1a738821d02cc4713eb5a0e06e1285d353b0e78a1fc422f9f12ab52831bc7f`  
		Last Modified: Fri, 14 Jan 2022 18:42:01 GMT  
		Size: 35.5 MB (35456907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b10520793f292d10f5862e10d4349f4b5e8dac2f667c397c9e74989a6984f6`  
		Last Modified: Fri, 14 Jan 2022 18:41:56 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675f8d76a61da0e0ac8d8516c3b1b941c8c3caca512633169db378da41690d17`  
		Last Modified: Fri, 14 Jan 2022 18:41:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e45719eb90d072234e25c87caf9254d85daccc866886c4cb9f96929370a8ea`  
		Last Modified: Fri, 14 Jan 2022 18:41:56 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; 386

```console
$ docker pull consul@sha256:2dedd279247f67ce3fb49de4b863667ab21e7e5d7b7d05ebb5fd64ff1f8f25bc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39525098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e73bdda17bf60a6befdc720c722bed8de90b48c6cb485e3d45f3c8f7090dda9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:39:17 GMT
ARG CONSUL_VERSION=1.9.14
# Fri, 14 Jan 2022 18:39:17 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.14 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:39:17 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:39:18 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 21 Jan 2022 18:51:29 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 21 Jan 2022 18:51:30 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 21 Jan 2022 18:51:31 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 21 Jan 2022 18:51:31 GMT
VOLUME [/consul/data]
# Fri, 21 Jan 2022 18:51:31 GMT
EXPOSE 8300
# Fri, 21 Jan 2022 18:51:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 21 Jan 2022 18:51:32 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 21 Jan 2022 18:51:32 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 21 Jan 2022 18:51:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Jan 2022 18:51:32 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2990cba78658da1fe597bab83ae381f92d4cb03f151962f52c96c0a63bb5f061`  
		Last Modified: Fri, 21 Jan 2022 18:52:00 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099d3a200ea798782758b82dde89157dd885c7e75877bf91e3fb76523031663a`  
		Last Modified: Fri, 21 Jan 2022 18:52:05 GMT  
		Size: 36.7 MB (36692920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9e8ed5acc0cdaaf439751f9ebddcaea1205b39fb9c4d33a8f259c2f92ffb25`  
		Last Modified: Fri, 21 Jan 2022 18:52:00 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07be9f6d2f774dcea5999ca10c3bdda92257844e5570bb6d81ad0dbcc65b792e`  
		Last Modified: Fri, 21 Jan 2022 18:52:00 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e76cc333c10f98075b79df21b626f201e1ec375516b47aa0e5f1c5c887c4e2f`  
		Last Modified: Fri, 21 Jan 2022 18:52:00 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9.14`

```console
$ docker pull consul@sha256:2f35f9d3ee051fa25311894c2740d3915fd08c8c9c1ca1648e180abf20aa21dc
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9.14` - linux; amd64

```console
$ docker pull consul@sha256:6aa8b6869809d0e522cf3098abb8164749a9a9642e6458ca084a81546fd7af24
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **40.2 MB (40186817 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:12fec3b64b99ae4a4f5a0213ea4b17ef35b361adccd5fdb2572ecc96810ceb22`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 17:19:58 GMT
ADD file:5a707b9d6cb5fff532e4c2141bc35707593f21da5528c9e71ae2ddb6ba4a4eb6 in / 
# Fri, 12 Nov 2021 17:19:58 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:20:17 GMT
ARG CONSUL_VERSION=1.9.14
# Fri, 14 Jan 2022 18:20:17 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.14 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:20:17 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:20:18 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:20:52 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:20:53 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:20:54 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:20:54 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:20:55 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:20:55 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:20:55 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:20:55 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:20:55 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:20:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:5758d4e389a3f662e94a85fb76143dbe338b64f8d2a65f45536a9663b05305ad`  
		Last Modified: Fri, 12 Nov 2021 17:21:00 GMT  
		Size: 2.8 MB (2822425 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9404fc309f18dec67cc01caf7f46c70d5063f23b93e5cf58c794dff89e9dffb8`  
		Last Modified: Fri, 14 Jan 2022 18:23:00 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5db6fd1d712f19f5e37518a8928338690f0aea86b37a79e115229dd3e7f62688`  
		Last Modified: Fri, 14 Jan 2022 18:23:05 GMT  
		Size: 37.4 MB (37361020 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8ef22807f8bd72cf8f2e407f8840a9b9236326a08b747bf4cbe5fe288231302e`  
		Last Modified: Fri, 14 Jan 2022 18:22:59 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:296f4b2065d929c8308b295c4257e2af845e2b47d637f11249c644d8b912200b`  
		Last Modified: Fri, 14 Jan 2022 18:23:00 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfae83c0341b8317db13a32e6abed487c1bd04a028fb837fef096ede4cb5b7d1`  
		Last Modified: Fri, 14 Jan 2022 18:23:00 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.14` - linux; arm variant v6

```console
$ docker pull consul@sha256:c4ff550d3c26885898398e3503ad129563748adb1dbed17d161fa52954b0bf5a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38229593 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f6bf67f42b8800b42c2976a6e2dc9eda8d98cd90f82c0b87f268899308615a62`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:49:57 GMT
ADD file:26e756fd544e28ae75be38d81452cf3266a2dabcffe9ecce3af2db9fde9edea3 in / 
# Fri, 12 Nov 2021 16:49:58 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:50:56 GMT
ARG CONSUL_VERSION=1.9.14
# Fri, 14 Jan 2022 18:50:57 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.14 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:50:57 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:50:58 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:51:15 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:51:17 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:51:18 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:51:18 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:51:19 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:51:19 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:51:20 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:51:20 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:51:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:51:21 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:846f3a0f3493d22f22643b6a1c057d2d37e608433cd1033d25dac92032b8b9e3`  
		Last Modified: Fri, 12 Nov 2021 16:51:54 GMT  
		Size: 2.6 MB (2633344 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6aeeb953e65a969234147e418dc7d5d6822a7384f598603d4a95620ce8f5179c`  
		Last Modified: Fri, 14 Jan 2022 18:53:17 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:83a91f6fa6034693705cebe373c62a151d41f576860cb443215588ac62bcb719`  
		Last Modified: Fri, 14 Jan 2022 18:53:39 GMT  
		Size: 35.6 MB (35592874 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b9000f488aab2e68600c706e45ee8576bd01cdcd104bab5e19e92f511fb2c293`  
		Last Modified: Fri, 14 Jan 2022 18:53:17 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ee55390692ee4742da5fa6f048994225671e35aae6100b56a0ee59eee8b14431`  
		Last Modified: Fri, 14 Jan 2022 18:53:17 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9794ebdc34347e3b4fa1f624b90c0cc2215e7164a7f9460d1aa36e7afd1d6901`  
		Last Modified: Fri, 14 Jan 2022 18:53:17 GMT  
		Size: 1.8 KB (1787 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.14` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:003be37312a0ee2537a271b4ef2b36e6b89892e50653b4e3ed8eb2c1cd8e34a3
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **38.2 MB (38179861 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3365225d1b2f36bbcd210b7b3a577202deb80bd065ca0b065da292d42c768549`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:40:05 GMT
ADD file:ad85e8724ab9b90e37aadca9513807d07d557e7fc4287ca017f01f269aff3920 in / 
# Fri, 12 Nov 2021 16:40:06 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:40:38 GMT
ARG CONSUL_VERSION=1.9.14
# Fri, 14 Jan 2022 18:40:39 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.14 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:40:40 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:40:41 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 14 Jan 2022 18:40:52 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 14 Jan 2022 18:40:52 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 14 Jan 2022 18:40:53 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 14 Jan 2022 18:40:54 GMT
VOLUME [/consul/data]
# Fri, 14 Jan 2022 18:40:55 GMT
EXPOSE 8300
# Fri, 14 Jan 2022 18:40:56 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 14 Jan 2022 18:40:57 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 14 Jan 2022 18:40:59 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 14 Jan 2022 18:40:59 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 14 Jan 2022 18:41:00 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:06decbbdea2401b400024fb2feadd51ee381cd4b7b78a30306c3828ec9f6c760`  
		Last Modified: Fri, 12 Nov 2021 16:41:15 GMT  
		Size: 2.7 MB (2719640 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5f7439133698bbbd600cf9d81057f5df91f92892e449e5bd2f672c09d8417570`  
		Last Modified: Fri, 14 Jan 2022 18:41:56 GMT  
		Size: 1.2 KB (1232 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ec1a738821d02cc4713eb5a0e06e1285d353b0e78a1fc422f9f12ab52831bc7f`  
		Last Modified: Fri, 14 Jan 2022 18:42:01 GMT  
		Size: 35.5 MB (35456907 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68b10520793f292d10f5862e10d4349f4b5e8dac2f667c397c9e74989a6984f6`  
		Last Modified: Fri, 14 Jan 2022 18:41:56 GMT  
		Size: 142.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675f8d76a61da0e0ac8d8516c3b1b941c8c3caca512633169db378da41690d17`  
		Last Modified: Fri, 14 Jan 2022 18:41:56 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:12e45719eb90d072234e25c87caf9254d85daccc866886c4cb9f96929370a8ea`  
		Last Modified: Fri, 14 Jan 2022 18:41:56 GMT  
		Size: 1.8 KB (1786 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.14` - linux; 386

```console
$ docker pull consul@sha256:2dedd279247f67ce3fb49de4b863667ab21e7e5d7b7d05ebb5fd64ff1f8f25bc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.5 MB (39525098 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3e73bdda17bf60a6befdc720c722bed8de90b48c6cb485e3d45f3c8f7090dda9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 12 Nov 2021 16:38:50 GMT
ADD file:f6503c5a96198c02627cf7250b271ec6d49ffa83a87a588498eee61ba7f9c6fe in / 
# Fri, 12 Nov 2021 16:38:50 GMT
CMD ["/bin/sh"]
# Fri, 14 Jan 2022 18:39:17 GMT
ARG CONSUL_VERSION=1.9.14
# Fri, 14 Jan 2022 18:39:17 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.9.14 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 14 Jan 2022 18:39:17 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 14 Jan 2022 18:39:18 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 21 Jan 2022 18:51:29 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 21 Jan 2022 18:51:30 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 21 Jan 2022 18:51:31 GMT
# ARGS: CONSUL_VERSION=1.9.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 21 Jan 2022 18:51:31 GMT
VOLUME [/consul/data]
# Fri, 21 Jan 2022 18:51:31 GMT
EXPOSE 8300
# Fri, 21 Jan 2022 18:51:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 21 Jan 2022 18:51:32 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 21 Jan 2022 18:51:32 GMT
COPY file:54fea1810b618dd421534c8fbe34fd9d05aa23929d2290f19c325d1c23d960c3 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 21 Jan 2022 18:51:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 21 Jan 2022 18:51:32 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:afe0e1febe23918824088b45b415ce1778e92899ae26f0867294eb91de50aa4f`  
		Last Modified: Fri, 12 Nov 2021 16:39:53 GMT  
		Size: 2.8 MB (2828811 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2990cba78658da1fe597bab83ae381f92d4cb03f151962f52c96c0a63bb5f061`  
		Last Modified: Fri, 21 Jan 2022 18:52:00 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:099d3a200ea798782758b82dde89157dd885c7e75877bf91e3fb76523031663a`  
		Last Modified: Fri, 21 Jan 2022 18:52:05 GMT  
		Size: 36.7 MB (36692920 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ce9e8ed5acc0cdaaf439751f9ebddcaea1205b39fb9c4d33a8f259c2f92ffb25`  
		Last Modified: Fri, 21 Jan 2022 18:52:00 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:07be9f6d2f774dcea5999ca10c3bdda92257844e5570bb6d81ad0dbcc65b792e`  
		Last Modified: Fri, 21 Jan 2022 18:52:00 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e76cc333c10f98075b79df21b626f201e1ec375516b47aa0e5f1c5c887c4e2f`  
		Last Modified: Fri, 21 Jan 2022 18:52:00 GMT  
		Size: 1.8 KB (1783 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

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
