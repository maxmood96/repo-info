<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.10`](#consul110)
-	[`consul:1.10.0`](#consul1100)
-	[`consul:1.8`](#consul18)
-	[`consul:1.8.13`](#consul1813)
-	[`consul:1.9`](#consul19)
-	[`consul:1.9.7`](#consul197)
-	[`consul:latest`](#consullatest)

## `consul:1.10`

```console
$ docker pull consul@sha256:c58e1f8d4f13eb4e2155a2830d55380ab3f66d8588e21bb135a75d803975da91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10` - linux; amd64

```console
$ docker pull consul@sha256:fcc3bc6c30ea40b47e6aa2f491a785965bea5ffcef722c666d1fa3a6949760fe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43619939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0846dc12365b73e2ffe2eb25541c30f1580d16b4ed424643f58975f3deae3ab0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 18:19:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 21:21:54 GMT
ARG CONSUL_VERSION=1.10.0
# Tue, 22 Jun 2021 21:21:54 GMT
LABEL org.opencontainers.image.version=1.10.0
# Tue, 22 Jun 2021 21:21:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 21:21:56 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 21:22:01 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 21:22:03 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 21:22:03 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 21:22:04 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 21:22:04 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 21:22:04 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 21:22:04 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 21:22:04 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 21:22:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 21:22:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d468a8c3b43256569f9b2b67d51514ec6679816787de88801a10bcb301a709`  
		Last Modified: Tue, 22 Jun 2021 21:22:48 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105d8515b2215472860538abf77d14b3601cae4b72884d459eefcafbe0e107f4`  
		Last Modified: Tue, 22 Jun 2021 21:22:54 GMT  
		Size: 40.8 MB (40804675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ed6bc2e594daff0582e63eb92f380145f7f303fb4346b05400bb01ab58183e`  
		Last Modified: Tue, 22 Jun 2021 21:22:47 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1981893a8c5f7dbc4d2305e2f37dfcfc9d99a71513555ed16fc5bb0ecc39a8e`  
		Last Modified: Tue, 22 Jun 2021 21:22:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b39d63083e8e2e70c8f000ac9b0828b61cecd954468d8f28a51358010ce881`  
		Last Modified: Tue, 22 Jun 2021 21:22:48 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm variant v6

```console
$ docker pull consul@sha256:20576537c4a0095923c8b23fe3aadc07c2cd0a828cfb467a4b499ddde6015b2b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39630159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a717761a11b7d16aac6a950fe0f8017e3c54b4856141b27d6335d8be3fd97b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Tue, 22 Jun 2021 22:20:06 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 22:20:06 GMT
ARG CONSUL_VERSION=1.10.0
# Tue, 22 Jun 2021 22:20:07 GMT
LABEL org.opencontainers.image.version=1.10.0
# Tue, 22 Jun 2021 22:20:07 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 22:20:08 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 22:20:21 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 22:20:23 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 22:20:24 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 22:20:25 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 22:20:25 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 22:20:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 22:20:26 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 22:20:27 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 22:20:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 22:20:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07d1eb174fc9249548c4b20da900dc348680f32d74676f33dd0951274dff98b`  
		Last Modified: Tue, 22 Jun 2021 22:22:10 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4881247682906d151dd4266dc1f16b3787c3782e123136a9d9174f81f6d6e250`  
		Last Modified: Tue, 22 Jun 2021 22:22:32 GMT  
		Size: 37.0 MB (37004734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8eb296fb8741f925b4e9a4bdd8d5f57d707bee2e71bcb95f8842b461902ac9b`  
		Last Modified: Tue, 22 Jun 2021 22:22:10 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0ff50377a85d926a7616c0ab6a4f499e49182fcbb508697866678c3e1ea1bf`  
		Last Modified: Tue, 22 Jun 2021 22:22:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20660d5b18ed07b69136dc58b3b854487ca3faa30c30d2320fd6ab0ffca7988b`  
		Last Modified: Tue, 22 Jun 2021 22:22:10 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:1a8038945ebb4d2983fe5aea38f8b676e45d432efabbb785a678d4d45e57a760
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39576123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2005a537b1b2d018ef3390c27e06be8ac9e9a65f06e01cff0f193a987a110f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:25:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 21:42:45 GMT
ARG CONSUL_VERSION=1.10.0
# Tue, 22 Jun 2021 21:42:45 GMT
LABEL org.opencontainers.image.version=1.10.0
# Tue, 22 Jun 2021 21:42:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 21:42:46 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 21:42:51 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 21:42:52 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 21:42:53 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 21:42:53 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 21:42:53 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 21:42:53 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 21:42:54 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 21:42:54 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 21:42:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 21:42:54 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3d1412f415f7d8fd08f4f596252a334bea5a112509304795c9242b32e30e3d`  
		Last Modified: Tue, 22 Jun 2021 21:43:46 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ca6286d3fe33aae8a5881ad0fc09d3e13850fb1a3984d67261199b1d8db56b`  
		Last Modified: Tue, 22 Jun 2021 21:43:51 GMT  
		Size: 36.9 MB (36860805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d513ae58978f46ffd449b76a88acd290bdbbf2c8dc7e90ef9e04014b99d11bf`  
		Last Modified: Tue, 22 Jun 2021 21:43:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4213bb62e786f44e51cf798e925ea48395500839e002338e8bea51c14f45db8b`  
		Last Modified: Tue, 22 Jun 2021 21:43:46 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b6bb821282f46b639f0ce35010cdaf11df4a929186515888a6c73479439af1`  
		Last Modified: Tue, 22 Jun 2021 21:43:46 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; 386

```console
$ docker pull consul@sha256:265f8bd3a47c18087b52ce60c3d1e40631f2199891a6039f6666ba4c13f12ddd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (42986555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a54f4d554dc437bf70ce8efa661163bb6233eb6f20c3a031c3fabf6f09bc99b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 17:39:34 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 21:42:06 GMT
ARG CONSUL_VERSION=1.10.0
# Tue, 22 Jun 2021 21:42:07 GMT
LABEL org.opencontainers.image.version=1.10.0
# Tue, 22 Jun 2021 21:42:07 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 21:42:08 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 21:42:15 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 21:42:16 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 21:42:17 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 21:42:17 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 21:42:17 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 21:42:18 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 21:42:18 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 21:42:18 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 21:42:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 21:42:18 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe0317095bb660706913746e0261e794f76eb1ae5ad739c83f672b50efe65ae`  
		Last Modified: Tue, 22 Jun 2021 21:43:19 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fadc1c405e1df51949be3115d7235c9ca7520b4eefa0e9c508716a02c910907`  
		Last Modified: Tue, 22 Jun 2021 21:43:27 GMT  
		Size: 40.2 MB (40164364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ecaad2c81fb77d29ad853f94b04a020c3266a11823d0a2883ae69dc84e01a9`  
		Last Modified: Tue, 22 Jun 2021 21:43:19 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d51ffce497a34f282fc5ebcc0d250873137530d051b74260446222831b2c45e`  
		Last Modified: Tue, 22 Jun 2021 21:43:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d5d813d3765868039b456e2edcf9ab175b0f7c836c532118ca67a42357d7ac`  
		Last Modified: Tue, 22 Jun 2021 21:43:19 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.10.0`

```console
$ docker pull consul@sha256:c58e1f8d4f13eb4e2155a2830d55380ab3f66d8588e21bb135a75d803975da91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10.0` - linux; amd64

```console
$ docker pull consul@sha256:fcc3bc6c30ea40b47e6aa2f491a785965bea5ffcef722c666d1fa3a6949760fe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43619939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0846dc12365b73e2ffe2eb25541c30f1580d16b4ed424643f58975f3deae3ab0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 18:19:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 21:21:54 GMT
ARG CONSUL_VERSION=1.10.0
# Tue, 22 Jun 2021 21:21:54 GMT
LABEL org.opencontainers.image.version=1.10.0
# Tue, 22 Jun 2021 21:21:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 21:21:56 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 21:22:01 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 21:22:03 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 21:22:03 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 21:22:04 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 21:22:04 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 21:22:04 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 21:22:04 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 21:22:04 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 21:22:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 21:22:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d468a8c3b43256569f9b2b67d51514ec6679816787de88801a10bcb301a709`  
		Last Modified: Tue, 22 Jun 2021 21:22:48 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105d8515b2215472860538abf77d14b3601cae4b72884d459eefcafbe0e107f4`  
		Last Modified: Tue, 22 Jun 2021 21:22:54 GMT  
		Size: 40.8 MB (40804675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ed6bc2e594daff0582e63eb92f380145f7f303fb4346b05400bb01ab58183e`  
		Last Modified: Tue, 22 Jun 2021 21:22:47 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1981893a8c5f7dbc4d2305e2f37dfcfc9d99a71513555ed16fc5bb0ecc39a8e`  
		Last Modified: Tue, 22 Jun 2021 21:22:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b39d63083e8e2e70c8f000ac9b0828b61cecd954468d8f28a51358010ce881`  
		Last Modified: Tue, 22 Jun 2021 21:22:48 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.0` - linux; arm variant v6

```console
$ docker pull consul@sha256:20576537c4a0095923c8b23fe3aadc07c2cd0a828cfb467a4b499ddde6015b2b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39630159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a717761a11b7d16aac6a950fe0f8017e3c54b4856141b27d6335d8be3fd97b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Tue, 22 Jun 2021 22:20:06 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 22:20:06 GMT
ARG CONSUL_VERSION=1.10.0
# Tue, 22 Jun 2021 22:20:07 GMT
LABEL org.opencontainers.image.version=1.10.0
# Tue, 22 Jun 2021 22:20:07 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 22:20:08 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 22:20:21 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 22:20:23 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 22:20:24 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 22:20:25 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 22:20:25 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 22:20:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 22:20:26 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 22:20:27 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 22:20:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 22:20:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07d1eb174fc9249548c4b20da900dc348680f32d74676f33dd0951274dff98b`  
		Last Modified: Tue, 22 Jun 2021 22:22:10 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4881247682906d151dd4266dc1f16b3787c3782e123136a9d9174f81f6d6e250`  
		Last Modified: Tue, 22 Jun 2021 22:22:32 GMT  
		Size: 37.0 MB (37004734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8eb296fb8741f925b4e9a4bdd8d5f57d707bee2e71bcb95f8842b461902ac9b`  
		Last Modified: Tue, 22 Jun 2021 22:22:10 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0ff50377a85d926a7616c0ab6a4f499e49182fcbb508697866678c3e1ea1bf`  
		Last Modified: Tue, 22 Jun 2021 22:22:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20660d5b18ed07b69136dc58b3b854487ca3faa30c30d2320fd6ab0ffca7988b`  
		Last Modified: Tue, 22 Jun 2021 22:22:10 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.0` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:1a8038945ebb4d2983fe5aea38f8b676e45d432efabbb785a678d4d45e57a760
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39576123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2005a537b1b2d018ef3390c27e06be8ac9e9a65f06e01cff0f193a987a110f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:25:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 21:42:45 GMT
ARG CONSUL_VERSION=1.10.0
# Tue, 22 Jun 2021 21:42:45 GMT
LABEL org.opencontainers.image.version=1.10.0
# Tue, 22 Jun 2021 21:42:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 21:42:46 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 21:42:51 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 21:42:52 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 21:42:53 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 21:42:53 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 21:42:53 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 21:42:53 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 21:42:54 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 21:42:54 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 21:42:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 21:42:54 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3d1412f415f7d8fd08f4f596252a334bea5a112509304795c9242b32e30e3d`  
		Last Modified: Tue, 22 Jun 2021 21:43:46 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ca6286d3fe33aae8a5881ad0fc09d3e13850fb1a3984d67261199b1d8db56b`  
		Last Modified: Tue, 22 Jun 2021 21:43:51 GMT  
		Size: 36.9 MB (36860805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d513ae58978f46ffd449b76a88acd290bdbbf2c8dc7e90ef9e04014b99d11bf`  
		Last Modified: Tue, 22 Jun 2021 21:43:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4213bb62e786f44e51cf798e925ea48395500839e002338e8bea51c14f45db8b`  
		Last Modified: Tue, 22 Jun 2021 21:43:46 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b6bb821282f46b639f0ce35010cdaf11df4a929186515888a6c73479439af1`  
		Last Modified: Tue, 22 Jun 2021 21:43:46 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.0` - linux; 386

```console
$ docker pull consul@sha256:265f8bd3a47c18087b52ce60c3d1e40631f2199891a6039f6666ba4c13f12ddd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (42986555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a54f4d554dc437bf70ce8efa661163bb6233eb6f20c3a031c3fabf6f09bc99b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 17:39:34 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 21:42:06 GMT
ARG CONSUL_VERSION=1.10.0
# Tue, 22 Jun 2021 21:42:07 GMT
LABEL org.opencontainers.image.version=1.10.0
# Tue, 22 Jun 2021 21:42:07 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 21:42:08 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 21:42:15 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 21:42:16 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 21:42:17 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 21:42:17 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 21:42:17 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 21:42:18 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 21:42:18 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 21:42:18 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 21:42:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 21:42:18 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe0317095bb660706913746e0261e794f76eb1ae5ad739c83f672b50efe65ae`  
		Last Modified: Tue, 22 Jun 2021 21:43:19 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fadc1c405e1df51949be3115d7235c9ca7520b4eefa0e9c508716a02c910907`  
		Last Modified: Tue, 22 Jun 2021 21:43:27 GMT  
		Size: 40.2 MB (40164364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ecaad2c81fb77d29ad853f94b04a020c3266a11823d0a2883ae69dc84e01a9`  
		Last Modified: Tue, 22 Jun 2021 21:43:19 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d51ffce497a34f282fc5ebcc0d250873137530d051b74260446222831b2c45e`  
		Last Modified: Tue, 22 Jun 2021 21:43:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d5d813d3765868039b456e2edcf9ab175b0f7c836c532118ca67a42357d7ac`  
		Last Modified: Tue, 22 Jun 2021 21:43:19 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8`

```console
$ docker pull consul@sha256:2f5a508a518c61eb835777fcd91b293277c155d7cce64a5ce6675eb68d5968d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8` - linux; amd64

```console
$ docker pull consul@sha256:593f310ff98c87cbd1c05c84ee8a68d4e0981d98d93f4d6bee6478453dcc87db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47787174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a1be6461c5d0e936c3cbc7845d2a7cbf07185501607ff6b9326a781f87a08b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 18:19:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 21:22:21 GMT
ARG CONSUL_VERSION=1.8.13
# Tue, 22 Jun 2021 21:22:22 GMT
LABEL org.opencontainers.image.version=1.8.13
# Tue, 22 Jun 2021 21:22:22 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 21:22:23 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 21:22:29 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 21:22:30 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 21:22:31 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 21:22:31 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 21:22:31 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 21:22:31 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 21:22:32 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 21:22:32 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 21:22:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 21:22:32 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6a01d5a74cef2fe3a1434a8a3d1a4f50b87e22ecbb6dbec751a712d1363496`  
		Last Modified: Tue, 22 Jun 2021 21:23:23 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e061614a002dfda954fb22b07c58ae54271515bd01a5d8a8879c35674dfc0`  
		Last Modified: Tue, 22 Jun 2021 21:23:31 GMT  
		Size: 45.0 MB (44971910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236bc01cf16d53e19c8ceda24cb9f2114f46f28cc7d1e3aa710718f2238eef2e`  
		Last Modified: Tue, 22 Jun 2021 21:23:23 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10df2afcd9668c9f59bf8e83826e19c187eae462a35859936d5f7d92ace7ac26`  
		Last Modified: Tue, 22 Jun 2021 21:23:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbad988e5f82690fcb42f15a367f7565831f561df38407ba7f19e6ce5fb6ef45`  
		Last Modified: Tue, 22 Jun 2021 21:23:23 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm variant v6

```console
$ docker pull consul@sha256:36cfc26a5954453c9e232dbca24c2e1ffb972de6a921827b1abca2133ddafb31
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43016212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181d5a82a80b8d33afde455da9886addff9dc13122795ad0bd48c36d7aeeaa54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Tue, 22 Jun 2021 22:20:06 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 22:21:08 GMT
ARG CONSUL_VERSION=1.8.13
# Tue, 22 Jun 2021 22:21:08 GMT
LABEL org.opencontainers.image.version=1.8.13
# Tue, 22 Jun 2021 22:21:09 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 22:21:10 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 22:21:21 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 22:21:23 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 22:21:24 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 22:21:25 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 22:21:25 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 22:21:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 22:21:26 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 22:21:27 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 22:21:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 22:21:28 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc1dad5b305fe1b07311ca788f6bbf30c43ba39f6b83451034add65def1ad1d`  
		Last Modified: Tue, 22 Jun 2021 22:23:22 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6989b5a9d1014551c2b6506d2343e6ff49d0ce65af84cf9a7a73e01806204c`  
		Last Modified: Tue, 22 Jun 2021 22:23:45 GMT  
		Size: 40.4 MB (40390782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d05fdd8f20fe0e87b5aa2615b87073a08bafd29d7242d1ba8693d6da45efa6`  
		Last Modified: Tue, 22 Jun 2021 22:23:22 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372f00348fdfc4df76ce209111a413c74555aecf3c23dc20641c76bf15a61fbd`  
		Last Modified: Tue, 22 Jun 2021 22:23:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6e3e6975da54969ea796781cbc957b7d07b1bfcf6de0591c1c7c4af8f01807`  
		Last Modified: Tue, 22 Jun 2021 22:23:23 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:44b5eb33df4903fe35298f4ab8a6904fde0352bec3ad56df448da2cd3d919ae2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43217135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4141fa92317ccbaf3d95264134cf46bb0c56051694b3e18b434ab28fe3a8fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:25:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 21:43:15 GMT
ARG CONSUL_VERSION=1.8.13
# Tue, 22 Jun 2021 21:43:15 GMT
LABEL org.opencontainers.image.version=1.8.13
# Tue, 22 Jun 2021 21:43:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 21:43:16 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 21:43:21 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 21:43:22 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 21:43:23 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 21:43:23 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 21:43:23 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 21:43:24 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 21:43:24 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 21:43:24 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 21:43:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 21:43:24 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a16a3a7536ab5a343392960e9723e88bf9f6c5e223022834a31c803c4cec5ab`  
		Last Modified: Tue, 22 Jun 2021 21:44:24 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d55f2e79453b44c942bee27ceb5ced5a5e7d3d8e41715a5976e935877abf6f`  
		Last Modified: Tue, 22 Jun 2021 21:44:31 GMT  
		Size: 40.5 MB (40501815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b919304680b669cc6afec8011e667e7e1eecc99890057b679c5820c3a07838`  
		Last Modified: Tue, 22 Jun 2021 21:44:24 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d6a2acf88f8720710653483a2ada92e63b8ddab80aacd7174b9f10850a42a3`  
		Last Modified: Tue, 22 Jun 2021 21:44:24 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cdf13f4d730b3f0a16a5d3d3a4caf6dbad7a7a31523796336ceaa0ea4f0864`  
		Last Modified: Tue, 22 Jun 2021 21:44:24 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; 386

```console
$ docker pull consul@sha256:58c92c1b493df76fc1c012ad6dc555bef1af1069c301098ae8e3bb1acd7bf9f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47351813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4fdb52aee73f669f5fdf09e2cb4c50567c13b22d84a001e130d98fd151e36d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 17:39:34 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 21:42:42 GMT
ARG CONSUL_VERSION=1.8.13
# Tue, 22 Jun 2021 21:42:43 GMT
LABEL org.opencontainers.image.version=1.8.13
# Tue, 22 Jun 2021 21:42:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 21:42:44 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 21:42:51 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 21:42:52 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 21:42:53 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 21:42:53 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 21:42:54 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 21:42:54 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 21:42:54 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 21:42:54 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 21:42:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 21:42:55 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb42e936a9b8f9402f66e3af766e1ba3f9dadd7e24d85edda954ea5ace08b63d`  
		Last Modified: Tue, 22 Jun 2021 21:44:03 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f7c3443d3df24c0db408e1e5aba5df45d3e571682f52d29700fe96b74d5ab1`  
		Last Modified: Tue, 22 Jun 2021 21:44:10 GMT  
		Size: 44.5 MB (44529623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d513ae58978f46ffd449b76a88acd290bdbbf2c8dc7e90ef9e04014b99d11bf`  
		Last Modified: Tue, 22 Jun 2021 21:43:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4213bb62e786f44e51cf798e925ea48395500839e002338e8bea51c14f45db8b`  
		Last Modified: Tue, 22 Jun 2021 21:43:46 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b84fb85067e960b52f6852f6b48070c46a5059c36fe7973a2de3886c22f87e9`  
		Last Modified: Tue, 22 Jun 2021 21:44:03 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8.13`

```console
$ docker pull consul@sha256:2f5a508a518c61eb835777fcd91b293277c155d7cce64a5ce6675eb68d5968d0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8.13` - linux; amd64

```console
$ docker pull consul@sha256:593f310ff98c87cbd1c05c84ee8a68d4e0981d98d93f4d6bee6478453dcc87db
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47787174 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f2a1be6461c5d0e936c3cbc7845d2a7cbf07185501607ff6b9326a781f87a08b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 18:19:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 21:22:21 GMT
ARG CONSUL_VERSION=1.8.13
# Tue, 22 Jun 2021 21:22:22 GMT
LABEL org.opencontainers.image.version=1.8.13
# Tue, 22 Jun 2021 21:22:22 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 21:22:23 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 21:22:29 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 21:22:30 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 21:22:31 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 21:22:31 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 21:22:31 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 21:22:31 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 21:22:32 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 21:22:32 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 21:22:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 21:22:32 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8f6a01d5a74cef2fe3a1434a8a3d1a4f50b87e22ecbb6dbec751a712d1363496`  
		Last Modified: Tue, 22 Jun 2021 21:23:23 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a05e061614a002dfda954fb22b07c58ae54271515bd01a5d8a8879c35674dfc0`  
		Last Modified: Tue, 22 Jun 2021 21:23:31 GMT  
		Size: 45.0 MB (44971910 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:236bc01cf16d53e19c8ceda24cb9f2114f46f28cc7d1e3aa710718f2238eef2e`  
		Last Modified: Tue, 22 Jun 2021 21:23:23 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:10df2afcd9668c9f59bf8e83826e19c187eae462a35859936d5f7d92ace7ac26`  
		Last Modified: Tue, 22 Jun 2021 21:23:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dbad988e5f82690fcb42f15a367f7565831f561df38407ba7f19e6ce5fb6ef45`  
		Last Modified: Tue, 22 Jun 2021 21:23:23 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.13` - linux; arm variant v6

```console
$ docker pull consul@sha256:36cfc26a5954453c9e232dbca24c2e1ffb972de6a921827b1abca2133ddafb31
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43016212 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:181d5a82a80b8d33afde455da9886addff9dc13122795ad0bd48c36d7aeeaa54`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Tue, 22 Jun 2021 22:20:06 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 22:21:08 GMT
ARG CONSUL_VERSION=1.8.13
# Tue, 22 Jun 2021 22:21:08 GMT
LABEL org.opencontainers.image.version=1.8.13
# Tue, 22 Jun 2021 22:21:09 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 22:21:10 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 22:21:21 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 22:21:23 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 22:21:24 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 22:21:25 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 22:21:25 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 22:21:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 22:21:26 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 22:21:27 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 22:21:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 22:21:28 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0dc1dad5b305fe1b07311ca788f6bbf30c43ba39f6b83451034add65def1ad1d`  
		Last Modified: Tue, 22 Jun 2021 22:23:22 GMT  
		Size: 1.3 KB (1262 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bd6989b5a9d1014551c2b6506d2343e6ff49d0ce65af84cf9a7a73e01806204c`  
		Last Modified: Tue, 22 Jun 2021 22:23:45 GMT  
		Size: 40.4 MB (40390782 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b7d05fdd8f20fe0e87b5aa2615b87073a08bafd29d7242d1ba8693d6da45efa6`  
		Last Modified: Tue, 22 Jun 2021 22:23:22 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:372f00348fdfc4df76ce209111a413c74555aecf3c23dc20641c76bf15a61fbd`  
		Last Modified: Tue, 22 Jun 2021 22:23:23 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9e6e3e6975da54969ea796781cbc957b7d07b1bfcf6de0591c1c7c4af8f01807`  
		Last Modified: Tue, 22 Jun 2021 22:23:23 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.13` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:44b5eb33df4903fe35298f4ab8a6904fde0352bec3ad56df448da2cd3d919ae2
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43217135 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ed4141fa92317ccbaf3d95264134cf46bb0c56051694b3e18b434ab28fe3a8fe`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:25:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 21:43:15 GMT
ARG CONSUL_VERSION=1.8.13
# Tue, 22 Jun 2021 21:43:15 GMT
LABEL org.opencontainers.image.version=1.8.13
# Tue, 22 Jun 2021 21:43:15 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 21:43:16 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 21:43:21 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 21:43:22 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 21:43:23 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 21:43:23 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 21:43:23 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 21:43:24 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 21:43:24 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 21:43:24 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 21:43:24 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 21:43:24 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9a16a3a7536ab5a343392960e9723e88bf9f6c5e223022834a31c803c4cec5ab`  
		Last Modified: Tue, 22 Jun 2021 21:44:24 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:45d55f2e79453b44c942bee27ceb5ced5a5e7d3d8e41715a5976e935877abf6f`  
		Last Modified: Tue, 22 Jun 2021 21:44:31 GMT  
		Size: 40.5 MB (40501815 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98b919304680b669cc6afec8011e667e7e1eecc99890057b679c5820c3a07838`  
		Last Modified: Tue, 22 Jun 2021 21:44:24 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72d6a2acf88f8720710653483a2ada92e63b8ddab80aacd7174b9f10850a42a3`  
		Last Modified: Tue, 22 Jun 2021 21:44:24 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:29cdf13f4d730b3f0a16a5d3d3a4caf6dbad7a7a31523796336ceaa0ea4f0864`  
		Last Modified: Tue, 22 Jun 2021 21:44:24 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.13` - linux; 386

```console
$ docker pull consul@sha256:58c92c1b493df76fc1c012ad6dc555bef1af1069c301098ae8e3bb1acd7bf9f0
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47351813 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bf4fdb52aee73f669f5fdf09e2cb4c50567c13b22d84a001e130d98fd151e36d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 17:39:34 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 21:42:42 GMT
ARG CONSUL_VERSION=1.8.13
# Tue, 22 Jun 2021 21:42:43 GMT
LABEL org.opencontainers.image.version=1.8.13
# Tue, 22 Jun 2021 21:42:43 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 21:42:44 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 21:42:51 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 21:42:52 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 21:42:53 GMT
# ARGS: CONSUL_VERSION=1.8.13
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 21:42:53 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 21:42:54 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 21:42:54 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 21:42:54 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 21:42:54 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 21:42:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 21:42:55 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb42e936a9b8f9402f66e3af766e1ba3f9dadd7e24d85edda954ea5ace08b63d`  
		Last Modified: Tue, 22 Jun 2021 21:44:03 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:23f7c3443d3df24c0db408e1e5aba5df45d3e571682f52d29700fe96b74d5ab1`  
		Last Modified: Tue, 22 Jun 2021 21:44:10 GMT  
		Size: 44.5 MB (44529623 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d513ae58978f46ffd449b76a88acd290bdbbf2c8dc7e90ef9e04014b99d11bf`  
		Last Modified: Tue, 22 Jun 2021 21:43:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4213bb62e786f44e51cf798e925ea48395500839e002338e8bea51c14f45db8b`  
		Last Modified: Tue, 22 Jun 2021 21:43:46 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4b84fb85067e960b52f6852f6b48070c46a5059c36fe7973a2de3886c22f87e9`  
		Last Modified: Tue, 22 Jun 2021 21:44:03 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9`

```console
$ docker pull consul@sha256:0c2a5fc42c9e15abfb59370992fdc2bced7017d6c4199e111e3b14959749b3d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9` - linux; amd64

```console
$ docker pull consul@sha256:2e03e7636733fcea0c690f965ab4c5537417c405a874fb246197e5aa352ab85b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46272673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a575ae275523cd2df1e32173b841d1674d353aa310799f73a74068acf07190da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 18:19:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 21:22:08 GMT
ARG CONSUL_VERSION=1.9.7
# Tue, 22 Jun 2021 21:22:08 GMT
LABEL org.opencontainers.image.version=1.9.7
# Tue, 22 Jun 2021 21:22:08 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 21:22:09 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 21:22:15 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 21:22:16 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 21:22:17 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 21:22:17 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 21:22:18 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 21:22:18 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 21:22:18 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 21:22:18 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 21:22:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 21:22:18 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba5573ab530fd85abc9caba6e40d25b1ffb4d6f1d7cd955d29b0a2b3c236882`  
		Last Modified: Tue, 22 Jun 2021 21:23:07 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ed34482102d7b96044f089577c0c669862bc058576dc8a305b09938b4eb909`  
		Last Modified: Tue, 22 Jun 2021 21:23:13 GMT  
		Size: 43.5 MB (43457411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3756ca2f5bebdaec791db519b75bf966a0c66c691ffd83395e25cd1425e38253`  
		Last Modified: Tue, 22 Jun 2021 21:23:07 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21bbe3129b594b791a9a818533550bbcaa66ea3d06bd580bd9e0b3afbcdd1d17`  
		Last Modified: Tue, 22 Jun 2021 21:23:07 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:035d02d3f8d93835d9aeb64d875679a510338e0752822cfc5888382a7941a264`  
		Last Modified: Tue, 22 Jun 2021 21:23:08 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:00a71dcd3db05546889c7d29a027c3c271edc39a9f2d57b6b1d154ddcd48edf1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41468215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5287da3fd296ac5b1e3086476048647f23d77fb641a394be2696a1e07659a56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Tue, 22 Jun 2021 22:20:06 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 22:20:39 GMT
ARG CONSUL_VERSION=1.9.7
# Tue, 22 Jun 2021 22:20:39 GMT
LABEL org.opencontainers.image.version=1.9.7
# Tue, 22 Jun 2021 22:20:39 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 22:20:41 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 22:20:52 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 22:20:53 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 22:20:55 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 22:20:55 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 22:20:56 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 22:20:56 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 22:20:56 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 22:20:57 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 22:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 22:20:58 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb580a1bee6f74f5f6509a45db9f760d5560852c566c56616ae78ae9f20b0cfa`  
		Last Modified: Tue, 22 Jun 2021 22:22:48 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e982d6d55d69567a42fcad358ba8010949f718a562fee9482fd732c291020a4`  
		Last Modified: Tue, 22 Jun 2021 22:23:10 GMT  
		Size: 38.8 MB (38842789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351444ad7265512ffcb0dc09afdcb8af9467a83d49e9bf5ec82ddda9805774c`  
		Last Modified: Tue, 22 Jun 2021 22:22:48 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0474aeeb7852653399594b7868f4d8b261d970ab8c36e50a91ee3d30380e63ef`  
		Last Modified: Tue, 22 Jun 2021 22:22:48 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ed5ecebc2a6b923cf3a5c587915ef2ea1770a36d36e8467d2cf2ba7f7a6ea`  
		Last Modified: Tue, 22 Jun 2021 22:22:48 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:ccff27b2dea838645fbd528d24e8c5e38ed0dc1793119c8517e190af4770d74d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41737742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4cb9e15a13a6c30e2c9315298f090155d6b459b9c92ac39e1c150e4e0086a3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:25:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 21:43:00 GMT
ARG CONSUL_VERSION=1.9.7
# Tue, 22 Jun 2021 21:43:00 GMT
LABEL org.opencontainers.image.version=1.9.7
# Tue, 22 Jun 2021 21:43:00 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 21:43:01 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 21:43:06 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 21:43:07 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 21:43:08 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 21:43:08 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 21:43:09 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 21:43:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 21:43:09 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 21:43:09 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 21:43:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 21:43:10 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5354e1b2a9e22d5912cc3b168fecc73e887a4a66e29073738322c7aad47dddf`  
		Last Modified: Tue, 22 Jun 2021 21:44:06 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea955f64a1de86ec105e6cf08900c3db9c364d648bb384498237fe61c599fd5`  
		Last Modified: Tue, 22 Jun 2021 21:44:12 GMT  
		Size: 39.0 MB (39022426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7207ea4b65e42fea636ce51f482401be1640bae90ab0ebae26078eb172bf65`  
		Last Modified: Tue, 22 Jun 2021 21:44:07 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d8f6bdfa7e8936d4819c7189d7f1593665e264b117d148598f7d4e5f271c7b`  
		Last Modified: Tue, 22 Jun 2021 21:44:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe66dcc5ee0d12c2ad470d7923f8c4f9dda4951c225094a190a3824ba5c3cf0`  
		Last Modified: Tue, 22 Jun 2021 21:44:06 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; 386

```console
$ docker pull consul@sha256:b2df482a87f79327dac09cc966f41db72ae7ffcf617dd8e8952e9fcc9b6a8004
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45648378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf09fd9c4f2c1a0e21e405ba4ed575dbfcd4f7d78a22476c29127759cee5a3d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 17:39:34 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 21:42:25 GMT
ARG CONSUL_VERSION=1.9.7
# Tue, 22 Jun 2021 21:42:25 GMT
LABEL org.opencontainers.image.version=1.9.7
# Tue, 22 Jun 2021 21:42:25 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 21:42:26 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 21:42:33 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 21:42:34 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 21:42:35 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 21:42:35 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 21:42:35 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 21:42:36 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 21:42:36 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 21:42:36 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 21:42:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 21:42:37 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cab99f845c3f4754bc8e6f6832bf5c55ce1b78a6c8dc1aad63315ad92e6c2fe`  
		Last Modified: Tue, 22 Jun 2021 21:43:43 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5613ecd90355a9b6da78a2020ba81716f207384f2386898e9c6dff3eca13bd31`  
		Last Modified: Tue, 22 Jun 2021 21:43:51 GMT  
		Size: 42.8 MB (42826188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f917c90b746594cb7fbda895c489fdfb16f3710f18cd9be9c30e7900c0ba120a`  
		Last Modified: Tue, 22 Jun 2021 21:43:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c72dfc82386c122a845d5f731994d869d140e08c825e3ddcde2125c220f79c2`  
		Last Modified: Tue, 22 Jun 2021 21:43:43 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa23ad67e6fb237611f71533619af34ecf0dac4efc1a96da766642dbbcf0aa58`  
		Last Modified: Tue, 22 Jun 2021 21:43:43 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9.7`

```console
$ docker pull consul@sha256:0c2a5fc42c9e15abfb59370992fdc2bced7017d6c4199e111e3b14959749b3d6
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9.7` - linux; amd64

```console
$ docker pull consul@sha256:2e03e7636733fcea0c690f965ab4c5537417c405a874fb246197e5aa352ab85b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46272673 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:a575ae275523cd2df1e32173b841d1674d353aa310799f73a74068acf07190da`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 18:19:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 21:22:08 GMT
ARG CONSUL_VERSION=1.9.7
# Tue, 22 Jun 2021 21:22:08 GMT
LABEL org.opencontainers.image.version=1.9.7
# Tue, 22 Jun 2021 21:22:08 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 21:22:09 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 21:22:15 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 21:22:16 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 21:22:17 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 21:22:17 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 21:22:18 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 21:22:18 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 21:22:18 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 21:22:18 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 21:22:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 21:22:18 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1ba5573ab530fd85abc9caba6e40d25b1ffb4d6f1d7cd955d29b0a2b3c236882`  
		Last Modified: Tue, 22 Jun 2021 21:23:07 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:46ed34482102d7b96044f089577c0c669862bc058576dc8a305b09938b4eb909`  
		Last Modified: Tue, 22 Jun 2021 21:23:13 GMT  
		Size: 43.5 MB (43457411 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3756ca2f5bebdaec791db519b75bf966a0c66c691ffd83395e25cd1425e38253`  
		Last Modified: Tue, 22 Jun 2021 21:23:07 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:21bbe3129b594b791a9a818533550bbcaa66ea3d06bd580bd9e0b3afbcdd1d17`  
		Last Modified: Tue, 22 Jun 2021 21:23:07 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:035d02d3f8d93835d9aeb64d875679a510338e0752822cfc5888382a7941a264`  
		Last Modified: Tue, 22 Jun 2021 21:23:08 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.7` - linux; arm variant v6

```console
$ docker pull consul@sha256:00a71dcd3db05546889c7d29a027c3c271edc39a9f2d57b6b1d154ddcd48edf1
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41468215 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e5287da3fd296ac5b1e3086476048647f23d77fb641a394be2696a1e07659a56`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Tue, 22 Jun 2021 22:20:06 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 22:20:39 GMT
ARG CONSUL_VERSION=1.9.7
# Tue, 22 Jun 2021 22:20:39 GMT
LABEL org.opencontainers.image.version=1.9.7
# Tue, 22 Jun 2021 22:20:39 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 22:20:41 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 22:20:52 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 22:20:53 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 22:20:55 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 22:20:55 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 22:20:56 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 22:20:56 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 22:20:56 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 22:20:57 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 22:20:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 22:20:58 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cb580a1bee6f74f5f6509a45db9f760d5560852c566c56616ae78ae9f20b0cfa`  
		Last Modified: Tue, 22 Jun 2021 22:22:48 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e982d6d55d69567a42fcad358ba8010949f718a562fee9482fd732c291020a4`  
		Last Modified: Tue, 22 Jun 2021 22:23:10 GMT  
		Size: 38.8 MB (38842789 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5351444ad7265512ffcb0dc09afdcb8af9467a83d49e9bf5ec82ddda9805774c`  
		Last Modified: Tue, 22 Jun 2021 22:22:48 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0474aeeb7852653399594b7868f4d8b261d970ab8c36e50a91ee3d30380e63ef`  
		Last Modified: Tue, 22 Jun 2021 22:22:48 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:973ed5ecebc2a6b923cf3a5c587915ef2ea1770a36d36e8467d2cf2ba7f7a6ea`  
		Last Modified: Tue, 22 Jun 2021 22:22:48 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.7` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:ccff27b2dea838645fbd528d24e8c5e38ed0dc1793119c8517e190af4770d74d
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41737742 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f4cb9e15a13a6c30e2c9315298f090155d6b459b9c92ac39e1c150e4e0086a3d`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:25:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 21:43:00 GMT
ARG CONSUL_VERSION=1.9.7
# Tue, 22 Jun 2021 21:43:00 GMT
LABEL org.opencontainers.image.version=1.9.7
# Tue, 22 Jun 2021 21:43:00 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 21:43:01 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 21:43:06 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 21:43:07 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 21:43:08 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 21:43:08 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 21:43:09 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 21:43:09 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 21:43:09 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 21:43:09 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 21:43:09 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 21:43:10 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b5354e1b2a9e22d5912cc3b168fecc73e887a4a66e29073738322c7aad47dddf`  
		Last Modified: Tue, 22 Jun 2021 21:44:06 GMT  
		Size: 1.3 KB (1257 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2ea955f64a1de86ec105e6cf08900c3db9c364d648bb384498237fe61c599fd5`  
		Last Modified: Tue, 22 Jun 2021 21:44:12 GMT  
		Size: 39.0 MB (39022426 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8d7207ea4b65e42fea636ce51f482401be1640bae90ab0ebae26078eb172bf65`  
		Last Modified: Tue, 22 Jun 2021 21:44:07 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:97d8f6bdfa7e8936d4819c7189d7f1593665e264b117d148598f7d4e5f271c7b`  
		Last Modified: Tue, 22 Jun 2021 21:44:06 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:dfe66dcc5ee0d12c2ad470d7923f8c4f9dda4951c225094a190a3824ba5c3cf0`  
		Last Modified: Tue, 22 Jun 2021 21:44:06 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.7` - linux; 386

```console
$ docker pull consul@sha256:b2df482a87f79327dac09cc966f41db72ae7ffcf617dd8e8952e9fcc9b6a8004
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45648378 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:cf09fd9c4f2c1a0e21e405ba4ed575dbfcd4f7d78a22476c29127759cee5a3d8`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 17:39:34 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 21:42:25 GMT
ARG CONSUL_VERSION=1.9.7
# Tue, 22 Jun 2021 21:42:25 GMT
LABEL org.opencontainers.image.version=1.9.7
# Tue, 22 Jun 2021 21:42:25 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 21:42:26 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 21:42:33 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 21:42:34 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 21:42:35 GMT
# ARGS: CONSUL_VERSION=1.9.7
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 21:42:35 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 21:42:35 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 21:42:36 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 21:42:36 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 21:42:36 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 21:42:37 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 21:42:37 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8cab99f845c3f4754bc8e6f6832bf5c55ce1b78a6c8dc1aad63315ad92e6c2fe`  
		Last Modified: Tue, 22 Jun 2021 21:43:43 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5613ecd90355a9b6da78a2020ba81716f207384f2386898e9c6dff3eca13bd31`  
		Last Modified: Tue, 22 Jun 2021 21:43:51 GMT  
		Size: 42.8 MB (42826188 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f917c90b746594cb7fbda895c489fdfb16f3710f18cd9be9c30e7900c0ba120a`  
		Last Modified: Tue, 22 Jun 2021 21:43:43 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:2c72dfc82386c122a845d5f731994d869d140e08c825e3ddcde2125c220f79c2`  
		Last Modified: Tue, 22 Jun 2021 21:43:43 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aa23ad67e6fb237611f71533619af34ecf0dac4efc1a96da766642dbbcf0aa58`  
		Last Modified: Tue, 22 Jun 2021 21:43:43 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:c58e1f8d4f13eb4e2155a2830d55380ab3f66d8588e21bb135a75d803975da91
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms:
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:fcc3bc6c30ea40b47e6aa2f491a785965bea5ffcef722c666d1fa3a6949760fe
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43619939 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0846dc12365b73e2ffe2eb25541c30f1580d16b4ed424643f58975f3deae3ab0`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 18:19:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 21:21:54 GMT
ARG CONSUL_VERSION=1.10.0
# Tue, 22 Jun 2021 21:21:54 GMT
LABEL org.opencontainers.image.version=1.10.0
# Tue, 22 Jun 2021 21:21:55 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 21:21:56 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 21:22:01 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 21:22:03 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 21:22:03 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 21:22:04 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 21:22:04 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 21:22:04 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 21:22:04 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 21:22:04 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 21:22:05 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 21:22:05 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98d468a8c3b43256569f9b2b67d51514ec6679816787de88801a10bcb301a709`  
		Last Modified: Tue, 22 Jun 2021 21:22:48 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:105d8515b2215472860538abf77d14b3601cae4b72884d459eefcafbe0e107f4`  
		Last Modified: Tue, 22 Jun 2021 21:22:54 GMT  
		Size: 40.8 MB (40804675 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c0ed6bc2e594daff0582e63eb92f380145f7f303fb4346b05400bb01ab58183e`  
		Last Modified: Tue, 22 Jun 2021 21:22:47 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:a1981893a8c5f7dbc4d2305e2f37dfcfc9d99a71513555ed16fc5bb0ecc39a8e`  
		Last Modified: Tue, 22 Jun 2021 21:22:47 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:72b39d63083e8e2e70c8f000ac9b0828b61cecd954468d8f28a51358010ce881`  
		Last Modified: Tue, 22 Jun 2021 21:22:48 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:20576537c4a0095923c8b23fe3aadc07c2cd0a828cfb467a4b499ddde6015b2b
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39630159 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:66a717761a11b7d16aac6a950fe0f8017e3c54b4856141b27d6335d8be3fd97b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Tue, 22 Jun 2021 22:20:06 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 22:20:06 GMT
ARG CONSUL_VERSION=1.10.0
# Tue, 22 Jun 2021 22:20:07 GMT
LABEL org.opencontainers.image.version=1.10.0
# Tue, 22 Jun 2021 22:20:07 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 22:20:08 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 22:20:21 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 22:20:23 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 22:20:24 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 22:20:25 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 22:20:25 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 22:20:26 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 22:20:26 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 22:20:27 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 22:20:27 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 22:20:27 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c07d1eb174fc9249548c4b20da900dc348680f32d74676f33dd0951274dff98b`  
		Last Modified: Tue, 22 Jun 2021 22:22:10 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4881247682906d151dd4266dc1f16b3787c3782e123136a9d9174f81f6d6e250`  
		Last Modified: Tue, 22 Jun 2021 22:22:32 GMT  
		Size: 37.0 MB (37004734 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c8eb296fb8741f925b4e9a4bdd8d5f57d707bee2e71bcb95f8842b461902ac9b`  
		Last Modified: Tue, 22 Jun 2021 22:22:10 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ef0ff50377a85d926a7616c0ab6a4f499e49182fcbb508697866678c3e1ea1bf`  
		Last Modified: Tue, 22 Jun 2021 22:22:10 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:20660d5b18ed07b69136dc58b3b854487ca3faa30c30d2320fd6ab0ffca7988b`  
		Last Modified: Tue, 22 Jun 2021 22:22:10 GMT  
		Size: 1.7 KB (1709 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:1a8038945ebb4d2983fe5aea38f8b676e45d432efabbb785a678d4d45e57a760
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39576123 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:dc2005a537b1b2d018ef3390c27e06be8ac9e9a65f06e01cff0f193a987a110f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:25:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 21:42:45 GMT
ARG CONSUL_VERSION=1.10.0
# Tue, 22 Jun 2021 21:42:45 GMT
LABEL org.opencontainers.image.version=1.10.0
# Tue, 22 Jun 2021 21:42:45 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 21:42:46 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 21:42:51 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 21:42:52 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 21:42:53 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 21:42:53 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 21:42:53 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 21:42:53 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 21:42:54 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 21:42:54 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 21:42:54 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 21:42:54 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9f3d1412f415f7d8fd08f4f596252a334bea5a112509304795c9242b32e30e3d`  
		Last Modified: Tue, 22 Jun 2021 21:43:46 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:38ca6286d3fe33aae8a5881ad0fc09d3e13850fb1a3984d67261199b1d8db56b`  
		Last Modified: Tue, 22 Jun 2021 21:43:51 GMT  
		Size: 36.9 MB (36860805 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d513ae58978f46ffd449b76a88acd290bdbbf2c8dc7e90ef9e04014b99d11bf`  
		Last Modified: Tue, 22 Jun 2021 21:43:46 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4213bb62e786f44e51cf798e925ea48395500839e002338e8bea51c14f45db8b`  
		Last Modified: Tue, 22 Jun 2021 21:43:46 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:34b6bb821282f46b639f0ce35010cdaf11df4a929186515888a6c73479439af1`  
		Last Modified: Tue, 22 Jun 2021 21:43:46 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:265f8bd3a47c18087b52ce60c3d1e40631f2199891a6039f6666ba4c13f12ddd
```

-	Docker Version: 19.03.12
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (42986555 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:5a54f4d554dc437bf70ce8efa661163bb6233eb6f20c3a031c3fabf6f09bc99b`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 17:39:34 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Tue, 22 Jun 2021 21:42:06 GMT
ARG CONSUL_VERSION=1.10.0
# Tue, 22 Jun 2021 21:42:07 GMT
LABEL org.opencontainers.image.version=1.10.0
# Tue, 22 Jun 2021 21:42:07 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Tue, 22 Jun 2021 21:42:08 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN addgroup consul &&     adduser -S -G consul consul
# Tue, 22 Jun 2021 21:42:15 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Tue, 22 Jun 2021 21:42:16 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Tue, 22 Jun 2021 21:42:17 GMT
# ARGS: CONSUL_VERSION=1.10.0
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Tue, 22 Jun 2021 21:42:17 GMT
VOLUME [/consul/data]
# Tue, 22 Jun 2021 21:42:17 GMT
EXPOSE 8300
# Tue, 22 Jun 2021 21:42:18 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Tue, 22 Jun 2021 21:42:18 GMT
EXPOSE 8500 8600 8600/udp
# Tue, 22 Jun 2021 21:42:18 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Tue, 22 Jun 2021 21:42:18 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Tue, 22 Jun 2021 21:42:18 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0fe0317095bb660706913746e0261e794f76eb1ae5ad739c83f672b50efe65ae`  
		Last Modified: Tue, 22 Jun 2021 21:43:19 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9fadc1c405e1df51949be3115d7235c9ca7520b4eefa0e9c508716a02c910907`  
		Last Modified: Tue, 22 Jun 2021 21:43:27 GMT  
		Size: 40.2 MB (40164364 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f2ecaad2c81fb77d29ad853f94b04a020c3266a11823d0a2883ae69dc84e01a9`  
		Last Modified: Tue, 22 Jun 2021 21:43:19 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9d51ffce497a34f282fc5ebcc0d250873137530d051b74260446222831b2c45e`  
		Last Modified: Tue, 22 Jun 2021 21:43:20 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e4d5d813d3765868039b456e2edcf9ab175b0f7c836c532118ca67a42357d7ac`  
		Last Modified: Tue, 22 Jun 2021 21:43:19 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
