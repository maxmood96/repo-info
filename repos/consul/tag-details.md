<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.13`](#consul113)
-	[`consul:1.13.9`](#consul1139)
-	[`consul:1.14`](#consul114)
-	[`consul:1.14.8`](#consul1148)
-	[`consul:1.15`](#consul115)
-	[`consul:1.15.4`](#consul1154)

## `consul:1.13`

```console
$ docker pull consul@sha256:1e4e3ceec04e972aa9b98944c4461ef202309f12e7fdc2fbef7772fb2d951a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.13` - linux; amd64

```console
$ docker pull consul@sha256:9301c1d6675ad78b919f25fe64baf9bafd1e7f229077470dc8987b7af2c826ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52882659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709ec67b3e8470fce6dadd63d0df4f392a6c290063365273916f6fe5cd666c80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:11 GMT
ADD file:aa1af71c6b66d2dddee4797236e3e526f70f904ab641cc0dd6b41445cfedf9b4 in / 
# Thu, 30 Nov 2023 23:23:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:58:18 GMT
ARG CONSUL_VERSION=1.13.9
# Fri, 01 Dec 2023 06:58:18 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 01 Dec 2023 06:58:18 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 01 Dec 2023 06:58:19 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 01 Dec 2023 06:58:24 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 01 Dec 2023 06:58:25 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 01 Dec 2023 06:58:26 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 01 Dec 2023 06:58:26 GMT
VOLUME [/consul/data]
# Fri, 01 Dec 2023 06:58:26 GMT
EXPOSE 8300
# Fri, 01 Dec 2023 06:58:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 01 Dec 2023 06:58:26 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 01 Dec 2023 06:58:26 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 01 Dec 2023 06:58:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 06:58:26 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d078792c4f9122259f14b539315bd92cbd9490ed73e08255a08689122b143108`  
		Last Modified: Thu, 30 Nov 2023 23:23:58 GMT  
		Size: 2.8 MB (2826431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dba966ef6ef17885880841074b2424e1d4b963e78d68081d9dd91431dd2e5e8`  
		Last Modified: Fri, 01 Dec 2023 06:59:05 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb4269433525321ab6345f1e321c964018cbcb38f12ab8caf3e157a039e7791`  
		Last Modified: Fri, 01 Dec 2023 06:59:11 GMT  
		Size: 50.1 MB (50052802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf42966a76373a0dc79f025db1d1d1c49e7c5766744160a4a9b7b4600bdd599`  
		Last Modified: Fri, 01 Dec 2023 06:59:05 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e558cb961615344425ddf507970140aa378a120f11c803ab15366aab61ecfdf9`  
		Last Modified: Fri, 01 Dec 2023 06:59:05 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c43f8ee523ea83de5aa3fed946a2427c3ae4dec83012c5084b4613fe2f92240`  
		Last Modified: Fri, 01 Dec 2023 06:59:05 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13` - linux; arm variant v6

```console
$ docker pull consul@sha256:316233c00f0333574f2ec88e565340ac850207235aa8148e4e343237ed0148d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50380771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f081945c5743156f301bdb751148f53309a8fcb93c6310deb96e9403dc0fa9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:27 GMT
ADD file:2270cb7f14826bc917baa12cd1ff166703f454ccd10ef5799d8106942bb0abe2 in / 
# Thu, 30 Nov 2023 22:49:27 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 01:08:38 GMT
ARG CONSUL_VERSION=1.13.9
# Sat, 16 Mar 2024 01:08:38 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 16 Mar 2024 01:08:38 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 16 Mar 2024 01:08:40 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 16 Mar 2024 01:08:50 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 16 Mar 2024 01:08:52 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 16 Mar 2024 01:08:53 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 16 Mar 2024 01:08:54 GMT
VOLUME [/consul/data]
# Sat, 16 Mar 2024 01:08:54 GMT
EXPOSE 8300
# Sat, 16 Mar 2024 01:08:54 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 16 Mar 2024 01:08:55 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 16 Mar 2024 01:08:55 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 16 Mar 2024 01:08:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 01:08:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:be5e3feadb89f4f40a3bc5997dbddd75fdc3686e938beb9d363990d92db9e4aa`  
		Last Modified: Thu, 30 Nov 2023 22:50:12 GMT  
		Size: 2.6 MB (2633457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc63b553ef8b8a8119558a8a19c5299b24a04c71905c3dd286dbfcdc650e6de0`  
		Last Modified: Sat, 16 Mar 2024 01:09:45 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411b14b841cd76176d1ddfecfd87a323ea4000526524892f497de45af508897a`  
		Last Modified: Sat, 16 Mar 2024 01:09:52 GMT  
		Size: 47.7 MB (47743882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f34b0384c5b0d619807db46ee3076289f862c5e784e95b8ef2b8dc1e67888d`  
		Last Modified: Sat, 16 Mar 2024 01:09:45 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af33cc37dae42ccbb65f164efbc8c2ec695150ec90a03d6a67eb036812c4404c`  
		Last Modified: Sat, 16 Mar 2024 01:09:45 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b826096d6992838494a6b10240eebec11a2d25aaef6f72bdc68afc9924a36bee`  
		Last Modified: Sat, 16 Mar 2024 01:09:45 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:f0428c05d4f2e00575577ff371550ebb55b7bbe0a8caf5af44fe21ca40aa90c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49911756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9339a9151a3e111fcd3dd018e894e5f5fb2149adb322878798595257b6e19b5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:15 GMT
ADD file:3982c510455cc0ceea8cf8dd0b50b69588e35fd4f84522cb4000582c73781672 in / 
# Thu, 30 Nov 2023 23:11:15 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:05:22 GMT
ARG CONSUL_VERSION=1.13.9
# Sat, 16 Mar 2024 03:05:22 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 16 Mar 2024 03:05:22 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 16 Mar 2024 03:05:22 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 16 Mar 2024 03:05:27 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 16 Mar 2024 03:05:28 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 16 Mar 2024 03:05:28 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:05:28 GMT
VOLUME [/consul/data]
# Sat, 16 Mar 2024 03:05:29 GMT
EXPOSE 8300
# Sat, 16 Mar 2024 03:05:29 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 16 Mar 2024 03:05:29 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 16 Mar 2024 03:05:29 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 16 Mar 2024 03:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:05:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8bc1ab4b84041d57f21a792410a00820f73fda7efe08bcd2ca6245349a40299d`  
		Last Modified: Thu, 30 Nov 2023 23:12:02 GMT  
		Size: 2.7 MB (2721527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f55f41307d72d5098b63dd105f1afeabd9c9941c7e4de2e47f1be62332fe04`  
		Last Modified: Sat, 16 Mar 2024 03:06:05 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e358ee67ea4bf16d6d6c78187847ff04273566579ca912341fd24c749e44160e`  
		Last Modified: Sat, 16 Mar 2024 03:06:09 GMT  
		Size: 47.2 MB (47186797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e99432ab36fea86b13a82cba1fbcc5f830efe9eb67c52dfcd2de16f9b7e01b`  
		Last Modified: Sat, 16 Mar 2024 03:06:05 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86f570ba77ee453457be7d7cb8a11996e50843a27705847895adfae2816d67d`  
		Last Modified: Sat, 16 Mar 2024 03:06:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df625012f913ece4a4631cef2e6afa54aa168c48505184a1399ad74a8db5bf6d`  
		Last Modified: Sat, 16 Mar 2024 03:06:05 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13` - linux; 386

```console
$ docker pull consul@sha256:c003dedb910978aae6e493b06a455ed24c8722f79d818306c6e22f8b108b078e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51713193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff04b94bbb3faeaf546c96dd37c4b4264ca35e05f7a89e54bfdd48a29882d47a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 01 Dec 2023 02:04:00 GMT
ADD file:5990d507b1d1b3a4a63574a2ec1c9e2ca4344d30f7618e002039cd6c9693a56d in / 
# Fri, 01 Dec 2023 02:04:00 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:54:04 GMT
ARG CONSUL_VERSION=1.13.9
# Fri, 15 Mar 2024 23:54:04 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 15 Mar 2024 23:54:04 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 15 Mar 2024 23:54:05 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 15 Mar 2024 23:54:12 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 15 Mar 2024 23:54:13 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 15 Mar 2024 23:54:14 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 15 Mar 2024 23:54:14 GMT
VOLUME [/consul/data]
# Fri, 15 Mar 2024 23:54:14 GMT
EXPOSE 8300
# Fri, 15 Mar 2024 23:54:14 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 15 Mar 2024 23:54:15 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 15 Mar 2024 23:54:15 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 15 Mar 2024 23:54:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Mar 2024 23:54:15 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:60aeec3a60ac12f63ba33495ce01db7daf3ed4c138213d85412a7fe01dbbb264`  
		Last Modified: Fri, 01 Dec 2023 02:04:52 GMT  
		Size: 2.8 MB (2832692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2891de9a8cc91a8a551c1844925d89b28b071413e5be681d423f588fad5ac4cc`  
		Last Modified: Fri, 15 Mar 2024 23:55:00 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7130a3d53086b8092a1ba79d08195eb55a6a3b733d170970f769043c9e40ca`  
		Last Modified: Fri, 15 Mar 2024 23:55:08 GMT  
		Size: 48.9 MB (48877071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675e3eb4e5dc3591015124652cddab19fc47d9715bcefb7601ef977e2121d467`  
		Last Modified: Fri, 15 Mar 2024 23:55:00 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef478b84bf141dd58f77f5723e1a4cd30ba3630461c17bc06ed71ef45b3d3914`  
		Last Modified: Fri, 15 Mar 2024 23:55:00 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc6b18ad58b77c58bc9fc504d3fb8677eae2d51c3a70b416d234707ca1592d0`  
		Last Modified: Fri, 15 Mar 2024 23:55:00 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.13.9`

```console
$ docker pull consul@sha256:1e4e3ceec04e972aa9b98944c4461ef202309f12e7fdc2fbef7772fb2d951a33
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.13.9` - linux; amd64

```console
$ docker pull consul@sha256:9301c1d6675ad78b919f25fe64baf9bafd1e7f229077470dc8987b7af2c826ab
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **52.9 MB (52882659 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:709ec67b3e8470fce6dadd63d0df4f392a6c290063365273916f6fe5cd666c80`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:11 GMT
ADD file:aa1af71c6b66d2dddee4797236e3e526f70f904ab641cc0dd6b41445cfedf9b4 in / 
# Thu, 30 Nov 2023 23:23:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:58:18 GMT
ARG CONSUL_VERSION=1.13.9
# Fri, 01 Dec 2023 06:58:18 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 01 Dec 2023 06:58:18 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 01 Dec 2023 06:58:19 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 01 Dec 2023 06:58:24 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 01 Dec 2023 06:58:25 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 01 Dec 2023 06:58:26 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 01 Dec 2023 06:58:26 GMT
VOLUME [/consul/data]
# Fri, 01 Dec 2023 06:58:26 GMT
EXPOSE 8300
# Fri, 01 Dec 2023 06:58:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 01 Dec 2023 06:58:26 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 01 Dec 2023 06:58:26 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 01 Dec 2023 06:58:26 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 06:58:26 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d078792c4f9122259f14b539315bd92cbd9490ed73e08255a08689122b143108`  
		Last Modified: Thu, 30 Nov 2023 23:23:58 GMT  
		Size: 2.8 MB (2826431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1dba966ef6ef17885880841074b2424e1d4b963e78d68081d9dd91431dd2e5e8`  
		Last Modified: Fri, 01 Dec 2023 06:59:05 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ceb4269433525321ab6345f1e321c964018cbcb38f12ab8caf3e157a039e7791`  
		Last Modified: Fri, 01 Dec 2023 06:59:11 GMT  
		Size: 50.1 MB (50052802 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:acf42966a76373a0dc79f025db1d1d1c49e7c5766744160a4a9b7b4600bdd599`  
		Last Modified: Fri, 01 Dec 2023 06:59:05 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e558cb961615344425ddf507970140aa378a120f11c803ab15366aab61ecfdf9`  
		Last Modified: Fri, 01 Dec 2023 06:59:05 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c43f8ee523ea83de5aa3fed946a2427c3ae4dec83012c5084b4613fe2f92240`  
		Last Modified: Fri, 01 Dec 2023 06:59:05 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:316233c00f0333574f2ec88e565340ac850207235aa8148e4e343237ed0148d1
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50380771 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:32f081945c5743156f301bdb751148f53309a8fcb93c6310deb96e9403dc0fa9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:27 GMT
ADD file:2270cb7f14826bc917baa12cd1ff166703f454ccd10ef5799d8106942bb0abe2 in / 
# Thu, 30 Nov 2023 22:49:27 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 01:08:38 GMT
ARG CONSUL_VERSION=1.13.9
# Sat, 16 Mar 2024 01:08:38 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 16 Mar 2024 01:08:38 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 16 Mar 2024 01:08:40 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 16 Mar 2024 01:08:50 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 16 Mar 2024 01:08:52 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 16 Mar 2024 01:08:53 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 16 Mar 2024 01:08:54 GMT
VOLUME [/consul/data]
# Sat, 16 Mar 2024 01:08:54 GMT
EXPOSE 8300
# Sat, 16 Mar 2024 01:08:54 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 16 Mar 2024 01:08:55 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 16 Mar 2024 01:08:55 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 16 Mar 2024 01:08:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 01:08:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:be5e3feadb89f4f40a3bc5997dbddd75fdc3686e938beb9d363990d92db9e4aa`  
		Last Modified: Thu, 30 Nov 2023 22:50:12 GMT  
		Size: 2.6 MB (2633457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dc63b553ef8b8a8119558a8a19c5299b24a04c71905c3dd286dbfcdc650e6de0`  
		Last Modified: Sat, 16 Mar 2024 01:09:45 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:411b14b841cd76176d1ddfecfd87a323ea4000526524892f497de45af508897a`  
		Last Modified: Sat, 16 Mar 2024 01:09:52 GMT  
		Size: 47.7 MB (47743882 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3f34b0384c5b0d619807db46ee3076289f862c5e784e95b8ef2b8dc1e67888d`  
		Last Modified: Sat, 16 Mar 2024 01:09:45 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:af33cc37dae42ccbb65f164efbc8c2ec695150ec90a03d6a67eb036812c4404c`  
		Last Modified: Sat, 16 Mar 2024 01:09:45 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b826096d6992838494a6b10240eebec11a2d25aaef6f72bdc68afc9924a36bee`  
		Last Modified: Sat, 16 Mar 2024 01:09:45 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:f0428c05d4f2e00575577ff371550ebb55b7bbe0a8caf5af44fe21ca40aa90c3
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49911756 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:9339a9151a3e111fcd3dd018e894e5f5fb2149adb322878798595257b6e19b5b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:15 GMT
ADD file:3982c510455cc0ceea8cf8dd0b50b69588e35fd4f84522cb4000582c73781672 in / 
# Thu, 30 Nov 2023 23:11:15 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:05:22 GMT
ARG CONSUL_VERSION=1.13.9
# Sat, 16 Mar 2024 03:05:22 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 16 Mar 2024 03:05:22 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 16 Mar 2024 03:05:22 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 16 Mar 2024 03:05:27 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 16 Mar 2024 03:05:28 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 16 Mar 2024 03:05:28 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:05:28 GMT
VOLUME [/consul/data]
# Sat, 16 Mar 2024 03:05:29 GMT
EXPOSE 8300
# Sat, 16 Mar 2024 03:05:29 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 16 Mar 2024 03:05:29 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 16 Mar 2024 03:05:29 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 16 Mar 2024 03:05:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:05:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8bc1ab4b84041d57f21a792410a00820f73fda7efe08bcd2ca6245349a40299d`  
		Last Modified: Thu, 30 Nov 2023 23:12:02 GMT  
		Size: 2.7 MB (2721527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5f55f41307d72d5098b63dd105f1afeabd9c9941c7e4de2e47f1be62332fe04`  
		Last Modified: Sat, 16 Mar 2024 03:06:05 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e358ee67ea4bf16d6d6c78187847ff04273566579ca912341fd24c749e44160e`  
		Last Modified: Sat, 16 Mar 2024 03:06:09 GMT  
		Size: 47.2 MB (47186797 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:66e99432ab36fea86b13a82cba1fbcc5f830efe9eb67c52dfcd2de16f9b7e01b`  
		Last Modified: Sat, 16 Mar 2024 03:06:05 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e86f570ba77ee453457be7d7cb8a11996e50843a27705847895adfae2816d67d`  
		Last Modified: Sat, 16 Mar 2024 03:06:05 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:df625012f913ece4a4631cef2e6afa54aa168c48505184a1399ad74a8db5bf6d`  
		Last Modified: Sat, 16 Mar 2024 03:06:05 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13.9` - linux; 386

```console
$ docker pull consul@sha256:c003dedb910978aae6e493b06a455ed24c8722f79d818306c6e22f8b108b078e
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51713193 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ff04b94bbb3faeaf546c96dd37c4b4264ca35e05f7a89e54bfdd48a29882d47a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 01 Dec 2023 02:04:00 GMT
ADD file:5990d507b1d1b3a4a63574a2ec1c9e2ca4344d30f7618e002039cd6c9693a56d in / 
# Fri, 01 Dec 2023 02:04:00 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:54:04 GMT
ARG CONSUL_VERSION=1.13.9
# Fri, 15 Mar 2024 23:54:04 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 15 Mar 2024 23:54:04 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 15 Mar 2024 23:54:05 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 15 Mar 2024 23:54:12 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 15 Mar 2024 23:54:13 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 15 Mar 2024 23:54:14 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 15 Mar 2024 23:54:14 GMT
VOLUME [/consul/data]
# Fri, 15 Mar 2024 23:54:14 GMT
EXPOSE 8300
# Fri, 15 Mar 2024 23:54:14 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 15 Mar 2024 23:54:15 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 15 Mar 2024 23:54:15 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 15 Mar 2024 23:54:15 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Mar 2024 23:54:15 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:60aeec3a60ac12f63ba33495ce01db7daf3ed4c138213d85412a7fe01dbbb264`  
		Last Modified: Fri, 01 Dec 2023 02:04:52 GMT  
		Size: 2.8 MB (2832692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2891de9a8cc91a8a551c1844925d89b28b071413e5be681d423f588fad5ac4cc`  
		Last Modified: Fri, 15 Mar 2024 23:55:00 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7c7130a3d53086b8092a1ba79d08195eb55a6a3b733d170970f769043c9e40ca`  
		Last Modified: Fri, 15 Mar 2024 23:55:08 GMT  
		Size: 48.9 MB (48877071 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:675e3eb4e5dc3591015124652cddab19fc47d9715bcefb7601ef977e2121d467`  
		Last Modified: Fri, 15 Mar 2024 23:55:00 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef478b84bf141dd58f77f5723e1a4cd30ba3630461c17bc06ed71ef45b3d3914`  
		Last Modified: Fri, 15 Mar 2024 23:55:00 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8fc6b18ad58b77c58bc9fc504d3fb8677eae2d51c3a70b416d234707ca1592d0`  
		Last Modified: Fri, 15 Mar 2024 23:55:00 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.14`

```console
$ docker pull consul@sha256:d738e65647e831cc67a9d17a3447bcd54be0ed43348a59d9c731c2950985e1d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.14` - linux; amd64

```console
$ docker pull consul@sha256:ec46ce3948c957d2f5b2207f2585e62c611c0caab2db4649cb1fbc851839c96a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56685867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5afc7e812bb8c4c006ca89586c1fb63bb5625a6e711135fc725692f772d02a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:11 GMT
ADD file:aa1af71c6b66d2dddee4797236e3e526f70f904ab641cc0dd6b41445cfedf9b4 in / 
# Thu, 30 Nov 2023 23:23:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:58:06 GMT
ARG CONSUL_VERSION=1.14.8
# Fri, 01 Dec 2023 06:58:06 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 01 Dec 2023 06:58:06 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 01 Dec 2023 06:58:06 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 01 Dec 2023 06:58:12 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 01 Dec 2023 06:58:13 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 01 Dec 2023 06:58:13 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 01 Dec 2023 06:58:13 GMT
VOLUME [/consul/data]
# Fri, 01 Dec 2023 06:58:14 GMT
EXPOSE 8300
# Fri, 01 Dec 2023 06:58:14 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 01 Dec 2023 06:58:14 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 01 Dec 2023 06:58:14 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 01 Dec 2023 06:58:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 06:58:14 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d078792c4f9122259f14b539315bd92cbd9490ed73e08255a08689122b143108`  
		Last Modified: Thu, 30 Nov 2023 23:23:58 GMT  
		Size: 2.8 MB (2826431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9dc77dec6a8df2e152581dd3f225f00f9433c03cb7ea289bb185e4d7d5f9e9`  
		Last Modified: Fri, 01 Dec 2023 06:58:51 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c9d89c24efc045f9c18b7cadd28ceed056cf4b6214a7eb6eb044c30b574c06`  
		Last Modified: Fri, 01 Dec 2023 06:58:57 GMT  
		Size: 53.9 MB (53856009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc87d572254175fbc38bf737251a6bf174a4931604eddbd3251fee8acf77d03`  
		Last Modified: Fri, 01 Dec 2023 06:58:51 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd844c9ec991d487ad230a89c441e5258b515ccbf333ab592ccbe09239a3c662`  
		Last Modified: Fri, 01 Dec 2023 06:58:51 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b6f8cb76599518c782b84d33d2eff5ed96986ff9b2159406d2eda3d69ee21a`  
		Last Modified: Fri, 01 Dec 2023 06:58:51 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14` - linux; arm variant v6

```console
$ docker pull consul@sha256:d0889383378a17431d2871d8d61a9637ad7cc783b3c893548510b3c558916766
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a166d22781cc448fca99909958275f40497871049eae9cc08bd8a82a4149bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:27 GMT
ADD file:2270cb7f14826bc917baa12cd1ff166703f454ccd10ef5799d8106942bb0abe2 in / 
# Thu, 30 Nov 2023 22:49:27 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 01:08:13 GMT
ARG CONSUL_VERSION=1.14.8
# Sat, 16 Mar 2024 01:08:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 16 Mar 2024 01:08:14 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 16 Mar 2024 01:08:16 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 16 Mar 2024 01:08:26 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 16 Mar 2024 01:08:28 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 16 Mar 2024 01:08:30 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 16 Mar 2024 01:08:30 GMT
VOLUME [/consul/data]
# Sat, 16 Mar 2024 01:08:30 GMT
EXPOSE 8300
# Sat, 16 Mar 2024 01:08:31 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 16 Mar 2024 01:08:31 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 16 Mar 2024 01:08:32 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 16 Mar 2024 01:08:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 01:08:33 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:be5e3feadb89f4f40a3bc5997dbddd75fdc3686e938beb9d363990d92db9e4aa`  
		Last Modified: Thu, 30 Nov 2023 22:50:12 GMT  
		Size: 2.6 MB (2633457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe67cc34564e160d5246ea5dba9523e73d66fd42c9ec091f230ed3c61b4469`  
		Last Modified: Sat, 16 Mar 2024 01:09:27 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19168ef7a6092568e76bbf955bf273b4f2b0043b37bcf320e715ef17b549198`  
		Last Modified: Sat, 16 Mar 2024 01:09:36 GMT  
		Size: 51.3 MB (51335678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35e28364913c2e99365ab8f8b3f55f7fc6503854accd97592663f7b2e098dc6`  
		Last Modified: Sat, 16 Mar 2024 01:09:27 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11805c06f3898112e32f3766843e64a614f437e2ed987fddad1ab225db47796c`  
		Last Modified: Sat, 16 Mar 2024 01:09:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b9c73a8d04cf45c2abf29e987db2e867c0ab7117343e648afc493b05a44c28`  
		Last Modified: Sat, 16 Mar 2024 01:09:27 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:8d63c16a00812ee9fb3cc22805d237b21a7243d877f01ad7aee45795a26c9944
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53533752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a4849967f07e5d2d4ea07c66c43be934ddf95197144e97c941d892634c6b17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:15 GMT
ADD file:3982c510455cc0ceea8cf8dd0b50b69588e35fd4f84522cb4000582c73781672 in / 
# Thu, 30 Nov 2023 23:11:15 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:05:12 GMT
ARG CONSUL_VERSION=1.14.8
# Sat, 16 Mar 2024 03:05:12 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 16 Mar 2024 03:05:12 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 16 Mar 2024 03:05:13 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 16 Mar 2024 03:05:18 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 16 Mar 2024 03:05:19 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 16 Mar 2024 03:05:19 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:05:19 GMT
VOLUME [/consul/data]
# Sat, 16 Mar 2024 03:05:19 GMT
EXPOSE 8300
# Sat, 16 Mar 2024 03:05:20 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 16 Mar 2024 03:05:20 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 16 Mar 2024 03:05:20 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 16 Mar 2024 03:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:05:20 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8bc1ab4b84041d57f21a792410a00820f73fda7efe08bcd2ca6245349a40299d`  
		Last Modified: Thu, 30 Nov 2023 23:12:02 GMT  
		Size: 2.7 MB (2721527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e76524077d04cb5cf6be16fb0344ab427d25fcd1e4513b585dd36bb8961f3e1`  
		Last Modified: Sat, 16 Mar 2024 03:05:52 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7c2efb5310e275f57a73bd0d79429962627e1d1aac098ef12beeb909087e99`  
		Last Modified: Sat, 16 Mar 2024 03:05:56 GMT  
		Size: 50.8 MB (50808798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195952423b262908af805bf138dc8961de0afbf1e4f2978fdd0268357b40fb2f`  
		Last Modified: Sat, 16 Mar 2024 03:05:51 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14d949065e6e305352408b29b2f196096476d12f5523d31549fdeba8a28e05c`  
		Last Modified: Sat, 16 Mar 2024 03:05:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048f69cf6c79213b9f009174653cdb6550e6dd6a3b33036f813c52c02c87aa26`  
		Last Modified: Sat, 16 Mar 2024 03:05:51 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14` - linux; 386

```console
$ docker pull consul@sha256:032dcd611695ceffd9caf3e3202e897e5d8285c18bf47fa08efff7aa980e6a33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.4 MB (55372984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca32b4a67c2871af8f3ee0a9142e002135276a533fb948b322aaab1f09774044`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 01 Dec 2023 02:04:00 GMT
ADD file:5990d507b1d1b3a4a63574a2ec1c9e2ca4344d30f7618e002039cd6c9693a56d in / 
# Fri, 01 Dec 2023 02:04:00 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:53:51 GMT
ARG CONSUL_VERSION=1.14.8
# Fri, 15 Mar 2024 23:53:51 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 15 Mar 2024 23:53:51 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 15 Mar 2024 23:53:52 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 15 Mar 2024 23:54:00 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 15 Mar 2024 23:54:01 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 15 Mar 2024 23:54:01 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 15 Mar 2024 23:54:01 GMT
VOLUME [/consul/data]
# Fri, 15 Mar 2024 23:54:02 GMT
EXPOSE 8300
# Fri, 15 Mar 2024 23:54:02 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 15 Mar 2024 23:54:02 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 15 Mar 2024 23:54:02 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 15 Mar 2024 23:54:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Mar 2024 23:54:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:60aeec3a60ac12f63ba33495ce01db7daf3ed4c138213d85412a7fe01dbbb264`  
		Last Modified: Fri, 01 Dec 2023 02:04:52 GMT  
		Size: 2.8 MB (2832692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48730e2cfbf8ad89e9973f43b85071ab9c0053872b5c8605d00469e66985ea12`  
		Last Modified: Fri, 15 Mar 2024 23:54:43 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e377e60aedbaf297801cb90aace8963a6ae2bea252727f3f8dee92e6da70e52`  
		Last Modified: Fri, 15 Mar 2024 23:54:52 GMT  
		Size: 52.5 MB (52536859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2a18dc2586bc674f7c08ffa0509333eba6b951c026e3bbd84a68c1e1e53150`  
		Last Modified: Fri, 15 Mar 2024 23:54:42 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348cf2262caf4805d55cb461339c24d0ef44367cec43dca7bab5046be6864f3f`  
		Last Modified: Fri, 15 Mar 2024 23:54:43 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae77f4efee1d2e14be32874cec3fc4d8dd56964f9bd6d03441974acd09b4d2b6`  
		Last Modified: Fri, 15 Mar 2024 23:54:42 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.14.8`

```console
$ docker pull consul@sha256:d738e65647e831cc67a9d17a3447bcd54be0ed43348a59d9c731c2950985e1d4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.14.8` - linux; amd64

```console
$ docker pull consul@sha256:ec46ce3948c957d2f5b2207f2585e62c611c0caab2db4649cb1fbc851839c96a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.7 MB (56685867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b5afc7e812bb8c4c006ca89586c1fb63bb5625a6e711135fc725692f772d02a2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:11 GMT
ADD file:aa1af71c6b66d2dddee4797236e3e526f70f904ab641cc0dd6b41445cfedf9b4 in / 
# Thu, 30 Nov 2023 23:23:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:58:06 GMT
ARG CONSUL_VERSION=1.14.8
# Fri, 01 Dec 2023 06:58:06 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 01 Dec 2023 06:58:06 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 01 Dec 2023 06:58:06 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 01 Dec 2023 06:58:12 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 01 Dec 2023 06:58:13 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 01 Dec 2023 06:58:13 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 01 Dec 2023 06:58:13 GMT
VOLUME [/consul/data]
# Fri, 01 Dec 2023 06:58:14 GMT
EXPOSE 8300
# Fri, 01 Dec 2023 06:58:14 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 01 Dec 2023 06:58:14 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 01 Dec 2023 06:58:14 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 01 Dec 2023 06:58:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 06:58:14 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d078792c4f9122259f14b539315bd92cbd9490ed73e08255a08689122b143108`  
		Last Modified: Thu, 30 Nov 2023 23:23:58 GMT  
		Size: 2.8 MB (2826431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c9dc77dec6a8df2e152581dd3f225f00f9433c03cb7ea289bb185e4d7d5f9e9`  
		Last Modified: Fri, 01 Dec 2023 06:58:51 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4c9d89c24efc045f9c18b7cadd28ceed056cf4b6214a7eb6eb044c30b574c06`  
		Last Modified: Fri, 01 Dec 2023 06:58:57 GMT  
		Size: 53.9 MB (53856009 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bcc87d572254175fbc38bf737251a6bf174a4931604eddbd3251fee8acf77d03`  
		Last Modified: Fri, 01 Dec 2023 06:58:51 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd844c9ec991d487ad230a89c441e5258b515ccbf333ab592ccbe09239a3c662`  
		Last Modified: Fri, 01 Dec 2023 06:58:51 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:25b6f8cb76599518c782b84d33d2eff5ed96986ff9b2159406d2eda3d69ee21a`  
		Last Modified: Fri, 01 Dec 2023 06:58:51 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14.8` - linux; arm variant v6

```console
$ docker pull consul@sha256:d0889383378a17431d2871d8d61a9637ad7cc783b3c893548510b3c558916766
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53972569 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:18a166d22781cc448fca99909958275f40497871049eae9cc08bd8a82a4149bb`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:27 GMT
ADD file:2270cb7f14826bc917baa12cd1ff166703f454ccd10ef5799d8106942bb0abe2 in / 
# Thu, 30 Nov 2023 22:49:27 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 01:08:13 GMT
ARG CONSUL_VERSION=1.14.8
# Sat, 16 Mar 2024 01:08:14 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 16 Mar 2024 01:08:14 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 16 Mar 2024 01:08:16 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 16 Mar 2024 01:08:26 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 16 Mar 2024 01:08:28 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 16 Mar 2024 01:08:30 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 16 Mar 2024 01:08:30 GMT
VOLUME [/consul/data]
# Sat, 16 Mar 2024 01:08:30 GMT
EXPOSE 8300
# Sat, 16 Mar 2024 01:08:31 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 16 Mar 2024 01:08:31 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 16 Mar 2024 01:08:32 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 16 Mar 2024 01:08:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 01:08:33 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:be5e3feadb89f4f40a3bc5997dbddd75fdc3686e938beb9d363990d92db9e4aa`  
		Last Modified: Thu, 30 Nov 2023 22:50:12 GMT  
		Size: 2.6 MB (2633457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34fe67cc34564e160d5246ea5dba9523e73d66fd42c9ec091f230ed3c61b4469`  
		Last Modified: Sat, 16 Mar 2024 01:09:27 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f19168ef7a6092568e76bbf955bf273b4f2b0043b37bcf320e715ef17b549198`  
		Last Modified: Sat, 16 Mar 2024 01:09:36 GMT  
		Size: 51.3 MB (51335678 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e35e28364913c2e99365ab8f8b3f55f7fc6503854accd97592663f7b2e098dc6`  
		Last Modified: Sat, 16 Mar 2024 01:09:27 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:11805c06f3898112e32f3766843e64a614f437e2ed987fddad1ab225db47796c`  
		Last Modified: Sat, 16 Mar 2024 01:09:27 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:65b9c73a8d04cf45c2abf29e987db2e867c0ab7117343e648afc493b05a44c28`  
		Last Modified: Sat, 16 Mar 2024 01:09:27 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14.8` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:8d63c16a00812ee9fb3cc22805d237b21a7243d877f01ad7aee45795a26c9944
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53533752 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:98a4849967f07e5d2d4ea07c66c43be934ddf95197144e97c941d892634c6b17`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:15 GMT
ADD file:3982c510455cc0ceea8cf8dd0b50b69588e35fd4f84522cb4000582c73781672 in / 
# Thu, 30 Nov 2023 23:11:15 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:05:12 GMT
ARG CONSUL_VERSION=1.14.8
# Sat, 16 Mar 2024 03:05:12 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 16 Mar 2024 03:05:12 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 16 Mar 2024 03:05:13 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 16 Mar 2024 03:05:18 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 16 Mar 2024 03:05:19 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 16 Mar 2024 03:05:19 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:05:19 GMT
VOLUME [/consul/data]
# Sat, 16 Mar 2024 03:05:19 GMT
EXPOSE 8300
# Sat, 16 Mar 2024 03:05:20 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 16 Mar 2024 03:05:20 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 16 Mar 2024 03:05:20 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 16 Mar 2024 03:05:20 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:05:20 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8bc1ab4b84041d57f21a792410a00820f73fda7efe08bcd2ca6245349a40299d`  
		Last Modified: Thu, 30 Nov 2023 23:12:02 GMT  
		Size: 2.7 MB (2721527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0e76524077d04cb5cf6be16fb0344ab427d25fcd1e4513b585dd36bb8961f3e1`  
		Last Modified: Sat, 16 Mar 2024 03:05:52 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d7c2efb5310e275f57a73bd0d79429962627e1d1aac098ef12beeb909087e99`  
		Last Modified: Sat, 16 Mar 2024 03:05:56 GMT  
		Size: 50.8 MB (50808798 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:195952423b262908af805bf138dc8961de0afbf1e4f2978fdd0268357b40fb2f`  
		Last Modified: Sat, 16 Mar 2024 03:05:51 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a14d949065e6e305352408b29b2f196096476d12f5523d31549fdeba8a28e05c`  
		Last Modified: Sat, 16 Mar 2024 03:05:52 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:048f69cf6c79213b9f009174653cdb6550e6dd6a3b33036f813c52c02c87aa26`  
		Last Modified: Sat, 16 Mar 2024 03:05:51 GMT  
		Size: 1.8 KB (1833 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14.8` - linux; 386

```console
$ docker pull consul@sha256:032dcd611695ceffd9caf3e3202e897e5d8285c18bf47fa08efff7aa980e6a33
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.4 MB (55372984 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ca32b4a67c2871af8f3ee0a9142e002135276a533fb948b322aaab1f09774044`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 01 Dec 2023 02:04:00 GMT
ADD file:5990d507b1d1b3a4a63574a2ec1c9e2ca4344d30f7618e002039cd6c9693a56d in / 
# Fri, 01 Dec 2023 02:04:00 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:53:51 GMT
ARG CONSUL_VERSION=1.14.8
# Fri, 15 Mar 2024 23:53:51 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 15 Mar 2024 23:53:51 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 15 Mar 2024 23:53:52 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 15 Mar 2024 23:54:00 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 15 Mar 2024 23:54:01 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 15 Mar 2024 23:54:01 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 15 Mar 2024 23:54:01 GMT
VOLUME [/consul/data]
# Fri, 15 Mar 2024 23:54:02 GMT
EXPOSE 8300
# Fri, 15 Mar 2024 23:54:02 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 15 Mar 2024 23:54:02 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 15 Mar 2024 23:54:02 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 15 Mar 2024 23:54:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Mar 2024 23:54:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:60aeec3a60ac12f63ba33495ce01db7daf3ed4c138213d85412a7fe01dbbb264`  
		Last Modified: Fri, 01 Dec 2023 02:04:52 GMT  
		Size: 2.8 MB (2832692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:48730e2cfbf8ad89e9973f43b85071ab9c0053872b5c8605d00469e66985ea12`  
		Last Modified: Fri, 15 Mar 2024 23:54:43 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7e377e60aedbaf297801cb90aace8963a6ae2bea252727f3f8dee92e6da70e52`  
		Last Modified: Fri, 15 Mar 2024 23:54:52 GMT  
		Size: 52.5 MB (52536859 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef2a18dc2586bc674f7c08ffa0509333eba6b951c026e3bbd84a68c1e1e53150`  
		Last Modified: Fri, 15 Mar 2024 23:54:42 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:348cf2262caf4805d55cb461339c24d0ef44367cec43dca7bab5046be6864f3f`  
		Last Modified: Fri, 15 Mar 2024 23:54:43 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ae77f4efee1d2e14be32874cec3fc4d8dd56964f9bd6d03441974acd09b4d2b6`  
		Last Modified: Fri, 15 Mar 2024 23:54:42 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.15`

```console
$ docker pull consul@sha256:4fc303277179c7eb248efc1b29660265b25019ae33da1db7c65858ced02eb141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.15` - linux; amd64

```console
$ docker pull consul@sha256:940888e9babd9dd18b995cc076782f6592fc6674281b1bdc013a0e4d9864bab7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58889374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3295d4f4567bf587d40182de3d5ff17f9a0007b6f011f5713211308778d859b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:11 GMT
ADD file:aa1af71c6b66d2dddee4797236e3e526f70f904ab641cc0dd6b41445cfedf9b4 in / 
# Thu, 30 Nov 2023 23:23:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:57:54 GMT
ARG CONSUL_VERSION=1.15.4
# Fri, 01 Dec 2023 06:57:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 01 Dec 2023 06:57:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 01 Dec 2023 06:57:54 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 01 Dec 2023 06:58:00 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 01 Dec 2023 06:58:01 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 01 Dec 2023 06:58:02 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 01 Dec 2023 06:58:02 GMT
VOLUME [/consul/data]
# Fri, 01 Dec 2023 06:58:02 GMT
EXPOSE 8300
# Fri, 01 Dec 2023 06:58:02 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 01 Dec 2023 06:58:02 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 01 Dec 2023 06:58:02 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 01 Dec 2023 06:58:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 06:58:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d078792c4f9122259f14b539315bd92cbd9490ed73e08255a08689122b143108`  
		Last Modified: Thu, 30 Nov 2023 23:23:58 GMT  
		Size: 2.8 MB (2826431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cf87e823498406fc599d3318af633c87d42a3837c3f230c775bedd616c7087`  
		Last Modified: Fri, 01 Dec 2023 06:58:36 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2596c56890598336f5af18125cd320d768152603f5649084d7878a5a37be4c07`  
		Last Modified: Fri, 01 Dec 2023 06:58:43 GMT  
		Size: 56.1 MB (56059513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817c0911392619c0a6adc9ade8d7bca389639b43a91926118bc0c16d2a5f7fae`  
		Last Modified: Fri, 01 Dec 2023 06:58:36 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3aba24fc602598a5aa9127c543e92932391c2044b13bf7dddea71a654adb38`  
		Last Modified: Fri, 01 Dec 2023 06:58:36 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e1ec22fe0323d7eb484da677c97b656ef7126b3eb0b5f57890bcf5fdd64cb9`  
		Last Modified: Fri, 01 Dec 2023 06:58:36 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.15` - linux; arm variant v6

```console
$ docker pull consul@sha256:7408db59b935a9bd5424b0ec3d20edd8ea25a479bd08010d2dec90f4bf6d5e94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56042423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2811e45fe44b32d19b7a517a5774120860ef1ed4c9830c93ab0f113b4ff2e4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:27 GMT
ADD file:2270cb7f14826bc917baa12cd1ff166703f454ccd10ef5799d8106942bb0abe2 in / 
# Thu, 30 Nov 2023 22:49:27 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 01:07:44 GMT
ARG CONSUL_VERSION=1.15.4
# Sat, 16 Mar 2024 01:07:45 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 16 Mar 2024 01:07:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 16 Mar 2024 01:07:46 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 16 Mar 2024 01:08:04 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 16 Mar 2024 01:08:06 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 16 Mar 2024 01:08:07 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 16 Mar 2024 01:08:08 GMT
VOLUME [/consul/data]
# Sat, 16 Mar 2024 01:08:08 GMT
EXPOSE 8300
# Sat, 16 Mar 2024 01:08:08 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 16 Mar 2024 01:08:09 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 16 Mar 2024 01:08:09 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 16 Mar 2024 01:08:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 01:08:10 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:be5e3feadb89f4f40a3bc5997dbddd75fdc3686e938beb9d363990d92db9e4aa`  
		Last Modified: Thu, 30 Nov 2023 22:50:12 GMT  
		Size: 2.6 MB (2633457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89c02bd02d33cbd2ed0e56250b3b96124eba8b070ab1694d05293b060469c04`  
		Last Modified: Sat, 16 Mar 2024 01:09:14 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c99bbf378ad5f80163b09a3927843410442d51742f6cc42189db7d6bbe2ac6cd`  
		Last Modified: Sat, 16 Mar 2024 01:09:19 GMT  
		Size: 53.4 MB (53405531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3189ba98252e96f47849371e01d49efeffc2c895a7e120e8de95fc933b0fc2c3`  
		Last Modified: Sat, 16 Mar 2024 01:09:10 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a2d6a9519ec8ae28e1fea232b225a82ac23a582debfb470be6aacbbc93850a`  
		Last Modified: Sat, 16 Mar 2024 01:09:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e91a11c29afc0f554437c86e986de507fbc14c767a02ee21e27ed55a93f76e8`  
		Last Modified: Sat, 16 Mar 2024 01:09:10 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.15` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:8e7755e4814ce8074deccc298ad3ca7563f2bde7febadf4fe2e5e09b62ae2c4a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55626643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04122b09617f6ffabc2e4bb7201ec957d25c4cdc29eb40444f7ab0581c2582c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:15 GMT
ADD file:3982c510455cc0ceea8cf8dd0b50b69588e35fd4f84522cb4000582c73781672 in / 
# Thu, 30 Nov 2023 23:11:15 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:05:01 GMT
ARG CONSUL_VERSION=1.15.4
# Sat, 16 Mar 2024 03:05:01 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 16 Mar 2024 03:05:01 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 16 Mar 2024 03:05:01 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 16 Mar 2024 03:05:07 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 16 Mar 2024 03:05:08 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 16 Mar 2024 03:05:08 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:05:09 GMT
VOLUME [/consul/data]
# Sat, 16 Mar 2024 03:05:09 GMT
EXPOSE 8300
# Sat, 16 Mar 2024 03:05:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 16 Mar 2024 03:05:09 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 16 Mar 2024 03:05:09 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 16 Mar 2024 03:05:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:05:09 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8bc1ab4b84041d57f21a792410a00820f73fda7efe08bcd2ca6245349a40299d`  
		Last Modified: Thu, 30 Nov 2023 23:12:02 GMT  
		Size: 2.7 MB (2721527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de41e283e5ecff9ba4f165155c9b98d8905304ba751145036b182c449e099d99`  
		Last Modified: Sat, 16 Mar 2024 03:05:39 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50782d78352e02b5e677358dee3ceae5eb33545452dbba4479798982ad1cc72c`  
		Last Modified: Sat, 16 Mar 2024 03:05:43 GMT  
		Size: 52.9 MB (52901686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1deaf4d5968c84ef7f1502ae21fced2344b486f006302cd3e71c24eb9f699565`  
		Last Modified: Sat, 16 Mar 2024 03:05:39 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34970a0f658bd98fa7713ffcead96df6292a1a72e975a9e5e59f59603a6f17a`  
		Last Modified: Sat, 16 Mar 2024 03:05:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1d4a65bcff321704b8a127551f4ab437068cfb7a91f8e4661d8d76d896cc32`  
		Last Modified: Sat, 16 Mar 2024 03:05:39 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.15` - linux; 386

```console
$ docker pull consul@sha256:e66cd4374779cd09203900689a00360eb139f3cef25bf941db9a330a35fdc9de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57454346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c976c298affbed37806d51f477dc72c9fe7b4bbbb54dbe9295d7299d3ca9853`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 01 Dec 2023 02:04:00 GMT
ADD file:5990d507b1d1b3a4a63574a2ec1c9e2ca4344d30f7618e002039cd6c9693a56d in / 
# Fri, 01 Dec 2023 02:04:00 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:53:27 GMT
ARG CONSUL_VERSION=1.15.4
# Fri, 15 Mar 2024 23:53:27 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 15 Mar 2024 23:53:27 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 15 Mar 2024 23:53:28 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 15 Mar 2024 23:53:45 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 15 Mar 2024 23:53:46 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 15 Mar 2024 23:53:46 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 15 Mar 2024 23:53:46 GMT
VOLUME [/consul/data]
# Fri, 15 Mar 2024 23:53:47 GMT
EXPOSE 8300
# Fri, 15 Mar 2024 23:53:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 15 Mar 2024 23:53:47 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 15 Mar 2024 23:53:47 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 15 Mar 2024 23:53:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Mar 2024 23:53:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:60aeec3a60ac12f63ba33495ce01db7daf3ed4c138213d85412a7fe01dbbb264`  
		Last Modified: Fri, 01 Dec 2023 02:04:52 GMT  
		Size: 2.8 MB (2832692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4576af8d5b8bb561453a33e951182b689e97b286d55ffef3244d2aa3f52e145f`  
		Last Modified: Fri, 15 Mar 2024 23:54:26 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23bba49a6f66e02f21c40a965cb085bb0a8fc9b4cca51bcccf5b879c362f006`  
		Last Modified: Fri, 15 Mar 2024 23:54:34 GMT  
		Size: 54.6 MB (54618221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f954583f15f8af79fae876c5ead32018043ee2274b30276a621a000e67340bfa`  
		Last Modified: Fri, 15 Mar 2024 23:54:26 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5dc6939fa00fc35ae5492bfe0c7a83f742f4e46de217ff7cfd9fb048a4597c`  
		Last Modified: Fri, 15 Mar 2024 23:54:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fade2a559de65d923512a96e7c961ec9aeab79f11e4d1aa25b1e18e3d09cf021`  
		Last Modified: Fri, 15 Mar 2024 23:54:25 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.15.4`

```console
$ docker pull consul@sha256:4fc303277179c7eb248efc1b29660265b25019ae33da1db7c65858ced02eb141
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.15.4` - linux; amd64

```console
$ docker pull consul@sha256:940888e9babd9dd18b995cc076782f6592fc6674281b1bdc013a0e4d9864bab7
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **58.9 MB (58889374 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:3295d4f4567bf587d40182de3d5ff17f9a0007b6f011f5713211308778d859b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 23:23:11 GMT
ADD file:aa1af71c6b66d2dddee4797236e3e526f70f904ab641cc0dd6b41445cfedf9b4 in / 
# Thu, 30 Nov 2023 23:23:11 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 06:57:54 GMT
ARG CONSUL_VERSION=1.15.4
# Fri, 01 Dec 2023 06:57:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 01 Dec 2023 06:57:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 01 Dec 2023 06:57:54 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 01 Dec 2023 06:58:00 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 01 Dec 2023 06:58:01 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 01 Dec 2023 06:58:02 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 01 Dec 2023 06:58:02 GMT
VOLUME [/consul/data]
# Fri, 01 Dec 2023 06:58:02 GMT
EXPOSE 8300
# Fri, 01 Dec 2023 06:58:02 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 01 Dec 2023 06:58:02 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 01 Dec 2023 06:58:02 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 01 Dec 2023 06:58:02 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 06:58:02 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:d078792c4f9122259f14b539315bd92cbd9490ed73e08255a08689122b143108`  
		Last Modified: Thu, 30 Nov 2023 23:23:58 GMT  
		Size: 2.8 MB (2826431 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b2cf87e823498406fc599d3318af633c87d42a3837c3f230c775bedd616c7087`  
		Last Modified: Fri, 01 Dec 2023 06:58:36 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2596c56890598336f5af18125cd320d768152603f5649084d7878a5a37be4c07`  
		Last Modified: Fri, 01 Dec 2023 06:58:43 GMT  
		Size: 56.1 MB (56059513 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:817c0911392619c0a6adc9ade8d7bca389639b43a91926118bc0c16d2a5f7fae`  
		Last Modified: Fri, 01 Dec 2023 06:58:36 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5c3aba24fc602598a5aa9127c543e92932391c2044b13bf7dddea71a654adb38`  
		Last Modified: Fri, 01 Dec 2023 06:58:36 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:89e1ec22fe0323d7eb484da677c97b656ef7126b3eb0b5f57890bcf5fdd64cb9`  
		Last Modified: Fri, 01 Dec 2023 06:58:36 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.15.4` - linux; arm variant v6

```console
$ docker pull consul@sha256:7408db59b935a9bd5424b0ec3d20edd8ea25a479bd08010d2dec90f4bf6d5e94
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56042423 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a2811e45fe44b32d19b7a517a5774120860ef1ed4c9830c93ab0f113b4ff2e4c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:27 GMT
ADD file:2270cb7f14826bc917baa12cd1ff166703f454ccd10ef5799d8106942bb0abe2 in / 
# Thu, 30 Nov 2023 22:49:27 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 01:07:44 GMT
ARG CONSUL_VERSION=1.15.4
# Sat, 16 Mar 2024 01:07:45 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 16 Mar 2024 01:07:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 16 Mar 2024 01:07:46 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 16 Mar 2024 01:08:04 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 16 Mar 2024 01:08:06 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 16 Mar 2024 01:08:07 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 16 Mar 2024 01:08:08 GMT
VOLUME [/consul/data]
# Sat, 16 Mar 2024 01:08:08 GMT
EXPOSE 8300
# Sat, 16 Mar 2024 01:08:08 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 16 Mar 2024 01:08:09 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 16 Mar 2024 01:08:09 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 16 Mar 2024 01:08:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 01:08:10 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:be5e3feadb89f4f40a3bc5997dbddd75fdc3686e938beb9d363990d92db9e4aa`  
		Last Modified: Thu, 30 Nov 2023 22:50:12 GMT  
		Size: 2.6 MB (2633457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e89c02bd02d33cbd2ed0e56250b3b96124eba8b070ab1694d05293b060469c04`  
		Last Modified: Sat, 16 Mar 2024 01:09:14 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c99bbf378ad5f80163b09a3927843410442d51742f6cc42189db7d6bbe2ac6cd`  
		Last Modified: Sat, 16 Mar 2024 01:09:19 GMT  
		Size: 53.4 MB (53405531 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3189ba98252e96f47849371e01d49efeffc2c895a7e120e8de95fc933b0fc2c3`  
		Last Modified: Sat, 16 Mar 2024 01:09:10 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:68a2d6a9519ec8ae28e1fea232b225a82ac23a582debfb470be6aacbbc93850a`  
		Last Modified: Sat, 16 Mar 2024 01:09:10 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4e91a11c29afc0f554437c86e986de507fbc14c767a02ee21e27ed55a93f76e8`  
		Last Modified: Sat, 16 Mar 2024 01:09:10 GMT  
		Size: 1.8 KB (1836 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.15.4` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:8e7755e4814ce8074deccc298ad3ca7563f2bde7febadf4fe2e5e09b62ae2c4a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55626643 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:c04122b09617f6ffabc2e4bb7201ec957d25c4cdc29eb40444f7ab0581c2582c`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 23:11:15 GMT
ADD file:3982c510455cc0ceea8cf8dd0b50b69588e35fd4f84522cb4000582c73781672 in / 
# Thu, 30 Nov 2023 23:11:15 GMT
CMD ["/bin/sh"]
# Sat, 16 Mar 2024 03:05:01 GMT
ARG CONSUL_VERSION=1.15.4
# Sat, 16 Mar 2024 03:05:01 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Sat, 16 Mar 2024 03:05:01 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Sat, 16 Mar 2024 03:05:01 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN addgroup consul &&     adduser -S -G consul consul
# Sat, 16 Mar 2024 03:05:07 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Sat, 16 Mar 2024 03:05:08 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Sat, 16 Mar 2024 03:05:08 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Sat, 16 Mar 2024 03:05:09 GMT
VOLUME [/consul/data]
# Sat, 16 Mar 2024 03:05:09 GMT
EXPOSE 8300
# Sat, 16 Mar 2024 03:05:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Sat, 16 Mar 2024 03:05:09 GMT
EXPOSE 8500 8600 8600/udp
# Sat, 16 Mar 2024 03:05:09 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Sat, 16 Mar 2024 03:05:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Sat, 16 Mar 2024 03:05:09 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:8bc1ab4b84041d57f21a792410a00820f73fda7efe08bcd2ca6245349a40299d`  
		Last Modified: Thu, 30 Nov 2023 23:12:02 GMT  
		Size: 2.7 MB (2721527 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:de41e283e5ecff9ba4f165155c9b98d8905304ba751145036b182c449e099d99`  
		Last Modified: Sat, 16 Mar 2024 03:05:39 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50782d78352e02b5e677358dee3ceae5eb33545452dbba4479798982ad1cc72c`  
		Last Modified: Sat, 16 Mar 2024 03:05:43 GMT  
		Size: 52.9 MB (52901686 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1deaf4d5968c84ef7f1502ae21fced2344b486f006302cd3e71c24eb9f699565`  
		Last Modified: Sat, 16 Mar 2024 03:05:39 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a34970a0f658bd98fa7713ffcead96df6292a1a72e975a9e5e59f59603a6f17a`  
		Last Modified: Sat, 16 Mar 2024 03:05:39 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6e1d4a65bcff321704b8a127551f4ab437068cfb7a91f8e4661d8d76d896cc32`  
		Last Modified: Sat, 16 Mar 2024 03:05:39 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.15.4` - linux; 386

```console
$ docker pull consul@sha256:e66cd4374779cd09203900689a00360eb139f3cef25bf941db9a330a35fdc9de
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.5 MB (57454346 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8c976c298affbed37806d51f477dc72c9fe7b4bbbb54dbe9295d7299d3ca9853`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Fri, 01 Dec 2023 02:04:00 GMT
ADD file:5990d507b1d1b3a4a63574a2ec1c9e2ca4344d30f7618e002039cd6c9693a56d in / 
# Fri, 01 Dec 2023 02:04:00 GMT
CMD ["/bin/sh"]
# Fri, 15 Mar 2024 23:53:27 GMT
ARG CONSUL_VERSION=1.15.4
# Fri, 15 Mar 2024 23:53:27 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 15 Mar 2024 23:53:27 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 15 Mar 2024 23:53:28 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 15 Mar 2024 23:53:45 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 15 Mar 2024 23:53:46 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 15 Mar 2024 23:53:46 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 15 Mar 2024 23:53:46 GMT
VOLUME [/consul/data]
# Fri, 15 Mar 2024 23:53:47 GMT
EXPOSE 8300
# Fri, 15 Mar 2024 23:53:47 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 15 Mar 2024 23:53:47 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 15 Mar 2024 23:53:47 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 15 Mar 2024 23:53:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 15 Mar 2024 23:53:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:60aeec3a60ac12f63ba33495ce01db7daf3ed4c138213d85412a7fe01dbbb264`  
		Last Modified: Fri, 01 Dec 2023 02:04:52 GMT  
		Size: 2.8 MB (2832692 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4576af8d5b8bb561453a33e951182b689e97b286d55ffef3244d2aa3f52e145f`  
		Last Modified: Fri, 15 Mar 2024 23:54:26 GMT  
		Size: 1.3 KB (1269 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d23bba49a6f66e02f21c40a965cb085bb0a8fc9b4cca51bcccf5b879c362f006`  
		Last Modified: Fri, 15 Mar 2024 23:54:34 GMT  
		Size: 54.6 MB (54618221 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f954583f15f8af79fae876c5ead32018043ee2274b30276a621a000e67340bfa`  
		Last Modified: Fri, 15 Mar 2024 23:54:26 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa5dc6939fa00fc35ae5492bfe0c7a83f742f4e46de217ff7cfd9fb048a4597c`  
		Last Modified: Fri, 15 Mar 2024 23:54:26 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fade2a559de65d923512a96e7c961ec9aeab79f11e4d1aa25b1e18e3d09cf021`  
		Last Modified: Fri, 15 Mar 2024 23:54:25 GMT  
		Size: 1.8 KB (1837 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
