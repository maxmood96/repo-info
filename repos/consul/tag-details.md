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
$ docker pull consul@sha256:6fed7792aa772b529b911cadee28d5f34cf198aa1dd13fed10abee0330309305
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
$ docker pull consul@sha256:cc96be97523232f563ebd8f62784479b2cacc3e42e54b5eea2e2ce0c9cfea248
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50377710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92742e30c543590118e401e25c4e998ae8c08030f768e12afeb42a866b6bf674`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:27 GMT
ADD file:2270cb7f14826bc917baa12cd1ff166703f454ccd10ef5799d8106942bb0abe2 in / 
# Thu, 30 Nov 2023 22:49:27 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:40:23 GMT
ARG CONSUL_VERSION=1.13.9
# Fri, 01 Dec 2023 00:40:23 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 01 Dec 2023 00:40:23 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 01 Dec 2023 00:40:24 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 01 Dec 2023 00:40:31 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 01 Dec 2023 00:40:31 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 01 Dec 2023 00:40:32 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 01 Dec 2023 00:40:32 GMT
VOLUME [/consul/data]
# Fri, 01 Dec 2023 00:40:32 GMT
EXPOSE 8300
# Fri, 01 Dec 2023 00:40:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 01 Dec 2023 00:40:32 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 01 Dec 2023 00:40:33 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 01 Dec 2023 00:40:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 00:40:33 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:be5e3feadb89f4f40a3bc5997dbddd75fdc3686e938beb9d363990d92db9e4aa`  
		Last Modified: Thu, 30 Nov 2023 22:50:12 GMT  
		Size: 2.6 MB (2633457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bc0edbd1e182fbcd9ea30fad85b7f3786a79345d565bfeccd56d563874dd58`  
		Last Modified: Fri, 01 Dec 2023 00:41:13 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae2fce0d59eff6cd1cd1544a9a914a709b695ab4bab10281b3963ce04631567`  
		Last Modified: Fri, 01 Dec 2023 00:41:20 GMT  
		Size: 47.7 MB (47740824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0386f84aa02d2daded9b41617f87ff22bcdbfd0e95ac9444a24ee8b6536d809f`  
		Last Modified: Fri, 01 Dec 2023 00:41:13 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2b009c6cf99873e81cb7299999a3af6578163db8da9dd297ced89771fc052a`  
		Last Modified: Fri, 01 Dec 2023 00:41:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0990c4b1b335414767bf2f4235e2aaa69ded5764dda375c98073115424f874`  
		Last Modified: Fri, 01 Dec 2023 00:41:13 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:9ca4db9be917c4628cf40e1cbcc2c82e585adbc1f61e74549e7a01e4ae2ae60a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49887900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38653cafba99cd59468e4289b19d753083ecca1d69a3378105554224b24736d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:29 GMT
ADD file:21f240e1e33b25dacee7291cdd8c7750995aa0f460d13496a08c4a2dd92323aa in / 
# Mon, 07 Aug 2023 19:39:29 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:18:00 GMT
ARG CONSUL_VERSION=1.13.9
# Mon, 07 Aug 2023 20:18:00 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Mon, 07 Aug 2023 20:18:00 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Mon, 07 Aug 2023 20:18:00 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN addgroup consul &&     adduser -S -G consul consul
# Mon, 07 Aug 2023 20:18:05 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Mon, 07 Aug 2023 20:18:05 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Mon, 07 Aug 2023 20:18:06 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 07 Aug 2023 20:18:06 GMT
VOLUME [/consul/data]
# Mon, 07 Aug 2023 20:18:06 GMT
EXPOSE 8300
# Mon, 07 Aug 2023 20:18:06 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Mon, 07 Aug 2023 20:18:06 GMT
EXPOSE 8500 8600 8600/udp
# Mon, 07 Aug 2023 20:18:06 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 07 Aug 2023 20:18:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 20:18:06 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ad3fa0ea069c04e4ee9be58cf0ae9e1a8a56f649b96a96298203b055e8c903ff`  
		Last Modified: Mon, 07 Aug 2023 19:40:16 GMT  
		Size: 2.7 MB (2720868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb692b9b206a6ea95e8c37d1de8d9f17283f4b82f0c084ab8052cb98e816c93`  
		Last Modified: Mon, 07 Aug 2023 20:18:45 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ee12e9352466ac63c42cda1c6f4c7c8de1a679bbd57e34e20a221a0bd4a5b8`  
		Last Modified: Mon, 07 Aug 2023 20:18:49 GMT  
		Size: 47.2 MB (47163603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63007ef03380bac6eb13b1d2f459c11a8a1678376b9e27602c49bf734eff4ef4`  
		Last Modified: Mon, 07 Aug 2023 20:18:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8386e27ddec81ad51a8d6de08a8a4c05dc34286584e52ad98c9c6e801551bc6d`  
		Last Modified: Mon, 07 Aug 2023 20:18:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db323a2b82c590e46937f6eac35b8e4c2adb2651d9427a3b1b81b671405f51e`  
		Last Modified: Mon, 07 Aug 2023 20:18:45 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13` - linux; 386

```console
$ docker pull consul@sha256:e6b605eb4ae59542c8331da9aaa1cce4e5f6ca3eb0c5b423a1d0c84ac1869668
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51689196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b73685b17d7d2000a7ca9994d1ef93b8be7f8d891fdc57c53f16ec92abce118a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:38 GMT
ADD file:2d8ac62dd229ef26536f5a9af9e61df30ea68d609fa969786dfd531aea18cf3c in / 
# Mon, 07 Aug 2023 19:38:38 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:28:55 GMT
ARG CONSUL_VERSION=1.13.9
# Mon, 07 Aug 2023 20:28:55 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Mon, 07 Aug 2023 20:28:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Mon, 07 Aug 2023 20:28:56 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN addgroup consul &&     adduser -S -G consul consul
# Mon, 07 Aug 2023 20:29:03 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Mon, 07 Aug 2023 20:29:04 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Mon, 07 Aug 2023 20:29:04 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 07 Aug 2023 20:29:05 GMT
VOLUME [/consul/data]
# Mon, 07 Aug 2023 20:29:05 GMT
EXPOSE 8300
# Mon, 07 Aug 2023 20:29:05 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Mon, 07 Aug 2023 20:29:05 GMT
EXPOSE 8500 8600 8600/udp
# Mon, 07 Aug 2023 20:29:05 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 07 Aug 2023 20:29:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 20:29:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:add53095769493cde9110fd91f113357e53b9e0d94abf216b811fcf00107674e`  
		Last Modified: Mon, 07 Aug 2023 19:39:29 GMT  
		Size: 2.8 MB (2832316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf61741b49cf223bba31911b7abee7b595c89d879db6ba07d9347e40c481ea88`  
		Last Modified: Mon, 07 Aug 2023 20:29:51 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c017cefef559895a7b360f6e5e54fc0d91ac29dfbe0239928d92b55b279c0d9`  
		Last Modified: Mon, 07 Aug 2023 20:29:59 GMT  
		Size: 48.9 MB (48853453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b7110fa29053f56b9575b4b2aa882d8fb03e07f1f3cce20f585cd3e8798006`  
		Last Modified: Mon, 07 Aug 2023 20:29:51 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5ec2f78201a40a548d9ebe371908950e0770bf9e12ff06c6ceb9b1e17bca3c`  
		Last Modified: Mon, 07 Aug 2023 20:29:35 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52acf8afc3bfc715e98b38b8e3cce9e83efd9f0fb22356b3ce96926e2a21605`  
		Last Modified: Mon, 07 Aug 2023 20:29:51 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.13.9`

```console
$ docker pull consul@sha256:6fed7792aa772b529b911cadee28d5f34cf198aa1dd13fed10abee0330309305
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
$ docker pull consul@sha256:cc96be97523232f563ebd8f62784479b2cacc3e42e54b5eea2e2ce0c9cfea248
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **50.4 MB (50377710 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:92742e30c543590118e401e25c4e998ae8c08030f768e12afeb42a866b6bf674`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:27 GMT
ADD file:2270cb7f14826bc917baa12cd1ff166703f454ccd10ef5799d8106942bb0abe2 in / 
# Thu, 30 Nov 2023 22:49:27 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:40:23 GMT
ARG CONSUL_VERSION=1.13.9
# Fri, 01 Dec 2023 00:40:23 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 01 Dec 2023 00:40:23 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 01 Dec 2023 00:40:24 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 01 Dec 2023 00:40:31 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 01 Dec 2023 00:40:31 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 01 Dec 2023 00:40:32 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 01 Dec 2023 00:40:32 GMT
VOLUME [/consul/data]
# Fri, 01 Dec 2023 00:40:32 GMT
EXPOSE 8300
# Fri, 01 Dec 2023 00:40:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 01 Dec 2023 00:40:32 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 01 Dec 2023 00:40:33 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 01 Dec 2023 00:40:33 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 00:40:33 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:be5e3feadb89f4f40a3bc5997dbddd75fdc3686e938beb9d363990d92db9e4aa`  
		Last Modified: Thu, 30 Nov 2023 22:50:12 GMT  
		Size: 2.6 MB (2633457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:00bc0edbd1e182fbcd9ea30fad85b7f3786a79345d565bfeccd56d563874dd58`  
		Last Modified: Fri, 01 Dec 2023 00:41:13 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4ae2fce0d59eff6cd1cd1544a9a914a709b695ab4bab10281b3963ce04631567`  
		Last Modified: Fri, 01 Dec 2023 00:41:20 GMT  
		Size: 47.7 MB (47740824 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0386f84aa02d2daded9b41617f87ff22bcdbfd0e95ac9444a24ee8b6536d809f`  
		Last Modified: Fri, 01 Dec 2023 00:41:13 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ab2b009c6cf99873e81cb7299999a3af6578163db8da9dd297ced89771fc052a`  
		Last Modified: Fri, 01 Dec 2023 00:41:12 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4c0990c4b1b335414767bf2f4235e2aaa69ded5764dda375c98073115424f874`  
		Last Modified: Fri, 01 Dec 2023 00:41:13 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:9ca4db9be917c4628cf40e1cbcc2c82e585adbc1f61e74549e7a01e4ae2ae60a
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **49.9 MB (49887900 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f38653cafba99cd59468e4289b19d753083ecca1d69a3378105554224b24736d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:29 GMT
ADD file:21f240e1e33b25dacee7291cdd8c7750995aa0f460d13496a08c4a2dd92323aa in / 
# Mon, 07 Aug 2023 19:39:29 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:18:00 GMT
ARG CONSUL_VERSION=1.13.9
# Mon, 07 Aug 2023 20:18:00 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Mon, 07 Aug 2023 20:18:00 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Mon, 07 Aug 2023 20:18:00 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN addgroup consul &&     adduser -S -G consul consul
# Mon, 07 Aug 2023 20:18:05 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Mon, 07 Aug 2023 20:18:05 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Mon, 07 Aug 2023 20:18:06 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 07 Aug 2023 20:18:06 GMT
VOLUME [/consul/data]
# Mon, 07 Aug 2023 20:18:06 GMT
EXPOSE 8300
# Mon, 07 Aug 2023 20:18:06 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Mon, 07 Aug 2023 20:18:06 GMT
EXPOSE 8500 8600 8600/udp
# Mon, 07 Aug 2023 20:18:06 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 07 Aug 2023 20:18:06 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 20:18:06 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ad3fa0ea069c04e4ee9be58cf0ae9e1a8a56f649b96a96298203b055e8c903ff`  
		Last Modified: Mon, 07 Aug 2023 19:40:16 GMT  
		Size: 2.7 MB (2720868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0eb692b9b206a6ea95e8c37d1de8d9f17283f4b82f0c084ab8052cb98e816c93`  
		Last Modified: Mon, 07 Aug 2023 20:18:45 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:96ee12e9352466ac63c42cda1c6f4c7c8de1a679bbd57e34e20a221a0bd4a5b8`  
		Last Modified: Mon, 07 Aug 2023 20:18:49 GMT  
		Size: 47.2 MB (47163603 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:63007ef03380bac6eb13b1d2f459c11a8a1678376b9e27602c49bf734eff4ef4`  
		Last Modified: Mon, 07 Aug 2023 20:18:44 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8386e27ddec81ad51a8d6de08a8a4c05dc34286584e52ad98c9c6e801551bc6d`  
		Last Modified: Mon, 07 Aug 2023 20:18:44 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4db323a2b82c590e46937f6eac35b8e4c2adb2651d9427a3b1b81b671405f51e`  
		Last Modified: Mon, 07 Aug 2023 20:18:45 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.13.9` - linux; 386

```console
$ docker pull consul@sha256:e6b605eb4ae59542c8331da9aaa1cce4e5f6ca3eb0c5b423a1d0c84ac1869668
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **51.7 MB (51689196 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b73685b17d7d2000a7ca9994d1ef93b8be7f8d891fdc57c53f16ec92abce118a`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:38 GMT
ADD file:2d8ac62dd229ef26536f5a9af9e61df30ea68d609fa969786dfd531aea18cf3c in / 
# Mon, 07 Aug 2023 19:38:38 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:28:55 GMT
ARG CONSUL_VERSION=1.13.9
# Mon, 07 Aug 2023 20:28:55 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.13.9 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Mon, 07 Aug 2023 20:28:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Mon, 07 Aug 2023 20:28:56 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN addgroup consul &&     adduser -S -G consul consul
# Mon, 07 Aug 2023 20:29:03 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Mon, 07 Aug 2023 20:29:04 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Mon, 07 Aug 2023 20:29:04 GMT
# ARGS: CONSUL_VERSION=1.13.9
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 07 Aug 2023 20:29:05 GMT
VOLUME [/consul/data]
# Mon, 07 Aug 2023 20:29:05 GMT
EXPOSE 8300
# Mon, 07 Aug 2023 20:29:05 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Mon, 07 Aug 2023 20:29:05 GMT
EXPOSE 8500 8600 8600/udp
# Mon, 07 Aug 2023 20:29:05 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 07 Aug 2023 20:29:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 20:29:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:add53095769493cde9110fd91f113357e53b9e0d94abf216b811fcf00107674e`  
		Last Modified: Mon, 07 Aug 2023 19:39:29 GMT  
		Size: 2.8 MB (2832316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cf61741b49cf223bba31911b7abee7b595c89d879db6ba07d9347e40c481ea88`  
		Last Modified: Mon, 07 Aug 2023 20:29:51 GMT  
		Size: 1.3 KB (1265 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0c017cefef559895a7b360f6e5e54fc0d91ac29dfbe0239928d92b55b279c0d9`  
		Last Modified: Mon, 07 Aug 2023 20:29:59 GMT  
		Size: 48.9 MB (48853453 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3b7110fa29053f56b9575b4b2aa882d8fb03e07f1f3cce20f585cd3e8798006`  
		Last Modified: Mon, 07 Aug 2023 20:29:51 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fd5ec2f78201a40a548d9ebe371908950e0770bf9e12ff06c6ceb9b1e17bca3c`  
		Last Modified: Mon, 07 Aug 2023 20:29:35 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d52acf8afc3bfc715e98b38b8e3cce9e83efd9f0fb22356b3ce96926e2a21605`  
		Last Modified: Mon, 07 Aug 2023 20:29:51 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.14`

```console
$ docker pull consul@sha256:61db114a8f84f01c21d6866818d6821ed8ba2efcf7f5550f7a6117a960982a9e
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
$ docker pull consul@sha256:590b5fb1bc18da7b0b63a02736f77737fb5fb662ace6fe12a48f0eea881132d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53968867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cf5527024cec9d6f492824b435f81fc74a4f5dc78ed213257751f464c99490`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:27 GMT
ADD file:2270cb7f14826bc917baa12cd1ff166703f454ccd10ef5799d8106942bb0abe2 in / 
# Thu, 30 Nov 2023 22:49:27 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:40:09 GMT
ARG CONSUL_VERSION=1.14.8
# Fri, 01 Dec 2023 00:40:09 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 01 Dec 2023 00:40:09 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 01 Dec 2023 00:40:10 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 01 Dec 2023 00:40:17 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 01 Dec 2023 00:40:18 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 01 Dec 2023 00:40:19 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 01 Dec 2023 00:40:19 GMT
VOLUME [/consul/data]
# Fri, 01 Dec 2023 00:40:19 GMT
EXPOSE 8300
# Fri, 01 Dec 2023 00:40:20 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 01 Dec 2023 00:40:20 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 01 Dec 2023 00:40:20 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 01 Dec 2023 00:40:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 00:40:21 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:be5e3feadb89f4f40a3bc5997dbddd75fdc3686e938beb9d363990d92db9e4aa`  
		Last Modified: Thu, 30 Nov 2023 22:50:12 GMT  
		Size: 2.6 MB (2633457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4207d01db70f83377abba935e54c2901408dbf281cfd7c75e3c5343cf5ee3428`  
		Last Modified: Fri, 01 Dec 2023 00:40:58 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891dc74a60db0d9de345ad57de44561e3aa71022ffb0a3b1c3c36988babc12a8`  
		Last Modified: Fri, 01 Dec 2023 00:41:04 GMT  
		Size: 51.3 MB (51331980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ef4227ccde8475b88177027bebdeb3af168faf9cc9b69165ce62979d9b9879`  
		Last Modified: Fri, 01 Dec 2023 00:40:58 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23b7910b33036343336c61f6edeb6556a6f0b09f7a31f6bb006954da0e41ecc`  
		Last Modified: Fri, 01 Dec 2023 00:40:58 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4160e9bd2d0889f8b9ac21a662500f482571708ab7c54b89a94cb36546af9a`  
		Last Modified: Fri, 01 Dec 2023 00:40:58 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:bac6fe85dea2d81b469c702904a2d789d69cd4904b4b84fc1d077a00ef9a6129
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53510951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852f1ca2417bd4b123073cd6bcf571b97b784f0ae898fb11d0303dd3732aff77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:29 GMT
ADD file:21f240e1e33b25dacee7291cdd8c7750995aa0f460d13496a08c4a2dd92323aa in / 
# Mon, 07 Aug 2023 19:39:29 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:17:50 GMT
ARG CONSUL_VERSION=1.14.8
# Mon, 07 Aug 2023 20:17:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Mon, 07 Aug 2023 20:17:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Mon, 07 Aug 2023 20:17:51 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN addgroup consul &&     adduser -S -G consul consul
# Mon, 07 Aug 2023 20:17:55 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Mon, 07 Aug 2023 20:17:56 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Mon, 07 Aug 2023 20:17:57 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 07 Aug 2023 20:17:57 GMT
VOLUME [/consul/data]
# Mon, 07 Aug 2023 20:17:57 GMT
EXPOSE 8300
# Mon, 07 Aug 2023 20:17:57 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Mon, 07 Aug 2023 20:17:57 GMT
EXPOSE 8500 8600 8600/udp
# Mon, 07 Aug 2023 20:17:57 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 07 Aug 2023 20:17:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 20:17:57 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ad3fa0ea069c04e4ee9be58cf0ae9e1a8a56f649b96a96298203b055e8c903ff`  
		Last Modified: Mon, 07 Aug 2023 19:40:16 GMT  
		Size: 2.7 MB (2720868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c69d01bb5e779a77b1b6be7b11e6e14b19aec1533dd63b5a65314f5b7691b6`  
		Last Modified: Mon, 07 Aug 2023 20:18:30 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce7aa33142a39195c54d295911e177b3707ef5a63ec8c4b0fcc455b1916da8f`  
		Last Modified: Mon, 07 Aug 2023 20:18:36 GMT  
		Size: 50.8 MB (50786658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4643c57e719dc24d07a83851939342452e1d28a3fe40f3a31521ee8debe52a4d`  
		Last Modified: Mon, 07 Aug 2023 20:18:31 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d856ab6a6f6a21e865284b96c4b2d2ea071950e50ff571b947c372c59e2153`  
		Last Modified: Mon, 07 Aug 2023 20:18:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e707499da1a15cf701449b919d58d13e3b02bea4d145c28b6506c33fe6630724`  
		Last Modified: Mon, 07 Aug 2023 20:18:30 GMT  
		Size: 1.8 KB (1830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14` - linux; 386

```console
$ docker pull consul@sha256:6c0dc4878c036e40a8f34b0a8de41de8d9546ea084a2312deda1e2262499a8fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.3 MB (55346322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e68227491146fa8b2b5ebaabeb2df0f7a4012c334cb2dd39d5dbef3cb347920`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:38 GMT
ADD file:2d8ac62dd229ef26536f5a9af9e61df30ea68d609fa969786dfd531aea18cf3c in / 
# Mon, 07 Aug 2023 19:38:38 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:28:41 GMT
ARG CONSUL_VERSION=1.14.8
# Mon, 07 Aug 2023 20:28:42 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Mon, 07 Aug 2023 20:28:42 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Mon, 07 Aug 2023 20:28:42 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN addgroup consul &&     adduser -S -G consul consul
# Mon, 07 Aug 2023 20:28:50 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Mon, 07 Aug 2023 20:28:51 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Mon, 07 Aug 2023 20:28:51 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 07 Aug 2023 20:28:51 GMT
VOLUME [/consul/data]
# Mon, 07 Aug 2023 20:28:51 GMT
EXPOSE 8300
# Mon, 07 Aug 2023 20:28:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Mon, 07 Aug 2023 20:28:52 GMT
EXPOSE 8500 8600 8600/udp
# Mon, 07 Aug 2023 20:28:52 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 07 Aug 2023 20:28:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 20:28:52 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:add53095769493cde9110fd91f113357e53b9e0d94abf216b811fcf00107674e`  
		Last Modified: Mon, 07 Aug 2023 19:39:29 GMT  
		Size: 2.8 MB (2832316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9727cd61e408aabce18f407d54181b9dc16cd78a91283dc9e6ca105c928de157`  
		Last Modified: Mon, 07 Aug 2023 20:29:34 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b37c874449c218e3b1dff71d111e100cb5ac0cc67e9d42e3e60e6a126c4d0e`  
		Last Modified: Mon, 07 Aug 2023 20:29:42 GMT  
		Size: 52.5 MB (52510580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ef26788782e2d661fa5687ec4987fdccfa2b1d89b190cf3e10f3552d56266e`  
		Last Modified: Mon, 07 Aug 2023 20:29:34 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c45703a10e2a107893650bd84f1b9ae9347468033c0a53fa155d1ee84549530`  
		Last Modified: Mon, 07 Aug 2023 20:29:34 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2b0d202297f4e4ee2e87ebf88811730d541606d7502bd58d2cd6a16ad671fd`  
		Last Modified: Mon, 07 Aug 2023 20:29:35 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.14.8`

```console
$ docker pull consul@sha256:61db114a8f84f01c21d6866818d6821ed8ba2efcf7f5550f7a6117a960982a9e
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
$ docker pull consul@sha256:590b5fb1bc18da7b0b63a02736f77737fb5fb662ace6fe12a48f0eea881132d8
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **54.0 MB (53968867 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e3cf5527024cec9d6f492824b435f81fc74a4f5dc78ed213257751f464c99490`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:27 GMT
ADD file:2270cb7f14826bc917baa12cd1ff166703f454ccd10ef5799d8106942bb0abe2 in / 
# Thu, 30 Nov 2023 22:49:27 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:40:09 GMT
ARG CONSUL_VERSION=1.14.8
# Fri, 01 Dec 2023 00:40:09 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 01 Dec 2023 00:40:09 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 01 Dec 2023 00:40:10 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 01 Dec 2023 00:40:17 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 01 Dec 2023 00:40:18 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 01 Dec 2023 00:40:19 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 01 Dec 2023 00:40:19 GMT
VOLUME [/consul/data]
# Fri, 01 Dec 2023 00:40:19 GMT
EXPOSE 8300
# Fri, 01 Dec 2023 00:40:20 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 01 Dec 2023 00:40:20 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 01 Dec 2023 00:40:20 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 01 Dec 2023 00:40:21 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 00:40:21 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:be5e3feadb89f4f40a3bc5997dbddd75fdc3686e938beb9d363990d92db9e4aa`  
		Last Modified: Thu, 30 Nov 2023 22:50:12 GMT  
		Size: 2.6 MB (2633457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4207d01db70f83377abba935e54c2901408dbf281cfd7c75e3c5343cf5ee3428`  
		Last Modified: Fri, 01 Dec 2023 00:40:58 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:891dc74a60db0d9de345ad57de44561e3aa71022ffb0a3b1c3c36988babc12a8`  
		Last Modified: Fri, 01 Dec 2023 00:41:04 GMT  
		Size: 51.3 MB (51331980 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:42ef4227ccde8475b88177027bebdeb3af168faf9cc9b69165ce62979d9b9879`  
		Last Modified: Fri, 01 Dec 2023 00:40:58 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e23b7910b33036343336c61f6edeb6556a6f0b09f7a31f6bb006954da0e41ecc`  
		Last Modified: Fri, 01 Dec 2023 00:40:58 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ff4160e9bd2d0889f8b9ac21a662500f482571708ab7c54b89a94cb36546af9a`  
		Last Modified: Fri, 01 Dec 2023 00:40:58 GMT  
		Size: 1.8 KB (1834 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14.8` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:bac6fe85dea2d81b469c702904a2d789d69cd4904b4b84fc1d077a00ef9a6129
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **53.5 MB (53510951 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:852f1ca2417bd4b123073cd6bcf571b97b784f0ae898fb11d0303dd3732aff77`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:29 GMT
ADD file:21f240e1e33b25dacee7291cdd8c7750995aa0f460d13496a08c4a2dd92323aa in / 
# Mon, 07 Aug 2023 19:39:29 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:17:50 GMT
ARG CONSUL_VERSION=1.14.8
# Mon, 07 Aug 2023 20:17:50 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Mon, 07 Aug 2023 20:17:50 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Mon, 07 Aug 2023 20:17:51 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN addgroup consul &&     adduser -S -G consul consul
# Mon, 07 Aug 2023 20:17:55 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Mon, 07 Aug 2023 20:17:56 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Mon, 07 Aug 2023 20:17:57 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 07 Aug 2023 20:17:57 GMT
VOLUME [/consul/data]
# Mon, 07 Aug 2023 20:17:57 GMT
EXPOSE 8300
# Mon, 07 Aug 2023 20:17:57 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Mon, 07 Aug 2023 20:17:57 GMT
EXPOSE 8500 8600 8600/udp
# Mon, 07 Aug 2023 20:17:57 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 07 Aug 2023 20:17:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 20:17:57 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ad3fa0ea069c04e4ee9be58cf0ae9e1a8a56f649b96a96298203b055e8c903ff`  
		Last Modified: Mon, 07 Aug 2023 19:40:16 GMT  
		Size: 2.7 MB (2720868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5c69d01bb5e779a77b1b6be7b11e6e14b19aec1533dd63b5a65314f5b7691b6`  
		Last Modified: Mon, 07 Aug 2023 20:18:30 GMT  
		Size: 1.3 KB (1266 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ce7aa33142a39195c54d295911e177b3707ef5a63ec8c4b0fcc455b1916da8f`  
		Last Modified: Mon, 07 Aug 2023 20:18:36 GMT  
		Size: 50.8 MB (50786658 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4643c57e719dc24d07a83851939342452e1d28a3fe40f3a31521ee8debe52a4d`  
		Last Modified: Mon, 07 Aug 2023 20:18:31 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62d856ab6a6f6a21e865284b96c4b2d2ea071950e50ff571b947c372c59e2153`  
		Last Modified: Mon, 07 Aug 2023 20:18:31 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e707499da1a15cf701449b919d58d13e3b02bea4d145c28b6506c33fe6630724`  
		Last Modified: Mon, 07 Aug 2023 20:18:30 GMT  
		Size: 1.8 KB (1830 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.14.8` - linux; 386

```console
$ docker pull consul@sha256:6c0dc4878c036e40a8f34b0a8de41de8d9546ea084a2312deda1e2262499a8fa
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.3 MB (55346322 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:7e68227491146fa8b2b5ebaabeb2df0f7a4012c334cb2dd39d5dbef3cb347920`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:38 GMT
ADD file:2d8ac62dd229ef26536f5a9af9e61df30ea68d609fa969786dfd531aea18cf3c in / 
# Mon, 07 Aug 2023 19:38:38 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:28:41 GMT
ARG CONSUL_VERSION=1.14.8
# Mon, 07 Aug 2023 20:28:42 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.14.8 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Mon, 07 Aug 2023 20:28:42 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Mon, 07 Aug 2023 20:28:42 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN addgroup consul &&     adduser -S -G consul consul
# Mon, 07 Aug 2023 20:28:50 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Mon, 07 Aug 2023 20:28:51 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Mon, 07 Aug 2023 20:28:51 GMT
# ARGS: CONSUL_VERSION=1.14.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 07 Aug 2023 20:28:51 GMT
VOLUME [/consul/data]
# Mon, 07 Aug 2023 20:28:51 GMT
EXPOSE 8300
# Mon, 07 Aug 2023 20:28:51 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Mon, 07 Aug 2023 20:28:52 GMT
EXPOSE 8500 8600 8600/udp
# Mon, 07 Aug 2023 20:28:52 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 07 Aug 2023 20:28:52 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 20:28:52 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:add53095769493cde9110fd91f113357e53b9e0d94abf216b811fcf00107674e`  
		Last Modified: Mon, 07 Aug 2023 19:39:29 GMT  
		Size: 2.8 MB (2832316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9727cd61e408aabce18f407d54181b9dc16cd78a91283dc9e6ca105c928de157`  
		Last Modified: Mon, 07 Aug 2023 20:29:34 GMT  
		Size: 1.3 KB (1268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d5b37c874449c218e3b1dff71d111e100cb5ac0cc67e9d42e3e60e6a126c4d0e`  
		Last Modified: Mon, 07 Aug 2023 20:29:42 GMT  
		Size: 52.5 MB (52510580 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58ef26788782e2d661fa5687ec4987fdccfa2b1d89b190cf3e10f3552d56266e`  
		Last Modified: Mon, 07 Aug 2023 20:29:34 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1c45703a10e2a107893650bd84f1b9ae9347468033c0a53fa155d1ee84549530`  
		Last Modified: Mon, 07 Aug 2023 20:29:34 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bb2b0d202297f4e4ee2e87ebf88811730d541606d7502bd58d2cd6a16ad671fd`  
		Last Modified: Mon, 07 Aug 2023 20:29:35 GMT  
		Size: 1.8 KB (1832 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.15`

```console
$ docker pull consul@sha256:35b840b9d37d6c28ed50d4e78a69a3cf20ac744ba26ae2727c24f7de7c522b4f
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
$ docker pull consul@sha256:e60ada3f4d51811514259a2f5b3d04d9aeb5084f2c5d00fa6200a47fb70bb825
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56038339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bff17cc6b014d1e5b3a8c2f086c1978c77f2fb5b2a2c7bfa6fa0aa4e775639d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:27 GMT
ADD file:2270cb7f14826bc917baa12cd1ff166703f454ccd10ef5799d8106942bb0abe2 in / 
# Thu, 30 Nov 2023 22:49:27 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:39:46 GMT
ARG CONSUL_VERSION=1.15.4
# Fri, 01 Dec 2023 00:39:46 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 01 Dec 2023 00:39:46 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 01 Dec 2023 00:39:46 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 01 Dec 2023 00:40:02 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 01 Dec 2023 00:40:03 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 01 Dec 2023 00:40:03 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 01 Dec 2023 00:40:03 GMT
VOLUME [/consul/data]
# Fri, 01 Dec 2023 00:40:03 GMT
EXPOSE 8300
# Fri, 01 Dec 2023 00:40:03 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 01 Dec 2023 00:40:04 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 01 Dec 2023 00:40:04 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 01 Dec 2023 00:40:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 00:40:04 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:be5e3feadb89f4f40a3bc5997dbddd75fdc3686e938beb9d363990d92db9e4aa`  
		Last Modified: Thu, 30 Nov 2023 22:50:12 GMT  
		Size: 2.6 MB (2633457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f04b195edcdd53580760227d2a5647547fe0e1a1b416daf000fa708b6a31f98`  
		Last Modified: Fri, 01 Dec 2023 00:40:42 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05285126896042a9338ebb9d3ed7dbaa97f47cd61a68e2a37595d5243158044`  
		Last Modified: Fri, 01 Dec 2023 00:40:49 GMT  
		Size: 53.4 MB (53401451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26c0a59e26ed82799fc4ddb48a81ffa7940f5c469411b5721ecb16d05b95b16`  
		Last Modified: Fri, 01 Dec 2023 00:40:42 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f89d2dcac915c8f8b5025470d0a364da12a2577102748754a17e97dbda69916`  
		Last Modified: Fri, 01 Dec 2023 00:40:42 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a0cd0ab4ca7627a45ca0719c869727355e0ebd054196d8597f0f30936addfa`  
		Last Modified: Fri, 01 Dec 2023 00:40:43 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.15` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:3e252086ef0da34ea27c0dcfade9252444be163a6a18a16ebb24095c7ead916d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55603514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea2b204bb98ec01683744f0991efb916fa505ec449149f9aff98a8645cb5f88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:29 GMT
ADD file:21f240e1e33b25dacee7291cdd8c7750995aa0f460d13496a08c4a2dd92323aa in / 
# Mon, 07 Aug 2023 19:39:29 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:17:39 GMT
ARG CONSUL_VERSION=1.15.4
# Mon, 07 Aug 2023 20:17:39 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Mon, 07 Aug 2023 20:17:39 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Mon, 07 Aug 2023 20:17:39 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN addgroup consul &&     adduser -S -G consul consul
# Mon, 07 Aug 2023 20:17:45 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Mon, 07 Aug 2023 20:17:46 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Mon, 07 Aug 2023 20:17:46 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 07 Aug 2023 20:17:46 GMT
VOLUME [/consul/data]
# Mon, 07 Aug 2023 20:17:46 GMT
EXPOSE 8300
# Mon, 07 Aug 2023 20:17:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Mon, 07 Aug 2023 20:17:47 GMT
EXPOSE 8500 8600 8600/udp
# Mon, 07 Aug 2023 20:17:47 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 07 Aug 2023 20:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 20:17:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ad3fa0ea069c04e4ee9be58cf0ae9e1a8a56f649b96a96298203b055e8c903ff`  
		Last Modified: Mon, 07 Aug 2023 19:40:16 GMT  
		Size: 2.7 MB (2720868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc0ff86a773a4b23131c6a192cb6265108a9bb27f571f7dd5c7c6425dabdef4`  
		Last Modified: Mon, 07 Aug 2023 20:18:16 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a221f2346c39c3f6194efb140134f02a0685d643a5ea0d4814b4abef95e3afcd`  
		Last Modified: Mon, 07 Aug 2023 20:18:22 GMT  
		Size: 52.9 MB (52879216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30201693224304958e9ecef50dac60c54d179a6c785bd84f436809ee88120a3d`  
		Last Modified: Mon, 07 Aug 2023 20:18:17 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec582cf4de3bbc225cde18e26925f71e6de25d7b02d20398b9f27d709362fcd`  
		Last Modified: Mon, 07 Aug 2023 20:18:16 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be66a0761e47c07a158fa069bb3ea8990a042f836f552d64c89b29daaf4f449d`  
		Last Modified: Mon, 07 Aug 2023 20:18:16 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.15` - linux; 386

```console
$ docker pull consul@sha256:df36500e40b488a5e2ba02c2d617dcebe2a6cecdb777579e651aeef499e1c295
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57428519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c7c086b3b6c90d643222a2582b3fa6cace55846f3c83991e735660b909aea2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:38 GMT
ADD file:2d8ac62dd229ef26536f5a9af9e61df30ea68d609fa969786dfd531aea18cf3c in / 
# Mon, 07 Aug 2023 19:38:38 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:28:22 GMT
ARG CONSUL_VERSION=1.15.4
# Mon, 07 Aug 2023 20:28:22 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Mon, 07 Aug 2023 20:28:22 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Mon, 07 Aug 2023 20:28:23 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN addgroup consul &&     adduser -S -G consul consul
# Mon, 07 Aug 2023 20:28:36 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Mon, 07 Aug 2023 20:28:36 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Mon, 07 Aug 2023 20:28:37 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 07 Aug 2023 20:28:37 GMT
VOLUME [/consul/data]
# Mon, 07 Aug 2023 20:28:37 GMT
EXPOSE 8300
# Mon, 07 Aug 2023 20:28:37 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Mon, 07 Aug 2023 20:28:37 GMT
EXPOSE 8500 8600 8600/udp
# Mon, 07 Aug 2023 20:28:38 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 07 Aug 2023 20:28:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 20:28:38 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:add53095769493cde9110fd91f113357e53b9e0d94abf216b811fcf00107674e`  
		Last Modified: Mon, 07 Aug 2023 19:39:29 GMT  
		Size: 2.8 MB (2832316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839237463244ad8fa7addb4ee8b214ca710e9be73179f1a4d481c75fb6007553`  
		Last Modified: Mon, 07 Aug 2023 20:29:17 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d3a79e0e88ffed7a72946d5847aec4e35775bf9f5436a04eb00425712f0eaa`  
		Last Modified: Mon, 07 Aug 2023 20:29:26 GMT  
		Size: 54.6 MB (54592773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc8a73d94f7aeb23b310e492bbe6faa3c194ba10785e5f5446758879acbd276`  
		Last Modified: Mon, 07 Aug 2023 20:29:17 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62687d6d763e66949be32cb9c9b4b38787ae35f407f59f6594421aee6de454cd`  
		Last Modified: Mon, 07 Aug 2023 20:29:17 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f0861dff5ccce5a271ba4a5a11fd46edadc6b527cd385eb060da57d5bb9816`  
		Last Modified: Mon, 07 Aug 2023 20:29:17 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.15.4`

```console
$ docker pull consul@sha256:35b840b9d37d6c28ed50d4e78a69a3cf20ac744ba26ae2727c24f7de7c522b4f
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
$ docker pull consul@sha256:e60ada3f4d51811514259a2f5b3d04d9aeb5084f2c5d00fa6200a47fb70bb825
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **56.0 MB (56038339 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:6bff17cc6b014d1e5b3a8c2f086c1978c77f2fb5b2a2c7bfa6fa0aa4e775639d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Thu, 30 Nov 2023 22:49:27 GMT
ADD file:2270cb7f14826bc917baa12cd1ff166703f454ccd10ef5799d8106942bb0abe2 in / 
# Thu, 30 Nov 2023 22:49:27 GMT
CMD ["/bin/sh"]
# Fri, 01 Dec 2023 00:39:46 GMT
ARG CONSUL_VERSION=1.15.4
# Fri, 01 Dec 2023 00:39:46 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Fri, 01 Dec 2023 00:39:46 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 01 Dec 2023 00:39:46 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 01 Dec 2023 00:40:02 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 01 Dec 2023 00:40:03 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 01 Dec 2023 00:40:03 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 01 Dec 2023 00:40:03 GMT
VOLUME [/consul/data]
# Fri, 01 Dec 2023 00:40:03 GMT
EXPOSE 8300
# Fri, 01 Dec 2023 00:40:03 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 01 Dec 2023 00:40:04 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 01 Dec 2023 00:40:04 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 01 Dec 2023 00:40:04 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 01 Dec 2023 00:40:04 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:be5e3feadb89f4f40a3bc5997dbddd75fdc3686e938beb9d363990d92db9e4aa`  
		Last Modified: Thu, 30 Nov 2023 22:50:12 GMT  
		Size: 2.6 MB (2633457 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:7f04b195edcdd53580760227d2a5647547fe0e1a1b416daf000fa708b6a31f98`  
		Last Modified: Fri, 01 Dec 2023 00:40:42 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05285126896042a9338ebb9d3ed7dbaa97f47cd61a68e2a37595d5243158044`  
		Last Modified: Fri, 01 Dec 2023 00:40:49 GMT  
		Size: 53.4 MB (53401451 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c26c0a59e26ed82799fc4ddb48a81ffa7940f5c469411b5721ecb16d05b95b16`  
		Last Modified: Fri, 01 Dec 2023 00:40:42 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f89d2dcac915c8f8b5025470d0a364da12a2577102748754a17e97dbda69916`  
		Last Modified: Fri, 01 Dec 2023 00:40:42 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88a0cd0ab4ca7627a45ca0719c869727355e0ebd054196d8597f0f30936addfa`  
		Last Modified: Fri, 01 Dec 2023 00:40:43 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.15.4` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:3e252086ef0da34ea27c0dcfade9252444be163a6a18a16ebb24095c7ead916d
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **55.6 MB (55603514 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:4ea2b204bb98ec01683744f0991efb916fa505ec449149f9aff98a8645cb5f88`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 07 Aug 2023 19:39:29 GMT
ADD file:21f240e1e33b25dacee7291cdd8c7750995aa0f460d13496a08c4a2dd92323aa in / 
# Mon, 07 Aug 2023 19:39:29 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:17:39 GMT
ARG CONSUL_VERSION=1.15.4
# Mon, 07 Aug 2023 20:17:39 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Mon, 07 Aug 2023 20:17:39 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Mon, 07 Aug 2023 20:17:39 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN addgroup consul &&     adduser -S -G consul consul
# Mon, 07 Aug 2023 20:17:45 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Mon, 07 Aug 2023 20:17:46 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Mon, 07 Aug 2023 20:17:46 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 07 Aug 2023 20:17:46 GMT
VOLUME [/consul/data]
# Mon, 07 Aug 2023 20:17:46 GMT
EXPOSE 8300
# Mon, 07 Aug 2023 20:17:46 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Mon, 07 Aug 2023 20:17:47 GMT
EXPOSE 8500 8600 8600/udp
# Mon, 07 Aug 2023 20:17:47 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 07 Aug 2023 20:17:47 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 20:17:47 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:ad3fa0ea069c04e4ee9be58cf0ae9e1a8a56f649b96a96298203b055e8c903ff`  
		Last Modified: Mon, 07 Aug 2023 19:40:16 GMT  
		Size: 2.7 MB (2720868 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cc0ff86a773a4b23131c6a192cb6265108a9bb27f571f7dd5c7c6425dabdef4`  
		Last Modified: Mon, 07 Aug 2023 20:18:16 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a221f2346c39c3f6194efb140134f02a0685d643a5ea0d4814b4abef95e3afcd`  
		Last Modified: Mon, 07 Aug 2023 20:18:22 GMT  
		Size: 52.9 MB (52879216 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:30201693224304958e9ecef50dac60c54d179a6c785bd84f436809ee88120a3d`  
		Last Modified: Mon, 07 Aug 2023 20:18:17 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3ec582cf4de3bbc225cde18e26925f71e6de25d7b02d20398b9f27d709362fcd`  
		Last Modified: Mon, 07 Aug 2023 20:18:16 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:be66a0761e47c07a158fa069bb3ea8990a042f836f552d64c89b29daaf4f449d`  
		Last Modified: Mon, 07 Aug 2023 20:18:16 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.15.4` - linux; 386

```console
$ docker pull consul@sha256:df36500e40b488a5e2ba02c2d617dcebe2a6cecdb777579e651aeef499e1c295
```

-	Docker Version: 20.10.23
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **57.4 MB (57428519 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:83c7c086b3b6c90d643222a2582b3fa6cace55846f3c83991e735660b909aea2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Mon, 07 Aug 2023 19:38:38 GMT
ADD file:2d8ac62dd229ef26536f5a9af9e61df30ea68d609fa969786dfd531aea18cf3c in / 
# Mon, 07 Aug 2023 19:38:38 GMT
CMD ["/bin/sh"]
# Mon, 07 Aug 2023 20:28:22 GMT
ARG CONSUL_VERSION=1.15.4
# Mon, 07 Aug 2023 20:28:22 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com> org.opencontainers.image.url=https://www.consul.io/ org.opencontainers.image.documentation=https://www.consul.io/docs org.opencontainers.image.source=https://github.com/hashicorp/consul org.opencontainers.image.version=1.15.4 org.opencontainers.image.vendor=HashiCorp org.opencontainers.image.title=consul org.opencontainers.image.description=Consul is a datacenter runtime that provides service discovery, configuration, and orchestration.
# Mon, 07 Aug 2023 20:28:22 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Mon, 07 Aug 2023 20:28:23 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN addgroup consul &&     adduser -S -G consul consul
# Mon, 07 Aug 2023 20:28:36 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables tzdata &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='arm' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Mon, 07 Aug 2023 20:28:36 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Mon, 07 Aug 2023 20:28:37 GMT
# ARGS: CONSUL_VERSION=1.15.4
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Mon, 07 Aug 2023 20:28:37 GMT
VOLUME [/consul/data]
# Mon, 07 Aug 2023 20:28:37 GMT
EXPOSE 8300
# Mon, 07 Aug 2023 20:28:37 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Mon, 07 Aug 2023 20:28:37 GMT
EXPOSE 8500 8600 8600/udp
# Mon, 07 Aug 2023 20:28:38 GMT
COPY file:f5ba00fb9fd3a67a835a792e07b11da3b163222c18f8512aa772b36520d2a653 in /usr/local/bin/docker-entrypoint.sh 
# Mon, 07 Aug 2023 20:28:38 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Mon, 07 Aug 2023 20:28:38 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:add53095769493cde9110fd91f113357e53b9e0d94abf216b811fcf00107674e`  
		Last Modified: Mon, 07 Aug 2023 19:39:29 GMT  
		Size: 2.8 MB (2832316 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:839237463244ad8fa7addb4ee8b214ca710e9be73179f1a4d481c75fb6007553`  
		Last Modified: Mon, 07 Aug 2023 20:29:17 GMT  
		Size: 1.3 KB (1267 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d3a79e0e88ffed7a72946d5847aec4e35775bf9f5436a04eb00425712f0eaa`  
		Last Modified: Mon, 07 Aug 2023 20:29:26 GMT  
		Size: 54.6 MB (54592773 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6dc8a73d94f7aeb23b310e492bbe6faa3c194ba10785e5f5446758879acbd276`  
		Last Modified: Mon, 07 Aug 2023 20:29:17 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:62687d6d763e66949be32cb9c9b4b38787ae35f407f59f6594421aee6de454cd`  
		Last Modified: Mon, 07 Aug 2023 20:29:17 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c4f0861dff5ccce5a271ba4a5a11fd46edadc6b527cd385eb060da57d5bb9816`  
		Last Modified: Mon, 07 Aug 2023 20:29:17 GMT  
		Size: 1.8 KB (1835 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
