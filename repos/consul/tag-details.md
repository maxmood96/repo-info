<!-- THIS FILE IS GENERATED VIA './update-remote.sh' -->

# Tags of `consul`

-	[`consul:1.10`](#consul110)
-	[`consul:1.10.1`](#consul1101)
-	[`consul:1.8`](#consul18)
-	[`consul:1.8.14`](#consul1814)
-	[`consul:1.9`](#consul19)
-	[`consul:1.9.8`](#consul198)
-	[`consul:latest`](#consullatest)

## `consul:1.10`

```console
$ docker pull consul@sha256:bccf8b08716e4bba6a36e39ff4659f4dc3d5d8b09f3ef7637d3a74b16ebde1e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10` - linux; amd64

```console
$ docker pull consul@sha256:1015ee4f222a938f3dc0e6e34b877670ff7296fabca12da671134b6d7d5995ea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43616392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f67cdd31f475de3882de8424e6796b404318c4ce3950c85ce4111b193f1a57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 18:19:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 12:49:54 GMT
ARG CONSUL_VERSION=1.10.1
# Fri, 23 Jul 2021 12:49:54 GMT
LABEL org.opencontainers.image.version=1.10.1
# Fri, 23 Jul 2021 12:49:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 12:49:56 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 12:50:04 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 12:50:06 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 12:50:07 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 12:50:08 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 12:50:08 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 12:50:08 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 12:50:09 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 12:50:09 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 12:50:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 12:50:10 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26219d328d3fceaa00722bf08b5b25052b3e0da4c15a6a77e1df9204a732de65`  
		Last Modified: Fri, 23 Jul 2021 12:51:01 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82ba3ce598354d1d1e9db209d6cefd802bae11112cc179b77cf361e9407c206`  
		Last Modified: Fri, 23 Jul 2021 12:51:07 GMT  
		Size: 40.8 MB (40801130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c403ab9c506f25ff589ed067c1f5553eabb4f3ba88f0cd0811b73e3732efcb09`  
		Last Modified: Fri, 23 Jul 2021 12:51:01 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3262b670efeeb779978bb086dbdc65962fac2f24282d2bc6a93f5456789949f2`  
		Last Modified: Fri, 23 Jul 2021 12:51:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e27d156c018aa365cae675cafe23837e07e696080fc7f770846623e5afa7eb`  
		Last Modified: Fri, 23 Jul 2021 12:51:01 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm variant v6

```console
$ docker pull consul@sha256:3f082cca98db7926582f9515e88bf2a38179feb7fdb0e43be6e75c00179a77cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39643432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0034be4ee660d9bf8d533babeb45de88f429ff749a4f9d2f26de431981c9d3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Tue, 22 Jun 2021 22:20:06 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 00:49:35 GMT
ARG CONSUL_VERSION=1.10.1
# Fri, 23 Jul 2021 00:49:35 GMT
LABEL org.opencontainers.image.version=1.10.1
# Fri, 23 Jul 2021 00:49:36 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 00:49:37 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 00:49:49 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 00:49:51 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 00:49:53 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 00:49:53 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 00:49:54 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 00:49:54 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 00:49:55 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 00:49:55 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 00:49:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 00:49:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc6805d20d4c45130ef58bfb2cd523ba3651adb7ed2aaad70c3b90d01064e72`  
		Last Modified: Fri, 23 Jul 2021 00:51:45 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9383569f273b7844f640f683fe66020085aba3e2aa266e4895a248aadbe1fd5f`  
		Last Modified: Fri, 23 Jul 2021 00:52:04 GMT  
		Size: 37.0 MB (37018011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea73ba318055a5182ac6934e8403229cc6797fa9b99233d5f9c01a180c3d82b4`  
		Last Modified: Fri, 23 Jul 2021 00:51:45 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a41f8b1035ff81249e1fda4ab3c1e663c24468c7fcef7c0259ae6468fbdc1b0`  
		Last Modified: Fri, 23 Jul 2021 00:51:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae4c8a9ec3ba9260ff2f6627b889cc8c60f7fdd1742b08557df4ddab6d8a7c8`  
		Last Modified: Fri, 23 Jul 2021 00:51:45 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:0081f4b20a6b484746ee30b2ede4f64241d94721c18b9c115ce61b88ca6588d2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39585136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945c65b74aabe05fbf0444ae754a6cf8bea788f8854c719189eecb6501793f52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:25:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 04:19:33 GMT
ARG CONSUL_VERSION=1.10.1
# Fri, 23 Jul 2021 04:19:33 GMT
LABEL org.opencontainers.image.version=1.10.1
# Fri, 23 Jul 2021 04:19:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 04:19:34 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 04:19:39 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 04:19:40 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 04:19:41 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 04:19:41 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 04:19:41 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 04:19:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 04:19:42 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 04:19:42 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 04:19:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 04:19:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec0bca027d4ed5928a09c462f06be2502d9e6dfd78d9ba3c527dc500cfcdfca`  
		Last Modified: Fri, 23 Jul 2021 04:20:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b3128d8785d803695d60c92ef9482ab1ddc021eeb844a226ba40208ccb0a54`  
		Last Modified: Fri, 23 Jul 2021 04:20:40 GMT  
		Size: 36.9 MB (36869818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbf322ffab66a9b685be5eb28cf5499c409303c57282a74d1c3c7380cf2f5f7`  
		Last Modified: Fri, 23 Jul 2021 04:20:34 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117f3c6fd6c3e6a3b608722cdf776c98efb4d2ab2be357bf99716b7e6f5e8343`  
		Last Modified: Fri, 23 Jul 2021 04:20:34 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418597e612cf3477bacd0c9730131f6a619802a05c2a5c37081550ec54fc2c60`  
		Last Modified: Fri, 23 Jul 2021 04:20:34 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10` - linux; 386

```console
$ docker pull consul@sha256:2253be5b7743047f15f8c0109a10e9df6c93331fc5d6d94bda29ec8aabf2e4c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (42993107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78083beb7456bcda3cdb6aeede0c945c374b4aa9b892836e46bab41c72c2eb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 17:39:34 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 04:13:44 GMT
ARG CONSUL_VERSION=1.10.1
# Fri, 23 Jul 2021 04:13:44 GMT
LABEL org.opencontainers.image.version=1.10.1
# Fri, 23 Jul 2021 04:13:44 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 04:13:45 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 04:13:52 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 04:13:54 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 04:13:55 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 04:13:55 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 04:13:55 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 04:13:55 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 04:13:56 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 04:13:56 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 04:13:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 04:13:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adae4dec86708fea7cb8b325f7ebbcd0ad7a355b0f12baafec74e19df9a4dc`  
		Last Modified: Fri, 23 Jul 2021 04:14:59 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfb9688831a6804e0ec0506100817e3550bdb499ad92c471c079f88bfa0a89f`  
		Last Modified: Fri, 23 Jul 2021 04:15:05 GMT  
		Size: 40.2 MB (40170917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e976b32b9c325b1e22a08c36e3bdfd3b9dec8c36f46272eb0389cc3d8a809695`  
		Last Modified: Fri, 23 Jul 2021 04:14:59 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe31b1e9a61cda7f0af1eafa67a2f6c07229a0135fa0c969f9c4acb45f907eca`  
		Last Modified: Fri, 23 Jul 2021 04:14:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b946799757bca26ba4264cb8891b48feceaa6c8646856330b320b6d012b491`  
		Last Modified: Fri, 23 Jul 2021 04:14:59 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.10.1`

```console
$ docker pull consul@sha256:bccf8b08716e4bba6a36e39ff4659f4dc3d5d8b09f3ef7637d3a74b16ebde1e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.10.1` - linux; amd64

```console
$ docker pull consul@sha256:1015ee4f222a938f3dc0e6e34b877670ff7296fabca12da671134b6d7d5995ea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43616392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f67cdd31f475de3882de8424e6796b404318c4ce3950c85ce4111b193f1a57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 18:19:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 12:49:54 GMT
ARG CONSUL_VERSION=1.10.1
# Fri, 23 Jul 2021 12:49:54 GMT
LABEL org.opencontainers.image.version=1.10.1
# Fri, 23 Jul 2021 12:49:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 12:49:56 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 12:50:04 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 12:50:06 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 12:50:07 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 12:50:08 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 12:50:08 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 12:50:08 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 12:50:09 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 12:50:09 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 12:50:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 12:50:10 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26219d328d3fceaa00722bf08b5b25052b3e0da4c15a6a77e1df9204a732de65`  
		Last Modified: Fri, 23 Jul 2021 12:51:01 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82ba3ce598354d1d1e9db209d6cefd802bae11112cc179b77cf361e9407c206`  
		Last Modified: Fri, 23 Jul 2021 12:51:07 GMT  
		Size: 40.8 MB (40801130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c403ab9c506f25ff589ed067c1f5553eabb4f3ba88f0cd0811b73e3732efcb09`  
		Last Modified: Fri, 23 Jul 2021 12:51:01 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3262b670efeeb779978bb086dbdc65962fac2f24282d2bc6a93f5456789949f2`  
		Last Modified: Fri, 23 Jul 2021 12:51:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e27d156c018aa365cae675cafe23837e07e696080fc7f770846623e5afa7eb`  
		Last Modified: Fri, 23 Jul 2021 12:51:01 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.1` - linux; arm variant v6

```console
$ docker pull consul@sha256:3f082cca98db7926582f9515e88bf2a38179feb7fdb0e43be6e75c00179a77cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39643432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0034be4ee660d9bf8d533babeb45de88f429ff749a4f9d2f26de431981c9d3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Tue, 22 Jun 2021 22:20:06 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 00:49:35 GMT
ARG CONSUL_VERSION=1.10.1
# Fri, 23 Jul 2021 00:49:35 GMT
LABEL org.opencontainers.image.version=1.10.1
# Fri, 23 Jul 2021 00:49:36 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 00:49:37 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 00:49:49 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 00:49:51 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 00:49:53 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 00:49:53 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 00:49:54 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 00:49:54 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 00:49:55 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 00:49:55 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 00:49:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 00:49:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc6805d20d4c45130ef58bfb2cd523ba3651adb7ed2aaad70c3b90d01064e72`  
		Last Modified: Fri, 23 Jul 2021 00:51:45 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9383569f273b7844f640f683fe66020085aba3e2aa266e4895a248aadbe1fd5f`  
		Last Modified: Fri, 23 Jul 2021 00:52:04 GMT  
		Size: 37.0 MB (37018011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea73ba318055a5182ac6934e8403229cc6797fa9b99233d5f9c01a180c3d82b4`  
		Last Modified: Fri, 23 Jul 2021 00:51:45 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a41f8b1035ff81249e1fda4ab3c1e663c24468c7fcef7c0259ae6468fbdc1b0`  
		Last Modified: Fri, 23 Jul 2021 00:51:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae4c8a9ec3ba9260ff2f6627b889cc8c60f7fdd1742b08557df4ddab6d8a7c8`  
		Last Modified: Fri, 23 Jul 2021 00:51:45 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.1` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:0081f4b20a6b484746ee30b2ede4f64241d94721c18b9c115ce61b88ca6588d2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39585136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945c65b74aabe05fbf0444ae754a6cf8bea788f8854c719189eecb6501793f52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:25:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 04:19:33 GMT
ARG CONSUL_VERSION=1.10.1
# Fri, 23 Jul 2021 04:19:33 GMT
LABEL org.opencontainers.image.version=1.10.1
# Fri, 23 Jul 2021 04:19:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 04:19:34 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 04:19:39 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 04:19:40 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 04:19:41 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 04:19:41 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 04:19:41 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 04:19:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 04:19:42 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 04:19:42 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 04:19:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 04:19:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec0bca027d4ed5928a09c462f06be2502d9e6dfd78d9ba3c527dc500cfcdfca`  
		Last Modified: Fri, 23 Jul 2021 04:20:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b3128d8785d803695d60c92ef9482ab1ddc021eeb844a226ba40208ccb0a54`  
		Last Modified: Fri, 23 Jul 2021 04:20:40 GMT  
		Size: 36.9 MB (36869818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbf322ffab66a9b685be5eb28cf5499c409303c57282a74d1c3c7380cf2f5f7`  
		Last Modified: Fri, 23 Jul 2021 04:20:34 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117f3c6fd6c3e6a3b608722cdf776c98efb4d2ab2be357bf99716b7e6f5e8343`  
		Last Modified: Fri, 23 Jul 2021 04:20:34 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418597e612cf3477bacd0c9730131f6a619802a05c2a5c37081550ec54fc2c60`  
		Last Modified: Fri, 23 Jul 2021 04:20:34 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.10.1` - linux; 386

```console
$ docker pull consul@sha256:2253be5b7743047f15f8c0109a10e9df6c93331fc5d6d94bda29ec8aabf2e4c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (42993107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78083beb7456bcda3cdb6aeede0c945c374b4aa9b892836e46bab41c72c2eb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 17:39:34 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 04:13:44 GMT
ARG CONSUL_VERSION=1.10.1
# Fri, 23 Jul 2021 04:13:44 GMT
LABEL org.opencontainers.image.version=1.10.1
# Fri, 23 Jul 2021 04:13:44 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 04:13:45 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 04:13:52 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 04:13:54 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 04:13:55 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 04:13:55 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 04:13:55 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 04:13:55 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 04:13:56 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 04:13:56 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 04:13:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 04:13:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adae4dec86708fea7cb8b325f7ebbcd0ad7a355b0f12baafec74e19df9a4dc`  
		Last Modified: Fri, 23 Jul 2021 04:14:59 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfb9688831a6804e0ec0506100817e3550bdb499ad92c471c079f88bfa0a89f`  
		Last Modified: Fri, 23 Jul 2021 04:15:05 GMT  
		Size: 40.2 MB (40170917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e976b32b9c325b1e22a08c36e3bdfd3b9dec8c36f46272eb0389cc3d8a809695`  
		Last Modified: Fri, 23 Jul 2021 04:14:59 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe31b1e9a61cda7f0af1eafa67a2f6c07229a0135fa0c969f9c4acb45f907eca`  
		Last Modified: Fri, 23 Jul 2021 04:14:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b946799757bca26ba4264cb8891b48feceaa6c8646856330b320b6d012b491`  
		Last Modified: Fri, 23 Jul 2021 04:14:59 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8`

```console
$ docker pull consul@sha256:82cb9df316e6ac32bba6870f19ac898944ff73d4769ae422d554f2d88fd18941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8` - linux; amd64

```console
$ docker pull consul@sha256:ee67369ee3fc67a306e88acfd8d38c6784163e8352be66d3eee4b6a2a1a7975a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47799496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22732ca68ebce2f6504636e10d5a966246b85c814eb728e44c5ff9deca655b46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 18:19:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 12:50:34 GMT
ARG CONSUL_VERSION=1.8.14
# Fri, 23 Jul 2021 12:50:35 GMT
LABEL org.opencontainers.image.version=1.8.14
# Fri, 23 Jul 2021 12:50:35 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 12:50:36 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 12:50:42 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 12:50:43 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 12:50:44 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 12:50:44 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 12:50:44 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 12:50:45 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 12:50:45 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 12:50:45 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 12:50:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 12:50:45 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651a6becf6db5ac5a164c41d3dd004a70f1c83629c8572144a504f6e2544d61a`  
		Last Modified: Fri, 23 Jul 2021 12:51:41 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e97db18dd873140a56a1f621af36ccc0112d173a065419c88fa9cc8df43e9d`  
		Last Modified: Fri, 23 Jul 2021 12:51:54 GMT  
		Size: 45.0 MB (44984234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3b888f4d8e404f393a4bbed55506b687e5e6ee6041b297346f1a6a9f79bd73`  
		Last Modified: Fri, 23 Jul 2021 12:51:41 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e29ab8e98a79e0f2061c24e17d273c4a409c16cd5e861fb469fbe986ca52e26`  
		Last Modified: Fri, 23 Jul 2021 12:51:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af768cc301fecd59f95f514b2fe667d26d0bad7455863282ba1206035176e58`  
		Last Modified: Fri, 23 Jul 2021 12:51:41 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm variant v6

```console
$ docker pull consul@sha256:43c970d2687b14e96828040b4bef690a546e19d0496bbf9575e890ec63bedb4c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43016996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7719b70438f93bcb3aca003c8d808521b643d6a68e89fd2654839c18871d26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Tue, 22 Jun 2021 22:20:06 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 00:50:39 GMT
ARG CONSUL_VERSION=1.8.14
# Fri, 23 Jul 2021 00:50:39 GMT
LABEL org.opencontainers.image.version=1.8.14
# Fri, 23 Jul 2021 00:50:40 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 00:50:42 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 00:50:54 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 00:50:56 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 00:50:58 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 00:50:58 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 00:50:58 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 00:50:59 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 00:50:59 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 00:51:00 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 00:51:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 00:51:01 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55481094b9c37d4dc92b75d55f849e3ec02fcb1352091dfb01ca6993bc0da2b`  
		Last Modified: Fri, 23 Jul 2021 00:52:54 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15357fe2cb7898f669fec0152fa518ddbb818f10a232a3165814d0b275f2f48a`  
		Last Modified: Fri, 23 Jul 2021 00:53:15 GMT  
		Size: 40.4 MB (40391571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cb9d0bb23cf73f453fc3424ed91839972926624ae15e44ad93a41f8a761ce4`  
		Last Modified: Fri, 23 Jul 2021 00:52:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d553ccd7892098587d114f76b87c132e2e9be7c0019c559c328b0ccbf14b208d`  
		Last Modified: Fri, 23 Jul 2021 00:52:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bcde50477d05ef378445e22036cf2864127ec92339f23c04ba1c32e10f1664`  
		Last Modified: Fri, 23 Jul 2021 00:52:54 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:c37cd7c096c4a934d7095ba5dbe5b05d8841aebeeb47afd80b7cce3104b235b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43230586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0cfde2c2c6d82ab2b74b9594be5f5f58d648747649a329cdcc46694d93f8144`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:25:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 04:20:02 GMT
ARG CONSUL_VERSION=1.8.14
# Fri, 23 Jul 2021 04:20:03 GMT
LABEL org.opencontainers.image.version=1.8.14
# Fri, 23 Jul 2021 04:20:03 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 04:20:03 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 04:20:08 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 04:20:09 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 04:20:10 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 04:20:10 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 04:20:10 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 04:20:11 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 04:20:11 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 04:20:11 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 04:20:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 04:20:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2cc36a972be65ab045851033f56e745ea4f4678929bce70330e8af9769a6de`  
		Last Modified: Fri, 23 Jul 2021 04:21:13 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98890b27f5655b4e3c19e344c6b9a207eba9ed9001964fe7b3fdc0cbffe2675c`  
		Last Modified: Fri, 23 Jul 2021 04:21:19 GMT  
		Size: 40.5 MB (40515268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94ee3335668307662b7979c8f5823acbe7721dc8ee8ca6aaf811fdbf98aa9f5`  
		Last Modified: Fri, 23 Jul 2021 04:21:12 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ac26ba2e3632a67ccf90d5d45b54ffa2524c9e9cfb7f2c39d98cfc3af61f60`  
		Last Modified: Fri, 23 Jul 2021 04:21:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc5a760885ea0a6fbb9d790eca5c1b90b5def97ab9b489273e8bc37173f4170`  
		Last Modified: Fri, 23 Jul 2021 04:21:13 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8` - linux; 386

```console
$ docker pull consul@sha256:d042b1ee5d0bef78590cf9204c2724f03dc6173ace399652e8d5729129642b3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47362530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179495a44e182055f8972be98da90704e37efc6734e89ed7de2902e309505379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 17:39:34 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 04:14:19 GMT
ARG CONSUL_VERSION=1.8.14
# Fri, 23 Jul 2021 04:14:20 GMT
LABEL org.opencontainers.image.version=1.8.14
# Fri, 23 Jul 2021 04:14:20 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 04:14:21 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 04:14:28 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 04:14:30 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 04:14:31 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 04:14:31 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 04:14:31 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 04:14:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 04:14:32 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 04:14:32 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 04:14:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 04:14:33 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3393e9f609169db67f6586669f2a6a31f824cb7b9a70ce776bfc254d8824d71`  
		Last Modified: Fri, 23 Jul 2021 04:15:42 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c625c0e39f6b9ab0228b7ad831b593993873b0fc967685d7d3054ad3f9d549`  
		Last Modified: Fri, 23 Jul 2021 04:15:50 GMT  
		Size: 44.5 MB (44540338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05db9125fb1a6eb2452820bf00890e319a7efc4be82ecb5da479b763eddacc6`  
		Last Modified: Fri, 23 Jul 2021 04:15:42 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85bb1b5cc084848808fa841c06104ae9c045605408658e10f5b765c6a08caf5`  
		Last Modified: Fri, 23 Jul 2021 04:15:42 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9798c93e0ee488d0c9ac37c47ab83dd6439390812d9e7c6c56db78d3989637`  
		Last Modified: Fri, 23 Jul 2021 04:15:42 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.8.14`

```console
$ docker pull consul@sha256:82cb9df316e6ac32bba6870f19ac898944ff73d4769ae422d554f2d88fd18941
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.8.14` - linux; amd64

```console
$ docker pull consul@sha256:ee67369ee3fc67a306e88acfd8d38c6784163e8352be66d3eee4b6a2a1a7975a
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.8 MB (47799496 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22732ca68ebce2f6504636e10d5a966246b85c814eb728e44c5ff9deca655b46`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 18:19:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 12:50:34 GMT
ARG CONSUL_VERSION=1.8.14
# Fri, 23 Jul 2021 12:50:35 GMT
LABEL org.opencontainers.image.version=1.8.14
# Fri, 23 Jul 2021 12:50:35 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 12:50:36 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 12:50:42 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 12:50:43 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 12:50:44 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 12:50:44 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 12:50:44 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 12:50:45 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 12:50:45 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 12:50:45 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 12:50:45 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 12:50:45 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:651a6becf6db5ac5a164c41d3dd004a70f1c83629c8572144a504f6e2544d61a`  
		Last Modified: Fri, 23 Jul 2021 12:51:41 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c5e97db18dd873140a56a1f621af36ccc0112d173a065419c88fa9cc8df43e9d`  
		Last Modified: Fri, 23 Jul 2021 12:51:54 GMT  
		Size: 45.0 MB (44984234 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ba3b888f4d8e404f393a4bbed55506b687e5e6ee6041b297346f1a6a9f79bd73`  
		Last Modified: Fri, 23 Jul 2021 12:51:41 GMT  
		Size: 175.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8e29ab8e98a79e0f2061c24e17d273c4a409c16cd5e861fb469fbe986ca52e26`  
		Last Modified: Fri, 23 Jul 2021 12:51:41 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5af768cc301fecd59f95f514b2fe667d26d0bad7455863282ba1206035176e58`  
		Last Modified: Fri, 23 Jul 2021 12:51:41 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.14` - linux; arm variant v6

```console
$ docker pull consul@sha256:43c970d2687b14e96828040b4bef690a546e19d0496bbf9575e890ec63bedb4c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (43016996 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:bb7719b70438f93bcb3aca003c8d808521b643d6a68e89fd2654839c18871d26`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Tue, 22 Jun 2021 22:20:06 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 00:50:39 GMT
ARG CONSUL_VERSION=1.8.14
# Fri, 23 Jul 2021 00:50:39 GMT
LABEL org.opencontainers.image.version=1.8.14
# Fri, 23 Jul 2021 00:50:40 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 00:50:42 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 00:50:54 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 00:50:56 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 00:50:58 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 00:50:58 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 00:50:58 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 00:50:59 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 00:50:59 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 00:51:00 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 00:51:00 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 00:51:01 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f55481094b9c37d4dc92b75d55f849e3ec02fcb1352091dfb01ca6993bc0da2b`  
		Last Modified: Fri, 23 Jul 2021 00:52:54 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:15357fe2cb7898f669fec0152fa518ddbb818f10a232a3165814d0b275f2f48a`  
		Last Modified: Fri, 23 Jul 2021 00:53:15 GMT  
		Size: 40.4 MB (40391571 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:50cb9d0bb23cf73f453fc3424ed91839972926624ae15e44ad93a41f8a761ce4`  
		Last Modified: Fri, 23 Jul 2021 00:52:54 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d553ccd7892098587d114f76b87c132e2e9be7c0019c559c328b0ccbf14b208d`  
		Last Modified: Fri, 23 Jul 2021 00:52:54 GMT  
		Size: 155.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:75bcde50477d05ef378445e22036cf2864127ec92339f23c04ba1c32e10f1664`  
		Last Modified: Fri, 23 Jul 2021 00:52:54 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.14` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:c37cd7c096c4a934d7095ba5dbe5b05d8841aebeeb47afd80b7cce3104b235b4
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.2 MB (43230586 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:d0cfde2c2c6d82ab2b74b9594be5f5f58d648747649a329cdcc46694d93f8144`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:25:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 04:20:02 GMT
ARG CONSUL_VERSION=1.8.14
# Fri, 23 Jul 2021 04:20:03 GMT
LABEL org.opencontainers.image.version=1.8.14
# Fri, 23 Jul 2021 04:20:03 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 04:20:03 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 04:20:08 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 04:20:09 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 04:20:10 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 04:20:10 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 04:20:10 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 04:20:11 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 04:20:11 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 04:20:11 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 04:20:11 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 04:20:11 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:cd2cc36a972be65ab045851033f56e745ea4f4678929bce70330e8af9769a6de`  
		Last Modified: Fri, 23 Jul 2021 04:21:13 GMT  
		Size: 1.3 KB (1259 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:98890b27f5655b4e3c19e344c6b9a207eba9ed9001964fe7b3fdc0cbffe2675c`  
		Last Modified: Fri, 23 Jul 2021 04:21:19 GMT  
		Size: 40.5 MB (40515268 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b94ee3335668307662b7979c8f5823acbe7721dc8ee8ca6aaf811fdbf98aa9f5`  
		Last Modified: Fri, 23 Jul 2021 04:21:12 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:88ac26ba2e3632a67ccf90d5d45b54ffa2524c9e9cfb7f2c39d98cfc3af61f60`  
		Last Modified: Fri, 23 Jul 2021 04:21:13 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:4bc5a760885ea0a6fbb9d790eca5c1b90b5def97ab9b489273e8bc37173f4170`  
		Last Modified: Fri, 23 Jul 2021 04:21:13 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.8.14` - linux; 386

```console
$ docker pull consul@sha256:d042b1ee5d0bef78590cf9204c2724f03dc6173ace399652e8d5729129642b3c
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **47.4 MB (47362530 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:179495a44e182055f8972be98da90704e37efc6734e89ed7de2902e309505379`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 17:39:34 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 04:14:19 GMT
ARG CONSUL_VERSION=1.8.14
# Fri, 23 Jul 2021 04:14:20 GMT
LABEL org.opencontainers.image.version=1.8.14
# Fri, 23 Jul 2021 04:14:20 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 04:14:21 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 04:14:28 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 04:14:30 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 04:14:31 GMT
# ARGS: CONSUL_VERSION=1.8.14
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 04:14:31 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 04:14:31 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 04:14:32 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 04:14:32 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 04:14:32 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 04:14:32 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 04:14:33 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e3393e9f609169db67f6586669f2a6a31f824cb7b9a70ce776bfc254d8824d71`  
		Last Modified: Fri, 23 Jul 2021 04:15:42 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:19c625c0e39f6b9ab0228b7ad831b593993873b0fc967685d7d3054ad3f9d549`  
		Last Modified: Fri, 23 Jul 2021 04:15:50 GMT  
		Size: 44.5 MB (44540338 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f05db9125fb1a6eb2452820bf00890e319a7efc4be82ecb5da479b763eddacc6`  
		Last Modified: Fri, 23 Jul 2021 04:15:42 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e85bb1b5cc084848808fa841c06104ae9c045605408658e10f5b765c6a08caf5`  
		Last Modified: Fri, 23 Jul 2021 04:15:42 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ca9798c93e0ee488d0c9ac37c47ab83dd6439390812d9e7c6c56db78d3989637`  
		Last Modified: Fri, 23 Jul 2021 04:15:42 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9`

```console
$ docker pull consul@sha256:9b538a4f12f7a794ca64653ac4ec3e45bfcfe58f46875def350f4bf7937f9cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9` - linux; amd64

```console
$ docker pull consul@sha256:3fbc18b4872358beb7d4d865a17065cd84c08afb5dd4056b6240afdc67583f55
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46282347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b061e6d43eaa3e1216fd483c362d3839083808590e3d3cbfe0876536731515`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 18:19:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 12:50:15 GMT
ARG CONSUL_VERSION=1.9.8
# Fri, 23 Jul 2021 12:50:16 GMT
LABEL org.opencontainers.image.version=1.9.8
# Fri, 23 Jul 2021 12:50:16 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 12:50:18 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 12:50:26 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 12:50:27 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 12:50:28 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 12:50:28 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 12:50:28 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 12:50:29 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 12:50:29 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 12:50:29 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 12:50:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 12:50:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f76215166e54053f91e087f5a3160cd21a34c6b57813d3a4e2631c8cd127f50`  
		Last Modified: Fri, 23 Jul 2021 12:51:22 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44e99d3c78a9289b48645fea3c7125101e1ab00b2b7ef496dd9f77a2e64223a`  
		Last Modified: Fri, 23 Jul 2021 12:51:30 GMT  
		Size: 43.5 MB (43467082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016a11d5b82044a80cd059e23a0518affdc87ca15281ae4a8518e3103b9574ea`  
		Last Modified: Fri, 23 Jul 2021 12:51:22 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78844cc5afba4bac56e78565001eaae6315e68605e18aaea429b25956257704a`  
		Last Modified: Fri, 23 Jul 2021 12:51:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc080c1f2f03be33b72e89dc0efb4f689915d0cc4053fec0216d5a19e9ff5076`  
		Last Modified: Fri, 23 Jul 2021 12:51:22 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm variant v6

```console
$ docker pull consul@sha256:22194daf3f35cc4686ee999f1fcd82981c23aa0f7162001e0761ae0ac3577455
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41466717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c7d2796ebb8463c14f4a36e44fa5efdecbb12f4ef51236368989942b5eebba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Tue, 22 Jun 2021 22:20:06 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 00:50:08 GMT
ARG CONSUL_VERSION=1.9.8
# Fri, 23 Jul 2021 00:50:08 GMT
LABEL org.opencontainers.image.version=1.9.8
# Fri, 23 Jul 2021 00:50:09 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 00:50:10 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 00:50:22 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 00:50:24 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 00:50:26 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 00:50:26 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 00:50:27 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 00:50:27 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 00:50:28 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 00:50:28 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 00:50:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 00:50:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92adf105b957dea8bf29bc48070b2405b28eda07617279f993a0eaa853a0007`  
		Last Modified: Fri, 23 Jul 2021 00:52:21 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09176acdc7608ca00f7179dcfa61731daff1b37c0a9461952d3fd7f1680ee70e`  
		Last Modified: Fri, 23 Jul 2021 00:52:41 GMT  
		Size: 38.8 MB (38841296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed81437b7c4fbc6370edf10594135c396f8847c1d2eab45f5cd48c4a7476a47`  
		Last Modified: Fri, 23 Jul 2021 00:52:21 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8940d06173d9ce4b8caa12f76870ee79b31494d918844a8f08901209fc5a78`  
		Last Modified: Fri, 23 Jul 2021 00:52:21 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29da8c4c89460b607ef0db2c7163906b593b9e29adb0c94d5dc2b9b935f0068`  
		Last Modified: Fri, 23 Jul 2021 00:52:21 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:3ab243a22e89032c573560ba2682aa7fad92a0e86142c3ed5706c48f514af8ea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41738920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ef1d30cb383b4ec553439ee5154aaf85c52a2112827156b93300011252aee9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:25:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 04:19:48 GMT
ARG CONSUL_VERSION=1.9.8
# Fri, 23 Jul 2021 04:19:48 GMT
LABEL org.opencontainers.image.version=1.9.8
# Fri, 23 Jul 2021 04:19:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 04:19:49 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 04:19:54 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 04:19:55 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 04:19:56 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 04:19:56 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 04:19:56 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 04:19:56 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 04:19:56 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 04:19:57 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 04:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 04:19:57 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b35a934ecade634b58bf55698d2b60aee4cec01f90f3a03e09672aea20b72fd`  
		Last Modified: Fri, 23 Jul 2021 04:20:55 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35566cf101e3ccb53cedd918658c3a2ff588b51f2bf4f4cd7ed6815b5bafdd8b`  
		Last Modified: Fri, 23 Jul 2021 04:21:01 GMT  
		Size: 39.0 MB (39023605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d73309e97ec1ff077f4f37791464cb53d50f136398aaf28ab215f221879af03`  
		Last Modified: Fri, 23 Jul 2021 04:20:55 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb22b284bb2cb30fcdecafcb5ea07c8af1795d1c2cbe66f050b4d12ea37425e`  
		Last Modified: Fri, 23 Jul 2021 04:20:55 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf077c858b328a39a43c0f9ed3cbe6bdc4194fa3d62f54ddee67e4fbcbd5c1e`  
		Last Modified: Fri, 23 Jul 2021 04:20:55 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9` - linux; 386

```console
$ docker pull consul@sha256:f5bc15cf6ebec60e3d6758a525f7ee4d50477d08b9167c3a1fcf28d8bfea71f5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45647577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce435b9c74403b9a3f9d9280db1bb93ef80fa3aa7720f4716fe845e27bf79b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 17:39:34 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 04:14:03 GMT
ARG CONSUL_VERSION=1.9.8
# Fri, 23 Jul 2021 04:14:03 GMT
LABEL org.opencontainers.image.version=1.9.8
# Fri, 23 Jul 2021 04:14:03 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 04:14:04 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 04:14:10 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 04:14:12 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 04:14:12 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 04:14:13 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 04:14:13 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 04:14:13 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 04:14:13 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 04:14:13 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 04:14:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 04:14:14 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac8bc78f45d5bfdee6c5832e2e575edd5225f5bebfa97bfc08426a3867940d`  
		Last Modified: Fri, 23 Jul 2021 04:15:22 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f617e76e964196e1147ff2414f5dcee721b70589f400bc81d824f3873519d1`  
		Last Modified: Fri, 23 Jul 2021 04:15:30 GMT  
		Size: 42.8 MB (42825387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed78354304408551df25ff25631b1aeb68cb5e485db6dc41130662cb17b692`  
		Last Modified: Fri, 23 Jul 2021 04:15:22 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e2ee1573f7fe9e0718a7bc6e2b6e3b010d85efc29027d363825da13672f255`  
		Last Modified: Fri, 23 Jul 2021 04:15:22 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35081567dc99f4b239d8f9e70d07d3796dc0fc624a5254ae3d19ded064f0a1cf`  
		Last Modified: Fri, 23 Jul 2021 04:15:22 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:1.9.8`

```console
$ docker pull consul@sha256:9b538a4f12f7a794ca64653ac4ec3e45bfcfe58f46875def350f4bf7937f9cd5
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:1.9.8` - linux; amd64

```console
$ docker pull consul@sha256:3fbc18b4872358beb7d4d865a17065cd84c08afb5dd4056b6240afdc67583f55
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **46.3 MB (46282347 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:62b061e6d43eaa3e1216fd483c362d3839083808590e3d3cbfe0876536731515`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 18:19:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 12:50:15 GMT
ARG CONSUL_VERSION=1.9.8
# Fri, 23 Jul 2021 12:50:16 GMT
LABEL org.opencontainers.image.version=1.9.8
# Fri, 23 Jul 2021 12:50:16 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 12:50:18 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 12:50:26 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 12:50:27 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 12:50:28 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 12:50:28 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 12:50:28 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 12:50:29 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 12:50:29 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 12:50:29 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 12:50:29 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 12:50:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1f76215166e54053f91e087f5a3160cd21a34c6b57813d3a4e2631c8cd127f50`  
		Last Modified: Fri, 23 Jul 2021 12:51:22 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b44e99d3c78a9289b48645fea3c7125101e1ab00b2b7ef496dd9f77a2e64223a`  
		Last Modified: Fri, 23 Jul 2021 12:51:30 GMT  
		Size: 43.5 MB (43467082 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:016a11d5b82044a80cd059e23a0518affdc87ca15281ae4a8518e3103b9574ea`  
		Last Modified: Fri, 23 Jul 2021 12:51:22 GMT  
		Size: 176.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:78844cc5afba4bac56e78565001eaae6315e68605e18aaea429b25956257704a`  
		Last Modified: Fri, 23 Jul 2021 12:51:22 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bc080c1f2f03be33b72e89dc0efb4f689915d0cc4053fec0216d5a19e9ff5076`  
		Last Modified: Fri, 23 Jul 2021 12:51:22 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.8` - linux; arm variant v6

```console
$ docker pull consul@sha256:22194daf3f35cc4686ee999f1fcd82981c23aa0f7162001e0761ae0ac3577455
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.5 MB (41466717 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:f0c7d2796ebb8463c14f4a36e44fa5efdecbb12f4ef51236368989942b5eebba`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Tue, 22 Jun 2021 22:20:06 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 00:50:08 GMT
ARG CONSUL_VERSION=1.9.8
# Fri, 23 Jul 2021 00:50:08 GMT
LABEL org.opencontainers.image.version=1.9.8
# Fri, 23 Jul 2021 00:50:09 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 00:50:10 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 00:50:22 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 00:50:24 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 00:50:26 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 00:50:26 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 00:50:27 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 00:50:27 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 00:50:28 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 00:50:28 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 00:50:28 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 00:50:29 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:f92adf105b957dea8bf29bc48070b2405b28eda07617279f993a0eaa853a0007`  
		Last Modified: Fri, 23 Jul 2021 00:52:21 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09176acdc7608ca00f7179dcfa61731daff1b37c0a9461952d3fd7f1680ee70e`  
		Last Modified: Fri, 23 Jul 2021 00:52:41 GMT  
		Size: 38.8 MB (38841296 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:aed81437b7c4fbc6370edf10594135c396f8847c1d2eab45f5cd48c4a7476a47`  
		Last Modified: Fri, 23 Jul 2021 00:52:21 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fc8940d06173d9ce4b8caa12f76870ee79b31494d918844a8f08901209fc5a78`  
		Last Modified: Fri, 23 Jul 2021 00:52:21 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b29da8c4c89460b607ef0db2c7163906b593b9e29adb0c94d5dc2b9b935f0068`  
		Last Modified: Fri, 23 Jul 2021 00:52:21 GMT  
		Size: 1.7 KB (1707 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.8` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:3ab243a22e89032c573560ba2682aa7fad92a0e86142c3ed5706c48f514af8ea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **41.7 MB (41738920 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:22ef1d30cb383b4ec553439ee5154aaf85c52a2112827156b93300011252aee9`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:25:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 04:19:48 GMT
ARG CONSUL_VERSION=1.9.8
# Fri, 23 Jul 2021 04:19:48 GMT
LABEL org.opencontainers.image.version=1.9.8
# Fri, 23 Jul 2021 04:19:48 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 04:19:49 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 04:19:54 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 04:19:55 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 04:19:56 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 04:19:56 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 04:19:56 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 04:19:56 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 04:19:56 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 04:19:57 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 04:19:57 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 04:19:57 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:0b35a934ecade634b58bf55698d2b60aee4cec01f90f3a03e09672aea20b72fd`  
		Last Modified: Fri, 23 Jul 2021 04:20:55 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35566cf101e3ccb53cedd918658c3a2ff588b51f2bf4f4cd7ed6815b5bafdd8b`  
		Last Modified: Fri, 23 Jul 2021 04:21:01 GMT  
		Size: 39.0 MB (39023605 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5d73309e97ec1ff077f4f37791464cb53d50f136398aaf28ab215f221879af03`  
		Last Modified: Fri, 23 Jul 2021 04:20:55 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:1bb22b284bb2cb30fcdecafcb5ea07c8af1795d1c2cbe66f050b4d12ea37425e`  
		Last Modified: Fri, 23 Jul 2021 04:20:55 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:6cf077c858b328a39a43c0f9ed3cbe6bdc4194fa3d62f54ddee67e4fbcbd5c1e`  
		Last Modified: Fri, 23 Jul 2021 04:20:55 GMT  
		Size: 1.7 KB (1703 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:1.9.8` - linux; 386

```console
$ docker pull consul@sha256:f5bc15cf6ebec60e3d6758a525f7ee4d50477d08b9167c3a1fcf28d8bfea71f5
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **45.6 MB (45647577 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:8ce435b9c74403b9a3f9d9280db1bb93ef80fa3aa7720f4716fe845e27bf79b2`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 17:39:34 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 04:14:03 GMT
ARG CONSUL_VERSION=1.9.8
# Fri, 23 Jul 2021 04:14:03 GMT
LABEL org.opencontainers.image.version=1.9.8
# Fri, 23 Jul 2021 04:14:03 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 04:14:04 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 04:14:10 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 04:14:12 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 04:14:12 GMT
# ARGS: CONSUL_VERSION=1.9.8
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 04:14:13 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 04:14:13 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 04:14:13 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 04:14:13 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 04:14:13 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 04:14:14 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 04:14:14 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:49ac8bc78f45d5bfdee6c5832e2e575edd5225f5bebfa97bfc08426a3867940d`  
		Last Modified: Fri, 23 Jul 2021 04:15:22 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:57f617e76e964196e1147ff2414f5dcee721b70589f400bc81d824f3873519d1`  
		Last Modified: Fri, 23 Jul 2021 04:15:30 GMT  
		Size: 42.8 MB (42825387 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:09ed78354304408551df25ff25631b1aeb68cb5e485db6dc41130662cb17b692`  
		Last Modified: Fri, 23 Jul 2021 04:15:22 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1e2ee1573f7fe9e0718a7bc6e2b6e3b010d85efc29027d363825da13672f255`  
		Last Modified: Fri, 23 Jul 2021 04:15:22 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:35081567dc99f4b239d8f9e70d07d3796dc0fc624a5254ae3d19ded064f0a1cf`  
		Last Modified: Fri, 23 Jul 2021 04:15:22 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

## `consul:latest`

```console
$ docker pull consul@sha256:bccf8b08716e4bba6a36e39ff4659f4dc3d5d8b09f3ef7637d3a74b16ebde1e4
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.list.v2+json`
-	Platforms: 4
	-	linux; amd64
	-	linux; arm variant v6
	-	linux; arm64 variant v8
	-	linux; 386

### `consul:latest` - linux; amd64

```console
$ docker pull consul@sha256:1015ee4f222a938f3dc0e6e34b877670ff7296fabca12da671134b6d7d5995ea
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.6 MB (43616392 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:51f67cdd31f475de3882de8424e6796b404318c4ce3950c85ce4111b193f1a57`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 19:19:39 GMT
ADD file:8ec69d882e7f29f0652d537557160e638168550f738d0d49f90a7ef96bf31787 in / 
# Wed, 14 Apr 2021 19:19:39 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 18:19:29 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 12:49:54 GMT
ARG CONSUL_VERSION=1.10.1
# Fri, 23 Jul 2021 12:49:54 GMT
LABEL org.opencontainers.image.version=1.10.1
# Fri, 23 Jul 2021 12:49:54 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 12:49:56 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 12:50:04 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 12:50:06 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 12:50:07 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 12:50:08 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 12:50:08 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 12:50:08 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 12:50:09 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 12:50:09 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 12:50:10 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 12:50:10 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:540db60ca9383eac9e418f78490994d0af424aab7bf6d0e47ac8ed4e2e9bcbba`  
		Last Modified: Wed, 14 Apr 2021 17:59:29 GMT  
		Size: 2.8 MB (2811969 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:26219d328d3fceaa00722bf08b5b25052b3e0da4c15a6a77e1df9204a732de65`  
		Last Modified: Fri, 23 Jul 2021 12:51:01 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e82ba3ce598354d1d1e9db209d6cefd802bae11112cc179b77cf361e9407c206`  
		Last Modified: Fri, 23 Jul 2021 12:51:07 GMT  
		Size: 40.8 MB (40801130 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:c403ab9c506f25ff589ed067c1f5553eabb4f3ba88f0cd0811b73e3732efcb09`  
		Last Modified: Fri, 23 Jul 2021 12:51:01 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:3262b670efeeb779978bb086dbdc65962fac2f24282d2bc6a93f5456789949f2`  
		Last Modified: Fri, 23 Jul 2021 12:51:01 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:01e27d156c018aa365cae675cafe23837e07e696080fc7f770846623e5afa7eb`  
		Last Modified: Fri, 23 Jul 2021 12:51:01 GMT  
		Size: 1.7 KB (1705 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm variant v6

```console
$ docker pull consul@sha256:3f082cca98db7926582f9515e88bf2a38179feb7fdb0e43be6e75c00179a77cc
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39643432 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:e0034be4ee660d9bf8d533babeb45de88f429ff749a4f9d2f26de431981c9d3f`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 22:57:34 GMT
ADD file:4479f0a51530e039edf231d87201896dcff908aa542a613cdccb015f93dda8a3 in / 
# Tue, 15 Jun 2021 22:57:34 GMT
CMD ["/bin/sh"]
# Tue, 22 Jun 2021 22:20:06 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 00:49:35 GMT
ARG CONSUL_VERSION=1.10.1
# Fri, 23 Jul 2021 00:49:35 GMT
LABEL org.opencontainers.image.version=1.10.1
# Fri, 23 Jul 2021 00:49:36 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 00:49:37 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 00:49:49 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 00:49:51 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 00:49:53 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 00:49:53 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 00:49:54 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 00:49:54 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 00:49:55 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 00:49:55 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 00:49:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 00:49:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:740c950346cf39c85b52576998695c9b909c24a58a8bb1b64cce91fda3ef1d3a`  
		Last Modified: Wed, 14 Apr 2021 18:50:30 GMT  
		Size: 2.6 MB (2622131 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:5cc6805d20d4c45130ef58bfb2cd523ba3651adb7ed2aaad70c3b90d01064e72`  
		Last Modified: Fri, 23 Jul 2021 00:51:45 GMT  
		Size: 1.3 KB (1256 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9383569f273b7844f640f683fe66020085aba3e2aa266e4895a248aadbe1fd5f`  
		Last Modified: Fri, 23 Jul 2021 00:52:04 GMT  
		Size: 37.0 MB (37018011 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ea73ba318055a5182ac6934e8403229cc6797fa9b99233d5f9c01a180c3d82b4`  
		Last Modified: Fri, 23 Jul 2021 00:51:45 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:8a41f8b1035ff81249e1fda4ab3c1e663c24468c7fcef7c0259ae6468fbdc1b0`  
		Last Modified: Fri, 23 Jul 2021 00:51:45 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:eae4c8a9ec3ba9260ff2f6627b889cc8c60f7fdd1742b08557df4ddab6d8a7c8`  
		Last Modified: Fri, 23 Jul 2021 00:51:45 GMT  
		Size: 1.7 KB (1708 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; arm64 variant v8

```console
$ docker pull consul@sha256:0081f4b20a6b484746ee30b2ede4f64241d94721c18b9c115ce61b88ca6588d2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **39.6 MB (39585136 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:945c65b74aabe05fbf0444ae754a6cf8bea788f8854c719189eecb6501793f52`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Tue, 15 Jun 2021 21:45:03 GMT
ADD file:ca9d8b5d1cc2f2186983fc6b9507da6ada5eb92f2b518c06af1128d5396c6f34 in / 
# Tue, 15 Jun 2021 21:45:04 GMT
CMD ["/bin/sh"]
# Tue, 15 Jun 2021 23:25:54 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 04:19:33 GMT
ARG CONSUL_VERSION=1.10.1
# Fri, 23 Jul 2021 04:19:33 GMT
LABEL org.opencontainers.image.version=1.10.1
# Fri, 23 Jul 2021 04:19:34 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 04:19:34 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 04:19:39 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 04:19:40 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 04:19:41 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 04:19:41 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 04:19:41 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 04:19:41 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 04:19:42 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 04:19:42 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 04:19:42 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 04:19:42 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:595b0fe564bb9444ebfe78288079a01ee6d7f666544028d5e96ba610f909ee43`  
		Last Modified: Wed, 14 Apr 2021 18:43:41 GMT  
		Size: 2.7 MB (2712026 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:9ec0bca027d4ed5928a09c462f06be2502d9e6dfd78d9ba3c527dc500cfcdfca`  
		Last Modified: Fri, 23 Jul 2021 04:20:34 GMT  
		Size: 1.3 KB (1260 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:b4b3128d8785d803695d60c92ef9482ab1ddc021eeb844a226ba40208ccb0a54`  
		Last Modified: Fri, 23 Jul 2021 04:20:40 GMT  
		Size: 36.9 MB (36869818 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:ccbf322ffab66a9b685be5eb28cf5499c409303c57282a74d1c3c7380cf2f5f7`  
		Last Modified: Fri, 23 Jul 2021 04:20:34 GMT  
		Size: 174.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:117f3c6fd6c3e6a3b608722cdf776c98efb4d2ab2be357bf99716b7e6f5e8343`  
		Last Modified: Fri, 23 Jul 2021 04:20:34 GMT  
		Size: 154.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:418597e612cf3477bacd0c9730131f6a619802a05c2a5c37081550ec54fc2c60`  
		Last Modified: Fri, 23 Jul 2021 04:20:34 GMT  
		Size: 1.7 KB (1704 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip

### `consul:latest` - linux; 386

```console
$ docker pull consul@sha256:2253be5b7743047f15f8c0109a10e9df6c93331fc5d6d94bda29ec8aabf2e4c2
```

-	Docker Version: 20.10.7
-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **43.0 MB (42993107 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:b78083beb7456bcda3cdb6aeede0c945c374b4aa9b892836e46bab41c72c2eb3`
-	Entrypoint: `["docker-entrypoint.sh"]`
-	Default Command: `["agent","-dev","-client","0.0.0.0"]`

```dockerfile
# Wed, 14 Apr 2021 18:38:29 GMT
ADD file:36634145ad6ec95a6b1a4f8d875f48719357c7a90f9b4906f8ce74f71b28c19d in / 
# Wed, 14 Apr 2021 18:38:29 GMT
CMD ["/bin/sh"]
# Thu, 10 Jun 2021 17:39:34 GMT
LABEL org.opencontainers.image.authors=Consul Team <consul@hashicorp.com>
# Fri, 23 Jul 2021 04:13:44 GMT
ARG CONSUL_VERSION=1.10.1
# Fri, 23 Jul 2021 04:13:44 GMT
LABEL org.opencontainers.image.version=1.10.1
# Fri, 23 Jul 2021 04:13:44 GMT
ENV HASHICORP_RELEASES=https://releases.hashicorp.com
# Fri, 23 Jul 2021 04:13:45 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN addgroup consul &&     adduser -S -G consul consul
# Fri, 23 Jul 2021 04:13:52 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN set -eux &&     apk add --no-cache ca-certificates curl dumb-init gnupg libcap openssl su-exec iputils jq libc6-compat iptables &&     gpg --keyserver keyserver.ubuntu.com --recv-keys C874011F0AB405110D02105534365D9472D7468F &&     mkdir -p /tmp/build &&     cd /tmp/build &&     apkArch="$(apk --print-arch)" &&     case "${apkArch}" in         aarch64) consulArch='arm64' ;;         armhf) consulArch='armhfv6' ;;         x86) consulArch='386' ;;         x86_64) consulArch='amd64' ;;         *) echo >&2 "error: unsupported architecture: ${apkArch} (see ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/)" && exit 1 ;;     esac &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS &&     wget ${HASHICORP_RELEASES}/consul/${CONSUL_VERSION}/consul_${CONSUL_VERSION}_SHA256SUMS.sig &&     gpg --batch --verify consul_${CONSUL_VERSION}_SHA256SUMS.sig consul_${CONSUL_VERSION}_SHA256SUMS &&     grep consul_${CONSUL_VERSION}_linux_${consulArch}.zip consul_${CONSUL_VERSION}_SHA256SUMS | sha256sum -c &&     unzip -d /tmp/build consul_${CONSUL_VERSION}_linux_${consulArch}.zip &&     cp /tmp/build/consul /bin/consul &&     if [ -f /tmp/build/EULA.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/EULA.txt /usr/share/doc/consul/EULA.txt; fi &&     if [ -f /tmp/build/TermsOfEvaluation.txt ]; then mkdir -p /usr/share/doc/consul; mv /tmp/build/TermsOfEvaluation.txt /usr/share/doc/consul/TermsOfEvaluation.txt; fi &&     cd /tmp &&     rm -rf /tmp/build &&     gpgconf --kill all &&     apk del gnupg openssl &&     rm -rf /root/.gnupg &&     consul version
# Fri, 23 Jul 2021 04:13:54 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN mkdir -p /consul/data &&     mkdir -p /consul/config &&     chown -R consul:consul /consul
# Fri, 23 Jul 2021 04:13:55 GMT
# ARGS: CONSUL_VERSION=1.10.1
RUN test -e /etc/nsswitch.conf || echo 'hosts: files dns' > /etc/nsswitch.conf
# Fri, 23 Jul 2021 04:13:55 GMT
VOLUME [/consul/data]
# Fri, 23 Jul 2021 04:13:55 GMT
EXPOSE 8300
# Fri, 23 Jul 2021 04:13:55 GMT
EXPOSE 8301 8301/udp 8302 8302/udp
# Fri, 23 Jul 2021 04:13:56 GMT
EXPOSE 8500 8600 8600/udp
# Fri, 23 Jul 2021 04:13:56 GMT
COPY file:247b557dfc58d59b4f83bd2bd196c7a03ff835064b0d7fef7dfe91b84120ff30 in /usr/local/bin/docker-entrypoint.sh 
# Fri, 23 Jul 2021 04:13:56 GMT
ENTRYPOINT ["docker-entrypoint.sh"]
# Fri, 23 Jul 2021 04:13:56 GMT
CMD ["agent" "-dev" "-client" "0.0.0.0"]
```

-	Layers:
	-	`sha256:31b7e7ccca9e17fd08b39c9a4ffd3ded380b62816c489d6c3758c9bb5a632430`  
		Last Modified: Wed, 14 Apr 2021 18:39:24 GMT  
		Size: 2.8 MB (2818900 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:d1adae4dec86708fea7cb8b325f7ebbcd0ad7a355b0f12baafec74e19df9a4dc`  
		Last Modified: Fri, 23 Jul 2021 04:14:59 GMT  
		Size: 1.3 KB (1258 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:bbfb9688831a6804e0ec0506100817e3550bdb499ad92c471c079f88bfa0a89f`  
		Last Modified: Fri, 23 Jul 2021 04:15:05 GMT  
		Size: 40.2 MB (40170917 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:e976b32b9c325b1e22a08c36e3bdfd3b9dec8c36f46272eb0389cc3d8a809695`  
		Last Modified: Fri, 23 Jul 2021 04:14:59 GMT  
		Size: 173.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:fe31b1e9a61cda7f0af1eafa67a2f6c07229a0135fa0c969f9c4acb45f907eca`  
		Last Modified: Fri, 23 Jul 2021 04:14:59 GMT  
		Size: 153.0 B  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
	-	`sha256:58b946799757bca26ba4264cb8891b48feceaa6c8646856330b320b6d012b491`  
		Last Modified: Fri, 23 Jul 2021 04:14:59 GMT  
		Size: 1.7 KB (1706 bytes)  
		MIME: application/vnd.docker.image.rootfs.diff.tar.gzip
