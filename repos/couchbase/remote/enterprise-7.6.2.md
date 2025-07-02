## `couchbase:enterprise-7.6.2`

```console
$ docker pull couchbase@sha256:52956344aa5f894e127966c6ddb9c88566e7f62f99f774892a4b1daa1a53ad01
```

-	Manifest MIME: `application/vnd.oci.image.index.v1+json`
-	Platforms: 4
	-	linux; amd64
	-	unknown; unknown
	-	linux; arm64 variant v8
	-	unknown; unknown

### `couchbase:enterprise-7.6.2` - linux; amd64

```console
$ docker pull couchbase@sha256:ca8cf49e12246337a3b8147313915822dbfc50fe0a042e175603dc75947c84b0
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **774.4 MB (774351777 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:ced95db906874cae18d89890bea37f4bf27f61bfdf32976e1e5dabaa8f203371`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 29 May 2025 04:20:59 GMT
ARG RELEASE
# Thu, 29 May 2025 04:20:59 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 29 May 2025 04:20:59 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 29 May 2025 04:21:01 GMT
ADD file:598ca0108009b5c2e9e6f4fc4bd19a6bcd604fccb5b9376fac14a75522a5cfa3 in / 
# Thu, 29 May 2025 04:21:01 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:45:24 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:45:24 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:45:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c5697f6f2bfc21bc696f27d86e6f01b92e23ccbd3213e524c910c10d7bcab3fb            ;;          'amd64')            CB_SHA256=05fd37139aab8f3538ddfcf04eec97bd27654a5279468dce79dfad0f605bd784            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:45:24 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:45:24 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:45:24 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:d9d352c11bbd3880007953ed6eec1cbace76898828f3434984a0ca60672fdf5a`  
		Last Modified: Tue, 03 Jun 2025 13:30:18 GMT  
		Size: 29.7 MB (29715337 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d3882126313fe1a25b4825da041ace7b8bc7f7f228a6bf588d2bfb1df9c26a6e`  
		Last Modified: Thu, 12 Jun 2025 22:54:09 GMT  
		Size: 44.5 MB (44462796 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:bf0b40090f76c753c8eb038cc192fd505dcd942fd017c63f9284b488639deabb`  
		Last Modified: Thu, 12 Jun 2025 22:54:07 GMT  
		Size: 877.9 KB (877910 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:46e0be32a665300ca61ed94fbb4d98c09fae2b720fcac15146d4533815ef41fd`  
		Last Modified: Thu, 12 Jun 2025 22:54:07 GMT  
		Size: 3.7 KB (3727 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:5546dc435c89078d16707ace865c3703a6cf5765bb3bf611d51a4c1cd56feb0b`  
		Last Modified: Thu, 12 Jun 2025 23:32:29 GMT  
		Size: 699.3 MB (699288816 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:e0f307ccfdf77152847509050292006e6c2d72069c62bab7be9970c9f3735ed8`  
		Last Modified: Thu, 12 Jun 2025 22:54:08 GMT  
		Size: 186.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:77a16d1afa31985697405cd913acb67158cf5d39ad047b0693f698f310ae31c0`  
		Last Modified: Thu, 12 Jun 2025 22:54:07 GMT  
		Size: 818.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:882d677decc39c0d8272e63c8c284b8d6deef4c3b4575894e24f2ff64914e2eb`  
		Last Modified: Thu, 12 Jun 2025 22:54:08 GMT  
		Size: 848.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:21d83b82cb36dfe0db3592c2903209c0a5d165040c2978a985bdabb3c05a4010`  
		Last Modified: Thu, 12 Jun 2025 22:54:08 GMT  
		Size: 234.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:9c66aeed2ad9a7c37ef2a926d6ee819ef13ed6511bc8ea514b34a2f44de76fd9`  
		Last Modified: Thu, 12 Jun 2025 22:54:09 GMT  
		Size: 217.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:56b27bfad1805a8c209119f1e44b896c0c244c2de1e7e3c7339b1b2450db66de`  
		Last Modified: Thu, 12 Jun 2025 22:54:09 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:02169ee36208c613bf0e0fd62fc043b027417bc7a77cce80c714d71e32b15951
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.6 KB (37565 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:316ded06288cd67d9131d05bed503c06f902304d5ec28bd9bdd5e9c915692e2a`

```dockerfile
```

-	Layers:
	-	`sha256:7b4c1ac3ba72f9ede95c0ff77413394a8c783c768f58fdbf2a827d6919a56531`  
		Last Modified: Thu, 12 Jun 2025 23:32:02 GMT  
		Size: 37.6 KB (37565 bytes)  
		MIME: application/vnd.in-toto+json

### `couchbase:enterprise-7.6.2` - linux; arm64 variant v8

```console
$ docker pull couchbase@sha256:035524182035b5170f65daf765c0f983e360891803542378a52631e2d1297e62
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **746.6 MB (746637168 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:68b8603cc54a44f660ad50302aa8face833a7cb229cda505f6c44404d8b197fd`
-	Entrypoint: `["\/entrypoint.sh"]`
-	Default Command: `["couchbase-server"]`

```dockerfile
# Thu, 12 Jun 2025 11:45:24 GMT
ARG RELEASE
# Thu, 12 Jun 2025 11:45:24 GMT
ARG LAUNCHPAD_BUILD_ARCH
# Thu, 12 Jun 2025 11:45:24 GMT
LABEL org.opencontainers.image.ref.name=ubuntu
# Thu, 12 Jun 2025 11:45:24 GMT
LABEL org.opencontainers.image.version=24.04
# Thu, 12 Jun 2025 11:45:24 GMT
ADD file:d3e5c3c7ed81035a9d3dc27dc9f7b63cca5f6bbbaa499c38e470d52b7e57817d in / 
# Thu, 12 Jun 2025 11:45:24 GMT
CMD ["/bin/bash"]
# Thu, 12 Jun 2025 11:45:24 GMT
LABEL maintainer=docker@couchbase.com
# Thu, 12 Jun 2025 11:45:24 GMT
ARG UPDATE_COMMAND=apt-get update -y -q
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && ${UPDATE_COMMAND}     && apt-get install -y -q wget tzdata       lsof lshw sysstat net-tools numactl bzip2     && ${CLEANUP_COMMAND} # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/*
RUN set -x     && apt-get update     && apt-get install -y gcc git make     && cd /usr/src     && git clone https://github.com/couchbasedeps/runit     && cd runit     && git checkout edb631449d89d5b452a5992c6ffaa1e384fea697     && ./package/compile     && cp ./command/* /sbin/     && apt-get purge -y --autoremove gcc git make     && apt-get clean     && rm -rf /var/lib/apt/lists/* /usr/src/runit # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb
# Thu, 12 Jun 2025 11:45:24 GMT
ARG CB_SKIP_CHECKSUM=false
# Thu, 12 Jun 2025 11:45:24 GMT
ENV PATH=/usr/local/sbin:/usr/local/bin:/usr/sbin:/usr/bin:/sbin:/bin:/opt/couchbase/bin:/opt/couchbase/bin/tools:/opt/couchbase/bin/install
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && if getent group 1000 >/dev/null; then           existing_group=$(getent group 1000 | cut -d: -f1);           groupmod --new-name couchbase "${existing_group}";        else           groupadd -g 1000 couchbase;        fi     && if getent passwd 1000 >/dev/null; then           existing_user=$(getent passwd 1000 | cut -d: -f1);           usermod --login couchbase -d /home/couchbase -m -g couchbase -s /bin/sh "${existing_user}";        else           useradd couchbase -u 1000 -g couchbase -M -s /bin/sh;        fi # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ${UPDATE_COMMAND}     && export INSTALL_DONT_START_SERVER=1     && dpkgArch="$(dpkg --print-architecture)"     && case "${dpkgArch}" in          'arm64')            CB_SHA256=c5697f6f2bfc21bc696f27d86e6f01b92e23ccbd3213e524c910c10d7bcab3fb            ;;          'amd64')            CB_SHA256=05fd37139aab8f3538ddfcf04eec97bd27654a5279468dce79dfad0f605bd784            ;;        esac     && CB_PACKAGE=$(echo ${CB_PACKAGE} | sed -e "s/@@ARCH@@/${dpkgArch}/")     && wget -N --no-verbose $CB_RELEASE_URL/$CB_PACKAGE     && { ${CB_SKIP_CHECKSUM} || echo "$CB_SHA256  $CB_PACKAGE" | sha256sum -c - ; }     && apt-get install -y ./$CB_PACKAGE     && rm -f ./$CB_PACKAGE     && ${CLEANUP_COMMAND}     && rm -rf /tmp/* /var/tmp/* # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN sed -i -e '1 s/$/\/docker/' /opt/couchbase/VARIANT.txt # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
COPY scripts/run /etc/service/couchbase-server/run # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && mkdir -p /etc/service/couchbase-server/supervise     && chown -R couchbase:couchbase                 /etc/service                 /etc/service/couchbase-server/supervise # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
COPY scripts/dummy.sh /usr/local/bin/ # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -x     && ln -s dummy.sh /usr/local/bin/iptables-save     && ln -s dummy.sh /usr/local/bin/lvdisplay     && ln -s dummy.sh /usr/local/bin/vgdisplay     && ln -s dummy.sh /usr/local/bin/pvdisplay # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
# ARGS: UPDATE_COMMAND=apt-get update -y -q CLEANUP_COMMAND=rm -rf /var/lib/apt/lists/* /tmp/* /var/tmp/* CB_RELEASE_URL=https://packages.couchbase.com/releases/7.6.2 CB_PACKAGE=couchbase-server-enterprise_7.6.2-linux_@@ARCH@@.deb CB_SKIP_CHECKSUM=false
RUN set -ex     &&  if [ ! -e /opt/couchbase/bin/curl.real ]; then             ${UPDATE_COMMAND};             apt-get install -y chrpath;             chrpath -r '$ORIGIN/../lib' /opt/couchbase/bin/curl;             apt-get remove -y chrpath;             apt-get autoremove -y;             ${CLEANUP_COMMAND};         fi # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
COPY scripts/entrypoint.sh / # buildkit
# Thu, 12 Jun 2025 11:45:24 GMT
ENTRYPOINT ["/entrypoint.sh"]
# Thu, 12 Jun 2025 11:45:24 GMT
CMD ["couchbase-server"]
# Thu, 12 Jun 2025 11:45:24 GMT
EXPOSE map[11207/tcp:{} 11210/tcp:{} 11280/tcp:{} 18091/tcp:{} 18092/tcp:{} 18093/tcp:{} 18094/tcp:{} 18095/tcp:{} 18096/tcp:{} 18097/tcp:{} 8091/tcp:{} 8092/tcp:{} 8093/tcp:{} 8094/tcp:{} 8095/tcp:{} 8096/tcp:{} 8097/tcp:{} 9123/tcp:{}]
# Thu, 12 Jun 2025 11:45:24 GMT
VOLUME [/opt/couchbase/var]
```

-	Layers:
	-	`sha256:3eff7d219313fd6db206bd90410da1ca5af1ba3e5b71b552381cea789c4c6713`  
		Last Modified: Fri, 20 Jun 2025 09:32:57 GMT  
		Size: 28.9 MB (28856018 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:d7a666f0d75a91d1bdd972442dfd700631ae19f600aec32195844e217e853e94`  
		Last Modified: Wed, 02 Jul 2025 04:40:27 GMT  
		Size: 43.6 MB (43614791 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:1340f0f0e8d481479063852b8f2a2deb3fb25af94716cb5f2ee3520b7b59e1f9`  
		Last Modified: Wed, 02 Jul 2025 04:39:58 GMT  
		Size: 764.6 KB (764615 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:152a85e0722cc65546d09e92af51b162d44255b26933eb3823fdc0c23d770975`  
		Last Modified: Wed, 02 Jul 2025 04:39:58 GMT  
		Size: 3.7 KB (3725 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c28c5e3f90d280649dd46d7299b35365002a3645ca149916e06a357d8de31b19`  
		Last Modified: Wed, 02 Jul 2025 05:32:31 GMT  
		Size: 673.4 MB (673394831 bytes)  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:c1a3319f0eab48581f2181f89b0406bf5317111f286239c84e581a3c1d6983d6`  
		Last Modified: Wed, 02 Jul 2025 04:39:58 GMT  
		Size: 185.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:2a016c75da52f819a15d1ac6cf622ff9e4d7f7be66096014e0df9b3b8bb5624e`  
		Last Modified: Wed, 02 Jul 2025 04:39:58 GMT  
		Size: 817.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:ceade7ff794a4ccc6a7ef8e65d99b73943776a0949a3baebff3fcaf6c65e9960`  
		Last Modified: Wed, 02 Jul 2025 04:39:58 GMT  
		Size: 850.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4822a39339320a0d038d8b7edbf0209fb131d14931ffcd37bb5b6bb218fc7e33`  
		Last Modified: Wed, 02 Jul 2025 04:39:58 GMT  
		Size: 232.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:340f808f9d8174ea325824bb865fe1be30657e817a2a99088309fe2e54297c1a`  
		Last Modified: Wed, 02 Jul 2025 04:39:58 GMT  
		Size: 216.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:4f4fb700ef54461cfa02571ae0db9a0dc1e0cdb5577484a6d75e68dc38e8acc1`  
		Last Modified: Fri, 13 Dec 2024 15:01:47 GMT  
		Size: 32.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip
	-	`sha256:b04c4e9d38a2f88a1da581993d6923900308ee920d92c705c885b5495bcded75`  
		Last Modified: Wed, 02 Jul 2025 04:39:58 GMT  
		Size: 856.0 B  
		MIME: application/vnd.oci.image.layer.v1.tar+gzip

### `couchbase:enterprise-7.6.2` - unknown; unknown

```console
$ docker pull couchbase@sha256:80e100d79bcf21f8828c41b87cc6d45ed6808e54dd6b39a024d0172e74ce2f05
```

-	Manifest MIME: `application/vnd.docker.distribution.manifest.v2+json`
-	Total Size: **37.8 KB (37750 bytes)**  
	(compressed transfer size, not on-disk size)
-	Image ID: `sha256:0c1875700eb73bc8d0c927ef3b0da0d31bd2210cb9dfa9f2d3a392fde97c193f`

```dockerfile
```

-	Layers:
	-	`sha256:5349e0db0e2ef0da07c8d5c991763a0ecbd81818510cf6cd91fbfd9db881f774`  
		Last Modified: Wed, 02 Jul 2025 05:32:11 GMT  
		Size: 37.8 KB (37750 bytes)  
		MIME: application/vnd.in-toto+json
